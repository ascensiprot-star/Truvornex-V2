# Data Architecture and Consistency

PostgreSQL is the canonical production store for Truvornex-owned identity links, organization memberships, catalog/resources, requests/offers/agreements/orders, internal ledger records, workflow state, and audits. External systems remain authoritative for facts they issue or execute.

Mobile DB is cache/offline workspace only; every local write is a pending command until server confirmation. Use ACID transactions for invariants; write outbox row in the same transaction for async effects. Consumers use inbox/deduplication and idempotent handlers. Surface eventual consistency to users.

Every table/aggregate has an owning domain. Cross-domain reads use defined interfaces or projections. Tenant checks are server-side; PostgreSQL RLS may be defense-in-depth only when connection-pool context is safe.

Financial amounts use exact decimal/minor-unit semantics and ISO currency code, never binary floating point. Fee, tax, rounding, currency scale, and FX metadata are explicit. Every data class has purpose, owner, legal basis assessment, retention, export/deletion rules, encryption, and access policy.

Use versioned migrations, pre/postconditions, expand/contract for deployed mobile compatibility, and backup/restore evidence before destructive changes.
