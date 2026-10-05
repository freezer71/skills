# Template — Analyse d'Impact relative à la Protection des Données (AIPD/DPIA)

*Modèle à adapter — ne pas publier brut.*

Structure conforme à l'article 35 du RGPD et à la méthodologie de la CNIL (guides « AIPD 1 : la méthode », « AIPD 2 : les modèles », « AIPD 3 : les bases de connaissances » et logiciel PIA).

L'AIPD est obligatoire lorsque le traitement est susceptible d'engendrer un **risque élevé**. Avant de démarrer, vérifie :
1. les cas de l'art. 35.3 ;
2. la **liste CNIL des traitements pour lesquels une AIPD est requise** (14 types, délibération n° 2018-327) ;
3. la **liste CNIL des traitements pour lesquels elle n'est pas requise** (12 types, délibération n° 2019-118) ;
4. à défaut, les **9 critères** du CEPD : deux critères réunis justifient en principe une AIPD.

Voir `references/obligations-responsable.md`.

> **Droit en vigueur / évolution annoncée** : la proposition « Digital Omnibus » (COM(2025) 837, 19 novembre 2025) remplacerait les listes nationales par des **listes européennes uniques** et un **modèle commun** d'AIPD préparés par le CEPD. Au 1er octobre 2026, elle est en première lecture : utilise les listes de la CNIL. Si un modèle européen est adopté, reporte le contenu de cette trame dans ce modèle.

---

## Analyse d'Impact relative à la Protection des Données

| Champ | Valeur |
|---|---|
| Référence | AIPD-XXX |
| Traitement | [Intitulé] |
| Responsable de traitement | [Société] |
| Pilote AIPD | [Nom, fonction] |
| DPO consulté | [Nom, date] |
| Personnes concernées consultées | ☐ Non / ☐ Oui : [méthode] |
| Date de réalisation | [JJ/MM/AAAA] |
| Date de prochaine revue | [JJ/MM/AAAA] |
| Statut | ☐ En cours / ☐ Validée / ☐ Consultation préalable CNIL |

## 1. Description systématique du traitement

### 1.1 Contexte
[Pourquoi ce traitement existe, dans quel projet/produit, qui est concerné.]

### 1.2 Finalités
**Finalité principale** : [...]

**Finalités secondaires** :
- [...]

### 1.3 Périmètre fonctionnel
[Décrire les processus métier impactés, les fonctionnalités, les acteurs.]

### 1.4 Acteurs et rôles
- **Responsable de traitement** : [...]
- **Sous-traitants** : [...]
- **Destinataires** : [...]
- **Personnes concernées** : nombre estimé, catégories, vulnérabilité éventuelle.

### 1.5 Données traitées
| Catégorie | Type | Source | Caractère obligatoire |
|---|---|---|---|
| | | | |

### 1.6 Cycle de vie des données
- **Collecte** : comment, où, par qui ?
- **Stockage** : où physiquement, qui y accède ?
- **Utilisation** : par qui, comment ?
- **Transfert** : à qui, où, comment ?
- **Conservation** : durées par phase.
- **Suppression** : modalités, journalisation.

### 1.7 Supports
- Applications, bases de données, serveurs, postes, supports papier, sauvegardes.

## 2. Évaluation de la nécessité et de la proportionnalité

### 2.1 Base légale (art. 6)
[Justifier le choix.]

### 2.2 Finalités déterminées, explicites et légitimes
[Démontrer.]

### 2.3 Minimisation des données
[Pourquoi chaque donnée est nécessaire. Données collectées « au cas où » à éliminer.]

### 2.4 Exactitude
[Mécanismes de mise à jour et de correction.]

### 2.5 Durée de conservation
[Justification.]

### 2.6 Information des personnes
[Mentions prévues, accessibilité.]

