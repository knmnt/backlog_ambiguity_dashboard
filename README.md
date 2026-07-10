# backlog_ambiguity_dashboard

Dedicated publication repository for the public-safe static Pecodex dashboard.

## Repository boundary

- Repository: `knmnt/backlog_ambiguity_dashboard`
- Default branch: `main`
- Initial visibility: private
- Planned Pages source: `main:/docs`
- `docs/` intentionally remains absent until the validated, sample-derived
  final dashboard HTML and assets are ready.

When publication is authorized, the Pages source may contain only
`docs/index.html` and public-safe files under `docs/assets/`. Contracts,
reports, status YAML, local inputs, logs, and private material remain outside
the Pages source or outside Git entirely.

## Input and output

The renderer input is a validated local, non-git status snapshot from
`knmnt/backlog_ambiguity_sample_repo`. The only publishable output is final
static HTML and public-safe assets. Raw status YAML is never copied or embedded
in the published surface.

See:

- `contracts/dashboard_publication_boundary.md`
- `contracts/input_output_contract.md`
- `reports/b_to_c_dashboard_repo_bootstrap_report.md`

The dashboard is a non-authority projection. Source repository records remain
authoritative, and this repository provides no mutation controls.
