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
  - "#channel"
  - "#sms"
  - "#call"
  - "#email"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "Channel Switching Logic"
fileIndex: "11"
---

# 11 — Channel Switching Logic

> When to stay on SMS, when to escalate to call, when to send email.

## Pattern summary

Channel mix across 387,647 messages:
- `TYPE_SMS`: 173,990
- `TYPE_ACTIVITY_OPPORTUNITY`: 94,798
- `TYPE_CAMPAIGN_VOICEMAIL`: 66,554
- `TYPE_ACTIVITY_CONTACT`: 37,600
- `TYPE_EMAIL`: 12,457
- `TYPE_CALL`: 1,280
- `TYPE_ACTIVITY_APPOINTMENT`: 667
- `TYPE_LIVE_CHAT`: 192
- `TYPE_LIVE_CHAT_INFO_MESSAGE`: 74
- `TYPE_FACEBOOK`: 16
- `TYPE_INSTAGRAM`: 8
- `TYPE_CUSTOM_EMAIL`: 5
- `TYPE_ACTIVITY_EMPLOYEE_ACTION_LOG`: 4
- `TYPE_SMS_REACTION`: 2

Conversations that switched SMS → call: 596

## Examples of channel transitions (sanitized)

> `GHxCksMmu7Q53ACeQL0B` — call at `2026-05-14T14:52:50.981Z`, duration `None`s, status `None`
> `9yFtGvwdY0Yhby9pFFs5` — call at `2026-05-13T20:44:46.679Z`, duration `None`s, status `None`
> `9yFtGvwdY0Yhby9pFFs5` — call at `2026-05-13T14:20:26.627Z`, duration `None`s, status `None`
> `xUPlbP8X5KpxHtTqYNdJ` — call at `2026-05-12T14:20:56.955Z`, duration `None`s, status `None`
> `xUPlbP8X5KpxHtTqYNdJ` — call at `2026-05-12T14:20:24.354Z`, duration `None`s, status `None`

## Dash-free training version

Channel switching decision tree:
1. Inbound SMS unanswered for 24h → try one more SMS
2. Inbound SMS says "call me" or "let's talk" → call within 1h
3. Outbound SMS bounced → switch to email
4. Outbound SMS delivered, no reply, 3rd attempt → STOP

## What the agent should learn

- Don't switch channels just to "try a different way" if the human already saw the message.
- Phone calls after explicit human request work; cold calls in this corpus are rare.

## What the agent should avoid

- Don't auto-call after SMS silence. Cold calls from SMS-conversation context are jarring.
- Don't send 5 emails after 5 SMS — that's spam across channels.
- Don't mix channels within the same response cycle.
