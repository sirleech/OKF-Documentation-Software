# OKF Documentation for Software

Use the OKF Spec to setup the OKF documentation
https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md

This repository contains structured project documentation organized by domain. Each top-level folder covers a distinct area of the software lifecycle.

If you are setting this up, and a section doesn't apply, don't include it at all (ie leave it out of the folder structure)

## CLAUDE.md
`the following goes into the MD with the @ imports`

### Always-loaded context

The full documentation lives in /docs and is read on demand, but two files are auto-imported into every session so the contributor rules and the map of design-decision regression guards are always in context. Before changing any non-trivial subsystem read its ADR from the decisions index below — those files carry "don't reintroduce X" warnings for bugs that were already fixed once.

@docs/03-development/coding-guidelines.md @docs/02-architecture/decisions/README.md


## Structure

Every folder contains a `README.md` so GitHub renders it as the default landing
page for that folder.

```
CLAUDE.md
docs/
├── README.md
├── 00-overview/
│   ├── README.md
│   ├── vision.md
│   ├── architecture-summary.md
│   └── glossary.md
│
├── 01-product/
│   ├── README.md
│   ├── requirements/
│   │   ├── README.md
│   │   ├── functional-requirements.md
│   │   ├── non-functional-requirements.md
│   │   └── user-stories.md
│   ├── design/
│   │   ├── README.md
│   │   ├── ux-ui/
│   │   │   └── README.md
│   │   ├── wireframes/
│   │   │   └── README.md
│   │   └── design-decisions.md
│   └── roadmap/
│       ├── README.md
│       └── roadmap.md
│
├── 02-architecture/
│   ├── README.md
│   ├── system-overview.md
│   ├── diagrams/
│   │   ├── README.md
│   │   ├── context-diagram.png
│   │   ├── container-diagram.png
│   │   └── sequence-diagrams/
│   │       └── README.md
│   ├── components/
│   │   ├── README.md
│   │   ├── frontend.md
│   │   ├── backend.md
│   │   ├── database.md
│   │   └── integrations.md
│   └── decisions/
│       ├── README.md
│       ├── ADR-001.md
│       └── ADR-002.md
│
├── 03-development/
│   ├── README.md
│   ├── setup/
│   │   ├── README.md
│   │   ├── local-setup.md
│   │   ├── environment-variables.md
│   │   └── dependencies.md
│   ├── coding-guidelines.md
│   ├── branching-strategy.md
│   ├── code-structure.md
│   └── contribution-guide.md
│
├── 04-api/
│   ├── README.md
│   ├── overview.md
│   ├── authentication.md
│   ├── endpoints/
│   │   ├── README.md
│   │   ├── users.md
│   │   ├── auth.md
│   │   └── products.md
│   └── openapi.yaml
│
├── 05-testing/
│   ├── README.md
│   ├── testing-strategy.md
│   ├── unit-tests.md
│   ├── integration-tests.md
│   ├── e2e-tests.md
│   └── test-data.md
│
├── 06-deployment/
│   ├── README.md
│   ├── deployment-overview.md
│   ├── ci-cd.md
│   ├── environments.md
│   ├── infrastructure.md
│   └── rollback.md
│
├── 07-operations/
│   ├── README.md
│   ├── monitoring.md
│   ├── logging.md
│   ├── alerts.md
│   ├── incident-response.md
│   └── maintenance.md
│
├── 08-security/
│   ├── README.md
│   ├── security-overview.md
│   ├── auth-authz.md
│   ├── data-protection.md
│   ├── threat-model.md
│   └── compliance.md
│
├── 09-user-docs/
│   ├── README.md
│   └── usermanual.md
│
└── 10-release-notes/
    ├── README.md
    └── changelog.md
```

## Sections

| Folder | Purpose |
|---|---|
| `00-overview` | Project vision, high-level architecture, and shared glossary |
| `01-product` | Requirements, design assets, and roadmap |
| `02-architecture` | System design, component docs, and Architecture Decision Records (ADRs) |
| `03-development` | Local setup, coding guidelines, branching, and contribution guide |
| `04-api` | API overview, authentication, endpoint references, and OpenAPI spec |
| `05-testing` | Testing strategy and docs for unit, integration, and end-to-end tests |
| `06-deployment` | CI/CD pipelines, environment configs, infrastructure, and rollback procedures |
| `07-operations` | Monitoring, logging, alerting, incident response, and maintenance |
| `08-security` | Security overview, auth/authz, data protection, threat model, and compliance |
| `09-user-docs` | End-user guides, tutorials, FAQ, and troubleshooting |
| `10-release-notes` | Per-version release notes and running changelog |
