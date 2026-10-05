# Établir les résultats

Un bon résumé ne se fait pas de mémoire. Il part des **demandes de l'utilisateur** et cherche, pour chacune, **l'état réel d'arrivée** et **la preuve** de cet état. Quand la conversation et l'état réel ne disent pas la même chose, c'est l'état réel qui gagne, et l'écart est signalé.

## 1. Partir des demandes

Parcours la conversation du début de la période jusqu'à maintenant et note :

- **Les demandes de l'utilisateur**, dans ses mots. Chacune devient un objectif.
- **Les étapes nécessaires** que l'utilisateur n'a pas demandées mais qui conditionnent le résultat (installer un outil, réparer ce qui bloquait). Elles ne deviennent un objectif que si elles ont un effet durable pour l'utilisateur.
- **Les décisions** : prises par l'utilisateur, ou prises par l'agent à sa place (nom choisi, option par défaut, approche retenue).
- **Les questions restées sans réponse** et les propositions faites mais pas acceptées.

Ne note pas le chemin : lectures, recherches, essais, erreurs corrigées en route. Ils ne comptent que s'ils ont laissé une trace dans le résultat, ou appris quelque chose d'utile à l'utilisateur.

## 2. Établir l'état d'arrivée

Pour chaque objectif, réponds à une seule question : **qu'est-ce qui est vrai maintenant, qui ne l'était pas avant ?**

- Une fonction marche, un document existe, une page est en ligne, une erreur ne se produit plus.
- Dis-le du point de vue de l'utilisateur : ce qu'il peut faire, voir ou utiliser.

Vérifie ce qui est vérifiable sans rien modifier :

- **Fichiers** : le résultat est-il bien présent ? Si le dossier est suivi par un outil de gestion de versions, est-il enregistré, envoyé sur le dépôt distant ?
- **Fichiers hors du dossier de travail** : configuration de l'utilisateur, dossiers globaux, liens. Ils font partie du résultat et sont souvent oubliés.
- **Services externes** : ce qui est publié ou envoyé. Relève l'adresse quand il y en a une.

Ces contrôles sont en **lecture seule**. Le skill ne corrige rien, n'enregistre rien et ne relance rien.

## 3. Trouver la preuve et classer

La preuve est un contrôle fait **après le dernier changement** qui touche le résultat : test, commande de vérification, page affichée, fichier relu.

| Statut | Sens |
|---|---|
| ATTEINT | Le résultat demandé existe, et une preuve le confirme. |
| ATTEINT EN PARTIE | Une partie du résultat existe ; le reste manque. |
| NON ATTEINT | Le résultat n'existe pas : échec, abandon ou refus de l'utilisateur. |
| NON VÉRIFIÉ | Le changement est fait, mais aucune preuve ne confirme le résultat. |

Une preuve obtenue **avant** un changement ultérieur ne compte plus si ce changement touche le résultat.

Ce qui a seulement été proposé n'est pas un résultat : il va dans « Et maintenant ».

## 4. Repérer ce qui est sorti du projet

Classe à part, pour la partie « Ce qui est sorti du projet » :
- tout ce qui est maintenant **envoyé ou publié** (visible par d'autres) ;
- tout ce qui est **difficile à annuler** : suppression, écrasement, message envoyé, système partagé modifié ;
- tout ce qui a un **coût** : service payant, ressource consommée.

## 5. Signaler les écarts

- La conversation dit qu'un résultat existe, mais l'état réel ne le montre pas : le signaler dans « Ce qui manque ».
- Un changement est apparu sans action de l'agent : le signaler comme « fait hors de la session », sans se l'attribuer.
- Une partie de la conversation a été compactée : le dire en tête, une ligne.

## Sources

- [Gouvernement du Canada — Langage clair](https://www.canada.ca/fr/services-publics-approvisionnement/services/langage-clair.html)
