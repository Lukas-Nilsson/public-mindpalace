---
title: "Astro Content Collections: Structuring Markdown for a Portfolio"
summary: A practical guide to validating and routing Markdown pages with Astro content collections.
publish: true
tags:
  - astro
  - content
  - markdown
  - portfolio
updated: 2025-11-03
---

# Astro Content Collections: Structuring Markdown for a Portfolio

This site uses Astro’s content collections to turn Markdown files into reliable pages.

---

## Why Content Collections

- Validate frontmatter at build time (catch mistakes early)
- Define a single schema for all notes
- Keep routes clean and predictable

---

## Minimal Setup

`src/content/config.ts`:

```ts
import { defineCollection, z } from 'astro:content';

const publicCollection = defineCollection({
  type: 'content',
  schema: ({ image }) => z.object({
    title: z.string().optional(),
    summary: z.string().optional(),
    publish: z.boolean().default(false),
    tags: z.array(z.string()).optional(),
    updated: z.date().or(z.string()).optional(),
  }),
});

export const collections = {
  public: publicCollection,
};
```

---

## Querying Content

List all projects that are marked `publish: true`:

```tsx
const allProjects = await getCollection('public', (entry) => {
  return entry.id.startsWith('Projects/') &&
         !entry.id.includes('index.md') &&
         entry.data.publish === true;
});
```

This powers `/projects` and individual project pages.

---

## Conventions

- Folder → route mapping: `Projects/the-human-archives.md` → `/projects/the-human-archives`
- `index.md` in a folder → `/about`, `/writing`, `/contact`
- Frontmatter uses YAML lists (e.g. `tags:` followed by `- tag`)

---

## Result

- Clean URLs
- Predictable structure
- Safer builds (invalid content fails early)
