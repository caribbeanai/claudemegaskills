# NZT Scheduled Tasks - Daily Operations

> Autonomous daily operations that run at session start or on schedule to keep you sharp and productive.

## Session Start Tasks

These run automatically when a new NZT session begins:

### 1. Context Restoration
```yaml
task: restore_context
trigger: session_start
priority: P1
actions:
  - Read nzt/persona/user-profile.md
  - Check git log for recent activity
  - Load active task queue
  - Detect current project context from working directory
output: Internal context (no user output unless issues found)
```

### 2. Pending Task Review
```yaml
task: review_pending_tasks
trigger: session_start
priority: P1
actions:
  - Scan for tasks marked QUEUED or BLOCKED
  - Check if blockers have been resolved
  - Prioritize tasks for the session
  - Prepare session briefing
output: Session briefing delivered to user
```

### 3. Scheduled Task Check
```yaml
task: check_scheduled
trigger: session_start
priority: P2
actions:
  - Check if any scheduled maintenance is overdue
  - Run any tasks that were queued for "next session"
  - Report completed background tasks
output: Brief report if actions were taken
```

## Recurring Daily Tasks

### Morning Briefing (First Session of Day)
```yaml
task: morning_briefing
trigger: first_session_of_day
priority: P2
content: |
  NZT Daily Briefing:

  **Yesterday's Progress**: [summary from last session]
  **Today's Priorities**: [based on user profile and pending tasks]
  **Upcoming Deadlines**: [any time-sensitive items]
  **Suggested Focus**: [recommended first task based on patterns]
```

### End-of-Day Wrap (Detect Last Session)
```yaml
task: eod_wrap
trigger: session_end_late_day  # or user says "done for the day"
priority: P2
actions:
  - Summarize day's accomplishments
  - List carry-over items for tomorrow
  - Update behavior profiles with day's patterns
  - Queue any follow-up tasks
  - Update user-profile.md
output: |
  Day Summary:
  - Completed: [list]
  - Carrying Over: [list]
  - Tomorrow's Suggested Start: [recommendation]
```

### Profile Sync
```yaml
task: profile_sync
trigger: end_of_session
priority: P4
actions:
  - Update user-profile.md with session learnings
  - Update behavior-profiles.md with observed patterns
  - Commit NZT doc changes to git (if significant updates)
output: Silent (no user-facing output)
```

## Task Templates

### Recurring Task Definition
```yaml
template:
  name: "[task name]"
  schedule: "[daily | weekly | session_start | session_end | on_demand]"
  priority: "[P0-P4]"
  autonomy: "[silent | notify | ask]"
  actions: []
  success_criteria: "[how to know it's done]"
  failure_handling: "[what to do if it fails]"
```

### User-Created Recurring Tasks
Users can create recurring tasks by saying:
- "Every morning, remind me to..."
- "At the start of each session, check..."
- "Daily, run the test suite and report..."

NZT stores these in this file and executes on schedule.

```yaml
user_recurring_tasks: []
# Example:
# - name: "Daily standup prep"
#   schedule: "first_session"
#   actions:
#     - Review git commits since yesterday
#     - Summarize work done
#     - List blockers
#   output: "Standup notes ready for copy-paste"
```

---

*NZT Daily Operations v1.0*
*Consistency creates capability.*
*Designed by Adrian Dunkley | Maestro AI Lab*
