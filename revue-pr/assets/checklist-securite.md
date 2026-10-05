# Checklist — Sécurité d'une PR

*Modèle à adapter — ne pas publier brut.*

À dérouler sur chaque PR, en partant de l'inventaire des fonctionnalités. Pour chaque case, la question est : « la PR ajoute, modifie ou supprime-t-elle quelque chose de ce genre ? » Si non, passer. Si oui, vérifier dans le code et noter le résultat dans la liste « Vérifié » du rapport ou en constat. Le détail de chaque point est dans `references/audit-securite.md`.

## Sommaire

1. [Points d'entrée](#1-points-dentrée)
2. [Données reçues](#2-données-reçues)
3. [Données renvoyées et stockées](#3-données-renvoyées-et-stockées)
4. [Secrets et configuration](#4-secrets-et-configuration)
5. [Dépendances et intégration continue](#5-dépendances-et-intégration-continue)
6. [Lignes supprimées](#6-lignes-supprimées)

## 1. Points d'entrée

- [ ] Chaque nouveau point d'entrée vérifie l'authentification **côté serveur**, avec le mécanisme habituel du projet.
- [ ] Chaque accès à une ressource par identifiant vérifie que l'utilisateur y a droit.
- [ ] Les actions réservées à un rôle vérifient le rôle côté serveur.
- [ ] Un filtre global éventuel couvre bien les nouveaux points d'entrée, sans être le seul contrôle.
- [ ] Les appels entrants de services tiers vérifient la signature, et un même événement n'est pas traité deux fois.
- [ ] Les points d'entrée sensibles ou coûteux limitent le nombre d'appels.
- [ ] Les actions qui modifient des données ne sont pas déclenchables par une simple lecture de page.

## 2. Données reçues

- [ ] Toutes les données reçues sont validées côté serveur (type, format, taille).
- [ ] Aucun champ sensible (rôle, propriétaire, organisation, prix) n'est accepté depuis la requête sans liste des champs autorisés.
- [ ] Aucune requête de base de données construite en assemblant du texte avec une donnée externe.
- [ ] Aucune commande système, chemin de fichier, évaluation de code ou désérialisation à partir d'une donnée externe.
- [ ] Aucune adresse fournie par l'utilisateur appelée par le serveur sans liste des destinations autorisées.
- [ ] Les redirections restent internes.
- [ ] Les fichiers envoyés sont vérifiés sur leur contenu, limités en taille, renommés et non exécutables.

## 3. Données renvoyées et stockées

- [ ] Aucun contenu externe affiché sans échappement.
- [ ] Les réponses ne contiennent que les champs nécessaires.
- [ ] Les erreurs renvoyées au client sont génériques ; le détail reste dans les logs.
- [ ] Pas de données personnelles ni de secrets dans les logs ou les outils tiers.
- [ ] Les nouvelles données personnelles ont une utilité claire (sinon, renvoyer au skill `rgpd`).
- [ ] Une réponse propre à un utilisateur n'est pas mise en cache pour les autres.

## 4. Secrets et configuration

- [ ] Aucun secret dans le diff, dans **aucun** commit de la PR.
- [ ] Aucun fichier de secrets ni clé privée ajouté au dépôt.
- [ ] Aucun secret visible côté client.
- [ ] Mots de passe hachés avec un algorithme fait pour cela ; jetons générés avec un aléa cryptographique.
- [ ] Comparaisons de signatures et de jetons en temps constant.
- [ ] Cookies de session avec les protections standard.
- [ ] Partage entre origines, politique de sécurité du contenu et en-têtes de sécurité non affaiblis ; vérification des certificats active ; pas de mode de débogage.

## 5. Dépendances et intégration continue

- [ ] Chaque dépendance ajoutée est connue, maintenue, au nom exact, sans script d'installation suspect.
- [ ] Pas de vulnérabilité connue sur les dépendances ajoutées ou mises à jour.
- [ ] Les changements d'intégration continue n'élargissent pas les droits et n'exposent pas les secrets au code d'une contribution externe.

## 6. Lignes supprimées

- [ ] Aucun contrôle d'accès, validation, limite d'appels, en-tête de sécurité ou test de sécurité retiré sans remplacement.
