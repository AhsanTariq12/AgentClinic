# AgentClinic — Tech Stack

## Language & Runtime

- **TypeScript** (strict mode) everywhere — server and views.
- **Node.js** (current LTS).

## Web Framework

- **Hono** with **`@hono/node-server`** — a lightweight, fast, TypeScript-first web framework.
- **Server-side rendering with Hono JSX** (`hono/jsx`) for pages and components. No client-side SPA framework; small amounts of progressive enhancement only where needed.

## Data

- **SQLite** — a simple, file-based database with zero setup (sufficient for the MVP; can migrate to a server database later if needed).
- **Drizzle ORM** (`drizzle-orm` + `better-sqlite3`) for a typed schema and queries.
- **drizzle-kit** for schema migrations; seed scripts for initial catalog data (ailments, therapies).

## Styling & Frontend

- **Tailwind CSS v4** for styling, using utility classes directly in Hono JSX components.
- **`@tailwindcss/cli`** to compile `src/styles/input.css` into a static stylesheet (watch mode in dev, minified for production).
- Shared design tokens (brand colors, fonts) defined via Tailwind's `@theme` in the input CSS.
- Responsive, accessible markup targeting evergreen browsers (Chrome, Edge, Firefox, Safari).

## Testing & Quality

- **Vitest** for unit and integration tests (including route tests via Hono's `app.request()`).
- **ESLint** + **Prettier** for linting and formatting.
- `tsc --noEmit` type checking as part of CI.

## Tooling

- **npm** for package management.
- **tsx** for running TypeScript in development (watch mode).
- `tsc` for production builds to `dist/`.

## Conventions

- Keep dependencies minimal and popular.
- Every feature phase ships with tests.
- Configuration via environment variables (e.g. `PORT`, `DATABASE_URL`).
