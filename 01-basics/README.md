## 01 — Cursor basics (60 minutes)

Learn Cursor’s core flow with hands‑on prompts. You’ll generate all artifacts yourself; no prewritten solutions are included.

### Objectives
- Install and tour Cursor; learn where to find things.
- Use attachments, docs, and rules to guide the agent.
- Generate your own `progress.md` and, later, your own simple visual dashboard by prompting Cursor.

### Prerequisites
- Cursor Business account. No Git needed; download or use this repo directly.
- macOS or Windows.
- Install a preview extension to render HTML/Markdown in the IDE.
  - Suggested: "Markdown Preview Enhanced" or built‑in preview if available.
  - Also recommended (optional): GitLens, Error Lens, Path Intellisense, MarkdownLint.

### What you’ll build
- A standardized `progress.md` checklist created via a structured prompt.

### Agenda (suggested)
- 0–10 min: Setup, open repo, orientation.
- 10–20 min: UI tour; chat, composer, tabs, settings.
- 20–35 min: Attach files, use rules; add docs context.
- 35–55 min: Create `progress.md` from a structured prompt. Optionally start scaffolding a simple viewer you will complete in a later section.
- 55–60 min: Recap and next steps.

---

### Step 1 — Open the repo and orient
1. Open this folder in Cursor.
2. Open the top‑level [README.md](../README.md). This file explains the training structure, section order, and how you’ll generate artifacts yourself.
3. Open Settings → General, Editor, Keyboard Shortcuts to see what’s available.
4. Install the recommended extensions from above. Ask Cursor for the exact steps if needed:
Optional: enable a faster build session (Vibe mode)
```text
Enable Vibe mode for this session. Follow `.cursor/rules/VibeMode.mdc` and `.cursor/rules/Writing.mdc`. Ask before any destructive change.
```
```text
I want to preview Markdown/HTML inside the IDE. Recommend a preview extension and provide step-by-step install instructions in Cursor.
```

Try in chat:
```text
Summarize the purpose of this repository in 4 bullets. Then list the next action I should take.
```

### Step 2 — Quick UI tour (hands‑on)
- Editor: files and tabs on the left.
- Chat: contextual conversation. You can attach files and reference rules.
- Composer: generate code or docs inline.
- Settings: gear icon bottom‑left. Models, privacy, MCP & integrations, rules.
- Show/hide sidebar: View menu → Appearance → Show/Hide Side Bar.
- Show/hide terminal: View menu → Terminal.
- Enter full screen: View menu → Appearance → Full Screen.
- Enter Zen (distraction‑free): View menu → Appearance → Zen Mode.

Try in chat with attachments:
```text
Read the top‑level [README.md](../README.md) and this [Basics README](README.md). In one paragraph, explain what I will build today.
```

Optional: ask for keyboard shortcut help
```text
List the key shortcuts for chat, inline edits, and opening settings. Keep it to one line per shortcut.
```

### Step 3 — Attach docs as context
Goal: show Cursor how to use nearby material.

1. Drag the top‑level [README.md](../README.md) and this [Basics README](README.md) into chat. Ask for a 3‑sentence summary.
2. Add docs for Cursor as external knowledge and cite them in your prompt:
   - Quickstart: `https://docs.cursor.com/get-started/introduction`
   - Concepts: `https://docs.cursor.com/get-started/concepts`
   - Working with documentation: `https://docs.cursor.com/en/guides/advanced/working-with-documentation`
3. Optional: attach any internal primer or policy PDFs allowed in your environment.

Open docs in your browser from the command line (optional):
- macOS Terminal (see how to open Terminal in the top‑level `README.md`):
```bash
open https://docs.cursor.com/get-started/introduction && open https://docs.cursor.com/get-started/concepts && open https://docs.cursor.com/en/guides/advanced/working-with-documentation
```
- Windows Command Prompt (see how to open Command Prompt in the top‑level `README.md`):
```bat
start https://docs.cursor.com/get-started/introduction & start https://docs.cursor.com/get-started/concepts & start https://docs.cursor.com/en/guides/advanced/working-with-documentation
```

Tip: keep attachments small and specific.

### Step 4 — Use rules to shape outputs
Rules live in `.cursor/rules/`.

