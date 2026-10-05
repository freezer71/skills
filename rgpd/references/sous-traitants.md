# Sous-traitants et DPA (Article 28 RGPD)

Tout prestataire qui traite des données personnelles **pour le compte** d'un responsable est un sous-traitant au sens du RGPD. Cela couvre la majorité des SaaS, hébergeurs, agences, prestataires informatiques, plateformes d'emailing, CRM, services cloud, prestataires paie.

## Qualification : qui est qui ?

| Rôle | Détermination |
|---|---|
| **Responsable de traitement** | Détermine **finalités et moyens** essentiels |
| **Sous-traitant** | Traite **sur instructions** du responsable, pour les finalités du responsable |
| **Responsables conjoints** | Déterminent ensemble finalités et moyens (art. 26) |
| **Tiers** | Personne autre que le responsable, le sous-traitant et les personnes autorisées sous leur autorité |

**Cas piège** : un prestataire qui utilise les données pour ses propres finalités (amélioration de son IA, statistiques agrégées vendues à des tiers) devient **responsable de traitement** pour ces finalités-là. → Demander qualification claire dans le contrat.

*Exemple :* Mailchimp est sous-traitant pour la diffusion d'emails que tu lui confies. Si Mailchimp utilise tes données pour entraîner son IA marketing, il devient responsable pour cette finalité-là.

## Choix du sous-traitant (art. 28.1)

Obligation de ne recourir qu'à des sous-traitants présentant **des garanties suffisantes** quant à la mise en œuvre de mesures techniques et organisationnelles appropriées.

**Diligences à mener avant contractualisation** :
- Vérifier les certifications (ISO 27001, HDS pour la santé, SecNumCloud, SOC 2…) ;
- Auditer (questionnaire RGPD, audit terrain, rapport SOC) ;
- Vérifier la localisation des données et sous-traitants ultérieurs ;
- Examiner la politique de sécurité, le PRA/PCA, les engagements de notification ;
- Lire la « DPA » et la politique de confidentialité du prestataire.

**Documenter cette diligence** = élément d'accountability.

## Contrat obligatoire (art. 28.3) — le DPA

Le sous-traitant ne peut traiter qu'**en vertu d'un acte juridique écrit** (papier ou électronique) liant le sous-traitant au responsable, fixant :

1. **L'objet et la durée** du traitement ;
2. La **nature et la finalité** du traitement ;
3. Le **type de données** et les **catégories de personnes concernées** ;
4. Les **obligations et droits** du responsable.

Et imposant que le sous-traitant :

### a) Ne traite les données que sur instruction documentée
Y compris pour les transferts hors UE. Si le sous-traitant est légalement obligé de traiter autrement par le **droit de l'Union ou d'un État membre** (réquisition judiciaire), il en informe le responsable avant — sauf interdiction légale.

