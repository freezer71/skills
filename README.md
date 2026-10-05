# Skills Claude Code

Skills Claude Code d'expertise-métier, rédigés en français. Chaque skill est un dossier autonome que Claude charge automatiquement quand la demande relève de son domaine.

## Skills disponibles

| Skill | Domaine | Déclencheurs typiques |
|---|---|---|
| [`rgpd`](rgpd/SKILL.md) | RGPD, loi Informatique et Libertés, doctrine CNIL et CEPD, articulation avec l'AI Act | données personnelles, base légale, cookies, AIPD, violation de données, politique de confidentialité, DPA |
| [`mentions-legales`](mentions-legales/SKILL.md) | Mentions légales d'un site ou d'une application (LCEN modifiée par la loi SREN, Code de commerce, Code de la consommation) | page `/mentions-legales`, éditeur, hébergeur, directeur de la publication, médiateur de la consommation |
| [`journaliste`](journaliste/SKILL.md) | Déontologie (Charte de Munich, SNJ, CDJM, FIJ), écriture journalistique, méthode d'enquête, droit de la presse | écrire un article, vérifier une information, protéger une source, diffamation, droit de réponse |

`rgpd` et `mentions-legales` fonctionnent ensemble : les mentions légales identifient l'éditeur et renvoient vers la politique de confidentialité et la gestion des cookies, qui relèvent du skill `rgpd`.

## Installation

Claude Code charge comme skills globaux tous les dossiers présents dans `~/.claude/skills/`. Le plus simple est d'y créer un lien symbolique vers chaque skill du dépôt : les modifications faites ici sont prises en compte sans rien copier.

Pour un skill :

```bash
ln -s ~/Workspace/skills/rgpd ~/.claude/skills/rgpd
```

Pour tous les skills du dépôt (les liens déjà présents ne sont pas modifiés) :

```bash
mkdir -p ~/.claude/skills
for d in ~/Workspace/skills/*/; do
  n=$(basename "$d")
  [ -f "$d/SKILL.md" ] && [ ! -e ~/.claude/skills/$n ] && ln -s "${d%/}" ~/.claude/skills/$n
done
```

Relancer ensuite Claude Code : les skills sont lus au démarrage de la session.

## Structure d'un skill

```
nom-du-skill/
├── SKILL.md       # frontmatter (name + description) et mode d'emploi du skill
├── references/    # fiches thématiques, chargées à la demande
└── assets/        # modèles et checklists à adapter
```

- **`SKILL.md`** : le frontmatter contient seulement `name` et `description`. La description est ce qui déclenche le skill : elle énumère largement les sujets et les formulations concernés. Le corps suit toujours les mêmes sections : accroche, « Quand utiliser ce skill », « Principes directeurs de réponse », « Architecture du skill — où chercher quoi » (tableau sujet → `references/x.md`), « Templates/checklists prêts à l'emploi » (tableau → `assets/x.md`), « Workflow standard », « Mises en garde transverses », « Sources officielles à privilégier ».
- **`references/`** : une fiche par sujet, pédagogique (on explique le pourquoi), terminée par une section `## Sources` avec des liens officiels.
- **`assets/`** : des modèles prêts à adapter, qui commencent par « *Modèle à adapter — ne pas publier brut* ».

## Conventions de rédaction

- Français uniquement, avec tous les accents et signes diacritiques.
- Les renvois entre fichiers se font par chemin en backticks, toujours préfixé du dossier : voir `references/bases-legales.md` (le mot « voir » reste hors des backticks).
- Exactitude juridique stricte : citer les articles de loi, rester prudent sur les points discutés et renvoyer vers un professionnel pour les cas réels.

## Ajouter un skill

1. Créer un dossier en slug bas de casse (`mon-skill/`), en partant de `rgpd/` comme gabarit.
2. Écrire la `description` du frontmatter avec soin : c'est d'elle que dépend le déclenchement du skill.
3. Rédiger les fiches `references/` et les modèles `assets/`, puis les référencer dans les tableaux de `SKILL.md`.
4. Créer le lien symbolique dans `~/.claude/skills/` (voir [Installation](#installation)) et ajouter une ligne au tableau [Skills disponibles](#skills-disponibles).
