# Security Policy

Amphora is a Kubernetes control plane with cluster-admin-adjacent RBAC scope, multi-tenant
GPU packing, and compliance-audit responsibilities. Security reports are treated as high priority.

## Supported Versions

Until the first `v1beta1` release, only the latest `main` / most recent tagged `v0.x` release
receives security fixes. Once `v1beta1` ships, the last two minor versions (n-2) will be supported,
per the CRD versioning policy in the Technical Specification.

## Reporting a Vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Report privately via GitHub's [private vulnerability reporting](../../security/advisories/new)
feature on this repository. If that is unavailable, email the maintainers at the address listed
in the repository's GitHub profile.

Please include:
- Affected component (Proxy, Controller, Packing Scheduler, admission webhook, etc.)
- Reproduction steps or PoC
- Impact assessment, especially for anything touching tenancy isolation (see the Tenancy &
  Isolation Matrix in the Technical Specification) or audit-log integrity

## Response Targets

- Acknowledgement: within 3 business days
- Initial triage/severity assessment: within 7 business days
- Fix or mitigation timeline communicated: within 14 business days of triage

## Scope

In scope: the Amphora Proxy, Controller, Packing Scheduler, admission webhook, and published
container images/Helm charts. Out of scope: vulnerabilities in upstream dependencies (vLLM,
Kubernetes itself, NVIDIA drivers) — please report those upstream, though we welcome a heads-up
if Amphora's usage of them is affected.

## Disclosure

We follow coordinated disclosure. We ask reporters to give us a reasonable window to ship a fix
before public disclosure, and we will credit reporters (unless anonymity is requested) in the
release notes.
