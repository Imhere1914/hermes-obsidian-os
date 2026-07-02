# Preview Renderer

_Generated: 2026-07-02T19:04:46.085495+00:00_

## Purpose

The Lead Finder preview renderer serves structured JSON
payloads under `data/lead_finder/preview_payloads/<slug>.json`
and renders them via deterministic React templates. No
freeform AI-generated code or copy at render time. No
outreach performed from this view.

## Route

- pattern: `/b2b-prospector/mockups/:previewSlug`
- local preview: `http://127.0.0.1:4173/b2b-prospector/mockups/arlington-ac-heating-4f72e8`
- production preview URL (planned): `https://preview.simpleconnect.ai/mockups/<preview_slug>`

## Acceptance slug

- slug: `arlington-ac-heating-4f72e8`
- business_id: `bid_4f72e8f662f7deceacc4ee94`
- template: `hvac_phone_first_v1`
- phone (canonical, normalized): `8175575000`
- resolved `tel:` href: `tel:8175575000`

## Payload counts

| category | count |
| --- | --- |
| compiled (from report) | 19 |
| active (on disk, excluding fixtures) | 19 |
| sparse fixtures | 1 |
| expired fixtures | 1 |

## Template coverage

### Implemented (in scope)

- `hvac_phone_first_v1`
- `contractor_quote_v1`
- `generic_local_service_v1`

### Pending (out of scope until acceptance)

- `dental_trust_v1`
- `medical_clean_v1`
- `warehouse_b2b_v1`
- `property_management_v1`
- `security_low_voltage_v1`
- `retail_local_v1`
- `restaurant_local_v1`

## Tap-to-call behavior

- primary CTA is a tap-to-call phone button, sticky on mobile
- resolved `tel:` href = `tel:${vom_demo_number || phone}`
- `vom_demo_number` is null on every current fixture; tap-to-call
  falls back to the business real phone (e.g. `tel:8175575000`
  for the Arlington AC acceptance slug)

## VOM demo number fallback

- schema field present (`PreviewPayload.vom_demo_number`)
- if `vom_demo_number` is set, tap-to-call dials it; otherwise
  it dials the business real `phone`
- demo number provisioning is a downstream task; field stays
  null on all current fixtures

## noindex policy

- every preview render sets `<meta name="robots" content="noindex">` on mount
- the meta tag is removed on unmount
- expired / draft previews render the neutral "This preview has
  expired." page; **no business data leaks** on expired previews

## Page-view counter

- rows recorded: 6
- file: `data/lead_finder/preview_page_views.jsonl`
- one JSONL line per successful render
- local-disk only; no third-party analytics

## Evidence bundle

- path: `/tmp/lead_finder_mockup_evidence/`
- contents: route HTML, real-payload-served JSON, page-view
  counter before/after, screenshots, tel-href snapshot,
  `evidence_summary.md`

## Status

- **ready_for_dee_review**
- final acceptance: Dee's own browser screen-recording of the
  acceptance slug loading and showing the correct tap-to-call
  number. Recorded substitute evidence is in the bundle above.

## No outreach

- This view is read-only. No outreach is performed from it.
- No SMS drafts. No email drafts. No social DMs. No calls.
- No GHL export. No Outscraper. No n8n. No Serper. No live
  Google Places calls during renderer work.