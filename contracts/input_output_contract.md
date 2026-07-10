# Dashboard Input/Output Contract

Status: repository-local PDX-DASH-28 input/output boundary; non-authority.

## Input

The only operational input for the initial dashboard is one validated status
snapshot generated from `knmnt/backlog_ambiguity_sample_repo` and retained in
an operator-owned local, non-git inbox or workdir.

The snapshot must retain the v1 core structure and may carry the additive
public projection fields `repo_id`, `generated_at`, `source_refs`,
`authority_boundary`, `validation_summary`, and `redaction_summary`. It must
pass fail-closed validation and contain no raw private or secret material.

Input is never obtained through a committed cross-repository downloader,
artifact lookup automation, workflow, schedule, on-merge hook, token, secret,
or credential.

## Processing boundary

Rendering is local and read-only with respect to source repositories. The
renderer may project only public-safe summaries, including repository identity,
lifecycle/status summary, generation time, validation summary, visibility or
freshness markers, high-level next-gate category, and sanitized source refs.

Raw YAML, raw logs, raw validation output, diffs, private paths, transcripts,
and chain-of-thought must not be copied or embedded.

## Output

The only Git-managed publication output is:

- final `docs/index.html`;
- required public-safe files under `docs/assets/**`.

Root metadata, contracts, and durable reports stay outside `docs/`. Local
inputs, work products, snapshots, and transient drivers remain untracked.

## Validation and stop boundary

Output must pass HTML structure, allowed-path inventory, raw-snapshot,
private-path, credential, and unsafe-content checks before merge. Rendering or
publication stops if it requires committed input data, committed generation
drivers, automation, credentials, raw/private content, or authority claims.
