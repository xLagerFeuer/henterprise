# Security

Security posture and standards, access policy, threat modeling, architecture and code review,
vulnerability management, and incident response.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `security` plugin.

**Reviewer-class department.** Its blocking findings are not overrulable by the department under
review; the escalation path is `enterprise/executive/chief-executive`, and risk accepted there is
recorded with a name against it. This is why the CISO reports independently rather than under the
CTO.

## Skills

| Skill | What it does |
|---|---|
| `access-and-identity` | Designs and audits who can reach what. |
| `chief-information-security-officer` | Owns the security posture of the organization. |
| `incident-response` | Runs a security incident from detection to closure. |
| `security-architecture-review` | Reviews a design or change for security. |
| `threat-modeling` | Identifies what could go wrong before it is built. |
| `vulnerability-management` | Runs the loop from weakness to confirmed fix. |

The split with IT Operations is deliberate: this department sets policy —
`access-and-identity` and `vulnerability-management` — and
`enterprise/it-operations/identity-lifecycle-administration` and
`enterprise/it-operations/systems-administration` execute it.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create security
```

```bash
cp security/SOUL.md ~/.hermes/profiles/security/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/security/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

Because this department is reviewer-class, running it as its own profile is the point: a separate
agent, with its own soul, reviewing what the building profiles produced. See the
[top-level README](../README.md).
