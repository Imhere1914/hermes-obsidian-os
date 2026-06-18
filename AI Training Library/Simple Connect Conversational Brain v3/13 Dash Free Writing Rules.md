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
  - "#writing"
  - "#dash-free"
  - "#preprocessing"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Dash Free Writing Rules"
fileIndex: "13"
---

# 13 — Dash Free Writing Rules

> Replacement rules applied to convert em/en dashes to spaces before training inputs. Dashes confuse some models (treated as minus signs) and never appear in human-written text in this corpus.

## Replacement table

| Original | Replacement | Reason |
|---|---|---|
| `—` (em-dash, U+2014) | space | Avoid minus-sign confusion in tokenizers |
| `–` (en-dash, U+2013) | space | Same |
| Multiple spaces | single space | Normalize |
| Tab | single space | Normalize |

## What the agent should learn

- Don't use em-dashes or en-dashes in outbound messages.
- Use periods, commas, or just spaces between clauses.
- Models trained on dash-free text learn cleaner sentence boundaries.

## What the agent should avoid

- Don't write "—" or "–" in any agent-generated text.
- Don't preserve dashes from raw training data — always run dash-free preprocessing.
