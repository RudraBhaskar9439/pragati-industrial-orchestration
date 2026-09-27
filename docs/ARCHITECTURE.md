# Architecture

## Current prototype

```text
Browser
├── index.html              Static application shell
├── styles.css              Responsive presentation layer
└── src/app.js              Route rendering, demo data, interactions
    └── localStorage        Fictional applicant-side demonstration state
```

There is no API server, database, authentication provider, document bucket, external AI model or department integration. A static origin serves all assets. Hash routes make module links work without server-side route rewrites. Browser state is local to the current origin and device.

## Domain concepts represented

- **Project profile** — applicant and project characteristics collected through KYA.
- **Approval catalogue** — illustrative nodes with departments, dependencies, document hints and sample durations.
- **Dependency graph** — approval edges determine readiness and parallel work opportunities.
- **Application draft** — local wizard state without an authority submission.
- **Document metadata** — sample type, expiry, status and validation message; no file content storage.
- **Case event** — fictional timeline entries shown in applicant and officer views.
- **Officer work item** — synthetic queue row, SLA indicator and human-controlled action proposal.

## Intended production boundaries

Separate identity, applicant profile, approval catalogue, case orchestration, document management and notification services. Treat each department as the authority for its own status and requirements. Use versioned, sourced rules with effective dates; represent unknown applicability explicitly; and retain human review for extracted or disputed information. Every cross-agency integration requires an approved data-sharing basis, consent model, least-privilege authorization, traceable audit events, retention policy and failure/reconciliation plan.

The prototype's estimates and classifications are presentation data, not an executable regulatory rules engine. A production risk model requires approved features, bias assessment, explainability, monitoring, appeal and officer override controls.
