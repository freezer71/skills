---
name: audit-rgpd
description: Audit de conformité RGPD d'un site internet, d'une application ou d'un écosystème numérique entier (sites, sous-domaines, applications mobiles, back-offices, API, outils SaaS, CRM, emailing, analytics, sous-traitants, transferts hors UE). Trouve tous les risques, les prouve, les cote par niveau de gravité ([CRITIQUE], [HAUTE], [MOYENNE], [BASSE], [À VÉRIFIER]) selon la méthode gravité × vraisemblance de la CNIL, et livre un rapport lisible avec un plan d'action priorisé. À utiliser dès que l'utilisateur demande un « audit RGPD », un « audit de conformité », un « diagnostic RGPD », un « état des lieux données personnelles », un « gap analysis GDPR », un « GDPR audit », « mon site est-il conforme au RGPD », « vérifie la conformité de mon site / de mon app / de mon SI », « quels sont mes risques RGPD », « suis-je prêt pour un contrôle CNIL », « audite mes cookies / mon bandeau / mes traceurs », « audite ce projet / ce dépôt côté données personnelles », ou veut préparer un contrôle CNIL, une due diligence, une reprise de société ou une mise en conformité. Couplé au skill `rgpd`, qui fournit le fond du droit, et au skill `mentions-legales`.
---

# Skill Audit RGPD — Trouver, prouver et coter les risques

Ce skill conduit un **audit de conformité RGPD** sur un périmètre choisi : une page, un site, une application, ou tout un écosystème (sites, applications, outils internes, prestataires).

Il répond à 4 questions, dans cet ordre :
1. **Qu'est-ce qui traite des données personnelles ?** La cartographie : traitements, flux, outils, tiers.
2. **Qu'est-ce qui n'est pas conforme ?** Chaque écart, avec sa preuve.
3. **Quelle est la gravité de chaque écart ?** Une cotation explicite, fondée sur le risque pour les personnes.
4. **Que faire, et dans quel ordre ?** Un plan d'action priorisé.

La méthode suit les pratiques reconnues : démarche d'audit en phases (cadrage, preuves, analyse d'écart, cotation, restitution, suivi), méthode de risque de la CNIL (gravité × vraisemblance), principes d'audit de la norme ISO 19011, et contrôle en ligne tel que le pratiquent la CNIL et l'outil d'audit de sites du CEPD. État des pratiques au **6 octobre 2026**.

## Quand utiliser ce skill

Active-toi quand l'utilisateur :
- Demande un **audit**, un **diagnostic**, un **état des lieux** ou une **analyse d'écart** RGPD.
- Demande si un **site**, une **application**, un **projet de code** ou un **système d'information** est conforme.
- Veut connaître ses **risques RGPD** et leur niveau.
- Prépare un **contrôle CNIL**, une **due diligence**, un rachat, une levée de fonds ou un appel d'offres qui exige la conformité.
- Veut auditer ses **cookies**, son **bandeau**, ses **formulaires**, sa **politique de confidentialité** ou ses **prestataires**.

Pour une question de droit isolée (« quelle base légale pour… ») : skill `rgpd`.
Pour rédiger les documents manquants découverts par l'audit : skill `rgpd` (politique, registre, DPA, AIPD) et skill `mentions-legales`.

## Principes directeurs de réponse

