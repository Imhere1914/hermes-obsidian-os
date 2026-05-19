

# Session Summaries

## Purpose

This folder stores high-level operational summaries of meaningful execution sessions inside the Simple Connect system.

Session Summaries are designed to preserve operational continuity between work periods without requiring Dee to read raw terminal history, git diffs, or detailed execution logs.

The purpose is fast operational understanding.

A Session Summary should quickly communicate:
- what happened
- what changed
- what was completed
- what failed
- what remains blocked
- what should happen next

This folder exists to reduce cognitive load and prevent execution drift over time.

---

## What Belongs Here

Session Summaries should contain:

- meaningful build progress
- completed milestones
- important infrastructure updates
- operational blockers
- major verification results
- current system state changes
- meaningful Hermes execution outcomes
- important Codex execution outcomes
- recommended next actions
- important governance or operational observations

---

## What Does Not Belong Here

This folder should not contain:

- raw terminal output
- every shell command
- detailed implementation logs
- repeated information
- low-value status updates
- brainstorming
- random ideas
- duplicate execution logs

Detailed technical implementation belongs in:
- Execution Logs
- CURRENT_STATE
- BUILD_PHASES
- Infrastructure
- Governance

---

## Hermes Usage

Hermes may create or append Session Summaries after meaningful execution periods.

Hermes should:
- summarize clearly
- remain concise
- focus on outcomes
- highlight risks and blockers
- identify next priorities

Hermes should not:
- create excessive summaries
- summarize trivial work
- generate duplicate summaries
- log every small action

---

## Recommended Session Summary Structure

Each Session Summary should include:

1. Timestamp
2. Objective of the session
3. Major completed work
4. Verification performed
5. Risks discovered
6. Current blockers
7. Recommended next actions

---

## Operational Philosophy

Execution Logs preserve implementation detail.

Session Summaries preserve operational understanding.

The goal is to allow Dee to quickly understand the state of the system without reading low-level execution history.

---

## Rule

A Session Summary should answer:

"What materially changed during this work session, and what matters next?"