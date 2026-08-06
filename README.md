# Portfolio

Persoonlijke portfolio- en blogsite, gebouwd met **Astro 7**. Blogposts staan als lokale Markdown/MDX in de repo — geen extern CMS.

## Stack

- Astro 7 (static)
- Content Collections (`src/content/blog/`)
- MDX, RSS, sitemap
- Node ≥ 22.12

## Structuur

```text
src/
  content/
    blog/              # Markdown/MDX-posts
  content.config.ts    # Collection-schema
  pages/
    index.astro
    blog/              # Lijst + [...id]
  components/
  layouts/
  styles/
public/
  fonts/               # o.a. Basteleur (nog niet aangesloten)
```

## Commands

| Command | Actie |
| --- | --- |
| `npm install` | Dependencies installeren |
| `npm run dev` | Dev-server op `localhost:4321` |
| `npm run build` | Productiebuild naar `./dist/` |
| `npm run preview` | Build lokaal previewen |

## Blogpost toevoegen

1. Maak een bestand in `src/content/blog/`, bijvoorbeeld `mijn-post.md`.
2. Vul frontmatter volgens het schema in `src/content.config.ts`:

```md
---
title: 'Mijn post'
description: 'Korte samenvatting'
pubDate: 2026-08-06
# updatedDate: 2026-08-07
# heroImage: ../../assets/blog-placeholder-1.jpg
---

Inhoud in Markdown…
```

De slug volgt uit de bestandsnaam (`mijn-post` → `/blog/mijn-post`).

## Opmerkingen

- Soft-reset vanaf de eerdere Astro 6 + Directus-opzet: content leeft nu in de repo.
- Site-URL staat nog op `https://example.com` in `astro.config.mjs` — pas aan bij deploy.
- Displayfont Basteleur ligt in `public/fonts/` voor latere styling.
