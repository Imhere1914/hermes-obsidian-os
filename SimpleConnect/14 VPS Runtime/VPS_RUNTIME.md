
---

## `14 VPS Runtime/VPS_RUNTIME.md`

```markdown
# VPS Runtime

## Purpose

This file documents the persistent execution environment for Simple Connect.

The VPS is the always-on worker node where Hermes and Codex run so Dee does not have to keep the Mac open or manually babysit execution.

The VPS exists to support autonomous build progress, long-running sessions, and remote orchestration.

## Current VPS Role

The VPS runs:

- Hermes
- Codex CLI
- Git repo
- tmux persistent sessions
- build verification commands
- future Discord gateway
- future Obsidian sync or memory integration

## Current Paths

Repo path:

```bash
/home/dee/Developer/business-flow-automator