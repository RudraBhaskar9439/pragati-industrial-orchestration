# PRAGATI | Industrial Approval & Compliance Orchestrator

A browser-based, multi-role prototype for discovering, preparing and tracking industrial approvals. PRAGATI models an applicant workspace and a department operations workspace with a dependency-aware approval roadmap.

> **Demonstration software.** PRAGATI is not an official government service. Applicant records, approval applicability, processing durations, SLAs, risk indicators, status events and department workflows are illustrative. There is no sign-in, backend, official portal integration, OCR service, AI inference, application transmission or government notification. Uploaded file contents are not stored or sent; the upload interaction records demo metadata only. Confirm requirements and deadlines with the competent authority.

## Run locally

No build step or package installation is required. Serve this folder over HTTP:

```sh
python3 -m http.server 4183
```

Open <http://localhost:4183>. The app is a static HTML/CSS/ES-module prototype; state persists in browser `localStorage`.

## Demonstration paths

- **Applicant · Mukesh Chemicals Pvt. Ltd.** Open **Know Your Approvals**, submit a chemical-manufacturing profile, explore its 17 illustrative approval nodes and start a local application draft.
- **Applicant · Rahul Foods** In the KYA flow select **Food Processing** and **Green** to build the small-business demonstration roadmap.
- **Department officer** Use the profile menu to switch workspaces and inspect the sample queue, applicant case, smart queue, analytics, SLA and transparency views.
- **Agent Mode** Opens contextual sample guidance; it does not invoke a language model or submit data.

## Phase plan

| Phase | Scope | Status |
|---|---|---|
| 1 · Applicant foundation | Government-service visual system, responsive shell, role workspaces, demo navigation and local state | Implemented |
| 2 · Approval discovery | Multi-step KYA, project profile and dependency roadmap with readiness, blockers, parallel paths and export | Implemented |
| 3 · Application preparation | Local application wizard, reusable document metadata, simulated validation, verified-data, scheme and renewal views | Implemented |
| 4 · Department operations | Review queue, applicant case, priority proposal, inspection proposal, SLA, risk, analytics and transparency | Implemented |
| 5 · Trust and governance | Human review, knowledge catalogue, notification events, reverse-integration mock and demo disclosures | Implemented |
| 6 · Production integration | Identity, permissioned data exchange, authoritative approval catalogue, department adapters, secure document storage, OCR, audit and monitoring | Not implemented; requires approved agency systems, data agreements, security design and hosting |

See [`docs/PHASES.md`](docs/PHASES.md), [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) and [`docs/DEMO-DATA.md`](docs/DEMO-DATA.md).

## Technology

- Semantic HTML5 and responsive CSS
- Native JavaScript ES modules (no runtime dependency)
- Client-side route rendering and localStorage persistence
- Static hosting compatible with Vercel, GitHub Pages or any HTTP server

## Deploy to Vercel

Import this repository in Vercel, use **Other** / static output with the repository root as the project root, and leave build and output commands empty. No secrets or environment variables are required for the prototype. Hash-based client navigation works on static hosting.

## Sources and boundaries

The discovery concept is inspired by the National Single Window System's public-facing approval discovery workflow. This prototype is an independent demonstration and is not affiliated with NSWS or any government department. The application does not scrape or claim to reproduce an authoritative approval catalogue. All presented rules and data require verification before real use.
