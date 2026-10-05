# Agentic Workflow Standard

## Purpose

This document defines how AI and agentic workflows should be used within the Tim Ubuntu Project.

The purpose of agentic automation is to improve efficiency without sacrificing technical understanding, safety, or control.

**AI should assist the work. AI should not hide the work.**

## Core Principle

Before trusting an automated result, understand enough of the underlying system to verify the result independently.

An agent reporting success is not proof of success.

## Agentic Workflow Lifecycle

For important agentic workflows:

1. Define the objective
2. Identify the environment
3. Determine required permissions
4. Inspect current state
5. Create a proposed action plan
6. Review the plan
7. Identify risks
8. Identify rollback options
9. Approve appropriate actions
10. Execute changes
11. Verify the result
12. Review logs and system state
13. Compare expected and actual results
14. Document what happened
15. Commit sanitized documentation

## Before the Agent Acts

Answer:

- What is the objective?
- What systems are involved?
- What commands may be executed?
- What files may be changed?
- What services may be affected?
- What permissions are required?
- What network access is required?
- What could fail?
- What is the rollback plan?
- How will success be verified?

## Least Privilege

Give agents only the permissions required for the task.

Prefer read-only before write access.

Prefer a normal user before `sudo` or root.

Prefer a narrow API scope before broad account access.

Avoid unnecessary administrative access.

## Proposed Actions

Before significant changes, the agent should describe its intended actions.

Example:

```text
1. Read Nginx configuration
2. Check configuration syntax
3. Read current service status
4. Read recent Nginx logs
5. Propose a configuration change
6. Create a backup
7. Apply the approved change
8. Validate configuration syntax
9. Reload Nginx
10. Verify HTTP response
```

The plan should be understandable before execution.

## Under-the-Hood Documentation

For important automated actions, record:

### Commands

Which commands were executed?

### Files

Which files were read and modified?

### Services

Which services were:

- Started
- Stopped
- Restarted
- Reloaded
- Enabled
- Disabled

### Processes

Which processes were inspected or modified?

### Network

Record:

- Connections
- Ports
- Routes
- DNS queries
- APIs
- Remote systems

### Permissions

Record:

- User context
- Group context
- `sudo` usage
- Root access
- API scopes

### Dependencies

Record:

- Packages
- Libraries
- Services
- APIs
- External tools

## Verification Standard

Agentic changes should be independently verified.

Examples:

```bash
systemctl status service
journalctl -u service
ss -lntup
ip addr
ip route
dig example.com
curl http://localhost
git diff
```

The exact verification depends on the task.

## Failure Modes

Possible failures include:

- Incorrect assumptions
- Wrong command
- Wrong target system
- Wrong file
- Syntax errors
- Incorrect permissions
- Service outage
- Network outage
- Broken routing
- DNS failure
- Firewall lockout
- Package conflicts
- Dependency mismatch
- Incomplete configuration
- Incorrect log interpretation
- False success report
- Partial execution

Consider these risks before high-impact changes.

## Rollback

Important changes should have a rollback plan when practical.

Examples:

- Configuration backup
- Git rollback
- Package downgrade
- Service restart
- Route removal
- Firewall rule removal
- Permission restoration
- VM snapshot
- Container redeployment

Rollback should also be verified.

## Human Approval

Human approval is especially important before:

- Deleting data
- Changing firewalls
- Changing routing
- Changing authentication
- Changing permissions
- Modifying production services
- Restarting critical services
- Changing DNS
- Changing VPN configuration
- Changing remote-access configuration
- Installing untrusted software
- Running destructive commands

## Manual vs Agentic Work

Manual work supports understanding, learning, troubleshooting, visibility, and control.

Agentic work supports speed, repetition, consistency, documentation, and routine validation.

A useful hybrid model is:

```text
Understand manually
        ↓
Automate repetitive work
        ↓
Verify manually
```

## Trust Model

Do not blindly trust:

- Generated commands
- Generated configuration
- Generated scripts
- Log interpretations
- Security recommendations
- Success messages
- Automated remediation

Review important changes before applying them and verify important results afterward.

## Sensitive Information

Agents should not unnecessarily receive:

- Passwords
- Private keys
- API secrets
- Authentication cookies
- Confidential customer data
- Unnecessary production data

Secrets must never be committed to GitHub.

## Documentation Requirement

When an agent materially contributes to a lab, record:

```text
Agent role:
Task:
Permissions:
Commands:
Files changed:
Services affected:
Network impact:
Risks:
Verification:
Rollback:
Result:
```

## Goal

The goal is not to avoid AI. The goal is to become skilled enough to use AI effectively.

A capable infrastructure professional should be able to:

- Understand a system
- Operate it manually
- Troubleshoot it
- Automate it
- Review automation
- Verify automation
- Recognize unsafe automation

Agentic tools should extend technical capability rather than replace technical understanding.
