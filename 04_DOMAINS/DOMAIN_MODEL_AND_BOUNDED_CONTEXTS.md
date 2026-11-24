# Domain Model and Bounded Contexts

## Core domain

Economic coordination: represent needs and capabilities; discover possible counterparties; establish offers and explicit agreements; manage orders and fulfillment; record payment status and financial evidence; resolve exceptions.

## Supporting domains

Identity/access; organizations/delegation; verification/credentials; catalog/capability; resources/capacity; communication; documents/invoices; disputes/appeals; reputation evidence; notifications; pricing/subscriptions; policy/jurisdiction; intelligence/analytics.

## Shared concepts

`ActorId`, `PersonId`, `OrganizationId`, `LegalEntityId`, `ResourceId`, `RequestId`, `OfferId`, `AgreementId`, `OrderId`, `PaymentReferenceId`, `DisputeId`. `Money` = exact amount + currency code + scale. `Jurisdiction` is an explicit territory. `Evidence` includes source, type, issuer, subject, scope, timestamp, expiry, verification method, status, and access policy. `Capability` describes what an actor/resource can do, under what conditions, and with what evidence.

## Invariants

One active legal actor is identified for each contractual action. Offer acceptance references exact offer version. An order references accepted agreement. Fulfillment is not accepted by the provider who submitted it unless policy expressly defines self-attestation. Payment status derives from authenticated provider confirmation or reviewed reconciliation. A dispute preserves challenged evidence and state history.

Keep aggregates small enough for transactional consistency. Avoid a giant User aggregate. Use explicit commands/events between domains. Define boundaries before tables.
