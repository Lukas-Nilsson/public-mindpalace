---
title: Personal Website
summary: Astro + GitHub Pages site with content synced from a public Obsidian vault.
publish: true
tags:
  - web-development
  - automation
  - portfolio
  - github
  - obsidian
updated: 2025-11-04
---

# Personal Website

A fast, static site built with Astro and deployed on GitHub Pages. Content is sourced from a separate public repository that mirrors selected notes from a private Obsidian vault.

---

## Architecture

- Repos: `mindpalace` (private) and `public-mindpalace` (public content)
- Sync: local scripts convert Obsidian markdown to web-ready content and push to the public repo
- Website: includes the public repo as a submodule and builds pages at deploy time

---

## Stack

- Framework: Astro v5 (static output)
- Deploy: GitHub Actions → GitHub Pages
- Content: Markdown with YAML frontmatter (title, summary, publish, tags, updated)
- Automation: `prepare_public.py` (sanitize links/media), `push_public.sh` (sync + submodule update)

---

## What’s done

- Content pipeline from `/Public` → `public-mindpalace` → website
- Dynamic routes for projects and writing
- Accessible, responsive layout with system fonts and minimal JS

---

## Why this approach

- Zero hosting cost; fully version-controlled
- Clear separation between private work and public pages
- Repeatable workflow: write → publish flag → sync → live

---

## Links

- Website: https://lukas-nilsson.github.io
- Content repo: https://github.com/Lukas-Nilsson/public-mindpalace
- Website repo: https://github.com/Lukas-Nilsson/lukas-nilsson.github.io
