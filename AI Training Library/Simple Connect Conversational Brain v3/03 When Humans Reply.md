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
  - "#timing"
  - "#reply-gap"
  - "#cadence"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "When Humans Reply"
fileIndex: "03"
---

# 03 — When Humans Reply

> Reply-gap distribution — how long after our last message did humans respond?

## Pattern summary

Across 44,276 inbound reply events:
- **instant**: 39,940 replies (90%)
- **minutes**: 2,523 replies (6%)
- **hours**: 1,028 replies (2%)
- **weeks**: 407 replies (1%)
- **days**: 378 replies (1%)

## Examples of human reply timing (sanitized)

> Gap: `169967` min (weeks) — message type: `TYPE_SMS`
> Gap: `2` min (instant) — message type: `TYPE_CAMPAIGN_VOICEMAIL`
> Gap: `1440` min (days) — message type: `TYPE_SMS`
> Gap: `1440` min (days) — message type: `TYPE_SMS`
> Gap: `1441` min (days) — message type: `TYPE_SMS`
> Gap: `297093` min (weeks) — message type: `TYPE_SMS`

## Dash-free training version

Timing data is numeric; dash-free training preserves:
- gap_minutes (integer)
- gap_bucket (enum: instant/minutes/hours/days/weeks)
- direction sequence (outbound → inbound)

## What the agent should learn

- Human replies cluster in **minutes** bucket — agents should be ready to respond fast.
- Long gaps (days/weeks) exist but are minority.

## What the agent should avoid

- Don't send multiple follow-ups in rapid succession when a reply is already coming.
- Don't assume silence means disinterest — sometimes humans reply 24-48h later.
