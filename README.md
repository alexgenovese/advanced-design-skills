# Advanced Design Skills (`google-design-expert`)

A premium visual design & cinematic motion skill for AI coding agents, based on the **Google DESIGN.md** specification.

This skill equips coding agents with a structured understanding of high-end, custom visual aesthetics and buttery-smooth micro-interactions, avoiding typical generic AI-style templates.

---

## ✨ Core Capabilities

1. **Benchmark-Driven Style Matching:** Replicates modern, top-tier aesthetics including **Linear, Stripe, Apple, and Bento/Vercel Grid**.
2. **Animation & Motion Tokens:** Extends Google's frontmatter format with physical easings (spring curves), custom durations, and staggered load animations.
3. **High-End Visual Polish:** Governs typography pairings, organic warm background foundations (limestone backgrounds), frosted glass layering (glassmorphism), and radial spotlight glows.
4. **Google Lint Compatibility:** Fully compatible with `@google/design.md` linter.

---

## 🚀 Installation & Testing

You can easily install this skill globally in your local agents environment or add it directly to a project.

### 1. Local Testing (Symlink/Copy to ~/.agents)
To test the skill immediately on your local machine, copy the skill folder into your agent's directory:
```bash
cp -r .agents/skills/google-design-expert ~/.agents/skills/
```

### 2. GitHub Installation
Since we have prepared this as a complete Git repository, you can publish it to your GitHub account:

1. Initialize and push this repository to GitHub:
   ```bash
   git init
   git add .
   git commit -m "feat: initialize advanced-design-skills package"
   git remote add origin git@github.com:<your_username>/advanced-design-skills.git
   git branch -M main
   git push -u origin main
   ```

2. Once pushed, install it in any of your project repositories using the standard `skills` command:
   ```bash
   npx skills add <your_username>/advanced-design-skills
   ```

---

## 📂 File Structure

```
google-design-expert/
├── SKILL.md                  # Core instructions and triggers for the agent
├── references/
│   ├── benchmark_matching.md  # Rules for decoding and matching Linear, Stripe, Apple, Bento
│   ├── animations_guide.md   # Blueprints for spring curves, delays, stagger, and micro-actions
│   └── visual_polish.md      # Rules for organic warm bases, typography pairings, glassmorphism
└── assets/
    ├── template-premium-ui.md # Editorial light system baseline
    ├── template-linear.md     # Engineering-first deep dark system
    ├── template-stripe.md     # Active enterprise light grid system
    └── template-apple.md      # Luxurious, spacious minimalist system
```

---

## 🎨 How to Trigger the Skill

Once installed, this skill will automatically activate on any request like:
- *"Create a beautiful bento landing page"*
- *"Style this page like Stripe"*
- *"Add smooth spring animation on hover"*
- *"Create a DESIGN.md file using Linear style"*
