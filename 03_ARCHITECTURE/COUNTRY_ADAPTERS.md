# Country and Jurisdiction Adapter Architecture

Model legal-entity establishment, person residence, service delivery country, customer location, transaction currency, tax jurisdiction, and regulatory territory separately. These can differ.

Country adapters may implement identity methods, business-registry connectors, qualification checks, address parsing, local tax/e-invoice rules, consumer disclosures, payment options, permitted service categories, and document templates. They must not rewrite core domain semantics.

A capability record contains territory code, capability, enabled status, legal review status, source, effective date, expiry/review date, provider dependency, limitations, fallback, and owner. Production enablement requires explicit approval. If eligibility for a consequential/regulated workflow cannot be established, fail closed and explain the missing check.

Use granular flags (`identity_link_supported`, `provider_verification_limited`, `payment_provider_sandbox_only`, `e_invoice_not_supported`), not one misleading `country_supported=true`.
