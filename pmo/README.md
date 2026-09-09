# PMO

Portfolio governance, program and project delivery, dependencies and delivery risk, benefits
realization, and change adoption.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `pmo` plugin.

## Skills

| Skill | What it does |
|---|---|
| `benefits-realization` | Ensures projects deliver the value they promised. |
| `change-and-adoption` | Gets people to actually use what was delivered. |
| `dependency-and-risk-management` | Manages delivery risk and cross-team dependencies. |
| `head-of-pmo` | Runs the PMO, and keeps it worth funding. |
| `portfolio-governance` | Governs the portfolio of work. |
| `program-management` | Plans and drives cross-functional programs. |
| `project-delivery` | Plans and delivers a single project. |

`benefits-realization` and `change-and-adoption` are the two that make the function worth funding —
a PMO that governs intake but never checks outcomes has only made the front door more expensive.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create pmo
```

```bash
cp pmo/SOUL.md ~/.hermes/profiles/pmo/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/pmo/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from `enterprise/pmo/<skill>`
without further configuration. To run the whole organization as one agent instead, install a single
profile and let all sixteen departments resolve from the same tree — see the
[top-level README](../README.md).
