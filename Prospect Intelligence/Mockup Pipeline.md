# Mockup Pipeline

_Generated: 2026-07-02T16:44:59.641198+00:00_

Generates STRUCTURED mockup payloads only. Never random websites. Never freeform code.

## Template distribution

| template | count |
| --- | --- |
| generic_local_service_v1 | 1150 |
| hvac_phone_first_v1 | 22 |
| warehouse_b2b_v1 | 7 |
| property_management_v1 | 7 |
| medical_clean_v1 | 3 |
| dental_trust_v1 | 1 |

## Mockup priority

| priority | count |
| --- | --- |
| auto_build | 0 |
| build_after_review | 0 |
| save_for_later | 0 |
| do_not_pitch | 0 |

## Compliance

- Do not include license/insured/family-owned/24-7/guaranteed unless supported by source fields.
- Do not invent trust signals.
- Do not invent map_url.

## Preview renderer

- compiled payloads: 19 (in-scope templates only)
- active payload count: 19
- expired fixture: 1 (`arlington-ac-heating-4f72e8-expired`)
- sparse fixture: 1 (`plano-hvac-cooling-service-3b6a0d-sparse`)
- templates implemented: 3 (hvac_phone_first_v1, contractor_quote_v1, generic_local_service_v1)
- Arlington AC acceptance slug: `arlington-ac-heating-4f72e8` (hvac_phone_first_v1)
- noindex policy: enforced in the renderer (every page sets `<meta name="robots" content="noindex">`)
- tap-to-call: resolves `vom_demo_number` ?? `payload.phone` -> `tel:<digits>`
- VOM demo number: field is on the payload; null on all current compiled fixtures
- no outreach performed: renderer is a read-only render, no sends, no SMS, no email, no DM