# Contributing to my-rubberduck

Thanks for considering a contribution. my-rubberduck is a philosophy-driven mentoring skill, so any change to `SKILL.md` or the reference files must keep the rubber-duck spirit alive: guide reasoning, ask questions, explain trade-offs, and never hand out complete solutions by default.

## Development Setup

### Prerequisites
- Git
- A compatible AI coding agent, via the [skills CLI](https://www.skills.sh/docs/cli)

```bash
git clone https://github.com/kevin-mmoura/my-rubberduck.git
cd my-rubberduck

npx skills add kevin-mmoura/my-rubberduck --skill my-rubberduck
```

There is no test suite and no build step. The skill is just markdown instructions consumed by an AI agent. Verify your change by reading the actual files — `SKILL.md` and `references/*.md` — and checking behavior against them. Never invent code behavior, test results, or file contents.

## Commit Guidelines

We use [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` — new capability or interaction mode
- `fix:` — correction to guidance or examples
- `docs:` — `SKILL.md`, reference files, or this documentation
- `refactor:` — rewording or restructuring without changing intent

```text
feat: add --challenge interaction mode
fix: stop the debug example from revealing the bug upfront
docs: rewrite quick start invocation examples
```

## Branch Naming

Branch from `main`:

```bash
git checkout -b feat/mentoring-hints
git checkout -b fix/debug-example
git checkout -b docs/quickstart
```

Prefixes: `feat/`, `fix/`, `docs/`, `refactor/`.

## Pull Request Process

1. Open a PR against `main` with a clear summary of what changed and why.
2. Keep the rubber-duck philosophy intact: proportional guidance, focused questions, no ready answers by default.
3. Verify against the actual repository files.
4. Keep PRs small and reviewable.

## A gut check before you change anything

Ask these questions about `SKILL.md` or any reference file:

- Does this guide reasoning instead of handing over a solution?
- Is the guidance proportional to the problem?
- Can it be verified against real code or files?
- Does it separate actual defects from stylistic preferences?

If the answer to any of them is no, rethink the change.
