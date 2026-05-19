
# Execution Logs

## Purpose

This folder stores operational execution history for Simple Connect.

Execution logs exist to preserve visibility into:
- what Hermes executed
- what Codex modified
- what was verified
- what failed
- what changed
- what remains unresolved

The purpose is operational continuity, not journaling.

Execution logs should help Dee quickly understand:
- what happened
- what changed
- what risks exist
- what requires review

---

## What Belongs Here

- Hermes execution summaries
- Codex execution summaries
- build verification results
- deployment summaries
- rollback summaries
- failed execution summaries
- important runtime events
- infrastructure changes
- phase completion logs

---

## What Does Not Belong Here

- raw brainstorming
- strategic philosophy
- temporary thoughts
- duplicate documentation
- full code dumps
- noisy terminal spam

---

## Hermes Usage

Hermes may write execution summaries here.

Hermes should:
- summarize meaningfully
- remain concise
- focus on outcomes
- avoid excessive detail

Hermes should not:
- log every shell command
- create noise
- repeat unchanged information
- overwrite prior execution history

---

## Recommended Log Structure

Each execution log should include:

1. Timestamp
2. Objective
3. Files affected
4. Verification performed
5. Risks identified
6. Remaining blockers
7. Recommended next step

---

## Operational Rule

Execution logs should help reconstruct:
- what happened
- why it happened
- whether it succeeded
- what should happen next

without requiring Dee to reread terminal history.