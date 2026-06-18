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
  - "#calls"
  - "#voicemails"
  - "#recordings"
  - "#transcripts"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Calls and Voicemails"
fileIndex: "12"
---

# 12 — Calls and Voicemails

> Call records, voicemail patterns, recording and transcript URLs.

## Pattern summary

- Calls: 1,280
- Voicemails: 66,554
- Recording URLs: 0
- Transcript URLs: 0

## Call records

> `GHxCksMmu7Q53ACeQL0B` at `2026-05-14T14:52:50.981Z` — status: `None`, duration: `None`s
> `9yFtGvwdY0Yhby9pFFs5` at `2026-05-13T20:44:46.679Z` — status: `None`, duration: `None`s
> `9yFtGvwdY0Yhby9pFFs5` at `2026-05-13T14:20:26.627Z` — status: `None`, duration: `None`s
> `xUPlbP8X5KpxHtTqYNdJ` at `2026-05-12T14:20:56.955Z` — status: `None`, duration: `None`s
> `xUPlbP8X5KpxHtTqYNdJ` at `2026-05-12T14:20:24.354Z` — status: `None`, duration: `None`s
> `O3ukY6s7Y5iaitWdYzow` at `2026-05-27T17:05:02.553Z` — status: `None`, duration: `None`s
> `vSdVavjP2Y0V8Kkjchzu` at `2026-05-22T17:59:34.658Z` — status: `None`, duration: `None`s
> `vSdVavjP2Y0V8Kkjchzu` at `2026-05-22T17:58:58.262Z` — status: `None`, duration: `None`s
> `vSdVavjP2Y0V8Kkjchzu` at `2026-05-22T17:57:55.260Z` — status: `None`, duration: `None`s
> `vSdVavjP2Y0V8Kkjchzu` at `2026-05-22T17:57:41.430Z` — status: `None`, duration: `None`s

## Voicemail records

> `drVmCFHMpcuf6Rvse3L3` at `2025-10-14T14:26:06.771Z`
> `1atgv8ONB7cLV6oLHTB1` at `2025-10-16T16:54:05.957Z`
> `9N1xEgsIujBRfBj7iK81` at `2025-06-25T13:36:05.151Z`
> `TxgIOkKgfkmc0fT2IUr3` at `2025-10-15T16:00:59.692Z`
> `uhRFMA8zX6Kaf4IAEUgQ` at `2025-10-23T15:55:07.415Z`

## Recording / transcript metadata

_No recording or transcript URLs were returned by the extraction. The GHL `messages` endpoint does not include media URLs in the v2 schema; recordings are surfaced via the contact or appointment APIs._

## Dash-free training version

Call attributes preserved:
- conversation_id, contact_id, created_at
- call_status (completed / failed / no-answer)
- call_duration (seconds)
- direction

## What the agent should learn

- Calls in this corpus are inbound (humans calling back).
- Call duration is short (5 sec for VOICE_AI), suggesting IVR/AI-handled.

## What the agent should avoid

- Don't assume voicemail-based follow-ups are common — verify per account.
- Don't trust call_duration alone for engagement — 5s could be IVR pickup.
