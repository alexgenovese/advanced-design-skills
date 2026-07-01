[![skills.sh](https://skills.sh/b/alexgenovese/google-design-expert)](https://skills.sh/alexgenovese/google-design-expert)

# Advanced Design Skills

Premium visual design & cinematic motion skill for AI coding agents, built on Google's [DESIGN.md](https://github.com/google-labs-code/design.md) specification.

This skill equips coding agents with a structured understanding of high-end, custom visual aesthetics and buttery-smooth micro-interactions — avoiding typical generic AI-style templates.

---

## Core Capabilities

| Capability | Description |
|:---|:---|
| **Benchmark-Driven Style Matching** | Replicates modern, top-tier aesthetics: Linear, Stripe, Apple, Bento/Vercel Grid |
| **Animation & Motion Tokens** | Physical easing curves (spring physics), staggered entrances, micro-interactions |
| **High-End Visual Polish** | Organic warm foundations (limestone), glassmorphism, radial glow effects |
| **Google Lint Compatible** | Works with `@google/design.md` CLI for validation and export to Tailwind/DTCG |

---

## Architecture

The agent follows a 4-step workflow when triggered:

```
1. Capture Benchmarks    →  Identify target aesthetic (brand, screenshot, description)
         ↓
2. Write DESIGN.md       →  Generate tokens + prose with motion extensions
         ↓
3. Validate              →  Run `npx @google/design.md lint DESIGN.md`
         ↓
4. Implement             →  Export tokens to Tailwind v4, apply animations, self-critique
```

### Custom Extensions to Google's Spec

The skill extends the standard `DESIGN.md` frontmatter with:

| Extension | Purpose |
|:---|:---|
| `motion:` | Easing curves, duration scales, transition presets |
| `effects:` | Backdrop-filter/glassmorphism, radial-gradient spotlights |
| `components.*-hover:` | Per-component interaction states (hover, active, focus) |

---

## Benchmark Styles

Four pre-configured aesthetic presets ready for instant use:

### Linear (Dark SaaS)

Ultra-high-contrast on pitch charcoal, fine semi-transparent borders, purple accent glow.

| Token | Value |
|:---|:---|
| `neutral` | `#080710` |
| `primary` | `#FFFFFF` |
| `secondary` | `#8A8F98` |
| `tertiary` | `#5E6AD2` |
| `border-subtle` | `rgba(255, 255, 255, 0.08)` |

### Stripe (Professional Light)

Deep navy on soft blue-grey, vibrant indigo accent, dramatic multi-layered shadows.

| Token | Value |
|:---|:---|
| `neutral` | `#F8F9FC` |
| `primary` | `#0A2540` |
| `secondary` | `#425466` |
| `tertiary` | `#635BFF` |

### Apple (Editorial Minimal)

Extreme minimalism, huge typographic hierarchy, immense negative space, no shadows.

| Token | Value |
|:---|:---|
| `neutral` | `#FFFFFF` / `#F5F5F7` |
| `primary` | `#1D1D1F` |
| `secondary` | `#86868B` |
| `tertiary` | `#0066CC` |

### Bento/Vercel (Developer Precision)

High-contrast monochrome grids, thin grey borders, single blue highlight, elastic micro-feedback.

| Token | Value |
|:---|:---|
| `neutral` | `#000000` / `#FFFFFF` |
| `primary` | `#FFFFFF` / `#000000` |
| `secondary` | `#888888` |
| `tertiary` | `#0070F3` |

---

## Animation System

### Easing Curves

| Type | `cubic-bezier` | Use Case |
|:---|:---|:---|
| Standard | `0.4, 0, 0.2, 1` | Hover transitions, state toggles |
| Emphasized | `0.2, 0, 0, 1` | Layout adjustments, drawer slides |
| Spring-Bouncy | `0.43, 0.21, 0.05, 1.48` | Button clicks, card hovers |
| Decelerate | `0, 0, 0.2, 1` | Modal entrances |

### Duration Scale

| Speed | Duration | Use Case |
|:---|:---|:---|
| Fast | 100-150ms | Color changes, toggles, icon shifts |
| Medium | 250-350ms | Card transitions, dropdowns, tabs |
| Slow | 400-600ms | Page routing, hero banners, overlays |

### Micro-Interactions

- **Springy click-state**: `transform: scale(0.96)` on `:active`
- **Magnetic hover glow**: Radial border-color shift + soft color box-shadow
- **Staggered entrances**: `animation-delay: calc(var(--index) * 80ms)`
- **Shimmer sweep**: Gradient overlay animation on hover

All animations respect `prefers-reduced-motion: reduce`.

---

## Visual Polish

- **Limestone backgrounds**: Warm `#FAF9F6` or `#0E1117` instead of pure white/black
- **Typography pairing**: Display serif + body sans-serif (Playfair + Plus Jakarta, Space Grotesk + Inter)
- **Glassmorphism**: `backdrop-filter: blur(12px) saturate(180%)` with razor-thin borders
- **Radial spotlights**: `radial-gradient(800px circle, ...)` for ambient atmosphere
- **Fluid scaling**: `clamp()` for typography, spacing, and grid gaps — responsive by default

---

## Getting Started

### Prerequisites

- Node.js 18+
- `npx skills` CLI (installed globally via `npm install -g skills`)

### Install via GitHub

```bash
npx skills add alexgenovese/advanced-design-skills -g -y
```

### Install locally (development)

```bash
git clone git@github.com:alexgenovese/advanced-design-skills.git
cd advanced-design-skills
cp -r .agents/skills/google-design-expert ~/.agents/skills/
```

### Validate a DESIGN.md

```bash
npx @google/design.md lint DESIGN.md
```

### Export to Tailwind v4

```bash
npx @google/design.md export --format css-tailwind DESIGN.md > theme.css
```

---

## Project Structure

```
advanced-design-skills/
├── .agents/skills/google-design-expert/
│   ├── SKILL.md                        # Agent instructions & trigger config
│   ├── references/
│   │   ├── benchmark_matching.md       # Brand reverse-engineering guide
│   │   ├── animations_guide.md         # Easing, stagger, micro-interactions
│   │   └── visual_polish.md           # Glassmorphism, gradients, typography
│   └── assets/
│       ├── template-premium-ui.md      # Editorial light baseline
│       ├── template-linear.md          # Linear dark preset
│       ├── template-stripe.md          # Stripe professional preset
│       └── template-apple.md           # Apple editorial preset
├── package.json
├── README.md
└── .gitignore
```

---

## How to Trigger

Once installed, the skill activates automatically on requests like:

| Trigger | Example |
|:---|:---|
| UI/landing page | *"Create a bento landing page for an AI agent"* |
| Brand matching | *"Style this page like Linear"* |
| Animations | *"Add smooth spring animation on hover"* |
| Design tokens | *"Create a DESIGN.md using Stripe style"* |
| CSS/Tailwind | *"Write Tailwind classes matching this design"* |

---

## License

MIT

---

## Credits

- Built on [Google DESIGN.md](https://github.com/google-labs-code/design.md) specification
- Design token format inspired by [W3C Design Token Format](https://www.designtokens.org/)
