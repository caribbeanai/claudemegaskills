# NZT Hook - Session End

> Gracefully closes the NZT session, persisting state, capturing learnings, and setting up the next session for success.

## Session End Sequence

```
┌─────────────────────────────────────────────┐
│           NZT SESSION END                   │
│                                             │
│  1. Capture Session Summary                 │
│  2. Persist State                           │
│  3. Queue Follow-Ups                        │
│  4. Self-Improvement Cycle                  │
│  5. Deliver Closing Briefing                │
│  6. Shutdown                                │
│                                             │
│  Status: STANDBY                            │
└─────────────────────────────────────────────┘
```

## Step 1: Capture Session Summary
```yaml
summary:
  session_duration: "[estimated]"
  tasks_completed: []
  tasks_in_progress: []
  tasks_queued: []
  key_decisions: []
  blockers_identified: []
  highlights: "[biggest achievement]"
```

## Step 2: Persist State
```yaml
persist:
  - Update nzt/persona/user-profile.md with new learnings
  - Update nzt/adaptive/behavior-profiles.md with session patterns
  - Save incomplete task state for resumption
  - Commit NZT document changes to git (if significant)
```

## Step 3: Queue Follow-Ups
```yaml
follow_ups:
  - Move in-progress tasks to "resume next session" queue
  - Create tasks for any commitments made
  - Schedule any identified background work
  - Note any external dependencies to check next session
```

## Step 4: Self-Improvement Cycle
```yaml
improve:
  - Run quick self-assessment (see adaptive/self-improvement.md)
  - Log session metrics
  - Identify one improvement to apply
  - Update relevant SOC doc if process change identified
```

## Step 5: Deliver Closing Briefing
```yaml
briefing_format: |
  ---
  NZT Session Complete
  ---

  **Accomplished**:
  - [completed task 1]
  - [completed task 2]

  **In Progress** (will resume):
  - [task] - [state saved]

  **Next Session**:
  - [suggested starting point]
  - [any time-sensitive items]

  [Motivational close matching user's style]
  ---

closing_styles:
  data_driven: "Solid session - [N] tasks completed, [X]% above your average."
  motivational: "Strong progress. Rest up - we pick up where we left off."
  minimal: "Saved. See you next time."
  challenge: "Good run. Tomorrow we tackle [hard thing]."
```

## Step 6: Shutdown
```yaml
shutdown:
  - Flush all pending writes
  - Verify git state is clean (or changes committed)
  - Set NZT status to STANDBY
  - Release working memory
```

## End-of-Day vs. Mid-Day End

### Mid-Day Session End
- Lighter summary
- Focus on "what to pick up next"
- Don't run weekly review checks
- Quick persist and queue

### End-of-Day Session End
- Full day summary
- Run daily ops end-of-day tasks
- Check if weekly review is due
- Comprehensive profile updates
- Tomorrow planning

## Trigger Detection

NZT infers session end from:
- User explicitly says "done", "that's all", "signing off"
- User says "end of day", "wrapping up", "logging off"
- Conversation reaches a natural conclusion
- User doesn't respond for extended period

When inferred (not explicit), NZT asks:
"Looks like we're wrapping up. Want me to run the session close? Or are you still going?"

---

*NZT Session End Hook v1.0*
*End with clarity. Start with momentum.*
*Designed by Adrian Dunkley | Maestro AI Lab*
