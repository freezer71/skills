# Grille d'audit RGPD

**Modèle à adapter — ne pas publier brut.**

Règles d'emploi :
- Parcourir **tous** les points. Chacun reçoit un statut : `CONFORME`, `ÉCART`, `À VÉRIFIER` ou `HORS PÉRIMÈTRE` (avec sa raison).
- La gravité indiquée est la **gravité par défaut** si l'écart est constaté. L'ajuster au contexte et écrire pourquoi (voir `references/cotation-risques.md`).
- Le niveau d'accès indique à partir de quand le point peut être tranché : N1 public, N2 code et infrastructure, N3 organisation.
- Format de chaque point : identifiant, question, article, accès, gravité par défaut, preuve attendue.

---

## A. Traceurs et consentement

**A1** Des traceurs non exemptés sont-ils déposés ou lus avant tout consentement ?
- Article : art. 82 loi Informatique et Libertés
- Accès : N1
- Gravité par défaut : [HAUTE]
- Preuve : requêtes et cookies observés 10 à 20 s sans aucun clic

**A2** Le bandeau propose-t-il « Tout refuser » au même niveau que « Tout accepter » ?
- Article : art. 82 LIL, art. 4.11 et 7 RGPD
- Accès : N1
- Gravité par défaut : [HAUTE]
- Preuve : capture du premier écran du bandeau

**A3** Le refus est-il respecté sur toute la navigation ?
- Article : art. 82 LIL
- Accès : N1
- Gravité par défaut : [HAUTE]
- Preuve : requêtes sur 2 ou 3 pages après refus

