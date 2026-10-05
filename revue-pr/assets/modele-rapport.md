# Modèle — Rapport de revue de PR

**Modèle à adapter — ne pas publier brut.**

Règles d'emploi :
- Garder **les 6 parties, dans cet ordre**. Une partie vide tient en une ligne.
- Suivre `references/lisibilite.md` : une idée par ligne, phrases courtes, pas d'italique, **aucun émoji**, mêmes libellés dans le même ordre.
- Faire les schémas avec `references/schemas-donnees.md`.
- Dans la partie 2, ne garder que les natures d'éléments présentes dans la PR.

Le rapport commence après la ligne suivante.

---

# Revue de la PR #[numéro]

**[Titre de la PR]**

- **Auteur :** [nom]
- **Branches :** `[source]` vers `[base]`
- **Taille :** [n] fichiers, +[ajouts] / -[suppressions]

[Si mode local, une ligne : « Revue locale de `[branche]`, sans PR GitHub. »]

---

## 1. Verdict : [NE PAS FUSIONNER | À CORRIGER AVANT DE FUSIONNER | PEUT ÊTRE FUSIONNÉE]

[1 phrase : la raison principale.]

- **Failles critiques :** [n]
- **Failles hautes :** [n]
- **Failles moyennes :** [n]
- **Bugs :** [n]

[Ne garder que les lignes dont le nombre n'est pas 0. Si tout est à 0 : « Aucune faille ni bug trouvé. »]

---

## 2. Ce que la PR ajoute

### En bref

- [Ce qu'un utilisateur peut faire de nouveau, en 1 phrase.]
- [Une autre fonctionnalité, en 1 phrase.]

### Pages et écrans

- `NOUVEAU` **[nom ou chemin]**
  - [Public | Réservé à …]
  - `[fichier]:[ligne]`

### Points d'entrée appelables

- `NOUVEAU` **[nom ou chemin]**
  - [Ce qu'il fait, en quelques mots.]
  - [Qui peut l'appeler.]
  - `[fichier]:[ligne]`

### Données

- `NOUVEAU` **[nom de la structure]** : voir schéma A
- `MODIFIÉ` **[nom de la structure]** : voir schéma B

### Configuration

- `NOUVEAU` **[nom du paramètre]**
  - [Visible côté client : oui | non]

### Dépendances

- `NOUVEAU` **[nom et version]** : [à quoi elle sert]

### Traitements en arrière-plan

- `NOUVEAU` **[nom]** : [quand il tourne, ce qu'il fait]

### Intégrations

- `NOUVEAU` **[service]** : [entrante ou sortante, ce qu'elle fait]

### Droits

- `MODIFIÉ` **[rôle ou permission]** : [ce qui change]

### Écarts avec la description

- [Annoncé mais absent du code, ou présent mais non annoncé.]

---

## 3. Structures de données

### Schéma A — [nom]

```
[boîtes selon references/schemas-donnees.md]
```

- [À quoi sert cette structure.]
- [Point à remarquer, avec renvoi : « Donnée personnelle, voir faille 2. »]

[Si rien de nouveau : « Aucune nouvelle structure de données. »]

---

## 4. Sécurité

[Si aucune faille : « Aucune faille trouvée. » puis directement « Vérifié ».]

### Faille 1 [CRITIQUE] — [Le problème en mots simples]

- **Où :** `[fichier]:[ligne]`
- **Problème :** [Ce qui manque ou ce qui est faux, en 1 phrase.]
- **Risque :** [Ce qu'un attaquant peut faire, en 1 ou 2 phrases.]
- **Correction :** [Le changement à faire, en 1 phrase.]

```
[extrait corrigé, seulement si c'est plus clair que la phrase]
```

### Faille 2 [HAUTE] — [Le problème en mots simples]

- **Où :** …
- **Problème :** …
- **Risque :** …
- **Correction :** …

### Vérifié

- [Point contrôlé, et sa conclusion en 1 ligne.]
- [Autre point.]

---

## 5. Code

### Bug 1 — [Le problème en mots simples]

- **Où :** `[fichier]:[ligne]`
- **Problème :** [Ce qui ne marche pas.]
- **Conséquence :** [Avec quelle entrée, et quel résultat faux.]
- **Correction :** [Le changement à faire.]

### Risque 1 — [Le problème en mots simples]

- **Où :** `[fichier]:[ligne]`
- **Problème :** …
- **Conséquence :** …
- **Correction :** …

### Suggestions (facultatives, 3 au plus)

- [Suggestion en 1 phrase.]

[Si rien : « Aucun bug trouvé. »]

---

## 6. Avant de fusionner

- [ ] [Action bloquante, avec renvoi : « Corriger la faille 1. »]
- [ ] [Action bloquante.]
- [ ] [Secret à révoquer, s'il y en a un.]

[Si rien : « Rien de bloquant. »]

---

Revue faite en lisant le code de la PR. Elle ne remplace ni les tests ni un audit complet de l'application.
