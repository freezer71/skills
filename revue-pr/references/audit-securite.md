# Audit de sécurité de la PR

L'audit porte sur **toute la PR** : lignes ajoutées, modifiées et supprimées, dans tous les commits. Il part de l'inventaire (voir `references/inventaire-features.md`) : chaque nouveau point d'entrée est examiné en premier, parce que c'est là qu'un attaquant frappera.

Les catégories ci-dessous sont valables pour tout langage et tout framework. Pour chacune, la question est la même : **comment ce projet-ci fait-il cette chose de façon sûre ?** Trouve la manière sûre déjà utilisée dans le dépôt (la fonction de contrôle d'accès, la méthode de requête paramétrée, la fonction d'échappement) et vérifie que la PR l'utilise.

## Méthode : suivre la donnée, de l'entrée à l'effet

Pour chaque point d'entrée ajouté ou modifié :

1. **Qui peut l'appeler ?** Anonyme, utilisateur connecté, rôle précis ? Trouve l'endroit exact du contrôle. « Le bouton n'apparaît que pour les admins » n'est pas un contrôle.
2. **Que reçoit-il ?** Paramètres, corps, en-têtes, cookies, fichiers. Est-ce validé côté serveur (type, format, taille) ?
3. **Où va la donnée ?** Stockage, commande système, chemin de fichier, appel réseau, page affichée, log, réponse. C'est le point d'arrivée qui décide du type de faille possible.
4. **Que renvoie-t-il ?** Plus de champs que nécessaire ? Des données d'autres utilisateurs ? Des messages d'erreur techniques ?

## Les catégories à vérifier

Les noms suivent l'OWASP Top 10 et les identifiants CWE, pour que chaque constat puisse être documenté.

### 1. Contrôle d'accès défaillant

