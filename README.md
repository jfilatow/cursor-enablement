## Cursor enablement: start here

This repo is a self‑paced, evolving Cursor training you can run any time or use in a hosted session.

### Before you start — set up Cursor for vibe coding
- Open Settings (gear icon bottom‑left).
- Enable these for a faster build flow:
  - Background Agents: turn on background agents so tasks continue while you edit.
  - MCP & Integrations: allow remote servers; add Atlassian now or later. Keep it enabled.
  - Rules & Memories: enable rules; ensure the workspace rules folder `.cursor/rules/` is active.
  - Indexing & Docs: enable workspace indexing and allow attaching local/online docs as context.
  - Notifications: enable system notifications; optional to disable completion sounds.
  - General → Reset “Don’t Ask Again” Dialogs: click Show; during the session you can choose “Don’t ask again” when confirming large edits to keep momentum. Re‑enable prompts after the session if you prefer.
- Optional helpers:
  - Extensions: install a Markdown/HTML preview extension; optionally GitLens, Error Lens, Path Intellisense, MarkdownLint.
  - Read `.cursor/rules/VibeMode.mdc` for the session permissions we use when building fast.

### Optional — enable Vibe mode (build‑fast permissions)
- Open [`.cursor/rules/VibeMode.mdc`](.cursor/rules/VibeMode.mdc) and skim.
- In chat, start your session by saying:
```text
Enable Vibe mode for this session. Follow `.cursor/rules/VibeMode.mdc` and `.cursor/rules/Writing.mdc`. Ask before any destructive change.
```
- This grants broader edit permission and multi‑file scaffolding while keeping confirmations for destructive actions.

### Quick start
1. Sign in to Cursor Business and open this folder in Cursor.
2. Open [01-basics/README.md](01-basics/README.md) and follow the prompts.
3. You’ll generate your own `progress.md` and later build a simple dashboard by prompting Cursor; no prewritten solutions are included.
4. Install a preview extension to render Markdown/HTML in the IDE; see the recommendations in [01-basics/README.md](01-basics/README.md).

Tip: terminal access on macOS and Windows
- macOS: Finder → Applications → Utilities → Terminal.
- Windows: Start menu → type "Command Prompt" → open. For PowerShell, search "PowerShell".

### Sections (grow over time)
- [01-basics](01-basics/README.md) — install, UI tour, rules, docs context, and your first hands‑on build via prompts.
- [02-prompting-basics](02-prompting-basics/README.md) — prompt patterns and context control.
- [03-inline-edits](03-inline-edits/README.md) — transform and refactor safely.
- [04-generate](04-generate/README.md) — create files/functions with explanations.
- [05-read-explain](05-read-explain/README.md) — summarize and document code.
- [06-docs-writing](06-docs-writing/README.md) — README and docs workflows for all roles.
- [07-bugfix-flow](07-bugfix-flow/README.md) — reproduce, fix, validate.
- [08-mcp-and-context](08-mcp-and-context/README.md) — connect external tools and data.
- [09-advanced-tips](09-advanced-tips/README.md) — speed, reliability, personalization.

Start with `01-basics`. Each section targets ~60 minutes and builds on the previous one.

