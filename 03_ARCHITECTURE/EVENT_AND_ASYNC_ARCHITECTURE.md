# Event and Asynchronous Processing

Events are facts that occurred; commands request state changes. Event envelope: stable ID, type, schema version, aggregate ID/version, tenant/actor scope where applicable, occurred/recorded time, correlation/causation IDs, and privacy classification.

When async work follows a domain transaction, write domain change and outbox in one PostgreSQL transaction. Workers claim safely, deliver, record attempts, and retry transient failures with bounded backoff/jitter. Poison events go to a dead-letter state with diagnostics and controlled replay. Assume at-least-once delivery, duplicates, delay, out-of-order messages, provider timeout after success, and process restart.

Do not broadcast full personal, payment, credential, or document payloads through generic streams. Prefer authorized references. Initial event families include AccountCreated, MembershipGranted/Revoked, EvidenceVerified/Expired, ListingPublished, AvailabilityChanged, RequestSubmitted, OfferIssued/Accepted, AgreementActivated, OrderCreated, FulfillmentSubmitted/Accepted, PaymentStatusChanged, InvoiceRecorded, DisputeOpened/Resolved.

Do not use event sourcing by default. Keep current state in relational aggregates plus audit/event history where justified. Event-sourced aggregates require ADR and operational evidence.
