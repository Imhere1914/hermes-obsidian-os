# Website Opportunity Engine

_Generated: 2026-07-02T06:20:22.968641+00:00_

Detects website pain points from the canonical row and scores them 0-100.
Pain points are NEVER invented: only those supported by data fields are emitted.

## Engine inputs

- `data/business_repository/business_repository.jsonl` (canonical)
- `data/lead_finder/lead_finder_candidates.jsonl` (lead finder)
- Existing crawl outputs in `data/business_repository/*`

## Engine counts

- audits written: 1731
- scores written: 1731

## Pain point frequency

| pain_point | count |
| --- | --- |
| no_service_pages_detected | 1070 |
| no_chat_widget | 939 |
| no_business_social_links | 787 |
| no_booking_button | 736 |
| no_commercial_service_language | 720 |
| thin_content | 592 |
| no_website | 515 |
| no_clear_cta | 449 |
| no_trust_signals | 59 |
| parked_domain | 8 |
| facebook_only | 4 |

## Acquisition plan

- queries planned: 5
- estimated API calls: 20
- max API calls: 25
- field mask (text search): places.id,places.displayName,places.formattedAddress,places.location,places.busi...