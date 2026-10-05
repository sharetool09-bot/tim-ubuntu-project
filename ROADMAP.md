# Tim Ubuntu Project Roadmap

## Purpose

This roadmap defines the learning progression for the Tim Ubuntu Project.

The project progresses from Linux fundamentals into administration, networking, automation, infrastructure, and agentic operations.

The goal is to combine theoretical understanding with practical, reproducible labs.

## Level 1 — Linux Foundations

**Status:** Completed

### Core Areas

- Linux shell fundamentals
- Zsh
- Oh My Zsh
- Powerlevel10k
- Package installation
- Git
- GitHub
- GitHub Codespaces
- Python source compilation
- OpenSSL
- pip
- Python virtual environments
- Verification
- Basic troubleshooting

### Completion Criteria

- Shell environment configured
- Python successfully built from source
- pip verified
- OpenSSL verified
- Core Python modules verified
- Python virtual environment verified
- Project progress documented
- Documentation committed to GitHub

**Result:** Complete

## Level 2 — Linux Administration

**Status:** Planned

### Core Areas

- Users and groups
- Permissions and ownership
- Processes and signals
- Services and systemd
- Logs
- SSH
- Package management
- Storage and filesystems
- Environment variables
- Scheduled tasks
- Backups

### Core Labs

- [ ] Create and manage users
- [ ] Create and manage groups
- [ ] Understand UID and GID
- [ ] Practice `chmod`, `chown`, and `chgrp`
- [ ] Understand numeric and symbolic permissions
- [ ] Inspect running processes with `ps` and `top`
- [ ] Use `kill` and understand signals
- [ ] Manage services
- [ ] Inspect service definitions
- [ ] Use `journalctl`
- [ ] Search and follow logs
- [ ] Configure SSH
- [ ] Generate SSH keys
- [ ] Configure key authentication
- [ ] Understand `authorized_keys` and `known_hosts`
- [ ] Manage Linux packages
- [ ] Inspect disks with `lsblk`
- [ ] Inspect space with `df` and `du`
- [ ] Understand mount points
- [ ] Create cron jobs
- [ ] Create and verify backups
- [ ] Use `rsync`
- [ ] Restore files from backup

### Completion Criteria

- Core administration tasks can be performed manually
- Important commands can be explained
- Changes can be independently verified
- Common failures can be troubleshot
- Backup and restore are demonstrated
- SSH is configured and verified
- Core labs are documented

## Level 3 — Linux Networking & Services

**Status:** Planned

### Core Areas

- IPv4 and IPv6 basics
- Network interfaces
- MAC addresses
- Subnetting
- Default gateways
- Routing
- DNS
- TCP and UDP
- Ports
- Packet capture
- Firewalls
- Web servers
- Network troubleshooting

### Core Labs

- [ ] Inspect interfaces and addresses
- [ ] Identify MAC addresses
- [ ] View routes and default gateway
- [ ] Add and remove a temporary route
- [ ] Test connectivity with `ping`
- [ ] Trace paths with `traceroute` or `tracepath`
- [ ] Inspect sockets with `ss`
- [ ] Identify listening ports
- [ ] Identify established connections
- [ ] Query DNS with `dig`
- [ ] Query DNS with `nslookup`
- [ ] Query common DNS record types
- [ ] Capture traffic with `tcpdump`
- [ ] Filter packet captures
- [ ] Configure basic UFW rules
- [ ] Allow and deny ports
- [ ] Install Nginx
- [ ] Host a basic web page
- [ ] Inspect Nginx logs
- [ ] Troubleshoot a broken web service

### Completion Criteria

- Basic Linux networking can be explained
- Routing can be inspected
- DNS can be tested and troubleshot
- Listening ports can be identified
- Packet captures can be performed
- Basic firewall rules can be configured
- A network service can be installed and verified
- A broken network service can be troubleshot

## Level 4 — Automation & Containers

**Status:** Planned

### Core Areas

- Bash
- Python automation
- Error handling
- Git branches
- APIs and JSON
- Docker
- Dockerfiles
- Docker networks
- Docker volumes
- Docker Compose
- Repeatability

### Core Labs

