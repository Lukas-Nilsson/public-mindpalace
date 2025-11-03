---
title: Personal Website
summary: Rebuilding my personal website as a self-hosted, automated portfolio that documents itself.
publish: true
tags:
  - web-development
  - automation
  - portfolio
  - github
  - obsidian
  - ai
updated: 2025-11-03
---

# Personal Website

## Overview
This project involved rebuilding my personal website from the ground up as both a **portfolio** and a **publishing system**.  
It connects my private Obsidian vault (MindPalace) to a public GitHub repository, automatically syncing selected Markdown files that are tagged for publication.

The page you are reading now is part of that same system — a project entry published through the pipeline it describes.  
In total, this setup was completed in roughly **five hours** using **Cursor** and various **AI tools** to assist with planning, scripting, and copy generation.

---

## Objectives
- Create a **self-hosted personal website** with zero ongoing hosting cost.  
- Build a **public publishing workflow** between Obsidian and GitHub Pages.  
- Integrate **AI-assisted development** for speed, consistency, and automation.  
- Keep the final product **transparent** and version-controlled — a portfolio that documents its own creation.  

---

## Key Work

### Architecture
- Established a two-repository structure:
  - `mindpalace` – private Obsidian vault containing all notes and development files.  
  - `public-mindpalace` – public repository automatically updated with only tagged public Markdown files.
- Wrote a Bash script (`push_public.sh`) to sync `/Public` from the private vault into the public repo using `rsync` and `git`.  
- Verified that Obsidian, Git, and GitHub Pages all work together without a backend or server.

### Design & Content
- Designed a minimal **homepage hero** with the core line:  
  > “Lukas Nilsson — Coding humanity’s past into our future.”
- Defined folder structure for publishable content:
  - `/Public/Projects` – case studies and technical builds  
  - `/Public/Writing` – essays and reflections  
  - `/Public/About` and `/Public/Contact` – personal and professional info
- Created frontmatter standards (`title`, `summary`, `tags`, `publish`, `updated`) to ensure all Markdown files can be parsed consistently.

### Toolchain
- **Code & AI:** Built collaboratively using **Cursor** (AI-assisted IDE) and **ChatGPT** for rapid iteration.  
- **Hosting:** GitHub Pages  
- **Version Control:** Git + GitHub  
- **Scripting:** Bash automation  
- **Design:** Figma for layout concepts, AI image generation for visual direction.  

---

## Outcomes
- Built a **maintainable personal site** with integrated publishing from Obsidian.  
- Implemented a working example of **AI-assisted web development** — from file structure to launch.  
- Established a scalable format for documenting future projects directly on the site itself.  
- Created a professional framework that functions as both résumé and living archive.  

---

## Skills Demonstrated
- Static site architecture & automation scripting  
- Git/GitHub workflow and repository design  
- AI-assisted development using Cursor and ChatGPT  
- Markdown content management  
- Design thinking and personal brand integration  

---

## Next Steps
- Add a **GitHub Action** for scheduled publishing.  
- Integrate **Next.js** for a dynamic front-end experience.  
- Build an **AI agent** to summarize and index new public notes automatically.  

---

**Duration:** ~5 hours (planning, setup, and first deployment)  
**Repository:** [github.com/Lukas-Nilsson/public-mindpalace](https://github.com/Lukas-Nilsson/public-mindpalace)  
**Status:** Live and evolving
