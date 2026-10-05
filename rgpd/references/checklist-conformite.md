# Checklist opérationnelle de mise en conformité RGPD

À adapter à la taille et au secteur. L'objectif n'est pas de cocher mécaniquement chaque case, mais d'avoir un état des lieux **honnête** et un plan d'action **priorisé**.

> Cette checklist suit le **droit en vigueur au 1er octobre 2026**. Les propositions de simplification (Omnibus IV sur le registre, Digital Omnibus sur l'AIPD, la notification de violation et l'information) ne sont pas encore applicables : voir la section « Évolutions annoncées » de `references/obligations-responsable.md`.

## Étape 1 — Cartographier (4-8 semaines)

### 1.1 Inventaire des traitements
- [ ] Recenser tous les traitements (RH, clients, prospection, sous-traitance, vidéoprotection, contrôle d'accès, IA, etc.).
- [ ] Pour chaque traitement : finalité(s), données, personnes, durée, destinataires, sécurité, transferts.
- [ ] **Sortir du périmètre** : ce qui est anonymisé de manière irréversible (test à valider).

### 1.2 Cartographie des flux et destinataires
- [ ] Lister sous-traitants et destinataires tiers.
- [ ] Identifier transferts hors UE.
- [ ] Vérifier base légale de chaque partage.

### 1.3 Identifier les obligations spécifiques
- [ ] Données sensibles, mineurs, salariés, patients, élèves.
- [ ] AIPD obligatoire : listes CNIL (AIPD requise / non requise) et 9 critères du CEPD (voir `references/obligations-responsable.md`).
- [ ] DPO obligatoire (art. 37.1).
- [ ] Entité concernée par NIS 2 (entité essentielle ou importante) ? Si oui, prévoir les notifications d'incidents propres à NIS 2 en plus de celles du RGPD (transposition française en cours d'adoption — vérifier l'état du texte).

## Étape 2 — Gouvernance (parallèle à l'étape 1)

### 2.1 Désigner les rôles
- [ ] **Sponsor** au COMEX/CODIR.
- [ ] **DPO** (si requis ou souhaitable), désigné auprès de la CNIL par son téléservice, sans conflit d'intérêts, avec ressources et rattachement à la direction (art. 37-38).
- [ ] **Référents** par direction (RH, marketing, IT, etc.).

### 2.2 Politiques internes
- [ ] Politique de protection des données.
- [ ] Politique de sécurité du système d'information (PSSI).
- [ ] Politique de gestion des incidents.
- [ ] Politique de conservation (par catégorie de données).
- [ ] Charte informatique pour les salariés.
- [ ] Procédure de gestion des droits des personnes.

### 2.3 Comité RGPD
- [ ] Réunion régulière (mensuelle ou trimestrielle).
- [ ] Tableau de bord : demandes droits, incidents, AIPD en cours, formations.

## Étape 3 — Documentation (continue)

### 3.1 Registre des activités de traitement (art. 30)
- [ ] Constitué et tenu à jour.
- [ ] Inclut tous les éléments requis par l'art. 30.1 (voir `assets/registre-traitements.md`).
- [ ] Exemption de l'art. 30.5 (moins de 250 salariés) invoquée seulement si **tous** les traitements sont occasionnels, sans risque et sans données sensibles ou pénales — ce qui est rare. Ne pas anticiper le seuil de 750 salariés proposé par Omnibus IV tant qu'il n'est pas publié et applicable.

### 3.2 AIPD (art. 35)
- [ ] Réalisées pour les traitements à risque (liste CNIL des AIPD requises + 9 critères).
- [ ] Dispense documentée pour les traitements de la liste CNIL des AIPD non requises.
- [ ] DPO consulté (art. 35.2) ; consultation préalable de la CNIL si risque résiduel élevé (art. 36).
- [ ] Mises à jour à chaque évolution significative.
- [ ] Outil PIA CNIL ou équivalent (voir `assets/aipd-template.md`).

### 3.3 Contrats sous-traitants
- [ ] Tous les sous-traitants ont signé un DPA conforme à l'art. 28.
- [ ] Vérification des garanties (certifications, audit).
- [ ] Suivi des sous-traitants ultérieurs.

### 3.4 Information des personnes (art. 13-14)
- [ ] Mentions sur site web (politique de confidentialité accessible depuis chaque page).
- [ ] Mentions sur formulaires (collecte directe).
- [ ] Mentions spécifiques RH (livret d'accueil, contrat de travail).
- [ ] Mentions CCTV.

### 3.5 Preuve des consentements (quand c'est la base)
- [ ] Système de log : date, contenu accepté, modalité.
- [ ] Conservation pendant la durée d'utilité + délai de prescription.

### 3.6 TIA pour transferts hors UE
- [ ] Une TIA documentée par mécanisme de transfert.

### 3.7 LIA pour intérêt légitime
- [ ] Test à trois niveaux documenté par traitement.

## Étape 4 — Sécurité (parallèle, continu)

Référence : guide CNIL « Sécurité des données personnelles », édition 2024 (25 fiches et liste de vérification, y compris IA, applications mobiles, cloud et API).

### 4.1 Mesures techniques (art. 32)
- [ ] Chiffrement (au repos et en transit).
- [ ] Authentification forte (MFA pour comptes sensibles, admins).
- [ ] Politique de mots de passe robuste.
- [ ] Gestion des habilitations (principe du moindre privilège).
- [ ] Journalisation et supervision.
- [ ] Sauvegardes testées (PRA/PCA).
- [ ] Mises à jour de sécurité régulières.
- [ ] Antivirus/EDR.
- [ ] Sécurisation des postes (BitLocker, FileVault).
- [ ] Cloisonnement réseau.

### 4.2 Mesures organisationnelles
- [ ] Formation des salariés (annuelle ou à l'embauche).
- [ ] Charte d'usage des SI.
- [ ] Procédure d'arrivée / départ (gestion des accès).
- [ ] NDA / clauses de confidentialité.
- [ ] Tests d'intrusion réguliers (pour systèmes critiques).

### 4.3 Plan de réponse à incident
- [ ] Procédure documentée.
- [ ] Équipe d'astreinte identifiée.
- [ ] Test de la procédure (simulation).
- [ ] Modèles de notification CNIL et d'information des personnes prêts (voir `assets/notification-violation.md`), avec la trame préparatoire du téléservice de la CNIL.
- [ ] Délai de **72 heures** (art. 33) intégré à la procédure ; notification en deux temps prévue si l'enquête n'est pas terminée.
- [ ] Registre interne des violations tenu, y compris pour les violations non notifiées (art. 33.5).

## Étape 5 — Droits des personnes

### 5.1 Canal de demande
- [ ] Adresse `dpo@…` ou formulaire en ligne.
- [ ] Mentionnée dans la politique de confidentialité et toute communication.

### 5.2 Procédure interne
- [ ] Qualification de la demande (accès, rectification, etc.).
- [ ] Vérification d'identité **proportionnée**.
- [ ] Investigation / collecte des données.
- [ ] Anonymisation/expurgation des données de tiers.
- [ ] Réponse motivée sous 1 mois, prorogeable de 2 mois si nécessaire en informant la personne (art. 12.3).
- [ ] Refus d'une demande « manifestement infondée ou excessive » (art. 12.5) motivé et documenté : la charge de la preuve pèse sur le responsable.
- [ ] Archivage de la demande et de la réponse.

### 5.3 Outils
- [ ] Tableur de suivi ou ticketing dédié.
- [ ] Templates de réponse par type de demande.

## Étape 6 — Cookies et marketing

### 6.1 Bandeau cookies
- [ ] Conforme aux recommandations CNIL (refuser aussi simple qu'accepter).
- [ ] Granularité par finalité.
- [ ] Aucun dépôt avant choix.
- [ ] Mécanisme de retrait permanent (icône, lien).
- [ ] Conservation preuves.
- [ ] Choix conservé et redemandé à intervalles raisonnables (la CNIL retient 6 mois comme bonne pratique, y compris pour conserver un refus) ; durée de vie des traceurs limitée à 13 mois (voir `references/consentement-cookies.md`).

### 6.2 Politique cookies
- [ ] Liste détaillée des traceurs et finalités.
- [ ] Durée de vie de chaque cookie.

### 6.3 Prospection
- [ ] Consentement B2C / opt-in.
- [ ] Intérêt légitime B2B documenté + opposition possible.
- [ ] Lien de désinscription dans tout email.

## Étape 7 — Vidéoprotection / vidéosurveillance

- [ ] Finalité légitime documentée.
- [ ] Affichage signalant la captation.
- [ ] Durée de conservation limitée (un mois maximum en principe, recommandation CNIL).
- [ ] Accès restreint.
- [ ] AIPD si dispositif étendu / lieu non public / employés.
- [ ] Pas de surveillance permanente du poste de travail.

## Étape 8 — Ressources humaines

- [ ] Information dès recrutement (mentions sur CV, processus).
- [ ] Conservation CV non retenus : 2 ans après le dernier contact au maximum, sauf opposition du candidat (référentiel CNIL « recrutement »).
- [ ] Dossier salarié : sécurisé, accès restreint.
- [ ] Bulletins de paie : double conservé 5 ans par l'employeur (art. L. 3243-4 du Code du travail) ; s'appuyer sur le référentiel CNIL « gestion du personnel » pour les autres durées.
- [ ] Vidéo-surveillance, géolocalisation, badges : encadrement strict + info CSE.
- [ ] Outils de contrôle (DLP, MDM) : information + proportionnalité.

## Étape 9 — Audit et amélioration continue

- [ ] Auto-évaluation annuelle.
- [ ] Audit externe périodique (recommandé pour > 250 salariés).
- [ ] Veille réglementaire (lignes directrices CEPD, recommandations CNIL, réformes européennes en cours : Omnibus IV, Digital Omnibus, règlement procédural (UE) 2025/2518 applicable au 2 avril 2027, transposition de NIS 2).
- [ ] Indicateurs au COMEX (volume incidents, demandes droits, formations, etc.).
- [ ] Test de conformité du site web (cookies, mentions, etc.).

## Priorisation pragmatique

Si on doit choisir par où commencer (PME, ressources limitées) :

**Priorité 1 (à faire maintenant)** :
1. Registre des traitements (au moins une version V1 par grande activité).
2. Politique de confidentialité du site web.
3. Mise en conformité du bandeau cookies.
4. DPA avec les sous-traitants critiques (cloud, paie, CRM).
5. Procédure de gestion des droits.

**Priorité 2 (3-6 mois)** :
1. Mesures de sécurité de base (MFA, sauvegardes, chiffrement, formation).
2. AIPD pour les traitements à risque.
3. Mentions d'information sur les principaux formulaires.
4. Plan de réponse à incident.

**Priorité 3 (6-12 mois)** :
1. Audit complet et plan d'action long terme.
2. Désignation DPO si les conditions de l'art. 37.1 sont remplies — à avancer en priorité 1 si c'est le cas : l'absence de DPO obligatoire est un manquement en soi.
3. Référentiel de durées de conservation (appui : référentiels sectoriels de la CNIL).
4. Politique d'archivage et purge automatique.

## Sources

- [RGPD : passer à l'action — CNIL](https://www.cnil.fr/fr/principes-cles/rgpd-passer-a-laction)
- [Modèle de registre — CNIL](https://www.cnil.fr/fr/RGDP-le-registre-des-activites-de-traitement)
- [Guide de la sécurité des données personnelles, édition 2024 — CNIL](https://www.cnil.fr/fr/guide-de-la-securite-des-donnees-personnelles-nouvelle-edition-2024)
- [Liste des traitements pour lesquels une AIPD est requise — CNIL](https://www.cnil.fr/sites/default/files/atoms/files/liste-traitements-aipd-requise.pdf)
- [Liste des traitements pour lesquels une AIPD n'est pas requise — CNIL](https://www.cnil.fr/fr/liste-traitements-aipd-non-requise)
- [Logiciel PIA — CNIL](https://www.cnil.fr/fr/outil-pia-telechargez-et-installez-le-logiciel-de-la-cnil)
- [Notifier une violation de données personnelles — CNIL](https://www.cnil.fr/fr/services-en-ligne/notifier-une-violation-de-donnees-personnelles)
- [Désigner un DPO — CNIL](https://www.cnil.fr/fr/designation-dpo)
- [Référentiel gestion du personnel — CNIL](https://www.cnil.fr/sites/cnil/files/atoms/files/referentiel_grh_novembre_2019_0.pdf)
- [Référentiel gestion des activités commerciales — CNIL](https://www.cnil.fr/sites/cnil/files/atoms/files/referentiel_traitements-donnees-caractere-personnel_gestion-activites-commerciales.pdf)
- [Guide RGPD du développeur — CNIL](https://www.cnil.fr/fr/guide-rgpd-du-developpeur)
- [Règlement (UE) 2025/2518 (règles de procédure RGPD) — EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:L_202502518)
