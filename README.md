## Cursor enablement: start here

Purpose
- Learn Cursor’s features by doing, not reading.
- Follow a clear path from `01-basics` through advanced topics.
- Use it for new‑hire onboarding or a one‑hour hosted session.

### Before you start — set up Cursor for the session
- Open Settings (gear icon top right).
- Enable these for a faster build flow:
  - Background Agents: turn on background agents so tasks continue while you edit.
  - MCP & Integrations: allow remote servers; add Atlassian now or later. Keep it enabled.
  - Rules & Memories: enable rules; ensure the workspace rules folder `.cursor/rules/` is active.
  - Indexing & Docs: enable indexing and add public docs for context.
    - Add documentation → URL `https://docs.cursor.com` → Index.
    - Keep “Allow using documentation as context” enabled.
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
1. Sign in to Cursor and open this folder:
2. Go to [01-basics/README.md](01-basics/README.md). This is the step‑by‑step guide.
3. Outcome of `01-basics`: your `progress.json` plus a simple dashboard you build by prompting Cursor.
4. Install a Markdown/HTML preview extension (details in [01-basics/README.md](01-basics/README.md)).

Tip: terminal access on macOS and Windows
- macOS: Finder → Applications → Utilities → Terminal.
- Windows: Start menu → type "Command Prompt" → open. For PowerShell, search "PowerShell".

### Sections
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

### Prompting basics in Cursor

How to get consistent results:
- State the goal first, then constraints and acceptance criteria.
- Say what context to use (files, rules, docs) and how to treat it.
- Prefer short, iterative follow‑ups over long, single prompts.

Model selection
- Where: open Settings → Models to pick defaults; or use the model picker in chat.
- Guidance: start with a reliable general model. Switch to a larger model for complex reasoning; switch to a faster model for bulk edits after you have a spec.

Attach rules and context
- Rules live under [`.cursor/rules/`](.cursor/rules/). Reference them by name in your prompt, for example: “Follow `.cursor/rules/Writing.mdc` and `.cursor/rules/LearningMode.mdc`.”
- Docs: Settings → Indexing & Docs → Add documentation. This repo adds `https://docs.cursor.com` for reference.
- Files: drag files into chat or mention their relative paths.

Modes you can use while prompting
- Learning mode: [`.cursor/rules/LearningMode.mdc`](.cursor/rules/LearningMode.mdc) explains first and confirms after each step.
- Vibe mode: [`.cursor/rules/VibeMode.mdc`](.cursor/rules/VibeMode.mdc) speeds up multi‑file building with confirmations for destructive actions.
- Presentations: [`.cursor/rules/Presentations.mdc`](.cursor/rules/Presentations.mdc) makes outputs print‑ready.
- Progress tracking: [`.cursor/rules/ProgressTracker.mdc`](.cursor/rules/ProgressTracker.mdc) keeps `progress.json` updated.

Prompt templates you can copy
- Orientation: “Read `README.md` and `01-basics/README.md`. In 4 bullets, say what I’ll do today and the final artifact.”
- With rules: “Follow `.cursor/rules/Writing.mdc` and `.cursor/rules/LearningMode.mdc`. Explain before acting; confirm after.”
- With context: “Use the attached files and `https://docs.cursor.com` as sources. Cite what you used.”
- Acceptance criteria: “List acceptance criteria first. Then propose the smallest next step.”

