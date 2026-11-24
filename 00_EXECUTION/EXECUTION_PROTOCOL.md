# Execution Protocol

Every work unit needs a bounded objective, prerequisite requirements, affected domains, artifacts, invariants, verification plan, and completion criteria. “Build this screen” is not a valid work-unit definition by itself.

Before editing, record languages/versions, entry points, data stores, schemas/migrations, environment variables, auth/session model, payment integrations, dependencies, tests, CI, deployment, logging, and current security posture. Verify current implementation instead of trusting documentation.

Use requirement IDs: `TRV-FND-*`, `TRV-DOM-*`, `TRV-SEC-*`, `TRV-REG-*`, `TRV-MOB-*`, `TRV-OPS-*`, `TRV-QA-*`. Every requirement links to implementation and verification evidence. Mark legal, partner, or research blockers as `BLOCKED`.

Changes to money movement, identity semantics, ownership, retention, cross-border eligibility, trust decisions, contract state, or system-of-record require an ADR and migration/rollback analysis.

Wrap every provider behind an adapter. Handle timeouts, duplicates, delays, out-of-order callbacks, signature verification, provider schema changes, and outage. Provider callbacks remain untrusted until authenticated and reconciled.

When work is incomplete, leave the branch safe and report blockers, assumptions, files changed, migrations applied/not applied, tests run, and exact resume instructions. A skipped test is not a passing test.
