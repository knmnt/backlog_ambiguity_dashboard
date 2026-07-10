# PDX-DASH-29 Pre-Private Exposure Inventory

Status: S02 public-exposure inventory recorded before Pages disablement or
repository visibility change.

This report is support input only. It does not decide acceptance, closure,
priority, dispatch, merge readiness, product authority, publication state,
visibility, cleanup, or WorkItem outcome.

## Scope

WorkItems:

- `PDX-DASH-29-PUBLICATION-SURFACE-SPLIT-PRIVATE-CONTROL-LONGRUN`
- `PDX-DASH-29-S02`

The inventory classifies paths, counts, and exposure judgments without copying
raw file content, validation output, private material, or repository history.
It describes the base state before this report is added.

## Base And Repository State

- inventory base: `9004e1d`;
- repository visibility: `PUBLIC`;
- default branch: `main`;
- open pull requests: `0`;
- reachable commits: `9`;
- Pages build state: built;
- Pages source: `main:/docs`;
- HTTPS: enabled;
- legacy Pages URL: `https://knmnt.github.io/backlog_ambiguity_dashboard/`.

## Current Tree And Reachable-History Inventory

The base has eight current tracked paths. The same eight unique path names are
present across reachable history; this count excludes the report added by the
current S02 branch.

| Category | Count | Exact paths | Judgment |
| --- | ---: | --- | --- |
| Root metadata | 2 | `.gitignore`; `README.md` | Publicly browseable repository metadata. |
| Contracts | 2 | `contracts/dashboard_publication_boundary.md`; `contracts/input_output_contract.md` | Present in the public current tree and reachable public history. |
| Pages content | 2 | `docs/index.html`; `docs/assets/dashboard.css` | Intended Pages-served HTML/CSS surface. |
| Reports | 2 | `reports/b_to_c_dashboard_repo_bootstrap_report.md`; `reports/b_to_c_dashboard_publication_report.md` | Present in the public current tree and reachable public history. |
| Total | 8 | Eight unique base paths | Current tree and reachable-history path inventory complete. |

Reports and contracts are confined from the Pages route, but remain browseable
through the public GitHub repository and its reachable history. Deleting them
from a later tree would not erase their historical presence. This report makes
no claim that third parties did not copy or cache previously public material,
and no later visibility change can establish third-party erasure.

## Classified Content Scan

The base tree and reachable history were classified without reproducing match
text.

| Category | Count | Judgment |
| --- | ---: | --- |
| YAML or YML paths | 0 | None tracked in the base tree or reachable path history. |
| Workflow paths | 0 | No GitHub Actions workflow path found. |
| `inbox/` or `work/` paths | 0 | No local ingestion or work path tracked. |
| Status snapshots | 0 | No raw or generated status snapshot path found. |
| Absolute local paths | 0 | No absolute local path occurrence classified. |
| Credential assignments | 0 | No credential, token, or secret assignment classified. |
| Private-key markers | 0 | No private-key payload marker classified. |

Policy and prohibition terms that appear in contracts, reports, or metadata are
policy references, not credential, secret, private-key, raw-status, or private
operational payloads. Their presence does not change the zero-count payload
judgments above.

## Pages Boundary Check

| Route class | Result | Judgment |
| --- | ---: | --- |
| Pages root | HTTP 200 | Legacy dashboard page is publicly served. |
| Pages CSS asset | HTTP 200 | Local dashboard stylesheet is publicly served. |
| `reports` route | HTTP 404 | Reports are not served through Pages. |
| `contracts` route | HTTP 404 | Contracts are not served through Pages. |
| `status` route | HTTP 404 | Status data is not served through Pages. |
| `inbox` route | HTTP 404 | Inbox content is not served through Pages. |
| `work` route | HTTP 404 | Work content is not served through Pages. |

Pages confinement therefore passes for the tested routes, but it does not make
the repository or Git history private. The public-repository exposure remains
the reason for the PDX-DASH-29 split architecture.

## Verification

- repository identity, branch, visibility, default branch, and open-PR state
  were checked before drafting;
- `git ls-files` classified the eight base tracked paths;
- reachable commit count was checked as nine;
- current and reachable-history path categories were compared;
- category-only scans found zero YAML, workflow, inbox/work, snapshot,
  absolute-local-path, credential-assignment, and private-key-marker findings;
- Pages root and CSS returned HTTP 200;
- tested reports, contracts, status, inbox, and work routes returned HTTP 404;
- raw matching text and raw validation output are intentionally excluded.

## Assumptions, Risks, And Deviations

- The inventory is anchored to base `9004e1d`; this S02 report becomes an
  additional tracked report path only after the current PR is merged.
- GitHub and Pages observations are point-in-time state and may later change.
- Public history may already have been copied or cached outside GitHub; erasure
  of third-party copies is neither assumed nor claimed.
- Reports and contracts are not Pages-served, but public repository browsing is
  a separate exposure surface.
- No deviation from the S02 category/count/judgment-only boundary occurred.

## Explicit Non-Actions

- No Pages source, build, HTTPS, or custom-domain setting changed.
- No repository visibility or default-branch setting changed.
- No existing tracked file was edited or deleted.
- No history rewrite, force push, broad cleanup, or archive movement occurred.
- No raw report, contract, log, validation output, status snapshot, credential,
  secret, private key, private path, transcript, or chain-of-thought was copied.
- No new public Pages repository was created.
- No workflow, schedule, on-merge automation, enforcement, branch protection,
  real-repository expansion, or completion declaration was introduced.

## Stop And Next Gate

S02 stops with the current public exposure durably classified. The next
dependency gate is S02 review, PR merge, post-merge branch synchronization, and
backlog reread before `PDX-DASH-29-S03` may create the clean-history public
HTML-only Pages repository. This statement is dependency eligibility only, not
priority, dispatch, acceptance, closure, or merge authority.
