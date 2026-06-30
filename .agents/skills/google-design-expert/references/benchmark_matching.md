# Design Benchmark Matching

This guide explains how to analyze visual benchmarks (screenshots, references, brand names) and translate them into custom, high-end `DESIGN.md` configurations. 

---

## 🎨 Method 1: Analyzing Visual References (Reverse-Engineering)

When the user uploads a screenshot or mentions a live website, decompose its visual identity using this framework:

### 1. Palette Extraction & Contrast Math
- **The Ground (Neutral):** Identify the background color. If dark mode, is it pitch-black (`#000`), deep navy (`#0A0B10`), or ink charcoal (`#0D0D0E`)? If light mode, is it warm ivory (`#FAF9F6`) or cold slate (`#F1F3F5`)?
- **The Ink (Primary & Secondary):** Observe text contrast. Modern premium designs use very high contrast for headings (e.g., `#FFFFFF` on dark, `#09090B` on light) and a muted, translucent secondary for body/metadata (e.g., `rgba(255,255,255,0.6)` or `#71717A`).
- **The Highlight (Tertiary/Accent):** Note the interaction trigger color (buttons, focus states, active pills). Verify that the contrast ratio between the highlight and the background passes WCAG AA (4.5:1).

### 2. Space, Rhythm & Scale
- **Density:** Is the design information-dense (dashboard/SaaS style) or airy and editorial (marketing/portfolio style)?
  - *Dense (SaaS):* Spacing scale uses small increments (4px, 8px, 12px, 16px, 20px, 24px) to cluster information tightly in border-separated cards.
  - *Airy (Editorial):* Spacing scale uses dramatic jumps (12px, 24px, 48px, 80px, 120px) to give text elements "room to breathe".
- **Container Structure:** Does content sit inside visible cards, or is it flat and separated by negative space and hairline rules?

### 3. Corners & Shape Language
- **Corner Radii (The `rounded` Token):**
  - *Strict Engineered:* 4px - 6px corners (evokes precision, high-tech, database-first).
  - *Modern Approachable:* 8px - 12px corners (the contemporary SaaS default; balanced and friendly).
  - *Soft/Organic:* 16px - 24px corners (extremely mobile-first, consumer-focused, playful).

---

## 🏛️ Method 2: Matching Iconic Style Benchmarks

Use these exact token mappings and prose styles when the user requests a signature aesthetic:

### 1. The "Linear" Aesthetic (Premium Dark SaaS)
- **Concept:** Ultra-high-contrast elements on a pitch charcoal background, separated by fine semi-transparent borders, using radial color glows to draw the eye.
- **Color Palettes:**
  - `neutral`: `#080710` (Background)
  - `primary`: `#FFFFFF` (Headings)
  - `secondary`: `#8A8F98` (Muted text & icons)
  - `tertiary`: `#5E6AD2` (Brand interaction purple)
  - `border-color`: `rgba(255, 255, 255, 0.08)` (Fine separator borders)
- **Shape Language:** 6px or 8px corners (`rounded.md`). Flat layers, elevation through tonal contrast rather than dropped shadows.
- **Motion:** Fast, highly structured transitions. Zero delay on hover; 200ms ease-out on elements.

### 2. The "Stripe" Aesthetic (Professional Dynamic Modern)
- **Concept:** Vibrant, fluid, light-themed canvas with bold geometric typography, diagonal split sections, and extremely smooth transition curves.
- **Color Palettes:**
  - `neutral`: `#F8F9FC` (Soft blue-grey background)
  - `primary`: `#0A2540` (Deep navy ink for headlines)
  - `secondary`: `#425466` (Slate body text)
  - `tertiary`: `#635BFF` (Stripe interaction purple)
  - `accent-cyan`: `#00D4B2` (Energetic accent)
- **Shape Language:** 8px corners (`rounded.md`). Deep, multi-layered, ultra-soft shadows for elevation (`box-shadow: 0 50px 100px -20px rgba(50,50,93,0.12), 0 30px 60px -30px rgba(0,0,0,0.15)`).
- **Motion:** Emphasized, smooth, slightly dramatic easing (`cubic-bezier(0.2, 0.8, 0.2, 1)`).

### 3. The "Apple" Aesthetic (Luxury Editorial Minimal)
- **Concept:** Extreme minimalism, huge typographic hierarchy, immense negative space, absolute focus on product photography/content with no decorative lines or shadows.
- **Color Palettes:**
  - `neutral`: `#FFFFFF` (Pure stark white background) or `#F5F5F7` (Light warm grey background)
  - `primary`: `#1D1D1F` (Deep dark grey text)
  - `secondary`: `#86868B` (Muted body text)
  - `tertiary`: `#0066CC` (Clean focus blue)
- **Shape Language:** 12px or 16px corners for cards, but often layout elements are entirely flat or full-width.
- **Motion:** Cinematic, fluid, and slower transition rates (`duration: 400ms`) with smooth deceleration curves (`cubic-bezier(0.25, 1, 0.5, 1)`).

### 4. The "Vercel/Bento Grid" Aesthetic (Developer Precision)
- **Concept:** High-contrast grids, monochrome focus with single highlight accents, thin grey grid borders, and dynamic interactive hover effects.
- **Color Palettes:**
  - `neutral`: `#000000` (Stark black) or `#FFFFFF` (Stark white)
  - `primary`: `#FFFFFF` / `#000000` (Inverted)
  - `secondary`: `#888888` (Mid-grey text)
  - `tertiary`: `#0070F3` (Vercel blue highlight)
- **Shape Language:** Sharp 4px to 8px corners. Heavy use of CSS grid layouts (`gap: 16px` or `24px`).
- **Motion:** Highly responsive micro-feedback. Elastic scale changes on action clicks.

---

## 📝 Example: Translating a Benchmark to a `DESIGN.md` Proposal

When a user says: *"Make a bento-style landing page for an AI agent, styled like Linear."*

You should immediately formulate and write a `DESIGN.md` like this:

```markdown
---
version: alpha
name: Linear Bento
colors:
  primary: "#FFFFFF"          # stark white headlines
  secondary: "#8A8F98"        # soft slate body
  tertiary: "#5E6AD2"         # purple brand accent
  neutral: "#080710"          # pitch deep background
  border-subtle: "rgba(255, 255, 255, 0.08)"
rounded:
  sm: "4px"
  md: "8px"
  lg: "16px"
spacing:
  base: "16px"
  sm: "8px"
  md: "16px"
  lg: "32px"
  xl: "64px"
motion:
  easings:
    standard: "cubic-bezier(0.4, 0, 0.2, 1)"
    emphasized: "cubic-bezier(0.16, 1, 0.3, 1)"
  durations:
    fast: "180ms"
    medium: "350ms"
---

## Overview
A dark, bento-grid layout utilizing high-contrast typography and precise hairline borders to evoke the engineering polish of Linear.

## Colors
- **Primary (#FFFFFF):** Bright stark white for high-contrast headlines.
- **Secondary (#8A8F98):** Slate secondary text for readable paragraphs.
- **Tertiary (#5E6AD2):** Deep digital purple for accents and interactive call-to-actions.
- **Neutral (#080710):** Dark background mimicking a premium engineering console.

## Layout
The layout utilizes a strict CSS Grid model (Bento grid) with 24px gutters. Content is structured into sharp border-delineated cards.
```

By presenting this structured document first, you ensure alignment with the user's dream visual aesthetic before writing a single line of application code.
