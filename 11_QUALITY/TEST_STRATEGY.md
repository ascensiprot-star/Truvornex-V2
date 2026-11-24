# Test Strategy

Test layers: unit tests for value objects, policies, state machines, authorization, financial arithmetic; component tests for modules/repositories; integration tests for PostgreSQL/outbox/object storage/provider adapters; contract tests for API/mobile/providers; end-to-end tests for economic workflows; security tests for IDOR/tenant escape/auth bypass/webhook spoofing/injection/rate limits/data leakage; mobile tests for accessibility/permissions/offline/context switching/lifecycle; operational tests for migrations/deployment/restore/replay/recovery.

Critical scenarios: duplicate request; concurrent capacity allocation; expired offer acceptance; revoked authority; context switch during pending command; duplicate/out-of-order PSP callback; provider success after timeout; refund retry; invoice correction; poison event; dispute during order change; data export/deletion; prompt injection; network loss during consequential action.

Use synthetic fixtures. Production data must not enter tests without approved anonymization and legal review. Include deterministic money, time zone/DST, language, and jurisdiction fixtures.

A skipped test due to missing dependency is not a pass. Mark env-dependent tests and provide integration pipeline. Do not hardcode local tool availability into product behavior.
