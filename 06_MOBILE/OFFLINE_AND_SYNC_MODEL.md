# Offline and Synchronization Model

Offline support is selective and does not make the client authoritative. Read caches, drafts, unsubmitted requests, and message composition may work offline with explicit freshness/pending state.

Do not complete offline: agreement acceptance, contested capacity allocation, organization authority changes, fulfillment confirmation, identity verification, payment initiation/confirmation, refund, or dispute resolution. These require fresh server validation.

Queued command metadata: command ID, creation time, principal/context, schema version, payload, idempotency key. Server resolves it as accepted/rejected/conflict/expired. Never replay blindly after account or organization context changes.

Use optimistic concurrency and explicit conflict resolution; never silently overwrite. Retain user drafts during conflict. Encrypt sensitive local data, use OS secure storage for tokens/keys, clear caches on logout/context switch as appropriate, and support lost-device revocation.
