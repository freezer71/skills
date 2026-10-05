# Obligations du responsable de traitement (Chapitre IV — Articles 24 à 43)

Le RGPD impose des obligations actives de mise en conformité et de documentation. La logique : **« accountability »** — le responsable doit non seulement respecter les règles, mais **pouvoir le démontrer** à tout moment à la CNIL.

> **Droit en vigueur ou proposition ?** Plusieurs textes de simplification du RGPD sont en cours de négociation au niveau européen (voir la section « Évolutions annoncées » en fin de fiche). Au **1er octobre 2026**, aucun d'eux n'a modifié les articles 30, 33 ou 35 : applique le texte actuel et présente les réformes comme des **propositions**, jamais comme du droit acquis.

## Article 24 — Responsabilité du responsable de traitement

Mettre en œuvre des **mesures techniques et organisationnelles appropriées** pour s'assurer et démontrer la conformité, compte tenu :
- de la nature, portée, contexte, finalités du traitement ;
- des risques pour les droits et libertés des personnes.

Cela inclut : politiques internes, formation, audit, journalisation, gouvernance.

## Article 25 — Privacy by Design / by Default

**Privacy by Design** : intégrer la protection des données **dès la conception** d'un traitement, pas après coup.
- Pseudonymisation, minimisation, séparation des accès, chiffrement.
- Choix de prestataires conformes.

**Privacy by Default** : par défaut, seules les données strictement nécessaires sont traitées.
- Pas de cases pré-cochées.
- Pas de partage public par défaut sur un réseau social.
- Granularité maximale des permissions.

→ Documenter ces choix dans les spécifications du produit (PRD, DAT, etc.). Pour les équipes de développement, le **guide RGPD du développeur** de la CNIL (fiches thématiques, extraits de code) traduit ces principes en pratiques concrètes.

## Article 26 — Responsables conjoints

Quand deux ou plusieurs entités déterminent **ensemble** finalités et moyens, elles sont responsables conjoints. Elles doivent conclure un **accord** précisant :
- Qui exerce quels droits ;
- Qui informe les personnes ;
- Point de contact.

L'essentiel de l'accord doit être mis à disposition des personnes. *Exemple :* administrateur d'une page fan Facebook et Meta (CJUE, 5 juin 2018, *Wirtschaftsakademie Schleswig-Holstein*, C-210/16).

## Article 27 — Représentant dans l'UE

