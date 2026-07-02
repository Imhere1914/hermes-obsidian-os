# Lead Finder

_Generated: 2026-07-02T06:46:30.748452+00:00_

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
- social handles indexed: 859
- canonical near-duplicates routed to human review: 20

## Score distribution

| band | count |
| --- | --- |
| urgent_opportunity | 4 |
| good_opportunity | 79 |
| possible_opportunity | 1107 |
| low_priority | 546 |

## Validation

- overall: **PASS**
- failing_issues: 0
- informational_issues: 13

## Next recommended move

- If --dry-run validates: request explicit human approval before --live.
- --live run will execute Google Places text search + place details, merge into canonical, re-run the rest of the pipeline.
- Serper is OFF by default. To enable as fallback for a specific --live run, pass `--allow-serper-fallback`.
- No outreach. No SMS. No email sending. No social DMs.