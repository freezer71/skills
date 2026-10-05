# RGPD × AI Act — Articulation Intelligence Artificielle

L'**AI Act** (règlement (UE) 2024/1689, ou RIA) est entré en vigueur le **1er août 2024** et s'applique par étapes jusqu'en 2028, voire 2030 pour certains systèmes existants. Son calendrier a été **modifié par le règlement (UE) 2026/1744 « Digital Omnibus sur l'IA »**, publié au JOUE le 24 juillet 2026 et en vigueur depuis le **27 juillet 2026** : les obligations « haut risque » ne s'appliquent plus au 2 août 2026 (voir le calendrier ci-dessous).

L'AI Act ne remplace pas le RGPD : il s'applique « sans préjudice » du droit de la protection des données (art. 2.7 RIA). Les deux régimes s'appliquent **simultanément** dès qu'un système d'IA traite des données personnelles.

## Logique différente, application conjointe

| | RGPD | AI Act |
|---|---|---|
| Objet | Protection des **données personnelles** | Encadrement des **systèmes et modèles d'IA** (sécurité des produits + droits fondamentaux) |
| Logique | Droits des personnes, responsabilité du responsable de traitement | Classification par le **risque du système**, obligations par rôle (fournisseur, déployeur, importateur, distributeur) |
| Périmètre | Tout traitement de données personnelles | Tout système d'IA mis sur le marché, mis en service ou utilisé dans l'UE ; modèles d'IA à usage général (GPAI) |
| Autorité | CNIL (France), CEPD/EDPB | Bureau de l'IA (Commission) pour les modèles GPAI + autorités nationales de surveillance du marché |

**Si une IA traite des données personnelles** (CV, photos, comportements, voix…), **les deux** régimes s'appliquent. Vérifie toujours les deux grilles : un système « à risque minimal » au sens de l'AI Act peut exiger une AIPD au sens du RGPD.

## Classification AI Act par niveau de risque

### Risque inacceptable (interdiction — art. 5)
Applicables depuis le **2 février 2025** :
- **Manipulation** subliminale ou délibérément trompeuse et **exploitation des vulnérabilités** (âge, handicap, situation sociale ou économique) — art. 5.1.a et b ;
- **Notation sociale** (social scoring) — art. 5.1.c ;
- **Évaluation du risque d'infraction** d'une personne fondée uniquement sur le profilage ou ses traits de personnalité — art. 5.1.d ;
- **Moissonnage non ciblé d'images faciales** (internet, vidéosurveillance) pour constituer des bases de reconnaissance faciale — art. 5.1.e ;
- **Reconnaissance des émotions** sur le lieu de travail et dans les établissements d'enseignement (sauf raisons médicales ou de sécurité) — art. 5.1.f ;
- **Catégorisation biométrique** déduisant race, opinions politiques, appartenance syndicale, convictions, vie sexuelle ou orientation sexuelle — art. 5.1.g ;
- **Identification biométrique à distance « en temps réel »** dans les espaces accessibles au public à des fins répressives (exceptions étroites et autorisation préalable) — art. 5.1.h.

Ajoutées par le règlement 2026/1744, applicables à partir du **2 décembre 2026** :
- Systèmes générant ou manipulant des **images intimes réalistes** d'une personne identifiable sans son consentement libre, spécifique, éclairé, univoque et explicite (« deepfakes » sexuels, applications de « nudification ») — art. 5.1.ba ;
- Systèmes générant ou manipulant des **contenus pédopornographiques** — art. 5.1.bb.

Ces traitements sont aussi presque toujours **illicites au regard du RGPD** (art. 9 sur les données sensibles, art. 22 sur les décisions automatisées, art. 5.1.a sur la loyauté). Pour interpréter l'art. 5, appuie-toi sur les **lignes directrices de la Commission sur les pratiques interdites** (février 2025), non contraignantes mais suivies par les autorités.

### Haut risque (chapitre III, art. 6 et annexes I et III)
Deux familles :
- **Annexe I** : IA composant de sécurité d'un produit déjà réglementé (machines, jouets, dispositifs médicaux, ascenseurs…) ;
- **Annexe III** : usages autonomes dans les domaines suivants :
  - biométrie (identification à distance, catégorisation, reconnaissance des émotions hors cas interdits) ;
  - infrastructures critiques ;
  - éducation et formation professionnelle (admission, notation, surveillance des examens) ;
  - emploi et gestion des travailleurs (recrutement, tri de CV, évaluation, promotion, licenciement) ;
  - accès aux services essentiels (prestations publiques, **solvabilité et crédit**, **tarification d'assurance vie et santé**, tri des appels d'urgence) ;
  - activités répressives ;
  - migration, asile, contrôle aux frontières ;
  - administration de la justice et processus démocratiques.