Attention à la rédaction : l'exception de l'art. 28.3.a ne vise que le droit de l'UE et des États membres. Le CEPD (avis 22/2024) recommande fortement de reprendre cette formule telle quelle plutôt qu'une formule large (« sauf si la loi applicable l'exige »), qui pourrait couvrir le droit d'un pays tiers. Pour les demandes d'autorités étrangères, voir `references/transferts-internationaux.md` (art. 48).

### b) Confidentialité
S'assure que les personnes autorisées à traiter sont soumises à une obligation de confidentialité (contrat de travail, NDA).

### c) Sécurité
Prend toutes les mesures requises au titre de l'article 32.

### d) Sous-traitance ultérieure
Ne recrute pas d'autre sous-traitant **sans autorisation écrite préalable, spécifique ou générale**, du responsable. En cas d'autorisation générale, informer de tout changement et permettre objection.

Le sous-traitant ultérieur est soumis aux **mêmes obligations** par contrat (art. 28.4), et le sous-traitant initial reste **pleinement responsable** envers le responsable de l'exécution par son sous-traitant ultérieur.

Voir plus bas « Chaîne de sous-traitance » pour ce que le CEPD attend du responsable.

### e) Assistance pour les droits des personnes
Aide le responsable, par des mesures techniques et organisationnelles appropriées, à répondre aux demandes des personnes (accès, rectification, effacement, etc.).

### f) Assistance pour la sécurité et les violations
Aide le responsable à respecter ses obligations de sécurité (art. 32), notification de violation (art. 33-34), AIPD (art. 35), consultation préalable (art. 36).

### g) Sort des données en fin de prestation
**Au choix du responsable** : suppression ou restitution de toutes les données + suppression des copies, sauf obligation légale de conservation (droit de l'UE ou d'un État membre).

Pourquoi c'est la clause la plus sanctionnée en pratique : des copies oubliées chez un ancien prestataire restent exposées sans que personne ne les surveille (voir la sanction Mobius ci-dessous). Exiger une **attestation de suppression** et vérifier la cohérence avec la clause de réversibilité du contrat cloud (Data Act, voir plus bas).

### h) Auditabilité
Met à disposition du responsable toutes les informations nécessaires pour démontrer le respect des obligations, et permet la réalisation d'audits, y compris inspections, par le responsable ou un mandataire.

## Obligations propres du sous-traitant

Le sous-traitant n'est pas un simple exécutant : le RGPD lui impose des obligations directes, sanctionnables par la CNIL **indépendamment** du responsable.

- **Ne traiter que sur instruction** (art. 29) — utiliser les données pour ses propres besoins est un manquement, et il devient responsable de traitement pour cet usage (art. 28.10).
- **Tenir son propre registre** des catégories de traitements effectués pour le compte de ses clients (art. 30.2).
- **Sécuriser** les données (art. 32).
- **Notifier au responsable** toute violation dans les meilleurs délais (art. 33.2).
- **Désigner un DPO** dans les cas de l'art. 37 et **coopérer** avec la CNIL (art. 31).
- **Encadrer ses transferts** hors EEE (chapitre V) ; un sous-traitant établi hors UE mais soumis au RGPD (art. 3.2) peut devoir désigner un représentant (art. 27).

## Chaîne de sous-traitance (avis CEPD 22/2024)

Adopté le 7 octobre 2024 à la demande de l'autorité danoise, l'avis 22/2024 précise ce que l'art. 28 implique quand il y a des sous-traitants ultérieurs (et des sous-traitants de sous-traitants) :

- **Identité de toute la chaîne** : le responsable doit pouvoir disposer **à tout moment** de l'identité (nom, adresse, personne de contact) de tous les sous-traitants et sous-traitants ultérieurs, quel que soit leur rang. Pourquoi : sans cette liste, il ne peut ni répondre à une demande d'accès sur les destinataires (art. 15.1.c), ni s'opposer à un nouveau prestataire.
- **Vérification des garanties** : l'obligation de ne recourir qu'à des sous-traitants présentant des garanties suffisantes (art. 28.1) s'étend à **toute la chaîne**. L'intensité de la vérification dépend du **risque** : le responsable peut s'appuyer sur les informations collectées par son sous-traitant direct, et ne vérifier lui-même en détail que lorsque le risque est élevé.
- **Transferts dans la chaîne** : le responsable reste tenu de s'assurer que les transferts effectués par ses sous-traitants (et leurs propres sous-traitants) sont encadrés. Le sous-traitant exportateur prépare la documentation (CCT module 3, AITD), mais le responsable doit pouvoir la consulter et l'évaluer.
- **Clause « droit de l'UE ou d'un État membre »** : voir point a) ci-dessus.

En pratique : exiger dans le DPA une **liste des sous-traitants ultérieurs à jour**, couvrant tous les rangs, avec pays et mécanisme de transfert ; et un engagement de fournir sur demande les contrats ou extraits pertinents.

## Clauses contractuelles types (CCT) sous-traitance

