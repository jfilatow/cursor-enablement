## Copy‑paste prompts for basics

Use these in Cursor chat. Edit names and goals as needed.

### Orientation
```text
Read the top‑level [README.md](../README.md) and [01-basics/README.md](README.md). In 4 bullets, describe what I will do today and the final artifact.
```

### UI tour
```text
List the main areas of the Cursor UI (chat, composer, tabs, settings). Give me one tip for each.
```

### Using attachments
```text
I attached two files. Summarize them, then propose my next action in one sentence.
```

### Rules
```text
Follow [`.cursor/rules/Enablement.mdc`](../.cursor/rules/Enablement.mdc) and [`.cursor/rules/Writing.mdc`](../.cursor/rules/Writing.mdc). Generate a concise checklist for my `progress.md`.
```

### Create progress.md (standardized)
```text
You are my enablement copilot. Follow `.cursor/rules/Enablement.mdc` and `.cursor/rules/Writing.mdc`.

Create a new file `progress.md` for "Cursor Basics" with:
- A title line, date placeholder, and my name placeholder.
- 10–14 GitHub‑style checklist items grouped under `##` headings: Setup & UI, Attachments & Docs, Rules, Progress Checklist, Stretch.
- Two items pre‑checked to demonstrate `[x]`.
- Each task is specific and testable.

Return only the markdown content.
```

### Print-friendly output
```text
Ensure any HTML you generate includes a "Print / Save PDF" option and landscape print CSS.
```

### MCP (Atlassian demo)
```text
Using the Atlassian OAuth MCP, list my Jira projects and suggest a small task I could track in `progress.md`.
```

### Add Atlassian MCP via JSON
```text
Create or update `.cursor/mcp.json` with this content exactly and confirm it loads in Settings → MCP & Integrations:
{
  "Atlassian-MCP-Server": {
    "url": "https://mcp.atlassian.com/v1/sse"
  }
}
Then run a test query to verify connectivity.
```

### Docs resources to attach
```text
Use these docs for context and cite them as sources:
- Quickstart: https://docs.cursor.com/get-started/introduction
- Concepts: https://docs.cursor.com/get-started/concepts
- Working with documentation: https://docs.cursor.com/en/guides/advanced/working-with-documentation
Summarize the key points relevant to the Basics session in 5 bullets.
```

### Plan a simple viewer (no solution)
```text
Plan a minimal, static way to visualize my `progress.md` locally with no heavy tooling and with a "Print / Save PDF" action and landscape print CSS. Output a short plan with steps and acceptance criteria. Do not output code yet.
```

### Ask for OS-specific commands
```text
I’m on macOS/Windows. Provide the exact terminal/Command Prompt commands for the previous step, and include brief instructions on how to open the terminal on my OS.
```


