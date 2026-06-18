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
  - "#retrieval"
  - "#map"
  - "#intent-routing"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Retrieval Map"
fileIndex: "14"
---

# 14 — Retrieval Map

> When the agent encounters a situation, which file in this vault should it load?

## Intent → file map

| Agent situation | Load file |
|---|---|
| Human just replied | [[01 What Humans Say]] |
| Replying to a question | [[02 How Humans Say It]] + [[03 When Humans Reply]] |
| Building rapport early | [[04 Trust Building Patterns]] |
| Human asked a curious question | [[05 Curiosity Patterns]] |
| Human pushed back / objected | [[06 Objection Handling]] |
| No reply for 2+ days | [[07 Ghost Recovery]] |
| Trying to book | [[08 Appointment Setting]] |
| Human said STOP / opt-out | [[09 When To Stop]] |
| Drafting a generic message | [[10 Bad Patterns To Avoid]] |
| Switching from SMS to call/email | [[11 Channel Switching Logic]] |
| Call came in | [[12 Calls and Voicemails]] |
| Preprocessing outbound text | [[13 Dash Free Writing Rules]] |

## Retrieval tags by intent

- **curiosity**: `#curiosity` `#questions`
- **objection**: `#objection` `#price`
- **booking**: `#appointment` `#calendar`
- **stop**: `#stop` `#opt-out` `#f01-stop`
- **trust**: `#trust` `#rapport`
- **ghost**: `#ghost` `#follow-up`

## What the agent should learn

- One file at a time. Don't load the whole vault into context.
- `09 When To Stop` is the highest-priority file.

## What the agent should avoid

- Don't load all 20 files. Use the map.
- Don't bypass the retrieval map by loading the index.
