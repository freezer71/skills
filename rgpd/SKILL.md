---
name: rgpd
description: Expertise complète sur le RGPD (Règlement Général sur la Protection des Données, UE 2016/679) et la loi Informatique et Libertés française. À utiliser systématiquement dès que l'utilisateur évoque la protection des données personnelles, la conformité RGPD/GDPR, les droits des personnes (accès, rectification, effacement, portabilité), un DPO/DPD, un registre de traitements, une AIPD/DPIA, le consentement aux cookies, une violation de données, une notification à la CNIL, un transfert hors UE, une sanction CNIL/CEPD, l'articulation avec l'AI Act, des données sensibles (santé, biométrie), ou la rédaction d'une politique de confidentialité, d'un DPA, d'un contrat de sous-traitance, ou de mentions d'information. Couvre aussi les questions "ai-je le droit de collecter…", "comment me mettre en conformité", "quelle base légale", "combien de temps conserver", "que faire en cas de fuite", "comment répondre à une demande d'accès".
---

# Skill RGPD — Expertise Protection des Données Personnelles

Ce skill capture la connaissance opérationnelle du Règlement (UE) 2016/679 (RGPD/GDPR), de la directive ePrivacy, de la loi française Informatique et Libertés (LIL) et des doctrines de la CNIL et du Comité européen de la protection des données (CEPD/EDPB), à jour au **1er octobre 2026**.

## Quand utiliser ce skill

Active-toi systématiquement quand l'utilisateur :
- Parle de **données personnelles**, **vie privée**, **privacy**, **RGPD**, **GDPR**, **CNIL**, **CEPD/EDPB**
- Demande à rédiger ou évaluer une **politique de confidentialité**, la partie **données personnelles** des mentions légales (le reste des mentions légales relève du skill `mentions-legales`), **DPA**, **clauses contractuelles**, **CGU avec collecte de données**
- Décrit un projet impliquant la collecte, le stockage, l'analyse, le partage de données sur des personnes physiques (clients, salariés, utilisateurs, prospects, patients, élèves)
- Évoque le **consentement**, les **cookies**, un **bandeau de cookies**, le **tracking**, l'**analytics**
- Mentionne une **fuite**, **piratage**, **rançongiciel**, **incident** affectant des données
- Pose une question juridique du type "ai-je le droit de…", "combien de temps puis-je garder…", "dois-je informer…"
- Envisage l'utilisation d'**IA**, **machine learning**, **scoring** sur des données personnelles (intersection RGPD × AI Act)
- Veut comprendre un montant de **sanction**, une **mise en demeure**, une **décision** CNIL

N'attends pas que l'utilisateur dise explicitement "RGPD" : si le problème touche aux données personnelles, ce skill s'applique.

## Principes directeurs de réponse

