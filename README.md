# Truvornex — European Economic Infrastructure Blueprint

**Reference snapshot:** 24 November 2026. **Client:** Native Flutter app for Android and iOS; no public web product.

This repository defines the product, domain model, system architecture, security/privacy controls, regulatory research, operational requirements, and implementation discipline for Truvornex. It is a specification pack, not a claim that the platform is already built, legally authorized, market-validated, or production-ready.

Truvornex is intended to coordinate real economic activity: participants express needs and capabilities, discover counterparties, coordinate resources, agree explicit terms, fulfill commitments, document outcomes, and reconcile payment and business records. The mobile app is the interface; the underlying infrastructure is the product.

## Non-negotiable architecture baseline

- Flutter/Dart is the only first-party user-facing app for Android and iOS. Do not create a parallel public web frontend.
- The backend is authoritative. Mobile storage is a cache/offline workspace, never a competing source of truth.
- Use a modular monolith with clear domain boundaries initially. Do not split into microservices without measured justification.
- PostgreSQL is the default canonical transactional database. Any deviation requires an ADR.
- Use transactional outbox/inbox patterns for reliable asynchronous work. Start with a database-backed outbox and worker; introduce a broker only when justified.
- Retire the concept of a separate SQLite production backend for the Flutter client. Local SQLite may be used only for cache/drafts/offline queues.
- Simon AI is an advisory/intelligence subsystem. It must not control identity truth, legal eligibility, contract finality, ledger entries, or settlement.
- Europe is not one jurisdiction. Model EU, EEA/EFTA, UK, Switzerland, and any other supported territory separately.
- Do not custody funds or provide regulated financial services without legal authorization. Default to licensed PSP integrations.

## Reading order

1. `00_EXECUTION/MASTER_BUILD_DIRECTIVE.md` — paste this into the coding agent first.
2. `01_FOUNDATION/` and `02_PRODUCT/` — mission, problem evidence, actors, product boundaries, native mobile UX.
3. `03_ARCHITECTURE/`, `04_DOMAINS/`, `05_DATA/` — system design and economic lifecycle.
4. `06_MOBILE/`, `07_INTELLIGENCE/`, `08_SECURITY_PRIVACY/` — app, Simon, privacy and security.
5. `09_REGULATORY/` — country and financial launch gates.
6. `10_OPERATIONS/`, `11_QUALITY/`, `12_ECONOMICS_GOVERNANCE/` — operations, acceptance, network economics.
7. `13_DELIVERY/` — dependency order, implementation epics, open questions, ADR and traceability templates.

## What this blueprint does not claim

It does not establish market demand, regulatory compliance, legal permission, financial partner availability, or production readiness. Each must be demonstrated with evidence. **MUST** is normative; **SHOULD** requires a documented reason to deviate; **MAY** is optional. Current code is evidence of current behavior, not proof that the design is correct.
