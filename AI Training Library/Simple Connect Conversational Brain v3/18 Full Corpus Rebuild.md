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
  - "#rebuild"
  - "#v3"
  - "#v3_from_v1brain"
  - "#phase-c5-5"
  - "#phase-c5-6"
  - "#history"
title: "Full Corpus Rebuild"
fileIndex: "18"
---

# 18 — Full Corpus Rebuild

> Why this vault exists. The history from 20-conv seed to 77,000-corpus v3.

## Timeline

1. **2026-06-09 to 2026-06-13 (v1brain run)** — Full live extraction of Simple_Connect from GHL API. Cap 80,000, walked 159,440 conversations, deduped to 77,000 unique. Output: `/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/live_threads/Simple_Connect/run_full_2026-06-12T19-12-17Z_v1brain/` (270 MB conversation_brain_v1.jsonl, 283 MB raw_all_messages/messages.jsonl with 387,647 records).

2. **2026-06-13 to 2026-06-16 (reconstruction)** — Built 32-file `reconstructed_brain/` with gold/nurture/failure/decision/channel brains. All 7 validation tests PASS.

3. **2026-06-17 (Phase C.5.4 rerun)** — Tried to extract from a corrupted input file (5,000 rows / 20 unique IDs). Built v2 sample (20 convs / 289 messages).

4. **2026-06-17 (Phase C.5.5)** — Created Gate 6 (unique-ID sufficiency check). Determined Simple_Connect corpus ceiling is 100 unique convs in the corrupted input.

5. **2026-06-17 evening (reconciliation)** — Discovered the v1brain extraction had been sitting on disk since 2026-06-13. Wrote `docs/GHL_MESSAGE_COUNT_RECONCILIATION.md`.

6. **2026-06-17 evening (this vault)** — Generalized scripts and re-built brain + vault from the full v1brain messages.jsonl.

## Source-to-vault mapping

| This vault file | Derived from |
|---|---|
| 00 Brain Index | v3 brain files (5 JSONL + 1 metrics) |
| 01-13 pattern files | messages.jsonl field analysis + v3 brain |
| 14 Retrieval Map | intent-routing from vault file tags |
| 15 Extraction Status | v3 metrics |
| 16 Corpus Quality | v3 metrics + enriched channel_mix |
| 17 Human Exchange Coverage | v3 metrics + messages array |
| 18 Full Corpus Rebuild (this file) | v1brain history |
| 19 V1Brain Source Map | v1brain file paths |
| 20 Training Readiness | v3 metrics vs training thresholds |
| retrieval_index.json | all files + intents |

## What the agent should learn

- The corpus was always 77,000 conversations — the 20-conv seed was an artifact of a corrupted input.

## What the agent should avoid

- Don't re-run the v1brain extraction — its output is preserved on disk.
- Don't trust the corrupted `high_signal_conversation_ids.jsonl`.