1. **Pas d'écart sans preuve.** Chaque risque cite sa preuve : requête réseau, capture, extrait de page, fichier et ligne de code, document, réponse de l'organisme. Sans preuve, le point est classé `[À VÉRIFIER]` et le rapport dit ce qui manque pour trancher.
2. **Constaté, déclaré, non vérifié : 3 statuts différents.** Ce que tu as observé toi-même n'a pas le même poids que ce que l'organisme affirme. Ne jamais écrire « conforme » pour un point seulement déclaré.
3. **Mesurer dans le temps, pas sur une photo.** Pour un site, observer les requêtes et les traceurs sur 10 à 20 secondes, avant tout clic, après refus, après acceptation. Un traceur qui part 5 secondes après le chargement reste un traceur déposé sans consentement.
4. **Coter le risque pour les personnes d'abord.** Le RGPD protège les personnes : la gravité se mesure à l'impact sur elles. Le risque de sanction pour l'organisme vient en second (voir `references/cotation-risques.md`).
5. **Être exhaustif sur le périmètre, honnête sur ses limites.** Parcourir toute la grille (voir `assets/grille-audit.md`). Ce qui n'a pas pu être contrôlé figure dans la partie « Limites de l'audit », jamais passé sous silence.
6. **Rester dans l'autorisation.** L'observation d'un site public, comme le ferait un visiteur, est toujours possible. Tout test actif (sondage de fichiers exposés, tentative de connexion, analyse de vulnérabilités, accès à un back-office) exige l'**autorisation écrite** du responsable du système. Sans elle : ne pas le faire, le noter en limite.
7. **Rester abstrait sur la technique.** Raisonner en concepts (point d'entrée, donnée stockée, tiers appelé, durée de conservation), pas en noms de frameworks. Apprendre les conventions d'un projet en lisant son code.
8. **Rapport lisible d'un coup d'œil.** L'utilisateur est dyslexique : parties fixes et numérotées, un bloc par risque, mêmes libellés dans le même ordre, une idée par ligne, pas d'italique, **aucun émoji** (voir `assets/modele-rapport.md`).
9. **Limite du conseil.** L'audit est une analyse, pas un avis juridique engageant. Pour un contentieux, une sanction en cours ou un risque `[CRITIQUE]` sur des données sensibles : recommander un avocat ou un DPO.

## Architecture du skill — où chercher quoi

Charge la fiche **au moment où l'étape arrive**. Ne charge pas tout d'avance.

| Étape ou sujet | Fiche |
|---|---|
| Déroulé complet d'un audit, phases, preuves, échantillonnage | `references/methode-audit.md` |
| Cotation des risques, matrice, niveaux, verdict global | `references/cotation-risques.md` |
| Contrôle en ligne d'un site ou d'une application (traceurs, bandeau, formulaires, information) | `references/controle-site-web.md` |
| Découvrir et cartographier un écosystème entier (domaines, outils, tiers, flux) | `references/cartographie-ecosysteme.md` |
| Auditer un code source ou une infrastructure (données stockées, journaux, purges, secrets) | `references/audit-code-infrastructure.md` |
| Contrôle des preuves documentaires (registre, AIPD, contrats, procédures) | `references/controle-documentaire.md` |
| Sécurité des données (référentiel CNIL 2024) | `references/securite.md` |
| Ce que la CNIL et le CEPD contrôlent en priorité en 2026 | `references/priorites-controle.md` |

Pour le fond du droit d'un point (base légale, durée, transfert…), charge la fiche correspondante du skill `rgpd`.

## Modèles et grilles prêts à l'emploi

| Besoin | Modèle |
|---|---|
| Questions de cadrage à poser avant l'audit | `assets/questionnaire-cadrage.md` |
| Grille complète des points de contrôle, avec gravité par défaut | `assets/grille-audit.md` |
| Rapport d'audit (format lisible) | `assets/modele-rapport.md` |

## Workflow standard

1. **Cadrer.** Périmètre, objectif, autorisations, accès disponibles (site public seul, code, documents, entretiens). Poser les questions de `assets/questionnaire-cadrage.md`. Si l'utilisateur ne répond pas, auditer ce qui est public et l'écrire.
2. **Cartographier.** Découvrir tout ce qui traite des données : domaines, applications, formulaires, outils, prestataires, flux (voir `references/cartographie-ecosysteme.md`).
3. **Collecter les preuves.** Contrôle en ligne (voir `references/controle-site-web.md`), lecture du code (voir `references/audit-code-infrastructure.md`), documents (voir `references/controle-documentaire.md`).
4. **Analyser les écarts.** Parcourir `assets/grille-audit.md` point par point. Chaque point reçoit un statut : `CONFORME`, `ÉCART`, `À VÉRIFIER` ou `HORS PÉRIMÈTRE`.
5. **Coter.** Chaque écart reçoit un niveau selon `references/cotation-risques.md`. Ajuster la gravité par défaut de la grille au contexte réel.
6. **Restituer.** Rapport selon `assets/modele-rapport.md`, risques classés par gravité, pas par domaine.
7. **Planifier.** Plan d'action : `[CRITIQUE]` immédiat, `[HAUTE]` sous 1 mois, `[MOYENNE]` sous 3 mois, `[BASSE]` au fil de l'eau. Proposer de produire les documents manquants avec le skill `rgpd`.

Pour un **écosystème** large : traiter chaque composant (site, application, outil) comme un sous-périmètre, puis consolider. Si des sous-agents sont disponibles, un composant par sous-agent, avec la même grille.

## Mises en garde transverses

- **« Conforme » n'existe que sur un périmètre et à une date.** Écrire « aucun écart constaté sur le périmètre contrôlé le [date] », jamais « le site est conforme au RGPD ».
- **Un outil automatique ne suffit pas.** Un scanner de cookies voit les traceurs, pas les bases légales, les durées ou les contrats. Il complète l'audit, il ne le remplace pas.
- **Le bandeau peut mentir.** Toujours vérifier le comportement réel (requêtes, traceurs) et pas seulement l'affichage.
- **Le droit bouge.** Avant de coter un point qui dépend d'un texte récent ou en projet, vérifier son statut avec le skill `rgpd` (section « État du droit »). Ne jamais coter un écart sur la base d'une proposition non adoptée.
- **Données découvertes pendant l'audit.** Si l'audit révèle une fuite active (fichier exposé, base ouverte), le signaler **immédiatement** à l'utilisateur, sans attendre le rapport : le délai de 72 h de l'art. 33 peut courir. Ne pas télécharger ni conserver ces données au-delà du strict constat.

## Sources officielles à privilégier

- RGPD : [eur-lex.europa.eu](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- CNIL, méthode d'analyse de risques (PIA) : [cnil.fr — outil PIA](https://www.cnil.fr/fr/outil-pia-telechargez-et-installez-le-logiciel-de-la-cnil)
- CNIL, guide de la sécurité des données personnelles (2024) : [cnil.fr](https://www.cnil.fr/fr/guide-de-la-securite-des-donnees-personnelles-nouvelle-edition-2024)
- CNIL, priorités de contrôle 2026 : [cnil.fr](https://cnil.fr/fr/controles-prioritaires-2026)
- CEPD, outil d'audit de sites web (programme « Support Pool of Experts ») : [edpb.europa.eu](https://www.edpb.europa.eu/support-pool-of-experts-spe-programme_fr)
- CEPD, action coordonnée 2026 sur la transparence : [edpb.europa.eu](https://www.edpb.europa.eu/news/cef-2026-edpb-launches-coordinated-enforcement-action-on-transparency-and-information_es)
- ISO 19011 (lignes directrices pour l'audit des systèmes de management) : [iso.org](https://www.iso.org/standard/70017.html)
