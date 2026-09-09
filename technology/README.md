# Technology

Architecture and delivery — system design, APIs, cloud infrastructure, release and deployment,
observability, debugging, testing, technical debt, and the agent-and-prompt engineering around them.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `technology` plugin — jointly
the largest department with `marketing`, eighteen skills.

## Skills

| Skill | What it does |
|---|---|
| `ai-workflow-architect` | Designs AI systems and agent workflows. |
| `api-design` | Designs interfaces that survive their consumers. |
| `branch-and-worktree-workflow` | Isolates feature work and integrates it cleanly. |
| `chief-technology-officer` | Owns architecture and engineering delivery. |
| `cloud-infrastructure` | Designs and runs cloud infrastructure. |
| `code-review` | Conducts and responds to code review. |
| `completion-verification` | Verifies work is complete before claiming it. |
| `implementation-planning` | Turns a spec into a plan another session can run. |
| `observability-and-reliability` | Makes systems debuggable and reliably operable. |
| `parallel-agent-delivery` | Splits work across agents running at once. |
| `prompt-optimizer` | Turns rough intent into a reliable prompt. |
| `release-and-deployment` | Ships changes safely and often. |
| `skill-authoring` | Writes agent skills that trigger and help. |
| `solution-architecture` | Designs system structure and records the why. |
| `solution-exploration` | Explores the problem before any code is written. |
| `systematic-debugging` | Finds the root cause before proposing a fix. |
| `technical-debt-management` | Makes technical debt visible and decidable. |
| `test-driven-development` | Drives implementation from a failing test. |

Four of these are about agent work rather than product code — `ai-workflow-architect`,
`parallel-agent-delivery`, `prompt-optimizer`, and `skill-authoring` — and pair with
`enterprise/executive/agent-hierarchy`.

The boundary with IT Operations: this department owns the technology the company sells;
`enterprise/it-operations/chief-information-officer` owns the technology the company works on.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create technology
```

```bash
cp technology/SOUL.md ~/.hermes/profiles/technology/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/technology/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/technology/<skill>` without further configuration. To run the whole organization as one
agent instead, install a single profile and let all sixteen departments resolve from the same tree —
see the [top-level README](../README.md).
