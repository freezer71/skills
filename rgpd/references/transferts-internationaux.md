# Transferts internationaux de données (Chapitre V — Articles 44 à 50)

Le transfert de données personnelles **hors de l'Espace économique européen** (UE + Islande, Liechtenstein, Norvège) n'est possible qu'avec un **mécanisme d'encadrement** garantissant un niveau de protection « substantiellement équivalent » à celui du RGPD (CJUE, Schrems II, 2020). Pourquoi cette exigence : sans elle, il suffirait d'exporter les données pour échapper au RGPD (art. 44 — la protection « voyage » avec les données).

## Qu'est-ce qu'un transfert ?

**Transfert** = transmission ou mise à disposition de données à un destinataire **situé en dehors de l'EEE**.

Cas typiques :
- Hébergement chez un cloud avec serveurs hors EEE ;
- Sous-traitant en Inde, Maroc, États-Unis ;
- Filiale d'un groupe située hors EEE qui accède aux données ;
- Maintenance à distance depuis un pays tiers ;
- Plateforme SaaS US (même si on choisit une « région EU », il faut vérifier où sont les opérations).

**Accès logique depuis l'étranger = transfert.** Une équipe support à Manille accédant à la base à Paris = transfert.

**Importateur déjà soumis au RGPD (art. 3.2)** : c'est quand même un transfert (lignes directrices CEPD 05/2021). Le RGPD s'applique à l'importateur, mais le droit local (surveillance, réquisitions) reste un risque : il faut un outil du chapitre V. Voir plus bas les CCT « art. 3.2 », toujours en préparation.

## Hiérarchie des mécanismes (art. 45-49)

### 1. Décision d'adéquation (art. 45) — le plus simple

La Commission européenne reconnaît qu'un pays tiers (ou une organisation internationale) assure un niveau adéquat de protection. **Pas de mesure supplémentaire requise** : le transfert est traité comme un transfert intra-UE.

**Pays, territoires et organisations adéquats (octobre 2026)** :
Andorre, Argentine, **Brésil** (depuis janvier 2026), Canada (organisations commerciales), Îles Féroé, Guernesey, Israël, Île de Man, Japon, Jersey, Nouvelle-Zélande, Corée du Sud, Suisse, Royaume-Uni, Uruguay, **États-Unis** (seulement les organisations certifiées au Data Privacy Framework — adéquation partielle), et **Organisation européenne des brevets** (première organisation internationale reconnue adéquate, juillet 2025).

Évolutions récentes à connaître :
- **Brésil** : décision d'exécution (UE) 2026/179 du 26 janvier 2026, fondée sur la LGPD et l'existence d'une autorité indépendante (ANPD). Adéquation **mutuelle** : le Brésil a reconnu l'UE en retour.
- **Royaume-Uni** : les deux décisions de 2021 (RGPD et directive « police-justice ») ont été **renouvelées le 19 décembre 2025**, après examen du *Data (Use and Access) Act 2025*. Elles expirent le **27 décembre 2031**, avec un réexamen à mi-parcours après quatre ans.
- **Corée du Sud** : premier réexamen conclu le 23 juillet 2026, adéquation confirmée ; les prochains réexamens auront lieu tous les quatre ans.

**Pourquoi vérifier la date** : une adéquation peut être limitée dans le temps (Royaume-Uni), partielle (Canada, États-Unis) ou invalidée par la CJUE (Safe Harbor, Privacy Shield). Consulter la liste officielle de la Commission avant chaque nouveau flux.

### 2. Garanties appropriées (art. 46) — le plus utilisé

