# Violations de données personnelles (articles 33-34 RGPD)

> À jour au 1er octobre 2026.

Une violation est tout incident **portant atteinte à la confidentialité, à l'intégrité ou à la disponibilité** des données personnelles. Elle peut résulter d'une action malveillante (piratage, vol, exfiltration) ou accidentelle (perte de matériel, erreur de destinataire, mauvaise configuration).

Pourquoi ces règles existent : la notification permet à l'autorité de vérifier que l'incident est maîtrisé, et l'information des personnes leur permet de se protéger (changer un mot de passe, surveiller leur compte bancaire, se méfier de l'hameçonnage). Un incident caché ne protège personne et aggrave la sanction.

**Ordre de grandeur** : la CNIL a reçu **6 167 notifications en 2025** (record, + 9,5 %), dont une sur deux due à un piratage. Ses trois constats : personne n'est épargné, les violations sont de plus en plus massives, et elles impliquent souvent des prestataires.

## Définition (art. 4.12)

> Une violation de la sécurité entraînant, de manière accidentelle ou illicite, la destruction, la perte, l'altération, la divulgation non autorisée de données à caractère personnel transmises, conservées ou traitées d'une autre manière, ou l'accès non autorisé à de telles données.

### Trois dimensions
- **Confidentialité** : accès ou divulgation non autorisés. *Exemples :* courriel envoyé au mauvais destinataire, vol de base, scraping.
- **Intégrité** : altération non autorisée. *Exemples :* modification frauduleuse d'enregistrements, données corrompues.
- **Disponibilité** : perte d'accès. *Exemples :* rançongiciel chiffrant les données sans exfiltration, suppression accidentelle sans sauvegarde.

Un rançongiciel qui **chiffre** sans exfiltrer constitue déjà une violation de disponibilité.

## Article 33 — Notification à la CNIL (droit en vigueur)

### Délai : 72 heures
À compter du moment où le responsable **a connaissance** de la violation, c'est-à-dire lorsqu'il a une certitude raisonnable qu'un incident de sécurité a compromis des données personnelles (un simple soupçon ouvre une courte phase d'enquête, pas un report indéfini).

### Quand notifier
Toute violation, **sauf** si elle n'est **pas susceptible d'engendrer un risque** pour les droits et libertés des personnes. La logique est donc : on notifie, sauf à pouvoir démontrer l'absence de risque.

