---
version: alpha
name: Premium Editorial UI
colors:
  primary: "#111111"          # Deep rich charcoal ink
  secondary: "#666666"        # Slate subtext
  tertiary: "#B8422E"         # Boston clay interaction color
  neutral: "#FAF9F6"          # Warm soft alabaster foundation
  surface: "#FFFFFF"          # Pure white card surface
rounded:
  sm: "4px"
  md: "8px"
  lg: "16px"
  full: "9999px"
spacing:
  base: "16px"
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "32px"
  xl: "64px"
typography:
  display-lg:
    fontFamily: Playfair Display
    fontSize: "48px"
    fontWeight: 600
    lineHeight: 1.15
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  label-mono:
    fontFamily: Geist Mono
    fontSize: "12px"
    fontWeight: 500
    lineHeight: 1.0
    letterSpacing: "0.1em"
motion:
  easings:
    standard: "cubic-bezier(0.4, 0, 0.2, 1)"
    emphasized: "cubic-bezier(0.2, 0, 0, 1)"
    spring-bouncy: "cubic-bezier(0.43, 0.21, 0.05, 1.48)"
  durations:
    fast: "150ms"
    medium: "300ms"
    slow: "500ms"
---

## Overview

A premium, gallery-style light design system pairing classic editorial serif typography with modern soft sans-serif body text. Perfect for high-end boutique branding, architectural journals, and minimalist portfolio sites.

## Colors

- **Primary (#111111):** Sophisticated, deep obsidian ink for headers and high-contrast titles.
- **Secondary (#666666):** Warm, soft charcoal slate for high readability on body copy and metadata.
- **Tertiary (#B8422E):** Boston Clay red accent used exclusively for interaction, hover highlights, and call-to-actions.
- **Neutral (#FAF9F6):** Warm, soft alabaster backdrop. Much softer and gentler on eyes than pure harsh white.
- **Surface (#FFFFFF):** Pure white layers for content cards, establishing elegant, low-contrast physical elevations.

## Typography

Pairing a classic high-contrast Serif Display face (**Playfair Display**) for elegant titles, a premium geometric Sans-Serif (**Plus Jakarta Sans**) for legible body copy, and a technical Mono font (**Geist Mono**) for spaced, uppercase labels and tags.

## Layout

A fluid grid alignment utilizing a strict 8px spacing system, combined with spacious negative margins. Cards have internal paddings of `24px` to establish containment.

## Elevation & Depth

Achieved entirely through low-contrast tonal transitions. Primary content sits on pure white cards floating softly on the alabaster neutral ground. Shadows are barely perceptible (`rgba(0,0,0,0.02)`) to preserve clean lines.

## Shapes

 approachable geometric sharpness using `8px` corner radius (`rounded.md`) for cards and inputs, and `4px` corner radius (`rounded.sm`) for buttons.

## Components

- **button-primary:**
  - `backgroundColor`: "{colors.tertiary}"
  - `textColor`: "{colors.neutral}"
  - `rounded`: "{rounded.sm}"
  - `padding`: "12px 24px"
- **button-primary-hover:**
  - `backgroundColor`: "#9A3220"
  - `transform`: "translateY(-1px)"
- **button-primary-active:**
  - `transform`: "scale(0.96)"

## Do's and Don'ts

- Do use the Boston Clay accent color sparingly (only one main action per view).
- Don't use heavy box-shadows; maintain flat, tonal elevations.
- Do implement fluid text clamp values for titles to prevent breaks on mobile.
