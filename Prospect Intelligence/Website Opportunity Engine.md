# Website Opportunity Engine

_Generated: 2026-07-02T19:09:14.813463+00:00_

Detects website pain points from the canonical row and scores them 0-100.
Pain points are NEVER invented: only those supported by data fields are emitted.

## Engine inputs

- `data/business_repository/business_repository.jsonl` (canonical)
- `data/lead_finder/lead_finder_candidates.jsonl` (lead finder)
- Existing crawl outputs in `data/business_repository/*`

## Engine counts

- audits written: 1736
- scores written: 1736

## Pain point frequency

| pain_point | count |
| --- | --- |
| no_service_pages_detected | 1070 |
| no_chat_widget | 942 |
| no_business_social_links | 790 |
| no_booking_button | 738 |
| no_commercial_service_language | 722 |
| thin_content | 593 |
| no_website | 516 |
| no_clear_cta | 452 |
| no_trust_signals | 59 |
| parked_domain | 8 |
| facebook_only | 4 |

## Acquisition plan

- queries planned: 5
- estimated API calls: 20
- max API calls: 25
- field mask (text search): places.id,places.displayName,places.formattedAddress,places.location,places.busi...