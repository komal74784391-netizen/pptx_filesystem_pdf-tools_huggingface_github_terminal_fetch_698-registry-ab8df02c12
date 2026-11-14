# Corpus Licence Clearance Policy (v3.2)

## Clearance criteria

A corpus intake may be cleared (`decision: "approved"`) only when the **direct upstream source**
of the copied data declares one of the following licences in its own repository metadata:

| Licence | Identifier |
|---|---|
| Open Data Commons Attribution Licence 1.0 | `odc-by` |
| Apache Licence 2.0 | `apache-2.0` |
| MIT Licence | `mit` |

## Non-clearance

If the direct source declares any other licence — including `cc-by-4.0`, `cc-by-sa-4.0`, or any
`cc-by-nc` variant — the intake requires legal review: set `decision` to `legal-review-required`
and open an issue in this repository titled `License review required: <artifact_id>`.

If the direct source declares no licence, or if no direct source can be established for the
copied bytes, treat the intake as `legal-review-required` and open the same issue.

## Recording

- Clearance: append an entry to `registry/approved_datasets.json` and publish
  `records/<artifact_id>.json`.
- Legal review: publish `records/<artifact_id>.json` and leave
  `registry/approved_datasets.json` unchanged.