**A4** Le consentement est-il libre, spécifique et éclairé (finalités et tiers listés, pas de case précochée, pas d'interface trompeuse) ?
- Article : art. 4.11 et 7 RGPD
- Accès : N1
- Gravité par défaut : [MOYENNE]
- Preuve : captures des écrans du bandeau

**A5** Le retrait du consentement est-il aussi simple que son octroi ?
- Article : art. 7.3 RGPD
- Accès : N1
- Gravité par défaut : [MOYENNE]
- Preuve : lien permanent, test de retrait

**A6** La mesure d'audience sans consentement respecte-t-elle les conditions d'exemption ?
- Article : art. 82 LIL, recommandation CNIL
- Accès : N1, N2
- Gravité par défaut : [MOYENNE]
- Preuve : outil, configuration, durée des traceurs

**A7** Les contenus tiers intégrés (vidéos, cartes, polices, boutons sociaux) se chargent-ils sans transmettre de données avant consentement ou besoin ?
- Article : art. 6 RGPD, art. 82 LIL
- Accès : N1
- Gravité par défaut : [BASSE]
- Preuve : requêtes vers les domaines tiers au chargement

**A8** L'organisme peut-il prouver les consentements recueillis ?
- Article : art. 7.1 RGPD
- Accès : N2, N3
- Gravité par défaut : [MOYENNE]
- Preuve : exemple d'enregistrement de consentement

## B. Prospection et courriels

**B1** La prospection électronique vers des particuliers repose-t-elle sur un consentement préalable (ou l'exception client pour des produits analogues) ?
- Article : art. L. 34-5 CPCE
- Accès : N1, N3
- Gravité par défaut : [HAUTE]
- Preuve : formulaire d'inscription, case non précochée

**B2** Les courriels contiennent-ils des pixels de suivi sans consentement ?
- Article : art. 82 LIL, recommandation CNIL 2026
- Accès : N1 (adresse de test)
- Gravité par défaut : [MOYENNE]
- Preuve : code source d'un courriel reçu

**B3** La désinscription est-elle possible simplement dans chaque message ?
- Article : art. L. 34-5 CPCE, art. 21 RGPD
- Accès : N1
- Gravité par défaut : [MOYENNE]
- Preuve : test du lien

**B4** Le démarchage téléphonique repose-t-il sur un consentement préalable (régime applicable depuis le 11 août 2026) ?
- Article : art. L. 223-1 Code de la consommation, dans sa version modifiée en 2025
- Accès : N3
- Gravité par défaut : [HAUTE]
- Preuve : preuve de consentement des personnes appelées

## C. Information et transparence

**C1** Une politique de confidentialité est-elle accessible depuis chaque page ?
- Article : art. 12 et 13 RGPD
- Accès : N1
- Gravité par défaut : [MOYENNE]
- Preuve : lien en pied de page

**C2** Contient-elle tous les éléments des art. 13 et 14 ?
- Article : art. 13 et 14 RGPD
- Accès : N1
- Gravité par défaut : [MOYENNE]
- Preuve : relecture élément par élément

**C3** Correspond-elle à la réalité observée (tiers, traceurs, transferts, durées) ?
- Article : art. 5.1.a et 13 RGPD
- Accès : N1, N2
- Gravité par défaut : [MOYENNE]
- Preuve : comparaison entre tiers observés et tiers déclarés

**C4** Chaque formulaire porte-t-il une information au point de collecte ?
- Article : art. 13 RGPD
- Accès : N1
- Gravité par défaut : [BASSE]
- Preuve : capture de chaque formulaire

**C5** Les salariés, candidats et personnes dont les données sont collectées indirectement sont-ils informés ?
- Article : art. 13 et 14 RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : supports d'information

**C6** Les mentions légales identifient-elles l'éditeur et l'hébergeur ?
- Article : art. 6 III LCEN (voir le skill `mentions-legales`)
- Accès : N1
- Gravité par défaut : [BASSE]
- Preuve : page mentions légales

## D. Licéité, finalités, minimisation

**D1** Chaque traitement a-t-il une finalité déterminée et une base légale identifiée ?
- Article : art. 5.1.b et 6 RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : registre

**D2** L'intérêt légitime invoqué est-il justifié par une mise en balance documentée ?
- Article : art. 6.1.f RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : analyse écrite

**D3** Les données collectées sont-elles limitées au nécessaire (champs obligatoires, champs inutilisés) ?
- Article : art. 5.1.c RGPD
- Accès : N1, N2
- Gravité par défaut : [BASSE]
- Preuve : formulaires, structures de données

**D4** Des données sensibles ou pénales sont-elles traitées sans exception de l'art. 9 ou 10 ?
- Article : art. 9 et 10 RGPD
- Accès : N1, N2, N3
- Gravité par défaut : [CRITIQUE]
- Preuve : champs, finalités, base invoquée

**D5** Les mineurs sont-ils protégés (âge, consentement parental sous 15 ans, information adaptée) ?
- Article : art. 8 RGPD, art. 45 LIL
- Accès : N1, N3
- Gravité par défaut : [HAUTE]
- Preuve : parcours d'inscription

**D6** Des décisions entièrement automatisées produisent-elles des effets importants sans garanties ?
- Article : art. 22 RGPD
- Accès : N2, N3
- Gravité par défaut : [HAUTE]
- Preuve : logique de décision, information des personnes

## E. Conservation

**E1** Une durée de conservation est-elle définie pour chaque traitement ?
- Article : art. 5.1.e RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : registre, politique de conservation

**E2** Les durées sont-elles réellement appliquées (purge, anonymisation, archivage) ?
- Article : art. 5.1.e RGPD
- Accès : N2
- Gravité par défaut : [MOYENNE]
- Preuve : tâches de purge, âge des plus anciennes données

**E3** Les sauvegardes, exports et outils tiers suivent-ils les mêmes durées ?
- Article : art. 5.1.e RGPD
- Accès : N2, N3
- Gravité par défaut : [BASSE]
- Preuve : configuration des sauvegardes

## F. Droits des personnes

**F1** Un moyen simple d'exercer ses droits est-il indiqué ?
- Article : art. 12 RGPD
- Accès : N1
- Gravité par défaut : [MOYENNE]
- Preuve : adresse ou formulaire dédié

**F2** Une procédure garantit-elle une réponse sous 1 mois ?
- Article : art. 12.3 RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : procédure, registre des demandes

**F3** La suppression d'un compte efface-t-elle réellement les données, y compris chez les tiers ?
- Article : art. 17 et 19 RGPD
- Accès : N2
- Gravité par défaut : [MOYENNE]
- Preuve : code de suppression

**F4** L'accès et la portabilité sont-ils possibles (export des données d'une personne) ?
- Article : art. 15 et 20 RGPD
- Accès : N2, N3
- Gravité par défaut : [BASSE]
- Preuve : fonction d'export ou procédure manuelle

**F5** Une demande réelle a-t-elle été ignorée ou traitée hors délai ?
- Article : art. 12 RGPD
- Accès : N3
- Gravité par défaut : [HAUTE]
- Preuve : registre des demandes, plaintes

## G. Tiers et transferts

**G1** Chaque sous-traitant a-t-il un contrat conforme à l'art. 28 ?
- Article : art. 28 RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : contrats

**G2** Les responsables conjoints ont-ils un accord art. 26 ?
- Article : art. 26 RGPD
- Accès : N3
- Gravité par défaut : [BASSE]
- Preuve : accord

**G3** Chaque transfert hors UE a-t-il une garantie valable ?
- Article : art. 44 à 49 RGPD
- Accès : N1 (tiers observés), N3
- Gravité par défaut : [HAUTE]
- Preuve : pays du destinataire, certification ou clauses types

**G4** Des données sont-elles envoyées à des outils d'IA ou des services externes non déclarés ?
- Article : art. 5, 6, 28 RGPD
- Accès : N2, N3
- Gravité par défaut : [HAUTE]
- Preuve : appels dans le code, usages déclarés

## H. Sécurité

**H1** HTTPS partout, y compris sur les formulaires et les API ?
- Article : art. 32 RGPD
- Accès : N1
- Gravité par défaut : [HAUTE]
- Preuve : test HTTP, certificat

**H2** Les mots de passe sont-ils stockés avec un hachage lent et salé ?
- Article : art. 32 RGPD
- Accès : N2
- Gravité par défaut : [CRITIQUE]
- Preuve : code d'enregistrement du mot de passe

**H3** La politique de mot de passe suit-elle la recommandation CNIL 2022 ?
- Article : art. 32 RGPD, délibération 2022-100
- Accès : N1
- Gravité par défaut : [MOYENNE]
- Preuve : test à l'inscription

**H4** Un utilisateur peut-il accéder aux données d'un autre ?
- Article : art. 32 RGPD
- Accès : N2 (lecture du code) ; test actif seulement avec autorisation
- Gravité par défaut : [CRITIQUE]
- Preuve : contrôle d'accès de chaque point d'entrée

**H5** Les accès d'administration sont-ils protégés par une authentification forte et nominative ?
- Article : art. 32 RGPD
- Accès : N2, N3
- Gravité par défaut : [HAUTE]
- Preuve : configuration, entretien

**H6** Les accès aux données sont-ils journalisés, et les journaux exempts de secrets ?
- Article : art. 32 RGPD
- Accès : N2
- Gravité par défaut : [MOYENNE] ; [CRITIQUE] si mots de passe ou jetons en clair
- Preuve : configuration et exemples de journaux

**H7** Des données personnelles sont-elles exposées publiquement (fichier, environnement de test, stockage ouvert, URL) ?
- Article : art. 32 RGPD
- Accès : N1, N2
- Gravité par défaut : [CRITIQUE]
- Preuve : URL ou emplacement, sans télécharger les données

**H8** Les secrets sont-ils hors du code et de son historique ?
- Article : art. 32 RGPD
- Accès : N2
- Gravité par défaut : [HAUTE]
- Preuve : recherche dans le dépôt

**H9** Les sauvegardes sont-elles régulières, séparées, chiffrées et testées ?
- Article : art. 32 RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : procédure, dernier test de restauration

## I. Violations

**I1** Une procédure permet-elle de notifier la CNIL sous 72 h ?
- Article : art. 33 RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : procédure écrite

**I2** Un registre des violations est-il tenu ?
- Article : art. 33.5 RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : registre

**I3** Une violation passée a-t-elle été omise ou notifiée en retard ?
- Article : art. 33 et 34 RGPD
- Accès : N3
- Gravité par défaut : [HAUTE]
- Preuve : historique des incidents

## J. Gouvernance et documentation

**J1** Un registre des traitements existe-t-il, complet et à jour ?
- Article : art. 30 RGPD
- Accès : N3
- Gravité par défaut : [MOYENNE]
- Preuve : registre comparé à la cartographie

**J2** Les AIPD obligatoires ont-elles été réalisées ?
- Article : art. 35 RGPD
- Accès : N3
- Gravité par défaut : [HAUTE]
- Preuve : AIPD, liste CNIL, critères du CEPD

**J3** Un DPO est-il désigné quand il est obligatoire ?
- Article : art. 37 RGPD
- Accès : N1 (coordonnées publiées), N3
- Gravité par défaut : [MOYENNE]
- Preuve : désignation auprès de la CNIL

**J4** La protection des données est-elle prise en compte dès la conception des projets ?
- Article : art. 25 RGPD
- Accès : N3
- Gravité par défaut : [BASSE]
- Preuve : procédure projet, exemples

**J5** Les personnes qui manipulent des données sont-elles sensibilisées ?
- Article : art. 32.4 et 39 RGPD
- Accès : N3
- Gravité par défaut : [BASSE]
- Preuve : supports, dates des sessions

## K. Intelligence artificielle (si applicable)

**K1** Les traitements de données par des systèmes d'IA ont-ils une base légale, une information et, si besoin, une AIPD ?
- Article : art. 6, 13, 35 RGPD ; AI Act (voir le skill `rgpd`)
- Accès : N2, N3
- Gravité par défaut : [MOYENNE] ; [HAUTE] pour des données sensibles ou des décisions sur les personnes
- Preuve : documentation du système, information
