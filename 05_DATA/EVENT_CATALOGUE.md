# Canonical Event Catalogue

Initial event families (exact payloads must be schema-versioned):

| Domain | Events | Meaning / sensitivity |
|---|---|---|
| Identity | `AccountCreated`, `ContactVerified`, `SessionRevoked` | Authentication facts; no credentials/tokens in payload. |
| Organization | `MembershipGranted`, `MembershipRevoked`, `DelegationChanged` | Authority facts; reference protected evidence. |
| Trust | `EvidenceSubmitted`, `EvidenceVerified`, `EvidenceExpired` | Restricted; no raw document content. |
| Catalog | `ListingPublished`, `ListingPaused`, `CapabilityChanged` | Publish only policy-approved projections. |
| Capacity | `AvailabilityChanged`, `CapacityHeld`, `CapacityReleased` | Location/schedule details are restricted. |
| Coordination | `RequestSubmitted`, `OfferIssued`, `OfferAccepted` | Access-limited to participants. |
| Agreement | `AgreementActivated`, `AgreementAmended`, `AgreementCancelled` | Contract details confidential. |
| Orders | `OrderCreated`, `MilestoneUpdated`, `FulfillmentSubmitted` | Evidence references restricted. |
| Payments | `PaymentIntentCreated`, `PaymentStatusChanged`, `RefundRecorded` | No card secrets; minimize provider data. |
| Documents | `InvoiceIssued`, `DocumentTransmitted` | Business-confidential and retention-controlled. |
| Disputes | `DisputeOpened`, `EvidenceAdded`, `DisputeResolved` | Highly restricted. |

Required envelope: `event_id`, `event_type`, `schema_version`, `aggregate_type/id/version`, tenant/actor scope where appropriate, `occurred_at`, `recorded_at`, `correlation_id`, `causation_id`, data classification, and minimal payload or protected reference.

Consumers tolerate additive optional fields. Breaking changes require new schema and migration plan. Retain data by classification/purpose. Never expose internal events wholesale through public APIs.
