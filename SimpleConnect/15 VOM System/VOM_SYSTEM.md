
# VOM System

## Purpose

This file defines the Virtual Office Manager system for Simple Connect.

The VOM is the core operational product being built inside the Simple Connect B2B automation platform.

The VOM exists to reduce or replace repetitive office work for contractors and service businesses by handling communication, booking, follow up, onboarding, operational visibility, and eventually invoice follow up workflows.

The VOM should function as an operational layer between businesses and their inbound or outbound customer interactions.

---

## Product Vision

The long-term VOM vision includes:

- inbound call handling
- missed call recovery
- SMS interaction
- booking coordination
- onboarding workflows
- customer follow up
- invoice follow up
- operational visibility
- office workflow reduction
- AI-assisted communication handling

The goal is not to create a generic CRM.

The goal is to create an operational automation system that reduces administrative workload while maintaining a believable customer experience.

---

## Current Demo Objective

The immediate goal is contractor demo readiness.

The current contractor demo should demonstrate:

1. customer interaction
2. VOM response
3. appointment booking
4. visible operational activity
5. onboarding visibility
6. invoice follow-up visibility

The demo should create belief without requiring every production workflow to be fully complete.

---

## Current System Components

### Vapi Interaction Layer

Purpose:
Voice interaction and receptionist-style call handling.

Current state:
- Vapi SDK connected
- browser interaction exists
- webhook exists
- booking capture partially exists
- deterministic booking still used for reliability

### Booking Pipeline

Purpose:
Convert interaction into appointment activity.

Current state:
- deterministic booking exists
- booking visibility exists
- booking capture from Vapi partially exists

### Dashboard Layer

Purpose:
Provide operational visibility into what VOM handled.

Current state:
- metric cards exist
- appointment visibility exists
- onboarding placeholder exists
- invoice placeholder exists

### Onboarding Layer

Purpose:
Prepare businesses for VOM operational usage.

Current state:
- onboarding flow exists
- client creation exists
- readiness flow incomplete

### Invoice Follow-Up Layer

Purpose:
Demonstrate future AR automation capability.

Current state:
- invoice schema exists
- invoice visibility exists
- automation incomplete

---

## Current Build Philosophy

The VOM should:
- feel operationally believable
- remain stable
- avoid overengineering
- preserve future capability visibility
- remain contractor-friendly
- focus on outcomes

The VOM should not:
- become a cluttered dashboard
- become a generic AI toy
- become a feature dump
- rely entirely on fragile live interactions

---

## Current Known Risks

- Vapi interaction instability
- weak booking visibility
- runtime failures
- partial booking workflow
- dashboard uncertainty
- demo complexity creep

---

## Hermes Usage

Hermes should preserve:
- VOM continuity
- future phase visibility
- demo reliability
- operational clarity

Hermes must not:
- redefine the VOM product direction
- remove future capabilities
- expand beyond active phase scope
- weaken demo stability

---

## Success Definition

The VOM is successful when a contractor can clearly understand:

- what VOM handled
- how office work was reduced
- how appointments were created
- how visibility was maintained
- how onboarding and follow-up fit into the workflow

without confusion or instability.