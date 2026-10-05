# Intégrer les mentions légales dans un site

La LCEN exige que les mentions soient « mises à disposition du public » et, pour le commerce électronique, **accessibles de façon facile, directe et permanente**, dans un **standard ouvert**. Traduction technique : une page HTML textuelle, liée depuis **toutes** les pages, lisible par tous (y compris lecteurs d'écran), avec un sommaire qui fonctionne.

## Sommaire

1. [Emplacement et accès](#1-emplacement-et-accès)
2. [Une seule source pour les informations de l'éditeur](#2-une-seule-source-pour-les-informations-de-léditeur)
3. [HTML sémantique et sommaire](#3-html-sémantique-et-sommaire)
4. [Exemple Next.js (App Router)](#4-exemple-nextjs-app-router)
5. [Autres environnements](#5-autres-environnements)
6. [Contrôles avant mise en ligne](#6-contrôles-avant-mise-en-ligne)
7. [Sources](#sources)

## 1. Emplacement et accès

- **URL** lisible et stable : `/mentions-legales`.
- **Lien « Mentions légales » dans le pied de page de toutes les pages**, à côté de « Politique de confidentialité », « Cookies » / « Gérer mes cookies », « CGV » / « CGU », « Accessibilité : … » selon le cas.
- Dans une **application mobile** : écran « Informations légales » accessible depuis le menu ou les réglages, et lien vers la version web.
- Page **indexable** en principe (pas d'obligation de `noindex`), accessible **sans connexion** ni consentement préalable, jamais masquée derrière le bandeau cookies.
- Pas de PDF ni d'image comme unique support.

## 2. Une seule source pour les informations de l'éditeur

Les mêmes données (dénomination, adresse, SIREN, e-mail) apparaissent dans le pied de page, les mentions légales, la politique de confidentialité, les CGV, parfois les données structurées (`Organization` en JSON-LD). Centralise-les dans **un fichier de configuration** unique, relu par tous ces endroits : une seule modification quand le siège ou le dirigeant change.

Dans un dépôt existant, **cherche d'abord** une configuration de ce type (`site.config.ts`, `siteConfig`, constantes de pied de page) avant d'en créer une.

## 3. HTML sémantique et sommaire

- Un seul `<h1>` (« Mentions légales »), puis un `<h2>` par section, avec un **`id` stable** sur chaque `<h2>` (voir les ancres recommandées dans `references/structure-et-redaction.md`).
- Le sommaire dans un **`<nav aria-label="Sommaire">`** contenant une **`<ol>`** de liens `href="#ancre"`.
- Date de mise à jour dans un élément `<time dateTime="2026-09-30">`.
- Identification en **liste de définitions** (`<dl>`, `<dt>`, `<dd>`) : sémantique et lisible.
- `scroll-margin-top` sur les titres si l'en-tête du site est fixe (sinon le titre ciblé passe sous l'en-tête).
- Liens `mailto:` et `tel:` ; liens externes explicites (pas de « cliquez ici »).
- Contraste et taille de texte normaux : ces pages sont souvent en gris clair minuscule, ce qui nuit à l'accessibilité.

## 4. Exemple Next.js (App Router)

Crée une **vraie route** `app/mentions-legales/page.tsx` (page statique). N'utilise pas de réécriture dans le proxy/middleware pour servir cette URL : une route réelle est plus simple et évite les effets de bord sur le préchargement côté client.

```ts
// config/editeur.ts — source unique des informations légales
export const editeur = {
  denomination: "[À COMPLÉTER : dénomination]",
  formeJuridique: "SAS",
  capital: "[À COMPLÉTER] €",
  siege: "[À COMPLÉTER : adresse du siège]",
  siren: "[À COMPLÉTER : 9 chiffres]",
  rcs: "RCS [À COMPLÉTER : ville du greffe]",
  tva: "[À COMPLÉTER : FR + 11 caractères]",
  telephone: "+33 [À COMPLÉTER]",
  email: "[À COMPLÉTER]@exemple.fr",
  directeurPublication: "[À COMPLÉTER : prénom nom], président",
  hebergeur: {
    nom: "[À COMPLÉTER : relevé sur la page légale de l'hébergeur]",
    adresse: "[À COMPLÉTER]",
    telephone: "[À COMPLÉTER]",
  },
  miseAJour: "2026-09-30",
} as const;
```

```tsx
// app/mentions-legales/page.tsx
import type { Metadata } from "next";
import Link from "next/link";
import { editeur } from "@/config/editeur";

export const metadata: Metadata = {
  title: "Mentions légales",
  description: `Informations légales sur l'éditeur et l'hébergeur du site ${editeur.denomination}.`,
};

const sections = [
  { id: "editeur", titre: "Éditeur du site" },
  { id: "directeur-publication", titre: "Directeur de la publication" },
  { id: "hebergement", titre: "Hébergement" },
  { id: "donnees-personnelles", titre: "Données personnelles" },
  { id: "cookies", titre: "Cookies" },
] as const;

const dateMaj = new Date(editeur.miseAJour).toLocaleDateString("fr-FR", {
  day: "numeric",
  month: "long",
  year: "numeric",
});

export default function MentionsLegalesPage() {
  return (
    <main className="mentions-legales">
      <h1>Mentions légales</h1>
      <p>
        Dernière mise à jour : <time dateTime={editeur.miseAJour}>{dateMaj}</time>
      </p>

      <nav aria-label="Sommaire">
        <h2 id="sommaire">Sommaire</h2>
        <ol>
          {sections.map((s) => (
            <li key={s.id}>
              <a href={`#${s.id}`}>{s.titre}</a>
            </li>
          ))}
        </ol>
      </nav>

      <section aria-labelledby="editeur">
        <h2 id="editeur">1. Éditeur du site</h2>
        <dl>
          <dt>Dénomination</dt>
          <dd>
            {editeur.denomination}, {editeur.formeJuridique} au capital de {editeur.capital}
          </dd>
          <dt>Siège social</dt>
          <dd>{editeur.siege}</dd>
          <dt>Immatriculation</dt>
          <dd>
            {editeur.siren} {editeur.rcs}
          </dd>
          <dt>TVA intracommunautaire</dt>
          <dd>{editeur.tva}</dd>
          <dt>Téléphone</dt>
          <dd>
            <a href={`tel:${editeur.telephone.replace(/\s/g, "")}`}>{editeur.telephone}</a>
          </dd>
          <dt>E-mail</dt>
          <dd>
            <a href={`mailto:${editeur.email}`}>{editeur.email}</a>
          </dd>
        </dl>
      </section>

      {/* 2. Directeur de la publication, 3. Hébergement : même principe */}

      <section aria-labelledby="donnees-personnelles">
        <h2 id="donnees-personnelles">4. Données personnelles</h2>
        <p>
          Le traitement de vos données est décrit dans notre{" "}
          <Link href="/politique-de-confidentialite">politique de confidentialité</Link>.
        </p>
      </section>

      {/* 5. Cookies : renvoi + lien « Gérer mes cookies » de l'outil de consentement */}
    </main>
  );
}
```

Points d'attention :
- La **numérotation** des titres doit correspondre à l'ordre du tableau `sections` : générer les deux depuis la même liste (ou numéroter avec une `<ol>` et du CSS) évite les décalages.
- `new Date("2026-09-30")` est interprété en UTC : en rendu statique c'est sans conséquence, mais pour éviter tout décalage d'un jour, on peut aussi stocker la date déjà formatée.
- Les liens d'ancre internes à la page restent de simples `<a href="#…">` ; `Link` sert pour les autres pages.
- Le lien « Gérer mes cookies » dépend de l'outil de consentement utilisé (fonction exposée par la CMP) : ne pas l'inventer, lire la documentation de l'outil présent dans le projet.
- Ajouter dans le composant de pied de page le lien vers `/mentions-legales` s'il manque.

## 5. Autres environnements

- **Markdown / MDX / CMS** : ancres explicites (`<a id="editeur"></a>` avant le titre, ou `{#editeur}` si le moteur le gère) ; vérifier que les liens du sommaire fonctionnent **dans le rendu final**, pas seulement dans l'éditeur.
- **WordPress, Shopify, Wix…** : utiliser la page légale native si elle existe, mais **relire son contenu** : les modèles fournis sont souvent génériques ou périmés (numéro CNIL, lien ODR). Ajouter le sommaire avec des ancres (bloc « Table des matières » ou liens manuels).
- **Application mobile** : liste de sections cliquables en tête d'écran ; ou lien vers la page web avec le sommaire.

## 6. Contrôles avant mise en ligne

- [ ] Chaque lien du sommaire mène à la bonne section (tester en cliquant, pas seulement en lisant le code).
- [ ] Le lien « Mentions légales » est présent dans le pied de page de toutes les pages, y compris tunnel de commande et pages d'erreur si elles ont un pied de page.
- [ ] Aucun `[À COMPLÉTER]` ne reste dans la page publiée (`grep` sur le dépôt).
- [ ] Les liens vers la politique de confidentialité, les cookies, les CGV/CGU, le médiateur et la déclaration d'accessibilité répondent (pas de 404).
- [ ] La page est lisible au clavier et au lecteur d'écran (ordre des titres, `nav` étiquetée).
- [ ] Les informations sont identiques partout (pied de page, CGV, politique de confidentialité, JSON-LD).

## Sources

- [LCEN, articles 1-1 et 19 — Légifrance](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000801164)
- [RGAA — Référentiel général d'amélioration de l'accessibilité](https://accessibilite.numerique.gouv.fr)
- [Next.js — Metadata et routage (App Router)](https://nextjs.org/docs/app)
