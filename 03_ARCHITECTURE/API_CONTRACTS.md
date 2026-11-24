# API Contract Standards

Use versioned HTTPS APIs with explicit schemas, stable IDs, bounded pagination/filtering, standardized errors, and OpenAPI contracts. Model state changes as explicit commands with actor, target, preconditions, idempotency key where needed, and expected version—not arbitrary patch endpoints.

Authenticate every request and enforce object-level authorization for every object ID. Apply request limits, schema validation, rate/abuse controls, and safe errors. Never trust client role, price, status, tenant, or ownership fields.

Idempotency keys are required for retryable operations (especially order and payment commands); scope to principal+operation, store request hash/result, reject reuse with different payload. Use optimistic concurrency and explicit conflict responses. Errors contain stable code, safe user message, field errors where suitable, correlation ID, retryability; never expose stack traces, internal rules, DB IDs, or provider secrets.

Version breaking changes. Support deployed mobile versions intentionally. Contract-test Flutter/API. External provider schemas stay inside adapters.
