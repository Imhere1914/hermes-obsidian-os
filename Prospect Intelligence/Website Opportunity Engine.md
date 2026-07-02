# Website Opportunity Engine

_Generated: 2026-07-02T19:23:31.808768+00:00_

Detects website pain points from the canonical row and scores them 0-100.
Pain points are NEVER invented: only those supported by data fields are emitted.

## Engine inputs

- `data/business_repository/business_repository.jsonl` (canonical)
- `data/lead_finder/lead_finder_candidates.jsonl` (lead finder)
- Existing crawl outputs in `data/business_repository/*`

## Engine counts

- audits written: 1752
- scores written: 1752

## Pain point frequency

| pain_point | count |
| --- | --- |
| no_service_pages_detected | 1070 |
| no_chat_widget | 950 |
| no_business_social_links | 796 |
| no_booking_button | 741 |
| no_commercial_service_language | 725 |
| thin_content | 594 |
| no_website | 518 |
| no_clear_cta | 460 |
| no_trust_signals | 60 |
| parked_domain | 8 |
| facebook_only | 4 |

## Acquisition plan

- queries planned: 6
- estimated API calls: 24
- max API calls: 25
- field mask (text search): places.id,places.displayName,places.formattedAddress,places.location,places.busi...