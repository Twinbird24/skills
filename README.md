# skills

A collection of reusable AI agent skills I use across projects and coding agents.

This repository follows the [Agent Skills specification](https://agentskills.io/specification). Each skill is portable rather than tied to a particular agent host.

## Structure

```text
skills/<skill-name>/SKILL.md
```

A skill may keep `scripts/`, `references/`, or `assets/` alongside `SKILL.md` when they are genuinely useful. The `skills/` directory is intentionally empty until there is a real skill to add.

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

## Publish

Validate the repository without publishing:

```bash
gh skill publish --dry-run
```

Publish the skills after pushing your changes:

```bash
gh skill publish
```

Run it from this repository after committing and pushing. It validates the skills and guides you through publishing them.

`gh skill` is a GitHub CLI preview feature, so its interface may change.
