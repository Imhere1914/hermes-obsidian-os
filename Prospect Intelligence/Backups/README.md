# Lead System Backups

Nightly gzip snapshots of the BFA lead repository (business_repository.jsonl)
plus dedupe/acquisition/enrichment indexes. Written by
`business-flow-automator/scripts/backup-repository-to-obsidian.sh` (cron,
02:30 UTC). Retention: forever. Vault pushes to GitHub = offsite copy.

- Latest snapshot: **2026-07-07** — **18389 records**
- Restore: `gunzip -c business_repository_<date>.jsonl.gz > .../business_repository.jsonl` then regenerate auxiliary indexes.
