# Checklist — Relire ou auditer des mentions légales

*Modèle à adapter — ne pas publier brut.*

À utiliser pour contrôler une page produite avec ce skill, ou pour auditer une page existante. Restitue le résultat sous forme de tableau **Point / Statut (✅ conforme · ⚠️ à améliorer · ❌ manquant ou erroné) / Correction proposée**, en commençant par les ❌.

## Sommaire

1. [Structure et lisibilité](#1-structure-et-lisibilité)
2. [Identification de l'éditeur](#2-identification-de-léditeur)
3. [Publication et hébergement](#3-publication-et-hébergement)
4. [Activité commerciale ou réglementée](#4-activité-commerciale-ou-réglementée)
5. [Renvois RGPD, cookies et documents liés](#5-renvois-rgpd-cookies-et-documents-liés)
6. [Mentions obsolètes ou fautives](#6-mentions-obsolètes-ou-fautives)
7. [Accès et intégration](#7-accès-et-intégration)

## 1. Structure et lisibilité

- [ ] Titre unique « Mentions légales »
- [ ] Date de dernière mise à jour, en toutes lettres, récente et plausible
- [ ] **Sommaire** numéroté juste après la date
- [ ] Chaque entrée du sommaire = un lien d'ancre qui fonctionne
- [ ] Libellés et numéros du sommaire **identiques** aux titres de section
- [ ] Ordre : éditeur → directeur de la publication → hébergement → (contact, activité, médiateur) → (PI) → renvois données/cookies → (accessibilité, crédits)
- [ ] Identification en liste ou tableau, pas en paragraphe dense
- [ ] Aucune section vide ou « non applicable » laissée sans raison
- [ ] Aucun `[À COMPLÉTER]` ni texte d'exemple (« Lorem ipsum », « Votre société ») restant
- [ ] Pas de clause d'intimidation ni d'exonération générale de responsabilité
- [ ] Texte en français

## 2. Identification de l'éditeur

- [ ] Le bon éditeur (le client, pas l'agence ; la bonne entité du groupe)
- [ ] Personne physique : nom, prénom, adresse, téléphone ; « EI » si entrepreneur individuel
- [ ] Personne morale : dénomination, forme juridique, capital social, siège, téléphone
- [ ] SIREN + « RCS [ville] » (ou mention d'immatriculation adaptée) si immatriculé
- [ ] N° de TVA intracommunautaire si assujetti (obligatoire en e-commerce)
- [ ] E-mail (obligatoire en e-commerce)
- [ ] Association : n° RNA
- [ ] Particulier anonyme : mention de l'article 1-1, II et coordonnées de l'hébergeur — et l'activité est bien non professionnelle
- [ ] Données cohérentes avec l'extrait d'immatriculation, le pied de page, les CGV et la politique de confidentialité

## 3. Publication et hébergement

- [ ] Directeur de la publication nommé, personne physique, cohérent avec le représentant légal
- [ ] Responsable de la rédaction (presse en ligne)
- [ ] Hébergeur : dénomination, adresse, **téléphone**, à jour
- [ ] Prestataire de stockage des données mentionné s'il est distinct de l'hébergeur

## 4. Activité commerciale ou réglementée

- [ ] Vente aux consommateurs : **médiateur de la consommation** (nom, adresse, site), adhésion réelle
- [ ] Lien vers les CGV (et CGU le cas échéant)
- [ ] Profession réglementée : titre, État d'obtention, ordre/organisme, n° d'inscription, règles professionnelles
- [ ] Activité sous autorisation : autorité délivrante
- [ ] Contenus d'utilisateurs : moyen de signaler un contenu illicite

## 5. Renvois RGPD, cookies et documents liés

- [ ] Section « Données personnelles » courte avec **lien** vers la politique de confidentialité (qui existe et répond)
- [ ] Contact pour exercer ses droits (e-mail dédié ou DPO)
- [ ] Section « Cookies » avec lien vers la politique cookies et moyen de **modifier ses choix**
- [ ] Si « aucune donnée collectée » est affirmé : vérifié (formulaires, statistiques, intégrations tierces, polices externes)
- [ ] Cohérence éditeur / responsable de traitement ; hébergeur présent parmi les sous-traitants de la politique (voir le skill `rgpd`)
- [ ] Accessibilité : mention de conformité et lien vers la déclaration si l'entité est concernée

## 6. Mentions obsolètes ou fautives

- [ ] Pas de « déclaration CNIL n° … » ni de récépissé CNIL
- [ ] Pas de référence à « l'article 34 de la loi du 6 janvier 1978 »
- [ ] Pas de lien vers la plateforme européenne ODR/RLL (fermée le 20 juillet 2025)
- [ ] Références LCEN à jour (« article 1-1 », plus « article 6-III »)
- [ ] Pas de « Accessibilité : conforme » sans audit
- [ ] Pas d'année de copyright figée et ancienne

## 7. Accès et intégration

- [ ] Lien « Mentions légales » dans le pied de page de **toutes** les pages
- [ ] Page en HTML textuel (pas d'image ni de PDF seul), accessible sans connexion ni consentement
- [ ] E-mail et téléphone cliquables (`mailto:`, `tel:`)
- [ ] Structure de titres correcte (un `h1`, des `h2`), sommaire dans une `nav` étiquetée
- [ ] Dans un dépôt de code : informations centralisées dans une seule source
