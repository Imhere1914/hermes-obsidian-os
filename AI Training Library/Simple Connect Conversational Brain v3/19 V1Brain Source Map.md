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
  - "#source-map"
  - "#v1brain"
  - "#v3"
  - "#v3_from_v1brain"
title: "V1Brain Source Map"
fileIndex: "19"
---

# 19 — V1Brain Source Map

> Audit trail from v1brain extraction to this v3 vault.

## V1Brain root: `/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/live_threads/Simple_Connect/run_full_2026-06-12T19-12-17Z_v1brain`

| File | Size | Records | Used for v3 |
|---|---:|---:|---|
| `raw_all_messages/messages.jsonl` | 283 MB | 387,647 records — primary source for v3 brain |
| `raw_all_conversations/conversations.jsonl` | 66 MB | 79,720 records — full conversations with lastMessageBody |
| `raw_all_conversations/conversation_threads.jsonl` | 16 MB | 79,720 records — thread headers |
| `raw_contacts/contacts.jsonl` | 71 MB | 76,024 records — contact identity |
| `raw_calls/calls.jsonl` | 0.3 MB | 1,280 records — call records |
| `raw_emails/emails.jsonl` | 21 MB | 12,457 records — email bodies (3,984 with body) |
| `raw_voicemails/voicemails.jsonl` | 12 MB | 66,554 records — voicemail metadata |
| `raw_opportunities/opportunity_activity.jsonl` | 52 MB | 94,798 records — opportunity events |
| `raw_appointments/from_messages.jsonl` | 0.13 MB | 667 records — appointment events |
| `conversation_brain_v1.jsonl` | 270 MB | 77,000 unique conversations — consolidated brain |

## V3 brain files: `/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/full/`

| File | Records | Source |
|---|---:|---|
| `conversation_brain_high_signal_enriched_v3_from_v1brain.jsonl` | 77,000 | Derived from messages.jsonl grouped by conversation_id |
| `message_sequence_index_enriched_v3_from_v1brain.jsonl` | 387,647 | One row per message, ordered by created_at |
| `timing_intelligence_enriched_v3_from_v1brain.jsonl` | 310,647 | Per-message-pair gap timing |
| `objection_recovery_enriched_v3_from_v1brain.jsonl` | 6,771 | Objection / stop / price / ghost patterns |
| `humanistic_language_patterns_v3_from_v1brain.jsonl` | 310,746 | Message shape tags |
| `v3_from_v1brain_metrics.json` | aggregate | Run metrics |

## Reconstructed brain (separate, v1brain-direct)

| File | Size | Purpose |
|---|---:|---|
| `reconstructed_brain/gold_brain/gold_brain_main.jsonl` | 484 KB / 118 records | High-quality training examples |
| `reconstructed_brain/nurture_brain/nurture_brain_main.jsonl` | 2.5 MB / 695 records | Mid-funnel nurture patterns |
| `reconstructed_brain/failure_brain/failure_brain_main.jsonl` | 54 MB / 76,009 records | Failure patterns + P0 violations excluded |

## What the agent should learn

- The v3 brain files were derived FROM the v1brain raw_all_messages/messages.jsonl.
- The v1brain reconstruction directory was built independently from the same source.

## What the agent should avoid

- Don't conflate v3 (in _libraries/.../full/) with reconstruction.