C'est la faille la plus fréquente dans les PR.
- **Authentification manquante** sur un point d'entrée (CWE-306).
- **Accès à la donnée d'un autre** (CWE-639) : la ressource est chargée par son identifiant sans vérifier qu'elle appartient à l'utilisateur ou à son organisation.
- **Élévation de privilèges** (CWE-915) : un champ sensible (rôle, statut d'administrateur, propriétaire, organisation, prix) accepté tel quel depuis la requête. Cherche les données de requête copiées en bloc dans un enregistrement.
- **Contrôle seulement côté client** : élément masqué dans l'interface, mais point d'entrée ouvert.
- **Contrôle seulement à l'entrée générale** : un filtre global qui ne couvre pas le nouveau point d'entrée, ou qui peut être contourné. Le contrôle doit être refait au plus près de la donnée.
- **Contrôle supprimé** par la PR : relis les lignes retirées.

### 2. Injections

Une donnée externe est interprétée comme du code ou une commande.
- **Requête de base de données** construite en assemblant du texte avec une donnée externe (CWE-89, CWE-943). Les requêtes paramétrées et les méthodes standard de l'outil d'accès aux données sont sûres ; leurs variantes « brutes » ou « non sûres » ne le sont pas.
- **Commande système** construite avec une donnée externe (CWE-78).
- **Chemin de fichier** construit avec une donnée externe, sans vérifier qu'il reste dans le dossier prévu (CWE-22).
- **Évaluation de code ou désérialisation** d'une donnée externe (CWE-94, CWE-502).
- **Contenu affiché sans échappement** (CWE-79) : texte d'utilisateur inséré comme HTML ou script dans une page, lien dont le schéma n'est pas contrôlé.
- **Instructions données à une IA** : texte externe passé à un modèle qui a accès à des outils ou à des données d'autres utilisateurs.

### 3. Requêtes sortantes et redirections

- **Le serveur appelle une adresse fournie par l'utilisateur** (CWE-918) : risque d'accès au réseau interne. Il faut une liste des destinations autorisées, pas une liste des interdites.
- **Redirection vers une adresse fournie par l'utilisateur** (CWE-601) sans vérifier qu'elle reste interne.

### 4. Secrets et cryptographie

- **Secret écrit dans le code ou dans un fichier commité** (CWE-798) : clé d'API, mot de passe, jeton, clé privée.
- **Secret visible côté client** : paramètre secret envoyé au navigateur ou embarqué dans l'application.
- **Mot de passe mal protégé** (CWE-916) : haché avec un algorithme rapide au lieu d'un algorithme fait pour les mots de passe (bcrypt, scrypt, Argon2).
- **Aléa prévisible** pour un jeton ou un code (CWE-338).
- **Comparaison de secret qui n'est pas en temps constant.**
- **Jeton signé mal vérifié** : signature non vérifiée, algorithme non imposé, secret faible.

### 5. Authentification et sessions

- Cookies de session sans les protections standard (inaccessible au script, transmis seulement en HTTPS, limité au même site).
- Lien de réinitialisation ou de connexion sans expiration, réutilisable ou prévisible.
- Pas de limitation du nombre d'essais sur connexion, inscription, réinitialisation ou envoi de code.
- Messages qui révèlent si un compte existe.
- Action qui modifie des données sans protection contre les requêtes forgées depuis un autre site (CWE-352).

### 6. Appels entrants de services tiers

Un service tiers qui notifie le système (paiement, dépôt de code, email) doit être **authentifié par sa signature** avant tout traitement ; sinon n'importe qui peut simuler l'événement. Vérifier aussi qu'un même événement reçu deux fois n'est pas traité deux fois.

### 7. Fichiers envoyés par les utilisateurs

Type vérifié côté serveur sur le contenu (pas seulement sur l'extension), taille limitée, nom régénéré, stockage où le fichier ne peut pas être exécuté. Les formats qui peuvent contenir du script (images vectorielles, HTML) sont traités comme dangereux.

### 8. Exposition de données

- Réponse qui renvoie l'enregistrement complet (avec mot de passe haché, jetons, champs internes) au lieu des seuls champs utiles.
- Données personnelles écrites dans les logs, envoyées à un outil de mesure d'audience ou à une IA tierce.
- Erreurs techniques détaillées renvoyées au client.
- Réponse propre à un utilisateur mise en cache et servie à un autre.
- Nouvelles données personnelles collectées sans utilité claire ni durée de conservation : le signaler et renvoyer au skill `rgpd`.

### 9. Configuration

Partage entre origines ouvert à tous, politique de sécurité du contenu affaiblie, mode de débogage ou accès de test laissés actifs, vérification des certificats désactivée, droits de l'intégration continue élargis, code d'une contribution externe exécuté avec accès aux secrets.

### 10. Dépendances

- Pour chaque dépendance ajoutée : est-elle connue et maintenue, son nom est-il exact (une faute de frappe peut cacher un paquet malveillant), exécute-t-elle un script à l'installation ?
- Si un outil d'audit des dépendances est déjà installé, lance-le en lecture seule sur la version de la PR et ne retiens que ce qui concerne les dépendances ajoutées ou mises à jour.
- Version d'un composant visée par un avis de sécurité connu : le mentionner avec le lien de l'avis.

### 11. Disponibilité et coûts

Lecture sans limite (pas de pagination), boucle sur une donnée externe sans plafond, expression régulière qui peut tourner très longtemps (CWE-1333), traitement de fichier sans taille maximale, appel à un service payant déclenchable sans limite par un anonyme, requêtes répétées en boucle par le client. Un point d'entrée qui peut faire exploser la facture est une faille.

## Échelle de gravité

| Gravité | Critère | Effet |
|---|---|---|
| CRITIQUE | Exploitable sans compte ou avec un compte ordinaire ; accès aux données des autres, à l'administration, à l'exécution de code, ou secret de production exposé | Bloque |
| HAUTE | Exploitable sous condition (rôle, action de la victime) ou impact limité mais sensible | Bloque |
| MOYENNE | Affaiblit une défense, sans faille directe démontrée | À corriger |
| BASSE | Bonne pratique non suivie, risque théorique | Suggestion |
| À VÉRIFIER | Plausible, mais dépend d'un élément non lisible (configuration hors dépôt, service externe) | Dire quoi vérifier |

## Écrire un constat

Chaque faille est un bloc séparé, toujours avec les mêmes libellés dans le même ordre (voir `assets/modele-rapport.md`, partie 3) :

- **Titre** : le numéro, la gravité entre crochets, puis le problème en mots simples. « Faille 1 [CRITIQUE] — Un utilisateur peut lire les factures des autres. »
- **Où :** `fichier:ligne`.
- **Problème :** ce qui manque ou ce qui est faux, en 1 phrase.
- **Risque :** ce qu'un attaquant fait et ce qu'il obtient, en 1 ou 2 phrases. Le nom technique et la CWE viennent ici entre parenthèses, une seule fois.
- **Correction :** le changement à faire, en 1 phrase, avec un court extrait de code si c'est plus clair.

## Sources

- [OWASP Top 10](https://owasp.org/Top10/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org)
- [OWASP ASVS](https://owasp.org/www-project-application-security-verification-standard/)
- [CWE — Common Weakness Enumeration](https://cwe.mitre.org)
- [CWE Top 25 Most Dangerous Software Weaknesses](https://cwe.mitre.org/top25/)
