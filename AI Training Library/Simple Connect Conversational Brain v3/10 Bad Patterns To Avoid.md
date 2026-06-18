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
  - "#bad-patterns"
  - "#robotic"
  - "#spam"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Bad Patterns To Avoid"
fileIndex: "10"
---

# 10 — Bad Patterns To Avoid

> Patterns that signal low quality — robotic openers, too-many-followups, generic asks.

## Pattern summary

- "Just checking in"-style openers in this corpus: 6
- Convs with 5+ outbound and 0-1 inbound (over-followed): 5

## Examples of robotic openers (sanitized, dash-free)

> **msg_id `eDwyORPjoS…`** at `2025-10-15T14:26:10`
> Just following up real quick.

I’ve been speaking with a few businesses in your area who are looking for those kinds of services and I want to make sure I’m connecting with the right provider.

Are you currently open to more jobs like that?
> **msg_id `QvaWl3KWcb…`** at `2026-05-24T02:35:45`
> Just checking in — what name should I use for our conversation?
> **msg_id `n395cttHLk…`** at `2026-06-01T02:25:27`
> Hey—just following up to see if you saw my last message?
> **msg_id `N5IBhEliyJ…`** at `2026-05-30T20:55:08`
> Just checking in — what name should I use for this chat?
> **msg_id `2rsOqbr1er…`** at `2025-10-17T16:54:10`
> Just following up real quick.

I’ve been speaking with a few businesses in your area who are looking for those kinds of services and I want to make sure I’m connecting with the right provider.

Are you currently open to more jobs like that?
> **msg_id `g8xbWsrwLv…`** at `2026-05-10T20:41:28`
> Hi Billy, just circling back—wanted to see if you had any thoughts on my last question. No rush, just checking in.

## Examples of over-followed convs

> `hrgwvUJOx7It1cHNOUdw` — 8 outbound, 1 inbound
> `diImOvU3TROkJkHhmVQ5` — 8 outbound, 1 inbound
> `JjH2XKTo4OEQyHtx53lK` — 8 outbound, 1 inbound
> `NMqTiNcyMAI01Erdu90I` — 8 outbound, 1 inbound
> `lSbIftaVR4ghiLiaHZ0g` — 8 outbound, 1 inbound

## What classifies as a bad pattern

- "Just checking in" / "Just wanted to..." openers (no information added)
- "Hope this finds you well" / "Hope you're doing well"
- Same message re-sent with minor wording changes
- 4+ follow-ups without inbound reply
- Generic opener without context-specific reference

## What the agent should learn

- Every message should add new value. If you can't, don't send it.
- Generic openers are detectable by humans and tank response rates.
- Follow-up cadence: max 3 total outbound without reply.

## What the agent should avoid

- "Just checking in" — banned.
- "Hope this finds you well" — banned.
- Re-sending the same template with date changes.
- Sending 5+ follow-ups to a non-replier.
