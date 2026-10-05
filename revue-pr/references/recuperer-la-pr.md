# Récupérer la PR et tout son contexte

Une revue juste commence par le bon périmètre : **tous les commits de la PR**, comparés à la branche dans laquelle elle sera fusionnée, et les fichiers **dans leur version de la PR**, pas dans celle de ta copie locale.

## 1. Identifier la PR

| Argument reçu | Commande |
|---|---|
| Un numéro (`42`) | `gh pr view 42` |
| Une URL (`https://github.com/org/depot/pull/42`) | `gh pr view <URL>` — fonctionne même si le dossier courant est un autre dépôt |
| Rien | `gh pr view` (PR de la branche courante) |
| Rien, et pas de PR pour la branche | Mode local, voir la section 5 |

Si `gh` répond qu'il n'est pas authentifié, demande à l'utilisateur de lancer `! gh auth login` et arrête-toi là.

## 2. Métadonnées

```bash
gh pr view <PR> --json number,title,body,author,state,isDraft,baseRefName,headRefName,headRefOid,url,additions,deletions,changedFiles,commits,files,labels
```

À retenir pour le rapport : titre, auteur, branche de base et branche source, nombre de fichiers et de lignes, état (brouillon, ouverte, fusionnée). Lis la description : elle dit ce que l'auteur **pense** avoir fait, que tu compareras au code.

## 3. Le diff complet

```bash
gh pr diff <PR>                 # diff unifié de toute la PR
gh pr diff <PR> --name-only     # liste des fichiers
```

`gh pr diff` compare la tête de la PR à la base de fusion : c'est le bon périmètre, tous commits confondus. Pour un diff très long, enregistre-le dans un fichier temporaire du dossier de travail de la session (le scratchpad) et lis-le par morceaux plutôt que de le tronquer.

## 4. Lire les fichiers dans leur version de la PR

Le diff ne montre que quelques lignes de contexte. Pour juger une route ou une requête, il faut le fichier entier, et souvent ses voisins (middleware, layout, schéma de validation).

- **Si la branche de la PR est déjà la branche courante** et à jour (`git rev-parse HEAD` égal à `headRefOid`), lis directement les fichiers.
- **Sinon, sans toucher à la copie de travail de l'utilisateur** :

```bash
git fetch origin pull/<numéro>/head:revue-pr-<numéro>
git show revue-pr-<numéro>:chemin/du/fichier
git grep -n "motif" revue-pr-<numéro>
```

  `git show` et `git grep` lisent la version de la PR sans changer de branche. Ne fais pas de `git checkout` ni de `gh pr checkout` sans l'accord de l'utilisateur : il peut avoir du travail en cours. Supprime la branche temporaire à la fin (`git branch -D revue-pr-<numéro>`).
- **Si le dossier courant n'est pas le dépôt de la PR**, utilise l'API : `gh api repos/<org>/<depot>/contents/<chemin>?ref=<headRefOid> --jq .content | base64 -d`.

## 5. Mode local, sans PR

Quand il n'y a pas de PR, revois la branche courante par rapport à la branche principale :

```bash
git remote show origin | sed -n 's/.*HEAD branch: //p'   # nom de la branche principale
git diff <base>...HEAD                                   # trois points : depuis le point de divergence
git log --oneline <base>..HEAD
```

Signale aussi les modifications non commitées (`git status --short`) : elles ne sont pas dans le diff, et le rapport doit dire qu'elles n'ont pas été revues. Indique clairement en tête de rapport qu'il s'agit d'une revue locale.

## 6. Contexte utile en plus

- **Langages, frameworks et versions** : lus dans le fichier de dépendances du projet, à la version de la PR.
- **Conventions du dépôt** : `CLAUDE.md`, `AGENTS.md`, `CONTRIBUTING.md`, s'ils existent ; une règle documentée du dépôt non respectée est un constat de revue.
- **État des vérifications automatiques** : `gh pr checks <PR>`. Un test rouge est à mentionner dans le rapport.

## Sources

- [GitHub CLI — `gh pr view`](https://cli.github.com/manual/gh_pr_view)
- [GitHub CLI — `gh pr diff`](https://cli.github.com/manual/gh_pr_diff)
- [GitHub Docs — Checking out pull requests locally](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/checking-out-pull-requests-locally)
