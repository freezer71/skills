---
name: resume-travail
description: Résumé complet, en mots simples, de tout ce que l'agent vient de faire dans la session, lancé par la commande `/resume-travail [période ou sujet, facultatif]`. Produit un compte rendu en français, découpé en blocs courts et faciles à parcourir : ce qui a été fait, les fichiers créés, modifiés ou supprimés, les actions qui ont un effet hors des fichiers (commit, push, publication, installation, message envoyé), ce qui a été vérifié et ce qui ne l'a pas été, les points d'attention, et ce qui reste à faire ou à décider. Fidèle aux faits : rien d'inventé, rien d'enjolivé, les échecs dits clairement. Indépendant du langage, du projet et du type de tâche.
argument-hint: "[période ou sujet, facultatif]"
disable-model-invocation: true
---

# Skill Résumé du travail — Tout ce qui a été fait, en mots simples

Ce skill est une **commande** : il ne se déclenche que quand l'utilisateur tape `/resume-travail`. Il produit un compte rendu de **tout** ce que l'agent a fait dans la session, pour que l'utilisateur comprenne en deux minutes où en est son travail, sans connaître le détail technique.

Le compte rendu répond à cinq questions, dans cet ordre :

1. **Qu'est-ce qui a été fait ?** En langage simple, par objectif.
2. **Qu'est-ce qui a changé ?** Les fichiers, et surtout les actions qui ont un effet ailleurs (dépôt distant, service en ligne, système).
3. **Est-ce que ça marche ?** Ce qui a été vérifié, avec le résultat, et ce qui ne l'a pas été.
4. **À quoi faire attention ?** Problèmes rencontrés, choix faits à la place de l'utilisateur, limites.
5. **Et maintenant ?** Ce qui reste à faire, et les décisions qui attendent l'utilisateur.

Argument reçu : `$ARGUMENTS`

## Quand utiliser ce skill

Uniquement sur appel explicite de la commande `/resume-travail`. Cas couverts :
- `/resume-travail` sans argument : toute la session, depuis le début de la conversation.
- `/resume-travail` suivi d'une période ou d'un sujet (« depuis le dernier commit », « la partie sécurité », « aujourd'hui ») : seulement cette partie, en le disant en tête du compte rendu.

Le skill s'applique à tout type de travail : code, documents, configuration, recherche, administration d'un système.

## Principes directeurs de réponse

1. **Fidèle aux faits, d'abord.** Ne résumer que ce qui s'est réellement passé, d'après la conversation et l'état réel des fichiers. Ne jamais présenter comme fait ce qui a seulement été prévu, proposé ou commencé. Voir `references/collecter-les-faits.md`.
2. **Dire les échecs aussi clairement que les réussites.** Une commande qui a échoué, un test rouge, une étape sautée, une action refusée par l'utilisateur : tout figure dans le compte rendu, sans l'atténuer.
3. **Distinguer fait, vérifié et supposé.** « Fait » : l'action a eu lieu. « Vérifié » : un contrôle a confirmé le résultat. Un changement fait mais non vérifié est dit comme tel.
4. **Mots simples.** Le compte rendu se comprend sans connaître la technique. Chaque terme technique nécessaire est expliqué en quelques mots la première fois. Voir `references/mots-simples.md`.
5. **Lisible d'un coup d'œil.** L'utilisateur est dyslexique. Toujours les mêmes parties dans le même ordre, un bloc par élément, une idée par ligne, des phrases courtes, pas d'italique, **aucun émoji**. Voir `references/lisibilite.md`.
6. **Par objectif, pas par ordre chronologique.** On regroupe ce qui sert le même but, même si c'était fait en plusieurs fois. Les allers-retours (une erreur corrigée deux messages plus tard) ne comptent que par leur résultat final, sauf s'ils ont laissé une trace.
7. **Mettre en avant ce qui est irréversible ou visible par d'autres.** Envoi sur un dépôt distant, publication, suppression, message envoyé, paiement, changement sur un système partagé : ces actions ont leur propre partie et ne se perdent jamais dans la liste.
8. **Ne rien faire d'autre.** Le skill résume ; il ne corrige rien, ne commite rien, ne relance rien. S'il remarque un problème, il le signale dans les points d'attention.

## Architecture du skill — où chercher quoi

| Étape | Fichier de référence |
|---|---|
| Retrouver ce qui a été fait : conversation, état des fichiers, historique | `references/collecter-les-faits.md` |
| Écrire en mots simples : remplacer le jargon, expliquer un terme, parler du résultat | `references/mots-simples.md` |
| Mettre en forme pour une lecture rapide | `references/lisibilite.md` |

## Templates/checklists prêts à l'emploi

| Besoin | Modèle |
|---|---|
| Structure du compte rendu | `assets/modele-resume.md` |
| Relecture finale avant de livrer | `assets/checklist-relecture.md` |

## Workflow standard

1. **Délimite la période** à partir de `$ARGUMENTS` : toute la session par défaut.
2. **Rassemble les faits** avec `references/collecter-les-faits.md` : relis la conversation, puis compare avec l'état réel (fichiers, historique de versions, système).
3. **Classe chaque fait** : fait et vérifié, fait non vérifié, échoué, abandonné, refusé, seulement proposé.
4. **Regroupe par objectif** : 1 objectif = ce que l'utilisateur a demandé, ou une étape nécessaire pour y arriver.
5. **Rédige** selon `assets/modele-resume.md`, en mots simples (voir `references/mots-simples.md`).
6. **Relis** avec `assets/checklist-relecture.md` : chaque phrase est-elle vraie, simple et courte ? Retire tout émoji.
7. **Livre** le compte rendu, sans proposer d'autre action que celles déjà listées dans « Et maintenant ».

## Mises en garde transverses

- **Ne jamais compléter par supposition.** Si un résultat n'est pas connu (une commande lancée dont la sortie n'a pas été lue, un test non relancé après un changement), écrire « non vérifié », pas « fonctionne ».
- **Une modification de l'utilisateur ou d'un outil n'est pas une action de l'agent.** Si des fichiers ont changé sans que l'agent les touche, les signaler à part, sans se les attribuer.
- **Une conversation résumée en partie** (contexte compacté) peut avoir perdu des détails : le dire, et s'appuyer d'autant plus sur l'état réel des fichiers et de l'historique.
- **Pas de secret dans le compte rendu.** Mot de passe, clé, jeton : mentionner qu'un secret a été manipulé, jamais sa valeur.
- **Le compte rendu n'est pas une publicité.** Pas d'adjectifs flatteurs (« robuste », « complet », « propre ») : les faits suffisent.

## Sources officielles à privilégier

- British Dyslexia Association, Dyslexia Style Guide : [bdadyslexia.org.uk](https://www.bdadyslexia.org.uk/advice/employers/creating-a-dyslexia-friendly-workplace/dyslexia-friendly-style-guide)
- Gouvernement du Canada, Guide de rédaction en langage clair : [canada.ca](https://www.canada.ca/fr/services-publics-approvisionnement/services/langage-clair.html)
- Plain Language Association International : [plainlanguagenetwork.org](https://plainlanguagenetwork.org)
