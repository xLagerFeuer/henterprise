# Customer Experience

Everything the customer experiences after the sale — support operations, escalation, self-service,
and the feedback loop back into product.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `customer-experience` plugin.

## Skills

| Skill | What it does |
|---|---|
| `chief-customer-officer` | Owns the customer experience after the sale. |
| `escalation-management` | Handles customer situations beyond normal support. |
| `self-service-and-knowledge` | Builds the help center and in-product guidance. |
| `support-operations` | Designs and runs the support function. |
| `voice-of-customer` | Builds the loop from what customers say to what changes. |

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create customer-experience
```

```bash
cp customer-experience/SOUL.md ~/.hermes/profiles/customer-experience/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/customer-experience/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/customer-experience/<skill>` without further configuration. To run the whole
organization as one agent instead, install a single profile and let all sixteen departments resolve
from the same tree — see the [top-level README](../README.md).
