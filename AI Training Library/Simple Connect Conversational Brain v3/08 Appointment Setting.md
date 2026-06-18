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
  - "#appointment"
  - "#booking"
  - "#calendar"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Appointment Setting"
fileIndex: "08"
---

# 08 — Appointment Setting

> Booking language and appointment-conversation patterns.

## Pattern summary

- Conversations with booking signals: 28,892 / 77,000 (38%)
- Outbound booking-language messages: 6

## Examples of booking-language outbound (sanitized, dash-free)

> **msg_id `lRBY8VkZSf…`** at `2025-10-16T14:26:12`
> Out of curiosity, how do most new projects find their way to you right now?

Referrals, word of mouth, or are you doing any kind of outreach or marketing?

I work with providers to get them on the calendar with pre-qualified commercial clients. Might be worth a quick chat.
> **msg_id `MsLfjdYbhb…`** at `2026-05-24T02:15:19`
> When customers call to book a visit, who usually handles it — an in-house scheduler, the owner, or an answering service?
> **msg_id `3jes18DH3J…`** at `2026-05-23T20:44:15`
> Who should I list as the contact so someone can reach out and schedule the site visit?
> **msg_id `8RryEJPCN5…`** at `2026-05-22T14:41:02`
> I don’t have the address in this chat. What’s your name so I can get someone to reach out and schedule a look?
> **msg_id `pktGLyFPeF…`** at `2026-05-21T20:26:45`
> When things pile up, does your team actually book estimate appointments or do requests sit as messages until someone calls back?
> **msg_id `8aoCTppb9D…`** at `2026-05-20T17:54:40`
> Yes — that’s the service address. Which slot should I book: 2:00 PM, 3:00 PM, 4:00 PM, or 5:00 PM on 20 May'2026 (Wednesday)?

## Examples of booked conversations

> `drVmCFHMpcuf6Rvse3L3` — first booking outbound at `2025-06-18T13:36:39.698Z`, first human reply at `2026-05-11T22:00:39.275Z`
> `wwAwozIEPevQXaOvsjxQ` — first booking outbound at `2026-05-22T14:06:38.974Z`, first human reply at `2026-05-22T14:09:38.520Z`
> `PPkBtx96v5fOGEjJYegq` — first booking outbound at `2026-05-22T14:04:37.819Z`, first human reply at `2026-05-22T14:39:50.768Z`
> `uvznnY3apjXwoJ6btWrS` — first booking outbound at `2026-05-21T14:04:09.643Z`, first human reply at `2026-05-21T14:04:52.550Z`
> `StDKHn1vi9O4HNq7fTQj` — first booking outbound at `2026-05-20T14:04:20.976Z`, first human reply at `2026-05-20T14:19:04.447Z`

## Dash-free training version

Booking sequence:
1. Soften ("happy to chat through this — when works?")
2. Offer concrete times
3. Confirm with link
4. Reminder 24h before

## What the agent should learn

- Concrete time slots beat open-ended "when works for you?"
- Confirmation messages should include meeting link inline.
- Reminders 24h before reduce no-shows.

## What the agent should avoid

- Don't ask "when are you free?" — too open.
- Don't send booking links without context.
- Don't assume the meeting is confirmed if they just clicked the link.
