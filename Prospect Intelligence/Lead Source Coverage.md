# Lead Source Coverage

_Generated: 2026-07-02T06:02:57.948429+00:00_

Lead Finder is the **umbrella layer** that joins the canonical
business repository with every lead_finder artifact (scores,
audits, mockups, previews, packs, social index). This view
answers: where did each lead come from, and how is it covered?

## Source counts (membership across acquisition_runs)

| source_type | records_with_this_source |
| --- | --- |
| google_places | 1731 |
| manual_import | 1731 |
| web_scrape | 1731 |
| historical_recovery | 1729 |
| serper | 1701 |
| website_crawl | 537 |
| social_handle_extraction | 396 |

## Source counts (primary_source_type)

| primary_source_type | records |
| --- | --- |
| serper | 1692 |
| web_scrape | 36 |
| google_places | 3 |

## Mixed provenance

- mixed_provenance (>= 2 source types): **1731** of 1731 records

## Coverage by readiness / artifact

| conversation_readiness_status | count |
| --- | --- |
| needs_enrichment | 958 |
| not_ready | 755 |
| needs_crawl | 11 |
| ready_for_review | 5 |
| no_ci_data | 2 |

## Field coverage

| field | count | pct |
| --- | --- | --- |
| with website | 1216 | 70.2% |
| with phone | 1686 | 97.4% |
| with email | 586 | 33.9% |
| with business social | 394 | 22.8% |
| with website_opportunity_score | 1731 | 100.0% |
| with mockup recommendation | 1185 | 68.5% |
| with preview_url | 1185 | 68.5% |
| with pitch_pack_available | 1185 | 68.5% |

## Validation

- overall: **PASS**
- failing: 0
- informational: 10