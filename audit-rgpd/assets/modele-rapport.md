# Modèle — Rapport d'audit RGPD

**Modèle à adapter — ne pas publier brut.**

Règles d'emploi :
- Garder **les 7 parties, dans cet ordre**. Une partie vide tient en une ligne, elle ne disparaît pas.
- Risques classés **par gravité**, pas par domaine. Numérotés R1, R2…
- Pour chaque risque, **toujours les mêmes libellés, dans le même ordre** : Où, Constat, Preuve, Règle, Risque pour les personnes, Exposition, Correction.
- Une idée par ligne. Phrases de 15 mots environ. Pas d'italique. Gras seulement sur les libellés. **Aucun émoji.**
- Étiquettes fixes, entre crochets, toujours en tête du titre du bloc : `[CRITIQUE]`, `[HAUTE]`, `[MOYENNE]`, `[BASSE]`, `[À VÉRIFIER]`.
- Tableaux de 3 colonnes au plus, cellules courtes.
- Ne jamais recopier une donnée personnelle réelle : la masquer (`j***@exemple.fr`).
- Ne jamais chiffrer une amende probable.

Le rapport commence après la ligne suivante.

---

# Audit RGPD — [nom du périmètre]

- **Date de référence :** [date]
- **Périmètre :** [sites, applications, outils]
- **Niveau d'accès :** [N1 public | N2 code et infrastructure | N3 organisation]
- **Auditeur :** [nom ou « Claude, analyse assistée »]

---

## 1. Verdict : [NON CONFORME — ACTION IMMÉDIATE | NON CONFORME — PLAN D'ACTION REQUIS | CONFORMITÉ PARTIELLE | AUCUN ÉCART CONSTATÉ SUR LE PÉRIMÈTRE]

[1 phrase : la raison principale.]

- **Risques critiques :** [n]
- **Risques hauts :** [n]
- **Risques moyens :** [n]
- **Risques bas :** [n]
- **Points à vérifier :** [n]

[Ne garder que les lignes dont le nombre n'est pas 0.]
[Si plus de la moitié des points sont à vérifier : « Verdict provisoire, audit incomplet. »]

**À faire en premier :**
1. [Action la plus urgente, 1 ligne.]
2. [Deuxième action.]
3. [Troisième action.]

[Si une fuite active est découverte : le dire ici, en premier, avec le rappel du délai de 72 h.]

---

## 2. Périmètre et méthode

- **Composants audités :** [liste courte]
- **Échantillon de pages :** [liste ou gabarits]
- **Tests réalisés :** [avant consentement, après refus, après acceptation, formulaires, courriels…]
- **Outils :** [navigateur piloté, récupération HTTP, lecture du code…]
- **Non autorisé ou non fait :** [tests actifs, entretiens…]

---

## 3. Cartographie

### Composants

| Composant | Données | Tiers |
|---|---|---|
| [Site vitrine] | [Visiteurs, contacts] | [Hébergeur UE] |

### Flux principaux

```
[Schéma en boîtes de texte : de la collecte à la suppression, avec chaque tiers et chaque sortie de l'UE.]
```

---

## 4. Risques

### R1 [CRITIQUE] [Titre court du risque]

- **Où :** [URL, composant, ou `fichier:ligne`]
- **Constat :** [ce qui se passe, 1 ou 2 lignes]
- **Preuve :** [requête, capture, extrait, date et heure]
- **Règle :** [article, 1 ligne]
- **Risque pour les personnes :** gravité [1-4], vraisemblance [1-4]. [Conséquence concrète, 1 ligne.]
- **Exposition :** [FORTE | MOYENNE | FAIBLE]. [Raison, 1 ligne.]
- **Correction :** [action concrète, 1 ou 2 lignes]
- **Délai :** [immédiat | 1 mois | 3 mois | au fil de l'eau]

### R2 [HAUTE] [Titre court]

[Même structure.]

### Points à vérifier

- **V1 [Titre court] :** [ce qui manque pour trancher, 1 ligne]. Niveau probable si confirmé : [HAUTE].

---

## 5. Points conformes

- **[Identifiant grille] [Titre court] :** [preuve en 1 ligne].

[Seulement les points vérifiés par une preuve. Les points déclarés mais non vérifiés vont en partie 4, « Points à vérifier ».]

---

## 6. Plan d'action

### Immédiat

- [ ] [Action] — risque R1

### Sous 1 mois

- [ ] [Action] — risque R2

### Sous 3 mois

- [ ] [Action] — risque R3

### Au fil de l'eau

- [ ] [Action] — risque R4

**Documents à produire :** [registre, politique de confidentialité, contrats…]. Le skill `rgpd` peut les rédiger.

---

## 7. Limites de l'audit

- [Ce qui n'a pas été contrôlé, et pourquoi.]
- [Les constats valent à la date de référence.]
- Cet audit est une analyse de conformité, pas un avis juridique. Pour un risque critique sur des données sensibles, un contentieux ou une sanction en cours, consulter un avocat ou un DPO.
