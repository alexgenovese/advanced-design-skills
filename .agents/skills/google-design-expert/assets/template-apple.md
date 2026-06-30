---
version: alpha
name: Apple Spacious Editorial
colors:
  primary: "#1D1D1F"          # Deep organic near-black
  secondary: "#86868B"        # Clean slate grey
  tertiary: "#0066CC"         # Royal blue brand focus
  neutral: "#FFFFFF"          # Pure clean stark white background
  surface: "#F5F5F7"          # Muted warm-grey surface layer
rounded:
  sm: "4px"
  md: "12px"
  lg: "18px"
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
    fontFamily: SF Pro Display
    fontSize: "56px"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: "-0.015em"
  body-lg:
    fontFamily: SF Pro Text
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.5
motion:
  easings:
    standard: "cubic-bezier(0.25, 1, 0.5, 1)"
    emphasized: "cubic-bezier(0.25, 1, 0.5, 1)"
  durations:
    fast: "200ms"
    medium: "400ms"
    slow: "600ms"
---

## Overview

An ultra-clean, luxury editorial style centered around immense typography, massive empty breathing rooms, and cinematic deceleration transitions. It eliminates all borders, lines, and complex shadows to let products and imagery stand as the absolute focus.

## Colors

- **Primary (#1D1D1F):** Warm near-black charcoal, softer than pure black to appear more premium and natural.
- **Secondary (#86868B):** Softer matte grey for descriptive paragraphs and subtexts.
- **Tertiary (#0066CC):** Pure primary blue, used very sparingly for link prompts and focus indicators.
- **Neutral (#FFFFFF):** stark, pure white light backdrop.

## Typography

Utilizes the modern sans-serif typographic scale (**SF Pro Display** or **Inter**) set with generous spacing, immense weights, and compressed line-heights.

## Layout

Spacious container margins (max-width `1200px`) combined with massive column paddings (`80px` to `120px`). Sections are wide-open.

## Elevation & Depth

No dropped shadows or borders. Elevation is achieved entirely through flat background shifts. Content sits on large, beautiful warm-grey cards (`#F5F5F7`) resting on the stark white background.

## Shapes

Highly smooth, large-radius geometry using `18px` corners (`rounded.lg`) for cards to emulate hardware curves, and `9999px` (`rounded.full`) for interaction buttons.

## Components

- **btn-apple:**
  - `backgroundColor`: "{colors.primary}"
  - `textColor`: "{colors.neutral}"
  - `rounded`: "{rounded.full}"
  - `padding`: "12px 24px"
- **btn-apple-hover:**
  - `opacity`: 0.85
- **btn-apple-active:**
  - `transform`: "scale(0.97)"
