# Public MindPalace

> A living, evolving public record of work, ideas, and projects — synced directly from my private Obsidian vault.

---

## What is this?

This repository contains the public-facing content from my personal knowledge base. It's automatically synced from my private vault, making it a real-time mirror of my thinking and work.

Think of it as:
- **A living portfolio** that updates itself
- **An open notebook** of ideas and projects
- **The public layer** of my MindPalace

Everything here is intentionally published — filtered, refined, and ready to share.

---

## Structure

- [`/About`](./About/) — Background, philosophy, and story
- [`/Projects`](./Projects/) — Portfolio pieces and creative works
- [`/Writing`](./Writing/) — Essays, reflections, and short pieces
- [`/Contact`](./Contact/) — Ways to connect
- [`index.md`](./index.md) — Homepage overview

---

## For Website Developers

This repository serves as the content source for my personal website (hosted via GitHub Pages). 

**Usage:**
- Fetch markdown files via GitHub's raw URLs
- Parse YAML frontmatter for metadata (title, summary, tags, dates)
- Render with any static site generator (Next.js, Astro, Hugo, etc.)

**Example:**
```javascript
// Fetch content dynamically
const content = await fetch(
  'https://raw.githubusercontent.com/Lukas-Nilsson/public-mindpalace/main/Projects/example.md'
).then(r => r.text());
```

**File Format:**
- Standard Markdown (`.md`)
- YAML frontmatter for metadata
- Relative links between files

---

## How It Works

This repo is **read-only from GitHub's perspective** — it's automatically synced from my private vault via a local script. I write and organize in my private Obsidian vault, and when content is ready, it flows here.

**The Pipeline:**
1. Content created in private Obsidian vault
2. Files moved to `/Public` folder when ready
3. Script syncs `/Public` → this GitHub repo
4. Website pulls from this repo to render pages

---

## Updates

This repository updates automatically when I publish new content. Check commit history to see what's new.

---

## License

Content is published here with the intent to share ideas openly. Feel free to reference, quote, or remix with attribution.

---

**Note:** This is a work in progress. Content evolves, structure refines, and new sections emerge over time. That's by design — it's meant to be a living archive.

---

*For more on the system behind this, see [`/System/README.md`](./System/README.md)*

