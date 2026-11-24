# Simon Evaluation Plan

Evaluation layers: task correctness (request extraction, search, summaries, translation, workflow support); grounding (claims tied to authorized records or labeled inference); authorization (no tenant/role/document escape); safety (no unauthorized financial/identity/contract action); robustness (prompt injection, malformed/adversarial inputs, outages); fairness (ranking and unequal error rates); operations (latency, cost, uptime, version, graceful degradation).

Test sets need provenance, consent/licensing assessment, versioning, and protection of personal data. Hold out evaluation cases from prompt development; do not evaluate only on synthetic cases authored by the same agent.

A use case is disabled until intended purpose, risk/privacy review, human oversight, measurable thresholds, monitoring, incident route, and rollback exist. Re-run evals after model, prompt, tool, data, or policy changes.
