# Publishing Contract

This repository is the durable public layer behind the Telegram briefings. Telegram delivery and GitHub archival are related but separately replayable operations.

## Edition size

- A normal AI News, Creator, GitHub, or Marketing Edge edition contains five to seven qualifying items.
- If three or four qualify, publish a daily short edition and display exactly `**Short edition — <reason>**` below its date.
- If zero to two qualify, hold them over and publish nothing.
- Never use filler or lower the evidence bar for either a normal or short edition.
- Historical approved AI samples in this repository predate this daily normal/short-edition rule and demonstrate card format only.

## Briefing footer

Every delivered briefing ends with:

```markdown
[Archive & practical resources ↗](https://github.com/agentarmy72-del/ai-cutting-edge)
```

This wording is deliberate. It links readers to the public archive and Library without claiming that the current post has already been archived; exact archival happens only after Telegram delivery is verified.

## Successful-edition sequence

1. Collect candidates deterministically.
2. Apply the relevant briefing skill and public-safety gate.
3. Append the exact GitHub footer as the final line.
4. Deliver the final Markdown to the intended Telegram destination.
5. Verify scheduler success, empty delivery error, and the exact rendered output.
6. Write that exact output—without regeneration—to the matching dated archive path.
7. Append one row to [`LEDGER.md`](LEDGER.md).
8. Commit and push the archive file and ledger together as one atomic publication unit.
9. Fetch the public archive URL without authentication and require a byte-for-byte match to the exact delivered Markdown.
10. Fetch the public ledger, require the new row to be present, and require its archive link to resolve.
11. Mark the archive operation complete only after both read-back checks pass.

## Paths

```text
news/YYYY/MM/YYYY-MM-DD.md
creators/YYYY/MM/YYYY-MM-DD.md
creators/guides/<method-slug>.md
github/YYYY/MM/YYYY-MM-DD.md
github/guides/<owner>-<repo>.md
marketing/YYYY/MM/YYYY-MM-DD.md
marketing/guides/<slug>.md
library/guides/<slug>.md
library/skills/<skill-name>/SKILL.md
```

If more than one edition of the same briefing is deliberately published on one date, add a short edition suffix rather than overwriting history.

## Value routing

Apply this only after the exact edition archive succeeds:

| Material | Route |
|---|---|
| Time-bound, thin, or duplicative | Dated briefing archive only. |
| Reusable for a person, but not agent-executable | One canonical Markdown guide, indexed from [`library/README.md`](library/README.md). |
| Repeatable agent procedure with clear triggers, complete steps, failure behavior, provenance, and a real test | `library/skills/<skill-name>/SKILL.md`, indexed from the Library. |
| Promotional, private, unsupported, or unsafe | Do not promote it. |

Creator guides remain canonical under `creators/guides/`; AI repository guides remain canonical under `github/guides/`; Marketing Edge guides remain canonical under `marketing/guides/`; continuing News and cross-product guides may live under `library/guides/`. Do not copy a guide body merely to centralize discovery.

Add the artifact, Library index update, and separate ledger row in one commit, then verify every public URL. The row becomes valid only after those read-back checks pass. An optional artifact failure never rolls back or reposts an already archived briefing.

## Failure behavior

| Failure | Required response |
|---|---|
| Telegram delivery fails | Preserve the source checkpoint and exact output; fix routing and replay Telegram. Do not archive it as published. |
| Telegram succeeds but GitHub archival fails | Advance delivered-item state, retain the exact output, alert privately, and retry GitHub only. Do not repost Telegram. |
| Archive or ledger read-back verification fails | Treat archival as incomplete and retry the same immutable commit/push/read-back path. |
| Correction needed | Add a visible correction note and append a ledger row; do not silently rewrite history. |
| Zero to two material items for any product | Stay silent and roll qualified items forward; create no empty archive file or ledger row. Three or four publish as a labelled short edition. |
| Optional guide/skill promotion fails | Keep the verified briefing archive intact; retry only the artifact, Library index, and ledger commit. |

## Durable-guide threshold

A daily card does not automatically become a guide. A creator method must remain reusable and evidence-aware. A repository must be credible, distinct, materially useful, and likely to matter beyond its trend window. A public skill must also be executable and testable; a creator's label or popularity is not sufficient.

## Publishing credential

Recurring archive writes use a fine-grained GitHub token restricted to `agentarmy72-del/ai-cutting-edge` with repository **Contents: read and write** and the automatic **Metadata: read** permission. Store it only as the Hermes `GITHUB_TOKEN` secret; never commit it, print it, embed it in the remote URL, or retain a broader all-public-repositories OAuth token for routine publishing.

If the credential is missing, expired, or rejected, preserve the exact delivered output and retry the GitHub archive only after private remediation. Never repost Telegram.

## Public boundary

Only reviewed public-safe Markdown enters this repository. Personal data/PII, confidential personal information, client/account data, private research, credentials, receipts, internal identifiers, and local paths are prohibited. A future chatbot may index this repository, but it must not access the private research or ingestion systems behind it.