La Commission européenne a publié des **CCT entre responsable et sous-traitant** (décision d'exécution (UE) 2021/915 du 4 juin 2021, art. 28.7). Modèle gratuit, optionnel mais sécurisant : leur utilisation garantit la conformité du contenu à l'art. 28.

À ne pas confondre avec les **CCT de transfert** (décision (UE) 2021/914), qui encadrent les flux hors EEE ; leurs modules 2 et 3 incluent déjà les exigences de l'art. 28 et peuvent donc tenir lieu de DPA pour un sous-traitant situé hors EEE. Voir `references/transferts-internationaux.md`.

La CNIL met aussi à disposition un modèle français (guide du sous-traitant).

## Contrats cloud et Data Act

Le **Data Act** (règlement (UE) 2023/2854), **applicable depuis le 12 septembre 2025**, impose aux fournisseurs de services cloud et SaaS des clauses de **changement de fournisseur** (art. 23 à 31) : préavis de résiliation de deux mois au plus, transition de 30 jours (prolongeable jusqu'à sept mois si impossibilité technique), au moins 30 jours pour récupérer les données, frais de changement interdits à partir du 12 janvier 2027 (art. 29). L'art. 32 impose aussi des mesures contre les accès gouvernementaux étrangers aux données non personnelles.

Pourquoi c'est lié au DPA : la restitution des données personnelles en fin de contrat (art. 28.3.g RGPD) et la portabilité vers un nouveau prestataire doivent fonctionner ensemble. Vérifier que le contrat cloud et le DPA prévoient les mêmes formats, délais et modalités de suppression.

## Responsabilité conjointe en cas de manquement

- Sanction possible **directement contre le sous-traitant** (art. 83).
- Action en justice possible par la personne **contre l'un ou l'autre** (art. 82.4) : solidarité pour assurer indemnisation effective.
- Recours interne entre responsable et sous-traitant selon contrat et part de responsabilité.

## Cas pratiques fréquents

### Cloud hébergeur (AWS, Azure, GCP, OVH…)
- Sous-traitants. DPA standard publié.
- Vérifier : localisation des régions, sous-traitants ultérieurs (annexe technique), engagements de sécurité, transferts hors UE.
- Pour les hyperscalers US : DPF + CCT en complément, voir `references/transferts-internationaux.md`.
- Vérifier les clauses Data Act (réversibilité, frais de sortie).

### SaaS de gestion (CRM, ERP, RH, helpdesk)
- Sous-traitants.
- Souvent contrat type non négociable pour les PME. Lire attentivement et noter les écarts.

### Prestataires intellectuels (cabinets de conseil, agences, freelances)
- Sous-traitants quand ils traitent des données pour ton compte.
- Souvent oubliés du DPA. Régulariser systématiquement.

### Cabinet comptable, paie externalisée
- Sous-traitants (la finalité — tenir la compta — est définie par le client).
- DPA + clause de confidentialité renforcée + sécurisation des échanges (pas de pièces jointes non chiffrées).

### Avocat
- **Responsable de traitement indépendant** dans l'exercice de sa mission (secret professionnel autonome). Pas sous-traitant.

### Prestataire d'analytics (Google Analytics, Matomo…)
- Sous-traitant si configuré en mode strict.
- GA en mode standard pose des problèmes RGPD (CNIL 2022) — préférer Matomo en local ou configuration avancée.

### Système de paiement (Stripe, etc.)
- Co-responsables ou responsable indépendant selon montage. Lire attentivement les CGU.

## Erreurs classiques sanctionnées par la CNIL

1. **Pas de contrat écrit** avec un sous-traitant manifeste (audit interne révèle qu'on a fourni des données à une agence sans DPA).
2. **DPA muet** sur la sous-traitance ultérieure, qui se découvre lors d'un incident.
3. **Audit jamais réalisé**, alors que le contrat le prévoit.
4. **Reconduction tacite** d'un contrat ancien (pré-RGPD) sans mise à niveau.
5. **Données conservées** par le sous-traitant après fin de prestation, sans purge.
6. **Sous-traitant hors UE non encadré** par DPF/CCT/BCR.
7. **Sous-traitant qui réutilise les données** de ses clients pour ses propres services (art. 29 et 28.10).

### Exemple : Mobius Solutions (CNIL, SAN-2025-014, 11 décembre 2025)

**1 million d'euros** d'amende contre un **sous-traitant** établi hors UE (soumis au RGPD par l'art. 3.2), ancien prestataire de campagnes publicitaires de Deezer. Manquements retenus :
- conservation, après la fin du contrat, d'une copie des données de plus de 46 millions d'utilisateurs (art. 28.3.g) — données ensuite retrouvées en ligne ;
- réutilisation de ces données, hors de toute instruction, pour améliorer ses propres services (art. 29) ;
- absence de registre des traitements en qualité de sous-traitant (art. 30.2).

Leçon : la CNIL sanctionne **directement** le sous-traitant défaillant. Côté responsable, la clause de suppression ne suffit pas : il faut obtenir et conserver la preuve de suppression.

## Évolutions proposées (non en vigueur)

La proposition « Digital Omnibus » (COM(2025) 837, 19 novembre 2025) ne modifie pas l'art. 28. Sa nouvelle définition « relative » des données personnelles pourrait toutefois compliquer la qualification des rôles dans les chaînes de prestataires. À octobre 2026, le texte est toujours en première lecture : raisonner sur le RGPD en vigueur.

## Sources

- [Article 28 — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- [Avis 22/2024 sur les obligations liées au recours à des sous-traitants et sous-traitants ultérieurs — CEPD](https://www.edpb.europa.eu/system/files/documents/2024-10/edpb_opinion_202422_relianceonprocessors-sub-processors_en.pdf)
- [Lignes directrices 07/2020 sur les notions de responsable de traitement et de sous-traitant — CEPD](https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-072020-concepts-controller-and-processor-gdpr_fr)
- [Sanction de MOBIUS SOLUTIONS LTD (1 M€) — CNIL](https://www.cnil.fr/fr/violation-de-donnees-sanction-dun-million-deuros-lencontre-de-la-societe-mobius-solutions-ltd)
- [Délibération SAN-2025-014 du 11 décembre 2025 — Légifrance](https://www.legifrance.gouv.fr/cnil/id/CNILTEXT000053048614)
- [Règlement (UE) 2023/2854 (Data Act) — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2023/2854/oj)
- [Guide du sous-traitant — CNIL](https://www.cnil.fr/sites/cnil/files/atoms/files/rgpd-guide_sous-traitant-cnil.pdf)
- [Clauses contractuelles types sous-traitance — CNIL](https://www.cnil.fr/fr/clauses-contractuelles-types-entre-responsable-de-traitement-et-sous-traitant)
- [Décision (UE) 2021/915 CCT sous-traitance — EUR-Lex](https://eur-lex.europa.eu/eli/dec_impl/2021/915/oj)