Un système de l'annexe III peut échapper à la qualification s'il ne présente pas de risque important (tâche procédurale étroite, simple amélioration d'une activité humaine…), **sauf s'il effectue du profilage** de personnes physiques (art. 6.3). Le fournisseur doit alors documenter son analyse ; le règlement 2026/1744 a allégé les informations à enregistrer dans ce cas.

**Obligations du fournisseur (art. 8 à 17)** :
- Système de gestion des risques (art. 9) ;
- Gouvernance des données : qualité, représentativité, examen des biais (art. 10) ;
- Documentation technique détaillée (art. 11) ;
- Journalisation automatique (art. 12) ;
- Transparence et notice d'utilisation pour les déployeurs (art. 13) ;
- Contrôle humain effectif (art. 14) ;
- Exactitude, robustesse, cybersécurité (art. 15) ;
- Système de management de la qualité (art. 17), **évaluation de conformité**, marquage CE et enregistrement dans la base de données de l'UE (art. 43, 48, 49).

**Obligations du déployeur (art. 26 et 27)** : utiliser le système conformément à la notice, assurer un contrôle humain compétent, conserver les journaux, **informer les salariés** avant la mise en service sur le lieu de travail, informer les personnes faisant l'objet de décisions ; pour les organismes publics et certains déployeurs privés (crédit, assurance), réaliser une **analyse d'impact sur les droits fondamentaux** (FRIA, art. 27).

**Articulation avec le RGPD** :
- L'**AIPD** (art. 35 RGPD) reste requise et le déployeur utilise les informations de la notice (art. 13 RIA) pour la réaliser (art. 26.9 RIA). La FRIA complète l'AIPD sans la remplacer (art. 27.4 RIA).
- Toute personne visée par une décision fondée sur un système à haut risque de l'annexe III a droit à une **explication** du rôle du système (art. 86 RIA), en plus des art. 13 à 15 et 22 RGPD.

**Date d'application** : **2 décembre 2027** pour l'annexe III et **2 août 2028** pour l'annexe I (règlement 2026/1744). Ne repousse pas pour autant la préparation : les obligations RGPD (AIPD, art. 22, information) s'appliquent déjà.

### Risque de transparence (chapitre IV, art. 50)
Applicable depuis le **2 août 2026** :
- Systèmes interagissant avec des personnes (chatbots) : **informer** qu'on interagit avec une IA, sauf évidence ;
- Contenus synthétiques (audio, image, vidéo, texte) : **marquage lisible par machine** par le fournisseur. Pour les systèmes mis sur le marché avant le 2 août 2026, le règlement 2026/1744 accorde un délai jusqu'au **2 décembre 2026** ;
- **Hypertrucages** (deepfakes) et textes publiés pour informer le public sur des sujets d'intérêt général : **étiquetage** par le déployeur ;
- Reconnaissance des émotions et catégorisation biométrique (hors cas interdits) : **information** des personnes exposées, en plus du RGPD.

La Commission a publié un **code de bonnes pratiques sur le marquage et l'étiquetage des contenus générés par IA** (août 2026), outil volontaire pour démontrer la conformité à l'art. 50.

### Risque minimal
Reste du marché. Pas d'obligation spécifique AI Act hors **maîtrise de l'IA** (art. 4), mais le RGPD s'applique pleinement si des données personnelles sont traitées.

### Maîtrise de l'IA (art. 4)
Depuis le 2 février 2025, fournisseurs et déployeurs doivent former leur personnel. Le règlement 2026/1744 a transformé cette exigence en **obligation de moyens** : prendre des mesures pour favoriser un niveau suffisant de maîtrise de l'IA, sans garantir un niveau donné pour chaque personne. Documente quand même les formations : c'est aussi une mesure organisationnelle au sens de l'art. 32 RGPD.

## Modèles d'IA à usage général (GPAI, chapitre V)

Régime spécifique pour les **modèles à usage général** (GPT, Claude, Gemini, Llama, Mistral…), applicable depuis le **2 août 2025** :
- Documentation technique pour le Bureau de l'IA et pour les fournisseurs en aval (art. 53) ;
- Politique de respect du **droit d'auteur**, y compris des réserves de droits (« opt-out » TDM) ;
- **Résumé public des données d'entraînement** selon le modèle publié par la Commission (juillet 2025) ;
- Obligations renforcées pour les modèles **à risque systémique** (présomption au-delà de 10²⁵ FLOP d'entraînement, art. 51) : évaluations, tests adversariaux, atténuation des risques, notification des incidents graves, cybersécurité (art. 55).

**Outils de référence** :
- **Code de bonnes pratiques GPAI** (juillet 2025), volontaire, en trois chapitres (transparence, droit d'auteur, sûreté et sécurité). L'adhérer facilite la démonstration de conformité ;
- **Lignes directrices de la Commission sur le champ des obligations GPAI** (juillet 2025).

**Calendrier** : les modèles mis sur le marché avant le 2 août 2025 ont jusqu'au **2 août 2027** pour se conformer (art. 111.3). Les pouvoirs de sanction de la Commission envers les fournisseurs GPAI (art. 101) s'exercent à partir du 2 août 2026. Le règlement 2026/1744 a aussi renforcé la compétence exclusive du Bureau de l'IA pour les systèmes fondés sur un modèle GPAI du même fournisseur et pour l'IA intégrée aux très grandes plateformes (art. 75 modifié).

**Côté RGPD**, un fournisseur de modèle reste responsable de traitement pour l'entraînement : base légale, information, droits, sécurité (voir ci-dessous et `references/bases-legales.md`).

## Points d'articulation pratiques RGPD × IA

### Statut du modèle : un modèle d'IA contient-il des données personnelles ?
L'**avis 28/2024 du CEPD** (17 décembre 2024) pose la grille de lecture :
- Un modèle entraîné sur des données personnelles **n'est pas automatiquement anonyme**. Il ne l'est que si la probabilité d'extraire des données des personnes ayant servi à l'entraînement (directement ou par requêtes) est **insignifiante**, ce que le responsable doit démontrer et documenter.
- Si le modèle n'est pas anonyme, le RGPD s'applique à son stockage, à sa diffusion et à son utilisation.
- Un entraînement **illicite** peut affecter la licéité du déploiement ultérieur, selon que le déployeur a vérifié ou non l'origine du modèle.

La CNIL a décliné cet avis dans sa fiche sur l'**applicabilité du RGPD aux modèles** (juillet 2025) : documenter l'analyse (tests de régurgitation, attaques d'inférence d'appartenance) et, à défaut d'anonymat, encapsuler le modèle dans un système doté de **filtres robustes** en sortie.

### Données d'entraînement
- **Source des données** : moissonnage du web (web scraping), jeux de données publics, données des utilisateurs ?
- **Base légale RGPD** : l'**intérêt légitime** (art. 6.1.f) est la base la plus souvent mobilisable, sous réserve du test en trois étapes (intérêt, nécessité, mise en balance). L'avis 28/2024 du CEPD et les recommandations CNIL de juin 2025 l'admettent avec des **garanties fortes** : exclusion de catégories de données ou de sites, respect des refus de collecte (robots.txt, ai.txt), minimisation, pseudonymisation, information renforcée, **droit d'opposition facilité** (y compris préalable à l'entraînement).
- **Données sensibles** dans le corpus : l'intérêt légitime ne suffit pas, il faut aussi une exception de l'art. 9.2 (voir `references/donnees-sensibles.md`). Filtre-les en amont autant que possible.
- **Réutilisation des données de ses propres utilisateurs** pour entraîner un modèle : nouvelle finalité, à analyser via le test de compatibilité (art. 6.4) ; information préalable et droit d'opposition effectif indispensables.

### Détection et correction des biais (art. 4a RIA)
Le règlement 2026/1744 a déplacé l'ancien art. 10.5 vers un **nouvel art. 4a**, applicable depuis le 27 juillet 2026 :
- Les **fournisseurs de systèmes à haut risque** peuvent, à titre exceptionnel et **dans la mesure strictement nécessaire**, traiter des données sensibles (art. 9.1 RGPD) pour détecter et corriger les biais ;
- Cette faculté est **étendue** aux déployeurs de systèmes à haut risque et aux fournisseurs et déployeurs d'autres systèmes et modèles, lorsque le biais est susceptible d'affecter la santé, la sécurité ou les droits fondamentaux, ou de conduire à une discrimination interdite ;
- Conditions cumulatives : impossibilité d'atteindre l'objectif avec d'autres données (synthétiques, anonymisées), limitations techniques à la réutilisation, sécurité et pseudonymisation à l'état de l'art, accès strictement contrôlé et documenté, **aucune transmission à des tiers**, effacement une fois le biais corrigé, justification de la stricte nécessité dans le **registre des traitements**.

C'est une base d'**intérêt public important** au sens de l'art. 9.2.g RGPD : elle ne dispense ni d'une base de l'art. 6, ni de l'AIPD.

### Information des personnes
- Si le modèle est entraîné sur des données collectées indirectement : information **art. 14**. L'exception d'effort disproportionné (art. 14.5.b) ne dispense pas d'une **information générale** accessible (site web, liste des sources).
- Si décision automatisée : information **art. 13.2.f / 14.2.g** sur la logique sous-jacente et les conséquences ; plus l'information de l'art. 50 RIA et, pour le haut risque, l'art. 26.11 et l'art. 86 RIA.

### Droits d'accès, d'effacement et d'opposition face à un modèle
- Un modèle peut « mémoriser » des données sans les stocker explicitement.
- Selon la CNIL (recommandations de février 2025), le responsable doit pouvoir répondre aux droits sur les **jeux de données** et, si le modèle n'est pas anonyme, sur le **modèle** : ré-entraînement périodique intégrant les demandes d'effacement, **filtres en sortie**, techniques de désapprentissage (machine unlearning) encore immatures. La CNIL admet une réponse proportionnée au coût et à l'état de l'art, à condition d'être documentée.

### Décisions automatisées (art. 22 RGPD)
- Une décision **exclusivement** automatisée produisant des effets juridiques ou significatifs est **interdite sauf** consentement explicite, nécessité contractuelle ou autorisation légale, avec garanties (intervention humaine, droit d'exprimer son point de vue et de contester).
- La CJUE retient une conception large : le calcul d'un score déterminant pour la décision d'un tiers est déjà une décision au sens de l'art. 22 (CJUE, 7 décembre 2023, SCHUFA, C-634/21). Le droit d'accès inclut une **explication compréhensible** de la procédure et des principes appliqués (CJUE, 27 février 2025, Dun & Bradstreet Austria, C-203/22).
- Avec l'AI Act haut risque : ajoute un **contrôle humain effectif** (art. 14 et 26 RIA), pas une simple validation cosmétique.

### Biais et discrimination
- RGPD : art. 5.1.a (loyauté), art. 9 (données sensibles), art. 22 (décisions automatisées).
- AI Act : qualité et représentativité des données (art. 10), traitement des données sensibles pour corriger les biais (art. 4a).

### Sécurité
- RGPD art. 32 : mesures appropriées.
- AI Act haut risque (art. 15) : résistance aux attaques d'évasion, d'empoisonnement des données, d'extraction de modèle, d'inversion.
- Fiche CNIL **sécurité du développement** (juillet 2025) et projet **PANAME** (CNIL, ANSSI, PEReN, PEPR iPoP) d'outillage pour tester si un modèle laisse fuiter des données personnelles.

## Recommandations CNIL sur l'IA (2024-2026)

Ce sont des recommandations, pas du droit dur, mais la CNIL s'y réfère en contrôle. Elles couvrent le **développement** des systèmes d'IA :
1. Déterminer le régime juridique applicable et définir une finalité (2024).
2. Qualifier les acteurs (responsable, sous-traitant) et choisir la base légale (2024).
3. Réaliser l'AIPD pour les systèmes d'IA (2024).
4. Concevoir le système et constituer la base de données d'entraînement : minimisation, durées de conservation (2024).
5. **Informer les personnes** et **faciliter l'exercice des droits** (février 2025).
6. **Intérêt légitime**, avec une fiche dédiée au **moissonnage** (juin 2025).
7. **Applicabilité du RGPD aux modèles**, **annotation** des données, **sécurité** du développement (juillet 2025), ce qui finalise la série.

Travaux annoncés ou en cours : responsabilités le long de la chaîne de valeur, recommandations sectorielles (éducation, emploi) et, en santé, un guide **HAS-CNIL** sur l'usage de l'IA en contexte de soins (consultation publique close en avril 2026). Vérifie sur cnil.fr la version en vigueur avant de citer une fiche.

## Calendrier AI Act (après le règlement 2026/1744)

| Date | Application |
|---|---|
| 1er août 2024 | Entrée en vigueur |
| **2 février 2025** | Interdictions (art. 5) et maîtrise de l'IA (art. 4) |
| **2 août 2025** | Régime GPAI, gouvernance (Bureau de l'IA, Comité IA), désignation des autorités nationales, sanctions (hors amendes GPAI) |
| 27 juillet 2026 | Entrée en vigueur du règlement 2026/1744 : art. 4 assoupli, nouvel art. 4a (biais), allègements PME et petites entreprises de taille intermédiaire |
| **2 août 2026** | Application générale : transparence (art. 50), amendes GPAI (art. 101), pouvoirs renforcés du Bureau de l'IA |
| 2 décembre 2026 | Nouvelles interdictions (art. 5.1.ba et bb) ; fin du délai de marquage pour les systèmes génératifs mis sur le marché avant le 2 août 2026 |
| 2 août 2027 | Mise en conformité des modèles GPAI antérieurs au 2 août 2025 ; bacs à sable réglementaires nationaux opérationnels |
| **2 décembre 2027** | Systèmes à haut risque de l'**annexe III** (au lieu du 2 août 2026) |
| **2 août 2028** | Systèmes à haut risque de l'**annexe I** (au lieu du 2 août 2027) |
| 2 août 2030 | Systèmes à haut risque déjà utilisés par des autorités publiques (art. 111.2) |

## Digital Omnibus : ce qui est adopté, ce qui ne l'est pas

La Commission a présenté le **19 novembre 2025** deux propositions distinctes. Ne les confonds pas :

| | **Omnibus IA** (COM(2025) 836) | **Omnibus numérique / données** (COM(2025) 837) |
|---|---|---|
| Objet | Modifie l'AI Act | Modifie notamment le RGPD, la directive ePrivacy, NIS2, le Data Act |
| Statut à octobre 2026 | **Adopté** : règlement (UE) 2026/1744 du 8 juillet 2026, JOUE du 24 juillet 2026, en vigueur le 27 juillet 2026 | **Proposition en négociation**, non adoptée : pas d'effet juridique |
| Contenu clé | Report du haut risque, art. 4 assoupli, art. 4a, nouvelles interdictions, pouvoirs du Bureau de l'IA | Voir ci-dessous |

**Contenu de la proposition « données », à ne pas appliquer comme du droit positif** :
- **Définition des données personnelles** (art. 4.1) : une information ne serait pas personnelle pour une entité qui n'a pas de moyens raisonnables de réidentifier la personne (approche relative inspirée de CJUE, 4 septembre 2025, CEPD c/ CRU, C-413/23 P) ;
- **Intérêt légitime pour le développement et le fonctionnement de l'IA** (nouvel art. 88c), avec garanties et droit d'opposition inconditionnel ;
- Dérogation pour le **traitement résiduel de données sensibles** dans le développement de l'IA lorsque leur suppression exigerait un effort disproportionné, et nouvelle exception pour la **vérification biométrique** sous le contrôle exclusif de la personne (art. 9) ;
- Transfert des règles « cookies » dans le RGPD et guichet unique de notification des violations.

Le **CEPD et le Contrôleur européen (EDPS)** ont, dans leur avis conjoint 2/2026 (11 février 2026), demandé de **ne pas modifier la définition des données personnelles**. Au Conseil, une version de compromis divulguée supprimait cette nouvelle définition, et le mandat de négociation n'avait toujours pas été adopté à la fin de l'été 2026. Avant de citer une disposition, vérifie où en est la procédure (EUR-Lex, Observatoire législatif du Parlement).

## Autorités compétentes en France

- **CNIL** : reste pleinement compétente pour le RGPD, y compris pour l'entraînement et l'usage des modèles.
- **Désignation au titre de l'AI Act** : le schéma annoncé par le Gouvernement le 9 septembre 2025 confie la coordination et le point de contact unique à la **DGCCRF**, la surveillance de nombreux usages à la **CNIL** (pratiques interdites, biométrie, emploi, éducation, usages répressifs, migration), l'**Arcom** pour certains usages de transparence, l'**ACPR** pour la finance, ainsi que d'autres autorités sectorielles. La loi qui formalise ce schéma (projet de loi « DDADUE » d'adaptation au droit de l'UE, adopté par le Sénat en février 2026) **n'était pas encore définitivement adoptée** à la mi-septembre 2026, bien que la date limite de désignation (2 août 2025) soit dépassée. Vérifie sur Légifrance avant d'affirmer qu'une autorité est formellement désignée.

## Sanctions AI Act (art. 99 et 101)

- Pratiques interdites : jusqu'à **35 M€ ou 7 % du CA** mondial.
- Autres obligations (haut risque, transparence…) : jusqu'à **15 M€ ou 3 % du CA**.
- Informations inexactes fournies aux autorités : jusqu'à **7,5 M€ ou 1 % du CA**.
- Fournisseurs de modèles GPAI (art. 101, prononcées par la Commission) : jusqu'à **15 M€ ou 3 % du CA**.
- PME, jeunes pousses et, depuis le règlement 2026/1744, petites entreprises de taille intermédiaire : le **plus bas** des deux montants.

**Cumul possible** avec les sanctions RGPD (art. 83) si les manquements sont distincts.

## Cas pratiques

### Outil RH de tri des CV
- AI Act : **haut risque** (annexe III, emploi), obligations au 2 décembre 2027 ; information des salariés et représentants avant mise en service (art. 26.7).
- RGPD : AIPD obligatoire, information des candidats, art. 22 (intervention humaine effective), pas de données sensibles déduites.
- Dès aujourd'hui : interdiction de la reconnaissance des émotions en entretien vidéo (art. 5.1.f).

### IA générative pour rédaction interne
- AI Act : fournisseur du modèle soumis au régime GPAI ; l'entreprise est déployeur, soumise à l'art. 4 (maîtrise) et, si elle publie des contenus générés, à l'art. 50.
- RGPD : contrat de sous-traitance (art. 28) avec le fournisseur, vérification de l'absence de réutilisation des données pour l'entraînement, transferts hors UE, consignes pour ne pas saisir de données sensibles, formation des utilisateurs.

### Scoring de crédit ou tarification d'assurance santé
- AI Act : haut risque (annexe III, services essentiels) ; FRIA (art. 27) pour les déployeurs concernés.
- RGPD : art. 22 et jurisprudence SCHUFA, explication compréhensible de la logique (Dun & Bradstreet), droit de contester.
- La simple **détection de fraude financière** est exclue du haut risque par l'annexe III, mais reste soumise au RGPD.

### Reconnaissance faciale dans un commerce
- AI Act : l'interdiction de l'art. 5.1.h ne vise que l'usage **répressif** en temps réel. Un usage privé d'identification biométrique à distance relève du **haut risque** (annexe III, point 1), et la constitution d'une base par moissonnage d'images est interdite (art. 5.1.e).
- RGPD : données biométriques (art. 9) sans exception mobilisable dans la plupart des cas, AIPD obligatoire. En pratique la CNIL y est hostile, et en France la vidéoprotection algorithmique n'est autorisée que dans le cadre expérimental et limité de la loi (voir `references/donnees-sensibles.md`).

## Sources

- [AI Act — règlement (UE) 2024/1689, texte officiel](https://eur-lex.europa.eu/eli/reg/2024/1689/oj)
- [Règlement (UE) 2026/1744 « Digital Omnibus sur l'IA »](https://eur-lex.europa.eu/eli/reg/2026/1744/oj)
- [Conseil de l'UE — adoption définitive de l'Omnibus IA (29 juin 2026)](https://www.consilium.europa.eu/en/press/press-releases/2026/06/29/artificial-intelligence-council-gives-final-green-light-to-simplify-and-streamline-rules/)
- [Commission — cadre réglementaire de l'IA, lignes directrices et codes de bonnes pratiques](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)
- [Bureau de l'IA — Commission européenne](https://digital-strategy.ec.europa.eu/en/policies/ai-office)
- [Avis 28/2024 du CEPD sur les modèles d'IA](https://www.edpb.europa.eu/our-work-tools/our-documents/opinion-board-art-64/opinion-282024-certain-data-protection-aspects_en)
- [Avis conjoint CEPD-EDPS 2/2026 sur le Digital Omnibus](https://www.edpb.europa.eu/our-work-tools/our-documents/edpbedps-joint-opinion/edpb-edps-joint-opinion-22026-proposal_en)
- [CNIL — recommandations sur l'information et les droits (février 2025)](https://www.cnil.fr/fr/ia-et-rgpd-la-cnil-publie-ses-nouvelles-recommandations-pour-accompagner-une-innovation-responsable)
- [CNIL — recommandations sur l'intérêt légitime (juin 2025)](https://www.cnil.fr/fr/recommandations-developpement-ia-interet-legitime)
- [CNIL — finalisation des recommandations : modèles, annotation, sécurité (juillet 2025)](https://www.cnil.fr/fr/ia-finalisation-recommandations-developpement-des-systemes-ia)
- [CNIL — questions-réponses sur l'entrée en vigueur du règlement IA](https://www.cnil.fr/fr/entree-en-vigueur-du-reglement-europeen-sur-lia-les-premieres-questions-reponses-de-la-cnil)
