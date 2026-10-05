# Écrire en mots simples

Le compte rendu doit être compris par quelqu'un qui n'a pas suivi le détail technique. Simple ne veut pas dire flou : on garde la précision, on retire l'effort de lecture.

## 1. Parler du résultat, pas de la mécanique

Dis d'abord ce que ça change pour l'utilisateur, ensuite comment.

- Plutôt que : « Ajout d'un contrôle sur le paramètre d'entrée de la fonction d'export. »
- Écrire : « L'export refuse maintenant les demandes incomplètes. »

## 2. Remplacer le jargon

Remplace un terme technique par des mots courants quand c'est possible sans perdre le sens.

| Au lieu de | Écrire |
|---|---|
| commit | enregistrement dans l'historique |
| push | envoi sur le dépôt en ligne |
| refactoriser | réorganiser le code sans changer ce qu'il fait |
| déprécié | ancien, à ne plus utiliser |
| régression | quelque chose qui marchait et ne marche plus |
| dépendance | outil externe utilisé par le projet |

Quand le terme technique est utile (l'utilisateur le reverra ailleurs), garde-le et explique-le une seule fois, entre parenthèses : « un commit (un enregistrement dans l'historique) ». Ensuite, utilise toujours le même mot.

## 3. Une phrase, une idée

- Sujet, verbe, complément.
- 15 mots environ, 20 au plus.
- Voix active : « J'ai supprimé le dossier. » plutôt que « Le dossier a été supprimé. » Le lecteur sait qui a fait quoi.
- Pas de double négation, pas de parenthèse dans une parenthèse.

## 4. Des mots précis

- Des nombres plutôt que des adjectifs : « 3 fichiers », pas « plusieurs fichiers ».
- Des noms exacts : le nom du fichier, de la commande ou du service, en `code`.
- Des verbes qui disent l'état réel : « créé », « modifié », « supprimé », « envoyé », « testé », « non testé ».
- Pas d'adjectifs de qualité (« robuste », « propre », « complet ») : ce sont des opinions, pas des faits.

## 5. Dire les mauvaises nouvelles simplement

- Directement, en début de bloc : « Le test a échoué. »
- Avec la conséquence : « Le changement n'est donc pas confirmé. »
- Sans excuse ni dramatisation.

## Sources

- [Gouvernement du Canada — Guide de rédaction en langage clair](https://www.canada.ca/fr/services-publics-approvisionnement/services/langage-clair.html)
- [Plain Language Association International](https://plainlanguagenetwork.org)
