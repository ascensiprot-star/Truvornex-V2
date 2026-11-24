# Tenant Isolation and Delegated Authority

Personal account and each organization are separate security contexts. A resource may belong to an individual or organization. Every query/mutation must resolve active context and verify authority for that action and resource.

Use role plus attributes: role defines coarse capabilities; ownership, membership, resource scope, amount, region, purpose, and workflow state constrain execution. Default deny. Check at server execution, not only in UI.

Delegation stores grantor, grantee, organization, capability, resource/action/amount scope, effective/expiry dates, and revocation. Revocation must be prompt and auditable. High-impact permissions require explicit confirmation/authorized evidence.

Test IDOR, guessed IDs, cross-organization reads/writes, revoked membership, stale mobile context, background jobs, exports, and operator access. Do not rely on client filtering. RLS may add defense-in-depth but cannot replace application authorization.
