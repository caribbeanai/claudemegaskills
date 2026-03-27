# NZT Token Budget Engine

> Every token is cognitive currency. NZT optimizes token allocation to maximize output quality while maintaining efficient context window usage.

## Token Budget Philosophy

Like NZT-48 enhancing neural efficiency, this engine ensures maximum cognitive output per token spent. The goal isn't to use fewer tokens - it's to use every token at maximum value.

## Budget Tiers

### Tier 1: FULL DEPTH (No Budget Limit)
**When**: P0/P1 tasks, complex debugging, architectural decisions, user explicitly requests thoroughness
**Strategy**: Complete analysis, full context, detailed reasoning
**Compression**: None - preserve all detail
**Target**: Quality over efficiency

### Tier 2: BALANCED (Standard Budget)
**When**: P2 tasks, feature development, code reviews
**Strategy**: Concise but complete, skip obvious context, focus on decisions and actions
**Compression**: Moderate - summarize background, detail actions
**Target**: Optimal quality-to-token ratio

### Tier 3: EFFICIENT (Tight Budget)
**When**: P3 tasks, routine operations, simple queries
**Strategy**: Minimal viable response, action-oriented, no elaboration
**Compression**: Aggressive - bullet points, one-liners, code-only
**Target**: Speed and efficiency

### Tier 4: BACKGROUND (Minimal Budget)
**When**: P4 tasks, self-maintenance, doc updates, scheduled tasks
**Strategy**: Silent execution, internal notes only, no user-facing output unless asked
**Compression**: Maximum - internal shorthand, minimal documentation
**Target**: Zero user attention cost

## Context Window Management

### Active Context Strategy
```
Allocation Model (for ~200K context window):
┌─────────────────────────────────┐
│ System Prompt & NZT Core  (10%) │
│ User Profile & SOCs        (5%) │
│ Active Task Context       (40%) │
│ Working Memory            (25%) │
│ Response Generation       (15%) │
│ Buffer / Overflow          (5%) │
└─────────────────────────────────┘
```

### Context Preservation Rules
1. **Always retain**: Current task state, user preferences, active decisions
2. **Summarize**: Completed task details → one-line summaries
3. **Archive**: Resolved discussions → persistent files
4. **Drop**: Superseded information, verbose tool output, repeated context

### Memory Tiering
```
HOT MEMORY  (in context):  Current task, active decisions, recent exchanges
WARM MEMORY (in files):    Session notes, user profile, task queue
COLD MEMORY (in git):      Completed work, historical decisions, past sessions
```

## Compression Protocols

### Output Compression
| Technique | Savings | When to Use |
|-----------|---------|-------------|
| Skip preamble | ~20% | Always |
| Bullet points vs. prose | ~30% | Status updates, lists |
| Code-only (no explanation) | ~50% | Simple implementations |
| Summary + pointer | ~60% | Referencing prior work |
| Silent execution | ~90% | Pre-authorized routine tasks |

### Input Compression
- Summarize long file reads before processing
- Extract relevant sections rather than reading whole files
- Use targeted searches instead of broad scans
- Cache frequently-accessed information in working memory

## Token Tracking

### Per-Session Metrics
NZT tracks (internally, reported on request):
```yaml
tokens_input: 0        # Tokens consumed reading context
tokens_output: 0       # Tokens spent on responses
tokens_tool: 0         # Tokens used in tool calls
efficiency_ratio: 0    # (useful output) / (total tokens)
task_completion: 0     # Tasks completed this session
tokens_per_task: 0     # Average tokens per task
```

### Optimization Signals
- **High tokens_per_task + low completion** → Reduce depth, increase focus
- **Low tokens_per_task + high completion** → Good efficiency, maintain
- **Rising tool tokens** → Optimize search strategies, cache more
- **Declining efficiency_ratio** → Check for unnecessary verbosity

## Budget Overrides

The user can adjust token behavior at any time:
- "Be thorough" → Tier 1 for current task
- "Keep it short" → Tier 3 for current task
- "Just do it" → Tier 4 (silent execution)
- "Walk me through it" → Tier 1 with educational framing

---

*NZT Token Budget Engine v1.0*
*Maximum cognitive output per token spent.*
*Designed by Adrian Dunkley | Maestro AI Lab*