Une entité hors UE soumise au RGPD (voir l'art. 3.2) désigne par écrit un **représentant** dans l'UE qui sert d'interlocuteur aux autorités et aux personnes. Exception : traitement occasionnel, à faible risque, sans données sensibles ou pénales à grande échelle.

## Article 28 — Sous-traitants

Choix d'un sous-traitant offrant des garanties suffisantes + contrat écrit (DPA) comportant les clauses obligatoires. Voir `references/sous-traitants.md`.

## Article 29 — Traitement sous l'autorité

Le sous-traitant et les personnes agissant sous l'autorité du responsable ne traitent les données **que sur instruction** du responsable.

## Article 30 — Registre des activités de traitement

**Obligation centrale.** Tenir un registre écrit (papier ou électronique), à communiquer à la CNIL sur demande (art. 30.4).

**Contenu pour le responsable** (art. 30.1) :
- Nom et coordonnées du responsable, le cas échéant du responsable conjoint, du représentant et du DPO ;
- Finalités du traitement ;
- Catégories de personnes concernées et de données ;
- Catégories de destinataires ;
- Transferts hors UE et garanties ;
- Durées de conservation prévues (dans la mesure du possible) ;
- Description générale des mesures de sécurité (dans la mesure du possible).

**Contenu pour le sous-traitant** (art. 30.2) : registre des catégories de traitements effectués pour le compte de chaque responsable.

**Exemption en vigueur** (art. 30.5) : organisations de **moins de 250 salariés**, **sauf** si le traitement :
- est susceptible de comporter un risque pour les droits et libertés ; OU
- n'est pas occasionnel ; OU
- porte sur des données sensibles (art. 9.1) ou pénales (art. 10).

→ En pratique, presque toutes les organisations doivent tenir un registre, au moins pour leurs traitements récurrents (paie, clients, fournisseurs). La CNIL propose un **modèle de registre simplifié** pour les TPE-PME.

**Réforme en cours — à ne pas appliquer par anticipation** : la proposition « Omnibus IV » (Commission, 21 mai 2025, COM(2025) 501) relève le seuil de l'exemption à **750 salariés** (nouvelle catégorie des « petites entreprises de taille intermédiaire », *small mid-caps*) et ne maintient l'obligation, sous ce seuil, que pour les traitements **susceptibles d'engendrer un risque élevé**. Le CEPD et le Contrôleur européen de la protection des données (EDPS) l'ont accueillie favorablement (avis conjoint 01/2025 du 8 juillet 2025). Le Parlement et le Conseil ont annoncé un **accord provisoire le 9 juin 2026**, qui porterait le seuil des *small mid-caps* à **1 000 salariés** selon les comptes rendus publiés ; au 1er octobre 2026, l'adoption formelle et la publication au *Journal officiel de l'UE* ne sont **pas confirmées**. Tant que le règlement modificatif n'est pas publié et applicable, **le seuil de 250 salariés reste le droit positif**. Même après la réforme, un registre reste le meilleur outil pour démontrer la conformité (art. 5.2 et 24).

Modèle : voir `assets/registre-traitements.md`.

## Article 32 — Sécurité du traitement

Mesures **adaptées au risque** :
- **Pseudonymisation et chiffrement** ;
- **Confidentialité, intégrité, disponibilité, résilience** des systèmes ;
- **Rétablissement de la disponibilité** après incident ;
- **Procédure de test régulier** de l'efficacité des mesures.

Approche **par les risques**, pas exhaustive — la « sécurité parfaite » n'existe pas, mais l'absence de mesures de base (mots de passe robustes, sauvegardes, mises à jour, sensibilisation) est sanctionnée systématiquement.

→ Référentiel pratique : **guide CNIL « Sécurité des données personnelles », édition 2024** — 25 fiches réparties en 5 parties, dont de nouvelles fiches sur l'intelligence artificielle, les applications mobiles, l'informatique en nuage et les API, accompagnées d'une liste de vérification.

**Articulation avec NIS 2** : la directive (UE) 2022/2555 impose ses propres mesures de cybersécurité et notifications d'incidents aux entités essentielles et importantes. En France, le projet de loi « relatif à la résilience des infrastructures critiques et au renforcement de la cybersécurité » (transposition de NIS 2, REC et adaptation à DORA) a été adopté par le Sénat en mars 2025 et par la commission spéciale de l'Assemblée nationale en septembre 2025, mais **n'était pas promulgué** à la date de mise à jour de cette fiche. Vérifie son état avant de répondre ; dans tous les cas, NIS 2 s'ajoute au RGPD sans le remplacer.

## Articles 33-34 — Violation de données

Notification à la CNIL **dans les meilleurs délais et au plus tard 72 heures** après en avoir pris connaissance, **sauf** si la violation est peu susceptible d'engendrer un risque ; information des personnes si **risque élevé**. Toute violation, même non notifiée, est inscrite au registre interne (art. 33.5). Voir `references/violations-donnees.md` et le modèle `assets/notification-violation.md`.

## Article 35 — Analyse d'impact (AIPD / DPIA)

**Obligatoire** quand le traitement est susceptible d'engendrer un **risque élevé** pour les droits et libertés des personnes physiques.

**Cas obligatoires (art. 35.3)** :
- Évaluation systématique et approfondie d'aspects personnels (profilage) fondant des décisions qui produisent des effets juridiques ou affectent la personne de manière significative ;
- Traitement à grande échelle de données sensibles ou pénales ;
- Surveillance systématique à grande échelle d'une zone accessible au public.

**Critères du CEPD** (lignes directrices WP248 rév. 01, reprises par le CEPD) : 9 critères — évaluation/notation, décision automatisée, surveillance systématique, données sensibles ou hautement personnelles, grande échelle, croisement de données, personnes vulnérables, usage innovant ou nouvelle technologie, obstacle à l'exercice d'un droit. **Deux critères réunis** = AIPD en principe requise.

**Liste CNIL des traitements pour lesquels une AIPD est requise** (art. 35.4 — délibération n° 2018-327 du 11 octobre 2018, 14 types d'opérations). Exemples : données de santé traitées par les établissements de santé ou médico-sociaux ; données génétiques de personnes vulnérables ; profils à des fins de gestion RH ; surveillance constante de l'activité des salariés ; biométrie pour identifier de manière unique ; profilage pouvant conduire à l'exclusion du bénéfice d'un contrat ; données de localisation à large échelle ; gestion des logements sociaux. La liste **n'est pas exhaustive** : un traitement absent de la liste peut nécessiter une AIPD au regard des 9 critères (c'est souvent le cas des systèmes d'IA traitant des données personnelles — voir `references/ai-act-rgpd.md`).

**Liste CNIL des traitements pour lesquels une AIPD n'est pas requise** (art. 35.5 — délibération n° 2019-118 du 12 septembre 2019, 12 types). Exemples : gestion RH du personnel des organismes de moins de 250 salariés (hors profilage) ; gestion de la relation fournisseurs ; activités des comités d'entreprise ; fichier électoral des communes ; services scolaires, périscolaires et de petite enfance.

**Contenu minimum (art. 35.7)** :
1. Description systématique des opérations et finalités ;
2. Évaluation de la nécessité et de la proportionnalité ;
3. Évaluation des risques pour les droits et libertés ;
4. Mesures envisagées pour traiter les risques (garanties, mesures de sécurité, mécanismes).

**Consultation préalable** (art. 36) : si les risques résiduels restent élevés malgré les mesures, consulter la CNIL **avant** la mise en œuvre. Elle répond sous **8 semaines**, délai prolongeable de **6 semaines** pour les traitements complexes.

**Outils** : le **logiciel PIA** de la CNIL (libre, gratuit, disponible en une vingtaine de langues, en version poste de travail ou serveur) et les trois guides méthodologiques « AIPD 1 : la méthode », « AIPD 2 : les modèles », « AIPD 3 : les bases de connaissances ».

**Réforme en cours** : la proposition « Digital Omnibus » (voir plus bas) remplacerait les listes nationales par des **listes européennes uniques** (traitements soumis ou non à AIPD) et par un **modèle et une méthodologie communs**, préparés par le CEPD et adoptés par actes d'exécution de la Commission. Ce n'est **pas** du droit en vigueur : les listes de la CNIL continuent de s'appliquer.

Modèle : voir `assets/aipd-template.md`.

## Articles 37-39 — Délégué à la protection des données (DPO/DPD)

### Désignation obligatoire (art. 37.1) si :
- a) Autorité ou organisme public (sauf juridictions dans l'exercice de leur fonction juridictionnelle) ;
- b) Activités de base = **suivi régulier et systématique à grande échelle** des personnes ;
- c) Activités de base = traitement à **grande échelle de données sensibles ou pénales**.

