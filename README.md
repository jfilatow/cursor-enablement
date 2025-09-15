## Cursor enablement: start here

This repo is a self‑paced, evolving Cursor training you can run any time or use in a hosted session.

### Before you start — make Cursor more VS Code compatible
- Open Settings (gear icon bottom‑left).
- In Settings, review:
  - Editor: enable visible minimap if you prefer; disable unusual keybindings.
  - Extensions: install a Markdown/HTML preview extension; optionally GitLens, Error Lens, Path Intellisense, MarkdownLint.
  - Rules: ensure `.cursor/rules/` are active.
- Goal: a simple, predictable setup that mirrors a typical VS Code layout.

### Optional — enable Vibe mode (build‑fast permissions)
- Open `.cursor/rules/VibeMode.mdc` and skim.
- In chat, start your session by saying:
```text
Enable Vibe mode for this session. Follow `.cursor/rules/VibeMode.mdc` and `.cursor/rules/Writing.mdc`. Ask before any destructive change.
```
- This grants broader edit permission and multi‑file scaffolding while keeping confirmations for destructive actions.

### Quick start
1. Sign in to Cursor Business and open this folder in Cursor.
2. Open `01-basics/README.md` and follow the prompts.
3. You’ll generate your own `progress.md` and later build a simple dashboard by prompting Cursor; no prewritten solutions are included.
4. Install a preview extension to render Markdown/HTML in the IDE; see the recommendations in `01-basics/README.md`.

Tip: terminal access on macOS and Windows
- macOS: Finder → Applications → Utilities → Terminal.
- Windows: Start menu → type "Command Prompt" → open. For PowerShell, search "PowerShell".

### Sections (grow over time)
- `01-basics` — install, UI tour, rules, docs context, and your first hands‑on build via prompts.
- `02-prompting-basics` — prompt patterns and context control.
- `03-inline-edits` — transform and refactor safely.
- `04-generate` — create files/functions with explanations.
- `05-read-explain` — summarize and document code.
- `06-docs-writing` — README and docs workflows for all roles.
- `07-bugfix-flow` — reproduce, fix, validate.
- `08-mcp-and-context` — connect external tools and data.
- `09-advanced-tips` — speed, reliability, personalization.

Start with `01-basics`. Each section targets ~60 minutes and builds on the previous one.

