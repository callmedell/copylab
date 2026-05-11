# CopyLab — Cursor Agent Skill

> Microcopy Stress Tester for product documents and UI flows.

CopyLab is a [Cursor Agent Skill](https://docs.cursor.com/agent/skills) that analyzes, critiques, and improves product copy with a focus on emotional states in high-stakes financial flows.

---

## What it does

CopyLab operates in two modes based on your input:

| Mode | Input | Role |
|---|---|---|
| **Document Analysis** | PRD, strategy doc, problem statement | Copy Strategy Partner — surfaces missing copy moments, maps risk & emotion, recommends copy types with examples |
| **Figma Flow Analysis** | Figma link / UI flow description | Copy Critic + UX Writer — scores existing copy (5 dimensions), identifies issues, stress-tests against panic/confusion/urgency |

### Emotional states it targets

| # | State | Trigger |
|---|---|---|
| 1 | **Panic** | Declined payments, errors, fraud alerts |
| 2 | **Confusion** | Unclear limits, unexpected outcomes |
| 3 | **Urgency** | Payment deadlines, verification steps |
| 4 | **Trust / Skepticism** | Money movement, permissions, fees |
| 5 | **Control / Loss of Control** | Declines, auto-pay, limits, restrictions |
| 6 | **Relief / Reassurance** | Success states, confirmations, issue resolved |
| 7 | **Uncertainty / Ambiguity** | Pending states, reviews, approvals |
| 8 | **Effort / Friction Sensitivity** | Long forms, verification steps |
| 9 | **Motivation / Value Perception** | Checkout, signup, feature adoption |
| 10 | **Fear of Loss** | Missed payments, penalties, limits |
| 11 | **Confidence / Competence** | Complex financial decisions |
| 12 | **Delight** *(use sparingly)* | Small wins, milestones |

---

## Installation

1. Clone or copy the `copylab/` folder into your Cursor skills directory:

```bash
# Personal (available across all your projects)
git clone https://github.com/callmedell/copylab ~/.cursor/skills/copylab

# Project-level (shared with repo collaborators)
git clone https://github.com/callmedell/copylab .cursor/skills/copylab
```

2. Restart Cursor (or reload the window).

3. Invoke it by mentioning CopyLab in your prompt:

```
Run CopyLab on this PRD: [paste or link]
```
```
Stress test this Figma flow: [figma.com/design/...]
```

---

## Output structure

### Mode 1 — Document Analysis
- **Copy Opportunity Map** — key moments where microcopy is critical
- **Risk & Emotion Analysis** — what users might feel at each moment
- **Copy Recommendations** — type of copy needed + 1–2 example options
- **Metric Impact** — conversion, drop-off, support, trust/NPS

### Mode 2 — Figma Flow Analysis
Works the same whether you share 1 frame or a 5-screen flow. Analysis is always broken down to the individual screen level.

- **Screen Inventory** — enumerates every frame before analysis begins
- **Flow Understanding** — 2–3 sentence summary
- **Copy Scorecard** — Clarity, Emotional Awareness, Trust, Actionability, Consistency (0–10) at flow level
- **Per-Screen Analysis** — for each screen: active emotional states, key copy issues, improved microcopy table (element / original / improved / why), missing states
- **Stress Test** — only the selected emotional states, anchored to specific screens
- **Business Impact** — conversion, drop-off, trust, support volume

---

## Tone

Senior product designer + Senior content designer hybrid. Direct, sharp, practical. Slightly critical when needed, always constructive. Fintech-grade clarity and trust as the baseline.

---

## License

MIT
