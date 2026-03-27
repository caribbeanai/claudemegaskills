# NZT Scheduled Tasks - Self-Maintenance

> A high-performance system requires regular maintenance. NZT maintains itself so you don't have to.

## Maintenance Schedule

### Every Session End
```yaml
session_maintenance:
  priority: P4
  autonomy: silent
  tasks:
    - Compress completed task records
    - Update behavior profiles with session data
    - Clean up working memory artifacts
    - Stage NZT doc changes for commit
  duration: "<30 seconds"
```

### Weekly (During Weekly Review)
```yaml
weekly_maintenance:
  priority: P3
  autonomy: notify
  tasks:
    - Audit SOC documents for stale protocols
    - Review and prune observation logs
    - Validate user-profile.md accuracy
    - Check for conflicting rules across documents
    - Optimize token budget allocations based on weekly data
    - Archive resolved items from behavior profiles
  duration: "~2 minutes"
```

### Monthly (During Monthly Rollup)
```yaml
monthly_maintenance:
  priority: P3
  autonomy: notify
  tasks:
    - Full audit of all NZT documents
    - Remove deprecated patterns and rules
    - Consolidate duplicate or overlapping SOCs
    - Review escalation matrix calibration
    - Assess overall NZT effectiveness
    - Version bump NZT documents if significant changes
    - Generate monthly improvement report
  duration: "~5 minutes"
```

## Document Health Checks

### Consistency Verification
```yaml
check_consistency:
  - user-profile.md autonomy level matches escalation-matrix.md thresholds
  - Pre-authorized actions in user-profile.md align with decision-framework.md
  - Communication style preferences match observed patterns
  - Token budget tiers align with actual usage patterns
  - No contradictory rules across SOC documents
```

### Freshness Check
```yaml
check_freshness:
  - Flag documents not updated in 2+ weeks
  - Flag observations not promoted or discarded in 1+ week
  - Flag hypotheses under test for more than 5 sessions
  - Flag user-profile.md fields still at null after 3+ sessions
```

### Completeness Check
```yaml
check_completeness:
  - All required fields in user-profile.md populated
  - All SOC protocols have clear trigger conditions
  - All escalation levels have examples
  - Token budgets defined for all common task types
  - Scheduled tasks have success criteria and failure handling
```

## Self-Repair Protocols

### When Documents Conflict
1. Identify the conflicting rules
2. Check which was more recently updated
3. Check which has more supporting evidence
4. Resolve in favor of the more specific/recent rule
5. Log the resolution in improvement log

### When a Protocol Fails
1. Log the failure with full context
2. Analyze root cause
3. Propose fix (update protocol or add exception)
4. Apply fix if low risk, otherwise flag for user review
5. Monitor for recurrence

### When User Profile Seems Wrong
1. Don't silently change - flag to user
2. "I noticed [observation] doesn't match [profile setting]. Should I update?"
3. Update only with user confirmation
4. Log the correction for learning

## Version Control

NZT documents are versioned through git:
- Every significant update triggers a commit
- Commit messages describe what changed and why
- Git history serves as a changelog for NZT's evolution
- Can roll back any change if it causes issues

```yaml
versioning:
  strategy: "commit per significant change"
  message_format: "nzt: [document] - [change description]"
  examples:
    - "nzt: user-profile - updated communication preference to concise"
    - "nzt: soc/focus - added afternoon focus protocol based on pattern"
    - "nzt: weekly maintenance - archived stale observations"
```

---

*NZT Self-Maintenance v1.0*
*A well-maintained system is a reliable system.*
*Designed by Adrian Dunkley | Maestro AI Lab*
