# Project Guidelines

## Overview

BYU-Idaho WDD 236 course site built with Astro. Static content delivery with interactive bakeoff/peer-review features backed by Supabase. Prioritize content authoring over framework refactors unless explicitly requested.

## Tech Stack

- **Framework:** Astro 6 with content collections (glob-based loaders) and static routes
- **Content:** Markdown and MDX under `src/content`
- **Interactive UI:** Svelte 5 + Supabase (bakeoff and peer-review pages only)
- **Package Manager:** pnpm

## Commands

- `pnpm dev` — local dev server
- `pnpm build` — static build (run after content changes to validate)
- `pnpm preview` — preview production build locally

No lint, test, or typecheck scripts are configured. Validate by building.

## Content Collections

`src/content.config.ts` is the source of truth. Five collections, all using glob loaders (no Zod schemas):

| Collection | Route             | Folder                  |
| ---------- | ----------------- | ----------------------- |
| prepare    | `/prepare/[id]`   | `src/content/prepare`   |
| prove      | `/prove/[id]`     | `src/content/prove`     |
| ponder     | `/ponder/[id]`    | `src/content/ponder`    |
| resources  | `/resources/[id]` | `src/content/resources` |
| units      | `/units/[id]`     | `src/content/units`     |

Route `id` = filename without extension. Legacy `src/content/config-old.ts` exists — do not add new schema there.

## Frontmatter by Collection

### prepare / prove

- `title`: string (required)
- `time`: string (required)
- `aiUsage`: `green` | `yellow` | `red` (strongly recommended)
- `description`: string (optional)

### ponder

- `title`: string (required)
- `description`: string (required for index summaries)
- `time`: string (recommended)
- `aiUsage`: `green` | `yellow` | `red` (strongly recommended)
- `tags`: string[] (optional)

### resources

- `title`: string (required)
- `description`: string (required for index summaries)
- `time`: string (recommended)
- `aiUsage`: `green` | `yellow` | `red` (optional)

### units

- `title`: string (required)
- `summary`: string (required)
- `tags`: string[] (required)
- `slug`: string (required) — keep equal to filename id to avoid routing mismatches

## MDX Components

Import with relative paths from content files:

- `AIUsage` — `../../components/AIUsage.astro`
- `Details` — `../../components/Details.astro`
- `Figure` — `../../components/Figure.astro`
- `Video` — `../../components/Video.astro`

## Internal Linking

- From units files to activities: `../../prepare/unit1a`
- Between sibling content files: relative paths without extensions
- Prefer links matching collection route ids

## Supabase (Bakeoff / Peer Review)

Interactive pages under `src/pages/bakeoff/` and `src/pages/peer-review/` use Supabase. Client in `src/lib/supabase.ts` requires `PUBLIC_SUPABASE_URL` and `PUBLIC_SUPABASE_ANON_KEY` from `.env` (gitignored, present in repo root). Svelte components live under `src/components/bakeoff/` and `src/components/peer-review/`. Do not modify these pages unless explicitly requested.

## Do Not Modify Unless Requested

- Global styling and layout structure
- Header navigation
- Svelte app pages (bakeoff, peer-review)
- Site metadata
- `types.mts` (product/user/order schemas for the bakeoff app)

## Validation

After adding or modifying content:

1. Frontmatter keys match collection expectations
2. Filename id and unit slug are consistent
3. All internal links resolve logically
4. Run `pnpm build` and fix any content or route errors

## Authoring Guidance

Review `docs/course-authoring-notes.md` before writing new content — it covers voice, activity patterns, component usage, and learning outcome alignment.

## Instruction Sources

- `.github/copilot-instructions.md` — duplicate of this file (keep in sync)
- `docs/course-authoring-notes.md` — pedagogical patterns and voice guide
