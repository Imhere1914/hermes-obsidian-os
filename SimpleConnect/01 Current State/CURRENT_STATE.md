
# Current State

Last Updated: 2026-05-18

## Purpose

This file is the authoritative snapshot of the current operational reality of Simple Connect.

Hermes should read this file before beginning any work session.

Hermes should use this file to:
- determine active priorities
- understand current phase context
- understand known risks
- avoid repeating solved work
- maintain continuity between sessions

Hermes should not overwrite this file casually. Updates should preserve historical continuity and reflect only meaningful operational changes.

What belongs here:
- active phase
- current goals
- current infrastructure
- current weaknesses
- current blockers
- current priorities
- current architecture state
- known risks
- repo and runtime state

What does not belong here:
- brainstorming
- long-term speculation
- temporary notes
- unverified assumptions
- detailed SOPs
- unrelated future ideas

---

## Sprint Context

Current Sprint: 60-day sales sprint
Demo Target: 2026-05-23
Hermes operates 24/7 to hit this deadline
Priority: Phase 1 completion before all other work

---

## Primary Objective

Simple Connect is building a B2B automation system centered around the Virtual Office Manager, or VOM.

The VOM is being built to replace front office busy work for service based businesses and contractors. The system should eventually handle calls, texts, follow ups, booking, onboarding, invoice follow up, and operational visibility.

The immediate objective is to move the VOM system into a contractor demo ready state by 2026-05-23.

The current target demo is for a high value general contractor prospect.

---

## Current Strategic Direction

Simple Connect is moving from build mode into proof and demo mode.

The priority is not to build every future feature fully right now. The priority is to create a believable, stable, controlled demo that proves the VOM can replace manual office work.

The demo must show a clear story:
1. A contractor prospect or customer reaches out
2. VOM handles the interaction
3. VOM books the appointment
4. The dashboard shows the activity
5. Onboarding is visible as the next system step
6. Invoice follow up is visible as the future automation proof

The current build philosophy is demo first, but product consistent.

This means:
- Build enough to prove the system
- Preserve future phase visibility
- Do not remove future features from the product story
- Do not overbuild before the demo validates the direction

If a prospect asks whether the booking was real, the answer is: this is a controlled demo flow. Do not misrepresent it.

---

## Current Active Phase

Phase 1: Demo Flow Hardening
Status: Active
Deadline: 2026-05-23

Phase 1 focuses on hardening the first visible VOM journey:
Call interaction to booking confirmation to visible system activity.

Phase 1 must produce:
1. A stable demo trigger
2. A visible Vapi interaction layer
3. A deterministic booking outcome
4. A clear appointment confirmation
5. A visible timeline or dashboard proof
6. Preserved placeholders for onboarding and invoice follow up
7. A demo flow that does not fail in front of a prospect

---

## Current Infrastructure

- VPS is active
- VPS user dee has sudo access
- Hermes is installed on VPS
- Hermes runs inside tmux
- Codex CLI is installed on VPS
- Codex is authenticated with OpenAI Platform API key
- GitHub SSH is working from VPS
- Repo is cloned on VPS at: /home/dee/Developer/business-flow-automator
- npm install completed
- npm run build passes on VPS

Repository:
- Remote: git@github.com:Imhere1914/business-flow-automator.git
- Local Mac path: /Users/dsmil/Developer/business-flow-automator
- VPS path: /home/dee/Developer/business-flow-automator

---

## Current VOM Build State

### Dashboard
- VOM routes and navigation exist
- Dashboard page exists
- Metric cards exist for calls, bookings, invoices, viewed invoices, and payments
- VOM pages exist: Dashboard, Clients, Agents, Conversations, Invoices, Onboard
- Known issue: dashboard may reference counts.data without clearly creating counts via useVomCounts. Build passes but runtime behavior should be inspected.

### Demo Journey Harness
- Demo harness exists and can seed a contractor style demo client
- Can seed a customer contact, voice conversation record, call handled activity, confirmed appointment, and booking activity proof
- Booking outcome is deterministic and seeded by design for demo reliability

### Vapi Call Interaction
- Browser Vapi SDK is wired through @vapi-ai/web
- Public demo key and assistant ID referenced through demo config
- Vapi server side functions exist: vapi-admin, vapi-webhook, vapi-demo-call, vapi-create-call
- Vapi webhook can record end of call data when client context is resolvable
- Current limitation: live Vapi interaction is not yet fully tied to appointment creation
- Strategic decision: do not depend on live Vapi to complete the demo booking. Live Vapi demonstrates interaction. Deterministic booking guarantees the demo outcome.

### Booking Flow
- Demo harness can create a confirmed appointment directly
- Vapi webhook can log appointment booking intent as an agent action
- Current limitation: Vapi booking capture does not yet create confirmed appointment rows automatically
- No review and confirm booking pipeline exists yet

### Onboarding
- /vom/onboard exists
- Multi step client creation flow exists
- Optional intake agent assignment exists
- Onboarding can log vom_client_onboarded
- Current limitation: not fully production ready
- Demo role: must remain visible as the next VOM system step

### Invoice Follow Up
- Invoice schema exists
- Invoice list view exists
- Dashboard metrics exist for invoices sent, viewed, paid, and follow up fields
- Current limitation: no real invoice follow up workflow exists yet
- Demo role: must remain visible as the future automation proof

---

## Current Known Weaknesses

1. Live Vapi is not yet fully connected to the booking pipeline
   Risk: prospect may question whether the AI actually booked the appointment
   Mitigation: use live Vapi as interaction layer and deterministic booking as guaranteed outcome

2. Booking proof needs to be visually obvious
   Risk: contractor may miss the outcome if it only appears in a toast or generic activity row
   Needed: clear booked appointment confirmation card or prominent dashboard state

3. Demo flow must remain controlled and reliable
   Risk: live voice interaction can introduce microphone, latency, or permission issues
   Needed: demo should fail gracefully and never leave the system in a confusing state

4. Node version mismatch on VPS
   Current VPS Node: v18.19.1
   Some packages require Node 20 or higher
   Status: build passes but VPS should be upgraded before extended autonomous build sessions

5. Package vulnerabilities exist
   Current npm audit: 19 vulnerabilities, 3 low, 7 moderate, 9 high
   Decision: do not run npm audit fix --force until impact is reviewed

---

## Immediate Next Build Tasks

1. Upgrade VPS Node to version 20
2. Verify build after Node upgrade: node -v, npm -v, npm run build
3. Run Codex read only repo check to identify next smallest Phase 1 hardening task
4. Review existing uncommitted changes made by Hermes
5. Decide whether to keep or revert direct Hermes changes made when Codex was not authenticated
6. Improve booking visibility so outcome is unmistakable
7. Stabilize Vapi interaction layer
8. Preserve Phase 2 and Phase 3 placeholders
9. Run full demo flow end to end and fix any breakpoints

---

## Agent Roles

Dee: strategic decisions and final authority
Hermes: execution coordinator and orchestrator
Codex: code execution layer
VPS: persistent runtime
Obsidian: operational memory
Discord: notification and operations control plane