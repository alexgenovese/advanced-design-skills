---
version: alpha
name: Linear Dark Aesthetic
colors:
  primary: "#FFFFFF"          # High-contrast stark white
  secondary: "#8A8F98"        # Soft engineering slate
  tertiary: "#5E6AD2"         # Deep digital purple
  neutral: "#080710"          # Pitch black dark backdrop
  border-subtle: "rgba(255, 255, 255, 0.08)"
rounded:
  sm: "4px"
  md: "6px"
  lg: "12px"
spacing:
  base: "16px"
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "48px"
typography:
  display-md:
    fontFamily: Space Grotesk
    fontSize: "36px"
    fontWeight: 600
    lineHeight: 1.2
  body-md:
    fontFamily: Inter
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.6
motion:
  easings:
    standard: "cubic-bezier(0.4, 0, 0.2, 1)"
    emphasized: "cubic-bezier(0.16, 1, 0.3, 1)"
  durations:
    fast: "180ms"
    medium: "350ms"
---

## Overview

A dark, high-performance developer console aesthetic mirroring the engineering polish of Linear. Uses ultra-fine semi-transparent borders, sharp geometry, and soft glowing focus-points.

## Colors

- **Primary (#FFFFFF):** stark white for headers to provide maximum readability in dark environments.
- **Secondary (#8A8F98):** soft muted slate for paragraphs, captions, and secondary actions.
- **Tertiary (#5E6AD2):** digital brand purple for primary accents, links, and keyboard focus outlines.
- **Neutral (#080710):** deep black background that eliminates screen glow.

## Typography

Leverages **Space Grotesk** for display headers, evoking high-tech precision, and **Inter** for body text to maintain robust readability at all dimensions.

## Layout

A modular CSS Grid model (Bento grid structure). Elements are tightly organized using small, uniform spacings (`16px` to `24px`) to present rich information efficiently.

## Elevation & Depth

No dropped shadows. Depth is achieved entirely using fine, glowing borders (`rgba(255, 255, 255, 0.08)`) and radial gradient spotlights behind active layers.

## Shapes

Precise, sharp architectural geometry using `6px` (`rounded.md`) for cards and `4px` (`rounded.sm`) for buttons.

## Components

- **card-bento:**
  - `backgroundColor`: "rgba(255, 255, 255, 0.02)"
  - `borderColor`: "{colors.border-subtle}"
  - `rounded`: "{rounded.md}"
  - `padding`: "24px"
- **card-bento-hover:**
  - `borderColor`: "rgba(94, 106, 210, 0.3)"
  - `boxShadow`: "0 0 30px -10px rgba(94, 106, 210, 0.1)"
