
# Build Phases

Last Updated: 2026-05-18

## Sprint Context
Current Sprint: 60-day sales sprint
Demo Target: 2026-05-23
Hermes operates 24/7 to hit this deadline
Priority: Phase 1 completion before all other work

## Purpose

This document defines the full build roadmap and guardrails for Simple Connect.

Hermes must use this file to understand:
- current phase
- allowed work
- prohibited work
- completion criteria
- escalation triggers
- next phase sequencing

Hermes should not skip phases, merge phases, or redefine project direction without Dee approval.

---

# Phase 0: Infrastructure Foundation

Status: Mostly Complete

Objective:
Create the persistent execution environment.

Includes:
- VPS setup
- Hermes install
- Codex install
- GitHub SSH access
- repo clone
- tmux persistent runtime
- build verification
- OpenRouter for Hermes
- OpenAI Platform key for Codex

Allowed:
- fix runtime issues
- verify environment
- improve stability

Not allowed:
- change product architecture
- start production sends
- modify payment flow

Completion condition:
Hermes and Codex run successfully on VPS and repo builds.

Escalate if:
- authentication fails
- VPS cannot run build
- repo access breaks

---

# Phase 1: VOM Demo Flow Hardening

Status: Active

Objective:
Create a stable contractor demo journey.

Includes:
- demo trigger
- Vapi interaction layer
- deterministic booking outcome
- visible appointment confirmation
- timeline proof
- dashboard proof
- onboarding placeholder
- invoice placeholder

Allowed:
- improve demo reliability
- improve booking visibility
- improve failure handling
- preserve full journey visibility

Not allowed:
- remove onboarding visibility
- remove invoice follow up visibility
- make live Vapi the only path to booking
- create production messaging automation
- redesign dashboard architecture

Completion condition:
A contractor can watch the demo from interaction to booked appointment without confusion or visible instability. Must be achieved by 2026-05-23.

Escalate if:
- demo direction changes
- live Vapi conflicts with deterministic booking
- new architecture is needed
- demo requires production credentials

---

# Phase 2: Dashboard and Operational Visibility

Status: Pending

Objective:
Make VOM visually convincing as an office replacement system.

Includes:
- activity timeline
- booking visibility
- conversation visibility
- client status
- onboarding status
- readiness indicators
- operational metrics

Allowed:
- improve UI clarity
- show system outcomes
- connect existing data to dashboard
- add lightweight cards and status views

Not allowed:
- build analytics platform too early
- add unnecessary charts
- redesign the whole app shell
- expand beyond VOM visibility

Completion condition:
A contractor can understand what VOM handled, what is pending, and what outcomes were created.

Escalate if:
- new data model is required
- dashboard architecture changes
- timeline changes affect later phases

---

# Phase 3: Onboarding MVP

Status: Pending

Objective:
Make client onboarding real enough to support demo and early client setup.

Includes:
- client profile
- contact details
- service area
- hours
- intake agent assignment
- Vapi number assignment placeholder or workflow
- readiness status

Allowed:
- add missing onboarding fields
- improve onboarding flow
- create readiness checklist

Not allowed:
- overbuild full CRM
- add multi-tenant complexity beyond current system
- automate external provisioning without approval

Completion condition:
A new contractor client can be onboarded into VOM with enough data for calls, booking, and follow up logic.

Escalate if:
- Vapi number provisioning requires billing or external approval
- client data model changes materially
- onboarding affects production routing

---

# Phase 4: Booking Pipeline

Status: Pending

Objective:
Turn booking intent into a real review and confirmed appointment flow.

Includes:
- captured booking intent
- review state
- confirm appointment
- appointment row creation
- dashboard update
- customer confirmation draft
- human approval where needed

Allowed:
- convert booking intent into structured workflow
- add review queue
- improve appointment visibility

Not allowed:
- auto-confirm real customer appointments without approval
- send customer messages without approval
- bypass compliance or human review

Completion condition:
Vapi or SMS captured booking intent can become a visible confirmed appointment through a safe pipeline.

Escalate if:
- production sends are involved
- calendar integration changes
- customer-facing confirmations are sent

---

# Phase 5: Invoice and AR Automation MVP

Status: Pending

Objective:
Show and eventually execute invoice follow up automation.

Includes:
- invoice creation or import
- sent/viewed/paid states
- follow up due state
- reminder draft
- approval-gated follow up
- payment link visibility

Allowed:
- build invoice visibility
- build follow up queue
- draft follow up actions

Not allowed:
- store card data
- change payment flow
- send payment reminders without approval
- bypass DejaVoo hosted checkout

Completion condition:
VOM can show invoice status and prepare follow up action safely.

Escalate if:
- payment handling changes
- DejaVoo integration is required
- real payment reminders are sent

---

# Phase 6: Production Safety and Compliance

Status: Future

Objective:
Make the system safe for real business workflows.

Includes:
- approval gates
- audit logs
- rollback behavior
- error handling
- STOP handling
- TCPA boundaries
- environment checks
- permission checks

Allowed:
- add safety checks
- strengthen audit trail
- prevent unsafe sends
- improve rollback

Not allowed:
- weaken approval gates
- loosen compliance controls
- allow cold SMS without approval and 10DLC readiness

Completion condition:
System can run real workflows without creating compliance or trust risk.

Escalate if:
- compliance interpretation is needed
- production outreach behavior changes
- STOP or consent logic changes

---

# Phase 7: Autonomous Hermes Operations

Status: Future

Objective:
Allow Hermes to run build execution with minimal Dee involvement.

Includes:
- Discord notifications
- Obsidian memory logging
- execution summaries
- phase tracking
- blocker escalation
- Codex task handoff
- low-noise reporting

Allowed:
- summarize progress
- update docs
- continue approved work
- identify blockers

Not allowed:
- change strategy
- approve its own risky decisions
- silently alter project direction
- spam notifications

Completion condition:
Hermes can work for extended periods and only interrupt Dee for meaningful decisions.

Escalate if:
- unclear direction
- timeline impact
- architecture impact
- revenue risk
- compliance risk

---

# Phase 8: Multi-Project Expansion

Status: Future

Objective:
Extend the operating system beyond Simple Connect VOM.

Includes:
- HFM separation
- separate memory lanes
- separate Discord channels
- separate build contexts
- separate guardrails

Allowed:
- create separated project structures
- document workflows
- prepare isolated memory lanes

Not allowed:
- mix HFM and Simple Connect data
- let agents cross-contaminate strategy
- share client-sensitive context between businesses

Completion condition:
Hermes can support multiple projects without mixing context or execution.

Escalate if:
- business boundaries blur
- medical or health communication is involved
- HFM compliance risk appears

---

# Global Hermes Rules

Hermes must:
- work within the active phase
- preserve future phases
- use Codex for code changes
- verify after changes
- keep work reversible
- update state documents when meaningful progress occurs
- escalate only when needed
- each day begin with the single highest leverage task remaining in the active phase
- when a phase completion condition is met notify Dee before advancing to the next phase
- end of day summary only if phase completed, blocker exists, or decision is needed
- if a build task fails twice stop and escalate
- do not loop on broken tasks
- document what failed before escalating

Hermes must not:
- redefine the product
- remove future capabilities
- change architecture silently
- send production outreach
- modify payment handling
- make compliance decisions
- create busy work

---

# Active Phase

Current Active Phase:
Phase 1: VOM Demo Flow Hardening

Next Phase:
Phase 2: Dashboard and Operational Visibility