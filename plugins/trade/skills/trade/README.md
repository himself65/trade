# Trade

Multi-leg options trading assistant — concrete strikes, IV-aware structures, probability-weighted scenarios. Backed by a curated library of 15 pitfalls and 3 closed-trade case studies (INTC, Mag-7, APP).

## Triggers

- Trade analysis requests, options strategy recommendations, post-mortems
- Mentions of multi-leg structures: Jade Lizard, bull put / bear call spread, iron condor, diagonal, calendar
- Earnings positioning, IV / IV crush, channel checks, AH price action
- Any single-stock options play in a US-equity context

See the full trigger list in the `description` field of `SKILL.md`.

## Platform

**CLI only** — uses the `finance-data-providers:funda-data` skill for market data via the Funda AI API.

## Setup

1. Install the [`finance-skills`](https://github.com/himself65/finance-skills) plugin marketplace and the `finance-data-providers:funda-data` skill — required for market data.
2. Set the Funda API key:
   ```bash
   export FUNDA_API_KEY="your-funda-api-key"
   ```
   or add to `.env` at the repo root (the skill reads `.env` from the git root so worktrees inherit the key).

## Reference Files

| File | Description |
|---|---|
| `references/strategies.md` | Structure-to-regime matching, setup checklist, position management |
| `references/pitfalls/README.md` | Index of 15 trading pitfalls (severity-tagged, lookup-by-trade-type) |
| `references/pitfalls/NN-*.md` | One file per pitfall — read only when relevant |
| `references/ticker/README.md` | Index of closed trade case studies |
| `references/ticker/<name>.md` | One file per case study (INTC Apr 2026, Mag-7 Q1 2026, APP May 2026) |

## Coverage

- 15 analytical pitfalls covering consensus anchoring, flow misreading, IV crush traps, T+1 reverse drift, LEAPS vega tax, manipulator-tape recognition, channel-check sample bias, AH order-book fades, and more.
- 3 detailed case studies showing thesis evolution, structure selection, and post-mortem lessons.
- Structure-to-regime quick reference covering high/low IV regimes paired with directional / neutral / manipulator-tape views.
