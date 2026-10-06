# Sécurité des données

L'art. 32 du RGPD impose des mesures de sécurité **adaptées au risque**. C'est le premier motif de sanction : la CNIL a annoncé consacrer en 2026 **la moitié** de ses contrôles et de ses actions répressives à la sécurité des données. Plusieurs sanctions lourdes récentes portent sur des mesures élémentaires absentes (mots de passe faibles, absence de chiffrement, accès non journalisés).

Le référentiel est le **guide de la sécurité des données personnelles** de la CNIL (édition mars 2024, 25 fiches en 5 parties). Il distingue les **précautions élémentaires**, attendues de tout organisme, et les mesures renforcées.

## Ce que l'audit contrôle

Pour chaque point : ce qu'on vérifie, et la gravité par défaut si l'écart est constaté.

### Authentification

- Politique de mot de passe conforme à la recommandation CNIL de 2022 (délibération 2022-100). Repères :
  - mot de passe seul : entropie d'au moins 80 bits, par exemple 12 caractères mêlant majuscules, minuscules, chiffres et caractères spéciaux ;
  - avec limitation des tentatives : au moins 50 bits, par exemple 8 caractères mêlant 3 des 4 types ;
  - la CNIL déconseille le renouvellement périodique forcé pour les utilisateurs.
  - Gravité par défaut : `[MOYENNE]`.
- Mots de passe stockés **hachés avec une fonction lente et salée**. Sinon : `[CRITIQUE]`.
- **Authentification forte** (deux facteurs) pour les accès d'administration et les accès à distance. Sinon : `[HAUTE]`.
- Comptes **nominatifs**, pas de compte partagé. Sinon : `[MOYENNE]`.

### Habilitations

- Chacun n'accède qu'aux données nécessaires à sa mission. Revue au moins annuelle des droits.
- Comptes des personnes parties **désactivés**.
- Contrôle d'accès sur chaque point d'entrée : un utilisateur ne peut pas lire les données d'un autre. Sinon : `[CRITIQUE]`.

### Traçabilité

- **Journalisation** des accès et des actions sur les données personnelles, surtout pour les administrateurs.
- Journaux protégés, conservés 6 mois à 1 an en règle générale, sans données sensibles en clair.
- Gravité par défaut si absente : `[MOYENNE]`, `[HAUTE]` pour des données sensibles.

### Chiffrement et transport

- **HTTPS** sur tout le site et toutes les API. Formulaire sans HTTPS : `[HAUTE]`.
- Chiffrement des **sauvegardes** et des supports mobiles (ordinateurs portables, clés).
- Chiffrement au repos des données sensibles.

### Sauvegardes et continuité

- Sauvegardes régulières, stockées à part, testées par une restauration.
- Durée de conservation des sauvegardes définie.

### Prestataires et cloud

- Clauses de sécurité dans les contrats (art. 28.3.c).
- Localisation et réversibilité connues.

### Développement

- Environnements de test séparés, sans données réelles ou avec données pseudonymisées.
- Gestion des secrets hors du code.
- Dépendances maintenues à jour.
- Données réelles dans un environnement de test public : `[CRITIQUE]`.

### API

- Authentification de chaque appel, limitation du débit, réponses limitées aux champs nécessaires (fiche API du guide 2024).

### Postes de travail et nomadisme

- Verrouillage automatique, antivirus, mises à jour, chiffrement des disques des postes nomades.
- Encadrement de l'usage des équipements personnels.

### Violations

- Procédure de gestion des incidents, registre des violations (voir `references/controle-documentaire.md`).

## Ce qu'on ne fait pas sans autorisation écrite

- Tester l'existence de fichiers ou répertoires exposés.
- Tenter une connexion, même avec des identifiants triviaux.
- Analyser les ports ou les vulnérabilités.
- Tenter d'accéder aux données d'un autre compte.

Ces tests relèvent d'un test d'intrusion. Sans autorisation, ils peuvent constituer une atteinte à un système de traitement automatisé de données (art. 323-1 du Code pénal). Les noter dans les limites de l'audit.

## Sources

- RGPD, art. 32 : https://eur-lex.europa.eu/eli/reg/2016/679/oj
- CNIL, guide de la sécurité des données personnelles, édition 2024 : https://www.cnil.fr/fr/guide-de-la-securite-des-donnees-personnelles-nouvelle-edition-2024
- CNIL, recommandation relative aux mots de passe (délibération 2022-100) : https://www.cnil.fr/fr/mots-de-passe-une-nouvelle-recommandation-pour-maitriser-sa-securite
- CNIL, priorités de contrôle 2026 : https://cnil.fr/fr/controles-prioritaires-2026
- Code pénal, art. 323-1 : https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070719
