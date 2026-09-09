# Legal & Risk

Contracts and commitments, IP and licensing, regulatory compliance and privacy, the enterprise risk
register, corporate governance, and audit readiness.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `legal-risk` plugin.

**Reviewer-class department.** Its findings are not overrulable by the department under review; the
path for disagreement is escalation to `enterprise/executive/chief-executive`, and risk accepted
there is recorded as accepted with a name against it.

## Skills

| Skill | What it does |
|---|---|
| `chief-legal-and-risk-officer` | Owns legal, compliance, privacy, and enterprise risk. |
| `contract-review` | Reviews and negotiates commercial agreements. |
| `corporate-governance` | Maintains the corporate record and governance machinery. |
| `enterprise-risk` | Identifies, assesses, and tracks organizational risk. |
| `privacy-and-data-protection` | Assesses how personal data is collected and used. |
| `regulatory-compliance` | Identifies which regulations actually apply to you. |

Every skill in this department carries an explicit boundary: it structures the question and names
what needs qualified counsel, rather than giving legal advice.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create legal-risk
```

```bash
cp legal-risk/SOUL.md ~/.hermes/profiles/legal-risk/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/legal-risk/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

Because this department is reviewer-class, running it as its own profile is the point: a separate
agent, with its own soul, reviewing what the producing profiles committed to. See the
[top-level README](../README.md).
