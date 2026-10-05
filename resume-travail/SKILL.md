---
name: resume-travail
description: Résumé des résultats du travail de la session, en mots simples, lancé par la commande `/resume-travail [période ou sujet, facultatif]`. Ne raconte pas ce que l'agent a fait : dit ce qui existe ou fonctionne maintenant, par objectif, avec la preuve que c'est vrai. Produit un compte rendu en français, découpé en blocs courts et faciles à parcourir : les résultats obtenus, ce qui n'est pas atteint ou pas confirmé, ce qui est désormais visible par d'autres ou difficile à annuler, où trouver le résultat, et ce qui reste à faire ou à décider. Fidèle aux faits : rien d'inventé, rien d'enjolivé, les échecs dits clairement. Indépendant du langage, du projet et du type de tâche.
argument-hint: "[période ou sujet, facultatif]"
disable-model-invocation: true
---

# Skill Résumé du travail — Les résultats, en mots simples

Ce skill est une **commande** : il ne se déclenche que quand l'utilisateur tape `/resume-travail`. Il produit un compte rendu des **résultats** de la session : ce que l'utilisateur a maintenant, qu'il n'avait pas avant.

Ce n'est **pas** le récit du travail. Les étapes, les commandes lancées, les fichiers lus, les allers-retours n'y figurent pas. Seul compte l'état d'arrivée.

- Récit du travail, à éviter : « J'ai créé `export.ts`, ajouté un contrôle, puis lancé les tests. »
- Résultat, à écrire : « L'export refuse maintenant les demandes incomplètes. Les 12 tests passent. »

Le compte rendu répond à cinq questions, dans cet ordre :

1. **Qu'est-ce qu'on a maintenant ?** Le résultat de chaque demande, en langage simple.
2. **Est-ce que c'est sûr ?** La preuve de chaque résultat, ou « non vérifié ».
3. **Qu'est-ce qui manque ?** Ce qui n'est pas atteint, atteint en partie, ou cassé.
4. **Qu'est-ce qui est sorti du projet ?** Ce qui est maintenant visible par d'autres ou difficile à annuler.
5. **Et maintenant ?** Ce qui reste à faire, et les décisions qui attendent l'utilisateur.

Argument reçu : `$ARGUMENTS`

## Quand utiliser ce skill

Uniquement sur appel explicite de la commande `/resume-travail`. Cas couverts :
- `/resume-travail` sans argument : toute la session, depuis le début de la conversation.
- `/resume-travail` suivi d'une période ou d'un sujet (« depuis le dernier commit », « la partie sécurité », « aujourd'hui ») : seulement cette partie, en le disant en tête du compte rendu.

Le skill s'applique à tout type de travail : code, documents, configuration, recherche, administration d'un système.

## Principes directeurs de réponse

1. **Le résultat, pas le chemin.** Pour chaque demande, dire l'état d'arrivée : ce qui existe, ce qui marche, ce qui a changé pour l'utilisateur. Ne pas décrire les étapes. Un fichier ou une commande n'est cité que comme endroit où trouver le résultat, ou comme preuve.
2. **Fidèle aux faits.** Ne résumer que ce qui est réellement obtenu, d'après la conversation et l'état réel. Ne jamais présenter comme obtenu ce qui a seulement été prévu, proposé ou commencé. Voir `references/collecter-les-faits.md`.
3. **Chaque résultat a sa preuve.** Un test, un contrôle, une page vue, un fichier présent. Sans preuve, le résultat est dit « non vérifié ».
4. **Dire ce qui manque aussi clairement que ce qui est obtenu.** Objectif non atteint, atteint en partie, cassé en route, refusé par l'utilisateur : tout figure, sans l'atténuer.
5. **Mots simples.** Le compte rendu se comprend sans connaître la technique. Chaque terme technique nécessaire est expliqué en quelques mots la première fois. Voir `references/mots-simples.md`.
6. **Lisible d'un coup d'œil.** L'utilisateur est dyslexique. Toujours les mêmes parties dans le même ordre, un bloc par résultat, une idée par ligne, des phrases courtes, pas d'italique, **aucun émoji**. Voir `references/lisibilite.md`.
7. **Mettre en avant ce qui est sorti du projet.** Envoi sur un dépôt distant, publication, suppression, message envoyé, paiement, changement sur un système partagé : ces résultats ont leur propre partie et ne se perdent jamais dans la liste.
8. **Ne rien faire d'autre.** Le skill résume ; il ne corrige rien, ne commite rien, ne relance rien. S'il remarque un problème, il le signale dans « Ce qui manque ».

## Architecture du skill — où chercher quoi

| Étape | Fichier de référence |
|---|---|
| Établir les résultats : demandes, état réel, preuves | `references/collecter-les-faits.md` |
| Écrire en mots simples : dire le résultat, remplacer le jargon | `references/mots-simples.md` |
| Mettre en forme pour une lecture rapide | `references/lisibilite.md` |

## Templates/checklists prêts à l'emploi

| Besoin | Modèle |
|---|---|
| Structure du compte rendu | `assets/modele-resume.md` |
| Relecture finale avant de livrer | `assets/checklist-relecture.md` |

## Workflow standard

1. **Délimite la période** à partir de `$ARGUMENTS` : toute la session par défaut.
2. **Liste les demandes** de l'utilisateur dans la période : chacune est un objectif.
3. **Établis le résultat de chaque objectif** avec `references/collecter-les-faits.md` : quel est l'état réel maintenant, et quelle preuve le montre.
4. **Classe chaque résultat** : ATTEINT, ATTEINT EN PARTIE, NON ATTEINT, NON VÉRIFIÉ.
5. **Rédige** selon `assets/modele-resume.md`, en mots simples (voir `references/mots-simples.md`).
6. **Relis** avec `assets/checklist-relecture.md` : chaque ligne dit-elle un résultat, et non une action ? Retire tout émoji.
7. **Livre** le compte rendu, sans proposer d'autre action que celles déjà listées dans « Et maintenant ».

## Mises en garde transverses

- **Ne jamais compléter par supposition.** Si un résultat n'est pas connu (une commande lancée dont la sortie n'a pas été lue, un test non relancé après un changement), écrire « non vérifié », pas « fonctionne ».
- **Un résultat obtenu par l'utilisateur ou un outil n'est pas un résultat de l'agent.** Le signaler à part, sans se l'attribuer.
- **Une conversation résumée en partie** (contexte compacté) peut avoir perdu des détails : le dire, et s'appuyer d'autant plus sur l'état réel.
- **Pas de secret dans le compte rendu.** Mot de passe, clé, jeton : mentionner qu'un secret est en place, jamais sa valeur.
- **Le compte rendu n'est pas une publicité.** Pas d'adjectifs flatteurs (« robuste », « complet », « propre ») : les faits suffisent.

## Sources officielles à privilégier

- British Dyslexia Association, Dyslexia Style Guide : [bdadyslexia.org.uk](https://www.bdadyslexia.org.uk/advice/employers/creating-a-dyslexia-friendly-workplace/dyslexia-friendly-style-guide)
- Gouvernement du Canada, Guide de rédaction en langage clair : [canada.ca](https://www.canada.ca/fr/services-publics-approvisionnement/services/langage-clair.html)
- Plain Language Association International : [plainlanguagenetwork.org](https://plainlanguagenetwork.org)
