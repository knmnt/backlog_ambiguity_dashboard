# Dashboard Publication Boundary

Status: repository-local publication boundary for PDX-DASH-28; non-authority
projection contract.

## Purpose

This contract confines GitHub Pages publication for
`knmnt/backlog_ambiguity_dashboard` to final, public-safe static dashboard
output. The intended Pages source is `main:/docs`, but Pages is not configured
by PDX-DASH-28-S03.

## Allowed Pages content

Only these paths may exist under `docs/`:

- `docs/index.html`
- public-safe assets under `docs/assets/**`

`docs/` must remain absent until the validated sample-derived final output is
ready for its reviewed publication PR.

## Forbidden Pages content

The following must never be placed under `docs/`:

- reports or contracts;
- raw or generated status YAML;
- inbox, workdir, local snapshots, or transient driver material;
- raw logs, validation output, diffs, or child/evaluator context;
- private local paths, private payloads, secrets, tokens, or credentials;
- accepted-resolution records, active ambiguity cases, or authority patches;
- chain-of-thought or completion declarations.

## Publication gates

Before Pages source configuration or publication:

1. The final sample-derived HTML/assets PR is merged to `main`.
2. The `docs/` inventory contains only the allowed paths.
3. Public-boundary and unsafe-content checks pass.
4. No raw snapshot or local input is tracked anywhere in this repository.
5. Any visibility change required by Pages is necessary, safe, and recorded.

If any gate cannot be confirmed, publication stops and the durable report
records the safe pending state. No workflow, credential, or broader repository
setting may be introduced to bypass a stop.

## Authority boundary

Published HTML is display-only support output. It does not decide acceptance,
closure, priority, next work, dispatch, merge readiness, completion, or product
authority, and it must not mutate a source repository.
