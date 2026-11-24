# Product Boundaries and Non-Goals

## Product boundary

Truvornex coordinates economic relationships and workflow state. External systems remain authoritative for government identity, business registration, professional licensing, bank accounts, payment execution, and tax filing unless a future legal model explicitly establishes otherwise.

## In scope

Account/identity linking; organizations/delegation; service and resource representation; discovery/matching; offers/quotes/commitments; orders/fulfillment; payment initiation through partners; payment-status and reconciliation references; structured documents/invoices; communications; disputes/evidence; trust evidence; analytics; country-specific configuration/integrations.

## Out of scope by default

Taking deposits into Truvornex-controlled accounts; holding withdrawable balances; issuing stored value; credit, insurance, lending, investment, remittance, or bank accounts; acting as recruitment agency/employer of record; making final public-benefit or legal eligibility decisions; issuing government credentials; replacing registries/tax administrations; giving legal, tax, or financial advice.

## Explicit non-goals

- Public web frontend or browser-first product.
- Broad engagement feed.
- Cryptocurrency/token or blockchain settlement without a concrete validated requirement.
- Microservice per domain.
- Bespoke identity wallet competing with EUDI Wallets.
- Bespoke payment rail competing with SEPA/local regulated rails.
- Opaque universal trust score.
- Launch in every European country without country-level validation.

## Boundary test

Does the feature coordinate a real economic workflow? Is it within the platform's lawful role? Is there an authoritative source or regulated partner to integrate? Does it create custody, employment, consumer, or data-protection duties? Can it be delivered with less data and less authority?
