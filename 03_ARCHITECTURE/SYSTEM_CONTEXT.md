# System Context Architecture

Truvornex sits between economic participants and external authoritative or regulated systems. It coordinates workflow and evidence; it does not replace institutions that issue legal identity, register companies, license professions, settle payments, or administer tax.

External actors/systems: individuals, providers, SMEs, organizations, platform operators, EUDI Wallets/national eID, business and professional registries, PSPs/banks/payment networks, e-invoicing networks, notification gateways, maps/geocoding, observability, support tooling, and public institutions where integration exists.

Trust boundaries: (1) mobile device ↔ API — client is untrusted; (2) backend ↔ provider — adapter boundary, signed callbacks and reconciliation; (3) tenant boundaries — object/row-level authorization; (4) operators ↔ user data — privileged and audited; (5) Simon ↔ transaction domains — advisory only; (6) country adapter ↔ core domain — explicit capability contract.

Truvornex owns internal IDs, request/offer/order/workflow state, agreements accepted in its product, event history, policy, and records of provider-reported status. External facts carry source, timestamp, verification method, and freshness/expiry.

Implementation must include version-controlled C4 context and data-flow diagrams. Every external system must show data sent/received, purpose, legal/contract status, failure modes, and owner.
