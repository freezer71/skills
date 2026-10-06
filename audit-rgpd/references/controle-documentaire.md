# Contrôle documentaire

Le RGPD repose sur la **responsabilité** (art. 5.2 et 24) : l'organisme doit pouvoir **démontrer** sa conformité. Lors d'un contrôle sur pièces, la CNIL demande ces documents. Leur absence est un écart en soi, et leur contenu doit correspondre à la réalité observée.

Niveau d'accès requis : 3 (organisation). Sans accès aux documents, tous ces points sont `[À VÉRIFIER]`.

Règle générale : un document **existe**, il est **complet**, il est **à jour**, il est **appliqué**. Vérifier les 4.

## 1. Registre des activités de traitement (art. 30)

- Existe pour l'organisme, et pour son rôle de sous-traitant s'il en a un.
- Chaque fiche contient : finalité, catégories de personnes et de données, destinataires, transferts hors UE, durées, mesures de sécurité.
- Couvre **tous** les traitements de la cartographie. Comparer : un traitement observé mais absent du registre est un écart.
- Exemption de l'art. 30.5 (moins de 250 salariés) : très étroite, car elle ne joue pas pour un traitement non occasionnel. En pratique, presque tout organisme doit tenir un registre.

Gravité par défaut si absent : `[MOYENNE]`, exposition MOYENNE. `[HAUTE]` pour un organisme qui traite des données sensibles ou à grande échelle.

## 2. Analyses d'impact (AIPD, art. 35)

- Identifier les traitements qui exigent une AIPD : liste CNIL des traitements pour lesquels une AIPD est requise, et 9 critères du CEPD (2 critères remplis suffisent en général).
- Vérifier que l'AIPD existe, qu'elle a été faite **avant** le traitement, qu'elle évalue les risques et prévoit des mesures.
- DPO consulté (art. 35.2). Consultation préalable de la CNIL si risque résiduel élevé (art. 36).

Gravité par défaut si absente alors qu'obligatoire : `[HAUTE]`.

## 3. Délégué à la protection des données (art. 37 à 39)

- Obligatoire pour : les organismes publics ; les organismes dont l'activité de base est un suivi régulier et systématique à grande échelle ; ceux qui traitent à grande échelle des données sensibles ou pénales.
- Si désigné : déclaré à la CNIL, coordonnées publiées, sans conflit d'intérêts, avec des moyens.

Gravité par défaut si absent alors qu'obligatoire : `[MOYENNE]`.

## 4. Contrats avec les tiers

- **Sous-traitants** (art. 28) : un contrat par sous-traitant, avec les clauses obligatoires (objet, durée, instructions, confidentialité, sécurité, sous-traitance ultérieure, aide à l'exercice des droits, sort des données en fin de contrat, audits).
- **Responsables conjoints** (art. 26) : accord qui répartit les obligations.
- **Transferts hors UE** : garantie identifiée pour chacun (pays adéquat ou certifié Data Privacy Framework, clauses contractuelles types, règles d'entreprise contraignantes) et analyse d'impact du transfert quand elle est requise.

Comparer avec la liste des tiers de la cartographie. Un tiers sans contrat est un écart.

Gravité par défaut : contrat manquant `[MOYENNE]` ; transfert hors UE sans garantie `[HAUTE]`.

## 5. Information des personnes

- Politique de confidentialité du site (voir `references/controle-site-web.md`, test 6).
- Information des **salariés** et des **candidats** (charte, livret, mention dans les offres).
- Information en cas de **collecte indirecte** (art. 14) : fichiers achetés, données reçues d'un partenaire.

## 6. Procédures

- **Exercice des droits** : procédure écrite, point de contact, délai d'un mois, vérification d'identité proportionnée, registre des demandes. Tester si possible : envoyer une demande d'accès et mesurer la réponse. Le CEPD a mené en 2025 une action coordonnée sur le droit à l'effacement : son rapport final relève surtout l'absence de procédures internes et une information insuffisante.
- **Violations de données** (art. 33 et 34) : procédure de détection et de notification sous 72 h, et **registre des violations** tenu même pour les violations non notifiées.
- **Durées de conservation** : politique écrite par catégorie, et preuve d'application (purges, archivage).
- **Preuves de consentement** : l'organisme peut-il montrer qui a consenti, quand, à quoi (art. 7.1) ?
- **Protection dès la conception** (art. 25) : la conformité est-elle vérifiée avant chaque nouveau projet ?

Gravité par défaut : registre des violations absent `[MOYENNE]` ; impossibilité de prouver les consentements `[HAUTE]` si la prospection en dépend.

## 7. Sécurité et sensibilisation

- Politique de sécurité, gestion des habilitations, revue des accès.
- **Sensibilisation** des personnes qui manipulent des données.
- Charte informatique.

Détails : voir `references/securite.md`.

## Comment demander les documents

Demander en une seule liste, au début de l'audit (voir `assets/questionnaire-cadrage.md`). Pour chaque document reçu, noter sa date et sa version. Un document non fourni après relance est `[À VÉRIFIER]`, avec la mention « non fourni ».

## Sources

- RGPD, art. 5.2, 24 à 39 : https://eur-lex.europa.eu/eli/reg/2016/679/oj
- CNIL, liste des traitements pour lesquels une AIPD est requise : https://www.cnil.fr/fr/liste-traitements-aipd-requise
- CEPD, lignes directrices sur l'AIPD (WP248 rév. 01) : https://ec.europa.eu/newsroom/article29/items/611236
- CNIL, registre des activités de traitement : https://www.cnil.fr/fr/RGPD-le-registre-des-activites-de-traitement
- CEPD, rapport final de l'action coordonnée 2025 sur le droit à l'effacement : https://www.edpb.europa.eu/system/files/2026-02/edpb_cef-report_2025_right-to-erasure_en.pdf
