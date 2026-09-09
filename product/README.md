# Product & Design

What gets built and why, and the design craft that decides whether it can be used — roadmap and
discovery, the design system, interface quality, visual direction, and audits.

Migrated from the [`headcount`](https://github.com/cbrock84/headcount) `product` plugin.

## Skills

| Skill | What it does |
|---|---|
| `brand-identity` | Defines and applies visual brand. |
| `chief-product-officer` | Owns what gets built and why. |
| `design-styles` | Applies a deliberate visual direction. |
| `design-system` | Builds and maintains the design system. |
| `interface-craft` | Raises the visual quality of an interface. |
| `interface-redesign` | Upgrades an interface without rebuilding it. |
| `presentation-design` | Designs decks and graphics that carry an argument. |
| `ux-product-auditor` | Audits an interface for usability and conversion. |
| `visual-reference-generation` | Produces design reference imagery before building. |

`interface-craft` raises quality; `ux-product-auditor` finds problems. They are deliberately
separate, and `design-system` is the dependency underneath both.

## Run this department as a Hermes profile

Hermes loads `SOUL.md` from `HERMES_HOME` only — **never** from a skills directory. The `SOUL.md`
here is a persona staged for installation, not a file Hermes picks up in place.

```bash
hermes profile create product
```

```bash
cp product/SOUL.md ~/.hermes/profiles/product/SOUL.md
```

Then point the profile at this skill tree in `~/.hermes/profiles/product/config.yaml`:

```yaml
skills:
  external_dirs:
    - <path-to>/hermes/skills
```

The skills themselves are discovered by directory walk, so they load from
`enterprise/product/<skill>` without further configuration. To run the whole organization as one
agent instead, install a single profile and let all sixteen departments resolve from the same tree —
see the [top-level README](../README.md).
