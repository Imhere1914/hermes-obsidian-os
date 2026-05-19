
# SOPs

## Purpose

This file stores repeatable operating procedures for Simple Connect.

SOPs exist so the same work is performed consistently every time without Dee needing to remember or re-explain the steps.

The goal is to reduce execution drift, prevent missed steps, and make Hermes, Codex, and future operators follow a consistent process.

## What Belongs Here

- VPS setup procedure
- Hermes restart procedure
- Codex authentication procedure
- repo clone and build procedure
- GitHub SSH setup
- tmux attach and detach procedure
- demo verification procedure
- rollback procedure
- build verification procedure
- Discord notification procedure
- Obsidian update procedure
- production safety checklist

## What Does Not Belong Here

- one time notes
- brainstorming
- strategic decisions
- active phase definitions
- temporary errors
- raw terminal output unless converted into a repeatable process

## Hermes Usage

Hermes may use SOPs when performing repeatable operational work.

Hermes should follow the SOP unless:
- the SOP is outdated
- the command fails
- the environment has changed
- following the SOP introduces risk

If the SOP appears outdated, Hermes should escalate or suggest an update.

## SOP Standard

Each SOP should include:

1. Purpose
2. When to use it
3. Preconditions
4. Step by step commands
5. Expected result
6. Failure handling
7. Verification step

## Rule

If a process will happen more than once, it deserves an SOP.