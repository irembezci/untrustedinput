# untrustedinput

A personal blog about AI Security, AI Red Teaming, and AI bug bounty research. The main blog is in English. A separate Turkish-language newsletter will share shorter updates and notes.

## Site structure

- The home page lists English articles, newest first.
- Topic categories and article types filter the article list.
- Article pages have a collapsible AI Security topic tree on the left.
- The article sidebar starts with the four latest English publications. Each title links directly to its article and updates automatically from `_posts/`.
- Below recent publications, the `AI Red Teaming` label heads the `AI Security` category tree.
- `_data/navigation.yml` defines the topic tree. Add a top-level category as a new `title`, and add subtopics under its `topics` list. Add a `url` when a topic should link to a published article.
- Turkish newsletter posts appear separately at `/newsletter/` and are excluded from the English home page.

## Add an English article on GitHub

Create a file in `_posts/` using the format `YYYY-MM-DD-short-title.md`, for example `2026-10-23-rag-security-notes.md`.

```yaml
---
title: RAG Security Notes
date: 2026-10-23 12:00:00 +0300
language: en
category: AI Agents
type: Tutorial
author: Your name
description: A short summary of the article.
tags: [RAG, AI Security]
---

Opening paragraph.

## First section

Article text...
```

Use `News`, `Tutorial`, `Finding`, `Review`, or `Explainer` for `type`. An `Explainer` is a clear, accessible article that explains a concept or technique. The article date controls its position in the feed. Add the topic to `_data/navigation.yml` when appropriate.

## Add a Turkish newsletter issue

Create another dated Markdown file in `_posts/`, then set `language: tr` and `type: Newsletter` in its front matter. It will appear on the Turkish Newsletter page, separate from the English blog feed. Keep technical terms in English if that suits the issue.

```yaml
---
title: AI Security'den bu haftanın notları
date: 2026-10-23 12:00:00 +0300
language: tr
category: Haftalık Notlar
type: Newsletter
description: Bu sayının kısa özeti.
---

Türkçe bülten içeriği...
```

## Publish with GitHub Pages

Upload the contents of this folder to the root of your GitHub repository. In **Settings → Pages**, select **Deploy from a branch**, `main`, and `/ (root)`. GitHub Pages will build the Jekyll site automatically.

## Key files

- `_posts/` — English blog articles and Turkish newsletter issues
- `_data/navigation.yml` — collapsible AI Security topic tree
- `_layouts/` — page and article templates
- `_config.yml` — Jekyll settings
- `styles.css` — dark theme and responsive layout
- `newsletter.md` — Turkish Newsletter landing page
- `about.md` — About page
