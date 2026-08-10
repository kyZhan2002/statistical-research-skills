# Statistical Research Skills

Reusable agent skills for statistical and biostatistical research. The repository contains no project-specific manuscript text, theorem statements, method names, datasets, unpublished numerical results, or paper-specific file paths.

## Included skills

- `statistical-manuscript-writer`: source-grounded, concise, copy-paste-ready LaTeX manuscript writing.
- `statistical-proof-auditor`: audit-before-proof theorem development and proof verification.
- `statistical-simulation-writer`: code-grounded simulation design, auditing, interpretation, and paper writing.
- `statistical-beamer-presenter`: intuitive, technically rigorous Beamer presentations for statistics audiences.

## Claude Code: recommended installation

This repository is a Claude Code plugin marketplace containing one plugin, `statistical-research`, which bundles all four skills.

From Claude Code:

```text
/plugin marketplace add YOUR_GITHUB_USERNAME/statistical-research-skills
/plugin install statistical-research@statistical-research-skills
```

Or from the shell:

```bash
claude plugin marketplace add YOUR_GITHUB_USERNAME/statistical-research-skills
claude plugin install statistical-research@statistical-research-skills
```

The plugin intentionally omits an explicit version. For a git-hosted marketplace, Claude Code can therefore use the source commit SHA for update detection. After pushing changes to GitHub, update manually with:

```text
/plugin marketplace update statistical-research-skills
/plugin update statistical-research@statistical-research-skills
```

For hands-off personal use, open `/plugin`, select the marketplace, and enable auto-update. Third-party marketplaces may have auto-update disabled by default.

Installed skill names are namespaced by the plugin, for example:

```text
/statistical-research:statistical-proof-auditor
/statistical-research:statistical-manuscript-writer
```

Claude can also invoke skills automatically when their descriptions match the task.

## Local testing before pushing

```bash
claude plugin validate .
claude --plugin-dir ./plugins/statistical-research
```

Inside Claude Code, test a skill and use `/reload-plugins` after edits when needed.

## Codex / other Agent Skills consumers

The canonical skill folders are under:

```text
plugins/statistical-research/skills/
```

For a filesystem-based Agent Skills consumer, copy or symlink individual skill folders from there into that product's supported skills directory. This keeps one source of truth while allowing Claude Code to use marketplace installation.

## Keep project-specific context separate

Do not put manuscript-specific facts in these reusable skills. Keep project-local facts in the repository's own instructions, such as `CLAUDE.md` or `AGENTS.md`: manuscript entrypoint, local macros, data/code directories, compute conventions, and project-specific notation.
