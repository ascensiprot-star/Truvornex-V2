# Interoperability and Standards Strategy

Integrate existing public and regulated infrastructure rather than rebuilding identity, payment, or invoice rails.

**Identity:** adapter for EUDI Wallet/national eID. Request only attributes needed for a stated purpose. Store issuer, credential type, verification method, scope, issue/expiry/status, and minimal proof reference. Do not assume all country wallets are production-ready or identical.

**Payments:** licensed PSP/SEPA/local rails. Normalize status while retaining provider IDs and protected callback metadata. Redirect completion is not proof of payment.

**Invoicing:** investigate EN 16931, national CIUS, Peppol and access-point profiles as applicable. A PDF is not necessarily a structured e-invoice.

**Business/professional evidence:** use official sources only where legally available and technically supported; record source/freshness; do not invent universal registry APIs.

**Portability:** define exportable resources, formats, schema semantics, authorization, and revocation. Maintain a standards register with owner, version, jurisdiction, URL, conformance requirements, test profile, review date, and gaps.
