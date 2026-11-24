# Change Control and Architecture Governance

**Class A — local implementation:** refactor preserves public behavior, domain invariants, data semantics, and trust boundaries. Standard review/tests.

**Class B — contract change:** API, event, schema, mobile, identity attribute, trust evidence, or provider contract changes. Requires compatibility analysis, versioning, migration, test updates, and release notes.

**Class C — critical architecture change:** money/ledger semantics, custody, identity authority, authorization, country eligibility, system of record, privacy boundary, or AI authority. Requires an ADR, risk assessment, legal/compliance review where applicable, migration/rollback plan, and explicit approval.

ADRs include status, context, constraints, alternatives, decision, consequences, security/privacy impact, data migration, compatibility, verification, and revisit conditions. Accepted ADRs are not rewritten; supersede them with a new ADR.

No new microservice, database, broker, blockchain, proprietary credential, payment-custody feature, or AI model dependency without an ADR showing concrete need and operational ownership.
