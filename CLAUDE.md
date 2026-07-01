# CLAUDE.md

Guidance for AI assistants (and humans) working in this repository.

## Current state of the repository

This repository is a **blank slate**. As of this writing it contains only:

- `README.md` — a single-line title (`# Hiking`)
- `CLAUDE.md` — this file

There is **no source code, build system, dependency manifest, test suite, or CI
configuration yet.** No language or framework has been chosen. Treat any task
here as greenfield work: you are likely creating the project's initial
structure rather than modifying existing code.

> Keep this file honest. When real code, tooling, or conventions land, replace
> the relevant sections below with concrete, verified details (build/test/lint
> commands, directory layout, architecture) instead of leaving placeholders.

## What the project is

Based on the name and README, this is intended to be a project called
**Hiking**. The scope, platform, and technology stack have not been defined.
If the intended purpose is unclear from the task description, ask the user
before scaffolding a stack, since that decision is hard to reverse.

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
