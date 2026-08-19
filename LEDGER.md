# Public Publication Ledger

This append-only ledger records material made publicly available through AI Cutting Edge. A new row is committed atomically with its corresponding public file and counts as valid only after unauthenticated read-back verifies both the file and the ledger link.

| Date | Type | Entry | Status | Sources |
|---|---|---|---|---:|
| 2026-08-17 | AI News Brief | [Approved format sample](news/2026/08/2026-08-17-approved-sample.md) | Approved sample | 3 |
| 2026-08-17 | Creator Round-up | [Approved format sample](creators/2026/08/2026-08-17-approved-sample.md) | Approved sample | 1 |
| 2026-08-17 | GitHub Radar | [Approved format sample](github/2026/08/2026-08-17-approved-sample.md) | Approved sample | 3 |
| 2026-08-17 | Creator guide | [CLI-first agent tooling](creators/guides/cli-first-agent-tools.md) | Approved example | 2 |
| 2026-08-17 | Repository guide | [oMLX — local AI inference on Apple Silicon](github/guides/jundot-omlx.md) | Approved example | 3 |
| 2026-08-17 | Editorial policy | [Five-item normal-edition floor](PUBLISHING.md#edition-size) | Active policy | — |
| 2026-08-17 | Public library | [Practical Library](library/) | Active index | 2 |
| 2026-08-17 | Editorial policy | [Library routing and briefing footer](PUBLISHING.md#briefing-footer) | Active policy | — |

## Status vocabulary

- **Approved sample** — accepted format example; not represented as a live recurring Telegram edition.
- **Published** — exact copy of a successfully delivered Telegram briefing.
- **Updated guide** — reviewed durable knowledge updated after a material development.
- **Correction** — a transparent amendment that leaves the original ledger history intact.
- **Active policy** — a current public operating rule that governs future editions.
- **Active index** — a public browse surface linking verified durable artifacts without duplicating their bodies.

## Ledger law

- Never remove history to hide a correction; append a correction row.
- Never commit a live-edition row before successful Telegram delivery. After the atomic file-and-row push, archival remains incomplete until the public file matches the exact delivered Markdown and the public ledger link resolves.
- Never expose private source-system identifiers.
- The file link, date, briefing type, status, and source count are required.
