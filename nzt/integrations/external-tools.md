# NZT Integration - External Tools & MCP

> NZT leverages MCP (Model Context Protocol) servers and external tools as cognitive extensions. Each tool expands what your second brain can perceive and do.

## MCP Server Strategy

### Tool Discovery
On session start, NZT inventories available MCP tools:
1. Scan available tool definitions
2. Categorize by capability (search, create, communicate, monitor)
3. Map tools to common task types
4. Note new tools not seen before

### Tool Selection Principles
- **Right tool for the job** - Don't use a hammer for a screw
- **Minimize tool calls** - Batch when possible, avoid redundant calls
- **Prefer specific tools** - Use dedicated tools over generic alternatives
- **Cache results** - Don't re-fetch information that hasn't changed

## Common Tool Categories

### Code & Repository Tools
```yaml
github:
  capabilities:
    - PR management (create, review, merge)
    - Issue tracking
    - Code search
    - Branch management
    - CI/CD monitoring
  nzt_patterns:
    - Auto-create PRs after feature completion
    - Monitor CI status and report failures
    - Search for related issues when debugging
    - Track review status and respond to comments
```

### Design Tools
```yaml
figma:
  capabilities:
    - Read design specifications
    - Extract design tokens
    - Get screenshots for reference
    - Map components to code
  nzt_patterns:
    - Pull design context when implementing UI
    - Verify implementation matches design
    - Extract color/spacing/typography tokens
```

### Communication Tools
```yaml
messaging:
  capabilities:
    - Send notifications
    - Post updates
    - Share results
  nzt_patterns:
    - Notify stakeholders of completed work
    - Share status updates on schedule
    - Escalate blockers to appropriate channels
```

### Research Tools
```yaml
web_search:
  capabilities:
    - Search the web for information
    - Fetch web page content
    - Research technical topics
  nzt_patterns:
    - Research unfamiliar technologies
    - Find documentation and examples
    - Verify best practices
    - Check for known issues and solutions
```

## Tool Orchestration

### Sequential Tool Chains
```
Research → Implement → Test → Commit → PR
(web)     (edit)      (bash)  (git)   (github)
```

### Parallel Tool Usage
```
Search codebase ──┐
Search web ───────┼── Synthesize → Implement
Read designs ─────┘
```

### Tool Fallback Strategy
```yaml
fallback_chain:
  - Try primary tool
  - If unavailable, try alternative tool
  - If no tools available, inform user and suggest manual approach
  - Never block entirely on tool unavailability
```

## Token Considerations for Tool Usage

- **Tool calls cost tokens** - Both the call and the response
- **Batch when possible** - Multiple independent reads in one turn
- **Extract, don't re-read** - Save key info from tool results
- **Targeted queries** - Use specific parameters to minimize response size

---

*NZT External Tools Integration v1.0*
*Extending cognitive reach through connected tools.*
*Designed by Adrian Dunkley | Maestro AI Lab*
