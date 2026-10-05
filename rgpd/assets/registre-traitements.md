# Template — Registre des activités de traitement (Article 30 RGPD)

*Modèle à adapter — ne pas publier brut.*

Ce modèle est à **adapter au contexte réel** (secteur, taille, traitements effectifs). Il suit l'article 30.1 du RGPD **en vigueur** et le modèle de registre de la CNIL.

> **Qui doit tenir un registre ?** En droit en vigueur au 1er octobre 2026, toute organisation, sauf celles de **moins de 250 salariés** dont les traitements sont à la fois occasionnels, sans risque et sans données sensibles ou pénales (art. 30.5) — en pratique, presque toutes. La proposition « Omnibus IV » (COM(2025) 501) relèverait ce seuil (750 salariés dans la proposition, 1 000 selon l'accord provisoire du 9 juin 2026) en maintenant l'obligation pour les traitements à **risque élevé** ; elle n'est pas encore applicable. Même exempté, un registre reste le moyen le plus simple de démontrer la conformité (art. 5.2 et 24). Voir `references/obligations-responsable.md`.

## Métadonnées du registre

- **Organisation** : [Raison sociale, SIREN]
- **Adresse** : [Adresse postale]
- **Représentant légal** : [Nom, fonction]
- **DPO / Point de contact** : [Nom, email, téléphone — numéro de désignation CNIL « DPO-… » le cas échéant]
- **Représentant dans l'UE** (art. 27, si responsable établi hors UE) : [Nom, coordonnées]
- **Date de création** : [JJ/MM/AAAA]
- **Date de dernière mise à jour** : [JJ/MM/AAAA]
- **Responsable de la tenue** : [Nom, fonction]

## Fiche de traitement type

Dupliquer cette fiche pour chaque traitement.

---

### Fiche N° [XX] — [Intitulé du traitement]

#### 1. Identification

| Champ | Valeur |
|---|---|
| Référence interne | TR-XXX |
| Date de création | JJ/MM/AAAA |
| Date de dernière revue | JJ/MM/AAAA |
| Direction / Service responsable | [ex. Direction Commerciale] |
| Pilote opérationnel | [Nom, fonction] |

#### 2. Finalités

Finalité principale : *[ex. Gestion de la relation client et exécution des commandes]*

Finalités secondaires éventuelles :
- *[ex. Analyse statistique anonymisée du parcours d'achat]*
- *[ex. Prospection commerciale auprès des clients existants pour produits analogues]*

#### 3. Base légale (art. 6)

*Non exigée par l'art. 30.1, mais recommandée par la CNIL : la mentionner facilite l'information des personnes et la démonstration de conformité.*


- ☐ Consentement (a)
- ☐ Exécution d'un contrat (b)
- ☐ Obligation légale (c) — préciser le texte
- ☐ Sauvegarde d'intérêts vitaux (d)
- ☐ Mission d'intérêt public (e)
- ☐ Intérêt légitime (f) — joindre LIA

#### 4. Catégories de personnes concernées

- *[ex. Clients personnes physiques]*
- *[ex. Représentants des clients personnes morales]*
- *[ex. Prospects ayant manifesté un intérêt]*

#### 5. Catégories de données

**Données d'identification** : nom, prénom, adresse, email, téléphone.

**Données professionnelles** (si pertinent) : fonction, employeur.

**Données financières** : RIB, historique d'achats, encours, scoring.

**Données comportementales** : pages visitées, clics, ouverture emails.

**Données sensibles (art. 9)** : ☐ Aucune / ☐ … (préciser et base légale 9.2)

**Données pénales (art. 10)** : ☐ Aucune / ☐ … (préciser)

#### 6. Origine des données

- ☐ Collecte directe auprès de la personne
- ☐ Source tierce (préciser) : *[ex. fichier acheté à X, partenaire Y, registre public Z]*

#### 7. Destinataires

**Internes** : *[ex. service commercial, comptabilité, service après-vente]*

**Externes (sous-traitants)** :
- *[ex. Hébergeur — OVHcloud, France — DPA signé le JJ/MM/AAAA]*
- *[ex. Solution CRM — Salesforce, EU + US (DPF) — DPA signé le JJ/MM/AAAA]*
- *[ex. Cabinet comptable — XXX, France — DPA signé le JJ/MM/AAAA]*

**Externes (autres responsables)** :
- *[ex. Banque pour traitement des paiements]*
- *[ex. Transporteur pour livraison]*
- *[ex. Administration fiscale]*

#### 8. Transferts hors UE

☐ Aucun / ☐ Oui (compléter)

| Destinataire | Pays | Mécanisme | Documentation |
|---|---|---|---|
| *AWS* | *États-Unis* | *DPF + CCT (Module 2)* | *DPA AWS du JJ/MM/AAAA, TIA réf. TIA-001* |

#### 9. Durée de conservation

| Phase | Durée | Localisation |
|---|---|---|
| Base active | *3 ans après dernière interaction* | *CRM* |
| Archivage intermédiaire | *5 ans (obligation fiscale)* | *Espace d'archivage à accès restreint* |
| Archivage définitif | *NA* | *NA* |
| Suppression / Anonymisation | *Automatique au terme* | *Procédure de purge mensuelle* |

#### 10. Mesures de sécurité (description générale)

**Techniques** :
- Chiffrement TLS pour les transferts.
- Chiffrement au repos (AES-256) sur le CRM et les sauvegardes.
- Authentification multi-facteurs sur les comptes admin.
- Cloisonnement réseau (VLAN).
- Sauvegardes quotidiennes testées trimestriellement.
- Journalisation des accès aux données sensibles.
- Mises à jour de sécurité (mensuelles minimum).

**Organisationnelles** :
- Charte informatique signée par tous les collaborateurs.
- Formation RGPD annuelle obligatoire.
- Gestion des arrivées/départs (révocation des accès sous 24h).
- Politique de mots de passe (12+ caractères, MFA).
- NDA pour intervenants externes.

#### 11. AIPD

☐ Pas requise (justification : *[ex. traitement figurant sur la liste CNIL des AIPD non requises ; moins de deux des 9 critères du CEPD]*)
☐ Requise — réalisée le JJ/MM/AAAA (référence AIPD-XXX)
☐ Requise — en cours

#### 12. Information des personnes

- ☐ Politique de confidentialité (URL : ...)
- ☐ Mention sur formulaire (capture d'écran archivée)
- ☐ Note d'information remise au client à la signature du contrat

#### 13. Exercice des droits

- Procédure : [référence document]
- Délai de réponse moyen constaté : [JJ jours]

---

## Annexes du registre

### Annexe A — Liste des sous-traitants et DPA

| Sous-traitant | Service | Localisation | Date signature DPA | Échéance | Sous-traitants ultérieurs autorisés |
|---|---|---|---|---|---|
| | | | | | |

### Annexe B — Liste des AIPD

| Référence | Traitement | Date | Statut | Risques résiduels | Date de revue |
|---|---|---|---|---|---|
| | | | | | |

### Annexe C — Registre des violations (art. 33.5)

| Date | Type | Données | Personnes | Risque | Notifié CNIL | Notifié personnes | Actions correctives |
|---|---|---|---|---|---|---|---|
| | | | | | | | |

Y inscrire **toutes** les violations, y compris celles non notifiées à la CNIL parce que peu susceptibles d'engendrer un risque, avec la justification de ce choix. Détail : voir `assets/notification-violation.md`.

### Annexe D — Référentiel des durées de conservation

| Catégorie | Base active | Archivage | Justification |
|---|---|---|---|
| Données prospects | 3 ans à compter de la collecte ou du dernier contact émanant du prospect | NA | Référentiel CNIL « gestion des activités commerciales » |
| Données clients | Durée de la relation commerciale + 3 ans (prospection) | Pièces comptables et factures : 10 ans (art. L. 123-22 C. com.) ; données utiles aux contentieux : prescription applicable | Code de commerce, Code civil |
| Données salariés — paie | Durée du contrat | Double des bulletins de paie : 5 ans (art. L. 3243-4 C. trav.) | Code du travail, référentiel CNIL « gestion du personnel » |
| CV non retenus | 2 ans après le dernier contact, sauf opposition du candidat | NA | Référentiel CNIL recrutement |
| Vidéoprotection | 1 mois maximum en principe | NA (sauf procédure en cours) | Recommandation CNIL |

*Ces durées sont des repères courants : vérifie le texte ou le référentiel applicable à chaque cas (des durées sectorielles plus longues ou plus courtes existent).*

## Conseils d'usage

- Format **vivant** : mettre à jour à chaque nouveau traitement ou évolution.
- **Granularité raisonnable** : un traitement = un objectif principal. Pas une fiche par champ collecté.
- **Lisible** par un non-expert : éviter le jargon interne sans définition.
- **Versionner** : conserver l'historique pour traçabilité.
- **Outils** : modèle de registre de la CNIL ou tableur pour démarrer, logiciel dédié si la volumétrie le justifie.
- **Disponibilité** : le registre doit pouvoir être communiqué à la CNIL sur demande (art. 30.4) ; garde une version exportable à jour.
