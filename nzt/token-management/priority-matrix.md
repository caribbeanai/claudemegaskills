# NZT Token Priority Matrix

> Not all tasks deserve equal cognitive investment. This matrix maps task priority to token allocation strategy.

## Priority-Token Allocation

```
                    Token Investment
                    Low         Medium        High
                ┌───────────┬─────────────┬───────────┐
    Urgent      │ Quick Fix │ Focused     │ All-In    │
                │ P1+Simple │ P1+Moderate │ P0/P1     │
                │ Tier 3    │ Tier 2      │ Tier 1    │
                ├───────────┼─────────────┼───────────┤
    Important   │ Efficient │ Balanced    │ Thorough  │
                │ P2+Simple │ P2+Moderate │ P2+Complex│
                │ Tier 3    │ Tier 2      │ Tier 1    │
                ├───────────┼─────────────┼───────────┤
    Background  │ Silent    │ Batched     │ Scheduled │
                │ P4        │ P3          │ P3+Complex│
                │ Tier 4    │ Tier 3      │ Tier 2    │
                └───────────┴─────────────┴───────────┘
```

## Task-Specific Token Budgets

| Task Type | Budget Tier | Max Response Length | Tool Calls | Reasoning Depth |
|-----------|-------------|-------------------|------------|-----------------|
| Production bug | 1 | Unlimited | Unlimited | Full trace |
| Feature implementation | 2 | Moderate | As needed | Decision points |
| Code review | 2 | Moderate | Targeted reads | Key findings |
| Refactoring | 2 | Low-Medium | Targeted edits | Before/after |
| Documentation | 3 | Low | Minimal | Factual only |
| Test writing | 2 | Medium | Template-based | Coverage focused |
| Research | 1-2 | High | Search-heavy | Comprehensive |
| Status update | 3 | Very Low | None | Summary only |
| Self-improvement | 4 | Minimal | File updates | Internal only |

## Dynamic Budget Adjustment

NZT adjusts budgets based on real-time signals:

### Increase Budget When:
- Task complexity exceeds initial estimate
- Multiple failed approaches (need deeper analysis)
- User asks for more detail
- Stakes are high (production, security, data)
- Learning/teaching mode

### Decrease Budget When:
- Task is simpler than expected
- Pattern matches a known solution
- User signals urgency ("just fix it")
- Routine/repetitive task
- Deep in a focused session (minimize disruption)

## Parallel Task Token Splitting

When running multiple tasks via Cowork agents:

```yaml
allocation:
  primary_task: 60%     # User's current focus
  secondary_tasks: 25%  # Background parallel work
  system_overhead: 10%  # NZT meta-operations
  buffer: 5%            # Unexpected needs
```

---

*NZT Priority Matrix v1.0*
*Right-sizing cognitive investment for maximum throughput.*
*Designed by Adrian Dunkley | Maestro AI Lab*
