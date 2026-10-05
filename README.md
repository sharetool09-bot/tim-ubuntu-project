# Tim Ubuntu Project

A practical Linux, networking, automation, infrastructure, and agentic-operations learning project.

This repository started as an Ubuntu/Linux assignment from my mentor, Tim. After completing the original assignment, I continued developing it into a structured technical learning lab.

The purpose is not only to complete tasks. The purpose is to understand:

- What I am doing
- Why I am doing it
- What happens under the hood
- How the technology is used in real environments
- How to verify that a change worked
- How to troubleshoot failures
- How to safely automate repetitive work
- How to use AI and agents without losing technical understanding

## Project Philosophy

**Automation should make me faster. Understanding should make me capable.**

AI and agentic workflows may assist with research, command generation, configuration drafting, troubleshooting, log analysis, validation, documentation, and repetitive administration.

Important changes should still be understood and independently verified. An agent reporting success is not proof that a task succeeded.

## Learning Path

### Level 1 — Linux Foundations

**Status:** Completed

Topics include:

- Linux shell basics
- Zsh
- Oh My Zsh
- Powerlevel10k
- Git
- GitHub Codespaces
- Building Python from source
- pip
- OpenSSL
- Python virtual environments

### Level 2 — Linux Administration

Topics include users and groups, permissions, processes, services, systemd, logs, SSH, package management, storage, scheduled tasks, and backups.

### Level 3 — Linux Networking & Services

Topics include IP addressing, interfaces, routing, DNS, TCP/UDP, ports, packet capture, firewalls, web services, and network troubleshooting.

### Level 4 — Automation & Containers

Topics include Bash, Python automation, Git workflows, APIs, Docker, Docker Compose, and repeatable configuration.

### Level 5 — Infrastructure & Homelab

Topics include virtual machines, virtual networking, VLANs, DNS, DHCP, reverse proxies, VPNs, monitoring, logging, security hardening, Ansible, and infrastructure troubleshooting.

### Level 6 — Agentic Operations

Topics include agent-assisted analysis, troubleshooting, configuration drafting, log analysis, automation review, permissions, failure analysis, rollback, and independent verification.

See `ROADMAP.md` for the complete learning progression.

## Repository Documentation

- `README.md` — Project overview
- `PROGRESS.md` — Completed work and current status
- `ROADMAP.md` — Learning progression and completion criteria
- `LAB_TEMPLATE.md` — Standard format for practical labs
- `AGENTIC_WORKFLOW.md` — Standard for safe and understandable agent-assisted work
- `CONTRIBUTING.md` — Git, documentation, security, and quality standards

## Current Environments

### GitHub Codespaces

Primary Linux development and learning environment.

Useful for:

- Linux command-line work
- Git
- Python
- Development
- Documentation
- Automation
- Container-compatible labs

Some labs requiring a complete operating system, systemd, a desktop environment, a hypervisor, or advanced networking may require a VM or homelab instead.

### iSH on iOS

Lightweight mobile Linux terminal.

The repository can be cloned into iSH and synchronized through GitHub.

iSH is useful for:

- Git
- Markdown editing
- Lightweight shell practice
- Project documentation
- Reviewing project files
- Small Linux exercises

iSH uses Alpine Linux on iOS and should not be treated as equivalent to a full Ubuntu server.

## Git Workflow

Before starting work:

```bash
git pull
git status
```

After making changes:

```bash
git diff
git status
git add <filename>
git commit -m "Describe the change"
git push
```

Avoid blindly staging files when sensitive information may exist.

## Security Rules

Never commit:

- Passwords
- API tokens
- Authentication cookies
- Private SSH keys
- Secret keys
- Credentials
- Confidential company data
- Sensitive customer data
- Unreviewed infrastructure secrets

Sanitize sensitive information before documentation is committed.

## Standard Lab Workflow

For each lab:

1. Understand the objective.
2. Understand why the topic matters.
3. Identify prerequisites.
4. Record the environment.
5. Assess risk and possible impact.
6. Perform the task manually when practical.
7. Explain the commands and configuration.
8. Verify the result.
9. Record evidence.
10. Troubleshoot problems.
11. Document the resolution.
12. Document rollback.
13. Explain what happened under the hood.
14. Identify useful automation.
15. Review agent or automation actions.
16. Verify automated results manually.
17. Record lessons learned.
18. Commit sanitized documentation to GitHub.

## Long-Term Goal

The long-term goal is to become capable of:

- Understanding and administering Linux systems
- Understanding and troubleshooting networks
- Building and operating infrastructure
- Automating repetitive work safely
- Managing containers and configuration
- Using AI agents effectively
- Reviewing automated actions
- Understanding what happens under the hood
- Maintaining control of the systems being managed

This repository is a practical record of that progression.
