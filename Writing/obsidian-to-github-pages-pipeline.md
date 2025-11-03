---
title: "Obsidian → GitHub Pages: A Simple Publishing Pipeline"
summary: How I publish selected Markdown notes to a live website with validation and no backend.
publish: true
tags:
  - markdown
  - github-pages
  - automation
  - astro
  - publishing
updated: 2025-11-03
---

# Obsidian → GitHub Pages: A Simple Publishing Pipeline

This is the setup I use to turn selected Obsidian notes into a live website. It’s fast, transparent, and requires no backend.

---

## Goals

- Publish only notes I explicitly mark for release
- Prevent broken links and missing images
- Keep content readable and structured for Astro
- Automate enough to avoid manual copy/paste

---

## The Repos

- `mindpalace` (private): full Obsidian vault
- `public-mindpalace` (public): auto-mirrors only `/Public` content
- `lukas-nilsson.github.io` (public): Astro site that renders Markdown

---

## The Workflow

1. Write in Obsidian as normal.
2. Move a note into `/Public` when it’s ready.
3. Add frontmatter with `publish: true`.
4. Run one command to validate and publish:

```bash
/Users/lukasnilsson/Developer/mindpalace/System/push_public.sh
```

---

## Guardrails (What the script checks)

- `publish: true` gate – drafts are ignored automatically
- Obsidian links – converts `wikilinks` → standard Markdown
- Embeds – `image.png` → `![image](/Media/image.png)` and copies assets
- Broken links – publish fails if a link can’t be resolved
- Frontmatter – fills `title`/`updated` if missing

Result: the public repo only contains clean Markdown the website can consume.

---

## Website Integration (Astro)

- Content is included as a git submodule at `src/content/public`
- Astro content collections validate frontmatter during build
- Pages are static, so the site is fast and cheap to host

---

## Why This Works

- Plain files → easy to review, diff, and back up
- No vendor lock‑in → Markdown outlives tools
- Fail‑fast publishing → mistakes caught before they go live

If you’re technical and curious, the scripts are in `System/`. They’re small, readable, and designed to be extended.
