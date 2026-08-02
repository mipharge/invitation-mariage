# Site d'invitation — Serge & Ayano

Site web d'invitation pour la fête de mariage de Serge & Ayano Garrigue.
Une page statique, en français, sans dépendance ni build.

## Contexte

- **Rencontre** : à Kyoto, au printemps 2020.
- Six ans vécus ensemble au Japon, entre Kyoto et Tokyo (installation à Suginami, Tokyo, en mars 2024).
- **Mariage** : célébré à Tokyo le **7 juillet 2024**, sans fête ni invités.
- **Henri** : leur fils, né à Kyoto le **13 juin 2025**. Il découvre la France pour la première fois.
- **La fête** : **dimanche 16 août 2026**, à **Eus** (66500, Pyrénées-Orientales).

## Programme du 16 août 2026

*(horaires indicatifs, susceptibles d'évoluer)*

| Heure | Moment | Lieu |
|-------|--------|------|
| 16h00 | Pre-reception *(inclut l'exposition photo)* | La Galerie de la Font — leur maison, 2 Carrer de la Font, 66500 Eus |
| 18h00 | Cérémonie | À la maison, même adresse |
| 19h00 | Dîner | Un Xic de Tot, 8 Carrer del Canigó, 66500 Eus |

Les deux adresses sont à deux minutes à pied l'une de l'autre, dans un village escarpé et pavé.

**Jamais « vernissage »** — l'exposition ne dure qu'un jour, le terme ne convient pas.
Toujours **« Pre-reception »**, jamais « reception » seul, pour que sa place dans la
journée (avant cérémonie et dîner) reste claire.

## Exposition « Henri »

La Pre-reception de 16h inclut, dans un coin de la Galerie de la Font, une exposition
de photos de l'album familial *Henri* — la vie du couple au Japon depuis la naissance
de leur fils. Première exposition de ces images, le jour où Henri arrive en France.
Ce n'est pas un événement à part : elle a lieu à l'intérieur de la Pre-reception.

Le site présente aussi trois cartes **Henri 1 / Henri 2 / Henri 3**, qui ouvrent chacune
un PDF (l'album complet de chaque édition) dans un nouvel onglet.

Référence de style du site : `HENRI 3 Best.pdf` (82 pages, album Pages/A4) — *non versionné, 406 Mo*.

## Tenue

> **Une tenue de fête, dans des couleurs claires et lumineuses.**
>
> Nous serions ravis de vous voir en couleurs vives ou pastel plutôt qu'en
> tons sombres. Le mois d'août est caniculaire à Eus, et les ruelles du
> village sont pavées et en pente : privilégiez surtout le confort.

Ton voulu : fête colorée, tenue facile à porter — pas de registre « chic »,
pas de détail de matière (lin, etc.), pas de consigne « éviter le noir »
dans le titre (ni la couleur noire n'est mentionnée du tout).

## Décisions prises

- **Bilingue français / anglais** (pas de version japonaise). Le français reste la
  version par défaut ; un sélecteur FR / EN en haut à droite bascule toute la page.
  *(Remplace la décision initiale « français uniquement ».)*
- **Pas de section** infos pratiques / transport / hébergement — les invités connaissent la région.
- **Pas de section** cadeaux ni liste de mariage.
- **Pas de section contact/RSVP sur le site** — tous les invités sont de la famille et ont
  déjà les coordonnées de Serge (téléphone, email, Instagram).
- **Pas de sous-titre/kicker** sur les sections ni dans le sommaire — seul le grand titre reste.

## Charte graphique

Reprise de l'album *HENRI* : mise en page éditoriale, papier blanc, encre noire.

- **Typographie** : Gilda Display (Google Fonts), serif élégant et plus lisible que le Bodoni Moda initial.
  Une seule graisse disponible (400, pas d'italique) : gras et italiques sont synthétisés par le navigateur.
  Fallbacks : Playfair Display, Didot, Georgia.
- **Titres** : capitales, très grands, interlettrage léger, graisse 700 (synthétisée).
- **Dates et légendes** : 10–11 px, capitales, interlettrage large (`.18em`), gris (`--ink-soft`).
- **Couverture** : photo plein écran, titre en blanc en haut à gauche, date en haut à droite.
- **Ouvertures de chapitre** : soit photo plein écran avec titre blanc superposé,
  soit page blanche avec titre noir (variante `.opener-plain`).
- **Beaucoup de blanc.** Photos parfois à 46–62 % de largeur, jamais toutes pleine page.
- Numéros de page discrets en bas à droite (`.folio`).
- Apparition en fondu au scroll via IntersectionObserver (classe `.rv` → `.in`).
- Respecte `prefers-reduced-motion`.

## Structure du site

```
site/
├── index.html        # tout : HTML + CSS + JS dans un seul fichier
├── images/           # photos optimisées (max 2000 px, qualité 82)
└── pdfs/              # henri1.pdf, henri2.pdf, henri3.pdf
```

Chapitres, dans l'ordre — l'invitation et les infos pratiques d'abord,
le contexte personnel à la fin :

1. **Programme** — Eus : lettre d'invitation, horaires, tenue (`#eus`, la tenue est une sous-section)
2. **Exposition** — Henri + Album fusionnés : texte, puis cartes PDF Henri 1/2/3 (`#henri`)
3. **Notre histoire** — frise photo à tap-to-reveal, 8 étapes chronologiques (`#tokyo`).
   Toutes les photos de la section sont en noir et blanc (`filter:grayscale(1)`).
4. **Photos** — album Google Photos partagé pour que les invités déposent leurs
   photos de la journée (`#photos`), lien externe en `target="_blank" rel="noopener"`.

Pas de sous-titre/kicker : seul le grand titre reste sur chaque section et dans le sommaire.

Précédés de la couverture et d'un sommaire (`#sommaire`) inspiré de la page 3 de l'album.

## Fichiers du dossier

- `CLAUDE.md` — ce fichier
- `contenu-site.md` — tous les textes, validés par Serge
- `site/index.html` — le site
- `site/images/` — photos optimisées
- `site/pdfs/` — henri1.pdf, henri2.pdf, henri3.pdf (copiés/renommés depuis `pdfs/HENRI 1.pdf` etc.)
- `pdfs/` — PDFs originaux (`HENRI 1.pdf`, `HENRI 2.pdf`, `HENRI 3.pdf`) *(non versionné à la racine)*
- `photos/`, `title/`, `notre histoire/` — photos originales non retouchées *(non versionnées, plusieurs Go)*
- `HENRI 3 Best.pdf` — l'album, référence de style *(non versionné, 406 Mo)*

## Reste à faire

- [x] ~~Photos de la frise « Notre histoire »~~ — les 8 étapes ont leur photo (`site/images/histoire-*.jpg`).
- [ ] **Confirmer les horaires** définitifs.

## Conventions

- Pas de framework, pas de build, pas de npm. Un seul fichier HTML avec `<style>` et `<script>` inline.
- Mobile-first : les media queries partent de 768 px puis 1200 px.
- Marges gérées par la variable CSS `--mar` (24 px → 56 px → 88 px).
- Ne pas utiliser `localStorage` ni `sessionStorage`.
- **Traductions** : chaque texte anglais vit dans un attribut `data-en` sur l'élément
  qui le porte ; le français est lu depuis le DOM au chargement (`data-fr` généré en JS).
  Le HTML inline (`<br>`, `<em>`, liens) est permis dans `data-en` — échapper les
  guillemets doubles en `&quot;`. Toute nouvelle phrase ajoutée au site a besoin de
  son `data-en`, sinon elle restera en français en mode EN.
- Images : `loading="lazy"` partout sauf la couverture.
- Textes : toujours répercuter les modifications dans `contenu-site.md`.
