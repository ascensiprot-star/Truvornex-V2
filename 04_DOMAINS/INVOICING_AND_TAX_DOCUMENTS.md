# Invoicing, Tax, and Business Documents

Truvornex may create/transmit/store business documents but must not imply a generated document satisfies every country's tax law. Invoice responsibility, VAT treatment, numbering, correction, archive, and reporting depend on seller status, transaction type, territory, and national law.

Document model: type, issuer, recipient, legal entity, transaction reference, issue date/tax point, currency, lines, tax categories, totals, correction relationship, schema/profile version, provenance/signature, transmission status, and retention class.

Support structured standards such as EN 16931 and applicable national specifications; assess Peppol/access-point ecosystems. Keep canonical invoice semantics separate from country serialization.

Invoice issuance, transmission/acceptance, payment, and accounting reconciliation are different states. Validate arithmetic, prevent duplicate invoice identifiers within issuer-defined series, preserve credit-note/correction links, and log access. Obtain qualified local tax/legal review before activation.
