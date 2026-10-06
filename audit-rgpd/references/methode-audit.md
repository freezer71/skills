# Méthode d'audit RGPD

Un audit RGPD compare **ce qui se passe réellement** à **ce que le droit exige**, puis mesure l'écart et le risque. Il ne se contente pas de vérifier que des documents existent : un registre parfait ne sert à rien si le site dépose des traceurs publicitaires avant tout consentement.

La démarche reconnue tient en 6 phases. Elle reprend les étapes décrites par la CNIL pour la mise en conformité (cartographier, prioriser, gérer les risques, organiser, documenter) et les principes d'audit de la norme ISO 19011.

## Les principes d'un bon audit

Ces principes viennent de la norme ISO 19011. Ils distinguent un audit d'une simple relecture.

- **Approche fondée sur la preuve.** Une conclusion repose sur une preuve vérifiable : observation, document, enregistrement, réponse tracée. Une impression n'est pas une preuve.
- **Indépendance et objectivité.** L'auditeur ne juge pas son propre travail. Si tu audites un projet que tu as aidé à écrire dans la même conversation, le dire dans le rapport.
- **Présentation impartiale.** Rapporter aussi ce qui est conforme et ce qui n'a pas pu être vérifié. Un rapport qui ne contient que des écarts n'est pas plus sérieux, il est incomplet.
- **Approche par les risques.** Passer plus de temps là où le risque pour les personnes est le plus fort : données sensibles, mineurs, volume, exposition publique.
- **Confidentialité.** Les preuves collectées (captures, extraits, données) restent dans le périmètre de l'audit. Ne jamais recopier de données personnelles réelles dans le rapport : les masquer (`j***@exemple.fr`).

## Phase 1 — Cadrage

But : savoir **quoi** auditer, **pourquoi**, et **avec quels accès**.

- Définir le **périmètre** : quels domaines, applications, outils, entités, pays.
- Définir l'**objectif** : état des lieux, préparation d'un contrôle, due diligence, suivi d'un audit précédent.
- Recenser les **accès** : site public seul ; code source ; documents (registre, contrats) ; entretiens ; accès aux outils (CRM, emailing).
- Obtenir les **autorisations** : tout test actif sur un système exige l'accord écrit de son responsable.
- Fixer la **date de référence** de l'audit : les constats valent à cette date.

Questions prêtes : voir `assets/questionnaire-cadrage.md`.

Niveaux d'accès et ce qu'ils permettent :

- **Niveau 1 — Public.** Contrôle en ligne du site et des applications, comme un visiteur. Couvre traceurs, bandeau, information, formulaires, sécurité visible.
- **Niveau 2 — Code et infrastructure.** Ajoute les données stockées, les durées réelles, les journaux, les tiers appelés côté serveur, les secrets, la sécurité interne.
- **Niveau 3 — Organisation.** Ajoute les documents, les contrats, les procédures, les entretiens. Seul ce niveau permet de conclure sur la gouvernance.

Le rapport indique toujours le niveau atteint. Un audit de niveau 1 ne conclut pas sur le registre ou les contrats : ces points sont `[À VÉRIFIER]`.

## Phase 2 — Cartographie

But : trouver **tout** ce qui traite des données personnelles dans le périmètre. Un traitement oublié est un risque non audité.

- Inventorier les composants : sites, sous-domaines, applications, API, back-offices, outils SaaS.
- Pour chaque composant : quelles données, sur qui, pour quoi, stockées où, partagées avec qui, pendant combien de temps.
- Dessiner les **flux** : de la collecte jusqu'à la suppression, en passant par chaque tiers.

Méthode détaillée : voir `references/cartographie-ecosysteme.md`.

## Phase 3 — Collecte des preuves

Trois sources, à croiser :

- **Observation** : ce que l'on voit soi-même (requêtes réseau, traceurs, pages, code). Poids le plus fort.
- **Documents** : registre, AIPD, contrats, politiques, procédures (voir `references/controle-documentaire.md`).
- **Déclarations** : réponses de l'organisme. Poids le plus faible tant qu'elles ne sont pas confirmées par une observation ou un document.

Pour chaque preuve, noter :
- la **source** (URL, fichier et ligne, document et page) ;
- la **date et l'heure** de l'observation ;
- les **conditions** (navigateur vierge, avant consentement, après refus…).

Une preuve qui ne peut pas être refaite par un tiers est une preuve faible.

### Échantillonnage

Un site de 5 000 pages ne s'audite pas page par page. Choisir un **échantillon raisonné** :
- la page d'accueil ;
- chaque **gabarit** de page distinct (article, fiche produit, liste, recherche) ;
- chaque page qui **collecte** des données (formulaires, inscription, connexion, panier, paiement, contact, candidature) ;
- les pages légales (mentions, politique, cookies) ;
- l'espace connecté si l'accès est autorisé.

Écrire l'échantillon dans le rapport. Un écart trouvé sur un gabarit vaut pour toutes les pages de ce gabarit.

## Phase 4 — Analyse d'écart

Parcourir `assets/grille-audit.md` point par point. Chaque point reçoit un statut :

- `CONFORME` : exigence remplie, preuve à l'appui.
- `ÉCART` : exigence non remplie, preuve à l'appui.
- `À VÉRIFIER` : impossible de trancher avec les accès disponibles. Dire ce qui manque.
- `HORS PÉRIMÈTRE` : le point ne s'applique pas (par exemple, aucun transfert hors UE). Dire pourquoi.

Ne pas sauter un point parce qu'il « ne semble pas concerné » : le noter `HORS PÉRIMÈTRE` avec sa raison. C'est ce qui rend l'audit exhaustif et vérifiable.

## Phase 5 — Cotation

Chaque écart reçoit un niveau de gravité. Méthode : voir `references/cotation-risques.md`.

Regrouper les écarts qui ont **la même cause** : 12 traceurs déposés sans consentement par le même gestionnaire de balises forment 1 risque, avec 12 preuves.

## Phase 6 — Restitution et suivi

- Rédiger le rapport selon `assets/modele-rapport.md`.
- Classer les risques **par gravité**, pas par domaine.
- Pour chaque risque : une correction concrète et un délai.
- Proposer un **audit de suivi** : vérifier que les corrections `[CRITIQUE]` et `[HAUTE]` sont effectives, avec les mêmes tests que la première fois.

Rythme conseillé : audit complet une fois par an ; contrôle des zones à fort risque à chaque évolution importante (nouvel outil, nouveau formulaire, nouveau prestataire, refonte du site).

## Sources

- CNIL, « RGPD : passer à l'action » (les étapes de mise en conformité) : https://www.cnil.fr/fr/rgpd-passer-a-laction
- CNIL, guide de sensibilisation au RGPD pour les PME : https://www.cnil.fr/fr/la-cnil-et-bpifrance-sassocient-pour-accompagner-les-tpe-et-pme-dans-leur-appropriation-du-reglement
- ISO 19011:2018, lignes directrices pour l'audit des systèmes de management : https://www.iso.org/standard/70017.html
- RGPD, art. 5.2 (responsabilité, « accountability ») et art. 24 : https://eur-lex.europa.eu/eli/reg/2016/679/oj
