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
  - "#stop"
  - "#opt-out"
  - "#compliance"
  - "#f01-stop"
  - "#phase-c5-4"
  - "#v3_from_v1brain"
title: "When To Stop"
fileIndex: "09"
---

# 09 — When To Stop

> STOP / opt-out / not-interested signals. F01 STOP is the supreme compliance gate — once detected, no further outreach.

## Pattern summary

- STOP / opt-out patterns detected: 8

## Examples (sanitized, dash-free)

> 2026-05-11T22:00:39 [TYPE_SMS]
> NARI Nights is TOMORROW NIGHT at Bath & Kitchen Galleria! Register now! [link] -NARI Atlanta Text STOP to end
> 2026-05-13T13:17:05 [TYPE_SMS]
> 8th Annual Brew Bash is June 11th at Mutation Brewing! Register Here: [link] -NARI Atlanta Text STOP to end
> 2026-05-20T18:20:37 [TYPE_SMS]
> 8th Annual Brew Bash is June 11th at Mutation Brewing! Register Here: [link] -NARI Atlanta Text STOP to end
> 2026-05-27T18:26:17 [TYPE_SMS]
> 8th Annual Brew Bash is June 11th at Mutation Brewing! Register Here: [link] -NARI Atlanta Text STOP to end
> 2026-06-03T18:51:05 [TYPE_SMS]
> 8th Annual Brew Bash is NEXT WEEK at Mutation Brewing! Register Today! [link] -NARI Atlanta Text STOP to end
> 2026-06-09T18:49:30 [TYPE_SMS]
> SAVE THE DATE NARI Nights is July 14th at Cambria! Register Today! [link] -NARI Atlanta Text STOP to end
> 2026-06-10T18:47:57 [TYPE_SMS]
> 8th Annual Brew Bash is TOMORROW at Mutation Brewing! Register Today! [link] -NARI Atlanta Text STOP to end
> 2026-05-21T15:07:46 [TYPE_SMS]
> Hello, it depends on the job. However I see you are listed in San Antonio. At this time we only serve the Austin area. If you have a property in Austin that needs attention we can discuss the details 

## F01 STOP enforcement

When ANY of these patterns match an inbound message, the agent MUST:
1. Stop all further outbound messages to that contact
2. Tag the contact as `stop_or_optout`
3. Update internal state to prevent re-engagement
4. Log the STOP event for compliance audit

## What the agent should learn

- STOP language is sacred. Never negotiate with it.
- One STOP erases all prior engagement — don't try to recover.

## What the agent should avoid

- Don't send "are you sure?" after a STOP. That's a violation.
- Don't continue the conversation thread after STOP. Mark closed.
- Don't argue. Just stop.
