# Collecter les faits

Un bon résumé ne se fait pas de mémoire. Il croise deux sources : **ce que dit la conversation** et **ce que montre l'état réel**. Quand elles ne disent pas la même chose, c'est l'état réel qui gagne, et l'écart est signalé.

## 1. Relire la conversation

Parcours la conversation du début de la période jusqu'à maintenant et note :

- **Les demandes de l'utilisateur**, dans ses mots. Ce sont les objectifs du résumé.
- **Chaque action de l'agent qui a eu un effet** : fichier créé, modifié, supprimé ou déplacé ; commande qui change quelque chose ; envoi, publication, installation.
- **Le résultat de chaque action** : réussie, échouée, refusée par l'utilisateur, interrompue.
- **Les vérifications** : test lancé, contrôle fait, avec leur résultat exact.
- **Les décisions** : prises par l'utilisateur, ou prises par l'agent à sa place (nom choisi, option par défaut, approche retenue).
- **Les questions restées sans réponse** et les propositions faites mais pas acceptées.

Ignore ce qui n'a eu aucun effet : lectures, recherches, tentatives annulées sans trace. Elles ne comptent que si elles ont appris quelque chose d'utile à l'utilisateur.

## 2. Comparer avec l'état réel

Selon le type de travail, vérifie ce qui est vérifiable sans rien modifier :

- **Fichiers** : liste les fichiers créés, modifiés et supprimés pendant la période. Si le dossier est suivi par un outil de gestion de versions, utilise-le pour obtenir l'état exact (fichiers modifiés, non enregistrés, enregistrés, envoyés ou non sur le dépôt distant).
- **Historique** : les enregistrements faits pendant la période, et s'ils ont été envoyés.
- **Fichiers hors du dossier de travail** : configuration de l'utilisateur, dossiers globaux, liens créés. Ils sont souvent oubliés dans un résumé.
- **Services externes** : ce qui a été publié ou envoyé (dépôt en ligne, page, message). Rappelle l'adresse quand il y en a une.

Ces contrôles sont en **lecture seule**. Le skill ne corrige rien, n'enregistre rien et ne relance rien.

## 3. Classer chaque fait

| Statut | Sens |
|---|---|
| FAIT ET VÉRIFIÉ | L'action a eu lieu et un contrôle a confirmé le résultat. |
| FAIT, NON VÉRIFIÉ | L'action a eu lieu, aucun contrôle ne le confirme. |
| ÉCHOUÉ | L'action a été tentée et n'a pas marché. |
| ABANDONNÉ | Commencé puis arrêté, volontairement ou non. |
| REFUSÉ | L'utilisateur a refusé l'action. |
| PROPOSÉ | Suggéré, pas fait. Va dans « Et maintenant ». |

Un fait vérifié **avant** un changement ultérieur redevient « non vérifié » si le changement l'a touché.

## 4. Repérer ce qui compte le plus

Classe à part, pour la partie « Actions visibles hors des fichiers » :
- tout ce qui a été **envoyé ou publié** (visible par d'autres) ;
- tout ce qui est **difficile à annuler** : suppression, écrasement, envoi d'un message, modification d'un système partagé ;
- tout ce qui a un **coût** : service payant, ressource consommée.

## 5. Signaler les écarts

- La conversation dit qu'un fichier a été créé, mais il n'existe pas : le signaler.
- Un fichier a changé sans action de l'agent : le signaler comme « modifié hors de la session », sans se l'attribuer.
- Une partie de la conversation a été compactée : le dire en tête, une ligne.

## Sources

- [Gouvernement du Canada — Langage clair](https://www.canada.ca/fr/services-publics-approvisionnement/services/langage-clair.html)
