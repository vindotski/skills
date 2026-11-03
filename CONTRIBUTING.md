# Contributing

Contributions are welcome. One skill per pull request.

## Steps

1. Copy the template: `cp -r template skills/<skill-name>`
2. Fill in `SKILL.md` (see rules below).
3. Validate it (see below).
4. Add a row to the **Skills** table in [README.md](README.md).
5. Open a pull request.

## Rules

Based on the [Agent Skills specification](https://agentskills.io/specification).

**`name`** (required)
- 1–64 characters: lowercase letters, numbers, and hyphens only
- No leading, trailing, or consecutive hyphens (`-pdf`, `pdf-`, `pdf--tools` are invalid)
- Must match the skill's directory name

**`description`** (required)
- Up to 1024 characters
- Say both **what** the skill does and **when** to use it, with keywords an agent can match on

**Body**
- Keep `SKILL.md` under 500 lines; move detail into `references/`
- Reference other files with relative paths from the skill root, one level deep
- Scripts in `scripts/` should be self-contained or document their dependencies

**Optional frontmatter:** `license`, `compatibility` (only if there are real environment requirements), `metadata`, `allowed-tools`.

Skills are MIT-licensed by default. If yours needs a different license, set `license` in its frontmatter.

## Validation

Use the reference validator, [skills-ref](https://github.com/agentskills/agentskills/tree/main/skills-ref):

```bash
uvx --from skills-ref skills-ref validate skills/<skill-name>
# or: pip install skills-ref && skills-ref validate skills/<skill-name>
```