#### a) Clauses contractuelles types (CCT)
Modèles juridiques adoptés par la Commission. **CCT du 4 juin 2021 (décision d'exécution (UE) 2021/914)**, seules utilisables depuis le 27 décembre 2022. Quatre modules :
- **Module 1** : responsable → responsable
- **Module 2** : responsable → sous-traitant
- **Module 3** : sous-traitant → sous-traitant
- **Module 4** : sous-traitant → responsable

Les CCT sont **complétées d'annexes** : description du transfert, mesures techniques et organisationnelles, sous-traitants ultérieurs. Ne pas modifier le texte des clauses : on peut seulement les compléter sans les contredire (clause 2).

**Limite importante** : les CCT de 2021 ne sont **pas conçues pour un importateur déjà soumis au RGPD par l'art. 3.2** (elles dupliqueraient ses obligations). La Commission annonce de **nouvelles CCT** pour ce cas (et pour les transferts des institutions de l'UE), mais **aucune décision n'est adoptée à octobre 2026**. En attendant, documenter le choix de l'outil retenu (en pratique, beaucoup continuent d'utiliser les CCT 2021) et surveiller la page CCT de la Commission.

**Obligation post-Schrems II** : réaliser une **AITD/TIA** (analyse d'impact des transferts) — voir plus bas.

#### b) Règles d'entreprise contraignantes (BCR — art. 47)
Pour les groupes multinationaux. Document interne approuvé par une autorité européenne, après procédure longue (12-24 mois). Adapté aux grandes entreprises.
- **BCR-C** (responsable) et **BCR-P** (sous-traitant, pour les transferts intragroupe entre entités agissant pour un client extérieur au groupe).
- Le CEPD a mis à jour le référentiel BCR-P (recommandations 1/2026, consultation publique close le 2 mars 2026). Vérifier sur edpb.europa.eu si la version finale est publiée avant de déposer un dossier.

#### c) Codes de conduite et certifications (art. 40, 42 et 46.2.e-f)
Longtemps théoriques, ils deviennent utilisables : le **16 avril 2026**, le CEPD a approuvé pour la première fois un **label européen (Europrivacy) comme outil de transfert**. Un importateur hors EEE **non soumis au RGPD** peut se faire certifier ; l'exportateur doit tout de même obtenir de lui des engagements contraignants et exécutoires (art. 46.2.f) et vérifier le droit local.

### 3. Dérogations pour situations particulières (art. 49) — exceptionnel

Pour des **transferts occasionnels** :
- Consentement explicite après information sur risques ;
- Nécessité contractuelle (avec la personne) ;
- Motif d'intérêt public important ;
- Constatation ou défense d'un droit en justice ;
- Intérêts vitaux ;
- Registres publics.

**À ne pas utiliser** pour des transferts récurrents ou structurés : le CEPD les interprète strictement (lignes directrices 2/2018). Risque de sanction.

## Demandes d'autorités étrangères (art. 48)

Une décision d'un tribunal ou d'une administration d'un pays tiers (par exemple une réquisition américaine au titre du CLOUD Act) **ne suffit pas, à elle seule**, à fonder un transfert : il faut un accord international (traité d'entraide judiciaire) ou, à défaut, une base légale (art. 6) **et** un outil du chapitre V.

Les **lignes directrices CEPD 02/2024 sur l'article 48** (version finale du 4 juin 2025) proposent une analyse en deux étapes : base légale, puis motif de transfert. Elles traitent aussi le cas où le destinataire de la demande est un **sous-traitant** (il doit en informer le responsable, art. 28.3.a) et celui de la maison mère hors UE qui réclame les données de sa filiale européenne.

**Pourquoi c'est utile** : c'est le texte de référence pour rédiger la politique de réponse aux demandes d'accès gouvernementales exigée par la clause 15 des CCT et pour évaluer un fournisseur cloud.

## Data Privacy Framework (DPF) — États-Unis

### Genèse
- **Safe Harbor** (2000), invalidé par la CJUE en 2015 (Schrems I, C-362/14).
- **Privacy Shield** (2016), invalidé par la CJUE en 2020 (Schrems II, C-311/18).
- **Data Privacy Framework** (décision d'adéquation (UE) 2023/1795 du 10 juillet 2023) — adéquation partielle.

### Mécanisme
Une entreprise américaine s'auto-certifie auprès du Department of Commerce en s'engageant à respecter les principes DPF. Liste publique : [dataprivacyframework.gov](https://www.dataprivacyframework.gov).

Plusieurs milliers d'organisations sont certifiées, dont la plupart des grands fournisseurs (cloud, bureautique, CRM, paiement, emailing). **Ne jamais présumer** : vérifier chaque entité et chaque service sur la liste.

### Contentieux : Latombe
- **Tribunal de l'UE, 3 septembre 2025, Latombe c/ Commission (T-553/23)** : recours en annulation **rejeté**. Le Tribunal juge que la *Data Protection Review Court* offre des garanties suffisantes d'indépendance et que la collecte « en vrac » par les services de renseignement américains est compatible avec le standard de Schrems II dès lors qu'elle est soumise à un contrôle juridictionnel a posteriori.
- **Pourvoi devant la CJUE (C-703/25 P)**, formé le 31 octobre 2025 : **pendant** à octobre 2026. La décision DPF reste en vigueur tant que la CJUE ne l'a pas annulée.

Pourquoi rester prudent : c'est la Cour de justice, et non le Tribunal, qui avait invalidé Safe Harbor et Privacy Shield. Un arrêt contraire en pourvoi ferait tomber les transferts fondés sur le seul DPF du jour au lendemain.

### Fragilités côté américain
- Le DPF repose sur l'**Executive Order 14086** (2022), modifiable par le Président sans vote du Congrès.
- Le **PCLOB** (Privacy and Civil Liberties Oversight Board), organe de contrôle cité dans la décision d'adéquation, a perdu son quorum après la révocation de trois de ses membres en janvier 2025 ; leur contestation judiciaire est toujours en cours aux États-Unis. Le Tribunal a rappelé que la légalité de la décision s'apprécie à la date de son adoption ; ces évolutions relèvent du suivi continu par la Commission et pourront peser dans le prochain réexamen (le pourvoi, lui, est limité aux questions de droit).
- **Réexamen périodique** : la Commission a publié le 9 octobre 2024 son rapport sur le premier réexamen (fonctionnement jugé satisfaisant) et a fixé le suivant **trois ans plus tard** (soit vers 2027). La Commission peut suspendre ou modifier la décision à tout moment si le cadre américain se dégrade (art. 45.5).

### Précautions
- **Vérifier la certification courante** (elle peut expirer ou être retirée).
- **Vérifier la portée** : certains services d'un même groupe sont certifiés, d'autres non ; vérifier la couverture des données RH (« HR data ») si besoin.
- **Prévoir un plan B** : faire signer les CCT dans le DPA du fournisseur, pour pouvoir basculer sans renégocier si le DPF tombe. Une AITD n'est pas exigée pour un transfert fondé sur le DPF, mais elle devient nécessaire dès qu'on bascule sur les CCT.

### Risque résiduel
Les autorités américaines peuvent toujours accéder aux données pour des motifs de sécurité nationale (FISA 702, CLOUD Act). C'est pourquoi, pour les **données particulièrement sensibles** (santé, défense, sources journalistiques), on recommande souvent un **hébergement souverain UE** plutôt que le DPF seul.

## Analyse d'impact des transferts (AITD / TIA) — obligation post-Schrems II

Pour tout transfert sur la base de CCT ou BCR (art. 46), l'exportateur doit évaluer, avec l'aide de l'importateur :

1. **Législation et pratiques du pays destinataire** : permettent-elles à l'importateur de respecter ses engagements ? (notamment surveillance étatique disproportionnée).
2. **Circonstances du transfert** : catégories de données, chaîne de sous-traitance, format, mode d'accès.
3. **Mesures supplémentaires** si nécessaire :
   - **Techniques** : chiffrement avec clés conservées en UE, pseudonymisation forte, fragmentation.
   - **Organisationnelles** : politique de réponse aux demandes d'accès gouvernementales, transparence.
   - **Contractuelles** : engagements renforcés, droit d'audit, notification.
4. **Réévaluation périodique**.

Méthodologie : **recommandations CEPD 01/2020** (version 2.0 du 18 juin 2021) et **guide pratique AITD de la CNIL (version finale publiée le 31 janvier 2025)**, qui propose une démarche en six étapes et un modèle de documentation. Conserver l'AITD dans la documentation d'accountability (art. 5.2).

## Data Act — accès gouvernementaux et changement de fournisseur cloud

Le **règlement (UE) 2023/2854 (Data Act)** est **applicable depuis le 12 septembre 2025**. Il ne remplace pas le RGPD, mais il touche directement les contrats cloud :

- **Art. 32 — accès gouvernementaux internationaux** : les fournisseurs de services de traitement de données (cloud, SaaS) doivent prendre des mesures techniques, organisationnelles et juridiques, y compris contractuelles, pour empêcher l'accès d'autorités de pays tiers aux **données à caractère non personnel** détenues dans l'UE lorsqu'il entrerait en conflit avec le droit de l'Union ou national. C'est le pendant, pour les données non personnelles, de l'art. 48 RGPD. Pour les données personnelles, le RGPD continue de s'appliquer.
- **Art. 23 à 31 — changement de fournisseur** : le contrat doit permettre de résilier et de migrer avec un **préavis de deux mois au plus**, suivi d'une **période de transition de 30 jours** (prolongeable jusqu'à sept mois si le fournisseur justifie une impossibilité technique), puis d'au moins 30 jours pour récupérer les données. Les **frais de changement** sont plafonnés aux coûts réels jusqu'au **12 janvier 2027**, puis **interdits** (art. 29).

Pourquoi c'est utile pour un DPA : la clause de restitution des données (art. 28.3.g RGPD) et la clause de réversibilité du contrat cloud doivent être cohérentes. Voir `references/sous-traitants.md`.

## Articulation pratique avec un cloud US

Pour un service comme AWS, Azure, GCP :

1. **Vérifier l'adhésion DPF** du fournisseur (et du service exact).
2. **Choisir une région EU** quand possible (localisation des données), en sachant que l'accès à distance depuis les États-Unis (support, administration) reste un transfert.
3. **Signer le DPA** du fournisseur, en vérifiant qu'il intègre les CCT en complément (plan B).
4. **Réaliser une AITD** documentant la configuration et les mesures supplémentaires (nécessaire si l'on s'appuie sur les CCT).
5. **Chiffrer côté client** pour les données les plus sensibles (BYOK/HYOK — gestion des clés en UE).
6. **Vérifier les clauses Data Act** (réversibilité, frais de sortie) et la politique de réponse aux réquisitions étrangères.

## Cas particuliers

### Transferts intra-groupe
- BCR si la volumétrie justifie le projet ;
- À défaut, CCT entre entités du groupe.
- Annexer la cartographie des flux dans la documentation RGPD.

### Maintenance et support à distance
- Souvent depuis Inde, Maroc, Tunisie.
- Soit DPA + CCT + AITD, soit interdiction d'accès depuis le pays tiers (accès via bastion EU).

### Vidéoconférence et messagerie
- Zoom, Microsoft Teams (DPF) : acceptables pour des réunions standard, après vérification de la certification ; pour les échanges sensibles, hébergement EU dédié.
- Alternatives souveraines : Tixeo, Olvid, Tchap (administrations).

### Open source hébergé sur GitHub
- Si dépôt public sans données personnelles : non concerné.
- Si dépôt privé contenant des données : transfert (GitHub = US, DPF).

### Newsletters via Mailchimp/Brevo
- Mailchimp (US, DPF) : acceptable avec DPA + précautions.
- Brevo (FR) : pas de transfert hors UE pour les serveurs européens, mais vérifier la liste de ses sous-traitants ultérieurs.

### Brésil
- Depuis janvier 2026, un prestataire brésilien soumis à la LGPD peut recevoir des données sans CCT ni AITD. Un DPA (art. 28) reste obligatoire s'il agit comme sous-traitant.

### Hyperscalers et données sensibles (santé, finance)
- Pour certaines données sensibles d'organismes publics ou d'opérateurs régulés, la doctrine française (« cloud au centre », données de santé) privilégie un cloud **qualifié SecNumCloud** par l'ANSSI, qui protège des lois extraterritoriales.
- Consulter la **liste à jour des prestataires qualifiés** sur le site de l'ANSSI (y figurent notamment des offres d'Outscale, d'OVHcloud et, depuis décembre 2025, l'offre PREMI3NS de S3NS). Vérifier le statut des autres offres annoncées (Bleu, etc.) au moment du choix.

## Évolutions proposées (non en vigueur)

**« Digital Omnibus »** (proposition de la Commission COM(2025) 837 du 19 novembre 2025) : il modifierait notamment la définition des données personnelles, la notification des violations (point d'entrée unique) et certaines dispositions du Data Act. Il **ne réforme pas le chapitre V** (transferts). À octobre 2026, le volet « données » est **toujours en première lecture** : le Conseil n'a pas arrêté sa position de négociation et aucun trilogue n'a commencé. **Ne pas l'appliquer** : raisonner sur le texte en vigueur.

## Sanctions et jurisprudence

### Schrems II (CJUE, 16 juillet 2020, C-311/18)
Invalide le Privacy Shield et impose l'analyse d'impact pour les CCT.

### Latombe (Tribunal de l'UE, 3 septembre 2025, T-553/23)
Valide le DPF en première instance ; pourvoi C-703/25 P pendant.

### Sanctions CNIL Google Analytics (2022)
GA en configuration standard = transfert non encadré → mises en demeure → utilisation de proxy ou alternative. Depuis le DPF, Google est certifié, mais la logique de vérification demeure.

### Meta (Irlande, 2023)
1,2 milliard d'€ pour transferts de données Facebook UE → US sans garanties suffisantes (avant DPF).

## Sources

- [Transférer des données hors UE — CNIL](https://www.cnil.fr/fr/les-outils-de-la-conformite/transferer-des-donnees-hors-de-lue)
- [Guide pratique AITD, version finale (janvier 2025) — CNIL](https://www.cnil.fr/fr/analyse-dimpact-des-transferts-des-donnees-la-cnil-publie-la-version-finale-de-son-guide-aitd)
- [Décisions d'adéquation — Commission](https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection/adequacy-decisions_en)
- [Décision d'exécution (UE) 2026/179 — adéquation du Brésil — EUR-Lex](https://eur-lex.europa.eu/eli/dec_impl/2026/179/oj)
- [Renouvellement des décisions d'adéquation du Royaume-Uni (19 décembre 2025) — Commission](https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection/adequacy-decisions_en)
- [Réexamen de l'adéquation de la Corée du Sud (23 juillet 2026) — Commission](https://commission.europa.eu/news-and-media/news/commission-finds-republic-korea-continues-provide-adequate-level-protection-personal-data-2026-07-23_en)
- [Décision (UE) 2025/1382 — adéquation de l'Organisation européenne des brevets — EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32025D1382)
- [Clauses contractuelles types — Commission](https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection/standard-contractual-clauses-scc_en)
- [Décision d'exécution (UE) 2021/914 (CCT transferts) — EUR-Lex](https://eur-lex.europa.eu/eli/dec_impl/2021/914/oj)
- [Décision d'adéquation (UE) 2023/1795 (DPF) — EUR-Lex](https://eur-lex.europa.eu/eli/dec_impl/2023/1795/oj)
- [Rapport sur le premier réexamen du DPF (9 octobre 2024) — Commission](https://commission.europa.eu/document/download/25695177-8073-4ce3-bf81-eb816dc6b468_en?filename=Report+on+the+first+periodic+review+of+the+functioning+of+the+adequacy+decision+on+the+EU-US+Data+Privacy+Framework.pdf)
- [Pourvoi C-703/25 P, Latombe c/ Commission — CURIA](https://curia.europa.eu/juris/liste.jsf?num=C-703/25)
- [Pourvoi C-703/25 P, publication au JO — EUR-Lex](https://eur-lex.europa.eu/eli/C/2025/6610/oj)
- [Data Privacy Framework officiel](https://www.dataprivacyframework.gov)
- [Recommandations 01/2020 sur les mesures supplémentaires — CEPD](https://www.edpb.europa.eu/our-work-tools/our-documents/recommendations/recommendations-012020-measures-supplement-transfer_fr)
- [Lignes directrices 02/2024 sur l'article 48 — CEPD](https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-022024-article-48-gdpr_en)
- [Lignes directrices 05/2021 sur l'interaction entre l'art. 3 et le chapitre V — CEPD](https://www.edpb.europa.eu/system/files/2023-02/edpb_guidelines_05-2021_interplay_between_the_application_of_art3-chapter_v_of_the_gdpr_v2_en_0.pdf)
- [Recommandations 1/2026 sur les BCR-P — CEPD](https://www.edpb.europa.eu/our-work-tools/documents/public-consultations/2026/recommendations-12026-application-approval-and_en)
- [Label Europrivacy approuvé comme outil de transfert (16 avril 2026) — CEPD](https://www.edpb.europa.eu/news/news/2026/edpb-brings-clarity-data-processing-scientific-research-speeds-finalisation_en)
- [Règlement (UE) 2023/2854 (Data Act) — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2023/2854/oj)
- [Arrêt Schrems II — CURIA](https://curia.europa.eu/juris/document/document.jsf?docid=228677)
