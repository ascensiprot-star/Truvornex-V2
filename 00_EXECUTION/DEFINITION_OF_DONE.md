# Definition of Done

A capability is done only when the problem and beneficiary are explicit; the primary and failure workflows are documented; domain ownership, invariants, states, permissions, and failure behavior are defined; and the workflow is usable without hidden manual intervention.

Correctness requires authoritative server validation, database constraints, idempotency where retries are possible, concurrency tests, explicit state transitions, and reconciled financial records. Security requires reviewed threat/abuse cases, object-level authorization, tenant isolation, managed secrets, audit, purpose and retention for sensitive data, and tested recovery.

Integrations require timeouts, bounded retries, idempotency, authenticated callbacks, logs/metrics/traces, backup and restore implications, deployment/rollback steps, and an accountable owner. Mobile requires loading, empty, success, error, offline, conflict, and permission-denied states where relevant, plus accessibility and localization tests.

Verification includes appropriate unit, component, integration, contract, migration, security, end-to-end, and operational tests. Environment-dependent tests must run in a real integration pipeline. A feature may be `EXPERIMENTAL`, `SANDBOX_ONLY`, or `DISABLED`; it may not be called production-ready until all applicable criteria pass.
