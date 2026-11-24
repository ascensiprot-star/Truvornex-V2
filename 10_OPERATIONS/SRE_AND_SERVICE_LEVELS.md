# Reliability Engineering and Service Objectives

Define service-level indicators before objectives. Critical journeys include login, discovery, request creation, offer acceptance, order status, payment-status refresh, and dispute submission.

Measure request success, latency percentiles, error rate, availability, crash-free mobile sessions, outbox lag, PSP webhook lag, DB saturation, backup freshness, and restore success. Set targets after usage/risk analysis; do not invent impressive availability numbers.

Separate critical paths from optional services. Maps/Simon outage must not prevent access to existing agreements/orders. A PSP outage must be reported honestly; it must not be interpreted as payment failure or success without authoritative confirmation.

Every alert needs an owner, severity, runbook, and action. Review error budgets and incidents; avoid dashboards without operational owners.
