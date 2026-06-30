# Modern Web Animations Guide

This guide provides precise blueprints and CSS/Tailwind rules for implementing buttery-smooth, cinematic web animations, micro-interactions, and transition orchestration.

---

## 📐 1. Easing Equations & Physics

Do not use default transitions like `ease`, `ease-in-out`, or simple linear transitions. Instead, implement specialized cubic-bezier values that mimic physical mass, friction, and tension:

| Easing Type | CSS cubic-bezier | Description | Use Case |
|:---|:---|:---|:---|
| **Standard** | `cubic-bezier(0.4, 0, 0.2, 1)` | Natural deceleration curve. | Standard on-page hover transitions, state toggles. |
| **Emphasized** | `cubic-bezier(0.2, 0, 0, 1)` | Fast initial acceleration with an extremely soft deceleration tail. | Major layout adjustments, slider swipes, drawer slides. |
| **Spring-Bouncy** | `cubic-bezier(0.43, 0.21, 0.05, 1.48)` | Elastic spring back. Overshoots the target value slightly and bounces into place. | Interactive action buttons, active click-states, card hovering. |
| **Decelerate** | `cubic-bezier(0, 0, 0.2, 1)` | Swift entry curve. | Modal or dialog entrances (element starts fast then settles). |

---

## ⏱️ 2. Duration Scale

Match duration to the physical size of the movement. Smaller distances/states require shorter durations to prevent the interface from feeling "mushy" or slow.

- **Fast (100ms - 150ms):** For color changes, hover states, checkbox toggles, and tiny icon shifts.
- **Medium (250ms - 350ms):** For card transitions, dropdown expansions, tab-switching, and layout shifting.
- **Slow (400ms - 600ms):** For full-page routing, hero banner slide-ins, and large full-screen overlays/modals.

---

## 🎼 3. Staggered Entrance Orchestration

When a page or section first loads, avoid popping all elements onto the screen at once. Orchestrate an elegant entrance using a **cascade / stagger effect** along the user's natural vertical reading line.

### CSS Custom Property Implementation (Re-usable & Performant)

Instead of hardcoding a separate animation delay for every single card, define a local delay calculation in your container, and assign indexes to elements:

```css
/* Core Keyframes */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Base Utility Class */
.animate-stagger-item {
  opacity: 0;
  animation: fadeInUp 450ms cubic-bezier(0.2, 0.8, 0.2, 1) forwards;
  animation-delay: calc(var(--stagger-index, 0) * 80ms);
}
```

```html
<!-- HTML Bento Grid Stagger Pattern -->
<div class="grid grid-cols-3 gap-6">
  <div class="animate-stagger-item" style="--stagger-index: 1;">Card A</div>
  <div class="animate-stagger-item" style="--stagger-index: 2;">Card B</div>
  <div class="animate-stagger-item" style="--stagger-index: 3;">Card C</div>
  <div class="animate-stagger-item" style="--stagger-index: 4;">Card D</div>
</div>
```

---

## 🔘 4. Micro-Interactions (Reactive UI)

Give elements tactile feedback to make the user interface feel responsive and "alive" under the cursor.

### A. The "Springy" Active Click-State
Every button should physically compress when clicked to mimic a real-world tactile button:
```css
.btn-premium {
  transition: transform 150ms cubic-bezier(0.43, 0.21, 0.05, 1.48);
}
.btn-premium:active {
  transform: scale(0.96); /* Instant compression */
}
```

### B. Magnetic Hover Glow
For dark-mode interfaces, implement a hover cursor follower (or simulated radial mask) to light up fine card borders when hovered:
```css
.card-premium {
  position: relative;
  background: linear-gradient(180deg, rgba(255,255,255,0.05) 0%, rgba(255,255,255,0) 100%);
  border: 1px solid rgba(255, 255, 255, 0.08);
  transition: border-color 200ms ease;
}
.card-premium:hover {
  border-color: var(--color-tertiary); /* Mapped to accent token */
  box-shadow: 0 0 25px -5px rgba(var(--color-tertiary-rgb), 0.15); /* Soft, matched color glow */
}
```

### C. Subtle Shimmer Effect
Give cards an organic, rotating light sweep to highlight their surface on load or hover:
```css
@keyframes shimmer {
  0% { background-position: -200% 0; }
  100% { background-position: 200% 0; }
}
.shimmer-trigger:hover .shimmer-element {
  background: linear-gradient(
    90deg, 
    rgba(255,255,255,0) 0%, 
    rgba(255,255,255,0.08) 50%, 
    rgba(255,255,255,0) 100%
  );
  background-size: 200% 100%;
  animation: shimmer 1.5s infinite;
}
```

---

## ♿ 5. Accessibility & Motion Respect

Always write highly accessible motion code. Users can configure their operating systems to reduce screen movement. Always respect this setting using CSS media queries by disabling translational and scaling movements while maintaining a simple, instant opacity toggle:

```css
@media (prefers-reduced-motion: reduce) {
  .animate-stagger-item {
    animation: none !important;
    opacity: 1 !important;
    transform: none !important;
    transition: none !important;
  }
  
  .btn-premium, .card-premium {
    transform: none !important;
    transition: opacity 150ms linear !important;
  }
}
```
Applying this wrapper guarantees that your high-end design is certified for all users, elevating the professional standard of your output.
