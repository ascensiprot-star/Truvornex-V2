# Deployment and Runtime Architecture

Reference runtime: Flutter app stores; versioned HTTPS API; async worker using durable outbox; PostgreSQL primary with managed backups; private object storage with short-lived authorized access; optional non-authoritative cache; managed observability and secret management.

Separate local, automated-test, integration/sandbox, pre-production, and production environments. No production data on developer machines. Separate provider sandbox/production keys. Deploy reproducibly from version-controlled configuration and immutable artifacts.

Use liveness/readiness checks, bounded timeouts, connection limits, graceful shutdown, backpressure, and safe worker restart/replay. Maps or Simon outages must not take down core order access. Measure before adding brokers, read replicas, or independent services. Apply least-privilege service identities, private database networking, encrypted transport, managed secrets, dependency scanning, and controlled migrations. No credentials in source or mobile binaries.
