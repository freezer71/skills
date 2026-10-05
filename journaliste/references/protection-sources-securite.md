# Protection des sources et sécurité

Protéger ses sources n'est pas un confort, c'est la condition d'existence du journalisme d'intérêt public. Sans garantie de confidentialité, personne ne révèle un scandale, une fraude ou un abus de pouvoir : le risque de représailles dissuade tout témoin. La protection des sources est donc moins un privilège du journaliste qu'un **droit du public à être informé**. Cette fiche explique pourquoi cette protection est vitale, ses limites en droit français, et les pratiques concrètes — numériques et de terrain — pour ne jamais trahir une promesse.

## Pourquoi protéger les sources est vital

- **Pas de source protégée, pas d'information sensible.** Les révélations qui dérangent (corruption, pollution, maltraitance, malversations) viennent presque toujours de personnes vulnérables : salariés, agents publics, lanceurs d'alerte. Si leur identité fuite, elles se taisent — et l'information meurt avant d'exister.
- **Un devoir déontologique.** La Charte de Munich (1971) en fait le **devoir n° 7** : « Garder le secret professionnel et ne pas divulguer la source des informations obtenues confidentiellement. » Voir `references/deontologie.md`.
- **Un principe protégé par le droit.** En France, le secret des sources est consacré à l'**article 2 de la loi du 29 juillet 1881 sur la liberté de la presse**, dans sa rédaction issue de la **loi du 4 janvier 2010** relative à la protection du secret des sources des journalistes. Voir `references/droit-presse.md`.
- **Un droit garanti en Europe.** La Cour européenne des droits de l'homme rattache la protection des sources à la liberté d'expression (article 10 de la Convention). L'arrêt fondateur **Goodwin c. Royaume-Uni (1996)** pose qu'une atteinte au secret des sources doit répondre à un « impératif prépondérant d'intérêt public » : sans cette protection, la presse ne peut plus jouer son rôle de « chien de garde » de la démocratie.

Retiens le principe directeur : **une promesse de confidentialité ne se renie jamais.** Avant de la donner, mesure ta capacité réelle à la tenir ; une fois donnée, elle t'engage absolument, y compris face à la pression judiciaire.

## Portée et limites du secret en droit français

Le secret des sources est un principe fort, mais **non absolu**. Le comprendre évite deux erreurs symétriques : promettre l'impossible, ou renoncer trop vite face à une pression.

- **Le principe** : nul ne peut contraindre un journaliste à révéler ses sources ; la protection s'étend aux personnes qui, par leur activité, contribuent à l'information (collaborateurs de la rédaction).
- **L'exception** : il peut y être porté atteinte **à titre exceptionnel**, lorsqu'un **impératif prépondérant d'intérêt public** le justifie et que les mesures envisagées sont **strictement nécessaires et proportionnées**.
- **Le contrôle du juge** : une telle atteinte se fait sous le contrôle de l'autorité judiciaire, garante des libertés. Les actes d'enquête visant indirectement à identifier une source (perquisition, interception, réquisition de données de connexion) sont eux aussi encadrés.
- **Ce que cela implique pour toi** : tu ne maîtrises pas le cadre légal, mais tu maîtrises ce que tu détiens. Moins tu conserves d'éléments permettant d'identifier une source, moins une réquisition ou une perquisition peut nuire. La meilleure protection juridique est doublée d'une **hygiène technique** rigoureuse.

