# Public Publication Ledger

This append-only ledger records material made publicly available through AI Cutting Edge. A new row is committed atomically with its corresponding public file and counts as valid only after unauthenticated read-back verifies both the file and the ledger link.

| Date | Type | Entry | Status | Sources |
|---|---|---|---|---:|
| 2026-08-17 | AI News Brief | [Approved format sample](examples/ai-news-2026-08-17-approved-sample.md) | Approved sample | 3 |
| 2026-08-17 | Creator Round-up | [Approved format sample](examples/creator-round-up-2026-08-17-approved-sample.md) | Approved sample | 1 |
| 2026-08-17 | GitHub Radar | [Approved format sample](examples/github-radar-2026-08-17-approved-sample.md) | Approved sample | 3 |
| 2026-08-17 | Creator guide | [CLI-first agent tooling](creators/guides/cli-first-agent-tools.md) | Approved example | 2 |
| 2026-08-17 | Repository guide | [oMLX — local AI inference on Apple Silicon](github/guides/jundot-omlx.md) | Approved example | 3 |
| 2026-08-17 | Editorial policy | [Five-item normal-edition floor](PUBLISHING.md#edition-size) | Active policy | — |
| 2026-08-17 | Public library | [Practical Library](library/) | Active index | 2 |
| 2026-08-17 | Editorial policy | [Library routing and briefing footer](PUBLISHING.md#briefing-footer) | Active policy | — |
| 2026-08-18 | GitHub Radar | [Daily edition](github/2026/08/2026-08-18.md) | Published | 7 |
| 2026-08-19 | Marketing Edge Brief | [Daily edition](marketing/2026/08/2026-08-19.md) | Published | 40 checks |
| 2026-08-19 | AI News Brief | [Daily edition](news/2026/08/2026-08-19.md) | Published | 7 |
| 2026-08-19 | Archive maintenance | [Historical format examples](examples/) | Path migration | 3 |
| 2026-08-19 | Marketing Edge Brief | [Exact-byte terminal-newline correction](marketing/2026/08/2026-08-19.md) | Correction | — |
| 2026-08-19 | AI News Brief | [Exact-byte terminal-newline correction](news/2026/08/2026-08-19.md) | Correction | — |
| 2026-08-19 | GitHub Radar | [Daily edition](github/2026/08/2026-08-19.md) | Published | 5 |
| 2026-08-20 | Marketing Edge Brief | [Daily edition](marketing/2026/08/2026-08-20.md) | Published | 41 checks |
| 2026-08-20 | AI News Brief | [Daily edition](news/2026/08/2026-08-20.md) | Published | 6 |
| 2026-08-20 | GitHub Radar | [Daily edition](github/2026/08/2026-08-20.md) | Published | 6 |
| 2026-08-21 | Marketing Edge Brief | [Daily edition](marketing/2026/08/2026-08-21.md) | Published | 36 checks |
| 2026-08-21 | AI News Brief | [Daily edition](news/2026/08/2026-08-21.md) | Published | 6 |
| 2026-08-21 | GitHub Radar | [Daily edition](github/2026/08/2026-08-21.md) | Published | 4 |
| 2026-08-22 | Marketing Edge Brief | [Daily edition](marketing/2026/08/2026-08-22.md) | Published | 58 checks |
| 2026-08-22 | AI News Brief | [Daily edition](news/2026/08/2026-08-22.md) | Published | 7 |
| 2026-08-22 | GitHub Radar | [Daily edition](github/2026/08/2026-08-22.md) | Published | 6 |
| 2026-08-23 | Marketing Edge Brief | [Daily edition](marketing/2026/08/2026-08-23.md) | Published | 56 checks |
| 2026-08-23 | AI News Brief | [Daily edition](news/2026/08/2026-08-23.md) | Published | 7 |
| 2026-08-23 | GitHub Radar | [Daily edition](github/2026/08/2026-08-23.md) | Published | 5 |
| 2026-08-24 | Marketing Edge Brief | [Daily edition](marketing/2026/08/2026-08-24.md) | Published | 42 checks |
| 2026-08-24 | AI News Brief | [Daily edition](news/2026/08/2026-08-24.md) | Published | 5 |
| 2026-08-24 | GitHub Radar | [Daily edition](github/2026/08/2026-08-24.md) | Published | 5 |
| 2026-08-25 | Marketing Edge Brief | [Daily edition](marketing/2026/08/2026-08-25.md) | Published | 209 checks |
| 2026-08-25 | AI News Brief | [Daily edition](news/2026/08/2026-08-25.md) | Published | 6 |
| 2026-08-25 | GitHub Radar | [Daily edition](github/2026/08/2026-08-25.md) | Published | 7 |

## Status vocabulary

- **Approved sample** — accepted format example; not represented as a live recurring Telegram edition.
- **Published** — exact copy of a successfully delivered Telegram briefing.
- **Updated guide** — reviewed durable knowledge updated after a material development.
- **Correction** — a transparent amendment that leaves the original ledger history intact.
- **Active policy** — a current public operating rule that governs future editions.
- **Active index** — a public browse surface linking verified durable artifacts without duplicating their bodies.
- **Path migration** — a transparent public-location change that leaves the archived body and its Git history intact.

## Ledger law

- Never remove history to hide a correction; append a correction row.
- Never commit a live-edition row before successful Telegram delivery. After the atomic file-and-row push, archival remains incomplete until the public file matches the exact delivered Markdown and the public ledger link resolves.
- Never expose private source-system identifiers.
- The file link, date, briefing type, status, and source count are required.
- When an unchanged artifact moves to a clearer public location, update its link and append a path-migration row rather than hiding the move.
