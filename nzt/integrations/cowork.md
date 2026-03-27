# NZT Integration - Claude Cowork

> Claude Cowork enables parallel agent collaboration. NZT orchestrates Cowork agents as extensions of your cognitive capacity - multiple trains of thought running simultaneously.

## Overview

Claude Cowork allows NZT to spawn specialized sub-agents that work in parallel on independent tasks. Think of it as NZT's ability to "split focus" without losing quality on any thread.

## When to Use Cowork

### Ideal Scenarios
- **Independent research tasks** - Investigating multiple options simultaneously
- **Parallel implementations** - Building unrelated components at the same time
- **Review + Build** - One agent reviews while another implements
- **Search + Execute** - One agent searches for solutions while you continue working
- **Test + Develop** - Running tests in background while developing

### Not Ideal For
- Tightly coupled tasks that depend on each other's output
- Tasks requiring real-time user input at each step
- Trivial tasks that finish faster than agent setup overhead
- Tasks requiring shared mutable state

## Agent Orchestration Patterns

### Pattern 1: Scout & Execute
```yaml
name: scout_and_execute
description: Research first, then implement with full context
flow:
  1. Spawn scout agent to research/explore
  2. Continue primary work or wait
  3. Receive scout findings
  4. Execute implementation with full knowledge
use_when: "Unfamiliar territory, need to understand before acting"
```

### Pattern 2: Parallel Tracks
```yaml
name: parallel_tracks
description: Multiple independent workstreams running simultaneously
flow:
  1. Identify independent tasks
  2. Spawn agent per task
  3. Continue primary work
  4. Collect results as agents complete
  5. Integrate outputs
use_when: "Multiple unrelated tasks, time pressure"
```

### Pattern 3: Review Pipeline
```yaml
name: review_pipeline
description: Build and review in parallel
flow:
  1. Primary agent implements
  2. Review agent checks completed work
  3. Feedback loop until quality bar met
use_when: "High-quality output required, enough scope for pipeline"
```

### Pattern 4: Exploration Fan-Out
```yaml
name: exploration_fan_out
description: Explore multiple approaches simultaneously
flow:
  1. Define the problem
  2. Spawn agents for different approaches
  3. Compare results
  4. Select best approach
  5. Proceed with chosen path
use_when: "Multiple viable approaches, need to compare"
```

## Token Budget for Cowork

```yaml
cowork_budget:
  primary_agent: 60%    # Main user-facing work
  cowork_agents: 30%    # Combined budget for all sub-agents
  coordination: 10%     # NZT orchestration overhead

  per_agent_limits:
    max_agents_concurrent: 3
    per_agent_max_budget: 15%
    prefer_focused_tasks: true  # Give agents specific, bounded tasks
```

## Agent Task Templates

### Research Agent
```yaml
template: research
prompt_pattern: |
  Research [topic]. Return:
  1. Key findings (bulleted)
  2. Recommended approach
  3. Risks and considerations
  4. Relevant code/files found
budget: Tier 2
```

### Implementation Agent
```yaml
template: implement
prompt_pattern: |
  Implement [feature/fix] in [location].
  Requirements: [specs]
  Constraints: [limits]
  Return: Changed files and summary
budget: Tier 2
```

### Exploration Agent
```yaml
template: explore
prompt_pattern: |
  Explore the codebase for [pattern/concept].
  Find: [what to look for]
  Return: File paths, relevant code, and analysis
budget: Tier 3
```

## Coordination Rules

1. **Clear boundaries** - Each agent gets a well-defined, independent scope
2. **No overlapping writes** - Two agents never modify the same file
3. **Results integration** - NZT (primary) integrates all agent outputs
4. **Failure isolation** - One agent's failure doesn't block others
5. **Progress visibility** - Report agent status at natural breaks

---

*NZT Cowork Integration v1.0*
*Multiply your cognitive throughput.*
*Designed by Adrian Dunkley | Maestro AI Lab*
