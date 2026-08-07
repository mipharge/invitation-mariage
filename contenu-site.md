# Serge & Ayano — Contenu du site d'invitation

Fête de mariage · Dimanche 16 août 2026 · Eus, Pyrénées-Orientales

**Site bilingue FR / EN.** Le français est la version par défaut ; un sélecteur
FR / EN en haut à droite bascule toute la page. Chaque texte anglais vit dans
un attribut `data-en` sur l'élément concerné ; le français est lu depuis le DOM
au chargement. `?lang=en` ouvre directement la version anglaise (lien
partageable). Pas de stockage local — le choix ne persiste pas d'une visite à
l'autre, seulement via l'URL.

Ordre du site : l'invitation et les infos pratiques (Programme) d'abord,
le contexte personnel (notre histoire) ensuite, puis l'album partagé à la
fin. Pas de section contact (tous les invités sont de la famille et ont
déjà nos coordonnées).

Aucune section n'a de sous-titre/kicker (retiré de partout, y compris du
sommaire) : seul le grand titre (« Programme », « Exposition »,
« Notre histoire », « Photos ») reste.

---

## 1. Accueil

**Serge & Ayano vous invitent**

Dimanche 16 août 2026
Eus, France

*Photo de couverture : nos mains / alliances, jour de notre mariage à Tokyo
(`title/20240701-DSC08056.jpg` → `site/images/mariage-mains.jpg`).*

---

## 2. Programme (Eus)

*Titre du chapitre : « Programme ». Pas de sous-titre.*

> Vous êtes invités à célébrer ce mariage.

Le 16 août 2026 à Eus, la cérémonie se tiendra sur la terrasse de notre
maison, suivie d'un dîner pour fêter notre mariage. Ce sera l'occasion de
réunir la famille Garrigue, et de découvrir le petit Henri pour la première
fois. Nous avons hâte de vous voir.

*Photo : nous deux, jour de notre mariage à Tokyo
(`title/20240701-DSC08040.jpg` → `site/images/mariage-nous.jpg`), juste après
le texte d'ouverture.*

**Dimanche 16 août 2026**
*(horaires encore à confirmer — mais la mention « Horaires indicatifs,
susceptibles d'évoluer d'ici l'été. » a été retirée du site, dans les deux
langues : la note ci-dessous est un rappel interne, pas du texte affiché.)*

