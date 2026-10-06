# Cotation des risques

Coter un risque, c'est dire **à quel point il est grave** et **dans quel ordre le traiter**. Une cotation doit être explicable : un lecteur doit pouvoir refaire le calcul et arriver au même niveau.

La méthode reprend celle de la CNIL pour les analyses d'impact (PIA) : un risque se mesure par sa **gravité** (l'impact sur les personnes) et sa **vraisemblance** (la probabilité qu'il se réalise). On y ajoute l'**exposition à la sanction**, qui ne change pas le niveau mais aide à prioriser.

## 1. La gravité — impact sur les personnes

Question : si le risque se réalise, que subissent les personnes concernées ?

Échelle de la CNIL, en 4 niveaux :

- **1 — Négligeable.** Désagrément vite surmonté. Exemple : un courriel non sollicité.
- **2 — Limitée.** Désagrément significatif, surmontable avec quelques difficultés. Exemple : profilage publicitaire non consenti, perte de temps pour exercer un droit.
- **3 — Importante.** Conséquences sérieuses, surmontables avec de réelles difficultés. Exemple : usurpation d'identité, fuite d'adresses et de mots de passe, refus d'un service, discrimination.
- **4 — Maximale.** Conséquences graves, voire irréversibles. Exemple : exposition de données de santé, d'opinions, de données de mineurs ; mise en danger physique ; perte d'emploi.

Ce qui fait monter la gravité :
- **données sensibles** (art. 9) ou pénales (art. 10), numéro de sécurité sociale, données bancaires, localisation précise ;
- **personnes vulnérables** : mineurs, patients, salariés, personnes en difficulté ;
- **volume** : nombre de personnes et quantité de données par personne ;
- **caractère irréversible** : une donnée publiée ne se rattrape pas.

## 2. La vraisemblance — probabilité de réalisation

Question : avec quelle facilité le risque se réalise-t-il, ou est-il déjà réalisé ?

- **1 — Négligeable.** Il faudrait un concours de circonstances improbable.
- **2 — Limitée.** Possible, mais exige un effort ou une compétence particulière.
- **3 — Importante.** Facile à réaliser, ou se produit dans certains cas.
- **4 — Maximale.** Se produit à chaque fois, ou est **déjà constaté**.

Règle clé : un écart **constaté** (traceur déposé à chaque visite, mot de passe stocké en clair, donnée visible publiquement) a une vraisemblance de 4. Ce n'est plus un risque, c'est un fait.

## 3. Le niveau de risque

Croiser gravité et vraisemblance :

- **[CRITIQUE]** : gravité 4 et vraisemblance 3 ou 4 ; ou gravité 3 et vraisemblance 4.
- **[HAUTE]** : gravité 4 et vraisemblance 1 ou 2 ; gravité 3 et vraisemblance 2 ou 3 ; gravité 2 et vraisemblance 4.
- **[MOYENNE]** : gravité 3 et vraisemblance 1 ; gravité 2 et vraisemblance 2 ou 3 ; gravité 1 et vraisemblance 4.
- **[BASSE]** : tout le reste (gravité 1 ou 2 avec faible vraisemblance).
- **[À VÉRIFIER]** : impossible à coter faute de preuve. Indiquer le niveau **probable** si la vérification confirme l'écart.

Matrice compacte (lignes = gravité, colonnes = vraisemblance 1 à 4) :

```
            V1        V2        V3        V4
G4      HAUTE     HAUTE     CRITIQUE  CRITIQUE
G3      MOYENNE   HAUTE     HAUTE     CRITIQUE
G2      BASSE     MOYENNE   MOYENNE   HAUTE
G1      BASSE     BASSE     BASSE     MOYENNE
```

## 4. L'exposition à la sanction — pour prioriser

Le niveau de risque reste fondé sur les personnes. Mais deux risques de même niveau ne pèsent pas pareil pour l'organisme. Ajouter une ligne « Exposition » à chaque risque :

- **FORTE** : manquement visible de l'extérieur (contrôle en ligne possible), thème prioritaire de la CNIL ou du CEPD, manquement déjà sanctionné à de nombreuses reprises, ou plainte probable.
- **MOYENNE** : manquement documentaire ou interne, découvert seulement en cas de contrôle sur pièces ou sur place.
- **FAIBLE** : bonne pratique ou recommandation non contraignante.

Les critères de l'art. 83.2 du RGPD, que la CNIL utilise pour fixer une amende, aident à juger l'exposition :
- nature, gravité et **durée** du manquement ;
- nombre de personnes et niveau du dommage ;
- caractère **délibéré** ou négligent ;
- mesures prises pour atténuer le dommage ;
- **manquements antérieurs** ;
- catégories de données concernées ;
- manière dont l'autorité a eu connaissance du manquement (plainte, violation notifiée…).

Plafonds de l'art. 83 : 10 M€ ou 2 % du chiffre d'affaires mondial (obligations du responsable, sécurité, registre, AIPD) ; 20 M€ ou 4 % (principes, bases légales, droits, transferts). Le plafond le plus élevé s'applique. Pour les traceurs, la CNIL sanctionne sur l'art. 82 de la loi Informatique et Libertés. Depuis 2022, une **procédure simplifiée** permet à la CNIL d'infliger jusqu'à 20 000 € pour des cas simples : même une petite structure est exposée.

Ne jamais chiffrer une amende probable dans le rapport. Indiquer le plafond légal et l'exposition, rien de plus.

## 5. Gravité par défaut et ajustement

La grille `assets/grille-audit.md` donne une **gravité par défaut** pour chaque point. C'est un point de départ. Ajuster selon le contexte, et **écrire la raison** de l'ajustement :

- monter d'un niveau si les données sont sensibles, concernent des mineurs ou un grand volume ;
- monter d'un niveau si l'écart est déjà exploité ou visible publiquement ;
- descendre d'un niveau si une mesure compensatoire réduit réellement le risque (et la citer).

## 6. Le verdict global

Le verdict découle des risques, sans appréciation libre :

- `NON CONFORME — ACTION IMMÉDIATE` : au moins 1 risque `[CRITIQUE]`.
- `NON CONFORME — PLAN D'ACTION REQUIS` : au moins 1 risque `[HAUTE]`, aucun `[CRITIQUE]`.
- `CONFORMITÉ PARTIELLE` : uniquement des risques `[MOYENNE]` et `[BASSE]`.
- `AUCUN ÉCART CONSTATÉ SUR LE PÉRIMÈTRE` : aucun écart. Toujours préciser le périmètre, le niveau d'accès et la date.

Si plus de la moitié des points sont `[À VÉRIFIER]`, l'ajouter au verdict : « verdict provisoire, audit incomplet ».

## 7. Délais de correction conseillés

- `[CRITIQUE]` : immédiat, dans les jours qui suivent. Vérifier si une notification de violation s'impose (art. 33 et 34).
- `[HAUTE]` : sous 1 mois.
- `[MOYENNE]` : sous 3 mois.
- `[BASSE]` : au fil de l'eau, lors de la prochaine évolution.

## Sources

- CNIL, méthode PIA (« Analyse d'impact relative à la protection des données — La méthode ») : https://www.cnil.fr/sites/cnil/files/atoms/files/cnil-pia-1-fr-methode.pdf
- CNIL, PIA — les bases de connaissances (échelles de gravité et de vraisemblance) : https://www.cnil.fr/sites/cnil/files/atoms/files/cnil-pia-3-fr-basesdeconnaissances.pdf
- RGPD, art. 83 (conditions générales pour imposer des amendes) : https://eur-lex.europa.eu/eli/reg/2016/679/oj
- CEPD, lignes directrices 04/2022 sur le calcul des amendes : https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-042022-calculation-administrative-fines-under_fr
- CNIL, procédure de sanction simplifiée : https://www.cnil.fr/fr/la-procedure-de-sanction-simplifiee
