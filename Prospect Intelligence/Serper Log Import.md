# Serper Log Import

**Generated:** 2026-06-30T04:37:14.500Z

**Records added by serper-log-import-* run_ids:** 0 run_ids

## Run IDs


## Source files mined

- `/home/dee/Developer/business-flow-automator/data/prospect_corpus/louisiana_hvac/2026-06-29-1748/prospects_enriched.jsonl`
- `/home/dee/Developer/business-flow-automator/data/prospect_corpus/louisiana_hvac_debug/2026-06-29-1807/prospects_enriched.jsonl`
- `/home/dee/Developer/business-flow-automator/data/prospect_corpus/louisiana_hvac_debug/2026-06-29-1813/prospects_enriched.jsonl`
- `/home/dee/Developer/business-flow-automator/data/prospect_corpus/louisiana_hvac_debug/2026-06-29-1826/prospects_enriched.jsonl`

## How to re-run

```bash
npx tsx scripts/mine-serper-logs.ts
```

The script is idempotent: it dedupes by place_id, phone, and domain against the
current canonical repo. Re-running produces 0 new records unless a new log file appears.