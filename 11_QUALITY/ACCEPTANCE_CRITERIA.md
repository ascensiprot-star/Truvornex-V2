# System Acceptance Criteria

**Actor/authority:** user acts personally or under authorized organization context; revoked membership prevents further commands; each acceptance records legal actor/authority.

**Discovery/capacity:** find eligible offers from declared capability and real availability; no double allocation under concurrency; stale/missing evidence is visible.

**Commitment:** request, offer, agreement, and order remain distinct; acceptance binds exact terms/version and current authority; material change requires amendment acceptance.

**Fulfillment:** provider submits completion evidence; receiving party accepts/rejects/requests correction; notification is not authoritative state.

**Payment:** user initiates partner-authorized flow; server authenticates callbacks, handles duplication/delay, normalizes status, and reconciles with provider; no fake success path.

**Trust:** every claim shows evidence type/source/scope/freshness; challenge possible; no unexplained universal score.

**Security/privacy:** tenant escape blocked; sensitive operator access audited; export/deletion tested; no secrets or unnecessary data in logs.

**Mobile/operations:** primary workflows have accessible loading/error/offline/conflict/empty/success states; cache cannot override server; production-like system can be deployed, observed, backed up, restored, and rolled back.
