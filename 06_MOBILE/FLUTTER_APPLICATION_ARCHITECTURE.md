# Flutter Application Architecture

Use feature-first layered architecture. Widgets handle presentation; domain/application logic stays outside widgets; server remains authoritative. Use one approved state-management, routing, and typed networking approach consistently (existing Riverpod/GoRouter/Dio may be retained only after dependency and platform review).

Suggested structure: `app/` bootstrap/routes; `core/` theme/localization/network/storage/errors/telemetry; `features/<domain>/{presentation,application,domain,data}`; `design_system/`; `platform/` device adapters.

Separate server state, transient UI state, and local drafts/offline state. Cache invalidation and staleness must be explicit. Do not keep critical identity or money state only on device. Use typed models, centralized error mapping, cancellation, bounded retries for safe operations, idempotency keys for retryable commands, and correlation IDs.

Validate permissions, deep links, secure storage, background work, push, camera/media, and lifecycle independently on Android and iOS. Every client-supplied value is untrusted.
