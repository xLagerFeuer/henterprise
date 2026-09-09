# Data & Analytics

Data as an asset — governance and definitions, the warehouse and semantic layer, pipelines,
reporting, and the governance of models built on top.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `data-analytics` plugin.

## Skills

| Skill | What it does |
|---|---|
| `ai-ml-governance` | Governs models and AI systems in production. |
| `business-intelligence` | Builds reporting and self-serve analytics people use. |
| `chief-data-officer` | Owns data as an asset. |
| `data-engineering` | Builds and operates data pipelines. |
| `data-governance` | Establishes ownership, definitions, quality, and access. |
| `data-modeling` | Designs the warehouse and semantic layer. |

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create data-analytics
```

```bash
cp data-analytics/SOUL.md ~/.hermes/profiles/data-analytics/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/data-analytics/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/data-analytics/<skill>` without further configuration. To run the whole organization as
one agent instead, install a single profile and let all sixteen departments resolve from the same
tree — see the [top-level README](../README.md).
