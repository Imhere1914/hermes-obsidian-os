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
  - "#index"
  - "#brain"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Brain Index"
fileIndex: "00"
---

# 00 — Simple Connect Conversational Brain Index (v3_from_v1brain)

> Master entry for the **v3_from_v1brain** vault. Built from the full Simple_Connect GHL extraction of 77,000 unique conversations / 387,647 messages.

## Source files

- V1Brain extraction (2026-06-12, raw): `/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/live_threads/Simple_Connect/run_full_2026-06-12T19-12-17Z_v1brain/raw_all_messages/messages.jsonl` (387,647 records, 283 MB)
- V3 brain files: `/home/dee/Developer/business-flow-automator/_libraries/conversational_brain/full/*v3_from_v1brain.jsonl` (5 files + metrics, rebuilt 2026-06-17)
- Obsidian vault: `~/Developer/hermes-obsidian-os/AI Training Library/Simple Connect Conversational Brain v3/`

## Corpus metrics

| Metric | Value |
|---|---:|
| Total conversations | 77,000 |
| Total messages | 387,647 |
| Inbound messages w/ body | 43,753 |
| Outbound messages w/ body | 267,579 |
| Conversations w/ 3+ inbound | 1,090 |
| Booked conversations | 28,892 |
| Calls | 1,280 |
| Voicemails | 66,554 |
| Objection patterns | 6,771 |

## Pattern summary (one line per file in this vault)

- **01 What Humans Say** — inbound message shapes, length buckets, opener patterns
- **02 How Humans Say It** — punctuation, casing, abbreviations, emoji usage
- **03 When Humans Reply** — reply-gap distribution (instant / minutes / hours / days)
- **04 Trust Building Patterns** — name-asking, role-asking, soft openers
- **05 Curiosity Patterns** — questions humans ask before buying
- **06 Objection Handling** — price, timing, "already have a guy" patterns
- **07 Ghost Recovery** — patterns after no-reply follow-ups
- **08 Appointment Setting** — booking language and confirmation patterns
- **09 When To Stop** — STOP / opt-out / not-interested signals
- **10 Bad Patterns To Avoid** — robotic openers, too-many-followups
- **11 Channel Switching Logic** — SMS → call → email transitions
- **12 Calls and Voicemails** — call types, durations, recording links
- **13 Dash Free Writing Rules** — replacement rules for em/en dashes
- **14 Retrieval Map** — when to load which file (intent → file)
- **15 Extraction Status** — current run state
- **16 Corpus Quality** — production-grade assessment
- **17 Human Exchange Coverage** — human-vs-system message analysis
- **18 Full Corpus Rebuild** — history from 20-conv seed to 77K corpus
- **19 V1Brain Source Map** — audit trail from v1brain to v3
- **20 Training Readiness** — can this corpus train a production model?

## Retrieval tags

`#phase-c5-4` `#simple-connect` `#conversational-brain` `#b2b-low-voltage` `#hvac` `#sms-heavy` `#booking-heavy`

## What the agent should learn

- This is a **production-scale corpus** for Simple_Connect (HVAC-dominant SMS patterns).
- Booking-rate is 37.5% — high signal density.
- 43,753 inbound-with-body messages provide ample direct-quote examples.

## What the agent should avoid

- Don't generalize HVAC patterns to other verticals — corpus is HVAC-dominant.
- Don't assume voicemail audio is available — only metadata.
- Don't conflate with v2 vault (20-conv sample) — that was a phase artifact, not the real corpus.
