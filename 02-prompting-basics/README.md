## 02 — Prompting basics (≤60 minutes)

Master effective prompting patterns, model selection, and modes to get consistent results from Cursor.

### Objectives
- Write clear, scoped prompts with goals and constraints.
- Choose the right model for your task and understand when to switch.
- Use attachments, rules, and modes to steer outputs effectively.
- Iterate with short follow‑ups to reach the target.

### Prerequisites
- Completed `01-basics` and have a working `progress.json`.

---

## Prompting fundamentals

### How to get consistent results
1. **State the goal first**: Be specific about what you want to achieve.
2. **Add constraints**: Define scope, format, length, and quality requirements.
3. **Specify context**: Say which files, rules, or docs to use and how to treat them.
4. **Acceptance criteria**: List what "done" looks like before asking for work.
5. **Iterate**: Prefer short follow‑ups over single massive prompts.

### Model selection guide

**Where to choose models**
- Settings → Models: set your default model for chat and inline edits.
- Chat model picker: click the model name at the top of chat to switch mid‑conversation.

**Which model to use when**
- **General tasks**: Start with a reliable mid‑tier model (Claude 3.5 Sonnet, GPT‑4).
- **Complex reasoning**: Switch to larger models for architecture decisions, debugging complex logic, or planning multi‑step workflows.
- **Bulk edits**: Use faster models once you have a clear spec for repetitive tasks like renaming, formatting, or applying patterns across files.
- **Code generation**: Prefer models trained on code for functions, classes, and technical implementations.

**Model switching strategy**
- Start general → get the approach right → switch to faster for execution.
- Use larger models to create templates and specs → use faster models to apply them.

### Attach rules and context effectively

**Rules**
- Location: [`.cursor/rules/`](../.cursor/rules/)
- Usage: Reference by name in prompts: "Follow `.cursor/rules/Writing.mdc` and `.cursor/rules/LearningMode.mdc`."
- Available modes:
  - [LearningMode.mdc](../.cursor/rules/LearningMode.mdc): explains first, confirms after each step.
  - [VibeMode.mdc](../.cursor/rules/VibeMode.mdc): speeds up multi‑file building with confirmations for destructive actions.
  - [Presentations.mdc](../.cursor/rules/Presentations.mdc): makes outputs print‑ready with landscape PDF support.
  - [ProgressTracker.mdc](../.cursor/rules/ProgressTracker.mdc): keeps `progress.json` updated automatically.

**Documentation context**
- Settings → Indexing & Docs → Add documentation.
- This repo includes `https://docs.cursor.com` for reference.
- Reference in prompts: "Use `https://docs.cursor.com` as a source and cite what you used."

**File attachments**
- Drag files into chat or mention relative paths.
- Keep attachments focused and relevant.
- For large files, summarize first, then attach specific sections.

### Prompting modes and best practices

**Learning mode** (for beginners or complex tasks)
```text
Enable Learning mode. Follow `.cursor/rules/LearningMode.mdc` plus the Writing rules. Explain each step briefly before acting and confirm after.
```

**Vibe mode** (for fast iteration)
```text
Enable Vibe mode for this session. Follow `.cursor/rules/VibeMode.mdc` and `.cursor/rules/Writing.mdc`. Ask before any destructive change.
```

**With progress tracking**
```text
Follow `.cursor/rules/ProgressTracker.mdc` to update progress.json. Add a changelog entry for this task.
```

### Prompt templates you can copy

**Orientation**
```text
Read the attached files. In 4 bullets, say what I should achieve today and the final artifact.
```

**With rules and context**
```text
Follow `.cursor/rules/Writing.mdc` and `.cursor/rules/LearningMode.mdc`. Use the attached files and `https://docs.cursor.com` as sources. Cite what you used.
```

**Acceptance criteria first**
```text
List acceptance criteria for this task first. Then propose the smallest next step that moves toward those criteria.
```

**Iterative refinement**
```text
Review the previous output. Identify one specific improvement and apply it. Explain what changed in one sentence.
```

### Exercises
1. Draft 3 reusable prompts for your role; store them in `prompts.md`.
2. Do one prompt → follow‑up → refine loop and capture the before/after.
3. Practice model switching: start with a general model, get the approach, then switch to a faster model for execution.
4. Update your dashboard after checking off tasks.

Next: `../03-inline-edits/README.md`.


### Terminal quick reference (macOS and Windows)

Access
- macOS Terminal: Applications > Utilities > Terminal.
- Windows Command Prompt: Start menu > search "Command Prompt".
- Windows PowerShell: Start menu > search "PowerShell".

Common commands
- Navigate to a folder
  - macOS: `cd /path/to/directory`
  - Windows CMD: `cd \path\to\directory`
  - PowerShell: `Set-Location \path\to\directory` (aliases: `cd`, `sl`)
- List files
  - macOS: `ls`
  - Windows CMD: `dir`
  - PowerShell: `Get-ChildItem` (alias `ls`)
- Create a file
  - macOS: `touch notes.md`
  - Windows CMD: `echo. > notes.md`
  - PowerShell: `New-Item notes.md`
- Open a URL
  - macOS: `open https://docs.cursor.com`
  - Windows CMD/PowerShell: `start https://docs.cursor.com`
- Clear screen
  - macOS: `clear`
  - Windows CMD: `cls`
  - PowerShell: `Clear-Host` (alias `clear`)

Note: macOS paths use `/`, Windows uses `\`.

