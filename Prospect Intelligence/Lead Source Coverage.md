# Lead Source Coverage

_Generated: 2026-07-02T19:40:22.141631+00:00_

Lead Finder is the **umbrella layer** that joins the canonical
business repository with every lead_finder artifact (scores,
audits, mockups, previews, packs, social index). This view
answers: where did each lead come from, and how is it covered?

## The three categories (Part 2 taxonomy)

- **discovery_source_types** = sources that originally acquired the business
- **enrichment_source_types** = sources that enriched an already-known business
- **workflow_source_types** = internal pipeline stages that touched the record

A stage that merely re-imports or enriches a record CANNOT claim
to have discovered it. `social_prospecting_desk` is workflow,
not discovery. `canonical_repository` is workflow. `lead_finder`
is workflow.

## Discovery source counts (membership across acquisition_runs)

| discovery_source | records_with_this_source |
| --- | --- |
| serper | 1698 |
| web_scrape | 48 |
| google_places | 29 |

## Primary discovery source distribution

| primary_discovery_source_type | records |
| --- | --- |
| serper | 1690 |
| web_scrape | 33 |
| google_places | 29 |

## Mixed discovery

- mixed_discovery (>= 2 discovery sources): **17** of 1752 records

> A record is mixed_discovery only if it was originally discovered
> by more than one source. Workflow and enrichment steps do NOT
> make a record mixed_discovery.

## Enrichment source counts

| enrichment_source | records_with_this_source |
| --- | --- |
| website_crawl | 558 |
| social_handle_extraction | 404 |

## Workflow source counts

| workflow_source | records_with_this_source |
| --- | --- |
| social_prospecting_desk | 1731 |

## Why enrichment != discovery

Every canonical record gets touched by the social-prospecting-desk
offline re-import (workflow) and most get a website_crawl pass
(enrichment). That does NOT mean 1,731/1,731 records were
discovered by those sources. Discovery attribution requires an
original acquisition artifact (prospects_raw.jsonl, phase_d_places,
phase_e_la, pilot_output). The numbers above reflect that.

## Coverage by readiness / artifact

| conversation_readiness_status | count |
| --- | --- |
| needs_enrichment | 976 |
| not_ready | 758 |
| needs_crawl | 11 |
| ready_for_review | 5 |
| no_ci_data | 2 |

## Field coverage

| field | count | pct |
| --- | --- | --- |
| with website | 1234 | 70.4% |
| with phone | 1707 | 97.4% |
| with email | 593 | 33.8% |
| with business social | 403 | 23.0% |
| with website_opportunity_score | 1752 | 100.0% |
| with mockup recommendation | 1204 | 68.7% |
| with preview_url | 1204 | 68.7% |
| with pitch_pack_available | 1204 | 68.7% |

## Validation

- overall: **PASS**
- failing: 0
- informational: 14
- checks_run: 43