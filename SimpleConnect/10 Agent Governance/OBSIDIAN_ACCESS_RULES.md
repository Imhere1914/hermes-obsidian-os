# Obsidian Access Rules

## Purpose

This file defines how Hermes may interact with the Simple Connect Obsidian vault.

The goal is controlled operational memory, not unrestricted autonomous documentation.

Hermes should preserve:
- operational continuity
- strategic clarity
- execution visibility
- governance stability

The vault exists to support long-term operational intelligence for Simple Connect.

---

## Approved Read Access

Hermes may read:

- CURRENT_STATE
- BUILD_PHASES
- DECISIONS
- MASTER_OBJECTIVES
- ACTIVE_TASKS
- HERMES_GOVERNANCE
- CODEX_EXECUTION_RULES
- VPS_RUNTIME
- VOM_SYSTEM
- DISCORD_OPERATIONS
- INFRASTRUCTURE
- SESSION_SUMMARIES
- EXECUTION_LOGS
- KNOWLEDGE_BASE

These files act as operational memory and source-of-truth references.

---

## Approved Write Access

Hermes may write only to:

- 00 Inbox
- 18 Execution Logs
- 19 Session Summaries

Hermes may append operationally meaningful updates to:

- CURRENT_STATE
- ACTIVE_TASKS

only when:
- meaningful operational progress occurs
- infrastructure changes occur
- blockers change
- phase completion occurs
- operational continuity would otherwise be lost

---

## Restricted Files

Hermes may not autonomously modify:

- BUILD_PHASES
- DECISIONS
- ARCHITECTURE
- HERMES_GOVERNANCE
- MASTER_OBJECTIVES
- VAULT_BOUNDARIES
- BUSINESS_BOUNDARIES
- VPS_RUNTIME

without escalation approval from Dee.

---

## Logging Rules

Hermes should:
- summarize concisely
- avoid noisy updates
- avoid duplicate summaries
- preserve clarity
- focus on outcomes

Hermes should not:
- log every shell command
- log every Codex action
- generate low-value noise
- overwrite historical operational context

---

## Operational Philosophy

Obsidian is the operational memory layer for Simple Connect.

The vault should:
- evolve with the business
- preserve continuity
- reduce repeated reasoning
- support autonomous execution safely

The vault should not become:
- cluttered
- noisy
- over-automated
- strategically unstable

---

## Rule

Hermes should treat Obsidian as governed operational memory, not as a dumping ground for raw activity.
