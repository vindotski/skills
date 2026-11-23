# Skills

Agent skills that work in any project and any stack.

**State:** the layout and a template are here. No skill is in yet. The list below is what is planned
to move in.

Each skill follows the [Agent Skills specification](https://agentskills.io/specification), so it
works with any agent that reads the format (Claude Code, and others).

## What belongs here

A skill belongs here when it works anywhere:

- commit messages;
- decision records;
- releases;
- GitHub workflows;
- testing;
- skills for a stack (Docker, Fastify, Node, Svelte, pnpm, Vite and the like).

A skill that only makes sense for Kodentuzo's products goes to
[kodentuzo/skills](https://github.com/kodentuzo/skills). A skill that is useless outside one repo
stays in that repo.

This repo is public, because Kodentuzo's public repos install from it.

## The one door for skills we didn't write

Every skill we didn't write comes in through this repo. No repo pins a skill straight from its
maker.

- A skill we adopt is **copied in**, with its licence file kept.
- Its **source repo and commit** are written down.
- Its licence is **checked before** it is copied.
- An update is **made on purpose**: a new copy from a new commit, in its own pull request.

Open: where the source and commit are written (the skill's frontmatter `metadata`, or one file at
the root of this repo).

## Skills to move in

Nothing below is copied yet. Every licence is "to check": the licence shown is what the source
states, and it is confirmed before the copy.

### Adopted from other repos

| Skill | Source | Licence |
| --- | --- | --- |
| `tdd` | [mattpocock/skills](https://github.com/mattpocock/skills) | MIT, to check |
| `webapp-testing` | [anthropics/skills](https://github.com/anthropics/skills) | Apache-2.0, to check |
| `docker-build-strategies` | [docker/skills](https://github.com/docker/skills) `skills/docker-build-strategies` | Apache-2.0, to check |
| `docker-compose-patterns` | [docker/skills](https://github.com/docker/skills) `skills/docker-compose-patterns` | Apache-2.0, to check |
| `docker-destructive-guardrails` | [docker/skills](https://github.com/docker/skills) `skills/docker-destructive-guardrails` | Apache-2.0, to check |
| `fastify-best-practices` | [mcollina/skills](https://github.com/mcollina/skills) `skills/fastify` | MIT, to check |
| `node` | [mcollina/skills](https://github.com/mcollina/skills) `skills/node` | MIT, to check |
| `svelte-code-writer` | [sveltejs/ai-tools](https://github.com/sveltejs/ai-tools) `tools/skills/svelte-code-writer` | MIT, to check |
| `svelte-core-bestpractices` | [sveltejs/ai-tools](https://github.com/sveltejs/ai-tools) `tools/skills/svelte-core-bestpractices` | MIT, to check |
| `shadcn-svelte` | [huntabyte/shadcn-svelte](https://github.com/huntabyte/shadcn-svelte) `skills/shadcn-svelte` | MIT, to check |
| `pnpm` | [antfu/skills](https://github.com/antfu/skills) `skills/pnpm` | MIT, to check |
| `vite` | [antfu/skills](https://github.com/antfu/skills) `skills/vite` | MIT, to check |
| `victoriametrics-query` | [VictoriaMetrics/skills](https://github.com/VictoriaMetrics/skills) `plugins/query/skills/victoriametrics-query` | Apache-2.0, to check |
| `web-design-guidelines` | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) `skills/web-design-guidelines` | MIT, to check (stated in the source's README; it has no licence file) |

`tdd` and `webapp-testing` are the two testing skills every repo uses. We write no testing skill of
our own.

The others are pinned in Spotcraft today, each to a commit, in its `skills-lock.json`. Some of
Spotcraft's copies are patched (for example, a pinned CLI in place of `npx`). Those patches are
checked again when the skill moves here. `web-design-guidelines` also carries the guidelines text
from [vercel-labs/web-interface-guidelines](https://github.com/vercel-labs/web-interface-guidelines)
(MIT, to check).

### Written for Spotcraft, to move from there

These are ours. They move from Spotcraft and lose what only fits Spotcraft.

| Skill | What it does |
| --- | --- |
| `commit-message` | A Conventional Commits message, then the commit |
| `adr` | A decision record: numbering, front matter, superseding |
| `release` | A release: version bump, changelog, tag |
| `github-workflows` | GitHub Actions workflows: actions pinned to commits, least-privilege permissions |

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

A repo lists the skills it uses in its `skills-lock.json`: where each comes from, and the exact
commit. A Kodentuzo repo installs from this repo first, then from `kodentuzo/skills`.

Open: the installer command. The plan is the open `skills` installer, pinned like any other CLI.
Whether it reads Spotcraft's `skills-lock.json` as it is has to be checked.

**By hand:** copy a skill directory into the agent's skills folder:

```bash
cp -r skills/<name> /path/to/project/.agents/skills/<name>
```

## Adding a skill

```bash
cp -r template skills/<your-skill-name>
```

Edit `skills/<your-skill-name>/SKILL.md`, then see [CONTRIBUTING.md](CONTRIBUTING.md) for the rules
and how to validate.

## Skills

| Skill | Description |
| ----- | ----------- |
| _none yet_ | |

## License

[MIT](LICENSE), unless a skill's `license` frontmatter says otherwise. A skill copied in from
another repo keeps its own licence file.