**Évaluation du risque** (lignes directrices du CEPD 9/2022, version 2.0 du 28 mars 2023) :
- nature, sensibilité et volume des données ;
- facilité d'identification des personnes ;
- gravité des conséquences possibles (usurpation d'identité, fraude, discrimination, préjudice financier, atteinte à la réputation, perte de contrôle) ;
- caractéristiques des personnes (mineurs, personnes vulnérables) ;
- caractéristiques du responsable (un établissement de santé ou une banque n'expose pas aux mêmes risques).

### Contenu de la notification (art. 33.3)
- nature de la violation, **catégories et nombre approximatif** de personnes et d'enregistrements concernés ;
- coordonnées du DPO ou d'un autre point de contact ;
- conséquences probables ;
- mesures prises ou envisagées pour remédier à la violation et en atténuer les effets.

Notification **par étapes** possible (art. 33.4) : notification initiale dans les 72 h, puis compléments au fil de l'enquête.

### Hors délai
Au-delà de 72 h : notifier quand même, en motivant le retard. Une notification tardive reste préférable à une absence de notification, qui est un manquement autonome sanctionné.

### Modalité
Téléservice de la CNIL : [notifications.cnil.fr](https://notifications.cnil.fr). Utilise le modèle `assets/notification-violation.md` pour préparer les informations.

**Formulaire européen commun en préparation** : le 10 juin 2026, le CEPD a adopté un **modèle commun de notification** (environ 120 champs structurés), soumis à consultation publique jusqu'au 5 août 2026. Il est destiné à être intégré par les autorités dans leurs propres téléservices. Ce n'est pas une nouvelle obligation : le contenu exigé reste celui de l'art. 33.3. Tant que la CNIL n'a pas annoncé de changement, continue d'utiliser son téléservice.

### Registre interne des violations (art. 33.5)
**Toutes les violations** doivent être documentées dans un registre interne, y compris celles qui ne sont pas notifiées (en motivant pourquoi). Ce registre est contrôlable par la CNIL, et son absence est sanctionnée en tant que telle (sanction simplifiée du 4 sept. 2025 contre un éditeur de logiciel de recrutement : « obligation de documenter une violation »).

Contenu : faits, effets, mesures correctrices, et raisonnement sur le risque.

## Article 34 — Information des personnes concernées (droit en vigueur)

### Quand
Si la violation est **susceptible d'engendrer un risque élevé** pour les droits et libertés des personnes. La CNIL peut l'ordonner si le responsable ne l'a pas fait (art. 34.4 et 58.2.e).

### Délai
**Dans les meilleurs délais.**

### Contenu (art. 34.2)
En **termes clairs et simples** :
- nature de la violation ;
- coordonnées du DPO ou du point de contact ;
- conséquences probables ;
- mesures prises pour remédier à la violation et en atténuer les effets ;
- conseils concrets aux personnes (changer de mot de passe, vigilance face à l'hameçonnage, opposition sur un IBAN, surveillance des prélèvements…).

**Ce que sanctionne la CNIL** : un message qui ne permet pas de comprendre directement les conséquences ni les gestes de protection. Free et Free Mobile (janv. 2026) ont été sanctionnés notamment parce que leur courriel aux abonnés ne contenait pas toutes les informations de l'art. 34.2, même si un numéro vert complétait le dispositif. Le premier message doit se suffire à lui-même.

**Toutes les personnes concernées** : pense aux personnes dont les données figurent dans le fichier sans être tes clients directs. L'Hôpital privé de la Loire (sept. 2026) a informé ses patients mais pas les 202 246 « tiers de confiance » dont les données avaient aussi été volées : manquement à l'art. 34.

### Exemptions (art. 34.3)
Pas d'information individuelle si :
- a) les données étaient chiffrées (clé non compromise) ou rendues autrement inintelligibles ;
- b) des mesures ultérieures rendent le risque élevé improbable ;
- c) l'information individuelle exigerait des efforts disproportionnés : une **communication publique** (communiqué, site web) la remplace alors.

### Format
Courriel, courrier, notification dans l'application, SMS. **Jamais noyée dans une infolettre ou des CGU.**

## Ce que dit la jurisprudence sur la responsabilité après une violation

- **Une attaque ne prouve pas à elle seule une faute, mais c'est au responsable de prouver ses mesures** (CJUE, C-340/21, 14 déc. 2023). Il ne suffit pas de dire « nous avons été victimes » : il faut démontrer que les mesures de l'art. 32 étaient adaptées.
- **La crainte d'une utilisation abusive peut être un dommage moral** indemnisable (C-340/21), de même que la perte de contrôle sur ses données (C-200/23, 4 oct. 2024), sans seuil de gravité (C-300/21, 4 mai 2023). En revanche, le risque purement hypothétique ne suffit pas quand le tiers n'a pas pris connaissance des données (C-687/21, MediaMarktSaturn, 25 janv. 2024).
- **Les sanctions CNIL récentes visent toujours les mêmes failles** : authentification d'accès distant sans facteur fort (VPN de Free, accès des médecins libéraux à l'Hôpital privé de la Loire, comptes Cap Emploi chez France Travail), habilitations trop larges, absence de détection des comportements anormaux. Si tes AIPD identifient une mesure de sécurité, déploie-la : France Travail a été sanctionné parce que les mesures prévues dans ses AIPD n'avaient jamais été mises en œuvre.

Voir `references/sanctions-jurisprudence.md` pour le détail des décisions.

## Procédure interne recommandée

### 1. Détection
- Sources : SIEM, alertes de journalisation, signalement d'un utilisateur, prestataire qui notifie.
- Canal d'alerte interne connu de tous (« si vous suspectez un incident, prévenez… »).

### 2. Qualification (dans les 24 h)
- Est-ce vraiment une violation de données personnelles ?
- Étendue : quelles données, combien de personnes, exfiltration ou simple accès ?

### 3. Évaluation du risque
- Pour les personnes : usurpation, fraude, discrimination ?
- Pour la sécurité : la faille est-elle encore exploitée ?

### 4. Notification à la CNIL (≤ 72 h)
- Si risque : téléservice.
- Si absence de risque démontrée : inscription au registre interne avec motivation.

