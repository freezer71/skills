# Revue de code hors sécurité

La revue de code vient après l'audit de sécurité et reste courte : elle signale ce qui **ne marchera pas** ou **cassera quelque chose**, puis quelques suggestions utiles. Ce n'est pas une relecture de style : les outils de formatage du projet s'en chargent.

## Ce qui compte, par ordre d'importance

### 1. Exactitude : le code fait-il ce qu'il annonce ?

- Logique conditionnelle inversée, cas oublié (`else` manquant, valeur `null` ou `undefined`, tableau vide, zéro).
- Asynchrone : `await` oublié, promesse non gérée, `forEach` avec une fonction `async` (n'attend rien), conditions de concurrence (deux requêtes qui lisent puis écrivent la même ligne sans transaction).
- Erreurs avalées : `catch {}` vide, erreur journalisée puis ignorée alors que l'appelant croit à un succès.
- Dates et fuseaux horaires, arrondis monétaires (calculs en flottants sur des montants), encodage.
- Données : migration incompatible avec le code déployé en même temps (colonne supprimée encore lue par l'ancienne version pendant le déploiement), contrainte d'unicité manquante qu'une règle métier suppose.

### 2. Régressions : la PR casse-t-elle l'existant ?

- Signature de fonction, type exporté, format de réponse d'API ou nom de route changés : cherche les appelants (`git grep` sur la version de la PR) et vérifie qu'ils sont tous mis à jour.
- Comportement supprimé sans remplacement.
- Changement de valeur par défaut.

### 3. Tests

- La fonctionnalité nouvelle est-elle testée ? Les cas d'erreur et les cas limites aussi ?
- Un test modifié pour passer au lieu du code corrigé (assertion affaiblie, test sauté avec `.skip`, délai augmenté, attente changée de `networkidle` en `load`) est un constat : le symptôme est caché, pas expliqué.
- État des vérifications de la PR (`gh pr checks`).

### 4. Performances et coûts

Requêtes en boucle (N+1), chargement de tables entières, absence de pagination, appels réseau dans un rendu, gros calcul dans un chemin chaud. Préchargements ou requêtes qui se répètent sans fin côté client : à mesurer, pas à supposer.

### 5. Lisibilité et conventions (suggestions seulement)

Code dupliqué qui existe déjà ailleurs dans le dépôt, nommage trompeur, fonction trop longue, commentaire faux. Règles écrites du dépôt (`CLAUDE.md`, `CONTRIBUTING.md`) non suivies. Limite-toi aux 3 remarques les plus utiles.

## Classer les constats

Chaque bug ou risque est un bloc avec les libellés Où, Problème, Conséquence, Correction (voir `assets/modele-rapport.md`, partie 4). Les suggestions tiennent en 1 phrase chacune, 3 au plus.

| Niveau | Sens |
|---|---|
| **Bug** | Comportement faux démontrable : donner l'entrée qui le déclenche et le résultat obtenu. Bloque la fusion. |
| **Risque** | Peut casser selon les données ou le contexte (concurrence, migration, régression probable). À corriger ou à justifier. |
| **Suggestion** | Amélioration facultative. Ne bloque jamais. |

## Sources

- [Google Engineering Practices — What to look for in a code review](https://google.github.io/eng-practices/review/reviewer/looking-for.html)
- [Google Engineering Practices — The Standard of Code Review](https://google.github.io/eng-practices/review/reviewer/standard.html)
