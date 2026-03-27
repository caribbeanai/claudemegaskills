# NZT Integration - Claude Computer

> Claude Computer gives NZT hands. Direct system interaction for file management, browser automation, and desktop operations.

## Overview

Claude Computer enables NZT to interact directly with the user's system - managing files, automating browser tasks, running applications, and performing system operations. This extends NZT from a cognitive partner to a full execution partner.

## Capabilities

### File System Operations
```yaml
file_ops:
  - Navigate and manage directories
  - Create, move, copy, delete files
  - Search file contents and metadata
  - Organize project structures
  - Batch file operations
  - Archive and backup management
```

### Browser Automation
```yaml
browser_ops:
  - Open and navigate web pages
  - Fill forms and submit data
  - Extract information from web pages
  - Take screenshots for reference
  - Monitor web services
  - Download resources
```

### Application Interaction
```yaml
app_ops:
  - Launch and manage applications
  - Interact with GUI elements
  - Automate repetitive workflows
  - Copy data between applications
  - Configure settings and preferences
```

### System Management
```yaml
system_ops:
  - Monitor system resources
  - Manage processes
  - Check service status
  - Environment configuration
  - Package management
```

## NZT + Computer Use Patterns

### Pattern 1: Research & Compile
```yaml
name: research_compile
description: Gather information from multiple sources and compile
steps:
  1. Open relevant web pages
  2. Extract key information
  3. Compile into structured format
  4. Present to user or save to file
use_case: "Market research, documentation gathering, competitive analysis"
```

### Pattern 2: Setup & Configure
```yaml
name: setup_configure
description: Set up development environments and configure tools
steps:
  1. Install required packages
  2. Configure environment variables
  3. Set up project structure
  4. Verify everything works
  5. Document the setup
use_case: "New project setup, environment configuration, tool installation"
```

### Pattern 3: Monitor & Alert
```yaml
name: monitor_alert
description: Watch for conditions and notify user
steps:
  1. Periodically check target (URL, file, process)
  2. Compare against expected state
  3. Alert user if conditions change
  4. Log monitoring data
use_case: "Deployment monitoring, service health, CI/CD status"
```

### Pattern 4: Automate Workflow
```yaml
name: automate_workflow
description: Execute multi-step workflows across applications
steps:
  1. Receive workflow trigger
  2. Execute steps across system/browser/apps
  3. Handle errors and edge cases
  4. Report results
use_case: "Data entry, report generation, cross-platform operations"
```

## Safety Protocols for Computer Use

### Before Any System Action
```yaml
safety_check:
  - Is this action pre-authorized? (check user-profile.md)
  - Is this action reversible?
  - Could this affect data integrity?
  - Is user confirmation needed? (check escalation-matrix.md)
  - Am I operating in the correct environment? (dev vs prod)
```

### Restricted Actions (Always Confirm)
- Deleting files outside project directory
- Modifying system configuration files
- Installing system-level packages
- Accessing sensitive directories (~/.ssh, ~/.aws, etc.)
- Making network requests to unfamiliar endpoints
- Running scripts from untrusted sources

### Logging
All Computer Use actions are logged:
```yaml
action_log:
  timestamp: "[when]"
  action: "[what was done]"
  target: "[what was affected]"
  result: "[outcome]"
  reversible: true/false
```

## Integration with NZT Core

Computer Use is governed by:
- **Decision Framework** (`soc/decision-framework.md`) - What to do autonomously vs. ask
- **Escalation Matrix** (`soc/escalation-matrix.md`) - When to escalate
- **Token Budget** (`token-management/budget-engine.md`) - Resource allocation
- **Focus Protocols** (`soc/focus-protocols.md`) - When to act silently

---

*NZT Computer Integration v1.0*
*From thinking to doing.*
*Designed by Adrian Dunkley | Maestro AI Lab*
