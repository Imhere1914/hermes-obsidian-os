# Business Repository

**Schema version:** 1 (canonical JSONL)
**Generated:** 2026-06-30T05:57:49.028751+00:00
**Maintained by:** SC Intelligence

Canonical record store at `data/business_repository/business_repository.jsonl`.
Single source of truth — every index in this directory is a view over it.

## Counts

- Total records: **41**
- Active: **18**
- Needs review: **10**
- Needs enrichment: **11**
- Lead-gen suspect: **2**
- Rejected (in `rejected_records.jsonl`): **21**

## Invariants

- Every record MERGES — never replaces existing business_ids
- Every business has exactly one `business_id` (sha1 of place_id or name+city+state key)
- Discovery → Enrich → Dedupe → Score → Merge counts always equal at every checkpoint
- Persistence: OFF. No Supabase, no GHL, no outreach
- Stage 2 cron/systemd is NOT enabled. Manual approval required

## Provenance

- Source files seen: **8**
- Records with phone: **37**
- Records with email: **7**
- Records with website: **41**
- Records with place_id: **17**

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