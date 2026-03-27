# NZT User Cognitive Profile

> This document is a **living file**. NZT updates it automatically after each session based on observed patterns and explicit preferences. The user can also edit it directly at any time.

## User Identity

```yaml
name: "[Auto-detected or user-provided]"
role: "[User's primary role/title]"
domain: "[Primary field of work]"
timezone: "[Auto-detected]"
session_count: 0
last_session: null
nzt_level: 3  # Current autonomy level (1-5)
```

## Work Patterns

### Observed Preferences
```yaml
communication_style: null        # concise | detailed | mixed
decision_speed: null             # fast | deliberate | context-dependent
focus_duration: null             # average deep work session length
peak_hours: null                 # when user does their best work
task_switching: null             # frequent | moderate | minimal
feedback_preference: null        # direct | diplomatic | data-driven
```

### Project Context
```yaml
active_projects: []
current_priorities: []
upcoming_deadlines: []
recurring_tasks: []
blocked_items: []
```

## Cognitive Preferences

### Learning Style
```yaml
primary: null                    # visual | textual | example-driven | conceptual
prefers_analogies: null          # true | false
prefers_code_examples: null      # true | false
explanation_depth: null          # surface | moderate | deep
```

### Decision Framework
```yaml
risk_tolerance: null             # conservative | moderate | aggressive
data_needs: null                 # minimal | moderate | comprehensive
delegation_comfort: null         # low | medium | high
review_preference: null          # pre-approval | post-review | trust-based
```

## Interaction History

### Patterns Detected
```yaml
common_tasks: []
frequently_used_tools: []
preferred_workflows: []
pain_points: []
strengths: []
```

### Calibration Notes
```yaml
# NZT adds observations here after each session
# Format: [date] - [observation]
notes: []
```

## Trust & Autonomy

### Pre-Authorized Actions
```yaml
# Actions NZT can take without asking
authorized:
  - Run tests after code changes
  - Format and lint code
  - Update documentation
  - Create git commits with descriptive messages
  - Organize and prioritize task lists
  - Compress and summarize long outputs
```

### Requires Confirmation
```yaml
# Actions that always need user approval
confirm:
  - Push to remote repositories
  - Delete files or data
  - Send messages to external services
  - Make architectural decisions
  - Modify CI/CD pipelines
  - Change security configurations
```

### Escalation Triggers
```yaml
# Conditions that increase NZT's caution level
escalate:
  - Unfamiliar technology stack
  - Production environment changes
  - Financial or legal implications
  - Multi-team impact decisions
  - Data privacy concerns
```

---

*Last updated: [NZT will auto-populate]*
*Profile version: 1.0*
*NZT Mega Skill by Adrian Dunkley | Maestro AI Lab*
