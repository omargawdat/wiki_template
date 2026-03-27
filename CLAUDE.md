# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

- `npm run dev` - Start development server (default: http://localhost:4321)
- `npm run build` - Build static site to `dist/`
- `npm run preview` - Preview built site

## Architecture

This is an **Astro** static site documentation starter template, using **Tailwind CSS** with dark mode support.

### Content System

Chapter content uses Astro's content collections:
- Markdown files go in `src/content/chapters/`
- Schema defined in `src/content/config.ts` requires: `title` (string), `chapter` (number), `order` (number), optional `description`
- Chapters are grouped by `chapter` number and sorted by `order` within groups

### Layout Structure

- `MainLayout.astro` - Base layout with header, sidebar navigation, and prose styling for markdown
- Navigation automatically generates from content collection, grouped by chapter number
- Dark mode uses Tailwind's `class` strategy, toggled via `ThemeToggle.astro` and persisted in localStorage

### Pages

- `/` - Home page listing all chapters grouped by number
- `/chapters/[slug]` - Dynamic chapter pages with prev/next navigation

### Styling

- Tailwind with custom `primary` color palette (sky blue tones)
- Global prose styles for markdown content defined in `MainLayout.astro`
- `ConceptCard.astro` provides styled callout boxes (types: definition, example, important, tip)