**Ne confonds pas deux secrets distincts.** Le *secret des sources* protège l'identité de qui t'a informé (article 2 de la loi de 1881, issu de la loi du 4 janvier 2010). Le *secret de l'instruction* (article 11 du Code de procédure pénale) protège, lui, la confidentialité d'une enquête pénale en cours et lie ceux qui **concourent à la procédure** — pas le journaliste, qui peut publier une information couverte par ce secret s'il ne l'a pas obtenue par un acte répréhensible, sous réserve des autres limites (présomption d'innocence, vie privée). Surtout, l'exception au secret des sources ne peut **jamais** te contraindre à livrer directement une source : seules des mesures indirectes (réquisition de données de connexion, géolocalisation, perquisition) peuvent être ordonnées, sous le contrôle du juge. En cas de réquisition, de perquisition ou d'assignation, **ne réponds pas seul : préviens immédiatement la direction de la rédaction et un avocat spécialisé en droit de la presse.**

Pour le détail des textes, des procédures et de la jurisprudence française, voir `references/droit-presse.md`.

## Sécurité numérique : réduire la surface d'exposition

Une source n'est pas trahie seulement par une indiscrétion : elle l'est par les **métadonnées et les traces** que laissent les outils numériques. Le réflexe : limiter ce qui existe, chiffrer ce qui subsiste, cloisonner ce qui circule.

| Risque | Trace laissée | Bonne pratique |
| --- | --- | --- |
| Appel, SMS | Numéro, horodatage, géolocalisation des bornes | Messagerie chiffrée de bout en bout (**Signal**) ; éviter le téléphone nominatif |
| E-mail | En-têtes, IP, serveurs, copies | Limiter les échanges sensibles ; chiffrer ; ne jamais nommer la source |
| Documents reçus | Métadonnées d'auteur, filigranes, identifiants imprimante | « Nettoyer » les métadonnées ; recopier l'information plutôt que diffuser le fichier brut |
| Stockage | Disque, cloud, sauvegardes | **Chiffrement** des supports ; pas de cloud grand public pour le sensible |
| Déplacements | Géolocalisation du smartphone, badges, péages | Couper/laisser le téléphone ; cloisonner un appareil dédié |

Quelques principes structurants :

- **Métadonnées d'abord.** Le contenu d'un message peut être chiffré, mais le simple fait que vous ayez communiqué (qui, quand, combien de temps) peut suffire à identifier une source. Réduisez le nombre de contacts traçables.
- **Messageries chiffrées.** Signal (chiffrement de bout en bout, messages éphémères) pour les échanges courants ; vérifiez l'identité du correspondant hors ligne quand l'enjeu est élevé.
- **Boîtes de dépôt sécurisées.** Pour recevoir des documents sans connaître l'identité de l'émetteur, des plateformes type **SecureDrop** ou **GlobaLeaks** (via le réseau Tor) permettent un dépôt anonyme. Elles protègent la source même de la rédaction.
- **Chiffrement et cloisonnement.** Chiffrez disques et clés USB. Cloisonnez : un appareil « propre » pour le sensible, distinct de l'usage personnel, pour qu'une compromission n'expose pas tout.
- **Prudence permanente.** Désactivez la géolocalisation lors des rendez-vous sensibles ; méfiez-vous des e-mails et des sauvegardes automatiques qui dupliquent l'information à votre insu.

La sécurité numérique n'est pas une affaire d'experts : c'est une discipline quotidienne. Le maillon faible est presque toujours une habitude, pas un logiciel.

## Gérer un lanceur d'alerte

Un lanceur d'alerte prend des risques personnels, professionnels et parfois juridiques considérables. Votre première responsabilité est de **ne pas aggraver son exposition**.

- **Protéger son identité avant tout.** Avant même d'évaluer son information, sécurisez le canal de contact. Ne créez aucune trace inutile ; ne révélez son existence à personne, pas même en interne sans nécessité.
- **Évaluer les motivations sans le trahir.** Un lanceur d'alerte peut agir par conviction, par rancune ou par intérêt : cela ne disqualifie pas l'information, mais impose de **recouper** rigoureusement (voir `references/verification-recoupement.md` et `references/methodologie-enquete.md`). Vérifier n'est pas suspecter ; c'est protéger la source d'une publication fragile.
- **Connaître le cadre légal de l'alerte.** En France, le statut du lanceur d'alerte découle de la **loi du 9 décembre 2016 dite « Sapin II »**, renforcée par la **loi du 21 mars 2022 dite « loi Waserman »** (qui transpose la directive européenne de 2019). Ces textes définissent qui peut alerter, sur quoi, selon quelles modalités, et organisent une **protection contre les représailles**. Connaître ce cadre vous aide à orienter la personne — sans vous substituer à un conseil juridique.
- **Être clair sur ce que vous pouvez garantir.** Expliquez à la source ce que vous protégerez, et ce qui échappe à votre contrôle. Une promesse honnête vaut mieux qu'une assurance illusoire.

## Précautions de terrain

La sécurité physique précède la sécurité numérique : une source repérée en votre compagnie est déjà compromise.

- **Zones sensibles.** Préparez vos déplacements (conflits, manifestations, milieux fermés) : itinéraires, contacts de secours, matériel minimal. Évaluez le risque avant, pas pendant.
- **Contacts à risque.** Choisissez le lieu et l'heure d'un rendez-vous pour qu'il ne soit ni observé ni enregistré. Évitez les habitudes prévisibles.
- **Discrétion.** Ne prenez pas de notes nominatives exploitables ; codez les identités ; ne photographiez pas une source sans nécessité et sans consentement éclairé.

## Protocole en cas de perquisition ou de réquisition

Réfléchir à froid à ce scénario évite la panique le jour venu — et limite ce que l'on peut vous prendre.

1. **Restez calme et courtois**, mais ne facilitez aucune identification de source.
2. **Exigez le cadre.** Une perquisition dans une rédaction ou au domicile d'un journaliste obéit à des règles renforcées ; en principe un magistrat est présent. Notez les références de l'acte.
3. **Faites valoir le secret des sources** : indiquez que des éléments sont couverts par la protection légale et demandez l'assistance de la direction de la rédaction et d'un avocat.
4. **N'effacez rien dans la précipitation** : la destruction de preuves vous expose ; la bonne défense est la **prévention en amont** (ne pas accumuler ce qui identifie une source).
5. **Documentez** le déroulement (qui, quoi, quand) pour un éventuel recours.
6. **Réquisition de données** (connexion, factures, géolocalisation) : elle aussi encadrée et contrôlée par le juge ; ne communiquez pas spontanément d'informations au-delà de l'acte. Voir `references/droit-presse.md`.

La meilleure réponse à une perquisition se prépare des mois plus tôt, par une hygiène stricte : moins vous détenez d'éléments compromettants, moins une saisie peut nuire à votre source.

## Sources

- [Charte de Munich (devoirs et droits) — SNJ](https://www.snj.fr/article/charte-d%C3%A9thique-professionnelle-des-journalistes-1086375069)
- [Conseil de déontologie journalistique et de médiation (CDJM)](https://cdjm.org/)
- [Loi du 29 juillet 1881 sur la liberté de la presse — Légifrance](https://www.legifrance.gouv.fr/loda/id/LEGITEXT000006070722/)
- [Loi du 4 janvier 2010 (protection du secret des sources) — Légifrance](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000021601312/)
- [Loi « Sapin II » du 9 décembre 2016 — Légifrance](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000033558528/)
- [Loi « Waserman » du 21 mars 2022 — Légifrance](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000045348441)
- [Arrêt CEDH Goodwin c. Royaume-Uni (1996) — HUDOC](https://hudoc.echr.coe.int/fre?i=001-62570)
- [Reporters sans frontières — sécurité des journalistes](https://rsf.org/fr)
- [GIJN — boîte à outils sécurité numérique et sources](https://gijn.org/fr/)
- [Fédération internationale des journalistes (IFJ)](https://www.ifj.org/fr)
