# Native Mobile Information Architecture

## Client rule

Flutter is the first-party client for Android/iOS. Support role-aware workspaces without assuming a person has one role only. Navigation should expose the user's next meaningful task, not internal modules.

## Proposed top-level navigation

- **Home:** actionable overview, pending approvals, open requests, upcoming commitments, alerts.
- **Network:** discover people, organizations, providers, services, and resources within permitted market and filters.
- **Work:** requests, offers, agreements, orders, schedules, fulfillment, invoices, disputes.
- **Simon:** contextual assistance and insights with provenance/uncertainty.
- **Profile:** identity, organizations, delegated permissions, credentials, privacy, security, preferences.

This is a design hypothesis. Validate task success and comprehension. Do not turn every domain into a tab.

## Role context

A user may act personally or for an organization. The active context must be visible before any action that could bind the user/entity. Before contract acceptance or payment approval, show legal actor, authority scope, counterparty, amount, currency, and consequences.

## Screen families

Search/discovery; provider/resource detail; request creation; quote comparison; agreement review; order detail/timeline; calendar/capacity; organization/member management; credential evidence; payment status/invoices; dispute center; settings/privacy; notifications; support/reporting.

Each workflow needs loading, empty, offline, permission-denied, validation-error, conflict, provider-unavailable, success, and retry states where relevant. Confirm consequential actions. Keep cancellation, appeal, export, and privacy controls discoverable.

Use semantic design tokens. Country flags/themes may decorate but must not encode eligibility, nationality, trust, or verification. No public browser frontend. A provider-hosted web redirect is an external integration, not a Truvornex web product.
