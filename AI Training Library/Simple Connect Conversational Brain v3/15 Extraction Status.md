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
  - "#extraction-status"
  - "#v3"
  - "#v3_from_v1brain"
title: "Extraction Status"
fileIndex: "15"
---

# 15 — Extraction Status

> Source: **v3_from_v1brain** corpus. v1brain extraction (2026-06-12), reused into brain builder 2026-06-17.

## Corpus at a glance

- Conversations: 77,000
- Messages: 387,647
- Inbound messages with body: 43,753
- Outbound messages with body: 267,579
- Booked conversations: 28,892
- Calls: 1,280
- Voicemails: 66,554
- Objection-pattern matches: 6,771
- 3+ inbound reply conversations: 1,090

## What this corpus is

The v3_from_v1brain corpus is a re-feed of the 2026-06-12 GHL live extraction
of all Simple_Connect conversations up to that point. It supersedes the
20-conversation v2 sample (Phase C.5.4 rerun, 2026-06-17) which was based
on a corrupted 5,000-row / 20-unique input file.

## How this vault was built

1. Raw v1brain extraction: `raw_all_messages/messages.jsonl` (387,647 records, 77,000 unique conversations)
2. Brain rebuild via `scripts/build_phase_c54_v2_brain.cjs --input <v1brain> --output-suffix v3_from_v1brain` — produced 5 v3 brain files plus metrics JSON
3. This vault built via `scripts/build_phase_c54_obsidian_vault.cjs` (parameterized) and Python one-pass builder

## What the agent should learn

- A 77,000-conversation corpus is statistically meaningful for SMS-pattern inference.
- Booking-rate (38%) is reliable at this scale.

## What the agent should avoid

- Don't read patterns from any v2-vault files — they reflect the 20-conv sample.
- Don't quote un-sanitized contact names.
