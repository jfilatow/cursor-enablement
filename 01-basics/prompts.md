## Ordered prompts for 01-basics

Run these in order. Edit names and goals as needed.

### Orientation
```text
Read the top‑level [README.md](../README.md) and [01-basics/README.md](README.md). In 4 bullets, describe what I will do today and the final artifact.
```

### 1) UI tour
```text
List the main areas of the Cursor UI (chat, composer, tabs, settings). Give me one tip for each.
```

### 2) Using attachments
```text
I attached two files. Summarize them, then propose my next action in one sentence.
```

### 3) Rules
```text
Follow [`.cursor/rules/Enablement.mdc`](../.cursor/rules/Enablement.mdc) and [`.cursor/rules/Writing.mdc`](../.cursor/rules/Writing.mdc). Generate a concise checklist for my `progress.json`.
```

### 3.0) Turn on Learning mode (optional)
```text
Enable Learning mode. Follow `.cursor/rules/LearningMode.mdc` plus the Writing rules. Explain each step briefly before acting and confirm after.
```

### 3.1) Add and index docs.cursor.com
```text
Open Settings → Indexing & Docs. Add documentation with URL https://docs.cursor.com and start indexing. Confirm "Allow using documentation as context" is enabled. Then summarize the 3 most relevant pages I should read for Basics.
```

### 4) Create progress.json (standardized)
```text
You are my enablement copilot. Follow `.cursor/rules/Enablement.mdc`, `.cursor/rules/Writing.mdc`, and `.cursor/rules/ProgressTracker.mdc`.

Create a new file `progress.json` for "Cursor Basics" using the schema in ProgressTracker. Seed sections for Setup & UI, Attachments & Docs, Rules, Dashboard, Stretch with pending exercises. Add a `file-created` changelog event.

Return only the JSON.
```

### 5) Print-friendly output
```text
Ensure any HTML you generate includes a "Print / Save PDF" option and landscape print CSS.
```

### 6) MCP (Atlassian demo)
```text
Using the Atlassian OAuth MCP, list my Jira projects and suggest a small task I could track in `progress.json`.
```

### 7) Add Atlassian MCP via JSON
```text
Create or update `.cursor/mcp.json` with this content exactly and confirm it loads in Settings → MCP & Integrations:
{
  "Atlassian-MCP-Server": {
    "url": "https://mcp.atlassian.com/v1/sse"
  }
}
Then run a test query to verify connectivity.
```

### 8) Docs resources to attach
```text
Use these docs for context and cite them as sources:
- Quickstart: https://docs.cursor.com/get-started/introduction
- Concepts: https://docs.cursor.com/get-started/concepts
- Working with documentation: https://docs.cursor.com/en/guides/advanced/working-with-documentation
Summarize the key points relevant to the Basics session in 5 bullets.
```

### 9) Plan a simple JSON dashboard (no solution)
```text
Plan a minimal, static way to visualize my `progress.json` locally with no heavy tooling and with a "Print / Save PDF" action and landscape print CSS. Output a short plan with steps and acceptance criteria. Do not output code yet.
```

### 10) Ask for OS-specific commands
```text
I’m on macOS/Windows. Provide the exact terminal/Command Prompt commands for the previous step, and include brief instructions on how to open the terminal on my OS.
```

### 11) Add a visual component (cards)
```text
Add a small plan to render each section as a card showing completed/pending counts from progress.json. Do not output code yet; list acceptance criteria.
```

### 12) Add a visual component (timeline)
```text
Plan a compact timeline that reads changelog events from progress.json and displays them with timestamps. No code yet; list acceptance criteria.
```


