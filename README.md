# KugCatch endpoint monitoring

This public repository checks only the review and portal `/healthz` endpoints.
It contains no customer data or service credentials. GitHub-hosted runners use
this repository's `GITHUB_TOKEN` to commit history and manage outage issues.
The public status page is https://javiergbravo.github.io/kugcatch-status/.
Issue comments are never used as published customer updates.

## Activation

Actions are disabled until both production hosts serve their approved endpoints.
After the deployment is accepted, enable Actions and run **Uptime CI** manually;
verify history commits, outage/recovery issues and the independent status page.
The monitor uses pinned upstream actions and has no template self-update job,
site workflow, Pages site, personal token, or email notification integration.
Updates to the pinned actions must pass a pull request.

## Safety

Missing, stale or failed monitoring means availability is unknown. Endpoint
liveness does not prove completed reviews, worker health or successful billing.
The six-step operational drill belongs to the service's support runbook and must
finish before relying on this monitor for the beta. No live readiness is claimed.

Upptime implementation: https://github.com/upptime/uptime-monitor/tree/v1.46.0
