# Bases légales du traitement (Article 6 RGPD)

Tout traitement doit reposer sur **une et une seule** base légale par finalité. Choisir la mauvaise base est l'une des causes les plus fréquentes de sanction CNIL. La base doit être déterminée **avant** la mise en œuvre et **communiquée** aux personnes.

## Les 6 bases possibles (article 6.1)

### a) Consentement (art. 6.1.a)
La personne a explicitement accepté. Critères de validité (art. 7) — voir `references/consentement-cookies.md` :
- **Libre** : pas de contrainte, pas de conséquence négative en cas de refus.
- **Spécifique** : un consentement = une finalité.
- **Éclairé** : information préalable suffisante.
- **Univoque** : acte positif clair (case à cocher non précochée, clic explicite).
- **Démontrable** : preuve à conserver par le responsable.
- **Réversible** : retrait aussi simple que l'octroi.

**À utiliser quand** : prospection commerciale par email B2C, cookies non strictement nécessaires, données sensibles (avec consentement *explicite* art. 9.2.a), inscription newsletter.

**À éviter quand** il y a déséquilibre (employeur/salarié, autorité publique/citoyen) — un consentement « contraint » n'est pas libre.

### b) Exécution d'un contrat (art. 6.1.b)
Le traitement est nécessaire à l'exécution d'un contrat auquel la personne est partie, ou à des mesures précontractuelles à sa demande.

**À utiliser quand** : facturation d'un client, livraison d'une commande, gestion d'un compte utilisateur, paiement des salaires.

**Limite** : seulement ce qui est *objectivement indispensable* à l'exécution du contrat. Le profilage marketing ou la revente de données ne relèvent pas de cette base. La **CJUE (4 juill. 2023, Meta Platforms, C-252/21)** a jugé que la personnalisation de la publicité ne peut, en principe, être justifiée par la nécessité contractuelle d'un réseau social (lignes directrices CEPD 2/2019).

### c) Obligation légale (art. 6.1.c)
Le traitement est imposé par un texte de l'UE ou d'un État membre.

**À utiliser quand** : déclarations fiscales et sociales, lutte contre le blanchiment (KYC bancaire), obligations comptables, conservation des factures (10 ans Code de commerce), DPAE en RH.

**Pas valide** pour une obligation contractuelle ou un simple usage de marché.

### d) Sauvegarde d'intérêts vitaux (art. 6.1.d)
Pour sauver la vie de la personne ou d'un tiers.

**À utiliser quand** : urgence médicale sur une personne inconsciente, catastrophes humanitaires. Marginal en pratique commerciale.

### e) Mission d'intérêt public ou exercice de l'autorité publique (art. 6.1.e)
Réservé typiquement au secteur public et aux délégataires de service public.

**À utiliser quand** : état civil, registres publics, missions de service public confiées par texte.

### f) Intérêt légitime (art. 6.1.f)
Le traitement est nécessaire aux intérêts légitimes poursuivis par le responsable ou un tiers, **sauf si** prévalent les intérêts ou libertés et droits fondamentaux de la personne concernée (notamment si elle est un enfant).

**À utiliser quand** : sécurité du système d'information, prévention de la fraude, prospection commerciale B2B (avec opposition possible), enquêtes internes, vidéoprotection limitée.

**Test à trois conditions cumulatives** (CJUE et lignes directrices CEPD 1/2024) :
1. **Intérêt légitime** : licite, formulé de manière claire et précise, réel et actuel (pas hypothétique).
2. **Nécessité** : le traitement doit être **strictement nécessaire** à cet intérêt ; vérifie qu'aucun moyen moins intrusif ne permet d'atteindre le même objectif, et applique la minimisation.
3. **Mise en balance** : intérêts et droits de la personne, **attentes raisonnables** au moment de la collecte, nature des données, ampleur du traitement, garanties (opposition facile, pseudonymisation, transparence).

Documente ce test (« legitimate interest assessment / LIA ») dans le registre, avant le traitement.

