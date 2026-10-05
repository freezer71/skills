# Skills Claude Code

Skills Claude Code d'expertise-métier, rédigés en français. Chaque skill est un dossier autonome que Claude charge automatiquement quand la demande relève de son domaine.

## Skills disponibles

| Skill | Domaine | Déclencheurs typiques |
|---|---|---|
| [`rgpd`](rgpd/SKILL.md) | RGPD, loi Informatique et Libertés, doctrine CNIL et CEPD, articulation avec l'AI Act | données personnelles, base légale, cookies, AIPD, violation de données, politique de confidentialité, DPA |
| [`mentions-legales`](mentions-legales/SKILL.md) | Mentions légales d'un site ou d'une application (LCEN modifiée par la loi SREN, Code de commerce, Code de la consommation) | page `/mentions-legales`, éditeur, hébergeur, directeur de la publication, médiateur de la consommation |
| [`journaliste`](journaliste/SKILL.md) | Déontologie (Charte de Munich, SNJ, CDJM, FIJ), écriture journalistique, méthode d'enquête, droit de la presse | écrire un article, vérifier une information, protéger une source, diffamation, droit de réponse |
| [`revue-pr`](revue-pr/SKILL.md) | Revue de code d'une pull request GitHub : inventaire des nouvelles fonctionnalités par nature (points d'entrée, données, dépendances, droits), schémas des nouvelles structures de données, audit de sécurité de toute la PR, revue de code ; indépendant du langage et du framework, rapport découpé en blocs courts | commande `/revue-pr [numéro ou URL]` uniquement, pas de déclenchement automatique |
| [`resume-travail`](resume-travail/SKILL.md) | Compte rendu, en mots simples, de tout ce que l'agent a fait dans la session : objectifs, fichiers, actions visibles hors des fichiers, vérifications, points d'attention, suite ; même mise en forme que `revue-pr` | commande `/resume-travail [période ou sujet]` uniquement |

`rgpd` et `mentions-legales` fonctionnent ensemble : les mentions légales identifient l'éditeur et renvoient vers la politique de confidentialité et la gestion des cookies, qui relèvent du skill `rgpd`.

## Structure d'un skill

```
nom-du-skill/
├── SKILL.md       # frontmatter (name + description) et mode d'emploi du skill
├── references/    # fiches thématiques, chargées à la demande
└── assets/        # modèles et checklists à adapter
```

- **`SKILL.md`** : le frontmatter contient `name` et `description` (plus deux champs pour les commandes, voir ci-dessous). La description est ce qui déclenche le skill : elle énumère largement les sujets et les formulations concernés. Le corps suit toujours les mêmes sections : accroche, « Quand utiliser ce skill », « Principes directeurs de réponse », « Architecture du skill — où chercher quoi » (tableau sujet → `references/x.md`), « Templates/checklists prêts à l'emploi » (tableau → `assets/x.md`), « Workflow standard », « Mises en garde transverses », « Sources officielles à privilégier ».
- **Commandes** : un skill qui ne doit se lancer que sur demande (comme `revue-pr` ou `resume-travail`) ajoute au frontmatter `disable-model-invocation: true` et, s'il prend un argument, `argument-hint`. Il s'appelle alors avec `/nom-du-skill`.
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
4. Ajouter une ligne au tableau [Skills disponibles](#skills-disponibles).