### 5. Information des personnes
- Si risque élevé : information individuelle (ou publique en cas d'effort disproportionné), complète dès le premier message.

### 6. Mesures correctives
- Correctif, révocation des accès, renouvellement des identifiants, fermeture des comptes compromis.

### 7. Investigation post-incident
- Cause racine, enseignements, mise à jour des AIPD et du registre, formation.

### 8. Communication externe (au cas par cas)
- Médias, partenaires, et régulateurs sectoriels (voir ci-dessous).

### 9. Coordination avec les autorités
- Plainte au procureur en cas d'infraction (intrusion, vol, extorsion) ; le parquet « cyber » de Paris traite les cas les plus graves.
- Données de santé : signalement des incidents graves de sécurité des systèmes d'information de santé (art. L. 1111-8-2 du Code de la santé publique) via le portail de signalement des événements sanitaires, en plus de la notification à la CNIL.

## Autres régimes de notification à articuler

Une même attaque peut déclencher plusieurs obligations, chacune avec son destinataire et son délai. Elles **s'ajoutent** à la notification RGPD, elles ne la remplacent pas.

- **NIS 2 (directive (UE) 2022/2555)** : alerte précoce sous 24 h, notification sous 72 h, rapport final sous un mois pour les incidents importants des entités essentielles et importantes (art. 23). **En France, la directive n'est toujours pas transposée au 1er octobre 2026** : le projet de loi « relatif à la résilience des infrastructures critiques et au renforcement de la cybersécurité » (adopté par le Sénat le 12 mars 2025) attend son examen en séance à l'Assemblée nationale, et la Commission a saisi la CJUE contre la France pour défaut de transposition en juillet 2026. D'ici l'entrée en vigueur de la loi, les obligations antérieures demeurent (opérateurs d'importance vitale, opérateurs de services essentiels de NIS 1, déclarations à l'ANSSI).
- **DORA (règlement (UE) 2022/2554)** : applicable depuis le 17 janvier 2025 aux entités financières ; les incidents majeurs liés aux TIC se déclarent à l'autorité financière compétente (ACPR, AMF).
- **Opérateurs de communications électroniques** : obligations spécifiques issues de la directive ePrivacy et du Code des postes et des communications électroniques.

## Proposition en cours : le « Digital Omnibus » (pas du droit en vigueur)

Le 19 novembre 2025, la Commission a proposé un règlement « Digital Omnibus » (COM(2025) 837, procédure 2025/0360(COD)) qui modifierait notamment l'art. 33 :
- notification à l'autorité **seulement en cas de risque élevé** (même seuil que l'art. 34) ;
- délai porté de 72 h à **96 heures** ;
- **guichet unique de notification des incidents**, mis en place en modifiant NIS 2 et géré par l'ENISA, commun au RGPD, à NIS 2 et à d'autres textes sectoriels ;
- un **modèle commun** de notification et une **liste commune des circonstances de risque élevé** préparés par le CEPD.

**Statut au 1er octobre 2026** : simple proposition. Au Parlement européen, les commissions ITRE et LIBE ont publié un projet de rapport le 22 juin 2026 et plus de 1 750 amendements ont été déposés. Au Conseil, le vote du Coreper sur le mandat de négociation prévu le 26 juin 2026 a été annulé et la présidence irlandaise travaille sur des textes de compromis. Aucun trilogue n'est ouvert. **Applique donc toujours les 72 h et le seuil actuel** (notification sauf absence de risque). Ne conseille jamais d'attendre 96 h ou de ne pas notifier un risque « non élevé » sur la base de ce projet.

## Cas types

### Courriel envoyé au mauvais destinataire
- Violation de confidentialité.
- Risque selon le contenu (RIB ou données de santé : risque élevé ; nom seul : faible).
- Action : demander la suppression, obtenir une confirmation écrite, consigner au registre.

### Vol d'un ordinateur professionnel chiffré
- Violation de disponibilité (et de confidentialité si le chiffrement est faible).
- Chiffrement robuste (FileVault, BitLocker) et clé non compromise : généralement pas de notification, mais inscription au registre.

### Hameçonnage réussi donnant accès aux données de 50 000 clients
- Violation grave, exfiltration probable.
- Notification à la CNIL et information des personnes (risque d'usurpation et d'hameçonnage ciblé).

### Rançongiciel sans exfiltration
- Violation de disponibilité.
- Notifier si l'indisponibilité a des effets sur les personnes (impossibilité d'accéder à un service, continuité des soins ou d'un service public). En pratique, l'exfiltration est rarement exclue avec certitude au début : notifie à titre conservatoire et complète ensuite.

### Sous-traitant victime d'une attaque
- Le **sous-traitant notifie le responsable dans les meilleurs délais** (art. 33.2).
- Le responsable notifie ensuite la CNIL ; ses 72 h courent à partir du moment où il a connaissance de la violation.
- Le contrat (art. 28) doit prévoir ce circuit et un délai court. Voir `references/sous-traitants.md`.
- Le sous-traitant est lui-même sanctionnable : Mobius Solutions (1 M€, déc. 2025) pour avoir conservé et réutilisé les données de Deezer après la fin du contrat, à l'origine d'une fuite ; Nexpublica France (1,7 M€, déc. 2025) pour la sécurité insuffisante d'un logiciel.

### Exposition par mauvaise configuration (bucket S3 public, Elasticsearch sans authentification)
- Violation à part entière, même sans preuve d'accès par un tiers.
- Notifier et analyser les journaux pour estimer l'exposition réelle.

### Fuite massive chez un organisme public
- Exemple : la violation du système d'information de la DGFiP rendue publique le 14 août 2026 (données fiscales et cadastrales), notifiée à la CNIL avec information individuelle des personnes. La CNIL a précisé qu'il était inutile de lui adresser des plaintes individuelles, car elle était déjà saisie.

