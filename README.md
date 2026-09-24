# skills

A collection of reusable AI agent skills I use across projects and coding agents.

This repository follows the [Agent Skills specification](https://agentskills.io/specification). Each skill is portable rather than tied to a particular agent host.

## Structure

```text
skills/<skill-name>/SKILL.md
```

A skill may keep `scripts/`, `references/`, or `assets/` alongside `SKILL.md` when they are genuinely useful.

## Skills

| Skill | Invoke | What it does |
| --- | --- | --- |
| [`design`](skills/design/SKILL.md) | `/design` → **Design** in the Codex app, or `$design` in Codex CLI/IDE | Intentional, production-ready UI design: explore, implement, inspect, refine, and simplify. |
| [`artifact-diagramming`](skills/artifact-diagramming/SKILL.md) | `/artifact-diagramming` in Claude Code or the Codex app, or `$artifact-diagramming` in Codex CLI/IDE | Focused, accessible SVG diagrams for real technical mechanisms and decisions. |

## Install a skill

Install it globally for Claude Code:

```bash
gh skill install Twinbird24/skills <skill-name> --agent claude-code --scope user
```

Install it globally for Codex:

```bash
gh skill install Twinbird24/skills <skill-name> --agent codex --scope user
```

Install every skill in this repository for Codex:

```bash
gh skill install Twinbird24/skills --all --agent codex --scope user
```

Install every skill in this repository for Claude Code:

```bash
gh skill install Twinbird24/skills --all --agent claude-code --scope user
```

When skills installed from GitHub change, check for updates and then install them—there is no need to re-add the skills:

```bash
gh skill update --dry-run
gh skill update --all
```

For skills installed with `--from-local`, rerun that local install command with `--force` after changing the source.

## Create a skill

1. Create `skills/<name>/` using a kebab-case name.
2. Add `SKILL.md` with `name` and `description` frontmatter.
3. Write focused instructions.
4. Add supporting files only when they improve the skill.
5. Validate before publishing.
6. Commit and push your changes.

## Optional publishing

This repository is usable directly from GitHub. If you later want tagged releases or broader discovery, see [GitHub's `gh skill publish` documentation](https://cli.github.com/manual/gh_skill_publish).
