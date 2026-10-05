# Inventaire des nouvelles fonctionnalités

L'inventaire répond à la question « qu'est-ce que cette PR ajoute ? » à deux niveaux : **fonctionnel** (ce qu'un utilisateur pourra faire de nouveau) et **par nature** (quels nouveaux éléments entrent dans le système). Le second niveau sert aussi de carte pour l'audit de sécurité : chaque nouveau point d'entrée ou nouvelle donnée est une surface à examiner.

## Principe : raisonner par nature, pas par technologie

Les mêmes choses existent dans tous les projets, sous des formes différentes. Une route peut être un fichier dans un dossier, une ligne dans un fichier de routes ou une annotation sur une fonction. Une table peut être un script de migration, une classe ou un fichier de schéma.

Méthode :
1. **Apprends la convention du projet.** Pour chaque nature ci-dessous, trouve un exemple existant dans le dépôt et note comment il est déclaré.
2. **Cherche dans le diff les éléments qui suivent la même convention.**
3. **Cherche aussi ce qui sort de la convention** : un point d'entrée déclaré autrement que les autres échappe souvent aux contrôles communs.

Pour chaque élément, note : sa **nature**, son **nom** (chemin, nom de table, nom de type…), le **fichier** et la ligne, et son **statut** : nouveau, modifié ou supprimé. Un élément modifié dont on change le comportement ou les droits compte autant qu'un nouveau.

## Les natures à repérer

### 1. Pages et écrans

Ce qu'un utilisateur peut ouvrir ou afficher : page web, écran d'application, vue.

Pour chacun : public ou réservé, et à qui.

### 2. Points d'entrée appelables

Tout ce qu'on peut appeler de l'extérieur : endpoint d'API, fonction serveur appelable depuis le client, requête ou mutation d'une API, commande en ligne, message écouté sur une file.

Pour chacun : ce qu'il fait, qui peut l'appeler, quelles données il reçoit.

Attention aux points d'entrée **implicites** : certaines technologies rendent une fonction appelable de l'extérieur sans le dire clairement. Dans le doute, considère qu'une fonction côté serveur appelée depuis le client est un point d'entrée public.

### 3. Données stockées

Ce que le système garde : tables, collections, fichiers, clés de cache, stockage local.

À noter à part, les **évolutions du stockage** risquées :
- suppression ou renommage d'un champ ;
- changement de type ;
- champ rendu obligatoire alors que des données existent déjà ;
- règles d'accès au stockage ajoutées, modifiées ou retirées.

### 4. Données échangées

Ce qui circule entre deux parties : types et structures exportés, formats de requête et de réponse, schémas de validation, contrats d'API, formats de messages, listes de valeurs possibles (états, catégories).

Retiens celles qui décrivent une donnée métier, pas les structures purement techniques internes.

Note les champs qui portent des **données personnelles ou sensibles** : identité, contact, adresse, santé, paiement. Ils comptent pour l'audit et pour le RGPD (skill `rgpd`).

### 5. Configuration

Nouveaux paramètres, variables d'environnement, options, drapeaux de fonctionnalité.

Pour chaque paramètre : à quoi il sert, et s'il finit **visible côté client** (envoyé au navigateur ou embarqué dans l'application).

### 6. Dépendances

Bibliothèques et services externes ajoutés, supprimés ou changés de version majeure.

Pour chaque ajout : à quoi il sert dans la PR, et s'il fait doublon avec une dépendance existante.

### 7. Traitements en arrière-plan

Tâches planifiées, files de travail, traitements déclenchés par un événement.

Pour chacun : quand il tourne, ce qu'il fait, avec quels droits.

### 8. Intégrations

- **Entrantes** : un service tiers appelle le système (notifications, rappels de paiement).
- **Sortantes** : le système appelle un service tiers (envoi d'emails, paiement, stockage, IA).

### 9. Droits

Nouveaux rôles, permissions, règles de qui peut faire quoi. C'est une nature à part : elle change la sécurité même sans nouveau point d'entrée.

### 10. Interface

Nouveaux formulaires (chaque formulaire est une entrée de données) et changements visibles de navigation. Reste au niveau utile : ne liste pas chaque petit composant.

## Restituer l'inventaire

La forme exacte est dans `assets/modele-rapport.md`, partie 1. En résumé :

1. **En bref** : 2 à 6 puces en langage fonctionnel, 1 phrase chacune. Exemple : « Un administrateur peut exporter la liste des clients. »
2. **Un sous-titre par nature**, seulement pour les natures présentes dans la PR.
3. **Un bloc par élément** : le statut (`NOUVEAU`, `MODIFIÉ`, `SUPPRIMÉ`), le nom en gras, puis 1 à 3 sous-puces courtes.
4. Les données stockées et échangées renvoient à leur schéma (voir `references/schemas-donnees.md`).
5. **Écarts avec la description** de la PR, s'il y en a.

Pas de tableau large : dans le terminal, il devient illisible (voir `references/lisibilite.md`).

## Sources

- [OWASP — Attack Surface Analysis Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Attack_Surface_Analysis_Cheat_Sheet.html)
