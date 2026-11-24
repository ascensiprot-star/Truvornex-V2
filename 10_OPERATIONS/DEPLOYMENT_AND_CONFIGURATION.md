# Deployment and Configuration Management

Provision environments reproducibly. Configuration is explicit, validated at startup, and separate from source. Fail fast on missing critical settings; safe defaults for optional capabilities.

API changes must support already-installed mobile versions; do not assume app upgrades are immediate. Feature flags are scoped, audited, owned, and have expiry/review dates. Do not hide unfinished critical logic behind flags indefinitely.

Migrations run as controlled jobs, not arbitrary startup actions across replicas. Deployments need health checks, smoke tests, rollback/roll-forward guidance, artifact provenance, and accountable incident owner.

Country capability flags, PSP availability, AI provider settings, and operational policy require change history and approval.
