# Threat Model

**Assets:** accounts/sessions; identity evidence; organization authority; service/resource availability; offers/agreements; payment references/ledger; invoices/documents; private messages; dispute evidence; API/deploy secrets; audit records.

**Threat actors:** credential thieves, impersonators, fake providers, malicious buyers, colluding users, abusive insiders, compromised devices, bot operators, attackers, dishonest partners, opportunistic fraud networks.

**Threats:** account takeover/session theft; IDOR/tenant escape; forged credentials/business identity; payment redirection; duplicate payment/refund; webhook spoofing; double booking; review collusion; scraping; harassment; insider misuse; prompt injection; data exfiltration; supply-chain compromise; ransomware; backup compromise; denial of service.

**Controls:** MFA/step-up, secure recovery, scoped authorization, tenant isolation, signed callbacks, idempotency, immutable financial records, rate limits, anomaly detection, encryption, secret rotation, dependency scanning, least-privilege operations, audit, minimization, tested backups, incident response, human review for consequential restrictions.

For each workflow write abuse stories: attacker goal, preconditions, exploit, harm, detection, prevention, mitigation, recovery, residual risk. Include insiders and collusion, not only external attacks. Update threat model when adding sensitive data, countries, providers, payments, AI tools, device permissions, or authority features.
