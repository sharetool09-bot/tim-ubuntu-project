# Contributing and Project Standards

## Purpose

This document defines the standards used when adding labs, documentation, scripts, configurations, or other material to the Tim Ubuntu Project.

The repository should remain:

- Organized
- Understandable
- Reproducible
- Safe
- Professional
- Useful as a learning record

## Before Starting Work

Synchronize the repository:

```bash
git pull
git status
```

Confirm the working tree is in the expected state.

## Documentation Standard

Every practical lab should use `LAB_TEMPLATE.md`.

Important labs should document:

- Objective
- Why the topic matters
- Prerequisites
- Expected result
- Environment
- Risk
- Commands
- Command explanations
- Configuration changes
- Verification
- Evidence
- Problems
- Troubleshooting
- Resolution
- Rollback
- Security considerations
- Agentic workflow
- Manual verification
- Lessons learned
- Real-world use case
- Completion criteria

## File Naming

Prefer lowercase names with hyphens.

Good:

```text
users-and-groups.md
ssh-key-authentication.md
nginx-basic-server.md
dns-troubleshooting.md
```

Avoid vague names such as:

```text
Lab1FINALNEW.md
stuff.md
test2.md
```

## Directory Structure

Create directories when they are actually needed.

Example:

```text
tim-ubuntu-project/
├── README.md
├── PROGRESS.md
├── ROADMAP.md
├── LAB_TEMPLATE.md
├── AGENTIC_WORKFLOW.md
├── CONTRIBUTING.md
├── level-2-linux-admin/
├── level-3-networking/
├── level-4-automation/
├── level-5-infrastructure/
└── level-6-agentic-operations/
```

Do not create large numbers of empty directories.

## Git Workflow

Before editing:

```bash
git pull
git status
```

After editing:

```bash
git diff
git status
```

Stage specific files:

```bash
git add filename
```

Review staged changes:

```bash
git diff --cached
```

Commit:

```bash
git commit -m "Describe the change"
```

Push:

```bash
git push
```

## Commit Messages

Good examples:

```text
Add Linux users and groups lab
Document SSH key authentication
Add DNS troubleshooting lab
Update agentic workflow verification rules
```

Avoid vague messages such as:

```text
update
stuff
changes
final
test
```

## Git Safety

Do not blindly run:

```bash
git add .
```

when sensitive files may exist.

Prefer reviewing and staging specific files.

## Secrets

Never commit:

- Passwords
- API tokens
- Private SSH keys
- Secret keys
- Authentication cookies
- VPN secrets
- Production credentials
- Confidential customer information
- Company-sensitive data

Before committing, review:

```bash
git diff --cached
```

## Sanitization

Technical evidence should be sanitized when necessary.

Consider removing or masking:

- Public IP addresses when unnecessary
- Internal hostnames
- Usernames
- Customer names
- Email addresses
- Tokens
- Account IDs
- Sensitive paths
- Credentials

Keep enough technical detail to demonstrate the process without exposing unnecessary sensitive information.

## Commands

Record important commands exactly when practical and explain what they do.

Documentation should not be only a list of unexplained commands.

## Verification

Every meaningful configuration change should include verification.

Examples:

```bash
systemctl status nginx
ss -lntup
curl http://localhost
dig example.com
```

A change is not considered complete until it has been verified.

## Rollback

Changes with meaningful risk should include rollback instructions.

Examples:

- Restore a configuration backup
- Remove a route
- Remove a firewall rule
- Restore permissions
- Disable a new service
- Revert a Git change
- Restore a VM snapshot

## Evidence

Useful evidence may include:

- Command output
- Sanitized logs
- Screenshots
- Diagrams
- Configuration snippets
- Test results

Evidence should support the conclusion that the task worked.

## Agentic Work

When AI or an agent performs meaningful technical work, follow `AGENTIC_WORKFLOW.md`.

Document:

- What the agent did
- Commands
- Files
- Permissions
- Risks
- Verification
- Rollback
- Final result

Do not hide meaningful agent involvement.

## Multi-Device Workflow

### GitHub Codespaces

Primary project environment.

Before working:

```bash
git pull
git status
```

After working:

```bash
git diff
git status
git add <filename>
git commit -m "Describe the change"
git push
```

### iSH on iOS

Mobile project environment.

Project path:

```text
~/tim-ubuntu-project
```

Before working:

```bash
git pull
git status
```

After working:

```bash
git diff
git status
git add <filename>
git commit -m "Describe the change"
git push
```

Always pull before switching environments to reduce merge conflicts.

## Quality Standard

A completed lab should allow another technical person to understand:

- What was attempted
- Why it was attempted
- What environment was used
- What commands were executed
- What changed
- How the result was verified
- What problems occurred
- How they were solved
- How the change can be reversed
- What was learned

## Final Principle

Documentation should prove understanding, not simply prove that commands were copied and executed.

The repository should become more useful as technical ability improves.
