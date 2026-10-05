# Consentement et cookies

Deux régimes se croisent :
- Le **RGPD** (art. 4.11, 7) pour le consentement en général ;
- La **directive ePrivacy 2002/58/CE** (art. 5.3, transposé à l'art. 82 LIL en France) pour les **cookies et traceurs** sur le terminal des utilisateurs, et son art. 13 (transposé à l'art. L. 34-5 CPCE) pour la **prospection électronique**.

La CNIL contrôle les deux. **Les cookies restent l'un des premiers motifs de sanction** : en 2025, 21 organismes ont été sanctionnés pour des manquements aux règles sur les traceurs, dont Google (325 M€) et Shein (150 M€) en septembre 2025.

**État du droit au 1er octobre 2026** : la directive ePrivacy et l'art. 82 LIL s'appliquent toujours. La proposition de **règlement ePrivacy** (2017) a été **retirée** par la Commission (retrait publié au JOUE le 6 octobre 2025). La proposition **« Digital Omnibus »** (novembre 2025), qui déplacerait les règles cookies dans le RGPD, **n'est pas adoptée** (voir plus bas). Ne présente jamais ses mesures comme du droit applicable.

## Critères de validité du consentement (Article 7 + 4.11 RGPD)

Un consentement valide est :

### Libre
- Pas de pression, pas de conséquence négative en cas de refus.
- Pas de déséquilibre marqué (employeur/salarié, autorité publique/administré).
- **Cookie wall** (« accepter ou partir ») : pas interdit par principe en France, mais apprécié au cas par cas par la CNIL ; il doit exister une alternative réelle et équitable. Pour les modèles « accepter ou payer », voir la section *Pay or consent* ci-dessous.

### Spécifique
- Un consentement = une finalité.
- **Granularité** : pas de bloc « j'accepte tout » sans alternative.

### Éclairé
- Information préalable claire, simple, accessible.
- Identité du responsable, finalités précises, droit de retrait, conséquences du refus.

### Univoque
- **Acte positif clair** : clic sur un bouton, case à cocher non précochée, signature.
- **Pas valide** : poursuite de navigation, case précochée, silence, inaction.

### Démontrable
- Le responsable doit pouvoir prouver que la personne a consenti et à quoi (art. 7.1).
- Tracer : date, version d'information, finalités acceptées, IP/identifiant.
- Conserver les preuves le temps de l'utilité + délai de prescription.

### Réversible
- Retrait **aussi simple** que l'octroi (art. 7.3).
- Pas de réversion compliquée (lien désinscription enterré, formulaire papier alors que consentement était par clic).
- Information sur le retrait avant consentement.

## Consentement explicite (cas particuliers)

Pour les **données sensibles** (art. 9.2.a) et certaines **décisions automatisées** (art. 22.2.c) : standard renforcé. En pratique, une case à cocher avec libellé sans ambiguïté mentionnant la donnée sensible et la finalité.

## Mineurs (Article 8 RGPD + 45 LIL)

- Services de la société de l'information offerts directement à un enfant.
- Âge de consentement autonome en France : **15 ans**.
- En-dessous : consentement conjoint du titulaire de l'autorité parentale + mineur.
- Vérification d'âge proportionnée (la simple déclaration peut suffire dans certains cas).

Recommandations CNIL sur les droits numériques des mineurs : information adaptée à l'âge, recueil progressif de consentement, garanties renforcées.

## « Pay or consent » (accepter ou payer)

