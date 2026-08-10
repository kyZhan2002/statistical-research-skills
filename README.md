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

The Claude plugin manifest intentionally omits an explicit version. For a git-hosted marketplace, Claude Code can use the source commit SHA for version resolution. After pushing changes, refresh with:

```bash
claude plugin marketplace update statistical-research-skills
```

You can also enable marketplace auto-update from `/plugin`.

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
```

Codex's plugin manifest uses semantic versioning. When you change any skill content that should be distributed as a new Codex plugin release, bump:

```text
plugins/statistical-research/.codex-plugin/plugin.json
```

For example, change `0.1.0` to `0.1.1`. Then commit and push. After upgrading the marketplace, Codex can recognize the newer plugin version.

## Updating the skills

Edit only the canonical files under:

```text
plugins/statistical-research/skills/
```

Do not maintain separate Claude and Codex copies of the skill instructions. The platform-specific manifests only point to the shared `skills/` tree.

A normal update is:

```bash
# edit SKILL.md or references/*
# bump the Codex plugin version, e.g. 0.1.0 -> 0.1.1

git add .
git commit -m "Improve statistical research skills"
git push
```

Claude can track the new git commit. Codex should also receive a semantic-version bump in `.codex-plugin/plugin.json` to avoid stale plugin caches.

## Local validation

Validate Claude Code metadata when Claude Code is installed:

```bash
claude plugin validate .
```

For Codex, verify the marketplace/plugin files are valid JSON and use the current Codex plugin validator when available. The Codex manifest follows the current official layout: `.agents/plugins/marketplace.json` plus `plugins/<name>/.codex-plugin/plugin.json`.

## Keep project-specific context separate

Keep manuscript-specific facts in each research repository's own project instructions, such as `CLAUDE.md` or `AGENTS.md`. Examples include manuscript entrypoints, project macros, data/code locations, compute conventions, and project-specific notation. Do not put those facts into these reusable public skills.