### 2.7 Exercice des droits
[Modalités d'exercice, contact, délais.]

### 2.8 Sous-traitants
[Vérification de la conformité, DPA en place.]

### 2.9 Transferts hors UE
[Mécanisme, garanties, TIA si applicable.]

## 3. Évaluation des risques pour les droits et libertés

### Méthodologie
Identifier les **événements redoutés** (accès illégitime, modification non désirée, disparition de données) et leurs sources (sources humaines internes, externes, non humaines).

Pour chaque risque, évaluer :
- **Gravité** (négligeable / limitée / importante / maximale) — impact sur les personnes.
- **Vraisemblance** (négligeable / limitée / importante / maximale) — probabilité.

### 3.1 Risque : Accès illégitime aux données

**Sources** :
- [Ex. Pirate informatique externe]
- [Ex. Salarié curieux non autorisé]
- [Ex. Sous-traitant peu sécurisé]

**Impacts potentiels sur les personnes** :
- [Ex. Usurpation d'identité, atteinte à la vie privée, discrimination, perte financière]

**Gravité brute** : [Limitée / Importante / Maximale]

**Vraisemblance brute** : [Limitée / Importante]

**Mesures existantes** :
- [Chiffrement, MFA, journalisation, formation, contrôle d'accès]

**Gravité résiduelle** : [...]

**Vraisemblance résiduelle** : [...]

### 3.2 Risque : Modification non désirée des données

[Même structure]

### 3.3 Risque : Disparition / indisponibilité des données

[Même structure]

### 3.4 Risque : Réutilisation pour une finalité incompatible

[Même structure]

## 4. Mesures pour traiter les risques

### 4.1 Mesures techniques
| Mesure | Risque traité | État | Responsable | Échéance |
|---|---|---|---|---|
| Chiffrement AES-256 au repos | Accès illégitime | Mis en œuvre | RSSI | — |
| MFA pour tous les comptes admin | Accès illégitime | Mis en œuvre | RSSI | — |
| Sauvegardes hors site + tests trimestriels | Disparition | À planifier | DSI | T1 N+1 |
| Tokenisation des données de paiement | Accès illégitime | Mis en œuvre | DSI | — |

### 4.2 Mesures organisationnelles
| Mesure | Risque traité | État | Responsable | Échéance |
|---|---|---|---|---|
| Charte informatique signée | Accès illégitime | Mis en œuvre | RH | — |
| Formation RGPD annuelle | Tous | Récurrent | RH/DPO | annuelle |
| Procédure d'habilitation | Accès illégitime | Mis en œuvre | DSI | — |
| Audit du sous-traitant principal | Accès illégitime | À réaliser | DPO | T2 N+1 |

## 5. Mesures relatives aux droits des personnes

| Droit | Modalité | Délai cible |
|---|---|---|
| Information | Mentions sur formulaire + politique | À l'inscription |
| Accès | Portail self-service + email DPO | 1 mois |
| Rectification | Portail self-service | Immédiat |
| Effacement | Email DPO + procédure | 1 mois |
| Opposition | Lien désinscription + email | Immédiat |
| Portabilité | Export CSV depuis portail | 1 mois |

## 6. Conclusions et validation

### 6.1 Risques résiduels acceptables ?
[Justifier]

### 6.2 Consultation CNIL requise (art. 36) ?
☐ Non
☐ Oui — rédiger la demande de consultation préalable (art. 36.3) **avant** la mise en œuvre ; la CNIL dispose de 8 semaines, prolongeables de 6 semaines

### 6.3 Avis du DPO (art. 35.2)
[Avis détaillé du DPO sur la conformité du traitement, les mesures et les risques résiduels. Si le responsable s'en écarte, motiver la décision.]

### 6.4 Avis des personnes concernées
[Si recueilli — synthèse]

### 6.5 Décision du responsable de traitement
☐ Approuvé — mise en œuvre autorisée
☐ Approuvé sous conditions : [...]
☐ Refusé — modifications requises

## 7. Suivi et révision

| Événement déclenchant une révision | Échéance |
|---|---|
| Modification du périmètre fonctionnel | Sous 30 jours |
| Nouvelle catégorie de données | Sous 30 jours |
| Nouveau sous-traitant majeur | Sous 30 jours |
| Incident significatif | Sous 60 jours |
| Revue périodique systématique | Tous les 3 ans |

---

## Conseils d'utilisation

- Utiliser de préférence le **logiciel PIA** de la CNIL (gratuit, libre, disponible en une vingtaine de langues, en version poste de travail ou serveur) qui guide la démarche pas à pas, intègre une base de connaissances personnalisable et permet d'exporter le rapport.
- **Système d'IA** : si le traitement relève aussi de l'AI Act (système à haut risque), articuler l'AIPD avec les évaluations exigées par ce règlement — voir `references/ai-act-rgpd.md`.
- Associer **équipe métier + DSI + RSSI + juridique + DPO**. L'AIPD n'est pas un exercice de DPO seul.
- **Itérer** : première version pour identifier les risques majeurs, affiner ensuite.
- **Documenter les choix** : ce qui n'a pas été retenu et pourquoi.
- **Mettre à jour** à chaque évolution structurante du traitement.
