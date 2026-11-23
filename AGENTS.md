# AGENTS.md

This repo is personal, not Kodentuzo's, but Kodentuzo's repos install from it. The shared rules
apply where they fit: <https://github.com/kodentuzo/.github/blob/main/AGENTS.md>, in a local
checkout `@~/Repositories/kodentuzo/.github/AGENTS.md`. This file wins where the two differ.

## Layout

| Path | What |
| --- | --- |
| `skills/<name>/` | One skill: `SKILL.md`, and optional `scripts/`, `references/`, `assets/` |
| `template/` | The starter for a new skill |

## Conventions

- One skill per pull request. The rules for `SKILL.md` are in [CONTRIBUTING.md](CONTRIBUTING.md).
- A skill we didn't write is copied in identical to its original, with its licence file kept.
  Check its licence first. Never link to the maker's repo instead of copying. Two differences are
  allowed, each recorded in `SOURCES.md`: a patch, only when a shared rule forces it (for example,
  `npx` replaced by a pinned CLI), and a folder the repo doesn't use, left out (for example,
  `agents/` or `evals/`).
- Write its source repo, commit and licence, and every patch and left-out folder, in `SOURCES.md`
  at the root (added with the first copied skill), not in the skill's frontmatter. An update is a
  new copy from a new commit.
- Add each skill to the **Skills** table in [README.md](README.md).
- Plain, short sentences.

## Exceptions

- No JavaScript, so like `.github` and the hetzner template this repo keeps the general root files
  (README, CHANGELOG, LICENSE, CONTRIBUTING, `AGENTS.md`) and skips the JavaScript-only ones
  (`.nvmrc`, `biome.json`, pnpm). So there is no `pnpm check` or `verify`. It also has no
  `skills-lock.json`, because it installs nothing. This exception is confirmed (QA 78).
- A skill is validated with `skills-ref`, pinned to an exact version (see
  [CONTRIBUTING.md](CONTRIBUTING.md)).
