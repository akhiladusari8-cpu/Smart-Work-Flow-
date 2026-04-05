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

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.

## Artifacts

### Smart Workflow Manager (`artifacts/smart-workflow`)
- **Kind**: react-vite
- **Preview Path**: `/`
- **Description**: A unified productivity dashboard combining task management, quick notes, a Pomodoro focus timer, activity tracking, and a switch-cost tracker.
- **Persistence**: localStorage only (no backend)
- **Features**:
  - Task Manager: add/complete/delete tasks with motivational messages on completion
  - Quick Notes: add/edit/delete notes with color-coded cards
  - Focus Timer: 25/5 min Pomodoro with circular progress ring, auto-switch modes
  - Activity Tracker: tracks tasks completed and total focus time with progress bar
  - Switch Cost Tracker: monitors section switching frequency, warns when switching too frequently
  - Dark mode toggle (persisted in localStorage)
