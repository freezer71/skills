---
name: mentions-legales
description: Rédaction correcte, complète et bien structurée des mentions légales d'un site internet, d'une application ou d'un service en ligne en droit français (LCEN modifiée par la loi SREN, Code de commerce, Code de la consommation, loi de 1982 sur le directeur de la publication, accessibilité numérique). À utiliser systématiquement dès que l'utilisateur veut écrire, générer, relire, auditer ou mettre à jour des « mentions légales », une page « informations légales », « legal notice », « imprint », « à propos / éditeur du site », ou demande « quelles mentions sont obligatoires sur mon site », « que mettre dans le pied de page légal », « qui est l'hébergeur / le directeur de la publication », « mentions obligatoires pour un auto-entrepreneur / une SAS / une association / un e-commerce / un avocat / un agent immobilier », « faut-il un numéro CNIL », « lien vers le médiateur de la consommation ». Produit toujours une page structurée avec un sommaire cliquable. Couplé au skill `rgpd` : les mentions légales renvoient vers la politique de confidentialité et la gestion des cookies, qu'elles ne remplacent pas. S'applique aussi à la création d'une page de mentions légales dans un projet web (Next.js, React, HTML, CMS).
---

# Skill Mentions légales — Rédiger des mentions légales justes, complètes et lisibles

