# Mentions exigées selon le profil de l'éditeur

Qualifie **d'abord** le profil, puis additionne les blocs : un avocat qui vend des consultations en ligne cumule « société ou EI » + « commerce électronique » + « profession réglementée ». Les références aux articles sont détaillées dans `references/cadre-juridique.md`.

Légende : **O** = obligatoire · **C** = obligatoire sous condition · **R** = recommandé.

## Sommaire

1. [Tableau de synthèse](#1-tableau-de-synthèse)
2. [Particulier, site non professionnel](#2-particulier-site-non-professionnel)
3. [Entrepreneur individuel et micro-entrepreneur](#3-entrepreneur-individuel-et-micro-entrepreneur)
4. [Société (SAS, SASU, SARL, EURL, SA, SCI…)](#4-société-sas-sasu-sarl-eurl-sa-sci)
5. [Association](#5-association)
6. [Commerce électronique et vente aux consommateurs](#6-commerce-électronique-et-vente-aux-consommateurs)
7. [Professions réglementées et activités sous autorisation](#7-professions-réglementées-et-activités-sous-autorisation)
8. [Presse en ligne](#8-presse-en-ligne)
9. [Secteur public](#9-secteur-public)
10. [Éditeur établi hors de France](#10-éditeur-établi-hors-de-france)
11. [Application mobile, SaaS, extension](#11-application-mobile-saas-extension)
12. [Sources](#sources)

## 1. Tableau de synthèse

| Mention | Particulier non pro | EI / micro | Société | Association | + e-commerce |
|---|---|---|---|---|---|
| Nom, prénom / dénomination | C (anonymat possible) | O (avec « EI ») | O (+ forme juridique) | O | O |
| Adresse (domicile / siège) | C | O | O | O | O |
| Téléphone | C | O | O | O | O |
| E-mail | R | R | R | R | **O** |
| SIREN + RCS/RNE | — | O si immatriculé | O | C (si SIREN) | O |
| Capital social | — | — | O | — | O |
| N° TVA intracommunautaire | — | C (si assujetti) | C (si assujetti) | C | **O si assujetti** |
| Directeur de la publication | C | O | O | O | O |
| Hébergeur (nom, adresse, tél.) | O | O | O | O | O |
| Stockage des données (si distinct) | C | C | C | C | C |
| Médiateur de la consommation | — | C (si clients consommateurs) | C (idem) | C (idem) | **O** |
| Renvoi politique de confidentialité | C (si données collectées) | C | C | C | O en pratique |
| Accessibilité | — | C | C | C | C (EAA) |

## 2. Particulier, site non professionnel

Blog personnel, portfolio sans activité commerciale, site de passionné.

- **Choix 1 — identification complète** : nom, prénom, domicile, téléphone, directeur de la publication (soi-même), hébergeur.
- **Choix 2 — anonymat** (LCEN art. 1-1, II) : seulement le nom et l'adresse de l'**hébergeur**, à condition de lui avoir fourni son identité. Rédiger alors une mention du type : « Conformément à l'article 1-1, II de la LCEN, l'éditeur de ce site, personne physique agissant à titre non professionnel, a choisi de ne pas rendre publiques ses coordonnées ; celles-ci ont été communiquées à l'hébergeur. »
- **Attention** : un portfolio de freelance qui démarche des clients, un blog monétisé de manière significative ou un site avec liens d'affiliation rémunérés au titre d'une activité sont **professionnels** — l'anonymat n'est plus possible.
- Si le site collecte des données (formulaire de contact, commentaires, statistiques avec cookies), une information RGPD reste due (skill `rgpd`).

## 3. Entrepreneur individuel et micro-entrepreneur

- Nom et prénom **précédés ou suivis de « EI » ou « entrepreneur individuel »** (ex. « Camille Martin EI »), et le nom commercial le cas échéant.
- Adresse de l'établissement. Beaucoup d'EI sont domiciliés chez eux : l'adresse publique peut être une **adresse de domiciliation** si l'entreprise en a une ; sinon l'adresse déclarée est due. Signale cette tension à l'utilisateur plutôt que de l'omettre.
- Téléphone, e-mail.
- SIREN et mention d'immatriculation telle qu'elle figure sur l'extrait (RCS de la ville du greffe pour un commerçant ; pour les activités libérales non immatriculées, le SIREN seul).
- **TVA** : si l'entrepreneur bénéficie de la franchise en base, pas de numéro de TVA à afficher ; la mention « TVA non applicable, art. 293 B du CGI » concerne les **factures et l'affichage des prix**, pas obligatoirement les mentions légales — l'ajouter si le site affiche des prix.
- Directeur de la publication : l'entrepreneur lui-même.
- Hébergeur.

## 4. Société (SAS, SASU, SARL, EURL, SA, SCI…)

- Dénomination sociale, **forme juridique** et **capital social** (préciser « à capital variable » le cas échéant ; pour un capital variable, le capital minimum ou le capital souscrit selon les statuts).
- Adresse du siège social, téléphone, e-mail.
- **SIREN** + « RCS [ville du greffe] » (ex. « 123 456 789 RCS Lyon »).
- Numéro de TVA intracommunautaire si assujettie.
- Nom commercial ou enseigne si différent de la dénomination.
- Directeur de la publication : le **représentant légal** (président, gérant, directeur général), nommé.
- Hébergeur ; stockage des données si distinct.
- **Groupe de sociétés** : c'est la société qui édite **ce** site qui doit être identifiée, pas la maison mère par défaut.

## 5. Association

- Nom de l'association, adresse du siège, téléphone, e-mail.
- Numéro **RNA** (W + 9 chiffres) et, si l'association en a un, son **SIREN/SIRET** ; mention de la déclaration en préfecture si utile.
- Pour une association reconnue d'utilité publique : la mention et le décret de reconnaissance (R).
- Directeur de la publication : en principe le **président**.
- Hébergeur.
- Si l'association vend (billetterie, boutique) ou reçoit des dons en ligne : ajouter les blocs e-commerce, et renvoyer vers les conditions de don et la politique de confidentialité (reçus fiscaux = données personnelles).

## 6. Commerce électronique et vente aux consommateurs

S'ajoutent au profil de base (article 19 LCEN, Code de la consommation) :

- **E-mail** de contact (un formulaire ne suffit pas).
- **Numéro de TVA intracommunautaire** si assujetti.
- **Médiateur de la consommation** : nom, adresse postale, site internet (et, si le médiateur le prévoit, le lien de saisie en ligne). Vérifier que l'entreprise a bien **adhéré** à ce médiateur.
- **Lien vers les CGV** (et CGU s'il y a des comptes utilisateurs) ; les CGV portent l'essentiel de l'information précontractuelle (prix, livraison, rétractation, garanties).
- **Ne plus** mettre de lien vers la plateforme européenne ODR (fermée le 20 juillet 2025).
- Accessibilité : service de commerce électronique couvert par la directive (UE) 2019/882 depuis le 28 juin 2025, sauf micro-entreprise prestataire de services.
- **Places de marché / plateformes** : obligations spécifiques de transparence (Code de la consommation, règlement (UE) 2022/2065 sur les services numériques — DSA) qui dépassent les mentions légales ; les traiter dans les CGU et une page dédiée, et le signaler à l'utilisateur.

## 7. Professions réglementées et activités sous autorisation

Pour toute profession réglementée (article 19, 6° LCEN) : **titre professionnel**, **État** où il a été obtenu, **ordre ou organisme** d'inscription, **référence aux règles professionnelles** applicables (lien vers le code de déontologie). Pour une activité sous autorisation (article 19, 5°) : nom et adresse de l'**autorité** qui l'a délivrée.

Exemples courants (vérifier les exigences propres à chaque profession auprès de l'ordre ou de l'organisme concerné, elles évoluent) :

| Profession | Éléments habituellement attendus |
|---|---|
| Avocat | Barreau d'inscription, titre d'avocat, règles : Règlement intérieur national (RIN) ; structure d'exercice le cas échéant |
| Médecin, chirurgien-dentiste, kinésithérapeute, pharmacien | Ordre d'inscription, numéro RPPS, règles déontologiques (Code de la santé publique) ; respecter les règles propres à la communication des professionnels de santé |
| Expert-comptable, commissaire aux comptes | Inscription au tableau de l'Ordre / sur la liste tenue par la Haute autorité de l'audit (H2A, ex-H3C) pour les commissaires aux comptes |
| Agent immobilier, administrateur de biens (loi Hoguet) | Numéro de carte professionnelle, CCI qui l'a délivrée, garant financier (nom, adresse, montant), assurance responsabilité civile professionnelle |
| Intermédiaire en assurance, en opérations de banque, conseiller en investissements financiers | Numéro d'immatriculation **ORIAS** (et lien vers orias.fr), catégorie d'intermédiaire, autorité de contrôle (ACPR, AMF selon le cas) |
| Architecte | Inscription au tableau de l'Ordre régional, assurance professionnelle |
| Artisan du bâtiment (obligation d'assurance décennale) | Assurance décennale : nom de l'assureur et couverture géographique — exigée sur devis et factures ; l'indiquer sur le site est une bonne pratique |

Si la profession de l'utilisateur ne figure pas ici ou si ses règles de communication sont strictes (santé, droit), **dis-le** et recommande de vérifier auprès de l'ordre avant publication.

## 8. Presse en ligne

- Un service de presse en ligne (SPEL) doit identifier le **directeur de la publication** et, le cas échéant, le **responsable de la rédaction**.
- Mentions d'usage : numéro ISSN s'il y en a un, numéro de commission paritaire (CPPAP) le cas échéant, informations sur la propriété et les actionnaires (transparence des entreprises de presse, loi n° 86-897 du 1er août 1986).
- Le **droit de réponse en ligne** (LCEN, art. 1-1, III depuis la loi SREN) s'exerce auprès du directeur de la publication : indiquer comment le joindre.
- Pour la déontologie et le droit de la presse, charge le skill `journaliste` (`references/droit-presse.md`).

## 9. Secteur public

Collectivités, établissements publics, administrations :

- Nom de l'entité, adresse, téléphone, SIRET (R).
- Directeur de la publication : l'autorité exécutive (maire, président du conseil départemental/régional, directeur d'établissement).
- Hébergeur.
- **Accessibilité** : mention de conformité en pied de page, **déclaration d'accessibilité**, schéma pluriannuel et plan d'action annuel (obligatoires).
- Réutilisation des informations publiques et licence (ex. Licence Ouverte / Etalab) (R).
- Le DPO est obligatoire pour les organismes publics (art. 37 RGPD) : le renvoi vers la politique de confidentialité doit mentionner son contact (skill `rgpd`).

## 10. Éditeur établi hors de France

- Un éditeur établi dans un autre État de l'UE relève en principe de la loi de son État d'établissement pour les règles d'identification (principe du pays d'origine de la directive 2000/31/CE sur le commerce électronique) — mais le **droit de la consommation français** s'applique largement lorsqu'il cible des consommateurs en France.
- Un éditeur hors UE qui cible le public français : appliquer par prudence le socle LCEN et, pour les données personnelles, désigner un **représentant dans l'UE** (art. 27 RGPD) — voir le skill `rgpd`.
- Signaler que ces cas relèvent d'une analyse juridique plus fine.

## 11. Application mobile, SaaS, extension

- La LCEN vise tout **service de communication au public en ligne** : une application ou un SaaS est concerné.
- Rendre les mentions accessibles **dans l'application** (écran « Informations légales » ou « À propos ») et sur la fiche du magasin d'applications ou le site associé.
- Hébergeur : celui du back-end (serveur, API, base de données) ; si le client est uniquement distribué par un magasin d'applications, le magasin n'est pas l'hébergeur du service.
- Les CGU sont souvent plus structurantes que les mentions légales pour un SaaS : lier les deux.

## Sources

- [LCEN, articles 1-1 et 19 — Légifrance](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000801164)
- [Obligations d'un site internet professionnel — Service-public.fr (Entreprendre)](https://entreprendre.service-public.gouv.fr/vosdroits/F31228)
- [Entrepreneur individuel (EI) : ce qu'il faut savoir — Service-public.fr (Entreprendre)](https://entreprendre.service-public.gouv.fr/vosdroits/F37396)
- [Médiation de la consommation — economie.gouv.fr](https://www.economie.gouv.fr/mediation-conso)
- [Registre ORIAS](https://www.orias.fr)
- [Accessibilité numérique : champ d'application — RGAA](https://accessibilite.numerique.gouv.fr/obligations/champ-application/)
