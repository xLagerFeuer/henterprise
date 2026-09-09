# Revenue

The revenue engine end to end — pricing and packaging, outbound, sales enablement, revenue
operations and forecasting, activation, retention, and referral.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `revenue` plugin.

## Skills

| Skill | What it does |
|---|---|
| `activation` | Gets new users from signup to first real value. |
| `chief-revenue-officer` | Owns the revenue engine end to end. |
| `outbound-prospecting` | Finds, qualifies, and reaches prospects cold. |
| `pricing-and-packaging` | Sets price, tiers, and the surfaces that carry them. |
| `referral-programs` | Designs referral and affiliate programs. |
| `retention` | Diagnoses and reduces churn. |
| `revenue-operations` | Runs the mechanics of the revenue engine. |
| `sales-enablement` | Builds what a sales team needs to sell. |

`revenue-operations` is the dependency underneath the rest: without agreed definitions, every number
the other skills produce is negotiable.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create revenue
```

```bash
cp revenue/SOUL.md ~/.hermes/profiles/revenue/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/revenue/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/revenue/<skill>` without further configuration. To run the whole organization as one
agent instead, install a single profile and let all sixteen departments resolve from the same tree —
see the [top-level README](../README.md).
