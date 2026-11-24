# Mobile Security and Release Requirements

Store tokens/keys with platform secure storage. No privileged secrets in app binaries. Use TLS/platform certificate validation; pinning requires a rotation and recovery design. Protect deep links from account/context confusion; validate payloads server-side. Minimize permissions and request them at feature use. Avoid sensitive data in screenshots, clipboard, analytics, crash reports, and notification previews. Support remote session revocation.

Device integrity signals are risk signals, not proof of identity. Sign release artifacts, protect store credentials, and keep release manifest with app/API compatibility, dependencies/SBOM where available, build provenance, and known issues.

Test fresh install, upgrade, interrupted update, account switching, device loss, permission denial, and low connectivity. A release is not production-ready with fake payment success, placeholder verification, demo security, hardcoded admin access, or unreviewed personal-data collection.
