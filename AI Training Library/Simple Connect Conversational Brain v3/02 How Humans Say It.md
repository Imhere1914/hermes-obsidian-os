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
  - "#style"
  - "#punctuation"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "How Humans Say It"
fileIndex: "02"
---

# 02 — How Humans Say It

> Style and punctuation patterns in inbound messages.

## Pattern summary

Across 43,270 tagged inbound messages:
- **Questions:** 1,182 (3%)
- **Greeting openers:** 826 (2%)
- **Length buckets:** short 39,710 / medium 2,262 / long 1,233 / very_long 65

## Examples (sanitized, dash-free)

> **msg_id `MpAsyh6rjU…`** at `2025-03-22T20:11:27`
> Welcome to join [[name] Capital], your trusted investment partner! As a leading global financial institution, we will provide you with tailor-made investment solutions, whether it is stocks, options, day trading, cryptocurrencies, etc., we can help you seize every opportunity and
> **msg_id `PynPDhFobU…`** at `2025-09-03T22:25:12`
> [name],

I am responding to the following message from you

"[name], Brandy here.

Quick question. Do you do commercial work like access control, camera installs, or low-voltage projects?
Thanks, [name]
Just following up real quick.

I've been speaking with a few businesses in yo
> **msg_id `f0Me8tXEgw…`** at `2025-10-31T19:05:51`
> With all due respect, I am a thirty-five year Entrepreneur, the last twenty-five in the [name] Integration industry as an award-winning, multi-million dollar company operating put of [name], CA. To use the term "unqualified" in a any manner towards my company is an absolute insul
> **msg_id `4LMz5qzYUi…`** at `2025-01-21T12:50:54`
> Help? In which way??? [name]? Not sure what that is at the moment, I havenât time to research.

My phone never stops ringing, as my reputation proceeds me, that being said:

We are trying to locally rank for these simple â[name] Servicesâ: by achieving rankings here we 
> **msg_id `CGOLSId1wT…`** at `2025-07-08T16:14:11`
> I wanted to introduce you to Bumpboxx ([link] — we design and sell the hottest, loudest, and by far the coolest-looking Bluetooth speakers on the market.

What makes Bumpboxx truly unique is the ability to fully customize each speaker with your company’s colors and logos. They’re
> **msg_id `hVfdWCwV5G…`** at `2025-07-16T14:20:50`
> DQoNCioqKiBQbGVhc2UgZW50ZXIgcmVwbGllcyBhYm92ZSB0aGlzIGxpbmUgKioqICAg
ICANCg0KUVVFVUVEOiBbRVhUXSAgUmVhY2hVQyBtZXNzYWdlIHJlY2VpdmVkIGF0IHRl
bDoxMzMwMjM0NTAyNSBmcm9tIHRlbDoxMjEzNzE1NTU3NyAtIFQyMDI1MDcxNi4wMDQ1
DQoNCkEgc2VydmljZSB0aWNrZXQgaGFzIGJlZW4gY3JlYXRlZCBhbmQgaXMgaW4gbGlu


## Dash-free training version

Style preservation:
- Casing preserved. Emojis preserved (mostly absent in this corpus).
- Em/en dashes replaced with spaces (see file 13).

## What the agent should learn

- Humans ask questions casually — lowercase, no greeting.
- Periods are rare in inbound SMS; line breaks even rarer.
- Em-dashes and en-dashes are absent from human writing (they're operator artifacts).

## What the agent should avoid

- Don't send messages with em-dashes to humans.
- Don't over-punctuate — humans don't.
- Don't echo formal greeting patterns back at humans.