- **Avis CEPD 08/2024** (17 avril 2024), visant les **grandes plateformes en ligne** : dans la plupart des cas, le choix binaire « consentir à la publicité comportementale ou payer » ne permet pas un consentement valide. Propose une **alternative équivalente gratuite** (par exemple une publicité non comportementale) ; si une redevance est demandée, elle ne doit pas dissuader le choix libre. Le CEPD a annoncé des lignes directrices plus larges sur ces modèles.
- **Décision de la Commission du 23 avril 2025 (DMA, art. 5.2)** : Meta sanctionnée de **200 M€** pour son modèle binaire sur Facebook et Instagram (période mars-novembre 2024), faute d'offrir une option équivalente utilisant moins de données. Meta s'est engagée (décembre 2025) à proposer à partir de janvier 2026 un choix entre publicité entièrement personnalisée et publicité moins personnalisée.
- **Pour un éditeur ordinaire** (hors contrôleur d'accès DMA) : la CNIL admet un dispositif « accepter ou payer » sous conditions (critères publiés en 2022 : alternative réelle, **prix raisonnable** justifié au cas par cas, traceurs limités aux finalités qui permettent de rémunérer équitablement le service). Documente le raisonnement ; évite d'étendre le paiement à des traceurs sans lien avec la monétisation.

## Cookies et traceurs (art. 82 LIL, ex-art. 32-II)

### Champ
**Toute opération** de lecture ou écriture d'information sur le terminal d'un utilisateur (cookies HTTP, local storage, SDK mobile, fingerprinting, pixels, SDK in-app, pixels dans les e-mails).

### Régime
**Consentement préalable** sauf exemption pour les traceurs :
- **Strictement nécessaires** à la fourniture d'un service expressément demandé (panier, authentification, sécurité, équilibrage de charge, préférences linguistiques).
- **De mesure d'audience** sous conditions strictes : finalité limitée à la mesure d'audience du site ou de l'application, **pour le compte exclusif de l'éditeur**, production de **statistiques anonymes** uniquement, pas de suivi de navigation inter-sites ni de recoupement, pas de transmission à des tiers, durée de vie des traceurs limitée à **13 mois** (non prorogée automatiquement), données conservées **25 mois** au plus, information dans la politique de confidentialité. La CNIL publie un **outil d'auto-évaluation** pour les fournisseurs de solutions (juillet 2025).

### Lignes directrices et recommandation CNIL (délibérations 2020-091 et 2020-092, recommandation consolidée janvier 2026)

**Obligations du bandeau cookies** :

1. **Information préalable** : identité, finalités, possibilité de refuser.
2. **Refuser doit être aussi simple qu'accepter** : un bouton « Tout refuser » au même niveau que « Tout accepter » (pas caché dans un second écran).
3. **Granularité** : choix par finalité (mesure d'audience, publicité, réseaux sociaux, personnalisation).
4. **Pas de dépôt avant le choix** : aucun traceur non exempté avant l'expression du consentement.
5. **Retrait facile** : icône permanente, lien en pied de page.
6. **Durée du choix** : conserve le choix (acceptation **comme refus**) pendant une durée raisonnable — la CNIL retient **6 mois** comme référence — sans redemander entre-temps.
7. **Conservation des preuves** du consentement.

### Recommandations CNIL récentes (droit souple, mais grille de contrôle)

- **Consentement multi-terminaux** (recommandation finale publiée le 16 janvier 2026, intégrée à la recommandation cookies consolidée) : en environnement connecté (compte utilisateur), si un seul consentement vaut pour tous les terminaux, le **refus et le retrait doivent avoir la même portée et la même simplicité** ; affiche un message temporaire sur un nouveau terminal pour rappeler la portée du choix ; règle les conflits de choix (priorité au dernier choix exprimé ou aux préférences du compte, selon la méthode retenue). La CNIL a annoncé des travaux en 2026 sur le consentement **multi-propriétés** (plusieurs sites d'un même groupe).
- **Pixels de suivi dans les courriels** (délibération 2026-042 du 12 mars 2026, publiée le 14 avril 2026) : le pixel qui mesure l'ouverture d'un e-mail relève de l'art. 82 LIL. **Consentement requis** en principe (notamment pour mesurer l'ouverture à des fins de ciblage ou de personnalisation). **Exemptions** : mesure individuelle de la **délivrabilité** liée à un service demandé (par exemple retirer des listes les destinataires inactifs) et fonctions de sécurité ou d'authentification ; e-mails transactionnels liés au service demandé. **Mesure transitoire** : pour les adresses collectées avant la publication, informe les destinataires dans les **3 mois** et permets-leur de s'opposer facilement.
- **Applications mobiles** (recommandation de 2024, mise à jour en 2025) : répartition des responsabilités entre éditeur, développeur, fournisseurs de SDK et magasins d'applications ; le consentement aux traceurs (SDK, identifiants publicitaires) se recueille dans l'application, distinctement des permissions du système d'exploitation.

### Cas pratiques sanctionnés (pour contexte)
- **Google (délibération du 1er sept. 2025, publiée le 3 sept.) — 325 M€** : publicités affichées entre les courriels Gmail (onglets « Promotions » et « Réseaux sociaux ») sans consentement = **prospection directe par courrier électronique** (art. L. 34-5 CPCE) ; traceurs publicitaires déposés à la création d'un compte Google sans consentement libre et éclairé (art. 82 LIL). Astreinte de 100 000 € par jour de retard.
- **Shein (1er sept. 2025) — 150 M€** : cookies déposés sans consentement, refus non respecté, information défaillante.
- **Procédure simplifiée (2025-2026)** : bandeaux incomplets (finalités, identité du responsable, modalités de refus), traceurs déposés avant toute action, absence de refus en un clic alors que l'acceptation se fait en un clic.

### Outils techniques
- **CMP** (Consent Management Platform) conforme (par exemple IAB TCF v2.2, à vérifier au regard des exigences CNIL et de la jurisprudence).
- **Vérification** : outils de développement du navigateur (onglets Réseau et Stockage), extensions d'inspection des cookies.
- **Test de conformité** : naviguer en refusant tout — aucun traceur non exempté ne doit se déposer ni être lu, aucun appel vers un tiers publicitaire.

## Proposition « Digital Omnibus » (non adoptée)

**Proposition de règlement COM(2025) 837 du 19 novembre 2025** (procédure 2025/0360(COD)). Ce qu'elle prévoit pour les traceurs :
- **Nouvel art. 88a RGPD** : le stockage ou l'accès à des données personnelles sur le terminal relèverait du RGPD (et non plus de l'art. 5.3 ePrivacy) ; consentement en principe.
- **Exemptions élargies** (« liste blanche ») : transmission d'une communication, service expressément demandé, **mesure d'audience agrégée** par l'éditeur pour son propre usage, **maintien ou rétablissement de la sécurité** du service ou du terminal.
- **Refus en un clic**, choix respecté **au moins 6 mois**.
- **Nouvel art. 88b RGPD** : préférences exprimées par des **signaux automatisés et lisibles par machine** (par exemple réglés dans le navigateur), que les sites devraient respecter.

**Statut au 1er octobre 2026** : la proposition est en **première lecture**. Au Parlement, les commissions LIBE et ITRE ont publié leur projet de rapport le 22 juin 2026 (plus de 1 750 amendements déposés), sans vote. Au Conseil, le vote du mandat de négociation prévu en juin 2026 a été annulé, les discussions continuent sous présidence irlandaise ; aucun trilogue n'a commencé. Le CEPD et le Contrôleur européen de la protection des données (avis conjoint 2/2026, février 2026) **soutiennent** l'objectif de réduire les bandeaux et les signaux lisibles par machine. Le texte final peut beaucoup changer : **appuie-toi sur l'art. 82 LIL et la doctrine CNIL actuelle**.

## Cas particuliers de consentement marketing

### Prospection commerciale par e-mail et SMS en B2C (art. L. 34-5 CPCE, art. 13 ePrivacy)
- **Consentement préalable** obligatoire (opt-in).
- **Exception « soft opt-in »** : coordonnées recueillies auprès de la personne à l'occasion d'une vente ou d'une prestation, pour des produits ou services **analogues** du même responsable, avec opposition possible à la collecte et à chaque envoi.
- **CJUE, 13 nov. 2025, Inteligo Media, C-654/23** : une newsletter à contenu éditorial adressée individuellement pour promouvoir une offre payante est une communication de **prospection directe** ; l'ouverture d'un compte **gratuit** qui donne accès à une offre commerciale peut constituer une « vente » au sens de l'exception ; quand l'art. 13.2 ePrivacy s'applique, il **n'y a pas lieu de chercher en plus une base légale de l'art. 6 RGPD** pour l'envoi.
- Une publicité affichée dans une messagerie sous la forme d'un courriel est de la prospection électronique (sanction Google, septembre 2025).

### Prospection B2B
- **Intérêt légitime possible** (pas de consentement) si :
  - E-mail professionnel générique (`contact@`, `info@`) : possible.
  - E-mail nominatif (`jean.dupont@`) : possible si l'objet de la sollicitation est en lien avec la fonction professionnelle, avec opposition possible.
- Lien d'opposition obligatoire à chaque envoi.

### Téléphone, courrier postal
- **Démarchage téléphonique** (art. L. 223-1 C. consom., réécrit par l'art. 13 de la loi n° 2025-594 du 30 juin 2025) : **depuis le 11 août 2026, consentement préalable obligatoire** (opt-in) du consommateur ; le régime d'opposition **Bloctel a pris fin**. Le consentement doit être libre, spécifique, éclairé, univoque, révocable, et prouvé par le professionnel. Exceptions : sollicitation dans le cadre d'un **contrat en cours** et en rapport avec son objet (y compris produits complémentaires), fourniture de journaux et périodiques. Interdiction maintenue pour la rénovation énergétique et l'adaptation du logement (hors contrat en cours).
- **Automates d'appel** : consentement préalable (L. 34-5 CPCE).
- **Postal** : opt-out (liste Robinson), base intérêt légitime.

## Erreurs fréquentes à éviter

1. **« Accepter ou payer »** sans alternative réelle ni prix raisonnable — consentement non libre.
2. **Pré-coché** : non valide.
3. **Continuation de navigation** assimilée à consentement — non valide.
4. **Granularité absente** : « j'accepte les cookies » sans détail des finalités.
5. **Dépôt avant choix** : tag manager qui charge un outil d'analytics non exempté dès la première visite.
6. **Pas de mécanisme de retrait** : seulement vider le navigateur (insuffisant).
7. **Choix non mémorisé** : redemander à chaque visite après un refus, ou ne jamais réinterroger après acceptation.
8. **Pixels de suivi** dans les newsletters sans information ni consentement.
9. **Appliquer le Digital Omnibus par anticipation** : ses exemptions ne sont pas en vigueur.

Pour la base légale des traitements en aval des traceurs, voir `references/bases-legales.md`.

## Sources

- [Cookies et autres traceurs : les règles — CNIL](https://www.cnil.fr/fr/cookies-et-autres-traceurs/regles/cookies)
- [Lignes directrices et recommandation cookies — CNIL](https://www.cnil.fr/fr/cookies-et-autres-traceurs/regles/cookies/lignes-directrices-modificatives-et-recommandation)
- [Recommandation cookies consolidée (janvier 2026) — CNIL](https://www.cnil.fr/sites/default/files/2026-01/recommandation_cookies_consolidee.pdf)
- [FAQ cookies — CNIL](https://www.cnil.fr/fr/cookies-et-autres-traceurs/regles/cookies/FAQ)
- [Consentement multi-terminaux : recommandations finales — CNIL](https://www.cnil.fr/fr/cookies-et-autres-traceurs-recommandations-finales-sur-le-consentement-multi-terminaux)
- [Pixels de suivi dans les courriers électroniques : recommandation — CNIL](https://www.cnil.fr/fr/recommandation-pixel-suivi-courriels)
- [Cookies : solutions pour les outils de mesure d'audience — CNIL](https://www.cnil.fr/fr/cookies-solutions-pour-les-outils-de-mesure-daudience)
- [Sanction Google 325 M€ — CNIL](https://www.cnil.fr/fr/publicites-inserees-entre-les-courriels-et-cookies-la-cnil-sanctionne-google-dune-amende-de-325)
- [Sanction Shein 150 M€ — CNIL](https://www.cnil.fr/fr/cookies-deposes-sans-consentement-la-cnil-sanctionne-shein-dune-amende-de-150-millions-deuros)
- [Sanctions et mesures correctrices 2025 — CNIL](https://www.cnil.fr/en/sanctions-and-corrective-measures-cnils-actions-2025)
- [Cookie walls : premiers critères d'évaluation — CNIL](https://www.cnil.fr/fr/cookies-et-autres-traceurs/regles/cookie-walls/la-cnil-publie-des-premiers-criteres-devaluation)
- [Lignes directrices CEPD 05/2020 sur le consentement](https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-052020-consent-under-regulation-2016679_en)
- [Avis CEPD 08/2024 « Consent or pay »](https://www.edpb.europa.eu/system/files/2024-04/edpb_opinion_202408_consentorpay_en.pdf)
- [Décision DMA Apple et Meta (23 avril 2025) — Commission](https://digital-strategy.ec.europa.eu/en/news/commission-finds-apple-and-meta-breach-digital-markets-act)
- [Engagements de Meta (8 déc. 2025) — Commission](https://digital-markets-act.ec.europa.eu/meta-commits-give-eu-users-choice-personalised-ads-under-dma-2025-12-08_en)
- [Proposition Digital Omnibus COM(2025) 837 — EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=COM%3A2025%3A837%3AFIN)
- [Digital Package, FAQ — Commission](https://digital-strategy.ec.europa.eu/en/faqs/digital-package)
- [Suivi législatif Digital Omnibus — Parlement européen](https://www.europarl.europa.eu/legislative-train/theme-a-new-plan-for-europe-s-sustainable-prosperity-and-competitiveness/file-digital-package)
- [Avis conjoint 2/2026 du CEPD et du Contrôleur européen sur le Digital Omnibus](https://www.edpb.europa.eu/documents/legislative-opinion/edpb-edps-joint-opinion-22026-on-the-proposal-for-a-regulation-as_en)
- [Retrait du règlement ePrivacy — Parlement européen](https://www.europarl.europa.eu/legislative-train/theme-connected-digital-single-market/file-jd-e-privacy-reform)
- [CJUE, 13 nov. 2025, Inteligo Media, C-654/23 — Curia](https://curia.europa.eu/juris/liste.jsf?language=en&num=C-654/23)
- [Art. 82 Loi Informatique et Libertés — Légifrance](https://www.legifrance.gouv.fr/loda/article_lc/LEGIARTI000037813978/)
- [Art. L. 223-1 Code de la consommation (version au 11 août 2026) — Légifrance](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000051830285/2026-08-11)
- [Démarchage téléphonique : consentement obligatoire — DGCCRF](https://www.economie.gouv.fr/dgccrf/actualites-dgccrf/le-demarchage-telephonique-desormais-interdit-si-vous-ny-avez-pas-consenti)
