# Finance

The financial position — planning and forecasting, unit economics, cash and liquidity, capital
allocation, close and reporting, controls, revenue recognition, and tax.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `finance` plugin.

## Skills

| Skill | What it does |
|---|---|
| `budgeting-and-forecasting` | Runs the planning cycle. |
| `capital-allocation` | Evaluates where to spend limited capital. |
| `chief-financial-officer` | Owns the financial position. |
| `financial-modeling` | Builds and stress-tests financial models. |
| `financial-reporting-and-close` | Runs the period-end close and produces reporting. |
| `internal-controls-and-audit` | Designs and tests controls over financial reporting. |
| `revenue-recognition` | Determines when and how revenue is recognized. |
| `tax` | Structures the tax questions a growing business faces. |
| `treasury-and-liquidity` | Manages cash and liquidity. |
| `unit-economics` | Establishes whether you make money on each customer. |

Several of these carry an explicit boundary: `revenue-recognition`, `tax`, and
`internal-controls-and-audit` structure the question and say what to ask, but route material or
novel positions to auditors and qualified advisers rather than concluding them.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create finance
```

```bash
cp finance/SOUL.md ~/.hermes/profiles/finance/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/finance/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/finance/<skill>` without further configuration. To run the whole organization as one
agent instead, install a single profile and let all sixteen departments resolve from the same tree —
see the [top-level README](../README.md).
