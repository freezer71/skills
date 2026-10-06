# Auditer un code source ou une infrastructure

Le code dit la vérité que les documents ne disent pas. Un registre peut annoncer « données supprimées après 3 ans » ; le code montre s'il existe une tâche qui supprime vraiment quelque chose. Cette fiche s'applique à tout langage et tout framework : elle raisonne en concepts, et s'appuie sur la lecture du code du projet pour en apprendre les conventions.

Niveau d'accès requis : 2 (code et infrastructure). Lire le code, ne rien exécuter qui vienne du dépôt sans accord.

## 1. Apprendre le projet

Avant de juger, repérer comment le projet :
- **déclare ses structures de données** (schémas, modèles, migrations, définitions de tables ou de collections) ;
- **expose ses points d'entrée** (pages, routes, API, webhooks, tâches planifiées) ;
- **contrôle les droits** (authentification, rôles, vérification que l'utilisateur accède à ses propres données) ;
- **appelle des services tiers** (clients d'API, kits intégrés, scripts chargés dans les pages) ;
- **journalise** (journaux applicatifs, outils de suivi d'erreurs).

Lire un exemple de chaque. C'est la base de comparaison pour la suite.

## 2. Inventorier les données personnelles stockées

Parcourir toutes les structures de données et relever les champs qui concernent une personne :
- identité : nom, prénom, adresse électronique, téléphone, adresse postale, date de naissance ;
- identifiants : adresse IP, identifiant d'appareil, identifiant publicitaire, identifiant de compte ;
- données sensibles ou à risque : santé, opinions, biométrie, localisation précise, numéro de sécurité sociale, données bancaires, pièces d'identité ;
- **champs libres** (commentaire, message, note interne) : ils contiennent souvent ce que personne n'a prévu.

Pour chaque champ, se demander : à quelle finalité sert-il ? Est-il utilisé quelque part ? Un champ collecté mais jamais lu est un écart de **minimisation** (art. 5.1.c).

Produire un schéma en boîtes de texte des structures qui contiennent des données personnelles, en marquant les champs sensibles.

## 3. Vérifier les durées de conservation réelles

- Chercher les **tâches de purge** : suppressions planifiées, expirations automatiques, anonymisation.
- Comparer avec les durées annoncées dans la politique de confidentialité et le registre.
- Vérifier ce que devient un compte **supprimé** : suppression réelle, simple marquage « supprimé », ou rien.
- Ne pas oublier les copies : sauvegardes, fichiers exportés, caches, index de recherche, entrepôts de données, outils tiers synchronisés.

Écart typique : aucune purge, données conservées sans limite. Gravité par défaut `[MOYENNE]`, `[HAUTE]` pour des données sensibles ou un grand volume. C'est l'un des manquements les plus fréquents dans les sanctions de la CNIL.

## 4. Suivre les flux vers les tiers

- Lister chaque service tiers appelé, côté serveur et côté navigateur.
- Pour chacun : quelles données lui sont envoyées ? Le strict nécessaire, ou l'objet complet de l'utilisateur ?
- Vérifier que les scripts tiers des pages ne se chargent **qu'après consentement** quand ils ne sont pas exemptés : chercher la condition qui les active.
- Repérer les envois de données vers des outils d'**IA générative** ou de traduction externes : nouvelle finalité, nouveau destinataire, souvent hors UE.

## 5. Données personnelles dans les journaux

- Les journaux contiennent-ils des adresses électroniques, des mots de passe, des jetons, des numéros de carte, des corps de requête entiers ?
- Les outils de suivi d'erreurs reçoivent-ils des données personnelles (contexte utilisateur, valeurs de formulaire) ?
- Durée de conservation des journaux : la CNIL recommande en général 6 mois à 1 an pour les journaux de sécurité.

Écart typique : mots de passe ou jetons en clair dans les journaux. Gravité par défaut `[CRITIQUE]`.

## 6. Sécurité dans le code

Points à contrôler en lisant (détails dans `references/securite.md`) :

- **Mots de passe** stockés avec une fonction de hachage lente et salée (par exemple bcrypt, scrypt, Argon2 ou PBKDF2). Stockage en clair, réversible ou avec un hachage rapide sans sel : `[CRITIQUE]`.
- **Contrôle d'accès** sur chaque point d'entrée qui renvoie des données personnelles : l'utilisateur ne peut obtenir que ses propres données. Un identifiant qu'on peut changer dans l'URL pour voir le compte d'un autre est un `[CRITIQUE]`.
- **Secrets** (clés d'API, mots de passe de base de données) absents du dépôt et de son historique.
- **Données de test** : pas de vraies données personnelles dans les jeux de test ou les fichiers d'exemple.
- **Chiffrement** des données sensibles au repos, quand la nature des données le justifie.
- **Exports** : les fonctions d'export de fichiers sont réservées aux rôles qui en ont besoin, et journalisées.

## 7. Droits des personnes dans le code

- Existe-t-il un moyen de **supprimer** un compte et toutes ses données, y compris chez les tiers ?
- Existe-t-il un moyen d'**exporter** les données d'une personne (accès, portabilité) ?
- Une **opposition** à la prospection est-elle prise en compte partout (liste d'exclusion partagée) ?

Si tout se fait à la main, le noter : ce n'est pas un écart en soi, mais le délai d'un mois de l'art. 12.3 doit être tenable.

## 8. Infrastructure

Si l'accès le permet :
- **Localisation** des hébergements et des sauvegardes (UE ou non).
- **Accès administrateurs** : authentification forte, comptes nominatifs, revue des droits.
- **Environnements** de test et de préproduction : isolés, non publics, sans vraies données ou avec des données pseudonymisées.
- **Stockages de fichiers** : aucun espace public par défaut.

Tout test actif sur l'infrastructure (analyse de ports, tentative d'accès) exige une autorisation écrite.

## Sources

- RGPD, art. 5.1.c (minimisation), 5.1.e (limitation de la conservation), 25 (protection dès la conception), 32 (sécurité) : https://eur-lex.europa.eu/eli/reg/2016/679/oj
- CNIL, guide RGPD du développeur : https://www.cnil.fr/fr/guide-rgpd-du-developpeur
- CNIL, recommandation sur les mesures de journalisation (2021) : https://www.cnil.fr/fr/la-cnil-publie-une-recommandation-relative-aux-mesures-de-journalisation
- CNIL, guide de la sécurité des données personnelles (2024) : https://www.cnil.fr/fr/guide-de-la-securite-des-donnees-personnelles-nouvelle-edition-2024