| Heure | Moment | Lieu |
|-------|--------|------|
| 16h00 | Pre-reception *(inclut l'exposition photo)* | La Galerie de la Font — notre maison<br>2 Carrer de la Font, 66500 Eus |
| 18h00 | Cérémonie | À la maison<br>2 Carrer de la Font, 66500 Eus |
| 19h00 | Dîner | Un Xic de Tot<br>8 Carrer del Canigó, 66500 Eus |

Les deux adresses sont à deux minutes à pied l'une de l'autre.

Ne jamais écrire « vernissage » (l'exposition ne dure qu'un jour, le terme ne
convient pas) — toujours « Pre-reception », jamais « reception » seul, pour
que sa place dans la journée (avant cérémonie et dîner) reste claire.

### Tenue (sous-section de Programme, sans petit titre « Tenue » affiché)

> **Une tenue de fête, dans des couleurs claires et lumineuses.**
>
> Nous serions ravis de vous voir en couleurs vives ou pastel plutôt qu'en
> tons sombres. Le mois d'août est caniculaire à Eus, et les ruelles du
> village sont pavées et en pente : privilégiez surtout le confort.

*Pas de photo dans cette sous-section (retirée : jugée trompeuse). La phrase sur
les soirées fraîches en altitude a aussi été retirée.*

---

## 3. Exposition (fusion Exposition + Album)

*Titre du chapitre : « Exposition ». Pas de sous-titre.*

> Une année au Japon, accrochée aux murs d'une maison catalane.

Depuis la naissance d'Henri, nous photographions notre vie au Japon. Ces
images, réunies dans un album que nous avons appelé simplement *Henri*,
racontent une première année à Tokyo : les jours ordinaires, la maison, les
saisons, un enfant qui grandit loin d'ici.

Nous les exposons pour la première fois à la Galerie de la Font, dans notre
maison à Eus, le jour où Henri découvre la France. La Pre-reception ouvre la
journée à 16h — un verre, les photos, et le temps de se retrouver avant la
cérémonie.

*Photos entre le texte et les cartes PDF retirées (p19, p09, p22, p17, p25) —
la section passe directement du texte aux cartes. La ligne « Une année au
Japon / Avril — juillet 2026, Japon. » a aussi été retirée.*

Puis quatre cartes **Henri 1 / Henri 2 / Henri 3 / Henri 4** (remplacent l'ancienne
grille Album) : chaque carte = vignette + libellé, cliquer ouvre le PDF
correspondant dans un nouvel onglet (`site/pdfs/henri1.pdf` … `henri4.pdf`).
Pas d'aperçu PDF intégré. Empilées verticalement sur mobile, 2 colonnes à
partir de 768px, 4 à partir de 1200px. Vignettes = la couverture réelle de chaque PDF (extraite via
Quick Look, `sips -Z 1200`, → `site/images/henri1-cover.jpg` etc.).

Sous les quatre cartes, un bouton isolé, plus visible que les liens PDF
(pilule noire pleine, `.album-link.primary`) :

**Voir l'exposition** / *See the exhibition* → `exposition.html`

Le lien conserve la langue courante (`exposition.html?lang=en` en anglais),
via l'attribut `data-keep-lang` + `data-base` traité par le script de langue.
Il passe d'une page à l'autre en fondu (`data-page-fade`), comme les deux
liens de retour de la page exposition.

---

## 3 bis. Page « exposition.html » — l'exposition en ligne

Page séparée (`site/exposition.html`), même charte, même mécanique FR / EN,
même `?lang=en`. Elle reprend en ligne l'accrochage montré à la Galerie de la
Font le 16 août.

Introduction : titre **Henri**, période **13.06.2025 – 17.07.2026**, la ligne
« Exposition · La Galerie de la Font, Eus · 16.08.2026 », puis :

> Dix photographies, la première année d'Henri, entre Kyoto et Tokyo.
>
> *Ten photographs, Henri's first year, between Kyoto and Tokyo.*

Puis les dix planches, en une seule colonne, dans l'ordre. Chaque planche :
photo pleine largeur, puis numéro (01–10), titre, ligne date · heure · lieu
(identique dans les deux langues), et le texte. Sur mobile tout s'empile ;
à partir de 768px le bloc titre et le texte passent côte à côte, la photo est
centrée (1080px de large, 640px pour les deux verticales, 09 et 10).

| N° | Titre FR | Titre EN | Date · heure · lieu |
|----|----------|----------|---------------------|
| 01 | Henri, un jour | Henri, One Day Old | 14.06.2025, 18:42 · Adachi Hospital, Kyoto |
| 02 | Gion Matsuri, le matin de la procession | Gion Matsuri, the Morning of the Procession | 17.07.2025, 08:42 · Kyoto |
| 03 | Shinjuku Gyoen | Shinjuku Gyoen | 27.09.2025, 12:39 · Shinjuku Gyoen, Tokyo |
| 04 | Cent jours | One Hundred Days | 21.09.2025, 14:00 · Asagaya, Tokyo |
| 05 | Les kochias du parc Showa Kinen | Kochia at Showa Kinen Park | 13.10.2025, 16:04 · Showa Kinen Park, Tachikawa, Tokyo |
| 06 | La plage de Zushi | Zushi Beach | 03.11.2025, 16:31 · Zushi Beach, Kanagawa |
| 07 | La fin de l'année en famille | The End of the Year, with Family | 28.12.2025, 19:30 · Tourouyama-cho, Kyoto |
| 08 | Les pruniers du parc Koganei | Plum Blossoms, Koganei Park | 21.02.2026, 14:57 · Koganei Park, Tokyo |
| 09 | Le premier anniversaire | First Birthday | 13.06.2026, 18:57 · Itabashi, Tokyo |
| 10 | Gion Matsuri, un an plus tard | Gion Matsuri, One Year Later | 17.07.2026, 08:18 · Tourouyama, Gion Matsuri, Kyoto |

Les textes complets (FR et EN) sont dans la page elle-même : le français dans
le DOM, l'anglais dans le `data-en` du paragraphe. Seul le titre 03
(« Shinjuku Gyoen ») est identique dans les deux langues, donc sans `data-en`.

Photos : `site/images/expo/01.jpg` … `10.jpg` (originaux dans `exhibition/`,
non versionné, réduits à 2000px de long côté avec `sips`, chacun sous 500 Ko).
09 et 10 sont verticales, les huit autres horizontales. `loading="lazy"`,
`width` / `height` sur chaque `<img>` pour éviter le décalage de mise en page.

Retour vers l'invitation à deux endroits : un petit lien « ← Retour à
l'invitation » en haut, et le bouton plein « Retour à l'invitation » en bas,
sous la signature Serge & Ayano. Les deux gardent la langue courante.

`og:image` de la page : `images/expo/06.jpg` (la plage de Zushi).

---

## 4. Notre histoire

*Titre du chapitre : « Notre histoire ». Pas de sous-titre.*

Frise photo à révéler au tap, 8 étapes chronologiques (les naissances des
deux, puis la rencontre jusqu'à la fête). Pas de légende permanente sur la
photo : un tap superpose « lieu · mois/année » + le texte, tout est masqué
tant qu'on n'a pas touché la photo. Toutes les photos sont fournies (dossier
`notre histoire/`, redimensionnées dans `site/images/histoire-*.jpg`).

Paragraphe d'intro, juste après le label de section :

> Nous nous sommes rencontrés à Kyoto en 2020. Depuis six ans, nous avons
> vécu ensemble au Japon, entre Kyoto et Tokyo. Nous serions heureux de
> retrouver notre famille en France.

Copie exacte des étapes (à ne pas reformuler), toutes dans la même mise en
page (1 colonne sur mobile, 2 à partir de 768px, comme le reste de la frise) :

Tout est au passé composé, sauf la dernière étape (août 2026) qui n'a pas
encore eu lieu et reste au présent.

0. **Osaka · Août 1997** — Ayano est née à Chihaya Akasaka, un village dans la montagne, au sud d'Osaka.
0. **Kyoto · Juillet 1998** — Serge est né à Nakagyō-ku, au centre de Kyoto.
1. **Kyoto · Mai 2020** — Nous nous sommes rencontrés à Kyoto, au printemps 2020. Depuis, nous avons voyagé dans beaucoup d'endroits ensemble.
2. **France · Août 2023** — Notre premier voyage en France ensemble. Ayano a découvert l'autre pays d'origine de Serge.
3. **Tokyo · Mars 2024** — Serge et Ayano ont tous les deux trouvé un travail à Tokyo. Nous avons quitté Kyoto et nous nous sommes installés à Suginami.
4. **Tokyo · Juillet 2024** — Nous nous sommes mariés à Tokyo.
5. **Kyoto · Juin 2025** — Henri est né à Kyoto. Peu après, il est venu vivre avec nous à Tokyo.
6. **Eus · Août 2026** — Nous rentrons en France avec Henri, et nous célébrons enfin notre mariage avec vous, à Eus.

Photos : `notre histoire/osaka aout 1997.jpg`, `kyoto juillet 1998.jpg`,
`kyoto mai 2020.jpg`, `france aout 2023.jpg`, `tokyo avril 2024.jpg`,
`tokyo juillet 2024.jpg`, `kyoto juin 2025.jpg`, `eus aout 2026.jpg` →
`site/images/histoire-*.jpg` (toutes fournies, aucun placeholder restant).

Photo d'ouverture du chapitre : `site/images/expo/10.jpg` — la photographie 10
de l'exposition (Gion Matsuri 2026, tous les trois devant le char du
Tourouyama). Elle est verticale, donc les visages restent bas dans le cadrage
plein écran, loin du titre « Notre histoire » posé en haut à gauche
(`object-position:50% 80%` pour garder la famille dans le champ sur écran large).

Toutes les photos de la section (l'ouverture de chapitre comprise) sont
affichées en noir et blanc, via `filter:grayscale(1)` en CSS — les fichiers
sources restent en couleur.

---

## 5. Photos (album partagé)

*Titre du chapitre : « Photos ». Pas de sous-titre. Dernière section, juste
avant le pied de page.*

> Partagez vos photos de la journée.

Nous avons créé un album partagé pour rassembler au même endroit les photos
du 16 août. Ajoutez les vôtres pendant ou après la journée, et venez voir
celles des autres.

Bouton : **Ouvrir l'album partagé** → https://photos.app.goo.gl/TY5worfLbMvZA8ry5
(`target="_blank" rel="noopener"`, style `.album-link`).

*Le lien est public, comme le reste du site : toute personne qui trouve le
site peut ouvrir l'album.*

---

## Points encore ouverts

- [ ] Confirmation des horaires
