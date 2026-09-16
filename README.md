# skills

A collection of reusable AI agent skills I use across projects and coding agents.

This repository follows the [Agent Skills specification](https://agentskills.io/specification). Each skill is portable rather than tied to a particular agent host.

## Structure

```text
skills/<skill-name>/SKILL.md
```

A skill may keep `scripts/`, `references/`, or `assets/` alongside `SKILL.md` when they are genuinely useful. The `skills/` directory is intentionally empty until there is a real skill to add.

## Install a skill

First inspect a remote skill:

```bash
gh skill preview <OWNER>/skills <skill-name>
```

Install it globally for Claude Code:

```bash
gh skill install <OWNER>/skills <skill-name> --agent claude-code --scope user
```

Install it globally for Codex:

```bash
gh skill install <OWNER>/skills <skill-name> --agent codex --scope user
```

Install it for a single project instead:

```bash
gh skill install <OWNER>/skills <skill-name> --agent claude-code --scope project
```

List installed skills and update them:

```bash
gh skill list
gh skill update
gh skill update --all
```

## Versioning

Without a version, `gh skill install` uses the latest release tag when one exists, otherwise the default branch. Pin a reproducible install to a tag or commit SHA:

```bash
gh skill install <OWNER>/skills <skill-name>@v1.0.0 --agent claude-code --scope user
```

`--pin v1.0.0` is an equivalent alternative. Pinned skills are skipped by normal updates; reinstall with a new pin, or run `gh skill update --unpin` to resume tracking the latest version.

## Create a skill

1. Create `skills/<name>/` using a kebab-case name.
2. Add `SKILL.md` with `name` and `description` frontmatter.
3. Write focused instructions.
4. Add supporting files only when they improve the skill.
5. Validate before publishing.
6. Commit and push.

## Publish

Validate the repository without publishing:

```bash
gh skill publish --dry-run
```

Publish a versioned release:

```bash
gh skill publish --tag v1.0.0
```

`gh skill publish` validates the Agent Skills layout, creates a GitHub release, and adds the `agent-skills` topic during its publish flow. Run it from this repository after committing and pushing the skill changes.

`gh skill` is a GitHub CLI preview feature, so its interface may change.
