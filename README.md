# platoism

I build small, fast tools: Go and Rust CLIs, Cloudflare Workers services, and security
tooling. Most of what I ship is paid or private, so the public repos here are the parts
that were worth open-sourcing.

[![Plato-Tempmail CI](https://github.com/aplatogg/Plato-Tempmail/actions/workflows/check.yml/badge.svg)](https://github.com/aplatogg/Plato-Tempmail/actions/workflows/check.yml)
[![nfatools-steam release](https://img.shields.io/github/v/release/aplatogg/nfatools-steam?style=flat-square)](https://github.com/aplatogg/nfatools-steam/releases)

## Now

- **aPlato Tools Recoil** — moving the licence allowlist off a public repo onto a signed
  delivery endpoint, so the customer HWID list stops being world-readable without
  breaking installed clients.
- **Plato-Tempmail** — hardening the multi-tenant side: role tiers, Web Push, and a
  Playwright suite that runs against the real Worker, not a mock.
- **CI reliability** — browser tests that run against the real Worker and D1, plus the
  workflow fixes that stopped a dry-run build from reading a file the runner never had.

## Selected work

| Repo | What it is |
|---|---|
| [Plato-Tempmail](https://github.com/aplatogg/Plato-Tempmail) | Self-hosted temporary mail on Workers + D1: Owner/Admin/Dev/Member roles, Web Push, strict CSP, Playwright-tested in two viewports |
| [nfatools-steam](https://github.com/aplatogg/nfatools-steam) | Rust tooling around Steam account data |
| [chess-assistant](https://github.com/aplatogg/chess-assistant) | Stockfish overlay that reads a live Chess.com board over CDP |
| [steamtools-cleaner](https://github.com/aplatogg/steamtools-cleaner) | PowerShell cleanup for a Steam toolchain |

**aPlato Tools Recoil** (private) — desktop toolkit with a signed licence allowlist:
Ed25519-signed list fetched at launch, HWID bound to `sha256(MachineGuid|Hostname)`,
offline cache with signature verification.

## Stack

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Cloudflare Workers](https://img.shields.io/badge/Workers-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

Day to day: Windows + PowerShell, Wrangler and D1, Vitest and `node --test`, Biome,
`go test` and `cargo test`, and a disassembler or two when the source is missing.

## Upstream

| Repo | What landed |
|---|---|
| [nilearn](https://github.com/nilearn/nilearn/pull/6752) | `plot_img_comparison` gained `cmap` and `gridsize` |
| [mcp-memory-service](https://github.com/doobidoo/mcp-memory-service/pull/2053) | Dark-mode search field: theme-aware placeholder and typed text (1.21:1 → 11.31:1) |
| [phi](https://github.com/pulseaiclub/phi) | Five PRs: zh-CN docs sync, MCP limit message, dead-code drops |
| [pysad](https://github.com/selimfirat/pysad/pull/805) | `HyperLogLog` distinct-count sketch |
| [reporters-db](https://github.com/freelawproject/reporters-db/pull/293) | FLRA reporter variation |

Also reviewed [icalendar#2137](https://github.com/PyCalendar/icalendar/pull/2137)
(1298 tests run against its branch) before it landed.

## How I work

- Reproduce first. A bug report without a failing case is a guess.
- Verify in the real runtime — a real browser, a real Worker, a real device — not just
  the unit test that agrees with me.
- Small diffs, one logical change, and a changelog line a human can read.
- If a claim goes in a description, it gets measured, not estimated.

## Contact

- Mail: [aplato.gg@proton.me](mailto:aplato.gg@proton.me)
- Site: [mail.haldgoff.com](https://mail.haldgoff.com)
- Open to contract work on Go/Rust tooling, Workers services, and CI/QA automation.
