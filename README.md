# Statistical Research Skills

Reusable agent skills for statistical and biostatistical research. This repository is intentionally project-agnostic: it contains no manuscript-specific text, theorem statements, method names, datasets, unpublished numerical results, reviewer reports, or paper-specific paths.

## Included skills

- `statistical-manuscript-writer`: source-grounded, concise, copy-paste-ready LaTeX manuscript writing.
- `statistical-proof-auditor`: audit-before-proof theorem development and proof verification.
- `statistical-simulation-writer`: code-grounded simulation design, auditing, interpretation, and paper writing.
- `statistical-beamer-presenter`: intuitive, technically rigorous Beamer presentations for statistics audiences.

The same canonical `skills/` directory is used by both Claude Code and Codex. Platform-specific marketplace and plugin manifests live beside it.

## Repository layout

```text
.
├── .claude-plugin/
│   └── marketplace.json
├── .agents/
│   └── plugins/
│       └── marketplace.json
└── plugins/
    └── statistical-research/
        ├── .claude-plugin/
        │   └── plugin.json
        ├── .codex-plugin/
        │   └── plugin.json
        └── skills/
            ├── statistical-manuscript-writer/
            ├── statistical-proof-auditor/
            ├── statistical-simulation-writer/
            └── statistical-beamer-presenter/
```

## Claude Code installation

Add the GitHub repository as a marketplace, then install the bundled plugin:

```bash
claude plugin marketplace add YOUR_GITHUB_USERNAME/statistical-research-skills
claude plugin install statistical-research@statistical-research-skills
```

Inside an interactive Claude Code session, the equivalent commands are:

```text
/plugin marketplace add YOUR_GITHUB_USERNAME/statistical-research-skills
/plugin install statistical-research@statistical-research-skills
```

Claude plugin skills are namespaced, for example:

```text
/statistical-research:statistical-proof-auditor
/statistical-research:statistical-manuscript-writer
```

The Claude and Codex plugin manifests use the same explicit release version. After pushing changes, refresh the marketplace and update the installed Claude plugin:

```bash
claude plugin marketplace update statistical-research-skills
claude plugin update statistical-research@statistical-research-skills
```

Start a new Claude Code session or run `/reload-plugins`. You can also enable marketplace auto-update from `/plugin`.

## Codex installation

Codex reads the repository marketplace from `.agents/plugins/marketplace.json` and the plugin manifest from `plugins/statistical-research/.codex-plugin/plugin.json`.

Add the GitHub repository as a marketplace:

```bash
codex plugin marketplace add YOUR_GITHUB_USERNAME/statistical-research-skills
```

Then install the plugin:

```bash
codex plugin add statistical-research@statistical-research-skills
```

You can also open Codex and use `/plugins` to find and install `Statistical Research` after adding the marketplace.

To refresh the Git-backed marketplace after new commits:

```bash
codex plugin marketplace upgrade statistical-research-skills
codex plugin add statistical-research@statistical-research-skills
```

Restart Codex and start a new conversation after updating. When you change skill content for a new release, bump both manifests to the same semantic version:

```text
plugins/statistical-research/.codex-plugin/plugin.json
plugins/statistical-research/.claude-plugin/plugin.json
```

For example, change `0.1.1` to `0.1.2`. Then commit and push so other devices can fetch the new release.

## Updating the skills

Edit only the canonical files under:

```text
plugins/statistical-research/skills/
```

Do not maintain separate Claude and Codex copies of the skill instructions. The platform-specific manifests only point to the shared `skills/` tree.

Common writing guidance lives in `plugins/statistical-research/references/writing-principles.md`. Each skill explicitly reads this reference and adapts it to its own task. Keep the plugin directory intact when installing or copying it manually so these relative references resolve. Update the shared reference for common prose rules and each `SKILL.md` for task-specific behavior.

A normal update is:

```bash
# edit SKILL.md or references/*
# bump both plugin versions, e.g. 0.1.1 -> 0.1.2

git add .
git commit -m "Improve statistical research skills"
git push
```

Keep the two manifest versions synchronized so both clients recognize the release.

## Local validation

Validate Claude Code metadata when Claude Code is installed:

```bash
claude plugin validate .
```

For Codex, verify the marketplace/plugin files are valid JSON and use the current Codex plugin validator when available. The Codex manifest follows the current official layout: `.agents/plugins/marketplace.json` plus `plugins/<name>/.codex-plugin/plugin.json`.

## Keep project-specific context separate

Keep manuscript-specific facts in each research repository's own project instructions, such as `CLAUDE.md` or `AGENTS.md`. Examples include manuscript entrypoints, project macros, data/code locations, compute conventions, and project-specific notation. Do not put those facts into these reusable public skills.
