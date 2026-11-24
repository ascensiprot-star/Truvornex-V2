# Canonical Entity Model

Conceptual model, not final SQL. Every entity needs a domain owner, lifecycle, identifier policy, privacy class, and migration plan.

**Identity/organization:** `Account`, `PersonProfile`, `AuthenticationFactor`, `DeviceSession`, `Organization`, `LegalEntityReference`, `Membership`, `DelegationGrant`, `Credential`, `VerificationEvidence`, `VerificationCheck`.

**Catalog/capacity:** `ServiceDefinition`, `ServiceListing`, `ListingVersion`, `Capability`, `Resource`, `ResourceAvailability`, `CapacityHold`, `ServiceArea`, `PriceQuotePolicy`.

**Coordination:** `Request`, `RequestVersion`, `MatchCandidate`, `Offer`, `OfferVersion`, `Agreement`, `AgreementAcceptance`, `Order`, `OrderMilestone`, `FulfillmentSubmission`, `FulfillmentAcceptance`, `Cancellation`, `ChangeOrder`.

**Financial/documents:** `PaymentIntent`, `PaymentProviderReference`, `PaymentStatusEvent`, `Journal`, `JournalEntry`, `RefundRecord`, `ReconciliationBatch`, `Invoice`, `InvoiceLine`, `BusinessDocument`, `TaxProfileReference`.

**Trust/operations:** `Conversation`, `Message`, `Notification`, `DisputeCase`, `Appeal`, `Review`, `AuditRecord`, `OutboxMessage`, `InboxReceipt`, `CountryCapability`, `ProviderConnection`, `ConsentRecord`, `DataSubjectRequest`.

Modeling cautions: an organization is not necessarily a legal entity; listing is not qualification; verified email is not legal identity; invoice is not payment; payment intent is not settlement; review is not verified fact; request is not agreement; provider callback is untrusted until authenticated and reconciled.

Use opaque non-sequential public IDs; never treat identifiers as authorization secrets.
