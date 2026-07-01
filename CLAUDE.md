# CLAUDE.md

Guidance for AI assistants (and humans) working in this repository.

## Current state of the repository

This repository currently holds **planning and knowledge documents**, not
software. As of this writing it contains:

- `README.md` — a single-line title (`# Hiking`)
- `CLAUDE.md` — this file
- `planning/` — markdown planning docs for section-hiking the Ozark Trail (OT)
  in Missouri (see layout below)

There is still **no source code, build system, dependency manifest, test suite,
or CI configuration.** No language or framework has been chosen. If a task asks
for application code, treat it as greenfield work and confirm the intended stack
first.

> Keep this file honest. When real code, tooling, or conventions land, replace
> the relevant sections below with concrete, verified details (build/test/lint
> commands, directory layout, architecture) instead of leaving placeholders.

## What the project is

**Hiking** is Dan's personal planning space for section-hiking the full **Ozark
Trail** over multiple years, with landscape and nature photography as a co-equal
goal. The content is captured from planning conversations and stored as markdown
so it can be loaded as context in future chats. No software scope, platform, or
technology stack has been defined; if a task implies building an application, ask
before scaffolding a stack, since that decision is hard to reverse.

## Repository layout

```
planning/
├── README.md            # index: section calendar + document map
├── project-overview.md  # multi-year plan, constraints, seasonal calendar
├── shuttle-logistics.md # cross-cutting transportation/shuttle strategy
└── taum-sauk/           # first planned section (Hwy 21 → Johnson's Shut-Ins)
    ├── overview.md      # project handoff summary
    ├── trip-plan.md     # master project tracker
    ├── gear-to-buy.md   # gear purchase checklist
    └── photography.md   # camera gear planning
```

### Planning document conventions

- Each **trail section** gets its own folder under `planning/` (e.g.
  `planning/taum-sauk/`); section sub-topics (gear, photography, etc.) are
  sibling files within it.
- **Cross-cutting topics** that span all sections live at the top level of
  `planning/` (e.g. `shuttle-logistics.md`).
- `planning/README.md` is the index — keep its sections table and document map
  in sync whenever you add or move a file.
- Documents are captured from planning chats; preserve their content faithfully
  and cross-link related docs so navigation stays easy.

## Development workflow

### Branching

Development happens on feature branches, not directly on `main`.

- Create work on a dedicated branch (e.g. `claude/<short-topic>`).
- Never push directly to `main` without explicit permission.
- Use `git push -u origin <branch-name>` when pushing.
- After pushing, open a pull request against `main` if one does not already
  exist for the branch.

### Commits

- Write clear, descriptive commit messages explaining the *why*, not just the
  *what*.
- Keep commits focused; commit related changes together.
- Only commit or push when the work is ready or the user asks.

## Conventions to establish

Because nothing is set yet, when you introduce the first real code, also
establish and document here:

1. **Language & framework** — and why it was chosen.
2. **Directory layout** — where source, tests, and assets live.
3. **Build / run commands** — how to build and start the project.
4. **Test commands** — how to run the test suite.
5. **Lint / format commands** — the formatter and linter, and how to run them.
6. **Dependency management** — the package manager and lockfile policy.

Once these exist, prefer running the project's own scripts (e.g. a `Makefile`,
`package.json` scripts, or task runner) over ad-hoc commands, and record them
in this file.

## Notes for AI assistants

- This repo currently has essentially no context to read — do not assume
  hidden structure. Verify with the filesystem before acting.
- When scaffolding, keep the initial footprint small and idiomatic for the
  chosen stack; avoid pulling in heavy tooling the project doesn't need yet.
- Update this file in the same change whenever you add tooling, structure, or
  conventions, so it never drifts from reality.
