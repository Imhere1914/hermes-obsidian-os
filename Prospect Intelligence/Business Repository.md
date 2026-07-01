# Business Repository

**Schema version:** 1.1 (canonical JSONL)
**Generated:** 2026-06-30T19:25:00.000Z
**Maintained by:** SC Intelligence

Canonical record store at `data/business_repository/business_repository.jsonl`.
Single source of truth — every index in this directory is a view over it.

## Counts

- Total records: **44**
- Active: **18**
- Needs review: **10**
- Needs enrichment: **14**
- Lead-gen suspect: **2**
- Rejected (in `rejected_records.jsonl`): **49**

## Invariants

- Every record MERGES — never replaces existing business_ids
- Every business has exactly one `business_id` (sha1 of place_id or name+city+state key)
- Discovery → Enrich → Dedupe → Score → Merge counts always equal at every checkpoint
- Persistence: OFF. No Supabase, no GHL, no outreach
- Stage 2 cron/systemd is NOT enabled. Manual approval required
- v1.1: every record carries `enrichment_status`, `crawl_history[]` (normalized), `tech_stack`, `expansion_signals`, `buying_signals`, `categories`, `website_platform`, `postal_code`, `last_extracted_at`

## Provenance

- Source files seen: **14**
- Records with phone: **39**
- Records with email: **7**
- Records with website: **44**
- Records with place_id: **20**

## Phase A Defect Repair

- **Completed:** 2026-06-30T19:23:06.754Z
- **Defects repaired (D-1..D-8):**
  - D-1: crawl_history.json backfilled from per-record crawl_history[]
  - D-2: missing enrichment_status defaulted to incomplete/pending
  - D-3: enrichment_history.json created and backfilled from enrichment_status
  - D-4: crawl_history[] schema normalized (crawl_id, started_at, finished_at, pages_fetched, bytes_downloaded, ok)
  - D-5: tech_stack added to every record (default null)
  - D-6: expansion_signals, buying_signals, categories (default []), website_platform, postal_code, last_extracted_at added (default null)
  - D-7: scripts/validate-repository.ts created
  - D-8: manifest updated to v1.1 with new field documentation
- **Validator:** `npx tsx scripts/validate-repository.ts` (9/9 checks pass after repair)

## Recent Remediation

- **2026-06-29 23:24 CT**: archived pre-remediation state to `data/business_repository/archive/2026-06-29-2324-pre-canonical-name-remediation/`
- Normalized `business_name` (split `:`, strip `, STATE`, strip `in <city>`, strip `...`)
- Cleared `legal_name` to null where it duplicated a defective `business_name`
- Moved aggregator/listicle candidates to `rejected_records.jsonl`
- Mined 156 existing Serper/api log files; merged 11 new needs_enrichment records (LA hvac)
- Rejected 5 aggregator/listicle records (4 from CSV parsing, 1 from improved listicle regex)
- **2026-06-30 00:56 CT**: removed 15 test-fixture records sourced from `/tmp/repo-build-*`
- Archived pre-removal state to `data/business_repository/archive/2026-06-30-0056-pre-test-artifact-removal/`
- All test artifacts moved to `rejected_records.jsonl` with `rejection_reason=test_artifact`
- **2026-06-30 14:25 CT**: Phase A structural defect repair (D-1..D-8) per spec; see `scripts/validate-repository.ts`

See:
- [Vertical Index](./Vertical Index.md)
- [Region Index](./Region Index.md)
- [Source Index](./Source Index.md)
- [Repository Quality Report](./Repository Quality Report.md)
- [Retrieval Index](./Retrieval Index.md)
- [Crawl Queue](./Crawl Queue.md)
- [Enrichment Queue](./Enrichment Queue.md)
- [Lead Send Backup](./Lead Send Backup.md)
- [Serper Log Import](./Serper Log Import.md)