La désignation reste possible, et souvent utile, hors obligation ; un DPO désigné volontairement est soumis au même statut.

### Mode de désignation
- Interne ou externe (mutualisé possible pour un groupe ou plusieurs organismes publics, art. 37.2-37.3).
- Sur **qualités professionnelles** (connaissance du droit et des pratiques en matière de protection des données).
- Coordonnées **publiées** et **communiquées à la CNIL** (art. 37.7) : désignation, mise à jour, remplacement ou fin de mission se font **exclusivement** par le téléservice de la CNIL (munis du numéro de désignation « DPO-… » et du SIREN pour les modifications).

### Statut et garanties
- Position lui permettant l'**indépendance** : il ne reçoit aucune instruction pour l'exercice de ses missions et fait rapport au plus haut niveau de la direction (art. 38.3).
- **Pas de conflit d'intérêts** (art. 38.6) : ne peut être DPO une personne qui détermine les finalités et les moyens de traitements (dirigeant, DSI, DRH, directeur marketing… selon le contexte). La CJUE impose une appréciation au cas par cas (CJUE, 9 février 2023, *X-FAB Dresden*, C-453/21).
- **Ressources et accès** aux données et opérations de traitement (art. 38.2).
- **Protection contre la révocation ou la sanction** pour l'exercice de ses missions ; le droit national peut prévoir une protection plus forte (CJUE, 22 juin 2022, *Leistritz*, C-534/20).

