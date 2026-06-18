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
  - "#corpus-quality"
  - "#v3"
  - "#v3_from_v1brain"
title: "Corpus Quality"
fileIndex: "16"
---

# 16 — Corpus Quality

> Corpus-level quality assessment for the **v3_from_v1brain** Simple_Connect build.

## Headline

77,000 unique conversations / 387,647 messages / 43,753 inbound-with-body messages.
This is a **production-scale corpus** — usable for both prompt-engineering examples and statistical inference on the Simple_Connect SMS/call patterns.

## Channel distribution (per-conversation channel_mix aggregated)

- `TYPE_SMS`: 173,990
- `TYPE_ACTIVITY_OPPORTUNITY`: 94,798
- `TYPE_CAMPAIGN_VOICEMAIL`: 66,554
- `TYPE_ACTIVITY_CONTACT`: 37,600
- `TYPE_EMAIL`: 12,457
- `TYPE_CALL`: 1,280
- `TYPE_ACTIVITY_APPOINTMENT`: 667
- `TYPE_LIVE_CHAT`: 192
- `TYPE_LIVE_CHAT_INFO_MESSAGE`: 74
- `TYPE_FACEBOOK`: 16

## What makes this corpus training-grade

| Threshold | Status |
|---|---|
| ≥1,000 conversations | ✓ (77,000) |
| ≥100 conversations with 3+ inbound | ✓ (1,090) |
| ≥10,000 inbound messages with body | ✓ (43,753) |
| Booking signal density | 38% |
| Channel diversity | 14 distinct channels |

## What the agent should learn

- The 77,000-conversation corpus reflects the actual SMS/IVR landscape of Simple_Connect.

## What the agent should avoid

- Don't generalize HVAC-industry patterns to other verticals.
