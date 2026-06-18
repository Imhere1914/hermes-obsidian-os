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
  - "#training-readiness"
  - "#v3"
  - "#v3_from_v1brain"
title: "Training Readiness"
fileIndex: "20"
---

# 20 — Training Readiness

> Is the **v3_from_v1brain** corpus ready for production model training?

## Verdict

**YES** for prompt-engineering, few-shot examples, and pattern mining.
**YES (with caveats)** for fine-tuning a narrow-purpose agent on Simple_Connect SMS patterns.

## Threshold checks

| Check | Pass | Value |
|---|:---:|---|
| Conversations ≥ 1,000 | ✓ | 77,000 |
| Inbound-with-body messages ≥ 10,000 | ✓ | 43,753 |
| Conversations with 3+ inbound ≥ 100 | ✓ | 1,090 |
| Booked conversations ≥ 100 | ✓ | 28,892 |
| Distinct channels ≥ 3 | ✓ | 14 distinct channels |

## Key rates

- Inbound rate: 11%
- Outbound rate: 69%
- Booking rate: 38%
- 3+ inbound rate: 1%

## Recommended use cases

1. **Few-shot prompt construction** — Use file 01-07 for example selection.
2. **Style / tone inference** — Use file 02 and 13.
3. **Booking-language mining** — Use file 08 with the 28,892 booked-conversation subset.
4. **Compliance / STOP handling** — Use file 09.
5. **Quality-control pre-send checks** — Use file 10.

## NOT recommended for production training

- **Cross-industry generalization** — Simple_Connect corpus is HVAC-dominant.
- **Voice-only training** — only 1,280 call records; voicemail audio not available.
- **Reply prediction** — outbound rate (69%) is so much higher than inbound (11%) that reply-likelihood modeling would need a balanced dataset.

## What the agent should learn

- This corpus is production-scale for Simple_Connect SMS/call patterns.

## What the agent should avoid

- Don't claim this corpus is multi-vertical — it's HVAC-dominant.
