# Structure et rédaction des mentions légales

Des mentions légales justes mais illisibles ratent leur but : l'utilisateur, le client ou l'autorité qui les consulte cherche **une information précise** (qui édite ? comment le joindre ? qui héberge ? quel médiateur ?). La page doit permettre de la trouver en quelques secondes. D'où trois règles : **un sommaire**, **un ordre stable**, **des blocs courts**.

## Sommaire

1. [Anatomie de la page](#1-anatomie-de-la-page)
2. [Le sommaire : règles de construction](#2-le-sommaire--règles-de-construction)
3. [Ordre des sections](#3-ordre-des-sections)
4. [Style d'écriture](#4-style-décriture)
5. [Sections facultatives : quand et comment](#5-sections-facultatives--quand-et-comment)
6. [Mise à jour et versionnage](#6-mise-à-jour-et-versionnage)
7. [Erreurs fréquentes](#7-erreurs-fréquentes)
8. [Sources](#sources)

## 1. Anatomie de la page

Dans cet ordre, toujours :

1. **Titre unique** (niveau 1) : « Mentions légales ».
2. **Date de dernière mise à jour** : « Dernière mise à jour : 30 septembre 2026 » (date en toutes lettres, pas de format ambigu 09/10).
3. **Phrase d'introduction** (une ou deux lignes) : ce que contient la page et, si utile, le fondement (« En application de l'article 1-1 de la loi n° 2004-575 du 21 juin 2004 pour la confiance dans l'économie numérique… »). Facultative, mais elle oriente.
4. **Sommaire** numéroté et cliquable.
5. **Sections numérotées** (niveau 2), dans l'ordre du sommaire, avec, si nécessaire, des sous-sections (niveau 3).
6. **Pied de page de la page** : rappel des documents liés (politique de confidentialité, cookies, CGU/CGV, accessibilité).

## 2. Le sommaire : règles de construction

Le sommaire est **obligatoire dans toute page produite avec ce skill**.

- **Placé juste après la date** de mise à jour, avant la première section.
- **Liste numérotée** dont chaque entrée reprend **exactement** l'intitulé de la section (même numéro, même libellé). Un décalage entre sommaire et titres est l'erreur la plus fréquente : vérifie-la en dernier.
- **Chaque entrée est un lien d'ancre** vers sa section (`#editeur`, `#hebergement`…).
- **Ancres courtes, stables, sans accent ni espace**, en français : `editeur`, `directeur-publication`, `hebergement`, `contact`, `mediation`, `propriete-intellectuelle`, `donnees-personnelles`, `cookies`, `accessibilite`, `credits`. Elles ne doivent pas changer d'une version à l'autre (des liens externes et le pied de page peuvent pointer dessus, par exemple `/mentions-legales#hebergement`).
- **Un seul niveau** dans le sommaire en principe (les sections de niveau 2). N'ajoute le niveau 3 que si la page est longue (plus de 8 à 10 sections, ou sous-sections consultées directement).
- **Libellés courts et parlants** : « Éditeur du site », pas « Article 1 — Informations relatives à l'identification de l'éditeur du présent site ».
- En **Markdown**, les ancres automatiques dépendent du moteur de rendu (GitHub, CMS, MDX) et gèrent mal les accents : préfère des **ancres explicites** (`<a id="editeur"></a>` ou `## 1. Éditeur du site {#editeur}` si le moteur le supporte). En **HTML/JSX**, mets l'`id` sur le titre de section. Voir `references/integration-web.md`.
- Optionnel sur les pages longues : un lien « ↑ Retour au sommaire » en fin de section.

Exemple (Markdown) :

```markdown
# Mentions légales

*Dernière mise à jour : 30 septembre 2026*

## Sommaire

1. [Éditeur du site](#editeur)
2. [Directeur de la publication](#directeur-publication)
3. [Hébergement](#hebergement)
4. [Nous contacter](#contact)
5. [Médiation de la consommation](#mediation)
6. [Propriété intellectuelle](#propriete-intellectuelle)
7. [Données personnelles](#donnees-personnelles)
8. [Cookies](#cookies)
9. [Accessibilité](#accessibilite)
```

## 3. Ordre des sections

Du **plus exigé** au **plus accessoire** : l'identification d'abord, les renvois ensuite, le confort en dernier.

| # | Section | Statut | Ancre |
|---|---|---|---|
| 1 | Éditeur du site | Obligatoire | `editeur` |
| 2 | Directeur de la publication | Obligatoire | `directeur-publication` |
| 3 | Hébergement (et stockage des données si distinct) | Obligatoire | `hebergement` |
| 4 | Nous contacter | Recommandé (obligatoire pour l'e-mail en e-commerce ; peut être fusionné dans « Éditeur ») | `contact` |
| 5 | Activité réglementée | Sous condition | `activite-reglementee` |
| 6 | Médiation de la consommation | Sous condition (vente aux consommateurs) | `mediation` |
| 7 | Propriété intellectuelle | Recommandé | `propriete-intellectuelle` |
| 8 | Données personnelles | Sous condition (collecte de données) — renvoi | `donnees-personnelles` |
| 9 | Cookies | Sous condition (traceurs) — renvoi | `cookies` |
| 10 | Accessibilité | Sous condition | `accessibilite` |
| 11 | Crédits | Facultatif | `credits` |

**Retire les sections sans objet** plutôt que de les laisser vides ; renumérote ensuite sommaire et titres ensemble.

## 4. Style d'écriture

- **Identification en liste ou tableau**, pas en prose : chaque donnée sur sa ligne, avec son libellé (« Siège social : … »). Le lecteur cherche une donnée, pas un paragraphe.
- **Troisième personne neutre ou « nous »**, cohérent sur toute la page. Pour un particulier : « l'éditeur » ou « je », au choix, mais constant.
- **Phrases courtes**, voix active, vocabulaire courant. Garde les termes juridiques nécessaires (« directeur de la publication », « hébergeur ») sans les paraphraser : ce sont eux que le lecteur cherche.
- **Références légales sobres** : une mention de texte en introduction ou en tête de section suffit ; ne transforme pas la page en mémoire juridique.
- **Coordonnées cliquables** : `mailto:` pour l'e-mail, `tel:` pour le téléphone (format international `+33…`), liens complets vers le médiateur, la politique de confidentialité, etc.
- **Aucune formule d'intimidation** (« toute reproduction sera poursuivie avec la plus grande sévérité ») ni **exonération générale** (« l'éditeur décline toute responsabilité ») : juridiquement faibles, parfois abusives face à un consommateur, et elles abîment la confiance. Préfère une formulation factuelle (voir section 5).
- **Pas de langage marketing** : cette page n'est pas une page « À propos ».
- **Langue** : le français est de rigueur pour un site destiné au public français (loi n° 94-665 du 4 août 1994, dite loi Toubon, pour l'information des consommateurs). Une version anglaise peut s'ajouter, elle ne remplace pas.

## 5. Sections facultatives : quand et comment

**Propriété intellectuelle** (recommandé) — rappeler sobrement que les contenus sont protégés et à qui ils appartiennent, sans prétendre à des droits qu'on n'a pas (photos de banques d'images, polices, logos tiers).

> Les contenus de ce site (textes, images, logos, code) sont protégés par le droit d'auteur et, le cas échéant, le droit des marques. Sauf mention contraire, ils appartiennent à [Éditeur]. Toute reproduction ou réutilisation non autorisée est interdite, sous réserve des exceptions prévues par le Code de la propriété intellectuelle (courte citation, notamment).

Si des contenus sont sous **licence libre** (CC BY, MIT…) ou proviennent de tiers, le dire : c'est plus juste qu'une interdiction générale.

**Liens hypertextes** (facultatif) — une phrase suffit : l'éditeur n'exerce pas de contrôle sur les sites tiers liés. Ne pas « interdire » les liens pointant vers le site : c'est en principe libre (sauf pratiques déloyales comme le framing trompeur).

**Crédits** (facultatif) — conception, développement, photographies, illustrations, polices, icônes. Les **crédits photo** peuvent être exigés par la licence de l'image : vérifier.

**Responsabilité** (facultatif, prudence) — si l'utilisateur tient à une clause, la limiter à des faits : informations fournies à titre indicatif, mises à jour régulières, signalement possible d'une erreur à [contact]. Jamais d'exclusion totale de responsabilité.

**Signalement de contenus illicites** (sous condition) — si le site héberge des contenus publiés par des utilisateurs (commentaires, avis, forum), indiquer comment signaler un contenu illicite. Pour les plateformes, le règlement (UE) 2022/2065 (DSA) impose en outre un **point de contact unique** : à traiter dans les CGU et le signaler.

## 6. Mise à jour et versionnage

- **Mettre à jour la date** à chaque modification substantielle.
- **Déclencheurs** : changement de siège, de dirigeant (donc de directeur de la publication), de forme juridique ou de capital, d'hébergeur, de médiateur, de numéro de téléphone ; début d'une activité de vente ; ajout d'un outil qui dépose des cookies.
- Dans un projet de code, centraliser les informations de l'éditeur dans **une seule source** (fichier de configuration) réutilisée par la page et le pied de page : cela évite les incohérences (voir `references/integration-web.md`).

## 7. Erreurs fréquentes

| Erreur | Correction |
|---|---|
| Pas de sommaire, ou sommaire désynchronisé des titres | Sommaire numéroté, libellés identiques aux titres, ancres vérifiées |
| L'agence web identifiée comme éditeur | L'éditeur est le client ; l'agence peut figurer dans « Crédits » |
| Directeur de la publication = une société ou « la rédaction » | Une personne physique, en principe le représentant légal |
| Hébergeur sans téléphone ou avec une adresse périmée | Reprendre les données sur la page légale de l'hébergeur, à la date du jour |
| « Déclaration CNIL n° … » | Supprimer (formalité disparue en 2018) |
| Lien vers la plateforme ODR européenne | Supprimer (fermée le 20 juillet 2025) ; garder le médiateur |
| Politique de confidentialité recopiée intégralement dans les mentions légales | Page distincte ; une section de renvoi courte (skill `rgpd`) |
| Formulaire de contact seul pour un site marchand | Ajouter une adresse e-mail (LCEN art. 19) |
| Capital social manquant pour une société | L'ajouter (et « à capital variable » si c'est le cas) |
| Micro-entrepreneur sans « EI » | Ajouter « EI » ou « entrepreneur individuel » au nom |
| Médiateur cité sans adhésion réelle | Vérifier la convention avec le médiateur |
| « © 2019 » figé dans le pied de page | Année dynamique ou retirer l'année ; le droit d'auteur ne dépend pas de cette mention |
| Mentions légales en image ou PDF non accessible | Texte HTML (« standard ouvert ») |
| Page introuvable (lien absent du pied de page, ou seulement sur l'accueil) | Lien « Mentions légales » dans le pied de page de **toutes** les pages |

## Sources

- [LCEN, article 1-1 — Légifrance](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000801164)
- [Obligations d'un site internet professionnel — Service-public.fr (Entreprendre)](https://entreprendre.service-public.gouv.fr/vosdroits/F31228)
- [Loi n° 94-665 du 4 août 1994 relative à l'emploi de la langue française — Légifrance](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000349929)
- [Règlement (UE) 2022/2065 sur les services numériques (DSA) — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2022/2065/oj)
