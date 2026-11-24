# European Regulatory Applicability Register

**Reference snapshot: 24 November 2026.** Engineering research only, not legal advice. Exact duties depend on platform role, services, funds/data flows, country, user type, and contract. Qualified local legal review is required before country launch.

| Framework | Why it may matter | Engineering implications | Required validation |
|---|---|---|---|
| GDPR (EU 2016/679) | Personal data processing and rights. | Purpose/legal basis, minimization, rights, security, processors, transfers, DPIA when required. | Controller/processor roles and national enforcement. |
| eIDAS 2.0 / EUDI Wallet (EU 2024/1183 + implementing acts) | Identity, credentials, trust services, signatures. | Wallet adapter, selective disclosure, issuer metadata, conformance, consent UX. | Real production availability, technical profile, role obligations. |
| PSD2 and evolving EU/national payment-services law | Marketplace money flows, payment initiation/execution/account functions. | Licensed PSP integration; document platform role; no custody/regulated activity without authorization. | Current legal perimeter, national transposition, partner agreement. |
| Instant Payments Regulation (EU 2024/886) | Euro instant transfer and payee verification obligations primarily on PSPs. | PSP rail compatibility and reconciliation. Truvornex is not thereby a PSP. | Provider coverage and country-specific dates/features. |
| AML/CFT and sanctions law | Merchant onboarding/payment flows. | Define responsibility split, data handling, escalation, evidence. | Whether Truvornex itself has obligations and current national implementation. |
| VAT in the Digital Age (ViDA) | VAT digital reporting and e-invoicing. | Structured invoice model and country adapters. EU-wide cross-border B2B digital reporting/e-invoice obligation is scheduled from 1 July 2030; domestic rules vary. | Transaction type, seller status, national implementation and technical standard. |
| EN 16931 / national CIUS / Peppol | Structured e-invoice interoperability. | Canonical invoice schema and national serialization/validation. | Applicable profile, network/access-point and mandates. |
| Digital Services Act | Potentially applies if service is intermediary/hosting/online platform. | Terms, notice/action, trader traceability, transparency/complaint workflows where applicable. | Service classification, thresholds, exemptions. |
| Digital Markets Act | Relevant if designated gatekeeper and covered service. | Monitor only if actual designation/scope makes applicable. | Legal applicability; do not assume for a new platform. |
| Data Act (EU 2023/2854) | Data access/sharing, switching and interoperability in covered contexts. | Data access/contract terms, portability, cloud switching, connected-product data when relevant. | Role/product context. Generally applies from 12 Sep 2025, with transition/provision nuances. |
| AI Act (EU 2024/1689, as amended) | Simon and AI-enabled workflows. | AI inventory, risk classification, transparency, literacy, documentation, oversight/evaluation where required. | Intended purpose, use context, amended dates, national implementation. |
| NIS2 and national cyber laws | Entity type/sector/size or supply-chain role may bring scope. | Proportionate security, incident handling, access, continuity, supplier controls. | Actual entity scope and national transposition. |
| European Accessibility Act | Certain products/services, including covered e-commerce services. | Accessible mobile journeys, information, support, and interfaces where in scope. | Service classification and applicable exemption/national rules. |
| Consumer/platform-to-business law | Distance contracts, unfair terms, cancellation, ranking, trader relations. | Counterparty, pricing, disclosures, cancellation, complaint and ranking transparency. | Country-specific rules. |
| Platform-work/employment law | Workflows may affect worker classification or platform-work duties. | Avoid control/discipline/algorithmic management without legal review. | Operating model and national law. |

## Official source register

- European Digital Identity: https://commission.europa.eu/topics/digital-economy-and-society/european-digital-identity_en
- eIDAS 2.0: https://digital-strategy.ec.europa.eu/en/policies/eudi-regulation
- Instant Payments Regulation (ECB): https://www.ecb.europa.eu/paym/retail/instant_payments/html/instant_payments_regulation.en.html
- eInvoicing / EN 16931: https://single-market-economy.ec.europa.eu/single-market/public-procurement/digital-procurement/einvoicing_en
- ViDA implementation: https://taxation-customs.ec.europa.eu/taxation/vat/vat-digital-age-vida_en
- AI Act: https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai
- Data Act: https://digital-strategy.ec.europa.eu/en/policies/data-act
- Single Market Strategy: https://single-market-economy.ec.europa.eu/single-market/strategy_en

## Regulatory operations

For each country-feature pair, sign off service description, role, user type, data/funds flows, EU and national instruments, partner authorization, disclosures, retention, complaints, reporting, and launch blockers. Never use one generic “EU compliant” flag.
