# Project Manager Interview Playbook

**Full-Time MBA Program · David Eccles School of Business, University of Utah**

A complete, self-contained prep system for project management interviews: **100 questions** with four-layer model answers, **10 frameworks**, an 8-section formulas-and-concepts **battlecard**, **10 red flags** with fixes, a **voice-powered practice studio**, and a **readiness tracker** that compares self-assessed confidence against logged coaching scores.

Built for general/cross-industry PM roles, including loops that test **PMP/CAPM-style knowledge** — critical path math, earned value formulas, risk analysis, contract types. Behavioral "tell me about a time" questions are deliberately excluded; stakeholder and leadership content is scenario-judgment instead.

---

## Live site
Deployed via GitHub Pages: [project-manager-interview-playbook.html](https://coryjburk.github.io/intv-playbook-proj-mgmt_vc/) — no build step, no dependencies, no server; the entire application is one HTML file.

---

## What's inside

| Section | Contents |
|---|---|
| **Question Bank** | 100 questions across 8 categories, tagged Foundational / Core / Advanced. Each has four answer layers: **Conversational** (say-it-out-loud model answer), **Deep Dive** (the underlying concept and formulas), **Coaching** (how to score points), **Red Flag** (what tanks the answer). Full-text search + stacking topic/level filters. |
| **Frameworks** | CPM (forward/backward pass, float), EVM (full formula suite), Triple Constraint, WBS & the 100% rule, RAID, Risk Management Cycle, RACI, Change Control, MoSCoW, Power/Interest Grid — each with steps and an interview tip. |
| **Battlecard** | Game-day reference: must-know concepts, formula card (CV, SV, CPI, SPI, EAC ×4, TCPI, PERT, float, comm channels, EMV), power phrases, methodology decision guide, common mistakes, candidate signals, final-round differentiators, last-minute checklist. |
| **Red Flags** | The 10 patterns that sink candidates — formula fumbles, methodology dogmatism, status-reporter syndrome, scope-creep tolerance, etc. — with warning signs and fixes. |
| **Practice Studio** | Per-question modal with Web Speech API transcription: live transcript with filler-word highlighting, words-per-minute (measured against speaking time, not think time), duration, and filler stats. Generates a complete AI-coaching prompt including your transcribed answer. |
| **Readiness** | Two views side by side: coach-graded scores (6-dimension rubric → 0–100 → five tiers) and your own confidence ratings — with calibration warnings when they disagree. Per-category trends and a 10-session history. |
| **AI Coach Generator** | Standalone prompts for four modes — mock interview, critique, rapid-fire drill, rubric scoring — scoped to any category. Paste into Claude or any AI assistant. |

### Question categories

1. PM Fundamentals & Methodology (12)
2. Scheduling & Critical Path (13)
3. Cost & Earned Value (12)
4. Scope, Requirements & Change Control (12)
5. Risk, Issues & RAID (13)
6. Agile, Scrum & Hybrid Delivery (12)
7. Stakeholders, Communication & Resources (13)
8. Quality, Procurement & Closure (13)

### Scoring rubric

Six dimensions, each 1–5, logged after AI-coached practice: **Problem Framing · Technical Fluency · Structure · Constraint Tradeoffs · Stakeholder Awareness · Communication**. Overall score maps to tiers: Getting Started (0–49) → Developing (50–67) → Competitive (68–81) → Interview Ready (82–91) → Offer Ready (92–100).

## Browser support

| Feature | Chrome | Edge | Safari | Firefox |
|---|:-:|:-:|:-:|:-:|
| Question bank, frameworks, battlecard, readiness | ✅ | ✅ | ✅ | ✅ |
| Voice practice (Web Speech API) | ✅ | ✅ | ✅ | ❌ (graceful fallback: timer + reveal tabs) |

## Data & privacy

All progress — reviewed checkmarks, confidence ratings, logged evaluations — lives in the browser's **localStorage** under keys prefixed `eccles_projmgr_playbook_*`. Nothing is transmitted to any server. Storage is per-browser/per-device; clearing site data erases it. The keys are namespaced so this playbook does not collide with other Eccles playbooks (e.g., Product Management) hosted on the same domain.

Voice transcription uses the browser's built-in speech engine; the playbook stores only the session's text transcript, and only until the modal closes.

## Deployment

```
# It's one static file. Any of these works:
1. Push to a repo with GitHub Pages enabled (deploy from main / root).
2. Or drop the file into any static host.
3. Or open it locally — everything works offline except clipboard copy,
   which some browsers restrict on file:// pages.
```

No build, no `node_modules`, no external requests at runtime (fonts and libraries are not CDN-loaded; styles and logic are inline).

## Customizing the content

All content is plain data at the top of the inline `<script>` — no framework knowledge required:

- `PM_QUESTIONS` — the 100 question objects (`id`, `category`, `difficulty`, `question`, `conversational`, `deepdive`, `coaching`, `redFlag`). Categories and filter pills are derived automatically from this array.
- `PM_FRAMEWORKS`, `PM_BATTLECARD`, `PM_REDFLAGS` — the reference sections.
- `PM_RUBRIC` / `PM_TIERS` — scoring dimensions and tier thresholds (inside the app logic).

Editing rules: keep question `id`s sequential, use one of the three difficulty strings exactly, and avoid backticks or `${` inside the template-literal content fields.

## Documentation

See **`Project-Manager-Playbook-User-Manual.docx`** for the full user manual, including the practice workflow, rubric definitions, troubleshooting, and a suggested two-week study plan.

## Related playbooks

Part of the Eccles interview-prep series alongside the Product Management, Product Marketing, and Operations/Supply Chain playbooks — same architecture, role-specific content.

---

*Built for Eccles MBA candidates. Practice out loud — reasoning beats recall.*
