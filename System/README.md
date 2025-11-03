# Public MindPalace

## Purpose
This folder contains all public-facing material for my personal website — a living portfolio and open extension of my private vault.  
It mirrors selected notes, essays, and projects that I’ve intentionally made public.  
The private vault remains my full MindPalace; this is its visible layer.

The idea: **a two-layer system**  
- **Private vault** → full creative, reflective, and experimental workspace.  
- **Public vault (/Public)** → carefully chosen files meant for sharing and publishing.  

Automation or an AI agent syncs this folder to  
[`public-mindpalace`](https://github.com/Lukas-Nilsson/public-mindpalace),  
which powers my website and public profile.

---

## Structure
```
/Public
│
├── index.md          → homepage overview (bio, main links)
├── About/            → background, philosophy, story
├── Projects/         → portfolio and creative works
├── Writing/          → essays, reflections, short pieces
├── Media/            → approved images or graphics
├── Contact/          → ways to reach me
└── System/           → meta files like this README
```

---

## Publishing Logic
1. Files inside `/Public` are considered *safe and intentional for publishing*.  
2. Every `.md` file starts with frontmatter metadata:  
   ```yaml
   title: "The Human Archives"
   summary: "A living museum of humanity woven through time, design, and technology."
   publish: true
   tags: [project, public]
   updated: 2025-11-03
   ```
3. Files marked `publish: true` are mirrored to the public GitHub repo.  
4. Files without that flag remain local (drafts) even if they’re in `/Public`.

---

## Safety & Privacy
- Anything outside `/Public` stays **private** by design.  
- Avoid Obsidian-only syntax like `[[links]]`; use relative Markdown links (`[About](../About/)`).  
- Place images only in `/Public/Media/`.  
- Check frontmatter for hidden or sensitive metadata before syncing.  
- The sync script excludes large assets (videos, raw exports, etc.).  
- If a mistake occurs, history in the public repo can be rewritten safely with `git filter-repo`.

---

## Meta Design: Two Worlds, One Source
This structure separates thinking from presentation.  
The private vault evolves freely. The public layer extracts only what’s mature enough to represent the work.  
Over time, this creates:
- A **living portfolio** that updates itself.  
- A **traceable intellectual history** where notes become essays, and essays become projects.  
- A **bridge** between inner work (ideas) and outer work (impact).

---

## Future Extensions
- Automated sync agent to check for `publish: true` and push updates nightly.  
- AI-generated summaries for new posts.  
- Dynamic site index or tag cloud built from this folder.  
- Public “Now” page reflecting current focus.  
- Visual graph view connecting all published pages.

---

**Intent:**  
To create a transparent, evolving public version of my MindPalace —  
a place where private thinking gradually crystallizes into public knowledge.
