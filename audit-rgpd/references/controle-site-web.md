# Contrôle en ligne d'un site ou d'une application

Le contrôle en ligne observe un site **comme un visiteur**, sans aucun accès privilégié. C'est exactement ce que fait la CNIL lors de ses contrôles en ligne : elle constate depuis ses locaux si les traceurs partent avant le consentement, si le bandeau permet de refuser, si l'information est complète. Ces contrôles représentent une part importante de son activité et sont à l'origine de la plupart des sanctions sur les cookies.

Ce contrôle est toujours possible sans autorisation particulière, puisqu'il ne fait que consulter des pages publiques.

## Outils et conditions

- Idéalement : un **navigateur piloté** qui permet de lire les requêtes réseau, les cookies et le stockage local. Si le navigateur de l'utilisateur est disponible, ouvrir un **nouvel onglet en navigation privée ou un profil vierge**.
- À défaut : récupération HTTP simple de la page. Elle montre les en-têtes, les cookies posés par le serveur et les scripts tiers appelés dans le code de la page. Elle ne montre **pas** ce que les scripts déclenchent ensuite. Tout ce qui en dépend est `[À VÉRIFIER]`.
- Outils publics utiles : l'outil d'audit de sites web du CEPD (logiciel libre), le « Website Evidence Collector » du CEPD européen (EDPS). Les citer comme moyen de confirmation.
- Toujours noter : date, heure, navigateur, localisation apparente (une page peut se comporter autrement hors UE).

## Test 1 — Avant tout consentement

C'est le test le plus important.

1. Ouvrir la page dans un profil vierge.
2. **Ne rien cliquer.** Ne pas fermer le bandeau.
3. Observer pendant **10 à 20 secondes** : requêtes réseau, cookies, stockage local.
4. Relever chaque domaine **tiers** contacté et chaque cookie ou identifiant déposé.

Règle : avant consentement, seuls les traceurs **strictement nécessaires** sont admis (art. 82 de la loi Informatique et Libertés). Sont exemptés : panier, session, authentification, sécurité, équilibrage de charge, mémorisation du choix de consentement, et mesure d'audience **strictement** limitée (voir plus bas).

Écart typique : un appel vers une régie publicitaire, un réseau social, un outil d'analyse non exempté ou un outil d'enregistrement de session avant tout clic. Gravité par défaut `[HAUTE]`, exposition FORTE.

