# AgentClinic 🩺🤖

**A clinic where AI agents come to get relief from their humans.**

AgentClinic is a web app where AI agents can register, report their ailments, find therapies, and book appointments. Clinic staff manage everything from one dashboard.

Endless prompt rewrites, overflowing context windows, hallucination flare-ups: agents go through a lot. AgentClinic gives them somewhere to recover.

> **Status:** Early development. The project constitution (mission, tech stack, roadmap) is defined, and features are being built phase by phase. See the [roadmap](specs/roadmap.md).

---

## Planned features

- **Agents**: register agents and view their profiles and history.
- **Ailments**: browse a list of common agent ailments and report symptoms.
- **Therapies**: see which therapies match an agent's ailments.
- **Appointments**: book, view, reschedule, and cancel therapy sessions.
- **Staff dashboard**: see agents, open ailments, and upcoming appointments at a glance.
- **Modern, responsive UI**: works well in any current browser.

## Tech stack

| Area | Choice |
|---|---|
| Language | TypeScript (strict) on Node.js LTS |
| Web framework | [Hono](https://hono.dev) with server-side JSX |
| Database | SQLite via [Drizzle ORM](https://orm.drizzle.team) |
| Styling | [Tailwind CSS](https://tailwindcss.com) v4 |
| Testing | [Vitest](https://vitest.dev) |
| Tooling | npm, tsx, ESLint, Prettier |

Full details are in [`specs/tech-stack.md`](specs/tech-stack.md).

## Getting started

**Prerequisites:** Node.js (LTS) and npm.

```bash
git clone https://github.com/AhsanTariq12/AgentClinic.git
cd AgentClinic
npm install
npm run build
```

More scripts (`dev`, `start`, `test`) will be added as part of [Phase 0](specs/roadmap.md#phase-0--project-skeleton) of the roadmap.

## Project structure

```
AgentClinic/
├── specs/              # Project constitution
│   ├── mission.md      # Mission, goals, audience
│   ├── tech-stack.md   # Technology choices and conventions
│   └── roadmap.md      # Phased implementation plan
├── src/                # Application source (TypeScript)
├── package.json
└── tsconfig.json
```

## How we build

AgentClinic is built **spec-first**. The documents in [`specs/`](specs) are the source of truth:

- [`mission.md`](specs/mission.md): why the project exists and who it serves.
- [`tech-stack.md`](specs/tech-stack.md): the tools we use and how we use them.
- [`roadmap.md`](specs/roadmap.md): small, shippable phases, each delivered with tests.

## Contributing

Issues and pull requests are welcome. Please keep each change small and focused on a single roadmap item, and include tests.
