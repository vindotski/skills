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
- A skill we didn't write is copied in unchanged, with its licence file kept. Check its licence
  first. Never link to the maker's repo instead of copying.
- Write its source repo, commit and licence in `SOURCES.md` at the root (added with the first
  copied skill), not in the skill's frontmatter. An update is a new copy from a new commit.
- Add each skill to the **Skills** table in [README.md](README.md).
- Plain, short sentences.

## Exceptions

- No JavaScript, so like `.github` and the hetzner template this repo keeps the general root files
  (README, CHANGELOG, LICENSE, CONTRIBUTING, `AGENTS.md`) and skips the JavaScript-only ones
  (`.nvmrc`, `biome.json`, pnpm). So there is no `pnpm check` or `verify`. A skill is validated
  with `skills-ref` (see [CONTRIBUTING.md](CONTRIBUTING.md)).
