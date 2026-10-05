# Modèle — Page de mentions légales avec sommaire

*Modèle à adapter — ne pas publier brut.*

**Mode d'emploi pour l'agent**
- Les blocs `<!-- SI … -->` sont conditionnels : garde ceux qui correspondent au profil (voir `references/mentions-par-profil.md`), **supprime les autres**, puis **renumérote ensemble** le sommaire et les titres.
- Remplace chaque `[…]` par la donnée réelle ; si elle manque, écris `[À COMPLÉTER : …]` et liste-la en fin de réponse. N'invente jamais un SIREN, une adresse, un hébergeur ou un médiateur.
- Les ancres (`{#editeur}` ou `<a id="editeur"></a>`) doivent rester identiques à celles du sommaire. Adapte la syntaxe au moteur de rendu (voir `references/integration-web.md`).
- Retire les commentaires `<!-- -->` et ce mode d'emploi avant livraison.

---

# Mentions légales

*Dernière mise à jour : [JJ mois AAAA]*

Cette page présente les informations légales relatives au site [nom ou URL du site], conformément aux articles 1-1 et 19 de la loi n° 2004-575 du 21 juin 2004 pour la confiance dans l'économie numérique (LCEN).

## Sommaire

1. [Éditeur du site](#editeur)
2. [Directeur de la publication](#directeur-publication)
3. [Hébergement](#hebergement)
4. [Nous contacter](#contact)
5. [Activité réglementée](#activite-reglementee)
6. [Médiation de la consommation](#mediation)
7. [Propriété intellectuelle](#propriete-intellectuelle)
8. [Données personnelles](#donnees-personnelles)
9. [Cookies](#cookies)
10. [Accessibilité](#accessibilite)
11. [Crédits](#credits)

---

<a id="editeur"></a>
## 1. Éditeur du site

<!-- SI SOCIÉTÉ -->
Le site [URL] est édité par :

- **Dénomination sociale** : [Dénomination]
- **Forme juridique** : [SAS / SARL / …] au capital de [montant] €
- **Siège social** : [adresse complète]
- **Immatriculation** : [SIREN 9 chiffres] RCS [ville du greffe]
- **N° de TVA intracommunautaire** : [FR…]
- **Téléphone** : [+33 …]
- **E-mail** : [adresse]

<!-- SI ENTREPRENEUR INDIVIDUEL / MICRO-ENTREPRENEUR -->
Le site [URL] est édité par :

- **[Prénom Nom] EI**[, exerçant sous le nom commercial « … »]
- **Adresse** : [adresse de l'établissement ou de domiciliation]
- **SIREN** : [9 chiffres][ — mention d'immatriculation telle que sur l'extrait, le cas échéant]
- **N° de TVA intracommunautaire** : [FR…] <!-- ou supprimer si franchise en base -->
- **Téléphone** : [+33 …]
- **E-mail** : [adresse]

<!-- SI ASSOCIATION -->
Le site [URL] est édité par l'association **[Nom]**, association déclarée régie par la loi du 1er juillet 1901.

- **Siège** : [adresse]
- **N° RNA** : [W…][ — SIREN : …]
- **Téléphone** : [+33 …]
- **E-mail** : [adresse]

<!-- SI PARTICULIER NON PROFESSIONNEL QUI S'IDENTIFIE -->
Le site [URL] est un site personnel édité à titre non professionnel par **[Prénom Nom]**, [adresse], [téléphone].

<!-- SI PARTICULIER NON PROFESSIONNEL ANONYME -->
Le site [URL] est un site personnel édité à titre non professionnel. Conformément à l'article 1-1, II de la LCEN, son éditeur a choisi de ne pas rendre publiques ses coordonnées ; celles-ci ont été communiquées à l'hébergeur mentionné ci-dessous.
<!-- Dans ce cas, supprimer la section « Directeur de la publication » si elle révélerait l'identité, et ne garder que le nom, la dénomination et l'adresse de l'hébergeur. -->

<a id="directeur-publication"></a>
## 2. Directeur de la publication

Le directeur de la publication est **[Prénom Nom]**, en qualité de [président / gérant / représentant légal / éditeur].

<!-- SI PRESSE EN LIGNE : ajouter -->
<!-- Responsable de la rédaction : [Prénom Nom]. Le droit de réponse s'exerce auprès du directeur de la publication à [e-mail / adresse]. -->

<a id="hebergement"></a>
## 3. Hébergement

Le site est hébergé par :

- **[Dénomination de l'hébergeur]**
- [Adresse complète]
- [Téléphone]
- [Site web de l'hébergeur]

<!-- SI DONNÉES STOCKÉES CHEZ UN AUTRE PRESTATAIRE (art. 1-1, I LCEN) -->
Les données traitées par le site sont stockées par **[Dénomination]**, [adresse], [localisation des serveurs si connue].

<a id="contact"></a>
## 4. Nous contacter

- **Par e-mail** : [adresse]
- **Par téléphone** : [+33 …][, du lundi au vendredi de … à …]
- **Par courrier** : [adresse]
<!-- Peut être fusionnée dans « Éditeur du site » si la page est courte ; un formulaire peut s'ajouter mais ne remplace pas l'e-mail pour un site marchand. -->

<!-- SI PROFESSION RÉGLEMENTÉE OU ACTIVITÉ SOUS AUTORISATION -->
<a id="activite-reglementee"></a>
## 5. Activité réglementée

- **Titre professionnel** : [titre], obtenu en [France / État membre]
- **Ordre ou organisme d'inscription** : [nom, adresse][ — n° d'inscription : RPPS / ORIAS / carte professionnelle n° … délivrée par …]
- **Règles professionnelles applicables** : [nom du code de déontologie ou règlement, avec lien]
- **Autorité ayant délivré l'autorisation** : [nom, adresse] <!-- si activité soumise à autorisation -->
- **Garantie financière / assurance professionnelle** : [le cas échéant]

<!-- SI VENTE À DES CONSOMMATEURS -->
<a id="mediation"></a>
## 6. Médiation de la consommation

Conformément aux articles L. 612-1 et suivants du Code de la consommation, en cas de litige non résolu avec notre service client, vous pouvez recourir gratuitement au médiateur de la consommation dont nous relevons :

- **[Nom du médiateur]**
- [Adresse postale]
- [Site internet — lien de saisie en ligne le cas échéant]

Avant de saisir le médiateur, vous devez avoir adressé une réclamation écrite à [e-mail / adresse du service client]. Nos conditions générales de vente sont disponibles [ici](/cgv).

<a id="propriete-intellectuelle"></a>
## 7. Propriété intellectuelle

Les contenus de ce site (textes, images, logos, éléments graphiques, [code]) sont protégés par le droit d'auteur et, le cas échéant, le droit des marques. Sauf mention contraire, ils appartiennent à [Éditeur]. Leur reproduction ou réutilisation sans autorisation est interdite, sous réserve des exceptions prévues par le Code de la propriété intellectuelle.

<!-- Si certains contenus sont sous licence libre ou appartiennent à des tiers, le préciser ici ou dans « Crédits ». -->

<a id="donnees-personnelles"></a>
## 8. Données personnelles

<!-- SI COLLECTE DE DONNÉES -->
[Éditeur] traite des données personnelles dans le cadre de ce site, en qualité de responsable de traitement. Les finalités, bases légales, durées de conservation, destinataires et vos droits sont détaillés dans notre [politique de confidentialité](/politique-de-confidentialite).

Pour exercer vos droits (accès, rectification, effacement, opposition, limitation, portabilité), écrivez à [e-mail dédié / DPO : Prénom Nom, e-mail]. Vous pouvez également introduire une réclamation auprès de la CNIL ([www.cnil.fr](https://www.cnil.fr)).

<!-- SI AUCUNE COLLECTE, VÉRIFIÉE -->
<!-- Ce site ne collecte pas de données personnelles. -->

<a id="cookies"></a>
## 9. Cookies

<!-- SI TRACEURS SOUMIS À CONSENTEMENT -->
Ce site utilise des cookies et autres traceurs, dont certains sont soumis à votre consentement. Leur fonctionnement est décrit dans notre [politique cookies](/cookies). Vous pouvez modifier vos choix à tout moment via le lien « [Gérer mes cookies] » présent en bas de chaque page.

<!-- SI AUCUN TRACEUR SOUMIS À CONSENTEMENT -->
<!-- Ce site n'utilise que des cookies strictement nécessaires à son fonctionnement, qui ne requièrent pas votre consentement. -->

<!-- SI ENTITÉ CONCERNÉE PAR LES OBLIGATIONS D'ACCESSIBILITÉ -->
<a id="accessibilite"></a>
## 10. Accessibilité

**Accessibilité : [totalement / partiellement / non] conforme.** Le détail figure dans notre [déclaration d'accessibilité](/accessibilite). Pour signaler une difficulté d'accès à un contenu : [e-mail / formulaire].

<a id="credits"></a>
## 11. Crédits

- **Conception et développement** : [prestataire ou « réalisé en interne »]
- **Photographies et illustrations** : [auteurs, banques d'images, licences]
- **Icônes et polices** : [noms et licences]

---

*Documents liés : [Politique de confidentialité](/politique-de-confidentialite) · [Cookies](/cookies) · [CGV](/cgv) · [CGU](/cgu) · [Accessibilité](/accessibilite)*

---

## Exemple rempli (fictif) — petite SAS de vente en ligne

*Toutes les données ci-dessous sont fictives et servent uniquement à illustrer le rendu attendu.*

> # Mentions légales
>
> *Dernière mise à jour : 30 septembre 2026*
>
> ## Sommaire
>
> 1. [Éditeur du site](#editeur)
> 2. [Directeur de la publication](#directeur-publication)
> 3. [Hébergement](#hebergement)
> 4. [Médiation de la consommation](#mediation)
> 5. [Propriété intellectuelle](#propriete-intellectuelle)
> 6. [Données personnelles](#donnees-personnelles)
> 7. [Cookies](#cookies)
>
> ## 1. Éditeur du site
>
> Le site atelier-exemple.fr est édité par :
>
> - **Dénomination sociale** : Atelier Exemple
> - **Forme juridique** : SAS au capital de 5 000 €
> - **Siège social** : 1 rue de l'Exemple, 00000 Villexemple
> - **Immatriculation** : 000 000 000 RCS Villexemple
> - **N° de TVA intracommunautaire** : FR00000000000
> - **Téléphone** : +33 1 00 00 00 00
> - **E-mail** : contact@atelier-exemple.fr
>
> ## 2. Directeur de la publication
>
> Le directeur de la publication est Camille Exemple, en qualité de présidente.
>
> ## 3. Hébergement
>
> …
