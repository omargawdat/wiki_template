---
title: "Getting Started"
chapter: 1
order: 1
description: "A sample chapter to demonstrate the template"
---

## Welcome

This is a sample chapter. Add your own content by creating markdown files in `src/content/chapters/`.

Each chapter file needs frontmatter with:

- **title** — displayed in the sidebar and page header
- **chapter** — number used for grouping in navigation
- **order** — controls sort order within a chapter group
- **description** (optional) — shown on the overview page

## Using Concept Cards

You can use the `ConceptCard` component for callouts:

```astro
<ConceptCard type="definition" title="My Term">
  Your definition here.
</ConceptCard>
```

Available types: `definition`, `example`, `important`, `tip`.
