# Principes fondamentaux du RGPD

Le RGPD (Règlement UE 2016/679) repose sur des principes définis aux **articles 5 à 11**. Tout traitement doit respecter simultanément l'ensemble de ces principes — ils ne sont pas alternatifs.

## Article 4 — Définitions essentielles

- **Donnée à caractère personnel** : toute information se rapportant à une personne physique identifiée ou identifiable (directement ou indirectement, par référence à un identifiant : nom, numéro, IP, données de localisation, identifiant en ligne, éléments propres à son identité).
- **Traitement** : toute opération sur des données (collecte, enregistrement, conservation, modification, consultation, communication, diffusion, effacement). Y compris un simple fichier Excel.
- **Responsable de traitement** : entité qui détermine **finalités et moyens** du traitement.
- **Sous-traitant** : entité qui traite des données **pour le compte du** responsable.
- **Personne concernée** : la personne physique dont les données sont traitées.
- **Profilage** : traitement automatisé visant à évaluer certains aspects personnels (performances au travail, situation économique, santé, préférences, comportement, localisation).
- **Pseudonymisation** (art. 4.5) : traitement de manière à ce que les données ne puissent plus être attribuées à une personne sans information supplémentaire conservée séparément et protégée. ≠ Anonymisation (irréversible, sort du champ du RGPD, considérant 26).

### Données identifiables, pseudonymisées, anonymes : l'approche contextuelle

Pour savoir si une personne est « identifiable », tiens compte de **l'ensemble des moyens raisonnablement susceptibles d'être utilisés** pour l'identifier, par le responsable ou par un tiers (considérant 26 ; CJUE, 19 oct. 2016, Breyer, C-582/14, pour l'adresse IP dynamique).

**CJUE, 4 sept. 2025, CEPD c/ CRU (SRB), C-413/23 P** (rendu sous le règlement 2018/1725, transposable au RGPD dont les définitions sont identiques) :
- Les **opinions ou commentaires** d'une personne sont des données qui la concernent, par nature.
- Les données pseudonymisées ne sont **pas, dans tous les cas et pour toute personne**, des données personnelles : pour un **destinataire** qui ne dispose pas de moyens raisonnables de réidentification (pas d'accès à la table de correspondance, mesures techniques et organisationnelles efficaces), elles peuvent ne pas l'être.
- Mais pour le **responsable** qui détient l'information supplémentaire, elles **restent des données personnelles**. L'obligation d'information (art. 13-14 RGPD, ici art. 15 du règlement 2018/1725) s'apprécie **de son point de vue, au moment de la collecte** : il doit informer les personnes des destinataires, même si ceux-ci ne peuvent pas les réidentifier.

**Conséquences pratiques** :
- Ne présume jamais qu'un jeu pseudonymisé « n'est plus du RGPD » chez toi : la relativité joue pour le destinataire, pas pour celui qui détient la clé.
- Pour le destinataire, documente l'analyse : moyens disponibles, contrats interdisant la réidentification, risque de recoupement avec d'autres sources.
- La pseudonymisation reste une **mesure de sécurité** et de minimisation (art. 25, 32) utile, qui réduit le risque.

**Doctrine du CEPD** :
- **Lignes directrices 01/2025 sur la pseudonymisation** (adoptées le 16 janvier 2025 en version soumise à consultation) : définition, avantages, mesures techniques, notion de « domaine de pseudonymisation ». Le CEPD prépare une version mise à jour après l'arrêt SRB ; vérifie si elle a été publiée.
- **Lignes directrices 02/2026 sur l'anonymisation** (adoptées le 7 juillet 2026, **consultation publique jusqu'au 30 octobre 2026**) : elles intègrent l'arrêt SRB et proposent une méthode **contextuelle** (selon les moyens de chaque acteur) ou une méthode **simplifiée**. Une donnée est anonyme si elle ne permet ni d'**isoler** un individu, ni de **relier** des enregistrements le concernant, ni de **déduire** des informations sur lui ; si l'un de ces critères n'est pas rempli, une analyse plus poussée s'impose. Vérifie, une fois la version finale adoptée, leur articulation avec l'avis 05/2014 du G29 sur les techniques d'anonymisation, qui reste la référence historique.

**Proposition Digital Omnibus (non adoptée)** : la Commission (COM(2025) 837, 19 novembre 2025) propose de modifier l'**art. 4.1** pour préciser qu'une information n'est pas une donnée personnelle pour une entité qui ne peut pas raisonnablement identifier la personne, même si une autre entité le peut. Le CEPD et le Contrôleur européen (avis conjoint 2/2026, février 2026) demandent aux colégislateurs de **ne pas adopter** ce changement, qui réduirait le champ du RGPD au-delà de la jurisprudence. Au Conseil, des compromis alternatifs (disposition spécifique sur la pseudonymisation) sont discutés. **Au 1er octobre 2026, la définition de l'art. 4.1 est inchangée** : raisonne avec le texte en vigueur et la jurisprudence.

## Article 5 — Les 6 + 1 principes