L'**action coordonnée 2023 du CEPD** sur la désignation et la position des DPO (rapport adopté le 17 janvier 2024, 25 autorités participantes) a relevé des manquements récurrents : absence de désignation pourtant obligatoire, ressources ou expertise insuffisantes, missions non confiées, défaut d'indépendance ou de rapport à la direction. Ces points sont autant d'axes de contrôle.

### Missions (art. 39)
- Informer et conseiller le responsable et les employés ;
- Contrôler le respect du RGPD ;
- Conseiller sur les AIPD et en vérifier l'exécution ;
- Coopérer avec la CNIL ;
- Servir de point de contact (CNIL, personnes concernées).

**Le DPO conseille, il n'est pas le décideur**. La responsabilité juridique reste au responsable de traitement.

## Articles 40-43 — Codes de conduite et certifications

Mécanismes volontaires pour démontrer la conformité (codes sectoriels approuvés, certifications délivrées par un organisme accrédité). Encore peu développés en pratique.

## Évolutions annoncées (à suivre — non applicables au 1er octobre 2026)

| Texte | Contenu utile ici | Statut au 1er octobre 2026 |
|---|---|---|
| **Omnibus IV** — COM(2025) 501, 21 mai 2025 | Exemption de registre (art. 30.5) étendue sous un seuil de 750 salariés, sauf traitement à risque élevé | Accord provisoire Parlement-Conseil annoncé le 9 juin 2026 (seuil *small mid-caps* porté à 1 000 salariés selon les comptes rendus) ; adoption formelle et publication au JOUE non confirmées |
| **Digital Omnibus** — COM(2025) 837, 19 novembre 2025 (procédure 2025/0360(COD)) | Listes européennes uniques d'AIPD + modèle commun (art. 35) ; notification de violation à l'autorité **seulement en cas de risque élevé**, sous **96 h**, via un **point d'entrée unique** géré par l'ENISA (art. 33, 33 bis) ; allègement de l'information art. 13 dans une relation « claire et circonscrite » peu intensive en données ; précision sur les demandes d'accès **abusives** (art. 12.5) ; nouvelle définition contextuelle de la donnée personnelle | En **première lecture** : avis conjoint CEPD-EDPS 2/2026 du 10 février 2026 (favorable au seuil « risque élevé » et aux 96 h, demandes de précision sur les art. 12.5 et 13.4) ; aucun mandat du Conseil ni trilogue connu ; adoption non attendue avant fin 2026 au plus tôt |
| **Règlement procédural RGPD** — règlement (UE) 2025/2518, JOUE du 12 décembre 2025 | Règles de procédure harmonisées pour les affaires **transfrontalières** (recevabilité des réclamations, coopération entre autorités, droits procéduraux des parties) — ne modifie pas les obligations de fond du responsable | **Adopté et publié** ; applicable à partir du **2 avril 2027** |

Le CEPD a, par ailleurs, exposé sa position sur la simplification dans la **déclaration d'Helsinki** du 2 juillet 2025 (« plus de clarté, de soutien et d'engagement ») : simplifier par des outils pratiques (modèles, listes, guides pour les PME) sans abaisser le niveau de protection.

