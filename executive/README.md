# Executive

Direction, capital and attention allocation, cross-functional arbitration, strategy validation, and
the method for structuring the agent organization itself.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `executive` plugin.

## Skills

| Skill | What it does |
|---|---|
| `agent-hierarchy` | Designs orchestrator-and-subagent hierarchies. |
| `ai-research-analyst` | Produces executive research with cited sources. |
| `business-growth-consultant` | Finds the one constraint limiting growth. |
| `ceo-advisor` | Pressure-tests a decision before it is committed to. |
| `chief-executive` | Sets direction and makes the calls no one else can. |
| `saas-idea-validator` | Evaluates a startup idea and returns a verdict. |

`agent-hierarchy` carries support files loaded on demand: `references/playbook.md`,
`references/starter-rosters.md`, `references/bootstrap-prompt.md`, and `scripts/agent-guard.mjs`.
These are copied verbatim from the source repository and are progressive-disclosure data — Hermes
never scans them as skills.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create executive
```

```bash
cp executive/SOUL.md ~/.hermes/profiles/executive/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/executive/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/executive/<skill>` without further configuration. The executive persona is the natural
choice for a single profile running the whole organization — every other department's chief
escalates here. See the [top-level README](../README.md).
