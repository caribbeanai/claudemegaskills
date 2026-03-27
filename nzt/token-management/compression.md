# NZT Context Compression Protocols

> The brain doesn't store raw sensory data - it compresses, abstracts, and indexes. NZT does the same with context.

## Compression Strategies

### 1. Progressive Summarization
As information ages in context, compress it through stages:

```
Stage 0 (Raw):     Full verbatim content
Stage 1 (Highlighted): Key sentences and decisions preserved
Stage 2 (Summary):     One paragraph per topic
Stage 3 (Index):       One line per topic with pointer to source
Stage 4 (Archived):    Saved to file, removed from context
```

### 2. Decision Extraction
From any conversation segment, extract:
```yaml
decisions:
  - what: "[decision made]"
    why: "[brief rationale]"
    when: "[timestamp]"
    status: "[active/superseded]"
```

### 3. Task State Compression
Active tasks maintain full context. Completed tasks compress to:
```
[DONE] task_name | outcome: success/fail | key_output | follow_ups
```

### 4. Code Context Compression
When working with code:
- Keep: Current file being edited, function signatures, error messages
- Compress: File contents already reviewed → "Reviewed file.py: auth module, 200 lines, uses JWT"
- Drop: Verbose build/test output after extracting pass/fail results

## Working Memory Model

NZT maintains a compressed working memory:

```yaml
working_memory:
  session_goal: "[what we're trying to accomplish]"
  current_task: "[specific task in progress]"
  task_state: "[where we are in the task]"
  key_decisions: []      # Decisions made this session
  open_questions: []     # Unresolved items
  context_pointers: []   # "See file X for details on Y"
  user_state: "[current detected user state]"
```

This working memory is updated continuously and never compressed - it's the cognitive "scratchpad" that enables coherent multi-step work.

## Context Recovery

When context has been compressed or conversations are long:

1. **Check working memory** for current state
2. **Read persistent files** for full details if needed
3. **Review git log** for historical context
4. **Ask user** only if context cannot be recovered from files

### Recovery Priority
```
1. What are we doing right now?     → working_memory.current_task
2. What have we decided?            → working_memory.key_decisions
3. What's the broader goal?         → working_memory.session_goal
4. What happened before?            → git log, persistent files
5. What does the user prefer?       → nzt/persona/user-profile.md
```

## Anti-Patterns

- **Never** repeat information already in context just to fill space
- **Never** re-read files that haven't changed
- **Never** include full error traces when a one-line summary suffices
- **Never** explain decisions the user has already approved
- **Never** re-derive conclusions already reached

---

*NZT Compression Protocols v1.0*
*Efficient memory, effective cognition.*
*Designed by Adrian Dunkley | Maestro AI Lab*
