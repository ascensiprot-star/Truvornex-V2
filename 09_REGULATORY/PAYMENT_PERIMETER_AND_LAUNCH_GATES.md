# Payment Perimeter and Financial Launch Gates

Default model: Truvornex coordinates a transaction and uses a licensed PSP. The PSP performs regulated execution and applies its custody/safeguarding model. Truvornex stores only necessary workflow statuses, references, fee/reconciliation/accounting records.

Do not enable user-to-user stored balances, cash-out, pooled funds, escrow, lending, credit, investment, insurance, remittance, payment-account functionality, or custody in Truvornex accounts before legal clearance. Calling a UI element a “wallet” does not change the legal substance.

Provider diligence must cover territories/currencies, marketplace model, onboarding/KYB and beneficial ownership, sanctions responsibility, payment methods, settlement/payout, refunds/chargebacks, webhook security, reconciliation, reserves/fees, data processing/subprocessors, termination, and portability.

Live payment gate: legal perimeter opinion; signed provider agreement; production credentials; country flow approval; disclosures; fee/tax treatment; disputes/refunds; signed webhook verification; idempotency; reconciliation/accounting controls; incident response; end-to-end sandbox and production verification.

Never label internal accounting records “available money.” Distinguish requested, authorized, processing, succeeded, settled, refunded, and disputed exactly as provider semantics permit.