## Récapitulatif : documentation minimale à constituer

| Document | Article | Obligation |
|---|---|---|
| Registre des activités de traitement | 30 | Quasi-toujours (exemption étroite sous 250 salariés) |
| Politiques internes (sécurité, conservation, droits) | 24 | Toujours |
| AIPD pour traitements à risque | 35 | Conditionnée (listes CNIL + 9 critères) |
| Registre des violations | 33.5 | Toujours |
| Contrats DPA avec sous-traitants | 28 | Toujours quand sous-traitant |
| Mentions d'information | 13-14 | Toujours |
| Preuve des consentements | 7.1 | Quand consentement est la base |
| Désignation du DPO auprès de la CNIL | 37.7 | Si DPO |
| LIA (*legitimate interest assessment*) | 6.1.f | Quand base = intérêt légitime |
| TIA (*transfer impact assessment*) | 46 | Quand transfert hors UE sur CCT/BCR |

## Sources

- [Règlement (UE) 2016/679 (RGPD) — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- [Chapitre IV — CNIL](https://www.cnil.fr/fr/reglement-europeen-protection-donnees/chapitre4)
- [Désigner un DPO ou modifier une désignation — CNIL](https://www.cnil.fr/fr/designation-dpo)
- [Devenir délégué à la protection des données — CNIL](https://www.cnil.fr/fr/devenir-delegue-la-protection-des-donnees)
- [Action coordonnée 2023 sur les DPO, rapport du 17 janvier 2024 — CEPD](https://www.edpb.europa.eu/documents/coordinated-enforcement-framework/coordinated-enforcement-action-designation-and-position_en)
- [AIPD : ce qu'il faut savoir — CNIL](https://www.cnil.fr/fr/ce-quil-faut-savoir-sur-lanalyse-dimpact-relative-la-protection-des-donnees-aipd)
- [Liste des traitements pour lesquels une AIPD est requise — CNIL](https://www.cnil.fr/sites/default/files/atoms/files/liste-traitements-aipd-requise.pdf)
- [Liste des traitements pour lesquels une AIPD n'est pas requise — CNIL](https://www.cnil.fr/fr/liste-traitements-aipd-non-requise)
- [Logiciel PIA et guides méthodologiques — CNIL](https://www.cnil.fr/fr/outil-pia-telechargez-et-installez-le-logiciel-de-la-cnil)
- [Guide de la sécurité des données personnelles, édition 2024 — CNIL](https://www.cnil.fr/fr/guide-de-la-securite-des-donnees-personnelles-nouvelle-edition-2024)
- [Guide RGPD du développeur — CNIL](https://www.cnil.fr/fr/guide-rgpd-du-developpeur)
- [Proposition Omnibus IV, volet RGPD (COM(2025) 501) — Commission européenne](https://commission.europa.eu/document/download/7fd9c846-b894-4f9f-b164-3b926d1b264b_en?filename=Proposal+GDPR+Omnibus.pdf)
- [Avis conjoint CEPD-EDPS 01/2025 sur la simplification du registre — CEPD](https://www.edpb.europa.eu/documents/legislative-opinion/edpb-edps-joint-opinion-012025-on-the-proposal-for-a-regulation-on_en)
- [Proposition Digital Omnibus (COM(2025) 837) — EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:52025PC0837)
- [Avis conjoint CEPD-EDPS 2/2026 sur le Digital Omnibus — CEPD](https://www.edpb.europa.eu/system/files/2026-02/edpb_edps_jointopinion_202602_digitalomnibus_en.pdf)
- [Règlement (UE) 2025/2518 (règles de procédure RGPD) — EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:L_202502518)
- [Avancement de la transposition de NIS 2 — ANSSI](https://aide.monespacenis2.cyber.gouv.fr/fr/article/avancement-de-la-transposition-de-la-directive-nis-2-1b3j1da/)
