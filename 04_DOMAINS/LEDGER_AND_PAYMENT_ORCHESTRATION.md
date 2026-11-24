# Ledger and Payment Orchestration Domain

## Regulatory boundary

Default: Truvornex does not custody funds, issue e-money, maintain withdrawable balances, or independently execute regulated payment services. Integrate a licensed PSP. Disable real-money flows until counsel/provider confirm platform role, country coverage, onboarding/KYB, safeguarding, refunds, chargebacks, sanctions, settlement, and reconciliation duties.

## Internal financial records

Maintain immutable auditable payment intents, provider references, platform fees, taxes where known, refunds, disputes, and reconciliation. If a platform accounting ledger is required, use double-entry records with balanced immutable postings, explicit account types, currency consistency, and controlled corrections. Display balances are derived, never directly edited.

## Lifecycle

Requested → PSP-created → requires action → processing → succeeded/failed/cancelled → refunded/partially refunded/disputed/chargeback as applicable → reconciled. Map provider states explicitly and preserve original status alongside normalized status.

## Controls

Server-to-server confirmation; signed webhook verification; deduplication; out-of-order handling; reconciliation against PSP reports; idempotent create/capture/refund; distinguish authorization from settlement; never infer success from app redirect/screenshot/user assertion; separate platform fees, PSP fees, taxes, and provider payouts; correct via reversing/adjusting records, never destructive edits.

Money uses integer minor units or fixed precision plus ISO currency, not floating point. FX needs source, quote time, expiry, spread, fees, and explicit acceptance.
