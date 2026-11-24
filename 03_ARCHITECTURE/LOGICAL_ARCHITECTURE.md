# Logical Architecture

Start with a modular monolith: testable domain modules, explicit interfaces, a small number of runtime processes (API, worker, scheduled jobs, controlled migrations/ops commands). They may share a codebase and domain libraries.

Layers: Flutter presentation; API boundary (auth, validation, rate limits, versioning, idempotency); application/use-case orchestration; domain model/policies/state machines; infrastructure (PostgreSQL, outbox, adapters, object storage, optional cache); intelligence/analytics isolated from transaction authority; operations (telemetry, audit, deployment, backup, support).

Modules: identity/access; organization/delegation; verification/credentials; catalog/capability; resource/capacity; discovery/matching; request/offer; agreement/order; fulfillment; payment/ledger records; invoicing/documents; communication; dispute/appeal; reputation; notifications; fees/subscriptions; policy/country configuration; intelligence.

Domains own state and publish stable interfaces. Avoid arbitrary cross-module table writes. Shared kernel stays small (IDs, Money, currency, time, jurisdiction, audit metadata). Extract a service only when measured scaling, fault isolation, release autonomy, regulatory isolation, or team ownership justify the operational cost.