1. Open [`.cursor/rules/Enablement.mdc`](../.cursor/rules/Enablement.mdc) and skim it.
2. In chat, refer to rules explicitly:
```text
Follow the Enablement and Writing rules when responding. Create a short checklist for my progress.md.
```
3. Optional: open [`.cursor/rules/Presentations.mdc`](../.cursor/rules/Presentations.mdc) for printable output guidance.

### Step 5 — Optional context via MCP (Atlassian demo)
You can connect external tools using MCP.

1. Settings → MCP & Integrations → Add remote server.
2. Search for “Atlassian (OAuth)” and connect with your account.
3. Test in chat: “List my Jira projects” or “Search issues assigned to me.”

This is a demo; you don’t need it to finish Basics.

Alternative: add the server via workspace config
- Create or update `.cursor/mcp.json` in this folder with:
```json
{
  "Atlassian-MCP-Server": {
    "url": "https://mcp.atlassian.com/v1/sse"
  }
}
```

Commands to create the file (optional):
- macOS:
```bash
mkdir -p .cursor && printf '{\n  "Atlassian-MCP-Server": {\n    "url": "https://mcp.atlassian.com/v1/sse"\n  }\n}\n' > .cursor/mcp.json
```
- Windows (PowerShell):
```powershell
$cfg = @{ 'Atlassian-MCP-Server' = @{ url = 'https://mcp.atlassian.com/v1/sse' } } | ConvertTo-Json -Depth 3; New-Item -ItemType Directory -Force .cursor | Out-Null; $cfg | Set-Content -Path .cursor\mcp.json
```

Verify it works
- Settings → MCP & Integrations: confirm “Atlassian-MCP-Server” appears. If prompted, authorize OAuth.
- In chat:
```text
Using the Atlassian OAuth MCP, list my Jira projects and suggest a small task I could track in progress.md.
```

### Step 6 — Create your training checklist
Use this structured prompt to generate your `progress.md` from scratch. For more prompts, see [prompts.md](prompts.md):
```text
You are my enablement copilot. Follow `.cursor/rules/Enablement.mdc` and `.cursor/rules/Writing.mdc`.

Goal: Create a personal training checklist for "Cursor Basics" as a GitHub‑style markdown file named `progress.md`.

Requirements:
- Group items under `##` headings that mirror this section’s agenda: Setup & UI, Attachments & Docs, Rules, Progress Checklist.
- 10–14 tasks total; each task uses `- [ ]` or `- [x]`.
- Tasks must be specific and testable, e.g., "Attach the top‑level README.md and ask for a 3‑sentence summary."
- Include 2 stretch tasks at the end under `## Stretch`.
- Put a short header at the top with: title, date placeholder, and my name placeholder.

Output: only the markdown content, no explanations.
```
After Cursor generates the content, create a new file `progress.md` in this folder and paste it in.

Optional: validate checkboxes render correctly in preview
```text
Open my new progress.md in a preview. Verify checkboxes display correctly and headings are structured.
```

If you need a terminal command to create the file directly:
- macOS:
```bash
printf "# Cursor Basics Progress\n\n- [ ] Example task" > progress.md
```
- Windows:
```bat
echo # Cursor Basics Progress>progress.md & echo.>>progress.md & echo - [ ] Example task>>progress.md
```

### Step 7 — Optional: start a simple viewer (no solution provided)
Ask Cursor to propose a minimal, static way to visualize `progress.md` without heavy tooling and with a landscape print option. Save your plan for the later section.

Suggested planning follow‑ups:
```text
Propose the minimal files and their roles (no code). Include acceptance criteria and print-to-PDF requirements.
```

### Step 8 — Reflection
In chat:
```text
Given my current progress.md, suggest the next best section to take and why. Keep it short.
```

### Next section
Go to `../02-prompting-basics/README.md`.

### Troubleshooting
- If attachments are too large, summarize first; then attach smaller excerpts.
- If MCP auth fails, complete OAuth in your browser, then retry.

### Optional activities (if you have time)
- Personalize `progress.md` with role-specific tasks.
- Add a “Stretch” section with 2–3 extra tasks.
- Draft a facilitator script outline in a new `Facilitator.md` with checkpoints every 10 minutes.



