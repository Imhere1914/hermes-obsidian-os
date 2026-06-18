---
schemaVersion: 2
sanitizationVersion: 1
extractionRunId: "v3_from_v1brain_2026-06-17"
extractedAt: "2026-06-18T06:19:54.292594Z"
account: "Simple_Connect"
locationId: "0sDrn6fnaatHFrxKih6y"
sourcePaths:
  - "/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/live_threads/Simple_Connect/run_full_2026-06-12T19-12-17Z_v1brain"
  - "/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/full"
  - "/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/live_threads/Simple_Connect/run_full_2026-06-12T19-12-17Z_v1brain/raw_all_messages/messages.jsonl"
  - "/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/full/conversation_brain_high_signal_enriched_v3_from_v1brain.jsonl"
  - "/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/full/message_sequence_index_enriched_v3_from_v1brain.jsonl"
  - "/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/full/timing_intelligence_enriched_v3_from_v1brain.jsonl"
  - "/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/full/objection_recovery_enriched_v3_from_v1brain.jsonl"
  - "/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/full/humanistic_language_patterns_v3_from_v1brain.jsonl"
  - "/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/full/v3_from_v1brain_metrics.json"
corpusSize:
  conversations: 77000
  messages: 387647
retrievalTags:
  - "#curiosity"
  - "#questions"
  - "#inbound"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Curiosity Patterns"
fileIndex: "05"
---

# 05 — Curiosity Patterns

> Questions humans ask before engaging — buying signals and information gaps.

## Pattern summary

8 inbound messages contain questions.

Top patterns:
- Pricing questions ("how much", "what's the cost", "do you guys price over the phone")
- Process questions ("how does this usually work", "do you come out first")
- Timing questions ("when can you start", "how long does it take")
- Authority questions ("who would I be talking to", "is this you calling")

## Examples (sanitized, dash-free)

> **msg_id `O4oZ8tRHSc…`** at `2026-05-22T20:34:21`
> What company are you with?
> **msg_id `8j5kOdlftB…`** at `2026-05-22T20:28:30`
> What are you needing a quote for?
> **msg_id `hu1gJ9nJhO…`** at `2026-05-22T20:22:49`
> I am not sure what you are referring too?
> **msg_id `j1oCahmpXK…`** at `2026-05-22T14:17:02`
> Hi! Yes we would send a technician out to provide an accurate estimate, could you please clarify what specific services or equipment you are needing pricing for?
> **msg_id `0Ng7J9CN0s…`** at `2026-05-22T14:42:44`
> Are you a lead or marketing company?
> **msg_id `LkrjqYR7DT…`** at `2026-05-22T14:39:50`
> Need to look at the job first. What's your address?
> **msg_id `aMeKxMgIgL…`** at `2026-05-20T17:53:30`
> Is that address where you are needing service?
> **msg_id `vMxqvtkPjh…`** at `2026-05-20T17:49:05`
> Can you provide me with your name, address, phone number and email address to get you booked?

## Dash-free training version

Curiosity questions in this corpus are short, lowercase, end with `?`. No greeting before the question.

## What the agent should learn

- Pricing questions are buying signals disguised as information requests.
- Process questions mean the human is mentally walking through engagement.

## What the agent should avoid

- Don't deflect pricing questions to "let's hop on a call."
- Don't answer process questions with vague timelines.
- Don't make the human feel they're interrogating you.
