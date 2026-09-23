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
| [`design`](skills/design/SKILL.md) | `/design` → **Design** in the Codex app, or `$design` in Codex CLI/IDE | Guides intentional, production-ready UI design: explore directions, implement, inspect the rendered result, refine, and simplify. |

## Install a skill

Install it globally for Claude Code:

```bash
gh skill install Twinbird24/skills <skill-name> --agent claude-code --scope user
```

Install it globally for Codex:

```bash
gh skill install Twinbird24/skills <skill-name> --agent codex --scope user
```

Update installed skills when you want the latest version:

```bash
gh skill update --all
```

## Create a skill

1. Create `skills/<name>/` using a kebab-case name.
2. Add `SKILL.md` with `name` and `description` frontmatter.
3. Write focused instructions.
4. Add supporting files only when they improve the skill.
5. Validate before publishing.
6. Commit and push your changes.

## Optional publishing

This repository is usable directly from GitHub. If you later want tagged releases or broader discovery, see [GitHub's `gh skill publish` documentation](https://cli.github.com/manual/gh_skill_publish).
