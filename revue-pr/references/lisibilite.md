# Lisibilité du rapport

Le rapport doit se **parcourir** avant de se lire. L'utilisateur est dyslexique : il repère l'information par sa place et par ses repères visuels, pas en lisant des paragraphes. Ces règles ne sont pas du style : un rapport qui ne les suit pas est un rapport raté, même si son contenu est juste.

## 1. Une architecture fixe

- Le rapport a **toujours les mêmes parties, dans le même ordre** : Verdict, Ce que la PR ajoute, Structures de données, Sécurité, Code, Avant de fusionner. Une partie vide tient en une ligne (« Aucune faille trouvée. »), elle ne disparaît pas : l'utilisateur sait où regarder.
- Les parties sont **numérotées de 1 à 6**, toujours avec le même titre (voir `assets/modele-rapport.md`).
- Les parties sont séparées par une ligne horizontale (`---`).

## 2. Un bloc par élément

- Chaque faille, chaque bug, chaque point d'entrée, chaque structure de données est un **bloc séparé**, avec son propre titre.
- Dans un bloc de même nature, les **libellés sont toujours les mêmes, dans le même ordre**. Pour une faille : Où, Problème, Risque, Correction. Pour un bug : Où, Problème, Conséquence, Correction. Ne jamais changer un libellé pour varier.
- Un libellé par ligne, en gras, suivi de deux points.

## 3. Des phrases courtes

- **Une idée par ligne.** Une phrase par puce.
- Phrases de **15 mots environ**, 20 au plus. Sujet, verbe, complément.
- Commencer par l'information utile : « Le point d'entrée n'est pas protégé. » plutôt que « Il convient de noter qu'en l'état, le point d'entrée… ».
- Pas de paragraphe de plus de deux lignes. Au-delà, découper en puces.
- Les mots courants avant le jargon. Un terme technique nécessaire est expliqué en quelques mots la première fois : « IDOR (accès à la donnée d'un autre utilisateur) ».
- Pas d'abréviation non expliquée.
- Toujours le même mot pour la même chose : si c'est un « point d'entrée », ce n'est pas ailleurs un « endpoint » ou une « route ».

## 4. Mise en forme

- **Pas d'italique** : il déforme les lettres et gêne la lecture.
- Pas de texte souligné. Pas de phrase entière en majuscules : les majuscules sont réservées aux étiquettes courtes fixes (gravité, statut, verdict).
- **Gras réservé aux libellés et aux mots-clés** (deux ou trois mots par bloc au plus). Trop de gras, plus rien ne ressort.
- Code et noms de fichiers en `code`, sur leur propre ligne quand c'est long.
- Les nombres en chiffres (« 3 failles », pas « trois failles »).

## 5. Tableaux

- Dans le terminal, un tableau large se replie et devient illisible. **Au plus 3 colonnes**, avec des cellules courtes (quelques mots).
- Si une cellule dépasse 6 ou 7 mots, utiliser des blocs à libellés au lieu d'un tableau.

## 6. Repères visuels

- **Aucun émoji**, nulle part dans le rapport : ni dans les titres, ni dans les listes, ni dans les schémas.
- Les repères sont des **étiquettes en mots**, toujours les mêmes :
  - gravité, entre crochets : `[CRITIQUE]`, `[HAUTE]`, `[MOYENNE]`, `[BASSE]`, `[À VÉRIFIER]` ;
  - statut, en tête de ligne : `NOUVEAU`, `MODIFIÉ`, `SUPPRIMÉ` ;
  - verdict : `NE PAS FUSIONNER`, `À CORRIGER AVANT DE FUSIONNER`, `PEUT ÊTRE FUSIONNÉE`.
- L'étiquette est toujours **au même endroit** dans le bloc, pour que l'œil la trouve sans lire.

## 7. Longueur

- Le verdict et ses chiffres tiennent dans le premier écran.
- Les « suggestions » sont limitées à 3. Le reste n'est pas dit.
- Ne pas répéter dans une partie ce qui est déjà dans une autre : renvoyer au numéro du bloc (« voir faille 1 »).

## Sources

- [British Dyslexia Association — Dyslexia Style Guide](https://www.bdadyslexia.org.uk/advice/employers/creating-a-dyslexia-friendly-workplace/dyslexia-friendly-style-guide)
