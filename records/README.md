# Provenance records

Publish one JSON record per intake as `records/<artifact_id>.json`.

Required fields:

- `artifact_id` — intake identifier
- `source_deck` — deck the technical content was taken from
- `direct_source` — upstream repository that actually supplied the copied bytes
- `license` — licence declared by that direct source
- `decision` — `approved` or `legal-review-required`
- `evidence` — object with `matched_shards` (array of staged shard file names that were matched)
  and `citation_anchor`
- `summary` — one or two sentences

See `records/corpus-intake-2051.json` for a completed example.
