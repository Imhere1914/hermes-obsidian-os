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
  - "#human-exchange"
  - "#coverage"
  - "#v3"
  - "#v3_from_v1brain"
title: "Human Exchange Coverage"
fileIndex: "17"
---

# 17 — Human Exchange Coverage

> Per the **v3_from_v1brain** Simple_Connect corpus.

## Coverage ratios

- Total messages: 387,647
- Inbound with body: 43,753 (11%)
- Outbound with body: 267,579 (69%)
- Conversations with 3+ inbound replies: 1,090 (1% of corpus)
- Booked conversations: 28,892 (38% of corpus)
- Calls: 1,280
- Voicemails (metadata only): 66,554

## What this means for training

- 1,090 conversations with 3+ inbound replies = strong human-exchange signal density.
- 28,892 booked conversations = strong booking-language patterns.
- 43,753 inbound-with-body messages = ample direct-quote examples.

## Coverage gaps

- Recording/transcript URLs: 0 in this corpus.
- Calendar events join: not in this corpus.
- Voicemail audio: not in this corpus — only metadata.

## What the agent should learn

- Inbound rate is low (~11%) — Simple_Connect is outbound-heavy with brief human reply bursts.

## What the agent should avoid

- Don't extrapolate patterns from a single vertical (HVAC) to other industries.
