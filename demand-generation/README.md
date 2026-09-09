# Demand Generation

Search, paid acquisition, lifecycle messaging, lead capture, listings, experimentation, and the
measurement underneath all of it.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `demand-generation` plugin.

## Skills

| Skill | What it does |
|---|---|
| `ai-search-optimization` | Optimizes for AI assistants and generated answers. |
| `app-store-optimization` | Improves App Store and Google Play performance. |
| `experimentation` | Designs, runs, and reads A/B tests. |
| `landing-page-cro-expert` | Audits and rewrites pages to increase conversion. |
| `lead-capture` | Converts anonymous traffic into known contacts. |
| `lifecycle-messaging` | Designs automated email and SMS programs. |
| `listing-distribution` | Gets a product listed where buyers look. |
| `marketing-analytics` | Sets up and audits marketing measurement. |
| `paid-advertising` | Plans, runs, and optimizes paid acquisition. |
| `programmatic-seo` | Builds search-targeted pages from a dataset. |
| `seo-strategy` | Audits and improves organic search performance. |

`marketing-analytics` is the dependency underneath `experimentation` and `paid-advertising` — verify
the tracking before optimizing against it. `lifecycle-messaging` carries a hard compliance boundary
on SMS.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create demand-generation
```

```bash
cp demand-generation/SOUL.md ~/.hermes/profiles/demand-generation/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/demand-generation/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/demand-generation/<skill>` without further configuration. To run the whole organization
as one agent instead, install a single profile and let all sixteen departments resolve from the same
tree — see the [top-level README](../README.md).