**Jurisprudence et doctrine** :
- **CJUE, 4 oct. 2024, KNLTB, C-621/22** : un **intérêt purement commercial** (ici, communiquer les données des membres d'une fédération sportive à des sponsors contre rémunération) **peut** être un intérêt légitime, à condition de ne pas être contraire au droit. Mais la nécessité s'apprécie strictement (la fédération aurait pu demander l'accord des membres) et la mise en balance tient compte des attentes raisonnables des personnes.
- **CJUE, 4 juill. 2023, Meta Platforms, C-252/21** : la publicité personnalisée d'un réseau social, financée par la collecte massive de données hors plateforme, ne peut en principe reposer sur l'intérêt légitime face aux attentes des utilisateurs ; les autres intérêts invoqués (sécurité du réseau, amélioration du produit) ne justifient le traitement que s'il est strictement nécessaire, ce que le juge national vérifie.
- **Lignes directrices CEPD 1/2024 sur l'intérêt légitime** (adoptées le 9 octobre 2024 en version soumise à consultation, close le 20 novembre 2024) : analyse détaillée des trois conditions, avec des cas pratiques (prévention de la fraude, prospection directe, sécurité des systèmes d'information). À la date de rédaction, la version finale figure au programme de travail 2026-2027 du CEPD ; vérifie si elle a été publiée.
- **Avis CEPD 28/2024** (décembre 2024) sur les modèles d'IA : l'intérêt légitime **peut**, dans certains cas, fonder le développement ou le déploiement d'un modèle d'IA, sous réserve du test en trois étapes (voir `references/ai-act-rgpd.md`).

**Proposition Digital Omnibus (non adoptée)** : la proposition de la Commission du 19 novembre 2025 (COM(2025) 837) prévoit une disposition indiquant que le traitement de données pour développer et exploiter des systèmes d'IA peut relever de l'intérêt légitime, sous conditions. Le CEPD et le Contrôleur européen jugent cette disposition inutile (avis conjoint 2/2026) et les textes de compromis successifs au Conseil l'ont reformulée ou retirée selon les versions. **Au 1er octobre 2026, rien n'est adopté** : l'art. 6.1.f s'applique tel quel.

**Exclu** pour les autorités publiques dans l'exercice de leurs missions (art. 6.1 §2).

## Tableau de décision rapide

| Situation | Base la plus probable |
|---|---|
| Création de compte client / commande e-commerce | Contrat (b) |
| Newsletter / inscription marketing | Consentement (a) |
| Cookies analytics non exemptés | Consentement (art. 82 LIL), voir `references/consentement-cookies.md` |
| Cookies strictement nécessaires (panier) | Pas de consentement requis (exemption ePrivacy), base = intérêt légitime ou contrat |
| Paie, déclarations sociales | Obligation légale (c) |
| Vidéoprotection bureaux | Intérêt légitime (f) avec AIPD |
| Recrutement (CV reçus) | Mesures précontractuelles (b) puis intérêt légitime (f) pour le vivier |
| Prospection B2B | Intérêt légitime (f) + droit d'opposition |
| Prospection B2C par email/SMS | Consentement préalable (art. L. 34-5 CPCE), sauf « soft opt-in » (client, produits analogues) |
| Démarchage téléphonique B2C (depuis le 11 août 2026) | Consentement préalable (art. L. 223-1 C. consom.), sauf contrat en cours |
| Données de santé hors soin | Consentement *explicite* (9.2.a) ou base santé (9.2.h-i-j) |
| Service public administratif | Mission d'intérêt public (e) |

## Prospection électronique : la règle ePrivacy prime

Pour l'envoi d'e-mails ou de SMS de prospection, la règle spéciale (art. 13 ePrivacy, art. L. 34-5 CPCE) détermine si l'envoi est permis. **CJUE, 13 nov. 2025, Inteligo Media, C-654/23** : quand les conditions du « soft opt-in » (art. 13.2 ePrivacy) sont réunies, il **n'y a pas lieu** de rechercher en plus une base de l'art. 6.1 RGPD pour l'envoi. Les autres obligations du RGPD (information, durée de conservation, sécurité, droit d'opposition) restent applicables.

## Changer de base légale

Très difficile en cours de traitement. La CNIL et le CEPD considèrent qu'on ne peut pas passer du consentement à l'intérêt légitime pour « rattraper » un consentement non valide. Mieux vaut **choisir correctement dès le départ**.

## Information de la personne (art. 13-14)

La base légale choisie doit figurer dans l'information transmise à la personne (et, pour l'intérêt légitime, l'intérêt poursuivi : art. 13.1.d). Pour un modèle, voir `assets/information-personnes.md`.

## Sources

- [Article 6 RGPD — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- [Les bases légales — CNIL](https://www.cnil.fr/fr/les-bases-legales)
- [La licéité du traitement : essentiel sur les bases légales — CNIL](https://www.cnil.fr/fr/les-bases-legales/liceite-essentiel-sur-les-bases-legales)
- [Lignes directrices CEPD 2/2019 sur l'art. 6.1.b](https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-22019-processing-personal-data-under-article-61b_en)
- [Lignes directrices CEPD 1/2024 sur l'intérêt légitime (version de consultation)](https://www.edpb.europa.eu/system/files/2024-10/edpb_guidelines_202401_legitimateinterest_en.pdf)
- [Programme de travail CEPD 2026-2027](https://www.edpb.europa.eu/system/files/documents/2026-02/edpb_work-programme_2026-2027_en.pdf)
- [CJUE, 4 oct. 2024, KNLTB, C-621/22 — Curia](https://curia.europa.eu/juris/liste.jsf?language=en&td=ALL&num=C-621/22)
- [CJUE, 4 juill. 2023, Meta Platforms, C-252/21 — Curia](https://curia.europa.eu/juris/liste.jsf?num=C-252/21)
- [CJUE, 13 nov. 2025, Inteligo Media, C-654/23 — Curia](https://curia.europa.eu/juris/liste.jsf?language=en&num=C-654/23)
- [Proposition Digital Omnibus COM(2025) 837 — EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=COM%3A2025%3A837%3AFIN)
- [Avis conjoint 2/2026 du CEPD et du Contrôleur européen sur le Digital Omnibus](https://www.edpb.europa.eu/documents/legislative-opinion/edpb-edps-joint-opinion-22026-on-the-proposal-for-a-regulation-as_en)
