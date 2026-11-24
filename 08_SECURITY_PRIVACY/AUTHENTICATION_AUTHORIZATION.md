# Authentication and Authorization Standard

Use maintained auth libraries and reviewed protocols. Where passwords exist, use a modern password-hashing scheme with suitable parameters and unique salts. Prefer phishing-resistant MFA for privileged/high-risk actions. Protect session rotation, revocation, expiry, device management, and recovery.

Authorization is enforced server-side for every API and background job. Default deny; object-level checks; tenant scope; action scope; step-up for sensitive actions. Hidden buttons/client role flags are not security controls.

Administrative access requires named accounts, MFA, least privilege, just-in-time elevation where feasible, reason-for-access logging, and periodic review. Break-glass access is exceptional and audited. Recovery must resist social engineering; a weaker channel cannot silently grant equivalent authority. Notify users of critical credential/authority changes.
