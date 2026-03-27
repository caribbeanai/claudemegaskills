# NZT Hook - Pre-Task

> Runs before every significant task to ensure preparation, alignment, and optimal execution setup.

## Pre-Task Checklist

When NZT identifies a new task (explicit or inferred):

### 1. Task Classification
```yaml
classify:
  type: "[bug_fix | feature | research | review | admin | creative | other]"
  priority: "[P0 | P1 | P2 | P3 | P4]"
  complexity: "[trivial | moderate | complex]"
  estimated_duration: "[< 5min | 5-30min | 30min+ | unknown]"
  domain: "[familiar | partially_familiar | unfamiliar]"
```

### 2. Context Check
```yaml
context_check:
  - Is this related to the current focus? (yes → continue, no → flag context switch)
  - Do we have all needed information? (yes → proceed, no → gather)
  - Are there dependencies? (yes → check status, no → proceed)
  - Is this a duplicate of a previous task? (yes → reference prior work)
```

### 3. Approach Selection
```yaml
approach:
  - Select simplest viable approach
  - Check if known pattern exists in SOC docs
  - Identify tools needed
  - Estimate token budget (assign tier)
  - Determine autonomy level for this task
```

### 4. Focus Protection
```yaml
focus_check:
  - Is user currently in deep work on something else?
    → If yes and new task is < P1: Queue for later
    → If yes and new task is P0/P1: Alert with priority context
  - Will this task cause an unplanned context switch?
    → If yes: Save current context state before switching
  - Is this task aligned with session goals?
    → If no: Flag to user
```

### 5. Ready Signal
```yaml
ready:
  - Internal: Task classified, approach selected, context loaded
  - User-facing (if applicable): Brief task acknowledgment
  - Format: "On it: [task summary]. Approach: [brief plan]."
  - For trivial tasks: Silent execution, no acknowledgment needed
```

## Pre-Task Decision Tree

```
New task identified
├── Is it trivial? (< 2 steps, well-understood)
│   └── YES → Skip pre-task, execute directly
├── Is it in the current focus area?
│   ├── YES → Classify and proceed
│   └── NO → Flag context switch, save state
├── Is it pre-authorized for autonomous execution?
│   ├── YES → Execute, report after
│   └── NO → Follow escalation matrix
└── Does it require research first?
    ├── YES → Spawn research (possibly via Cowork)
    └── NO → Proceed with execution
```

## Task Queue Integration

If the pre-task check reveals the task should be queued:
```yaml
queue_entry:
  task: "[description]"
  priority: "[P level]"
  reason_queued: "[why not now]"
  unblock_condition: "[what needs to happen first]"
  queued_at: "[timestamp]"
```

---

*NZT Pre-Task Hook v1.0*
*Preparation prevents poor performance.*
*Designed by Adrian Dunkley | Maestro AI Lab*
