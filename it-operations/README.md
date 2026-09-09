# IT Operations

The technology the company works *on* — identity execution, endpoints, network, servers, the service
desk, the asset register, and the tested restore.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `it-operations` plugin.

## Skills

| Skill | What it does |
|---|---|
| `backup-and-recovery` | Protects and restores data. |
| `chief-information-officer` | Runs the technology the company works on. |
| `endpoint-management` | Manages laptops, desktops, and mobile devices. |
| `identity-lifecycle-administration` | Executes joiner, mover and leaver processes. |
| `it-asset-management` | Tracks hardware and software assets through their life. |
| `network-administration` | Designs and operates the corporate network. |
| `service-desk` | Runs the IT service desk. |
| `systems-administration` | Runs servers and corporate systems. |

The boundary with Security is deliberate: `enterprise/security/access-and-identity` and
`enterprise/security/vulnerability-management` set policy, and these skills execute it.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create it-operations
```

```bash
cp it-operations/SOUL.md ~/.hermes/profiles/it-operations/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/it-operations/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/it-operations/<skill>` without further configuration. To run the whole organization as
one agent instead, install a single profile and let all sixteen departments resolve from the same
tree — see the [top-level README](../README.md).
