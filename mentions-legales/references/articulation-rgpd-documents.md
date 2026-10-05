# Articulation avec le RGPD et les autres documents légaux

Un site a en général **plusieurs pages légales**, chacune avec un objet propre. L'erreur classique est de tout fondre dans « Mentions légales » : la page devient longue, illisible, et les informations RGPD y sont incomplètes. La bonne pratique : **une page par objet, reliées par des liens**, et un pied de page qui les expose toutes.

## Sommaire

1. [Qui va où](#1-qui-va-où)
2. [La section « Données personnelles » des mentions légales](#2-la-section--données-personnelles--des-mentions-légales)
3. [La section « Cookies »](#3-la-section--cookies-)
4. [Cohérence entre mentions légales et politique de confidentialité](#4-cohérence-entre-mentions-légales-et-politique-de-confidentialité)
5. [CGU, CGV, accessibilité](#5-cgu-cgv-accessibilité)
6. [Cas du petit site : une seule page ?](#6-cas-du-petit-site--une-seule-page-)
7. [Sources](#sources)

## 1. Qui va où

| Document | Objet | Fondement | Skill |
|---|---|---|---|
| **Mentions légales** | Identifier l'éditeur, le directeur de la publication, l'hébergeur ; médiateur, activité réglementée | LCEN art. 1-1 et 19, C. com., C. consom. | `mentions-legales` |
| **Politique de confidentialité** | Informer sur les traitements de données : responsable, finalités, bases légales, durées, destinataires, transferts, droits, DPO, réclamation CNIL | RGPD art. 12 à 14 | `rgpd` (`assets/politique-confidentialite.md`) |
| **Politique cookies** + module de gestion | Informer sur les traceurs et recueillir / retirer le consentement | Loi Informatique et Libertés art. 82, lignes directrices CNIL | `rgpd` (`references/consentement-cookies.md`) |
| **Mentions d'information sur formulaire** | Information courte au point de collecte | RGPD art. 13 | `rgpd` (`assets/information-personnes.md`) |
| **CGU** | Règles d'usage du service, comptes, contenus des utilisateurs | Droit des contrats, DSA le cas échéant | — |
| **CGV** | Conditions de vente : prix, livraison, rétractation, garanties, médiateur | C. consom. | — |
| **Déclaration d'accessibilité** | Niveau de conformité RGAA, contenus non accessibles, contact | Loi 2005-102 art. 47, directive (UE) 2019/882 | — |

Les mentions légales disent **qui** ; la politique de confidentialité dit **ce qu'on fait des données**. Les deux se renvoient l'une à l'autre.

## 2. La section « Données personnelles » des mentions légales

Courte, et **seulement un renvoi**. Elle contient :

- une phrase indiquant que le site traite des données personnelles et qui en est responsable ;
- le **lien** vers la politique de confidentialité ;
- le **contact** pour exercer ses droits (e-mail dédié ou contact du DPO s'il y en a un) ;
- le rappel du droit d'introduire une réclamation auprès de la **CNIL** (facultatif ici puisqu'il figure dans la politique, mais utile).

Modèle :

> [Éditeur] traite des données personnelles dans le cadre de ce site, en qualité de responsable de traitement. Les finalités, bases légales, durées de conservation, destinataires et vos droits sont détaillés dans notre [politique de confidentialité](/politique-de-confidentialite).
>
> Pour exercer vos droits (accès, rectification, effacement, opposition, limitation, portabilité), écrivez à [e-mail dédié ou DPO]. Vous pouvez aussi introduire une réclamation auprès de la CNIL ([cnil.fr](https://www.cnil.fr)).

**Si le site ne collecte réellement aucune donnée** (site statique, sans formulaire, sans statistiques ni cookies non essentiels, sans polices ou vidéos tierces chargées depuis un serveur externe) : ne pas inventer une politique ; une phrase suffit (« Ce site ne collecte pas de données personnelles et ne dépose pas de cookies soumis à consentement »). **Vérifie-le** avant de l'écrire : les journaux serveur de l'hébergeur, une police chargée depuis un service tiers ou une vidéo intégrée suffisent à créer un traitement. Dans un projet de code, inspecte les scripts, balises et intégrations tiers.

**Si la politique de confidentialité n'existe pas** alors qu'il y a collecte : dis-le à l'utilisateur et propose de la rédiger avec le skill `rgpd`, plutôt que de livrer un lien mort.

## 3. La section « Cookies »

- Renvoi vers la **politique cookies** (ou la section cookies de la politique de confidentialité).
- **Lien ou bouton permettant de modifier ses choix à tout moment** (« Gérer mes cookies ») : le retrait du consentement doit être aussi simple que son recueil. Dans une page web, ce lien ouvre le module de gestion du consentement.
- Si aucun traceur soumis à consentement n'est déposé, le dire en une phrase.

Pour les règles de fond (liste des traceurs exemptés, durée de 13 mois, bouton « Tout refuser »), charge `references/consentement-cookies.md` du skill `rgpd`.

## 4. Cohérence entre mentions légales et politique de confidentialité

Vérifie que les deux documents concordent sur :

- **L'identité** : l'éditeur des mentions légales est en principe le **responsable de traitement** de la politique (même dénomination, même adresse). Si ce n'est pas le cas (ex. site édité par une filiale, données traitées par la maison mère), l'expliquer.
- **L'hébergeur et le stockage des données** : ils figurent aussi parmi les **sous-traitants / destinataires** de la politique de confidentialité, avec leur localisation. Un hébergeur hors UE implique une section « transferts » dans la politique (skill `rgpd`, `references/transferts-internationaux.md`).
- **Les contacts** : même adresse e-mail pour les demandes relatives aux données.
- **Les dates** de mise à jour : modifier l'un peut imposer de modifier l'autre.

## 5. CGU, CGV, accessibilité

- **CGV** (vente à des consommateurs) : les mentions légales **renvoient** aux CGV, et reprennent le médiateur (qui doit figurer aussi dans les CGV).
- **CGU** (comptes, contenus des utilisateurs, SaaS) : renvoi, et dans les CGU le mécanisme de signalement des contenus illicites.
- **Accessibilité** : si l'entité est concernée, section « Accessibilité » avec le niveau de conformité et le lien vers la déclaration d'accessibilité.

## 6. Cas du petit site : une seule page ?

Pour un petit site vitrine avec un simple formulaire de contact, il est admis de réunir mentions légales et politique de confidentialité sur **une même page**, à condition que :

- les deux parties soient **clairement séparées** (titres distincts, sommaire commun avec les deux parties) ;
- l'information RGPD reste **complète** (art. 13 : responsable, finalités, base légale, durée, destinataires, droits, réclamation CNIL) — ce n'est pas une version allégée ;
- le pied de page expose un lien direct vers chacune des parties (ancres).

Titre possible : « Mentions légales et politique de confidentialité ». Au-delà d'un site vitrine simple (comptes, e-commerce, analytics, newsletter), sépare les pages.

## Sources

- [RGPD, articles 12 à 14 — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- [Loi Informatique et Libertés, article 82 — Légifrance](https://www.legifrance.gouv.fr/loda/article_lc/LEGIARTI000037813978/)
- [Cookies et autres traceurs — CNIL](https://www.cnil.fr/fr/cookies-et-autres-traceurs/regles/cookies)
- [Obligations d'un site internet professionnel — Service-public.fr (Entreprendre)](https://entreprendre.service-public.gouv.fr/vosdroits/F31228)
- [Déclaration d'accessibilité — RGAA](https://accessibilite.numerique.gouv.fr/obligations/declaration-accessibilite/)
