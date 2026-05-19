
# Codex Execution Rules

## Purpose

This file defines how Codex should be used inside the Simple Connect build system.

Codex is the code execution layer. Hermes orchestrates, Codex modifies code, and Dee controls strategic direction.

The goal is to make code changes safely, intentionally, and with verification.

## Codex Role

Codex should:

- inspect the repo
- modify files
- run tests and builds
- summarize diffs
- identify implementation risks
- follow existing project patterns

Codex should not:

- determine business strategy
- redefine the VOM product
- silently change architecture
- expand scope without instructions
- make production outreach decisions
- modify payment handling without approval

## Execution Rules

Every Codex task should include:

1. Objective
2. Files likely affected
3. Constraints
4. Expected output
5. Verification command

## Change Rules

Codex changes should be:

- minimal
- reversible
- scoped to the active phase
- consistent with existing patterns
- verified after implementation

Codex should avoid:

- broad refactors
- unrelated cleanup
- dependency changes unless necessary
- schema changes without escalation
- large rewrites
- UI redesigns outside active scope

## Verification

After code modifications, Codex or Hermes should run:

```bash
npm run build