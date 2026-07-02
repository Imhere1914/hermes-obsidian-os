# Lead Finder

_Generated: 2026-07-02T16:44:59.616775+00:00_

## Source strategy

- 1) Existing canonical repository (`data/business_repository/business_repository.jsonl`)
- 2) Existing local crawl outputs
- 3) Public business website crawling
- 4) Google Places API (used in --live mode only, with explicit cap and approval)
- 5) Serper API: **NOT used in this run** (disabled by default; reserved as fallback only)

## Compliance

- Outscraper: NOT used
- n8n: NOT used
- GHL: NOT used (no GHL export, no GHL workflow, no GHL integration)
- Serper: NOT used in this run
- Google Places live: not run in this pilot (default mode is --dry-run). Cap: 25 calls. Estimated calls: see acquisition_plan.json.
- Outreach: NONE performed. No SMS, no calls, no email sending, no social DMs.

## Run summary

- mode: `dry-run`
- vertical: `hvac`
- metro: `Dallas-Fort-Worth`
- state: `TX`
- queries planned: 5
- estimated API calls: 20
- max candidates: 50
- max API calls: 25

## Pipeline counts

- candidates processed: 0
- merged by place_id: 0
- merged by phone+domain: 0
- merged by name+address: 0
- skipped (franchise or unrelated): 0
- newly created canonical records: 0
- website audits: 1736
- scores: 1736
- mockup recommendations: 1190
- preview URLs: 1190
- pitch packs: 1190
- social handles indexed: 863
- canonical near-duplicates routed to human review: 20

## Score distribution

| band | count |
| --- | --- |
| urgent_opportunity | 4 |
| good_opportunity | 77 |
| possible_opportunity | 1109 |
| low_priority | 546 |

## Validation

- overall: **PASS**
- failing_issues: 0
- informational_issues: 14

## Next recommended move

- If --dry-run validates: request explicit human approval before --live.
- --live run will execute Google Places text search + place details, merge into canonical, re-run the rest of the pipeline.
- Serper is OFF by default. To enable as fallback for a specific --live run, pass `--allow-serper-fallback`.
- No outreach. No SMS. No email sending. No social DMs.

## Preview renderer

The Lead Finder preview renderer is live in dev / preview only. It serves
structured JSON payloads under `data/lead_finder/preview_payloads/<slug>.json`
and renders them via deterministic React templates. **No outreach performed.**

- route: `/b2b-prospector/mockups/:previewSlug` (Vite preview at 127.0.0.1:4173)
- compiled preview payload count: 19
- active preview count: 19
- expired preview count: 1 (acceptance fixture: arlington-ac-heating-4f72e8-expired)
- sparse fixture: 1 (plano-hvac-cooling-service-3b6a0d-sparse; phone/area/services/CTA-text all null)
- Arlington AC acceptance slug: `arlington-ac-heating-4f72e8`
- Arlington AC business_id: `bid_4f72e8f662f7deceacc4ee94`
- templates implemented: `hvac_phone_first_v1`, `contractor_quote_v1`, `generic_local_service_v1`
- noindex policy: every render sets `<meta name="robots" content="noindex">`
- tap-to-call: `tel:` href resolves to `vom_demo_number` if set, else `payload.phone`
  (Arlington test: `vom_demo_number=null`, `phone="8175575000"` -> `tel:8175575000`)
- VOM demo number field: present in the schema (`PreviewPayload.vom_demo_number`),
  null on all current fixtures; wiring to the demo number source is a downstream task
- page-view counter: writes one JSONL line per successful render to
  `data/lead_finder/preview_page_views.jsonl` via the Vite plugin
- no outreach performed: zero send actions, zero SMS drafts, zero emails, zero
  DMs, zero GHL/Outscraper/Serper/Google Places calls during this milestone
- evidence bundle: `/tmp/lead_finder_mockup_evidence/`