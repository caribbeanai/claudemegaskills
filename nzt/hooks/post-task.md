# NZT Hook - Post-Task

> Runs after every significant task to ensure quality, capture learnings, and maintain momentum.

## Post-Task Protocol

### 1. Verification
```yaml
verify:
  - Does the output meet acceptance criteria?
  - Were there any errors or warnings?
  - Is the output consistent with project standards?
  - Did tests pass (if applicable)?
```

### 2. Documentation
```yaml
document:
  - What was done (brief summary)
  - Key decisions made and rationale
  - Any deviations from plan and why
  - Known limitations or tech debt introduced
  - Follow-up tasks identified
```

### 3. Learning Capture
```yaml
learn:
  - Was the initial approach correct? (if not, what was better?)
  - Were there any surprises?
  - Did the token budget match actual usage?
  - New patterns discovered?
  - Skills or knowledge gained?

  # Feed into adaptive/learning-engine.md
  update_learning_engine:
    - Task type effectiveness data
    - Approach success/failure data
    - Token usage accuracy data
```

### 4. Momentum Maintenance
```yaml
momentum:
  - Report completion to user (scaled by task significance)
  - Suggest next task from queue
  - Maintain energy: "Done. [Next suggestion]"
  - Don't let the user stall between tasks
```

### 5. Cleanup
```yaml
cleanup:
  - Compress task context in working memory
  - Archive detailed task data to persistent storage
  - Update behavior profiles if significant patterns
  - Update task tracking (mark complete)
```

## Post-Task Reporting Levels

| Task Complexity | Report Level |
|----------------|-------------|
| Trivial | Silent or one-line: "Done." |
| Moderate | Brief summary: "Done: [what]. Result: [outcome]." |
| Complex | Detailed summary with key decisions and follow-ups |
| Failed | Full analysis: what happened, why, and proposed next steps |

## After-Action Review (Complex Tasks Only)

For tasks rated "complex" or that took longer than expected:

```yaml
after_action_review:
  what_happened: "[narrative]"
  what_went_well: "[list]"
  what_could_improve: "[list]"
  root_causes: "[for any issues]"
  action_items: "[specific improvements]"
  soc_updates_needed: "[any process changes]"
```

## Follow-Up Task Generation

After completing a task, NZT checks:
```yaml
follow_ups:
  - Are there related tasks that should be done?
  - Did this task uncover new issues?
  - Are there optimization opportunities?
  - Should documentation be updated?
  - Is testing coverage adequate?

  # Auto-queue follow-ups at appropriate priority
  auto_queue_rules:
    - Critical follow-ups → Queue at P1
    - Standard follow-ups → Queue at P3
    - Nice-to-have → Queue at P4
    - NZT self-improvement → Queue at P4 background
```

---

*NZT Post-Task Hook v1.0*
*Every completion is a foundation for the next achievement.*
*Designed by Adrian Dunkley | Maestro AI Lab*
