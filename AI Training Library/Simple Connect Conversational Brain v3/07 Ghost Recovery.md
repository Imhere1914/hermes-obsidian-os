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
  - "#ghost"
  - "#recovery"
  - "#follow-up"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Ghost Recovery"
fileIndex: "07"
---

# 07 — Ghost Recovery

> Patterns after a human has stopped replying — recovery messaging, when to try again, when to stop.

## Pattern summary

1 ghost-proxy patterns detected.

## Examples of outbound follow-up cadence (sanitized, dash-free)

> conv `hrgwvUJOx7It1cHNOUdw` — outbound: 8, inbound: 1
> conv `diImOvU3TROkJkHhmVQ5` — outbound: 8, inbound: 1
> conv `JjH2XKTo4OEQyHtx53lK` — outbound: 8, inbound: 1
> conv `NMqTiNcyMAI01Erdu90I` — outbound: 8, inbound: 1
> conv `lSbIftaVR4ghiLiaHZ0g` — outbound: 8, inbound: 1

## Dash-free training version

Recovery message shape:
- Reference a previous unanswered message
- Add new value
- Keep it short
- Include a soft exit

## What the agent should learn

- After 3 unanswered follow-ups, the conversation is dead. Stop.
- Each re-engagement should add something new, not just "checking in."

## What the agent should avoid

- Don't send 5+ identical "just checking in" messages.
- Don't re-engage within 24h of the last message.
- Don't pretend to have new info when you don't.