### 1. Licéité, loyauté, transparence (art. 5.1.a)
Le traitement doit reposer sur une **base légale valide** (cf. article 6, voir `references/bases-legales.md`), être conduit de manière loyale (sans tromperie, sans collecte cachée) et transparente (la personne sait qui traite, pourquoi, comment).

### 2. Limitation des finalités (art. 5.1.b)
Les données sont collectées pour des **finalités déterminées, explicites et légitimes**. Pas de traitement ultérieur incompatible. *Exemple :* des données collectées pour la facturation ne peuvent être réutilisées pour de la prospection commerciale sans nouvelle base légale.

### 3. Minimisation des données (art. 5.1.c)
Les données doivent être **adéquates, pertinentes et limitées à ce qui est nécessaire**. La question à se poser : *« puis-je atteindre cette finalité avec moins de données ? »* Si oui, ne collecte pas le superflu.

### 4. Exactitude (art. 5.1.d)
Les données doivent être **exactes et tenues à jour**. Les données inexactes doivent être effacées ou rectifiées **sans délai**. C'est l'envers du droit de rectification (art. 16).

### 5. Limitation de la conservation (art. 5.1.e)
Les données sont conservées **pas plus longtemps que nécessaire**. Pour chaque finalité, fixer une durée (base active, archivage intermédiaire, archivage définitif ou suppression). Référentiels de durées CNIL par secteur (RH, prospection, santé, etc.).

### 6. Intégrité et confidentialité (art. 5.1.f)
Les données sont traitées de manière à garantir **une sécurité appropriée** (mesures techniques et organisationnelles contre traitement non autorisé, perte, destruction). Couvre chiffrement, contrôle d'accès, journalisation, sauvegardes.

### 7. Responsabilité / Accountability (art. 5.2)
Le responsable de traitement est **non seulement tenu** de respecter les principes, **mais doit pouvoir démontrer** ce respect. → Documentation : registre, politiques, AIPD, traces de consentement, audits, contrats.

C'est la transformation majeure du RGPD vs. la directive de 1995 : passage d'un régime déclaratif (formalités préalables à la CNIL) à un régime de responsabilisation.

## Article 6 — Bases légales

Voir le fichier dédié `references/bases-legales.md`. Six bases possibles, une seule à choisir par finalité.

## Article 7 — Conditions du consentement

Voir `references/consentement-cookies.md`.

## Article 8 — Consentement des mineurs

En France, l'âge minimal pour consentir seul aux services de la société de l'information est **15 ans**. En-dessous, consentement conjoint titulaire de l'autorité parentale + mineur.

## Article 9 — Données sensibles

Voir `references/donnees-sensibles.md`. Régime d'interdiction de principe avec exceptions strictes.

## Article 10 — Données pénales

Le traitement de données relatives aux **condamnations et infractions** est réservé à l'autorité publique sauf exceptions encadrées par le droit national (en France, art. 46 LIL).

## Article 11 — Traitement sans identification

Si le responsable n'a pas besoin d'identifier la personne, il n'a pas à conserver les éléments d'identification au seul fait du RGPD. Mais alors, certains droits (accès, rectification…) ne s'appliquent pas si la personne ne fournit pas d'éléments complémentaires.

## Champ d'application territorial (article 3)

Le RGPD s'applique :
- Aux établissements **dans l'UE** (peu importe où se déroule le traitement) ;
- Aux entités **hors UE** qui : (a) offrent biens/services à des personnes dans l'UE, OU (b) suivent le comportement de personnes dans l'UE (ex. tracking d'utilisateurs européens).

→ Une startup américaine qui vend en France est dans le champ. Elle doit désigner un représentant dans l'UE (art. 27).

## Sources

- [Texte RGPD consolidé — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- [Les 6 grands principes — CNIL](https://www.cnil.fr/fr/comprendre-le-rgpd/les-six-grands-principes-du-rgpd)
- [Chapitre II Principes — CNIL](https://www.cnil.fr/fr/reglement-europeen-protection-donnees/chapitre2)
- [CJUE, 4 sept. 2025, CEPD c/ CRU, C-413/23 P — communiqué](https://curia.europa.eu/site/upload/docs/application/pdf/2025-09/cp250107en.pdf)
- [CJUE, C-413/23 P — Curia](https://curia.europa.eu/juris/liste.jsf?num=C-413%2F23)
- [Lignes directrices CEPD 01/2025 sur la pseudonymisation](https://www.edpb.europa.eu/news/news/2025/edpb-adopts-pseudonymisation-guidelines-and-paves-way-improve-cooperation_en)
- [Lignes directrices CEPD 02/2026 sur l'anonymisation (consultation)](https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en)
- [Communiqué CEPD sur l'anonymisation (8 juillet 2026)](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)
- [Proposition Digital Omnibus COM(2025) 837 — EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=COM%3A2025%3A837%3AFIN)
- [Avis conjoint 2/2026 du CEPD et du Contrôleur européen sur le Digital Omnibus](https://www.edpb.europa.eu/news/news/2026/digital-omnibus-edpb-and-edps-support-simplification-and-competitiveness-while_en)
