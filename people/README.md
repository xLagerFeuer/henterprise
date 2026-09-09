# People

The organization itself — org design, workforce planning, hiring, leveling and pay, performance,
development, benefits, onboarding and offboarding, and employee relations.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `people` plugin.

## Skills

| Skill | What it does |
|---|---|
| `benefits-and-leave` | Designs and runs employee benefits and leave. |
| `chief-human-resources-officer` | Owns the organization itself. |
| `compensation-and-leveling` | Builds the leveling framework and pay structure. |
| `employee-relations` | Handles the difficult human situations. |
| `hiring-and-interviewing` | Designs and runs hiring. |
| `learning-and-development` | Builds capability across the organization. |
| `onboarding-and-offboarding` | Designs the joining and leaving experience. |
| `org-design` | Designs how an organization is structured. |
| `performance-management` | Runs performance systems that change behavior. |
| `workforce-planning` | Plans the shape and size of the workforce. |

`employee-relations`, `performance-management`, `compensation-and-leveling`, and `benefits-and-leave`
each carry an explicit boundary: they structure the decision and name what to ask, and route the
legally regulated parts to qualified counsel.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create people
```

```bash
cp people/SOUL.md ~/.hermes/profiles/people/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/people/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/people/<skill>` without further configuration. To run the whole organization as one
agent instead, install a single profile and let all sixteen departments resolve from the same tree —
see the [top-level README](../README.md).
