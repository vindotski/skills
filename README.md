# Skills

A collection of reusable [Agent Skills](https://agentskills.io) for use across projects. Each skill follows the [Agent Skills specification](https://agentskills.io/specification), so it works with any agent that supports the format (Claude Code, and others).

## Layout

```
skills/
└── <skill-name>/
    ├── SKILL.md      # required: frontmatter + instructions
    ├── scripts/      # optional: executable code
    ├── references/   # optional: docs loaded on demand
    └── assets/       # optional: templates, data, images
template/
└── SKILL.md          # starter for new skills
```

## Using skills in a project

**With the `skills` CLI:**

```bash
npx skills add <github-user>/skills                    # pick from all skills
npx skills add <github-user>/skills --skill <name>     # a specific skill
```

**Manually:** copy or symlink a skill directory into your agent's skills folder. For Claude Code:

```bash
# per project
cp -r skills/<name> /path/to/project/.claude/skills/<name>

# globally
ln -s "$PWD/skills/<name>" ~/.claude/skills/<name>
```

## Adding a skill

```bash
cp -r template skills/<your-skill-name>
```

Edit `skills/<your-skill-name>/SKILL.md`, then see [CONTRIBUTING.md](CONTRIBUTING.md) for the rules and how to validate.

## Skills

| Skill | Description |
| ----- | ----------- |
| _none yet_ | |

## License

[MIT](LICENSE), unless a skill's `license` frontmatter says otherwise.
