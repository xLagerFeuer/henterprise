# Operations

How work actually gets done — process design, capacity, quality, service levels, procurement,
vendors, supply chain, facilities, and continuity.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `operations` plugin.

## Skills

| Skill | What it does |
|---|---|
| `business-continuity-and-resilience` | Plans for operating through disruption. |
| `capacity-and-demand-planning` | Matches operational capacity to expected demand. |
| `chief-operating-officer` | Owns execution across the organization. |
| `facilities-and-workplace` | Runs the physical and hybrid workplace. |
| `process-design` | Designs, documents, and fixes operational processes. |
| `procurement-and-sourcing` | Buys well, before a contract exists. |
| `quality-management` | Builds quality into operations. |
| `service-level-management` | Defines and manages service levels. |
| `supply-chain-and-logistics` | Manages the flow of goods and inputs. |
| `vendor-management` | Selects, contracts, and manages suppliers. |

`procurement-and-sourcing` and `vendor-management` split at signature: everything before belongs to
the first, everything after to the second.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create operations
```

```bash
cp operations/SOUL.md ~/.hermes/profiles/operations/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/operations/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/operations/<skill>` without further configuration. To run the whole organization as one
agent instead, install a single profile and let all sixteen departments resolve from the same tree —
see the [top-level README](../README.md).
