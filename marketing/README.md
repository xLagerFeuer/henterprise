# Marketing

Positioning and messaging, content strategy and operations, campaigns and launches, copy, social,
video, visual assets, PR, partnerships, events, and the research underneath all of it.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `marketing` plugin — the
largest department, eighteen skills.

## Skills

| Skill | What it does |
|---|---|
| `behavioral-marketing` | Applies decision science to marketing choices. |
| `brand-voice` | Captures how a brand actually writes. |
| `chief-content-officer` | Runs content as an operation. |
| `chief-marketing-officer` | Owns brand, demand, content, and communications. |
| `content-strategy` | Decides what content to make and why. |
| `customer-research` | Plans, runs, and synthesizes customer research. |
| `events-and-field-marketing` | Plans and runs events that produce pipeline. |
| `marketing-campaign-planner` | Designs a multi-channel campaign around one story. |
| `marketing-copywriting` | Writes and edits marketing copy for any surface. |
| `marketing-planning` | Builds the marketing plan of record. |
| `newsletter-writer` | Writes newsletters and emails people actually open. |
| `partnership-marketing` | Builds reach through other people's audiences. |
| `positioning-and-messaging` | Establishes what a product is understood to be. |
| `public-relations` | Plans and executes earned media. |
| `social-post-craft` | Writes and evaluates social posts end to end. |
| `video-content` | Plans and scripts video, and designs the packaging. |
| `visual-content` | Designs the visual assets that carry content. |
| `youtube-producer` | Plans, packages, and scripts long-form video. |

`brand-voice` is the upstream dependency for every writing skill here — load it first for a new
brand, or the output comes back sounding like everyone else.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create marketing
```

```bash
cp marketing/SOUL.md ~/.hermes/profiles/marketing/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/marketing/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/marketing/<skill>` without further configuration. To run the whole organization as one
agent instead, install a single profile and let all sixteen departments resolve from the same tree —
see the [top-level README](../README.md).
