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
  - "#trust"
  - "#rapport"
  - "#first-message"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Trust Building Patterns"
fileIndex: "04"
---

# 04 — Trust Building Patterns

> Outbound message patterns that establish rapport early.

## Pattern summary

5 outbound messages matched trust-building language (name-introduction, role-disclosure, soft opener).

## Examples (sanitized, dash-free)

> **msg_id `OBEN5ijHLY…`** at `2026-06-01T02:36:06`
> Could you tell me the name you prefer I use here?
> **msg_id `NPExl7zyBr…`** at `2026-05-27T02:35:52`
> What's the best name to use so I know who I'm talking to?
> **msg_id `QvaWl3KWcb…`** at `2026-05-24T02:35:45`
> Just checking in — what name should I use for our conversation?
> **msg_id `dyKan7Hs0L…`** at `2026-05-23T02:35:40`
> Following up — please tell me your name so I know who I’m talking to?
> **msg_id `RqVG7VUNuT…`** at `2026-05-22T20:35:32`
> I’m Renee — I work with a company that talks to service shops about how their front end handles calls, texts, and booking. Who am I speaking with?

## Dash-free training version

Trust-building messages tend to:
- Use first-name self-identification early
- Acknowledge context
- Avoid hard asks in the first message

## What the agent should learn

- Identify yourself by first name in early messages.
- Use a context-acknowledgement pattern.
- Don't push for a meeting in message 1.

## What the agent should avoid

- Don't open with a generic "Hi, I'm X from Y" — too templated.
- Don't assume context without referencing it.
- Don't use "Hope this finds you well" — flagged as robotic.
