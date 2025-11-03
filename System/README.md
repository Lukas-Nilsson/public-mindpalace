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

### Automatic Preparation

Before publishing, content is automatically processed:

1. **Gate Check** — Only files with `publish: true` are published
2. **Link Rewriting** — Obsidian `[[wikilinks]]` are converted to proper markdown links
3. **Media Handling** — Embedded images (`![[image.png]]`) are copied to `/Media` and paths updated
4. **Frontmatter Normalization** — Missing `title` or `updated` fields are auto-filled
5. **Link Validation** — Broken links cause publish to fail (prevents broken site)
6. **Preview Mode** — Files with `preview: true` get a "Work in progress" banner

### Frontmatter Requirements

Every `.md` file needs:

```yaml
title: "The Human Archives"
summary: "A living museum of humanity woven through time, design, and technology."
publish: true    # REQUIRED: Only files with this are published
tags: [project, public]
updated: 2025-11-03  # Auto-set during publish if missing
preview: false   # Optional: Adds "Work in progress" banner
```

### Using Obsidian Links

You can use Obsidian syntax in `/Public` — it gets automatically converted:

- `[[Note Name]]` → `[Note Name](/note-name/)`
- `[[Note#Section]]` → `[Note](/note-name/#section)`
- `[[Note|Custom Text]]` → `[Custom Text](/note-name/)`
- `![[image.png]]` → `![image](/Media/image.png)`

**Note:** Links to files that don't exist will cause publish to fail. This prevents broken links on your site.

---

## Safety & Privacy
- Anything outside `/Public` stays **private** by design.  
- Obsidian syntax (`[[links]]`, `![[images]]`) is fine — automatically converted during publish.  
- Place images in `/Public/Media/` or reference them from elsewhere (auto-copied during publish).  
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
