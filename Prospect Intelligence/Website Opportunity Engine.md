# Website Opportunity Engine

_Generated: 2026-07-02T16:44:59.639974+00:00_

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

## Preview renderer

The Lead Finder preview renderer consumes the same canonical / mockup / preview
data this engine produces. Status (separate from the engine's reachability
state):

- compiled preview payload count: 19
- active preview count: 19
- expired preview count: 1 (acceptance fixture: `arlington-ac-heating-4f72e8-expired`)
- sparse fixture: 1 (`plano-hvac-cooling-service-3b6a0d-sparse`)
- Arlington AC acceptance slug: `arlington-ac-heating-4f72e8` (hvac_phone_first_v1)
- templates implemented: `hvac_phone_first_v1`, `contractor_quote_v1`, `generic_local_service_v1`
- preview renderer route: `/b2b-prospector/mockups/<previewSlug>`
- noindex policy: every render sets `<meta name="robots" content="noindex">`
- tap-to-call: resolves `vom_demo_number` ?? `payload.phone` -> `tel:<digits>`
- VOM demo number: field on the payload; null on all current fixtures
- no outreach performed: zero sends, zero SMS drafts, zero emails, zero DMs
- evidence bundle: `/tmp/lead_finder_mockup_evidence/`