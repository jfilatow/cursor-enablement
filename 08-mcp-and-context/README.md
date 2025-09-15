## 08 — MCP and external context (≤60 minutes)

Connect remote tools and data sources.

Objectives
- Enable the Atlassian OAuth MCP and run a basic query.
- Use retrieved data to enrich a prompt or checklist.
- Understand privacy and scoping concerns.

Next: `../09-advanced-tips/README.md`.


### Atlassian MCP quick setup

Add via Settings (recommended)
- Settings → MCP & Integrations → Add remote server → Atlassian (OAuth) → Authorize.

Add via JSON (alternative)
Create or update `.cursor/mcp.json`:
```json
{
  "Atlassian-MCP-Server": {
    "url": "https://mcp.atlassian.com/v1/sse"
  }
}
```

Test queries
```text
Using the Atlassian MCP, list my Jira projects with names and keys.
```
```text
Search for issues assigned to me this week and summarize them in 5 bullets.
```

### Terminal quick reference (macOS and Windows)

- macOS: Applications → Utilities → Terminal. Open URLs with `open <url>`.
- Windows (CMD/PowerShell): Start menu → search "Command Prompt" or "PowerShell". Open URLs with `start <url>`.