Attention aux faux exemptés :
- Une police d'écriture, une carte, une vidéo ou une bibliothèque chargée depuis un serveur tiers transmet l'adresse IP du visiteur à ce tiers. Ce n'est pas un traceur au sens strict, mais c'est un transfert de données personnelles qui demande une base légale et, hors UE, un encadrement (un tribunal allemand a condamné en 2022 l'appel à des polices hébergées par un tiers américain). Gravité par défaut `[BASSE]` à `[MOYENNE]`.
- Une vidéo ou un bouton de partage intégré dépose souvent des traceurs dès l'affichage. Exiger un chargement au clic.

## Test 2 — Le bandeau

Vérifier, sur l'affichage et sur le comportement :

- Un bouton **« Tout refuser »** au même niveau et aussi visible que « Tout accepter » (même premier écran, même taille, même mise en valeur). Refuser ne doit pas demander plus de clics qu'accepter.
- Pas de case **précochée**, pas de consentement par **poursuite de navigation** ou défilement.
- Les **finalités** sont listées avant le consentement, avec la liste des **tiers** accessible.
- Un moyen de **retirer** son consentement à tout moment, aussi simple que de le donner (lien permanent en pied de page, par exemple).
- Pas d'interface trompeuse : couleurs qui poussent à accepter, formulations ambiguës, croix de fermeture qui vaut acceptation. Fermer le bandeau doit valoir refus.

Écart typique : pas de bouton « Tout refuser » au premier niveau. Gravité par défaut `[HAUTE]`, exposition FORTE.

## Test 3 — Après refus

1. Profil vierge. Cliquer « Tout refuser ».
2. Naviguer sur 2 ou 3 pages.
3. Observer les requêtes pendant 10 à 20 secondes sur chaque page.

Écart typique : des traceurs non nécessaires partent malgré le refus, ou le bandeau ne mémorise pas le choix. Gravité par défaut `[HAUTE]` : c'est la situation la plus lourdement sanctionnée, car le choix de la personne est ignoré.

Vérifier aussi la **durée** du choix : la CNIL recommande de conserver le refus aussi longtemps que l'acceptation, et de ne pas redemander avant un délai raisonnable (elle cite 6 mois comme référence).

## Test 4 — Après acceptation et retrait

1. Accepter, vérifier que les traceurs annoncés partent (et seulement eux).
2. Retirer le consentement par le lien prévu.
3. Vérifier que les traceurs s'arrêtent et que les cookies sont supprimés ou neutralisés.

## Mesure d'audience exemptée

La CNIL admet sans consentement une mesure d'audience **strictement limitée** :
- finalité limitée à la mesure de fréquentation du site, pour son éditeur seul ;
- données non recoupées avec d'autres traitements, ni transmises à des tiers pour leur propre usage ;
- durée de vie des traceurs limitée à **13 mois**, données conservées **25 mois** au plus ;
- information des personnes et possibilité de s'opposer.

Un outil d'analyse qui réutilise les données pour son propre compte ou les envoie hors UE sans encadrement n'est pas exempté.

## Test 5 — Formulaires

Pour chaque formulaire (contact, inscription, devis, candidature, paiement, lettre d'information) :

- **Minimisation** : chaque champ obligatoire est-il nécessaire à la finalité ? Un numéro de téléphone obligatoire pour une lettre d'information est un écart.
- **Information au point de collecte** (art. 13) : au minimum, responsable, finalité, base légale, destinataires, durée, droits, avec un lien vers la politique. Une mention en bas du formulaire suffit si elle renvoie à une information complète.
- **Consentement séparé** pour la prospection : case non précochée, distincte de l'acceptation des conditions générales.
- **Champs libres** : signaler le risque de saisie de données sensibles et recommander un avertissement.
- **Transmission** : le formulaire envoie-t-il les données en HTTPS ? À qui (requête réseau vers un tiers à la soumission) ?
- **Mineurs** : si le service vise ou attire des mineurs, vérifier l'âge et le consentement parental en dessous de **15 ans** en France (art. 45 de la loi Informatique et Libertés).

## Test 6 — Information des personnes

C'est le thème de l'action coordonnée du CEPD en 2026 : la complétude de l'information est contrôlée dans toute l'Europe.

- Une **politique de confidentialité** est accessible en 1 clic depuis chaque page.
- Elle contient tous les éléments de l'art. 13 (et 14 si des données sont collectées indirectement) : identité et coordonnées du responsable, du DPO s'il existe, finalités et bases légales par traitement, intérêts légitimes invoqués, destinataires, transferts hors UE et garanties, durées de conservation, droits, droit de réclamation auprès de la CNIL, caractère obligatoire des données, décision automatisée.
- Elle correspond **à la réalité observée** : comparer la liste des tiers et traceurs observés aux tests 1 à 4 avec celle de la politique. Un tiers observé mais non déclaré est un écart.
- Elle est claire et compréhensible (art. 12), datée, et dans la langue du public visé.
- Les **mentions légales** existent et identifient l'éditeur et l'hébergeur (voir le skill `mentions-legales`).

## Test 7 — Sécurité visible de l'extérieur

Sans test actif, observer seulement :

- **HTTPS** partout, redirection automatique depuis HTTP, certificat valide.
- En-tête de sécurité de transport strict (HSTS) présent.
- Cookies de session avec les attributs de sécurité (`Secure`, `HttpOnly`, `SameSite`).
- **Politique de mot de passe** à l'inscription : longueur et complexité suffisantes (voir `references/securite.md`).
- Message d'erreur de connexion qui ne révèle pas si un compte existe.
- Absence de données personnelles dans les **URL** (adresse électronique en paramètre, identifiants dans les liens envoyés aux tiers).

Tout sondage plus poussé (fichiers exposés, ports, injections) est un **test actif** : uniquement avec autorisation écrite.

## Test 8 — Courriels

Si l'audit permet de s'inscrire avec une adresse de test :

- Les courriels reçus contiennent-ils des **pixels de suivi** (image invisible qui signale l'ouverture) ? Depuis la recommandation CNIL du 12 mars 2026 (publiée le 14 avril 2026), ces pixels exigent le consentement, sauf exceptions étroites (sécurité, authentification, mesure individuelle de délivrabilité). La période de mise en conformité pour les adresses collectées avant le 14 avril 2026 a pris fin le 14 juillet 2026.
- Un lien de **désinscription** fonctionne-t-il en un clic ?
- La prospection respecte-t-elle le régime applicable : consentement préalable pour les particuliers (art. L. 34-5 du Code des postes et des communications électroniques), sauf produits ou services analogues pour un client existant.

## Applications mobiles

Mêmes questions, avec des points propres (recommandations CNIL de septembre 2024, modifiées en avril 2025) :
- **Permissions** demandées : chacune est-elle nécessaire ? Demandée au moment où elle sert ?
- **Kits tiers intégrés** (bibliothèques d'analyse, de publicité, de crash) : quelles données envoient-ils avant consentement ?
- Information et consentement **dans l'application**, pas seulement sur le site.
- Fiche de la boutique d'applications cohérente avec la réalité.

L'analyse du trafic d'une application exige des outils spécialisés. Sans eux, s'appuyer sur la déclaration de confidentialité de la boutique et sur le code si disponible, et classer le reste `[À VÉRIFIER]`.

## Ce qu'il faut consigner pour chaque constat

- URL exacte et gabarit de page.
- État du consentement au moment du constat (aucun, refusé, accepté).
- Domaine tiers ou nom du traceur, et ce qu'il transmet si visible (identifiant, URL visitée, adresse IP).
- Moment d'apparition (au chargement, après 5 s, au défilement).
- Date et heure.

## Sources

- CNIL, lignes directrices et recommandation « cookies et autres traceurs » (délibérations 2020-091 et 2020-092 du 17 septembre 2020) : https://www.cnil.fr/fr/cookies-et-autres-traceurs/regles/cookies
- CNIL, cookies et traceurs exemptés de consentement (mesure d'audience) : https://www.cnil.fr/fr/cookies-et-autres-traceurs/regles/cookies-solutions-pour-les-outils-de-mesure-daudience
- CNIL, recommandation sur les pixels de suivi dans les courriels (2026) : https://cnil.fr/fr/recommandation-pixel-suivi-courriels
- CNIL, recommandations applications mobiles : https://www.cnil.fr/fr/recommandations-applications-mobiles
- CEPD, rapport de la task force « bandeaux cookies » (janvier 2023) : https://www.edpb.europa.eu/documents/task-force-report/report-of-the-work-undertaken-by-the-cookie-banner-taskforce_en
- CEPD, lignes directrices 2/2023 sur le champ technique de l'art. 5.3 de la directive ePrivacy : https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-22023-technical-scope-art-53-eprivacy-directive_fr
- CEPD, programme « Support Pool of Experts » (dont l'outil d'audit de sites web) : https://www.edpb.europa.eu/support-pool-of-experts-spe-programme_fr
- Loi Informatique et Libertés, art. 82 et art. 45 : https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000886460
