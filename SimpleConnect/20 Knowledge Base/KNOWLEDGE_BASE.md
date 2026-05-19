
# Session Summaries

## Purpose

Session summaries provide high-level operational snapshots of meaningful work sessions.

The goal is to preserve:
- continuity
- progress visibility
- context recovery
- operational awareness

Session summaries are not detailed execution logs.

They exist so Dee can quickly understand:
- what changed
- what improved
- what broke
- what remains unfinished
- what matters next

---

## What Belongs Here

- completed milestones
- major phase progress
- infrastructure updates
- major risks discovered
- operational blockers
- meaningful verification outcomes
- next session priorities

---

## What Does Not Belong Here

- every code modification
- noisy shell output
- low-level implementation detail
- repetitive status updates

---

## Hermes Usage

Hermes may generate session summaries after meaningful execution periods.

Hermes should:
- summarize outcomes
- remain concise
- identify risks
- identify next priorities

Hermes should avoid:
- excessive verbosity
- filler
- repeated information
- low-value updates

---

## Recommended Summary Structure

1. Session objective
2. Major completed work
3. Risks or blockers
4. Verification status
5. Recommended next actions

---

## Rule

Session summaries should reduce the need for Dee to manually inspect:
- terminal logs
- git history
- raw execution details

The summary should communicate operational meaning, not noise.