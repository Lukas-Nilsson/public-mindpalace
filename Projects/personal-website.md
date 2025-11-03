---
title: Personal Website
summary: A GitHub-hosted personal portfolio and publishing system connected to my Obsidian knowledge base.
publish: true
tags: ""
updated: 2025-11-03
---

# Personal Website

## Overview
This project involved rebuilding my personal website to act as both a portfolio and a public publishing system.  
It connects my private Obsidian vault to a public GitHub repository, automatically syncing selected Markdown files that are tagged for publication.

The result is a professional, self-maintained website that showcases my work, writing, and projects using an efficient, developer-friendly workflow.

---

## Objectives
- Create a **modern personal website** hosted on GitHub Pages with no ongoing hosting costs.  
- Develop a **public publishing pipeline** from Obsidian to GitHub using a simple automation script.  
- Build a **portfolio framework** that reflects both design and technical skills.  
- Maintain **clear separation** between private and public data.  

---

## Key Work
### Architecture
- Set up a **two-repo system**:
  - `mindpalace` (private): full Obsidian vault.  
  - `public-mindpalace` (public): contains only Markdown files marked as publishable.  
- Implemented a **sync script** (`push_public.sh`) using `rsync` and Git to mirror `/Public` content into the public repo.
- Ensured reliable publishing from local edits to live site via a single command.

### Design & Content
- Built a **minimal homepage** featuring personal identity, tagline, and featured work.  
- Structured `/Public` folder into clear categories:
  - `/Projects` – portfolio case studies  
  - `/Writing` – essays and notes  
  - `/About` and `/Contact` – background and links
- Defined Markdown frontmatter standards (`title`, `summary`, `publish`, `updated`).

### Technology
- **Hosting:** GitHub Pages (static)  
- **Version Control:** Git + GitHub  
- **Scripting:** Bash automation  
- **Design Tools:** Figma for layout concepts, image generation for hero visuals  
- **Future Integration:** Next.js or Astro for dynamic builds  

---

## Outcomes
- Created a **fully version-controlled personal website** that requires no backend or CMS.  
- Simplified the process of **publishing content directly from Obsidian**.  
- Improved content organization through clear folder and tag systems.  
- Reduced maintenance cost and dependency on third-party tools.  

---

## Skills Demonstrated
- Front-end architecture & static site deployment  
- Git/GitHub workflow and automation scripting  
- Markdown-based content management  
- Design systems thinking and typography  
- Data privacy and repo management  

---

## Next Steps
- Implement a **GitHub Action** for automatic syncing.  
- Add an **AI summarization layer** for new public notes.  
- Migrate visual design to **Next.js** for better scalability and performance.  

---

**Repository:** [github.com/Lukas-Nilsson/public-mindpalace](https://github.com/Lukas-Nilsson/public-mindpalace)  
**Status:** In active development
