# Corporate Strategy

Where the business plays and how it wins over a multi-year horizon — portfolio choices, corporate
development, strategic partnerships, and planning under uncertainty.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `corporate-strategy` plugin.

## Skills

| Skill | What it does |
|---|---|
| `chief-strategy-officer` | Owns where the business plays and how it wins. |
| `mergers-and-acquisitions` | Runs corporate development end to end. |
| `portfolio-strategy` | Decides where capital and attention go. |
| `scenario-planning` | Plans under genuine uncertainty. |
| `strategic-alliances` | Structures partnerships that change what you can do. |

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create corporate-strategy
```

```bash
cp corporate-strategy/SOUL.md ~/.hermes/profiles/corporate-strategy/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/corporate-strategy/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/corporate-strategy/<skill>` without further configuration. To run the whole
organization as one agent instead, install a single profile and let all sixteen departments resolve
from the same tree — see the [top-level README](../README.md).
