# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

## PrimeIntel — Business Intelligence & Research Website

**Artifact:** `artifacts/primeintel` | Preview path: `/`

A dark-mode, cinematic single-page business intelligence site built with React + Vite.

### Design
- Background: `#05070A` (deep near-black) with cobalt blue (`#0047AB`) accent
- Typography: Inter, ultra-tracked uppercase headings
- Faint dot-grid background pattern
- Glassmorphism card effects
- Cobalt pulse animation on CTA buttons

### Pages
- `/` — **Home**: Hero with cycling text animation, Service Intelligence accordion section (4 expandable panels with cobalt glow on open), CTA strip
- `/about` — **About Us**: Mission layout with stats grid (150+, 24h, 98%, $500), three pillars (Research / Policy / UX)
- `/blog` — **The Briefing Room**: Featured article card + 3-column article grid
- `/contact` — **Discovery Briefing Form**: Business info, email, research goals textarea, Standard/Expedited timeline toggle, sidebar trust signals

### Key Components
- `src/components/Nav.tsx` — Sticky header with active-link highlighting, mobile hamburger overlay
- `src/pages/HomePage.tsx` — Hero + service accordion with Framer Motion
- `src/pages/AboutPage.tsx` — Mission + stats + three pillars
- `src/pages/BlogPage.tsx` — Article grid with featured card
- `src/pages/ContactPage.tsx` — Discovery briefing form with success state

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
