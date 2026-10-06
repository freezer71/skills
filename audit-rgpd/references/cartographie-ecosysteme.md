# Cartographier un écosystème entier

Auditer un écosystème, ce n'est pas auditer un site plusieurs fois. C'est d'abord **trouver tout ce qui existe** : les risques se cachent dans ce que personne n'a pensé à lister. Un vieux sous-domaine de campagne, un formulaire de recrutement hébergé chez un prestataire, un export de fichier clients partagé en lien public.

La cartographie est la première étape de toute démarche de conformité selon la CNIL : sans elle, impossible de savoir quoi auditer.

## 1. Inventorier les composants

Chercher dans toutes les directions, puis croiser.

### Depuis l'extérieur (niveau 1, toujours possible)

- **Liens** depuis le site principal : pied de page, menus, pages légales, liens « espace client », « recrutement », « boutique », « support ».
- **Sous-domaines publics** : les journaux publics de certificats (certificate transparency) listent les noms de domaine pour lesquels un certificat a été émis. C'est une consultation passive de données publiques.
- **Politique de confidentialité et mentions légales** : elles nomment souvent les prestataires, l'hébergeur, les outils.
- **Tiers observés** pendant le contrôle en ligne (voir `references/controle-site-web.md`) : chaque domaine tiers est un composant de l'écosystème.
- **Boutiques d'applications** : applications publiées par l'éditeur.
- **Courriels reçus** après inscription : ils révèlent l'outil d'emailing et ses traceurs.

### Depuis l'intérieur (niveaux 2 et 3)

- Code source : services tiers appelés, variables de configuration qui désignent des services, tâches planifiées (voir `references/audit-code-infrastructure.md`).
- Liste des abonnements et factures logicielles : chaque outil payé traite peut-être des données.
- Entretiens par service : RH, marketing, ventes, support, comptabilité, informatique. Demander à chacun : « quels outils utilisez-vous, qu'y mettez-vous ? ».
- Annuaire des comptes : outils où des salariés se connectent avec leur compte professionnel.

## 2. Décrire chaque composant

Pour chaque composant trouvé, une fiche courte :

- **Nom et rôle** : ce que c'est, à quoi il sert.
- **Données** : quelles catégories, dont sensibles ou pénales.
- **Personnes** : clients, prospects, visiteurs, salariés, candidats, mineurs…
- **Finalité et base légale** déclarées.
- **Où** : hébergement, pays.
- **Qui** : l'organisme seul, un sous-traitant, un responsable conjoint, un tiers indépendant.
- **Combien de temps** : durée de conservation déclarée, et durée réelle si observable.
- **Accès** : qui peut voir les données.

Un composant dont on ne sait rien reste dans la liste avec la mention `[À VÉRIFIER]`. Ne jamais le retirer parce qu'il manque d'information.

## 3. Dessiner les flux

Suivre la donnée de bout en bout, pour les parcours principaux : inscription, achat, contact, candidature, prospection.

Exemple de flux en boîtes de texte :

```
Visiteur
   |
   v
[Formulaire de contact] --(HTTPS)--> [Serveur du site, UE]
   |                                       |
   |                                       +--> [Outil CRM, États-Unis]  <- transfert hors UE
   |                                       |
   |                                       +--> [Boîte de réception commerciale]
   v
[Outil d'emailing, UE] --> courriels avec pixels de suivi
```

À chaque flèche, se demander :
- La donnée est-elle **chiffrée** en transit ?
- Le destinataire est-il **couvert par un contrat** (art. 28) ?
- Sort-elle de l'**UE** ? Avec quelle garantie (art. 44 à 49) ?
- Le destinataire en a-t-il **besoin** ?

## 4. Qualifier les rôles

Pour chaque tiers, déterminer son rôle. Cela fixe le document attendu :

- **Sous-traitant** (agit pour le compte de l'organisme) : contrat conforme à l'art. 28 attendu.
- **Responsable conjoint** (définit les finalités avec l'organisme, comme un réseau social dont on intègre le bouton) : accord art. 26 attendu.
- **Responsable indépendant** (utilise les données pour lui-même) : base légale pour la transmission et information des personnes.

Une régie publicitaire ou un réseau social qui reçoit des données via un traceur est souvent **responsable conjoint** pour la collecte (CJUE, Fashion ID, C-40/17, 2019).

## 5. Consolider

Produire un tableau de synthèse (3 colonnes au plus) :

```
| Composant              | Données                | Risque principal           |
|------------------------|------------------------|----------------------------|
| Site vitrine           | Visiteurs, contacts    | Traceurs avant consentement|
| Outil CRM              | Clients, prospects     | Transfert hors UE          |
```

Puis auditer chaque composant avec la grille `assets/grille-audit.md`. Pour un écosystème large, si des sous-agents sont disponibles, confier un composant par sous-agent avec la même grille, puis fusionner en regroupant les risques de même cause.

## Signaux d'alerte fréquents

- Sous-domaine abandonné qui collecte encore des données (ancienne campagne, ancien jeu-concours).
- Environnement de test ou de préproduction **public** et rempli de vraies données.
- Formulaire hébergé chez un prestataire non déclaré.
- Export de fichier partagé par **lien public** dans un outil de stockage en ligne.
- Outil gratuit adopté par une équipe sans validation (agenda partagé, outil de sondage, outil d'IA générative alimenté avec des données clients).
- Sauvegardes conservées sans limite de durée.

## Sources

- CNIL, « Cartographier vos traitements de données personnelles » : https://www.cnil.fr/fr/rgpd-passer-a-laction
- RGPD, art. 26, 28, 30, 44 à 49 : https://eur-lex.europa.eu/eli/reg/2016/679/oj
- CEPD, lignes directrices 07/2020 sur les notions de responsable et de sous-traitant : https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-072020-concepts-controller-and-processor-gdpr_fr
- CJUE, Fashion ID, C-40/17, 29 juillet 2019 : https://curia.europa.eu/juris/liste.jsf?num=C-40/17
