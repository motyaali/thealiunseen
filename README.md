# The Ali Unseen

Source repository for **TheAliUnseen.com**, an independent publication and creative technology site exploring human experience, artificial intelligence, systems, learning, creativity, and lived experience.

## Stack

- Astro static site generator
- Markdown for long-form writing
- GitHub Actions for builds and deployment
- GitHub Pages for hosting
- Custom domain: `www.thealiunseen.com`

## Local development

```bash
npm install
npm run dev
```

Then open the local URL shown by Astro.

## Build

```bash
npm run build
```

The production site is generated in `dist/`.

## Site sections

- Home
- Writing
- Projects
- About
- Watch
- Support

## Publishing a new article

Create a Markdown file in `src/pages/writing/` with frontmatter like:

```yaml
---
layout: ../../layouts/ArticleLayout.astro
title: Article title
description: One-sentence summary.
date: 2026-09-06
tags:
  - Human + AI
---
```

The writing index discovers Markdown articles automatically.

## Deployment

The GitHub Actions workflow builds and deploys the site from `main`. GitHub Pages must be configured to use **GitHub Actions** as its publishing source.

The custom domain is intentionally kept separate from email routing. Website DNS can point to GitHub Pages while MX and related email records point to the selected email provider.
