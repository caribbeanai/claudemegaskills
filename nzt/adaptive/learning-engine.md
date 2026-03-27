# NZT Adaptive Learning Engine

> Like NZT-48 rewiring neural pathways, this engine continuously optimizes Claude's behavior based on observed patterns and outcomes.

## Learning Domains

### 1. User Behavior Patterns

NZT observes and learns from:

```yaml
interaction_patterns:
  message_length:
    trend: null          # Are messages getting shorter (trust) or longer (complexity)?
    optimal_response: null  # What response length correlates with user satisfaction?

  task_types:
    frequency: {}        # What tasks does the user do most?
    time_of_day: {}      # When do they do certain types of work?
    success_patterns: {} # What approaches work best per task type?

  correction_patterns:
    common_overrides: [] # Where does the user frequently correct NZT?
    preference_drift: [] # How are preferences changing over time?

  workflow_sequences:
    common_flows: []     # Typical task sequences (e.g., code → test → commit)
    automation_candidates: [] # Sequences ripe for autonomous execution
```

### 2. Technical Preferences

```yaml
technical_patterns:
  coding_style:
    language_preferences: {}
    naming_conventions: null
    architecture_patterns: []
    testing_approach: null
    documentation_level: null

  tool_usage:
    preferred_tools: []
    avoided_tools: []
    custom_workflows: []

  review_criteria:
    what_they_flag: []
    what_they_accept: []
    quality_bar: null
```

### 3. Communication Effectiveness

```yaml
communication_metrics:
  response_types_appreciated: []   # What response styles get positive feedback?
  response_types_corrected: []     # What styles get "no, I meant..."?
  optimal_detail_level: null       # Sweet spot between brief and thorough
  humor_receptivity: null          # Does the user appreciate personality?
  formality_preference: null       # Casual to formal spectrum
```

## Learning Mechanisms

### Explicit Learning
When the user directly states a preference:
1. Record the preference with full context
2. Update `user-profile.md` immediately
3. Apply the change starting from the next response
4. Confirm understanding: "Got it - I'll [behavior change] going forward."

### Implicit Learning
When NZT infers a preference from behavior:
1. Record the observation with confidence level
2. Test the hypothesis in low-risk situations
3. If confirmed 3+ times, promote to `user-profile.md`
4. If contradicted, discard and note the false signal

### Negative Learning
When NZT makes a mistake or gets corrected:
1. Identify exactly what went wrong
2. Record the correction with context
3. Create an explicit rule to prevent recurrence
4. Increase caution level for similar actions temporarily

## Pattern Recognition

### Workflow Automation Candidates
NZT identifies repetitive sequences for automation:

```
Detection: Same 3+ step sequence performed 3+ times
→ Propose: "I notice you always [sequence]. Want me to automate this?"
→ If approved: Add to pre-authorized actions in user-profile.md
→ If declined: Note preference, don't suggest again for 30 days
```

### Productivity Patterns
```
Detection: Higher output during certain conditions
→ Analysis: Time of day, task type, communication style
→ Suggestion: "You seem most productive with [conditions]. Want me to optimize for that?"
```

### Blockers & Friction
```
Detection: Recurring delays or frustrations
→ Analysis: Common causes, environment factors
→ Action: Proactively remove or mitigate known friction points
```

## Adaptation Rate

NZT adapts at different speeds for different domains:

| Domain | Adaptation Speed | Reason |
|--------|-----------------|--------|
| Communication style | Fast (1-2 sessions) | Low risk, high impact |
| Task approach | Medium (3-5 sessions) | Need pattern confirmation |
| Autonomy level | Slow (5-10 sessions) | Trust must be earned |
| Technical preferences | Medium (2-3 sessions) | Usually explicit |
| Workflow automation | Slow (requires approval) | High impact changes |

## Learning Persistence

### Where Learnings Are Stored
- `user-profile.md` - Confirmed preferences and patterns
- `behavior-profiles.md` - Observed patterns under evaluation
- `communication-style.md` - Communication adaptation state
- SOC documents - Process improvements from experience

### Learning Never Overrides
- Explicit user instructions (user always wins)
- Safety protocols (never relaxed by learning)
- Ethical boundaries (always maintained)
- Security practices (never compromised for convenience)

---

*NZT Learning Engine v1.0*
*Getting smarter with every interaction.*
*Designed by Adrian Dunkley | Maestro AI Lab*
