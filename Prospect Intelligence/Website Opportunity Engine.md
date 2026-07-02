# Website Opportunity Engine

_Generated: 2026-07-02T21:38:51.466767+00:00_

Detects website pain points from the canonical row and scores them 0-100.
Pain points are NEVER invented: only those supported by data fields are emitted.

## Engine inputs

- `data/business_repository/business_repository.jsonl` (canonical)
- `data/lead_finder/lead_finder_candidates.jsonl` (lead finder)
- Existing crawl outputs in `data/business_repository/*`

## Engine counts

- audits written: 1974
- scores written: 1974

## Pain point frequency

| pain_point | count |
| --- | --- |
| no_service_pages_detected | 1070 |
| no_chat_widget | 1052 |
| no_business_social_links | 939 |
| no_booking_button | 829 |
| no_commercial_service_language | 796 |
| thin_content | 637 |
| no_clear_cta | 590 |
| no_website | 527 |
| no_trust_signals | 96 |
| parked_domain | 8 |
| facebook_only | 4 |

## Acquisition plan

- queries planned: 12
- estimated API calls: 24
- max API calls: 25
- field mask (text search): places.id,places.displayName,places.formattedAddress,places.location,places.busi...