Ce skill capture la pratique de rédaction des **mentions légales** d'un service en ligne en droit français : ce que la loi exige selon le profil de l'éditeur (particulier, entrepreneur individuel, société, association, e-commerce, profession réglementée, presse, secteur public), **comment l'écrire** (structure, sommaire, style), et **comment l'articuler** avec les documents voisins (politique de confidentialité, cookies, CGU/CGV, déclaration d'accessibilité). Cadre : droit français à jour de la **loi SREN du 21 mai 2024** et de la fermeture de la plateforme européenne de règlement en ligne des litiges (20 juillet 2025).

## Quand utiliser ce skill

Active-toi systématiquement quand l'utilisateur :
- Demande d'**écrire, générer, compléter, relire ou auditer** des mentions légales (page web, application mobile, SaaS, boutique en ligne, blog, site vitrine)
- Crée une **page `/mentions-legales`** ou un **pied de page légal** dans un projet web
- Se demande **quelles mentions sont obligatoires** pour son statut (micro-entreprise, EI, SAS, SARL, association, profession libérale, collectivité…)
- Cherche **qui est l'éditeur, le directeur de la publication, l'hébergeur**, ou comment les désigner
- Évoque le **médiateur de la consommation**, le **numéro de TVA**, le **RCS / SIREN / RNE**, le **capital social**, l'**ORIAS**, la **carte professionnelle**
- Mélange mentions légales, **politique de confidentialité**, **cookies** et **CGU/CGV** (il faut alors démêler et répartir)
- Recopie un **vieux modèle** (numéro de déclaration CNIL, « article 6 de la LCEN », lien vers la plateforme ODR) qu'il faut mettre à jour

N'attends pas le mot exact : « page légale », « legal », « imprint », « infos éditeur », « bas de page obligatoire » relèvent de ce skill.

## Couplage avec le skill `rgpd`

Les mentions légales **identifient** l'éditeur ; la politique de confidentialité **informe** sur les traitements de données (art. 13-14 RGPD). Ce sont deux documents distincts, reliés par des liens.

- Pour tout ce qui concerne les **données personnelles, les cookies, le consentement, le DPO**, charge le skill **`rgpd`** (notamment `assets/politique-confidentialite.md`, `assets/information-personnes.md` et `references/consentement-cookies.md` de ce skill).
- Dans les mentions légales, ne rédige qu'**une section courte de renvoi** (voir `references/articulation-rgpd-documents.md`) : jamais la politique de confidentialité entière recopiée dans la page.
- Si la politique de confidentialité **n'existe pas encore** et que le site collecte des données (formulaire, compte, analytics, cookies), signale-le explicitement et propose de la rédiger avec le skill `rgpd` : des mentions légales qui renvoient vers une page absente sont un défaut, pas une formalité.

## Principes directeurs de rédaction

1. **Toujours un sommaire.** Toute page de mentions légales produite commence par un titre, la date de mise à jour, puis un **sommaire numéroté et cliquable** (liens d'ancre vers chaque section). C'est non négociable : la page doit se parcourir en quelques secondes. Voir `references/structure-et-redaction.md`.
2. **Ne jamais inventer une donnée d'identification.** SIREN, adresse, capital, téléphone, hébergeur, médiateur : si l'information n'est pas fournie, écris un marqueur visible `[À COMPLÉTER : …]` et liste les manques en fin de réponse. Une mention légale fausse est pire qu'une mention manquante : elle engage l'éditeur.
3. **Qualifier d'abord le profil de l'éditeur**, puis choisir les mentions. Les obligations d'un particulier, d'une SAS e-commerce et d'un avocat ne sont pas les mêmes. Utilise `assets/questionnaire-collecte.md` pour recueillir ce qu'il faut.
4. **Distinguer obligatoire, obligatoire sous condition et recommandé.** Ne présente pas une clause de confort (propriété intellectuelle, liens hypertextes) comme une exigence légale, et inversement.
5. **Écrire clair et sobre.** Phrases courtes, tableaux ou listes pour l'identification, pas de jargon inutile, pas de clauses d'intimidation ni d'exonérations de responsabilité générales (souvent inopérantes, et abusives face à un consommateur).
6. **Citer le texte à jour** quand tu expliques une obligation (ex. « LCEN, art. 1-1 », « C. consom., art. L. 616-1 »). Pas d'articles périmés dans la page livrée.
7. **Livrer un document prêt à intégrer** dans le format demandé (Markdown, HTML, JSX/TSX, texte pour CMS), avec des ancres stables. Voir `references/integration-web.md`.
8. **Préciser la limite du conseil.** Tu aides à rédiger, tu ne délivres pas un avis juridique engageant. Pour une activité réglementée complexe, un contentieux ou une mise en demeure, recommande un avocat.

## Architecture du skill — où chercher quoi

Charge le fichier de référence pertinent **au moment où le sujet apparaît**. Ne charge pas tout d'avance.

| Sujet de la question | Fichier de référence |
|---|---|
| Textes applicables (LCEN art. 1-1, 1-2 et 19, loi de 1982, C. com., C. consom.), sanctions, qui est éditeur / hébergeur / directeur de la publication | `references/cadre-juridique.md` |
| Mentions exigées selon le profil : particulier, EI/micro-entreprise, société, association, e-commerce, profession réglementée, presse en ligne, secteur public, éditeur hors UE, application mobile | `references/mentions-par-profil.md` |
| Comment écrire : plan type, sommaire, ordre des sections, style, mise à jour, erreurs fréquentes | `references/structure-et-redaction.md` |
| Articulation avec le RGPD, les cookies, les CGU/CGV, l'accessibilité : qui va où, quels liens | `references/articulation-rgpd-documents.md` |
| Intégration dans un site : pied de page, ancres, HTML sémantique, composant Next.js/React, accessibilité de la page | `references/integration-web.md` |

## Modèles prêts à l'emploi (à adapter, pas à copier tel quel)

| Besoin | Modèle |
|---|---|
| Recueillir les informations avant d'écrire | `assets/questionnaire-collecte.md` |
| Rédiger la page complète, avec sommaire et blocs conditionnels par profil | `assets/modele-mentions-legales.md` |
| Relire ou auditer des mentions légales existantes | `assets/checklist-audit.md` |

## Workflow standard

1. **Qualifie le cas.** Qui édite le service (personne physique ou morale, professionnel ou non) ? Quelle activité (vitrine, vente aux consommateurs, B2B, presse, activité réglementée, service public) ? Quel support (site, app, SaaS) ? Où est-il hébergé ?
2. **Recueille les données** avec `assets/questionnaire-collecte.md`. Si le projet est un dépôt de code, cherche d'abord les informations déjà présentes (pied de page, page existante, `package.json`, configuration de déploiement pour l'hébergeur) avant de poser des questions — et fais confirmer ce que tu déduis.
3. **Sélectionne les mentions** applicables avec `references/mentions-par-profil.md`.
4. **Rédige** à partir de `assets/modele-mentions-legales.md` : titre, date de mise à jour, **sommaire**, sections numérotées, en retirant les blocs sans objet (ne laisse pas de sections vides ou « non applicable » sans raison).
5. **Relie** la page à la politique de confidentialité et à la gestion des cookies (skill `rgpd`) et, le cas échéant, aux CGV/CGU et à la déclaration d'accessibilité.
6. **Contrôle** avec `assets/checklist-audit.md`, puis termine la réponse par : la liste des `[À COMPLÉTER]` restants, les documents voisins manquants, et les points à faire valider par un professionnel s'il y en a.

## Mises en garde transverses

- **Le numéro de déclaration CNIL n'existe plus** depuis l'entrée en application du RGPD (25 mai 2018) pour la quasi-totalité des traitements : ne jamais l'écrire, le retirer lors d'un audit.
- **Le lien vers la plateforme européenne de règlement en ligne des litiges (ODR/RLL) n'est plus exigé** : la plateforme a fermé le 20 juillet 2025 (règlement (UE) 2024/3228). Le **médiateur de la consommation**, lui, reste obligatoire pour les professionnels qui vendent à des consommateurs.
- **Depuis la loi SREN**, l'identification de l'éditeur figure à l'**article 1-1** de la LCEN et les sanctions à l'**article 1-2** (anciennement article 6, III et VI). Mettre à jour les références dans les vieux modèles.
- **L'agence web n'est pas l'éditeur.** Les mentions légales identifient celui pour le compte duquel le site est publié. Un crédit « site réalisé par » est facultatif et distinct.
- **Le directeur de la publication est une personne physique**, en principe le représentant légal pour une personne morale — pas une société, pas un service.
- **Un site sans mentions légales à jour expose à des sanctions pénales** (jusqu'à un an d'emprisonnement et 75 000 € d'amende pour une personne physique) — le risque réel tient surtout aux contrôles DGCCRF pour les sites marchands et à la perte de confiance des utilisateurs.

## Sources officielles à privilégier

- LCEN (loi n° 2004-575 du 21 juin 2004), version consolidée : [legifrance.gouv.fr](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000801164)
- Obligations d'un site internet professionnel : [entreprendre.service-public.gouv.fr](https://entreprendre.service-public.gouv.fr/vosdroits/F31228)
- Médiation de la consommation : [economie.gouv.fr/mediation-conso](https://www.economie.gouv.fr/mediation-conso)
- Accessibilité numérique (RGAA) : [accessibilite.numerique.gouv.fr](https://accessibilite.numerique.gouv.fr)
- CNIL : [cnil.fr](https://www.cnil.fr)