## Sanctions

Un manquement aux art. 32, 33 ou 34 relève du premier palier : jusqu'à **10 M€ ou 2 % du chiffre d'affaires annuel mondial** (art. 83.4.a). Le défaut de sécurité s'accompagne souvent d'autres manquements (conservation excessive, art. 5.1.e), qui relèvent du second palier (20 M€ ou 4 %).

Décisions marquantes liées à des violations :
- **Free Mobile (27 M€) et Free (15 M€)**, 13 janv. 2026 : intrusion d'octobre 2024 touchant 24 millions de contrats, dont des IBAN. Manquements à la sécurité (art. 32 : authentification VPN insuffisante, détection inefficace) et à l'information des personnes (art. 34 : courriel incomplet) ; conservation excessive des données d'anciens abonnés pour Free Mobile. Injonction d'achever les mesures de sécurité sous trois mois.
- **France Travail (5 M€)**, 22 janv. 2026 : intrusion du premier trimestre 2024 par ingénierie sociale via des comptes de conseillers Cap Emploi, touchant les données de toutes les personnes inscrites depuis 20 ans (dont le NIR). Manquement à l'art. 32 ; injonction sous astreinte de 5 000 € par jour.
- **Hôpital privé de la Loire (500 000 €)**, 3 sept. 2026 : accès au dossier patient informatisé à l'été 2025 (524 867 patients, 202 246 tiers de confiance). Manquements aux art. 32 et 34.
- **DPC irlandaise, Permanent TSB** (30 avril 2026) : prises de contrôle de comptes clients via le centre d'appels ; 250 000 € pour la sécurité (art. 5.1.f et 32.1) et 27 500 € pour la notification hors délai (art. 33.1). Le retard de notification est sanctionné séparément.

## Sources

- [Notifier une violation de données personnelles — CNIL](https://www.cnil.fr/fr/services-en-ligne/notifier-une-violation-de-donnees-personnelles)
- [Les violations de données personnelles — CNIL](https://www.cnil.fr/fr/violations-de-donnees-personnelles-les-regles-suivre)
- [Rapport annuel 2025 de la CNIL (6 167 notifications)](https://www.cnil.fr/fr/rapport-annuel-2025)
- [Sanction Free Mobile et Free — CNIL](https://www.cnil.fr/fr/sanction-free-2026)
- [Sanction France Travail — CNIL](https://www.cnil.fr/fr/violation-de-donnees-sanction-5millions-france-travail)
- [Sanction Hôpital privé de la Loire — CNIL](https://www.cnil.fr/fr/sanction-hopital-prive-loire)
- [Sanction Mobius Solutions — CNIL](https://www.cnil.fr/fr/violation-de-donnees-sanction-dun-million-deuros-lencontre-de-la-societe-mobius-solutions-ltd)
- [Piratage de la DGFiP : les vérifications sont en cours — CNIL](https://www.cnil.fr/fr/piratage-du-systeme-dinformation-des-impots-les-verifications-sont-en-cours)
- [Cybermois 2026 : que faire en 3 étapes après une violation — CNIL](https://www.cnil.fr/fr/cybermois-2026)
- [Lignes directrices 9/2022 sur la notification des violations — CEPD](https://www.edpb.europa.eu/documents/guideline/guidelines-92022-on-personal-data-breach-notification-under-gdpr_en)
- [Lignes directrices 01/2021, exemples de violations — CEPD](https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-012021-examples-regarding-personal-data-breach_en)
- [Modèle commun de notification — consultation publique du CEPD](https://www.edpb.europa.eu/public-consultations/template-for-personal-data-breach-notification_en)
- [CEPD : adoption du modèle commun (10 juin 2026)](https://www.edpb.europa.eu/news/edpb-meets-with-eu-commissioner-mcgrath-and-adopts-common-data-breach-notification-template_en)
- [Proposition Digital Omnibus, COM(2025) 837 — Commission européenne](https://digital-strategy.ec.europa.eu/en/library/digital-omnibus-regulation-proposal)
- [Suivi législatif du Digital Omnibus — Parlement européen](https://www.europarl.europa.eu/legislative-train/theme-a-new-plan-for-europe-s-sustainable-prosperity-and-competitiveness/file-digital-package)
- [Saisine de la CJUE contre la France pour défaut de transposition de NIS 2 — Commission européenne](https://ec.europa.eu/commission/presscorner/detail/en/ip_26_1499)
- [DPC — décision Permanent TSB](https://www.dataprotection.ie/en/dpc-guidance/decisions/inquiry-permanent-TSB-april-2026)
- [Articles 33 et 34 du RGPD — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
