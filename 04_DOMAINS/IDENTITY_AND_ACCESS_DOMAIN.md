# Identity and Access Domain

Separate: login account (authentication principal); person profile (user-editable representation); legal identity evidence (issuer-backed proof); organization (Truvornex collaboration/authority boundary); legal entity (external registered entity); credential (issuer-backed qualification); session/device.

Support registration, verified contact methods, MFA/step-up based on risk, device/session management, recovery, closure, and identity-provider linking. Contact verification is not legal identity verification.

Build provider-neutral EUDI Wallet/national eID adapters. Request minimal attributes for a specific purpose; retain proof/result references rather than entire identity scans where possible. Wallet-unavailable alternatives must be lawful and reviewed.

Separate authentication from authorization. Enforce least privilege, scoped organization membership, revocation, object-level checks, and action-specific step-up. Record actor and authority for contractual/financial commands.

Identity evidence is sensitive: encrypt at rest, restrict access, avoid logs, set retention, provide access transparency, and support lawful deletion/anonymization. Never repurpose it for unrelated ranking or advertising.
