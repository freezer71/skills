# Données sensibles et particulières (Articles 9 et 10 RGPD)

L'article 9 pose une **interdiction de principe** du traitement de certaines catégories de données particulièrement intrusives, avec des exceptions strictes. L'article 10 encadre les données pénales. Ces régimes sont **plus stricts** que le régime général.

## Article 9.1 — Catégories interdites par principe

Sont interdits par principe le traitement des données qui révèlent :

1. **Origine raciale ou ethnique** (note : pas de race au sens biologique, mais perception sociale)
2. **Opinions politiques**
3. **Convictions religieuses ou philosophiques**
4. **Appartenance syndicale**
5. **Données génétiques** (caractéristiques héréditaires/acquises résultant d'analyse biologique)
6. **Données biométriques** *aux fins d'identifier une personne de manière unique* (empreinte, reconnaissance faciale, vocale, rétinienne)
7. **Données concernant la santé** (état physique ou mental, passé, présent, futur ; numéro de patient ; informations issues de tests)
8. **Données concernant la vie sexuelle ou l'orientation sexuelle**

**Précision sur la biométrie** : une photo n'est sensible **que si** elle est traitée par un dispositif technique permettant l'identification ou l'authentification unique (considérant 51). Une photo simple n'est pas sensible en soi, mais une photo passée par un système de reconnaissance faciale l'est.

### Une interprétation large par la CJUE : les données qui « révèlent » indirectement

La Cour de justice retient une conception extensive de l'art. 9.1. Raisonne en conséquence :
- **Déduction indirecte** : une donnée anodine devient sensible si elle permet de déduire une catégorie sensible par recoupement (le nom du conjoint ou partenaire révélant l'orientation sexuelle) — CJUE, 1er août 2022, OT, C-184/20.
- **Navigation et profilage** : la collecte de données de consultation de sites ou d'applications révélant des opinions, la santé ou l'orientation sexuelle relève de l'art. 9, même sans intention de catégoriser ; s'inscrire ou cliquer sur un site ne rend pas ces données « manifestement publiques » (art. 9.2.e) — CJUE, 4 juillet 2023, Meta Platforms c/ Bundeskartellamt, C-252/21.
- **Commandes en ligne** : les informations saisies pour commander un médicament, même non soumis à prescription, sont des données de santé — CJUE, 4 octobre 2024, Lindenapotheke, C-21/23.
- **Publicité ciblée** : une déclaration publique d'une personne sur son orientation sexuelle ne permet pas de traiter d'autres données relatives à cette orientation, collectées ailleurs, à des fins publicitaires — CJUE, 4 octobre 2024, Schrems c/ Meta, C-446/21.
- **Cumul art. 6 + art. 9** : une exception de l'art. 9.2 ne suffit pas, il faut aussi une base légale de l'art. 6 — CJUE, 21 décembre 2023, Krankenversicherung Nordrhein, C-667/21.
- **Plateformes de contenus** : l'exploitant d'une place de marché en ligne est responsable de traitement des données contenues dans les annonces ; il doit repérer **avant publication** les annonces contenant des données sensibles, vérifier que l'annonceur est la personne concernée ou dispose de son consentement explicite, et refuser la publication à défaut d'une autre exception — CJUE (grande chambre), 2 décembre 2025, Russmedia Digital, C-492/23.
- **Limite** : la publication du nom d'un sportif sanctionné pour dopage, de la durée et du motif de sa suspension n'est pas en principe une donnée de santé, sauf si la mention de la substance ou de la méthode interdite, combinée à d'autres informations, permet d'en déduire l'état de santé — CJUE (grande chambre), 14 juillet 2026, NADA Austria, C-474/24.

## Article 9.2 — Les 10 exceptions à l'interdiction

Le traitement de données sensibles n'est possible que si **l'une** des conditions suivantes est remplie ET, en parallèle, une base légale de l'article 6 (cumul confirmé par la CJUE, C-667/21, voir ci-dessus).

### a) Consentement explicite
**Standard plus élevé** que le consentement « ordinaire » (art. 7) : la personne doit consentir de manière non équivoque et active **pour ce traitement spécifique de données sensibles**. En pratique : case à cocher non précochée + libellé clair mentionnant explicitement la donnée sensible.

### b) Droit du travail, sécurité sociale, protection sociale
Si autorisé par le droit UE/national avec garanties (ex. déclarations sociales, médecine du travail).

### c) Intérêts vitaux de la personne
Quand elle est physiquement ou juridiquement incapable de consentir.

### d) Activités politiques, philosophiques, religieuses, syndicales
Par une fondation, association, organisme à but non lucratif, sur ses **membres ou anciens membres**, sans communication externe sans consentement.

### e) Données manifestement rendues publiques par la personne
*Exemple :* opinion politique tweetée publiquement. Interprétation stricte : la personne doit avoir eu l'intention explicite de rendre la donnée accessible au public (C-252/21).

### f) Constatation, exercice ou défense d'un droit en justice
Y compris instruction par les juridictions.

### g) Motif d'intérêt public important
Sur la base du droit UE/national, avec garanties. *Exemple récent :* l'**art. 4a de l'AI Act**, introduit par le règlement (UE) 2026/1744, permet de traiter des données sensibles dans la mesure strictement nécessaire à la **détection et à la correction des biais** des systèmes d'IA (voir `references/ai-act-rgpd.md`).

### h) Médecine préventive, médecine du travail, diagnostic médical, prise en charge sanitaire ou sociale
Sous la responsabilité d'un professionnel soumis au secret. **Base la plus utilisée en santé pour les soins courants**.

### i) Intérêt public en santé publique
Veille sanitaire, qualité et sécurité des soins, médicaments, dispositifs médicaux.

### j) Archivage, recherche scientifique ou historique, statistique
Avec garanties appropriées (pseudonymisation, accès restreint, comité d'éthique).

### Ce qui pourrait changer (proposition, non adoptée)
La proposition « Digital Omnibus » de la Commission (19 novembre 2025, COM(2025) 837) prévoit notamment une dérogation pour les **données sensibles résiduelles** présentes dans les données d'entraînement ou de test de l'IA, et une exception pour la **vérification biométrique** restant sous le contrôle exclusif de la personne. À l'automne 2026, ce texte est **toujours en négociation** : ne l'applique pas, et vérifie son statut avant d'en parler (voir `references/ai-act-rgpd.md`).

## Données de santé : cadre français et européen

### Formalités et hébergement
- **AIPD** obligatoire pour la plupart des traitements de données de santé à grande échelle (liste CNIL).
- **Recherche, étude, évaluation** dans le domaine de la santé (art. 66 et suivants LIL) : conformité à une **méthodologie de référence** CNIL (MR-001 à MR-008) ou, à défaut, autorisation de la CNIL. Les entrepôts de données de santé relèvent d'un **référentiel** CNIL dédié ou d'une autorisation.
- **Hébergement** : toute personne qui héberge des données de santé **pour le compte d'un tiers** (établissement, professionnel, éditeur d'application) doit être **certifiée HDS** (art. L. 1111-8 du Code de la santé publique). Un établissement qui héberge lui-même ses données n'a pas besoin de la certification, mais reste tenu par l'art. 32 RGPD.
- **Référentiel HDS v2** (arrêté publié au JO le 16 mai 2024, élaboré par l'Agence du numérique en santé) : il impose le **stockage des données dans l'EEE**, la transparence sur les **accès possibles depuis un pays tiers** (risque d'extraterritorialité, ex. Cloud Act) et une présentation standardisée des garanties. Les hébergeurs déjà certifiés avaient jusqu'au **16 mai 2026** pour migrer : exige désormais un certificat conforme à la v2.

### Plateforme des données de santé (Health Data Hub)
Hébergée depuis sa création chez Microsoft Azure, ce qui a suscité les critiques de la CNIL et du Conseil d'État sur l'exposition au droit américain, la plateforme fait l'objet d'une **migration vers un hébergeur qualifié SecNumCloud** annoncée par le Gouvernement en février 2026, avec un objectif de bascule fin 2026. Vérifie l'état d'avancement avant de l'affirmer comme acquise.

### Espace européen des données de santé (EHDS)
Le **règlement (UE) 2025/327**, publié au JOUE le 5 mars 2025, est entré en vigueur le **26 mars 2025**. Il s'applique par étapes :
- **26 mars 2027** : application générale du règlement (les obligations opérationnelles dépendent des actes d'exécution) ;
- **26 mars 2029** : **usage primaire** pour les premières catégories (résumé patient, prescription et dispensation électroniques) via MyHealth@EU, et **usage secondaire** (recherche, innovation, politiques publiques) via des organismes d'accès aux données de santé délivrant des permis ;
- **26 mars 2031** : autres catégories (imagerie, résultats de laboratoire, comptes rendus de sortie ; pour l'usage secondaire, certaines données comme les données génétiques et d'essais cliniques).

L'EHDS **complète** le RGPD sans le remplacer : il crée des droits renforcés d'accès et de contrôle pour les patients (dont un droit de retrait de l'usage secondaire) et une base légale encadrée pour la réutilisation, mais l'art. 9 reste applicable.

## Biométrie

### Au travail
- Le **règlement type CNIL** sur la biométrie au travail (2019) est la seule voie pour un contrôle d'accès biométrique par l'employeur (art. 9.4 RGPD et LIL) : justifier la nécessité (zones ou outils sensibles), privilégier un gabarit **sous le contrôle de la personne** (carte, terminal personnel), AIPD obligatoire.
- Le contrôle des **horaires** par biométrie est en principe disproportionné. Privilégie le badge nominatif.
- AI Act : la **reconnaissance des émotions** sur le lieu de travail est **interdite** depuis le 2 février 2025 (art. 5.1.f).

### Vidéoprotection « augmentée » (caméras algorithmiques)
- **Sans texte spécifique**, la CNIL considère les caméras augmentées comme illégales dès lors qu'elles traitent des données biométriques ou privent les personnes de leur droit d'opposition (position de juillet 2022).
- **Expérimentation législative** : l'art. 10 de la loi n° 2023-380 du 19 mai 2023 (JOP 2024) a autorisé, à titre expérimental, la détection d'événements prédéterminés par algorithme **sans reconnaissance faciale ni traitement biométrique** lors de grands événements. Une première prolongation a été censurée comme cavalier législatif (Conseil constitutionnel, 24 avril 2025, n° 2025-878 DC). L'**art. 47 de la loi n° 2026-201 du 20 mars 2026** relative aux JOP 2030 a rouvert et prolongé l'expérimentation **jusqu'au 31 décembre 2027**, validée avec réserves (décision n° 2026-902 DC du 19 mars 2026).
- **Reconnaissance faciale** : aucun texte ne l'autorise pour la vidéoprotection en France. Côté AI Act, l'identification biométrique en temps réel à des fins répressives dans l'espace public est interdite sauf exceptions (art. 5.1.h) et l'identification biométrique à distance relève du haut risque.

## Article 10 — Données pénales

Données relatives aux **condamnations pénales et infractions**, y compris mesures de sûreté.

**Régime français (LIL art. 46)** — peuvent traiter :
- Les juridictions, autorités publiques compétentes ;
- Les auxiliaires de justice pour les besoins de leur mission ;
- Les personnes physiques ou morales, aux fins de leur permettre de **préparer, exercer et suivre une action en justice** en tant que victime, mise en cause ou pour leur compte ;
- Les réutilisateurs de décisions de justice rendues publiques (sous conditions de open data) ;
- Les associations spécifiques (victimes, lutte contre les discriminations).

**Pratique RH** : l'extrait de casier judiciaire (bulletin n° 3) ne peut être demandé que pour les emplois **où la loi le prévoit** ou pour certains postes (sécurité, finance, sensibles). Pas de collecte généralisée.

## Cas pratiques

### Recrutement et données sensibles
- Pas de question sur la santé, religion, vie privée hors cadre strict du poste.
- Photo CV : pas obligatoire, n'a pas à être exigée.
- Tests psychologiques : finalité du poste, consentement éclairé, professionnel agréé.
- Outil d'IA de tri des CV : attention aux données sensibles **déduites** (C-184/20) et au régime haut risque de l'AI Act (voir `references/ai-act-rgpd.md`).

### Santé au travail
- Le médecin du travail traite des données de santé en vertu de l'art. 9.2.h (sous secret médical).
- L'employeur n'accède **pas** au dossier médical, seulement à l'avis d'aptitude.
- Absences pour arrêt maladie : motif médical pas communiqué à l'employeur.

### Application santé / e-santé
- Données de santé, y compris des données de bien-être lorsqu'elles permettent de déduire l'état de santé.
- AIPD obligatoire (liste CNIL).
- Hébergement par un **HDS** certifié selon le référentiel v2 si un prestataire héberge les données.
- Consentement explicite ou base 9.2.h selon contexte.
- Conformité aux référentiels d'interopérabilité et de sécurité de l'**Agence du numérique en santé (ANS)** si dans l'écosystème santé public ; anticipe l'EHDS si tu édites un logiciel de dossier médical.

### Données génétiques
- Tests généalogiques privés : enjeu RGPD majeur, transferts hors UE problématiques. En France, les tests génétiques « récréatifs » restent interdits (art. 16-10 du Code civil).
- En recherche : comité d'éthique + consentement explicite.

### Orientation sexuelle et identité de genre
- Collecte interdite sauf exception 9.2 (ex. associations LGBT pour leurs membres).
- Mention du genre ou de la civilité dans les formulaires : limiter à ce qui est nécessaire (souvent ne l'est pas — CJUE, 9 janvier 2025, Mousse, C-394/23, sur la minimisation).

## Sanctions spécifiques

Article 83.5 : amendes jusqu'à **20 M€ ou 4 % du CA mondial** pour manquement aux règles sur les données sensibles (catégorie la plus haute).

Cas marquants :
- **Clearview AI (CNIL, 2022)** : 20 M€ pour constitution d'une base de reconnaissance faciale par moissonnage d'images (pratique désormais interdite aussi par l'art. 5.1.e AI Act).
- **Cegedim Santé (CNIL, 2024)** : 800 000 € pour traitement de données de santé insuffisamment anonymisées sans autorisation.
- **Mercadona (AEPD, Espagne, 2021)** : environ 2,5 M€ pour reconnaissance faciale dans des supermarchés.
- Établissements de santé français : sanctions répétées pour défauts de sécurité sur les données de santé.

## Sources

- [RGPD, art. 9 et 10 — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- [Données sensibles — CNIL](https://www.cnil.fr/fr/definition/donnee-sensible)
- [Données de santé — CNIL](https://www.cnil.fr/fr/sante)
- [Biométrie sur les lieux de travail — CNIL](https://www.cnil.fr/fr/biometrie-sur-les-lieux-de-travail)
- [LIL art. 46 — Légifrance](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000886460)
- [Certification HDS — Agence du numérique en santé](https://esante.gouv.fr/ens/offre/hds)
- [Règlement (UE) 2025/327 — Espace européen des données de santé](https://eur-lex.europa.eu/eli/reg/2025/327/oj)
- [Règlement (UE) 2026/1744 — Digital Omnibus sur l'IA (art. 4a)](https://eur-lex.europa.eu/eli/reg/2026/1744/oj)
- [Conseil constitutionnel, décision n° 2026-902 DC du 19 mars 2026 (JOP 2030)](https://www.conseil-constitutionnel.fr/decision/2026/2026902DC.htm)
- [CJUE, Russmedia Digital, C-492/23 — EUR-Lex](https://eur-lex.europa.eu/legal-content/FR/TXT/?uri=CELEX:62023CJ0492)
- [CJUE, NADA Austria, C-474/24 — communiqué de presse](https://curia.europa.eu/site/upload/docs/application/pdf/2026-07/cp260103en.pdf)