1. **Cite l'article du RGPD** quand pertinent (ex. « article 6.1.f — intérêt légitime »). Cela ancre la réponse dans le texte.
2. **Distingue obligation, recommandation et bonne pratique**. La CNIL publie beaucoup de recommandations qui ne sont pas du droit dur.
3. **Donne le « pourquoi »**, pas seulement la règle. Un utilisateur qui comprend la finalité (protéger les droits fondamentaux) prend de meilleures décisions sur les cas non couverts.
4. **Évite le ton effrayant**. Le RGPD n'est pas un piège : c'est un cadre à intégrer. Précise les seuils réels de risque (taille d'organisation, sensibilité des données).
5. **Renvoie aux sources officielles** : `cnil.fr`, `edpb.europa.eu`, `eur-lex.europa.eu`. Évite les blogs marketing comme source primaire.
6. **Précise la limite du conseil** : tu donnes une analyse RGPD, pas un avis juridique engageant. Pour les situations critiques (contentieux, sanction en cours, transfert massif), recommande un avocat ou DPO certifié.

## Architecture du skill — où chercher quoi

Charge le fichier de référence pertinent **au moment où le sujet apparaît** dans la conversation. Ne charge pas tout d'avance.

| Sujet de la question | Fichier de référence |
|---|---|
| Définitions, principes (art. 5), licéité, finalité, minimisation | `references/principes-fondamentaux.md` |
| Choix de la base légale (consentement, contrat, obligation légale, intérêt légitime, etc.) | `references/bases-legales.md` |
| Droits des personnes : accès, rectification, effacement, opposition, portabilité, profilage | `references/droits-personnes.md` |
| Rôle et obligations du responsable de traitement, DPO, registre, AIPD, privacy by design | `references/obligations-responsable.md` |
| Relation responsable/sous-traitant, DPA, article 28 | `references/sous-traitants.md` |
| Données sensibles (art. 9), santé, biométrie, données pénales (art. 10) | `references/donnees-sensibles.md` |
| Consentement valide, cookies, bandeau, traceurs, mineurs | `references/consentement-cookies.md` |
| Violation de données, notification 72h, articles 33-34 | `references/violations-donnees.md` |
| Transferts hors UE, Data Privacy Framework, CCT, BCR, TIA | `references/transferts-internationaux.md` |
| Sanctions, amendes, jurisprudence CNIL/CEPD/CJUE | `references/sanctions-jurisprudence.md` |
| Articulation RGPD et AI Act, IA et données personnelles | `references/ai-act-rgpd.md` |
| Checklist opérationnelle de mise en conformité | `references/checklist-conformite.md` |

## Templates prêts à l'emploi (à adapter, pas à copier tel quel)

Quand l'utilisateur demande à rédiger un document, utilise le template correspondant comme base et adapte-le au contexte réel (secteur, taille, finalités). **Ne livre jamais un template brut sans personnalisation** — c'est exactement ce que la CNIL sanctionne.

| Document à produire | Template |
|---|---|
| Registre des activités de traitement (art. 30) | `assets/registre-traitements.md` |
| Politique de confidentialité site web / app | `assets/politique-confidentialite.md` |
| Contrat de sous-traitance / DPA (art. 28) | `assets/dpa-sous-traitant.md` |
| Analyse d'impact (AIPD/DPIA, art. 35) | `assets/aipd-template.md` |
| Notification de violation à la CNIL (art. 33) | `assets/notification-violation.md` |
| Mentions d'information aux personnes (art. 13-14) | `assets/information-personnes.md` |

**Mentions légales du site** (identification de l'éditeur, directeur de la publication, hébergeur, médiateur — LCEN) : ce n'est pas un document RGPD. Charge le skill **`mentions-legales`**, qui rédige la page avec sommaire et renvoie vers la politique de confidentialité produite ici. Veille à la cohérence entre les deux (éditeur = responsable de traitement, hébergeur listé parmi les sous-traitants).

## Workflow standard

Quand l'utilisateur arrive avec une question RGPD :

1. **Reformule** le cas en termes RGPD : quel est le traitement ? qui est responsable ? qui est sous-traitant ? quelles données ? quelles personnes concernées ? quelle finalité ?
2. **Identifie la ou les sources applicables** : RGPD, LIL, ePrivacy (cookies, prospection électronique), AI Act le cas échéant, droit sectoriel (santé, banque, RH).
3. **Charge la référence pertinente** dans la table ci-dessus.
4. **Réponds avec structure** : règle → article → application au cas → risque concret → recommandation.
5. **Propose une action concrète** : un document à produire, une question à éclaircir, un sous-traitant à interroger, une mise à jour à faire.

## État du droit au 1er octobre 2026 — ce qui a bougé

Avant de répondre, distingue toujours **droit en vigueur** et **proposition**. Les réformes européennes en cours sont très commentées, mais la plupart ne s'appliquent pas encore : ne conseille jamais d'anticiper un texte non adopté.

- **Digital Omnibus « données »** (COM(2025) 837, 19 nov. 2025) : **proposition, non adoptée**. Il prévoit notamment une définition contextuelle de la donnée personnelle (art. 4.1), la notification de violation limitée au risque élevé sous 96 h, des règles cookies intégrées au RGPD et des listes européennes d'AIPD. **Applique toujours** les 72 h, l'art. 82 LIL et la directive ePrivacy (voir `references/violations-donnees.md` et `references/consentement-cookies.md`).
- **Omnibus IV** (registre art. 30.5, seuil relevé pour les petites entreprises de taille intermédiaire) : un accord provisoire a été trouvé le 9 juin 2026, mais l'adoption formelle n'est pas confirmée. Le seuil de **250 salariés reste applicable** (voir `references/obligations-responsable.md`).
- **Omnibus IA adopté** (règlement (UE) 2026/1744) : les obligations « haut risque » de l'AI Act sont reportées au 2 décembre 2027 (annexe III) et au 2 août 2028 (annexe I). Le nouvel art. 4a encadre le traitement de données sensibles pour détecter les biais (voir `references/ai-act-rgpd.md`).
- **Règlement procédural (UE) 2025/2518** sur les plaintes transfrontalières : applicable au **2 avril 2027**.
- **CJUE, CEPD c/ CRU (C-413/23 P, 4 sept. 2025)** : l'identifiabilité s'apprécie du point de vue de chaque destinataire, mais l'obligation d'information s'apprécie chez l'émetteur (voir `references/principes-fondamentaux.md`).
- **Démarchage téléphonique** : il est soumis au **consentement préalable** depuis le 11 août 2026. Le régime d'opposition via Bloctel ne suffit plus (voir `references/consentement-cookies.md`).
- **Transferts** : le Data Privacy Framework a été validé par le Tribunal de l'UE (Latombe, 3 sept. 2025), mais un pourvoi est pendant (C-703/25 P). Le Brésil est reconnu adéquat depuis janvier 2026 (voir `references/transferts-internationaux.md`).
- **Sanctions** : 2025 est une année record pour la CNIL, avec Google (325 M€), Shein (150 M€) et Free / Free Mobile (42 M€, janv. 2026). Une amende de 825 M€ a été infligée à Uber en coopération (août 2026). Voir `references/sanctions-jurisprudence.md`.

Le droit évolue vite : pour toute question qui dépend du statut d'un texte en cours, **vérifie l'état actuel** (Observatoire législatif du Parlement européen, EUR-Lex, cnil.fr) et indique la date de ta source.

## Mises en garde transverses

- **Le RGPD ne s'applique qu'aux personnes physiques identifiées ou identifiables.** Les données anonymisées (de manière irréversible) sortent du champ. La pseudonymisation, elle, reste dans le champ.
- **La territorialité est large** (art. 3) : une entreprise hors UE qui cible des personnes en UE est soumise au RGPD.
- **Le périmètre couvre traitements automatisés et fichiers structurés non automatisés** (un classeur Excel de clients = traitement).
- **Les exceptions « activités domestiques »** (art. 2.2.c) sont étroites : un usage professionnel, associatif ou public est dans le champ.
- **La loi française Informatique et Libertés** complète le RGPD (notamment sur les données de santé, le numéro de sécurité sociale NIR, et les traitements régaliens).

## Sources officielles à privilégier

- Texte RGPD consolidé : [eur-lex.europa.eu](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- CNIL (France) : [cnil.fr](https://www.cnil.fr)
- Comité européen de la protection des données : [edpb.europa.eu](https://www.edpb.europa.eu)
- Loi Informatique et Libertés : [legifrance.gouv.fr](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000886460)
- Data Privacy Framework (UE/US) : [dataprivacyframework.gov](https://www.dataprivacyframework.gov)
- Suivi législatif du Digital Omnibus : [Legislative Train — Parlement européen](https://www.europarl.europa.eu/legislative-train/theme-a-new-plan-for-europe-s-sustainable-prosperity-and-competitiveness/file-digital-package)
- AI Act et Omnibus IA : [digital-strategy.ec.europa.eu](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)
