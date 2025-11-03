---
title: "Secure Publishing: Scripts that Don’t Leak"
summary: How the pipeline avoids accidental leaks and broken pages when publishing Markdown.
publish: true
tags:
  - security
  - automation
  - github
  - validation
updated: 2025-11-03
---

# Secure Publishing: Scripts that Don’t Leak

Publishing should be deliberate. These are the safeguards built into the pipeline.

---

## Intentional Gate

- Only files with `publish: true` are included
- Drafts can live in `/Public` without going live

---

## Automatic Rewrites

- `wikilinks` → standard Markdown links
- `image.png` → `![alt](/Media/image.png)` with files copied

---

## Validation

- Broken links abort publishing
- Missing media is reported and blocks release
- Frontmatter is normalized and validated by Astro

---

## Repo Boundaries

- Private vault and public content are separate repos
- Website consumes public content via submodule
- No tokens committed; SSH used for pushes

Result: a predictable, reviewable publishing loop that favors safety.
