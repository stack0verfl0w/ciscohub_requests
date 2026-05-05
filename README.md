# CiscoHub — public API request intake

This folder is a **bootstrap** for a **separate, public** GitHub repository used only for **API coverage requests** (issues). The main CiscoHub documentation repository can stay **private**.

## Create the public repo

1. On GitHub, create a new **public** repository (suggested name: `ciscohub-requests`).
2. Copy **everything under `intake-public/`** (including `.github`) into the root of that new repository and push.
3. In your **private** docs repo, set the same slug in two places (keep them in sync):
   - `mkdocs.yml` → `extra.public_issues_repo`
   - `scripts/data/cisco_pillars.yaml` → `intake_repository`

## Labels

GitHub will attach labels from the issue template when users submit. Ensure these exist (they are usually created automatically on first use):

- `api-request`
- `needs-triage`
- `accepted` (for maintainers after triage)

## Sync when templates change

When you edit `intake-public/.github/ISSUE_TEMPLATE/api_coverage_request.yml`, copy the updated files to the public intake repo and push. The dropdown options must stay aligned with `scripts/data/cisco_pillars.yaml` in the private repo.

## Actions

The included workflow posts a short welcome comment on new `api-request` issues. Enable **Actions** on the public repo if prompted.
