# Tim Ubuntu Project Progress

## Current Status

**Original mentor assignment:** Completed  
**Current phase:** Expanding into structured Linux, networking, automation, infrastructure, and agentic-operations labs.

## Level 1 — Linux Foundations

**Status:** Completed

### Shell and Terminal

Completed:

- Checked the active shell
- Installed and configured Zsh
- Changed the default shell to Zsh
- Verified Zsh as the active shell
- Verified Oh My Zsh
- Installed and configured Powerlevel10k
- Completed the Powerlevel10k setup wizard
- Installed `zsh-autosuggestions`
- Installed `zsh-syntax-highlighting`
- Updated `.zshrc`
- Verified the shell loaded successfully

Configured plugins:

```text
git
zsh-autosuggestions
zsh-syntax-highlighting
```

### Python 3.10.1 From Source

Completed:

- Created source and installation directories
- Downloaded Python 3.10.1 source
- Extracted the source archive
- Installed build dependencies
- Configured Python with optimizations
- Configured OpenSSL support
- Enabled `ensurepip`
- Compiled Python from source
- Ran the Python test suite
- Installed Python with `make altinstall`
- Verified the custom installation

Custom installation:

```text
~/training_sandbox/python/environments/py310_1
```

Verified version:

```text
Python 3.10.1
```

### OpenSSL

Verified through Python:

```bash
python3.10 -c "import ssl; print(ssl.OPENSSL_VERSION)"
```

Observed result:

```text
OpenSSL 3.0.13 30 Jan 2024
```

### pip

Verified version:

```text
pip 21.2.4
```

### Core Python Module Verification

Successfully imported:

- `ssl`
- `sqlite3`
- `bz2`
- `lzma`
- `ctypes`
- `multiprocessing`

### Python Test Suite

Executed:

```bash
make test
```

Observed summary:

```text
405 tests OK.
7 test groups failed.
15 tests skipped.
```

Failed test groups:

```text
test_c_locale_coercion
test_distutils
test_email
test_import
test_ssl
test_subprocess
test_urllib2
```

The build was performed on a modern Ubuntu/GitHub Codespaces environment while Python 3.10.1 is considerably older. The failures were documented rather than hidden.

Manual verification confirmed the required Python functionality was working.

### Python Virtual Environment

Created:

```text
~/training_sandbox/python/virtual_environments/venv310_1
```

Verified:

- Python 3.10.1
- Python executable inside the virtual environment
- pip inside the virtual environment

## GitHub

Completed:

- Added progress documentation
- Added a structured roadmap
- Committed documentation
- Pushed changes to GitHub
- Verified a clean working tree
- Used GitHub as the synchronization point between environments

Repository:

```text
https://github.com/sharetool09-bot/tim-ubuntu-project
```

## iSH on iOS

Completed:

- Installed Git in iSH
- Cloned the repository
- Verified project files
- Verified the `main` branch
- Verified synchronization with `origin/main`

Current iSH path:

```text
~/tim-ubuntu-project
```

iSH is available for lightweight Git, documentation, Markdown editing, and small shell exercises.

## Environment Differences

The original assignment targeted a traditional Ubuntu environment. The project was completed in GitHub Codespaces, which is a development container rather than a complete Ubuntu desktop.

Desktop-specific tasks such as GNOME Tweaks, desktop font configuration, and graphical Chromium setup are therefore not directly equivalent.

Those differences are documented rather than treated as identical environments.

## Key Lessons From Level 1

I learned how to:

- Work from the Linux command line
- Configure a shell
- Understand shell configuration files
- Install Linux packages
- Use Git and GitHub
- Use GitHub Codespaces
- Compile Python from source
- Understand build dependencies
- Configure and test a source build
- Interpret test failures
- Install a separate Python version
- Verify OpenSSL and pip
- Create Python virtual environments
- Verify software manually
- Document technical work
- Synchronize work between Codespaces, GitHub, and iSH

## Mentor Feedback Incorporated

A key lesson from mentor feedback is that completing commands is not enough.

The project should demonstrate:

- What each step does
- Why each step is required
- Where the skill is useful
- What happens under the hood
- What automation changes
- How agentic work is verified

These principles are now built into the project documentation standards.

## Next Phase

### Level 2 — Linux Administration

Planned areas:

- Users and groups
- Permissions
- Processes
- Services
- Logs
- SSH
- Package management
- Storage
- Scheduled tasks
- Backups

Each new lab should follow `LAB_TEMPLATE.md`.
