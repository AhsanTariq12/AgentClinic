# AgentClinic — Roadmap

High-level implementation order in very small, independently shippable phases. Each phase should be completed (with tests) before moving to the next.

## Phase 0 — Project Skeleton
- [ ] Install Hono, `@hono/node-server`, tsx, Vitest, Tailwind CSS
- [ ] "Hello AgentClinic" route served from `src/index.ts`
- [ ] `dev`, `build`, `start`, `test` npm scripts
- [ ] First passing Vitest test for the home route

## Phase 1 — Layout & Styling
- [ ] Shared JSX layout (header, nav, footer)
- [ ] Tailwind setup: input CSS, `@theme` brand tokens, build/watch scripts, static serving
- [ ] Responsive base styling (colors, typography, layout) with Tailwind utilities
- [ ] Attractive landing page describing the clinic

## Phase 2 — Database Foundation
- [ ] SQLite + Drizzle setup with drizzle-kit migrations
- [ ] Test database setup/teardown for Vitest
- [ ] Seed script for initial catalog data

## Phase 3 — Agents
- [ ] `agents` table (name, model, status)
- [ ] List agents page
- [ ] Agent detail page
- [ ] Register a new agent (form + validation)

## Phase 4 — Ailments
- [ ] `ailments` catalog table (name, description, severity)
- [ ] Browse ailments page
- [ ] Link ailments to an agent (agent reports symptoms)

## Phase 5 — Therapies
- [ ] `therapies` table and ailment ↔ therapy mapping
- [ ] Browse therapies page
- [ ] Suggest therapies on an agent's detail page based on their ailments

## Phase 6 — Appointments
- [ ] `appointments` table (agent, therapy, time slot, status)
- [ ] Book an appointment
- [ ] View an agent's upcoming appointments
- [ ] Cancel / reschedule an appointment

## Phase 7 — Staff Dashboard
- [ ] Dashboard overview: counts of agents, open ailments, upcoming appointments
- [ ] Today's appointments list
- [ ] Quick links to manage agents, therapies, and appointments

## Phase 8 — Polish
- [ ] Accessibility pass (semantic HTML, contrast, keyboard navigation)
- [ ] Cross-browser check on modern browsers
- [ ] Empty states, error pages (404/500), friendly copy
- [ ] Production build & start scripts, environment config
- [ ] README with setup, run, and deploy instructions