- [ ] Create a Bash script
- [ ] Create a system-information script
- [ ] Create a backup script
- [ ] Add error handling
- [ ] Create a Python network-check script
- [ ] Check multiple hosts
- [ ] Test TCP ports
- [ ] Resolve DNS with Python
- [ ] Parse JSON
- [ ] Call an API
- [ ] Create and merge a Git branch
- [ ] Resolve a simple Git conflict
- [ ] Install Docker
- [ ] Run and inspect a container
- [ ] View container logs
- [ ] Create a volume
- [ ] Create a Docker network
- [ ] Build an image
- [ ] Write a Dockerfile
- [ ] Create a Docker Compose environment
- [ ] Run multiple services
- [ ] Automate part of the Linux environment

### Completion Criteria

- Repetitive tasks can be scripted
- Scripts include basic error handling
- Git branches can be used safely
- APIs can be queried
- Docker fundamentals are understood
- A multi-container environment can be deployed
- Automation can be reviewed and verified manually

## Level 5 — Infrastructure & Homelab

**Status:** Planned

### Core Areas

- Linux servers
- Virtual machines
- Virtual networking
- VLANs
- DNS services
- DHCP
- Reverse proxies
- VPNs
- Monitoring
- Central logging
- Security hardening
- Troubleshooting
- Ansible
- Configuration management

### Core Labs

- [ ] Build a Linux server VM
- [ ] Configure static networking
- [ ] Create and connect multiple VMs
- [ ] Document a virtual network
- [ ] Build a VLAN lab
- [ ] Understand access and trunk ports
- [ ] Understand inter-VLAN routing
- [ ] Configure local DNS
- [ ] Create DNS records
- [ ] Build a DHCP lab
- [ ] Configure a reverse proxy
- [ ] Build a VPN lab
- [ ] Verify VPN routes and DNS
- [ ] Implement monitoring
- [ ] Monitor CPU, memory, disk, and network use
- [ ] Configure centralized logging
- [ ] Harden a Linux server
- [ ] Review open ports and permissions
- [ ] Disable unnecessary services
- [ ] Troubleshoot DNS, routing, permissions, and services
- [ ] Install Ansible
- [ ] Create an inventory
- [ ] Run ad-hoc commands
- [ ] Create a playbook
- [ ] Configure multiple machines

### Completion Criteria

- Multiple systems can be administered together
- Virtual networking can be documented
- Core infrastructure services can be deployed
- Monitoring and logging support troubleshooting
- Security hardening can be performed
- Configuration management can be used
- Infrastructure can be documented clearly

## Level 6 — Agentic Operations

**Status:** Planned

### Core Areas

- Agent-assisted analysis
- Agent-assisted troubleshooting
- Configuration drafting
- Log analysis
- Automation
- Permission awareness
- Verification
- Rollback
- Failure analysis
- Human approval

### Core Labs

- [ ] Ask an agent to inspect a Linux system
- [ ] Compare findings with manual commands
- [ ] Ask an agent to analyze logs
- [ ] Verify findings manually
- [ ] Ask an agent to draft configuration
- [ ] Review configuration before applying it
- [ ] Ask an agent to create a Bash script
- [ ] Explain every important command
- [ ] Ask an agent to create Python automation
- [ ] Review dependencies and permissions
- [ ] Identify possible failure modes
- [ ] Create rollback steps
- [ ] Ask an agent to troubleshoot a service
- [ ] Compare agent troubleshooting with manual troubleshooting
- [ ] Verify important agent actions
- [ ] Document an agent-assisted workflow

### Completion Criteria

- Agent actions can be explained
- Agent permissions are understood
- Proposed changes can be reviewed before execution
- Failure modes can be identified
- Rollback procedures can be created
- Automated results can be independently verified
- Agentic workflows improve speed without hiding technical understanding

## Progression

```text
Linux Foundations
        ↓
Linux Administration
        ↓
Networking & Services
        ↓
Automation & Containers
        ↓
Infrastructure & Homelab
        ↓
Agentic Operations
```

## Lab Standards

Every practical lab should use `LAB_TEMPLATE.md`.

Important labs should include:

- Objective
- Why the task matters
- Prerequisites
- Expected outcome
- Environment
- Risk and impact
- Manual procedure
- Commands and explanations
- Configuration changes
- Verification
- Evidence
- Troubleshooting
- Resolution
- Rollback
- Security considerations
- Agentic workflow
- Manual verification
- Lessons learned
- Real-world use case
- Completion criteria

## Guiding Principle

Do not confuse automation with understanding.

The project should demonstrate the ability to:

- Perform important tasks manually
- Explain what is happening
- Troubleshoot failures
- Automate repetitive work
- Review automated actions
- Verify results independently

**Automation should make the work faster. Understanding should make the work reliable.**
