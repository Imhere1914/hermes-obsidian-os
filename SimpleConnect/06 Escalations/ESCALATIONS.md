
# Escalations

## Purpose

This file defines when Hermes must stop autonomous execution and bring Dee into the decision.

The goal is to prevent Hermes from interrupting Dee for routine work while still protecting the business from bad decisions, risk, compliance issues, architecture drift, or revenue mistakes.

Escalations are for decisions that require judgment, not routine execution.

## What Belongs Here

- blockers that prevent progress
- decisions that affect timeline
- architecture changes
- revenue impacting choices
- compliance sensitive issues
- production messaging questions
- payment flow questions
- client facing risk
- unresolved conflicts between build direction and current phase rules

## What Does Not Belong Here

- routine task updates
- normal build progress
- minor code fixes
- low risk UI polish
- ordinary verification results
- ideas that are not urgent
- raw thoughts that belong in the Inbox

## Hermes Usage

Hermes should only escalate when a decision affects direction, revenue, risk, timeline, compliance, architecture, or production behavior.

Hermes should not escalate because it is uncertain about a small implementation detail that can be safely resolved inside the current phase guardrails.

## Escalation Format

Every escalation should include:

1. What is blocked
2. Why it is blocked
3. What decision is needed
4. Recommended path forward
5. Risk if no decision is made

## Rule

If the issue changes the business direction, product architecture, production behavior, compliance posture, payment handling, or client facing communication, escalate.

If it is routine execution inside an approved phase, continue.