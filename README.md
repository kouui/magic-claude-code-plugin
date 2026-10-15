# magic-claude-code-plugin

A Claude Code plugin marketplace. This repo is only an index (`.claude-plugin/marketplace.json`); each plugin lives in its own repository and is pulled from GitHub.

## Use

```bash
claude plugin marketplace add kouui/magic-claude-code-plugin
claude plugin install <plugin>@magic-claude-code-plugin -s user
```

## Plugins

| Plugin | Repository | What it does |
| --- | --- | --- |
| `struct-compact` | [kouui/struct-compact-claude-plugin](https://github.com/kouui/struct-compact-claude-plugin) | Compaction via a structured handoff written by haiku; keeps the last 4 text messages |
| `ste` | [kouui/ste-claude-plugin](https://github.com/kouui/ste-claude-plugin) | Rewrite English into ASD-STE100 Simplified Technical English for agent-readable text |
| `zh-plain` | [kouui/zh-plain-claude-plugin](https://github.com/kouui/zh-plain-claude-plugin) | Write or rewrite Chinese text so a human or AI agent cannot misread it |
| `usage-hud` | [kouui/usage-hud-claude-plugin](https://github.com/kouui/usage-hud-claude-plugin) | A band above the prompt with model, git branch, context fill and plan usage; replaces a status-line HUD |
| `readonly-agents` | [kouui/readonly-agents-claude-plugin](https://github.com/kouui/readonly-agents-claude-plugin) | Subagents `reader` (read-only, plus read-only git queries) and `verifier` (runs in its own git worktree) |
| `coding` | [kouui/coding-claude-plugin](https://github.com/kouui/coding-claude-plugin) | Skills `task-prepare-implementation`, `github-create-pr`, `github-cli`, and agents `architecture-reviewer`, `brainstormer`, `code-reviewer`, `plan-reviewer` |

## Add a plugin

Add an entry to `plugins` in `.claude-plugin/marketplace.json`:

```json
{
  "name": "<plugin-name>",
  "description": "...",
  "source": { "source": "github", "repo": "kouui/<repo>" }
}
```

The plugin repo needs its own `.claude-plugin/plugin.json`.
