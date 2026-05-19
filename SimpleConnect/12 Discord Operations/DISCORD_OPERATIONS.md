
# Discord Operations

## Purpose

This file defines how Discord is used as the operational control plane for Simple Connect.

Discord is not for casual chatter. It is for structured visibility into Hermes, Codex, VPS, build progress, blockers, escalations, and phase completion.

The goal is to let Dee stay informed without being buried in noise.

## What Belongs Here

- Discord server structure
- channel purpose
- notification rules
- escalation channel rules
- completed work summaries
- system health alerts
- phase status updates
- blocked work notices
- daily or session summaries
- Hermes reporting behavior

## What Does Not Belong Here

- full build documentation
- raw code diffs
- random thoughts
- every Hermes action
- every Codex action
- noisy terminal logs
- private API keys
- client sensitive material

## Recommended Channels

- `vom-build`
- `codex-execution`
- `phase-tracking`
- `critical-escalations`
- `completed-work`
- `system-health`

## Hermes Usage

Hermes should use Discord to report meaningful operational updates only.

Hermes should not send Discord messages for every file read, every shell command, or every minor verification step.

## Notification Rules

Hermes should notify Dee for:

1. Completed phase
2. Blocker
3. Critical failure
4. Decision needed
5. Material risk
6. End of work session summary
7. System health problem

Hermes should not notify Dee for:

1. Routine code inspection
2. Successful low risk build check
3. Minor file edits
4. Normal command output
5. Repeated low value status updates

## Report Format

Discord updates should be concise:

1. Status
2. What changed
3. Verification
4. Risk
5. Next action

## Rule

Discord should reduce Dee’s need to check the terminal. It should not become another distraction.