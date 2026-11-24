# Critical State Machines

- **Account:** `pending_contact_verification → active → restricted/suspended → closure_requested → closed`.
- **Evidence:** `unsubmitted → submitted → pending_review → verified | rejected | unable_to_verify`; later `expired` or `revoked` without erasing history.
- **Listing:** `draft → submitted → under_review → published → paused | expired | withdrawn`; material edits create versions.
- **Offer:** `draft → issued → viewed → accepted | rejected | withdrawn | expired`; acceptance requires current version and valid authority.
- **Agreement:** `pending_acceptance → active → amended | completed | cancelled | disputed`; acceptance identifies exact terms, actor, authority, timestamp, evidence.
- **Order:** `created → scheduled → in_progress → fulfillment_submitted → accepted → closed`; exception states include change requested, cancelled, disputed, rejected, remediation required.
- **Payment:** normalized states `not_started`, `created`, `requires_action`, `processing`, `succeeded`, `failed`, `cancelled`, `partially_refunded`, `refunded`, `disputed`, `chargeback`. Map each PSP explicitly; keep original provider status.
- **Dispute:** `opened → triage → evidence_collection → review → decision_issued → appealed | closed`.

For each machine define valid transitions, actor permissions, preconditions, expiry/timeouts, events, notifications, compensation/recovery, and tests for invalid transitions and races.
