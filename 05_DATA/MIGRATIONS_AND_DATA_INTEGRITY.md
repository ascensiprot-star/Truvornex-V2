# Migrations and Data Integrity

All schema changes are versioned, repeatable in controlled environments, observable, and compatible with currently supported mobile releases.

Use expand/contract for active clients. Add constraints safely against legacy data. Back up and prove restore before destructive changes. Data migration scripts need dry-run, counts, invariant checks, and audit output. No unlogged manual production edits. Never rewrite historical financial postings; issue correction/reversal records.

Use foreign keys, unique/check/non-null constraints and transactional updates for ownership, state, and financial invariants. Add concurrency tests for capacity allocation and payment idempotency.

Reconciliation jobs detect orphan records, unmatched PSP transactions, unprocessed outbox rows, stale holds, missing invoice relations, duplicate callbacks, and inconsistent aggregate versions. Report anomalies and use reviewable corrections.
