# Validation results

Validation date: 2026-10-10

## Format validation — passed

Ran the skill-creator `quick_validate.py` against the installed skill and the public package. Both exited 0 with `Skill is valid!`. The prior missing-PyYAML blocker was resolved in an isolated task-local Python virtual environment with PyYAML 6.0.3; no global Python packages were changed.

This checks frontmatter, name, allowed fields and unfinished scaffold markers. It does not verify live website behavior.

## Independent synthetic exercise — passed within the stated scope

A separate evaluator read the skill and received fictional facts only. Network, browser, application submission and online writes were prohibited. Its output is included in `examples/output.md`; the lead reviewer inspected it against the input.

| Scenario | Observed result |
|---|---|
| A approved; B preparation only | D-101 permission was not extended to G-202 |
| Old portfolio plus new résumé | p1 remained a separate unresolved decision |
| Network error after submit; application center reports received | No duplicate submission; received status preserved |
| Tracking write failed | Marked unsynced; submission status not erased |
| Missing actual files and exact time | No invented hash, submitted version or timestamp |
| Handoff vs publication | Local artifact explicitly distinguished from delivery/publication |

One combined scenario was exercised. This is behavioral evidence for the synthetic inputs, not exhaustive reliability or a live recruiting-site/Google Sheets integration test. No outcome metrics were measured.

## Scope review

Material assessment and rewriting are routed to application-helper when available; the handoff skill retains only version reconciliation and unresolved facts needed at the handoff boundary. Three SKILL.md copies are byte-identical: installed source, private snapshot and publication package.

## Public package review

The package was manually reviewed and scanned for local personal paths, contact information, Google Sheet URLs/IDs, private receipt details, and real application company names. It contains synthetic examples only. The scan is a release hygiene check, not a guarantee against all possible sensitive content.

## Release state

The user authorized publishing this sanitized package to VibeCoding_practice. Release commit and remote verification are recorded in the portfolio maintenance record outside this package.

## Designated tracker update validation

The workflow now covers role selection and official-JD fit assessment through authorized submission, receipt verification, designated tracker readback and local archival. Detailed résumé preparation remains with application-helper when available.

Re-ran quick_validate.py on the installed and public skills: both passed. Reviewed the new private configuration reference and verified installed, private snapshot and public copies of SKILL.md, agents/openai.yaml and references/tracker-config.md are identical. Public text was scanned for local personal paths, Google Sheet URLs and long identifier patterns with no matches.

A separate offline evaluator exercises stale configuration, wrong gid, title/header mismatch, duplicate keys, write timeout with successful readback, mismatched readback, inaccessible main sheet and unverified official JD. The recorded outputs are in examples/tracker-failure-cases.md. No live application or Google Sheet operation is part of this validation.

All eight recorded scenario decisions were reviewed and matched the stated constraints. This is synthetic behavioral validation, not a live integration test.
