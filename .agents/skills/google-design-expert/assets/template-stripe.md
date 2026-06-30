---
version: alpha
name: Stripe Clean Canvas
colors:
  primary: "#0A2540"          # Deep rich navy
  secondary: "#425466"        # Slate grey
  tertiary: "#635BFF"         # Vibrant Stripe Indigo
  neutral: "#F8F9FC"          # Light soft blue-grey
  surface: "#FFFFFF"          # Pure white surface layers
rounded:
  sm: "4px"
  md: "8px"
  lg: "16px"
spacing:
  base: "16px"
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "32px"
  xl: "64px"
typography:
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: "42px"
    fontWeight: 700
    lineHeight: 1.1
  body-md:
    fontFamily: Inter
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
motion:
  easings:
    standard: "cubic-bezier(0.4, 0, 0.2, 1)"
    emphasized: "cubic-bezier(0.2, 0.8, 0.2, 1)"
  durations:
    fast: "150ms"
    medium: "300ms"
    slow: "450ms"
---

## Overview

A light, energetic, enterprise SaaS aesthetic. Focuses on dynamic diagonal grids, deep elegant box-shadows, and bright accent color transitions that suggest movement and professional velocity.

## Colors

- **Primary (#0A2540):** Deep noble navy for professional title weights and strong structural lines.
- **Secondary (#425466):** Balanced slate grey for extensive body copy.
- **Tertiary (#635BFF):** High-saturation violet indigo, evoking digital currency and premium interactions.
- **Neutral (#F8F9FC):** Bright, high-end, clean background foundation.

## Typography

Utilizes the modern geometric **Plus Jakarta Sans** for headlines (to look friendly yet highly established) and **Inter** for clean, legible layout typography.

## Layout

Dynamic and fluid layout utilizing massive, bold negative spaces and split diagonal dividers. Sections are spaced widely (`64px` to `120px` margins) to emphasize large scale and premium quality.

## Elevation & Depth

Dramatic, ultra-soft, multi-layered card shadows that diffuse light widely, creating premium elevations and physical presence:
`box-shadow: 0 50px 100px -20px rgba(50,50,93,0.08), 0 30px 60px -30px rgba(0,0,0,0.12)`.

## Shapes

Clean, balanced geometric structures using `8px` corner radius (`rounded.md`) for cards and inputs.

## Components

- **button-stripe:**
  - `backgroundColor`: "{colors.tertiary}"
  - `textColor`: "{colors.surface}"
  - `rounded`: "{rounded.md}"
  - `padding`: "12px 20px"
- **button-stripe-hover:**
  - `backgroundColor`: "#4F46E5"
  - `boxShadow`: "0 7px 14px rgba(50, 50, 93, 0.1), 0 3px 6px rgba(0, 0, 0, 0.08)"
  - `transform`: "translateY(-1px)"
