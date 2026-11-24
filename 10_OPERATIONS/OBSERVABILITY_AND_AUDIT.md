# Observability and Audit

Use structured logs, metrics, and distributed traces with correlation IDs. Instrument API/database latency, queue/outbox lag/retries, provider latency/errors, mobile crashes, workflow conversion, and reconciliation anomalies.

Never log passwords, tokens, secrets, full payment credentials, identity docs, private message bodies, or unnecessary personal data. Redact sensitive fields; pseudonymize IDs; restrict telemetry access and retention.

Audit sensitive actions: security changes, role grant/revocation, evidence status, moderation, contract acceptance/amendments, payment commands/refunds, dispute decisions, data exports/deletions, operator access. Record actor, authority context, action, target, timestamp, correlation ID, reason, and before/after reference where appropriate.

Ordinary app roles cannot alter audit records. Corrections create separate events. Audit data is purpose-limited and monitored, not generalized surveillance.
