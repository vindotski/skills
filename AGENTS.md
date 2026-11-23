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
- A skill we didn't write is copied in with its licence file kept, and its source repo and commit
  written down. Check its licence first. Never link to the maker's repo instead of copying.
- Add each skill to the **Skills** table in [README.md](README.md).
- Plain, short sentences.

## Exceptions

- No `package.json`, so no `pnpm check` or `verify`. A skill is validated with `skills-ref` (see
  [CONTRIBUTING.md](CONTRIBUTING.md)).
