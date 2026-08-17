# Publishing Contract

This repository is the durable public layer behind the Telegram briefings. Telegram delivery and GitHub archival are related but separately replayable operations.

## Successful-edition sequence

1. Collect candidates deterministically.
2. Apply the relevant briefing skill and public-safety gate.
3. Deliver the final Markdown to the intended Telegram group.
4. Verify scheduler success, empty delivery error, and the exact rendered output.
5. Write that exact output—without regeneration—to the matching dated archive path.
6. Append one row to [`LEDGER.md`](LEDGER.md).
7. Commit and push the archive file and ledger together.
8. Fetch the public file URL and require a successful response.
9. Mark the archive operation complete.

## Paths

```text
news/YYYY/MM/YYYY-MM-DD.md
creators/YYYY/MM/YYYY-MM-DD.md
creators/guides/<method-slug>.md
github/YYYY/MM/YYYY-MM-DD.md
github/guides/<owner>-<repo>.md
```

If more than one edition of the same briefing is deliberately published on one date, add a short edition suffix rather than overwriting history.

## Failure behavior

| Failure | Required response |
|---|---|
| Telegram delivery fails | Preserve the source checkpoint and exact output; fix routing and replay Telegram. Do not archive it as published. |
| Telegram succeeds but GitHub archival fails | Advance delivered-item state, retain the exact output, alert privately, and retry GitHub only. Do not repost Telegram. |
| Public URL verification fails | Treat archival as incomplete and retry the same commit/push path. |
| Correction needed | Add a visible correction note and append a ledger row; do not silently rewrite history. |
| No material Creator output | Stay silent; create no empty archive file or ledger row. |

## Durable-guide threshold

A daily card does not automatically become a guide. A creator method must remain reusable and evidence-aware. A repository must be credible, distinct, materially useful, and likely to matter beyond its trend window.

## Public boundary

Only reviewed public-safe Markdown enters this repository. A future chatbot may index this repository, but it must not access the private research or ingestion systems behind it.
