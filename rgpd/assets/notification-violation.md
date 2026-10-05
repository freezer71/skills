# Template — Notification de violation de données

*Modèle à adapter — ne pas publier brut.*

Trois documents en un :
1. **Notification CNIL** (article 33 RGPD) — via le téléservice de la CNIL ([notifications.cnil.fr](https://notifications.cnil.fr/notifications/)), réservé aux responsables de traitement ; la CNIL propose une **trame préparatoire** téléchargeable qui reprend les étapes du formulaire
2. **Information aux personnes concernées** (article 34) — si risque élevé
3. **Fiche d'inscription au registre interne** des violations (art. 33.5)

---

## 1. Notification à la CNIL (article 33)

**Règle en vigueur** : notifier **dans les meilleurs délais et, si possible, 72 heures au plus tard** après avoir pris connaissance de la violation, **sauf** si elle est peu susceptible d'engendrer un risque pour les droits et libertés (art. 33.1). Au-delà de 72 heures, joindre les **motifs du retard**. Si toutes les informations ne sont pas disponibles, procéder en **deux temps** : notification initiale, puis notification complémentaire (art. 33.4). Le sous-traitant, lui, alerte le responsable dans les meilleurs délais (art. 33.2). Méthode d'évaluation du risque et exemples : lignes directrices du CEPD 9/2022 et 01/2021 — voir `references/violations-donnees.md`.

> **Évolution annoncée, non applicable au 1er octobre 2026** : la proposition « Digital Omnibus » (COM(2025) 837) limiterait la notification à l'autorité aux violations susceptibles d'engendrer un **risque élevé**, porterait le délai à **96 heures** et créerait un **point d'entrée unique** européen (géré par l'ENISA) commun au RGPD, à NIS 2, à DORA, etc. Tant que ce texte n'est pas adopté et applicable, la règle des 72 heures et le seuil du « risque » s'appliquent.

### Informations administratives

| Champ | Valeur |
|---|---|
| Organisme | [Raison sociale, SIREN] |
| Adresse | [Adresse postale du siège] |
| Pays | France |
| Personne en charge | [Nom, fonction, email, téléphone] |
| DPO | [Nom, email, téléphone] |
| Type d'organisme | [Privé / Public ; le cas échéant OIV, OSE ou, après transposition de NIS 2, entité essentielle / importante] |
| Secteur d'activité | [Code NAF, secteur] |
| Sous-traitant impliqué | [Nom, date à laquelle il a alerté le responsable] |
| Autres États membres concernés | [Personnes concernées dans d'autres pays de l'UE ? — utile pour la coopération entre autorités] |

### Caractéristiques de l'incident

**Date de connaissance de la violation** : [JJ/MM/AAAA — HH:MM]

**Date de survenance estimée** : [JJ/MM/AAAA — ou « non déterminée »]

**Date et heure de la notification** : [JJ/MM/AAAA — HH:MM] — si plus de 72 h après la prise de connaissance, **motifs du retard** : [...]

**Type de notification** : ☐ Initiale (complément à suivre) / ☐ Complémentaire (réf. de la notification initiale : [...]) / ☐ Complète

**Origine de la détection** :
- ☐ Détection interne (SIEM, monitoring)
- ☐ Signalement par un salarié
- ☐ Signalement par un utilisateur
- ☐ Signalement par un sous-traitant
- ☐ Information externe (média, autorité, chercheur en sécurité)
- ☐ Autre : [...]

**Nature de la violation** (cocher tout ce qui s'applique) :
- ☐ Confidentialité (accès / divulgation non autorisés)
- ☐ Intégrité (altération non autorisée)
- ☐ Disponibilité (perte d'accès)

**Cause** :
- ☐ Action malveillante externe (cyberattaque, phishing, rançongiciel, exfiltration)
- ☐ Action malveillante interne (vol par un salarié, ancien collaborateur)
- ☐ Erreur humaine (mauvais destinataire, mauvaise configuration, perte)
- ☐ Défaillance technique
- ☐ Cause non identifiée à ce stade

**Description circonstanciée** :
[Décrire les faits dans un ordre chronologique :
- Comment l'incident s'est produit (technique : faille, méthode d'attaque, etc.) ;
- Quand il a été détecté et comment ;
- Quelles données ont été affectées ;
- Quelles personnes ont été affectées (catégories, volumétrie) ;
- L'incident est-il toujours en cours ?]

### Données concernées

**Catégories de données** :
- ☐ Identification (nom, prénom, adresse, email)
- ☐ Données techniques (IP, logs)
- ☐ Authentification (mots de passe — chiffrés / clair / hachés ?)
- ☐ Données contractuelles
- ☐ Données financières (RIB, transactions)
- ☐ Numéro de pièce d'identité / passeport
- ☐ Numéro de Sécurité sociale (NIR)
- ☐ Données de localisation
- ☐ Données sensibles (art. 9) : [préciser]
- ☐ Données pénales (art. 10) : [préciser]
- ☐ Autre : [...]

**Volumétrie approximative** :
- Nombre d'enregistrements : [...]
- Nombre de personnes concernées : [...]
- Catégories de personnes : [clients, salariés, prospects, etc.]

### Conséquences probables

[Détailler les impacts possibles sur les personnes :
- Atteinte à la vie privée
- Usurpation d'identité
- Phishing ciblé sur la base des données fuités
- Perte financière
- Discrimination
- Atteinte à la réputation
- Effets psychologiques]

### Évaluation du risque

- Pour les personnes : ☐ Faible / ☐ Moyen / ☐ Élevé
- Justification : [...]

**Information des personnes (art. 34)** : ☐ Effectuée / ☐ En cours / ☐ Pas requise — préciser pourquoi

### Mesures prises ou envisagées

**Mesures immédiates de confinement** :
- [Ex. Patch de la faille déployé le ____]
- [Ex. Comptes compromis désactivés]
- [Ex. Sauvegardes restaurées]
- [Ex. Mots de passe réinitialisés]

**Mesures correctives à moyen terme** :
- [Ex. Audit de sécurité externe planifié]
- [Ex. Renforcement des mécanismes d'authentification]
- [Ex. Formation accrue]

**Mesures pour atténuer l'impact sur les personnes** :
- [Ex. Information personnelle envoyée]
- [Ex. Réinitialisation forcée des mots de passe]
- [Ex. Surveillance d'usage anormal]

**Plainte pénale déposée** : ☐ Oui ([date], [parquet]) / ☐ Non / ☐ Envisagée

**Coordination avec d'autres autorités** :
- ☐ ANSSI (CERT-FR) — date : [...] *(notification d'incident distincte si l'organisme est soumis à NIS 2 ou au régime OIV/OSE : délais propres, plus courts)*
- ☐ Autorité sectorielle (ARS, ACPR, etc.) — date : [...]
- ☐ Préfecture (si OIV) — date : [...]

### Pièces jointes
- [Rapport d'analyse forensique]
- [Synthèse technique du fournisseur de cybersécurité]
- [Communication transmise aux personnes (si fait)]

---

## 2. Information aux personnes concernées (article 34)

À envoyer **dans les meilleurs délais** quand la violation est susceptible d'engendrer un **risque élevé** (art. 34.1), en des termes clairs et simples (art. 34.2).

Exceptions (art. 34.3) : données rendues incompréhensibles (chiffrement robuste dont la clé n'est pas compromise) ; mesures ultérieures ayant fait disparaître le risque élevé ; efforts disproportionnés — remplacés alors par une **communication publique** d'efficacité équivalente. La CNIL peut exiger l'information des personnes (art. 34.4).

### Modèle d'email

**Objet** : Information importante concernant la sécurité de vos données

Madame, Monsieur,

Nous tenons à vous informer en toute transparence d'un incident de sécurité affectant des données personnelles vous concernant.

**Ce qui s'est passé**
Le [date], nous avons découvert que [description simple et claire de la violation — pas de jargon].

**Quelles données sont concernées**
Les informations suivantes vous concernant ont été [exposées / consultées / divulguées] :
- [Liste explicite]

[Préciser ce qui **n'a pas** été affecté, s'il y a lieu — ex. mots de passe stockés sous forme hachée, pas de données bancaires concernées.]

**Quels risques pour vous**
Cet incident peut entraîner [risques concrets : tentatives de phishing, usurpation d'identité, etc.].

**Ce que nous avons fait**
Dès la détection, nous avons :
- [Action 1]
- [Action 2]
- [Action 3]

Nous avons également notifié l'incident à la Commission nationale de l'informatique et des libertés (CNIL) conformément à nos obligations légales.

**Contact**
Notre délégué à la protection des données (ou point de contact) : [nom, email, téléphone].

**Ce que nous vous recommandons**
- [Ex. Changer votre mot de passe sur notre service, et sur tout autre service où vous utiliseriez le même]
- [Ex. Activer l'authentification à deux facteurs]
- [Ex. Rester vigilant aux emails et appels suspects vous demandant vos identifiants ou des informations confidentielles]
- [Ex. Surveiller votre compte bancaire si données financières concernées]

**Votre droit à l'information**
Vous pouvez exercer vos droits (accès, rectification, effacement, opposition…) à tout moment en nous contactant à [email DPO].

Vous avez également le droit d'introduire une réclamation auprès de la CNIL : [www.cnil.fr/fr/plaintes](https://www.cnil.fr/fr/plaintes).

**Nous restons à votre disposition**
Pour toute question : [email dédié / téléphone] — équipe d'astreinte du [horaires].

Nous vous présentons nos sincères excuses pour cet incident et les inquiétudes qu'il peut générer. Soyez assuré(e) de notre engagement à protéger vos données et à tirer toutes les conséquences de cet événement.

[Nom, fonction]
[Société]

---

## 3. Fiche d'inscription au registre interne des violations (art. 33.5)

À conserver pour toutes les violations, y compris celles non notifiées à la CNIL.

| Champ | Valeur |
|---|---|
| Référence | VIO-AAAA-NNN |
| Date de survenance | |
| Date de détection | |
| Date de qualification | |
| Type (C/I/D) | Confidentialité / Intégrité / Disponibilité |
| Cause | |
| Description | |
| Données concernées | |
| Personnes concernées (catégories + volumétrie) | |
| Évaluation du risque | Faible / Moyen / Élevé |
| Notifiée CNIL ? | Oui — réf. [...] / Non — justification |
| Personnes informées ? | Oui / Non — justification |
| Mesures correctives | |
| Statut | Ouvert / Clos |
| Date de clôture | |
| Coût estimé | |
| Leçons apprises / Mise à jour AIPD | |

---

## Conseils

- **72h ce n'est pas long** (week-ends et jours fériés compris) : avoir une procédure interne pré-rédigée, un canal d'alerte connu, une équipe d'astreinte joignable, et la trame préparatoire de la CNIL déjà remplie pour la partie administrative.
- **Notification par étapes** possible : initiale rapide même incomplète, puis compléments.
- **Notifications multiples** : une même cyberattaque peut exiger, en parallèle, une notification RGPD à la CNIL, une notification NIS 2 ou DORA et un signalement sectoriel — chacune avec son délai. Le point d'entrée unique envisagé par le Digital Omnibus n'existe pas encore.
- **Honnêteté** : ne pas minimiser. La CNIL valorise la transparence et le sérieux de la réponse.
- **Coordination interne** : direction, com, juridique, IT, RH (si salariés concernés) — pré-aligner les messages.
- **Garder les traces** : logs, captures, analyse forensique. Précieux en cas de contrôle ultérieur.
