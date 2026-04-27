![Version](https://img.shields.io/badge/version-1.0.0-blue?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Claude Code](https://img.shields.io/badge/Claude_Code-Plugin-D97757?style=flat-square&logo=anthropic&logoColor=white)
![AI-Native](https://img.shields.io/badge/AI--Native_PM-ff6b35?style=flat-square)

# 🚀 Lean PM Skills for Claude Code

**AI-native product management skills that move at the speed your team needs.**

Compress the mechanical PM work — research synthesis, artifact generation, framework execution — so you can focus on what only a human PM can do: stakeholder relationships, strategic decisions, and understanding problems worth solving.

> 💡 **The philosophy:** Traditional PM frameworks are sound. Traditional PM timelines are not. Every skill in this plugin is designed for hours and days, not weeks and months. AI handles the first 80%. You handle the last 20% — the 20% that determines whether the product succeeds.

---

## 📦 Installation

### Claude Code Plugin (recommended)

```bash
/plugin install lean-pm-skills
```

### Manual — Just the Guidelines

```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/mrthames/lean-pm-skills/main/CLAUDE.md
```

### Full Clone — All Guides, Templates, and Skills

```bash
git clone https://github.com/mrthames/lean-pm-skills.git
```

<details>
<summary>🖱️ Cursor IDE Setup</summary>

```bash
mkdir -p .cursor/rules
cp lean-pm-skills/.cursor/rules/product-manager-guidelines.mdc .cursor/rules/
```

See [CURSOR.md](CURSOR.md) for details.

</details>

---

## 🛠️ Skills

### 🔍 Discovery & Strategy

| Skill | What It Does | Time |
|---|---|---|
| **[Discovery Process](skills/discovery-process/SKILL.md)** | Compressed discovery cycle — frame, research, interview, map, decide | 5 days |
| **[Product Strategy & Vision](skills/product-strategy-vision/SKILL.md)** | Craft a product vision, north star metric, and strategy-on-a-page | 2-4 hours |
| **[User Research Methods](skills/user-research-methods/SKILL.md)** | Plan and execute interviews, usability tests, or surveys with synthesis | 1-3 days |
| **[Pricing & Packaging](skills/pricing-packaging/SKILL.md)** | Value-based pricing analysis, tier design, and revenue modeling | 1-2 days |
| **[Build vs. Buy](skills/build-vs-buy/SKILL.md)** | Evaluate build in-house vs. vendor vs. partner with TCO analysis | Half day |

### ⚡ Execution & Delivery

| Skill | What It Does | Time |
|---|---|---|
| **[Sprint & Release Planning](skills/sprint-release-planning/SKILL.md)** | Break epics into stories, model capacity, sequence work, flag risks | 1 hour |
| **[OKR & Goal Setting](skills/okr-goal-setting/SKILL.md)** | Set quarterly OKRs — objectives, key results, alignment, stress-test | 2-3 hours |
| **[Go-to-Market Planning](skills/go-to-market-planning/SKILL.md)** | Build a GTM plan — messaging, channels, enablement, launch timeline | 1-2 days |
| **[Feature Sunset & EOL](skills/feature-sunset/SKILL.md)** | Plan and communicate a feature deprecation or product end-of-life | Half day |

### 🤝 Alignment & Communication

| Skill | What It Does | Time |
|---|---|---|
| **[Stakeholder Alignment](skills/stakeholder-alignment/SKILL.md)** | Get stakeholders aligned on a decision with a decision-forcing document | 2-4 hours |
| **[Tech Debt Communication](skills/tech-debt-communication/SKILL.md)** | Quantify and communicate tech debt as a business investment case | 2-4 hours |
| **[Competitive Response](skills/competitive-response/SKILL.md)** | Assess and respond to a competitor move within 24-48 hours | 2-4 hours |

### 📊 Operations & Analysis

| Skill | What It Does | Time |
|---|---|---|
| **[Metrics Review](skills/metrics-review/SKILL.md)** | Regular metrics review — spot patterns, flag anomalies, build the data narrative | 30 minutes |
| **[Growth & Retention Diagnostics](skills/growth-retention-diagnostics/SKILL.md)** | Diagnose churn and retention problems with cohort analysis and root cause identification | Half day |
| **[Post-Mortem](skills/post-mortem/SKILL.md)** | Structured, blameless post-mortem after a failure or incident | 2-3 hours |

---

## 💬 When Would I Use This?

Real scenarios. Real PM problems. Here's how Lean PM Skills helps you move faster.

### 🔍 "We have a hypothesis but I don't know if this problem is worth solving."

You've heard the signal from customers, sales, or support — but you're not sure it's real. Traditionally, this means a 3-8 week discovery process: scheduling interviews, synthesizing feedback, mapping the opportunity space, and building a recommendation.

**With Lean PM Skills:** The [Discovery Process](skills/discovery-process/SKILL.md) compresses this into a 5-day cycle. Claude helps you frame the problem on Day 1, synthesize existing research on Day 2, prepare and debrief interviews on Day 3, map the opportunity space on Day 4, and build a build/validate/kill recommendation on Day 5. You still talk to real users — AI just eliminates the weeks of synthesis work between conversations.

**What you get:** Problem framing document, research synthesis, interview guides, opportunity map, and a decision recommendation with supporting evidence.

---

### 🏛️ "Three VPs want three different things and I need alignment by Friday."

Every PM has been here. Competing priorities, unclear decision criteria, and a meeting on the calendar where someone needs to say yes or no. The traditional approach — back-channel conversations, lengthy slide decks, consensus-building over weeks — doesn't fit when you need a decision now.

**With Lean PM Skills:** [Stakeholder Alignment](skills/stakeholder-alignment/SKILL.md) helps you build a stakeholder map, draft a decision-forcing document that makes the trade-offs explicit, pre-empt the most likely objections, and prepare a decision memo — all in a 2-4 hour focused session. You walk into the room with a clear recommendation and the analysis to back it up.

**What you get:** Stakeholder map with positions and concerns, decision-forcing document, objection responses, and a decision memo ready for sign-off.

---

### 📉 "Churn went up 2 points this quarter and nobody can tell me why."

The dashboard is red but the explanations are vague. Is it onboarding? Is it a specific segment? Is it a competitor? The traditional approach means weeks of pulling data, scheduling deep dives with analytics, and chasing down anecdotes.

**With Lean PM Skills:** [Growth & Retention Diagnostics](skills/growth-retention-diagnostics/SKILL.md) gives you a structured diagnostic framework in half a day. Claude helps you design the cohort analysis, identify which segments are driving the change, build a root cause hypothesis tree, and design interventions — while you provide the product context and customer knowledge that data alone can't surface.

**What you get:** Cohort analysis framework, segment-level diagnosis, root cause tree, and a prioritized retention intervention plan.

---

### 🚀 "We're launching in 4 weeks and we don't have a GTM plan."

The feature is almost done. Marketing wants messaging. Sales wants enablement. Support wants docs. Leadership wants a timeline. And nobody has coordinated any of it.

**With Lean PM Skills:** [Go-to-Market Planning](skills/go-to-market-planning/SKILL.md) helps you build the full GTM package in 1-2 days: messaging framework, channel strategy, sales enablement materials, support preparation, and a week-by-week launch timeline. Claude generates the structure and drafts; you add the market knowledge and relationship context.

**What you get:** Messaging framework, channel strategy, enablement materials, support documentation, and a phased launch timeline.

---

### ⚔️ "A competitor just dropped a feature that undercuts our main value prop."

Your Slack is blowing up. Sales is asking for talking points. Your VP wants a response by end of day. The traditional approach — schedule a competitive analysis sprint, convene a cross-functional working group — takes weeks you don't have.

**With Lean PM Skills:** [Competitive Response](skills/competitive-response/SKILL.md) helps you assess the move, evaluate your response options, draft sales talking points, and prepare a leadership brief — all in 2-4 hours. Claude does the rapid analysis while you apply the strategic judgment about what this actually means for your product and customers.

**What you get:** Competitive impact assessment, response options with trade-offs, sales talking points, and an executive brief.

---

### 🗓️ "Sprint planning is tomorrow and I haven't broken down the epic."

It's Sunday night. Tomorrow's sprint planning. The epic is clear in your head but it's one big block in the backlog with no stories, no acceptance criteria, and no dependency map.

**With Lean PM Skills:** [Sprint & Release Planning](skills/sprint-release-planning/SKILL.md) takes you from epic to sprint-ready in about an hour. Claude helps you break the epic into user stories with acceptance criteria, model team capacity, map dependencies, and identify the scope trade-offs you'll need to discuss with the team.

**What you get:** Broken-down stories with acceptance criteria, capacity model, dependency map, and scope trade-off recommendations.

---

### 💸 "We need to set pricing for the new enterprise tier."

Pricing decisions have huge leverage — and most teams spend either way too long or way too little time on them. The traditional approach involves weeks of competitive analysis, value metric identification, willingness-to-pay research, and financial modeling.

**With Lean PM Skills:** [Pricing & Packaging](skills/pricing-packaging/SKILL.md) compresses this into 1-2 days. Claude helps you identify value metrics, build a competitive pricing matrix, design tier structures, and model revenue scenarios — while you bring the customer knowledge and strategic context about where your product sits in the market.

**What you get:** Value metric analysis, competitive pricing matrix, tier design options, and revenue scenario models.

---

### 🔧 "Engineering wants to spend two sprints on tech debt and leadership wants justification."

The engineers are frustrated. The codebase is slowing them down. But "we need to refactor" doesn't get budget. Leadership wants to know the business impact.

**With Lean PM Skills:** [Tech Debt Communication](skills/tech-debt-communication/SKILL.md) helps you translate technical debt into a business investment case in 2-4 hours. Claude helps you quantify the velocity impact, calculate the risk exposure, frame the opportunity cost of not investing, and build a recommendation that speaks leadership's language — revenue, risk, and speed.

**What you get:** Business-framed investment case with velocity impact, risk quantification, opportunity cost analysis, and a specific recommendation.

---

### 📊 "What story are our metrics telling this week?"

You have dashboards. You have data. But turning numbers into a narrative that drives action takes time — and it's easy to miss the signal in the noise.

**With Lean PM Skills:** [Metrics Review](skills/metrics-review/SKILL.md) gives you a structured 30-minute weekly review process. Claude helps you pull the key metrics, spot trends and anomalies, compare against targets, and draft audience-specific narratives — whether you're updating your team, your VP, or your board.

**What you get:** Structured metrics review with trends, anomalies, target comparison, and audience-ready narrative.

---

### 😬 "That launch did not go well. What happened?"

Something went wrong — missed targets, quality issues, user backlash, or a full-on incident. The team needs to learn from it, but post-mortems often devolve into blame games or produce action items nobody follows up on.

**With Lean PM Skills:** [Post-Mortem](skills/post-mortem/SKILL.md) structures a blameless post-mortem in 2-3 hours. Claude builds the timeline from your notes, categorizes contributing factors objectively, extracts lessons, and drafts 3-5 specific, owned, time-bound action items. You facilitate the conversation and ensure the team actually learns.

**What you get:** Chronological timeline, contributing factors analysis, prioritized lessons, and 3-5 actionable follow-ups with owners and deadlines.

---

## 🧠 How It Works

Every skill follows the same model:

```
┌─────────────────────────────────────────────┐
│  🤖 AI handles the first 80%               │
│  Structure, research, drafts, frameworks    │
├─────────────────────────────────────────────┤
│  🧑 You handle the last 20%                │
│  Judgment, context, relationships, decisions│
└─────────────────────────────────────────────┘
```

This applies across all three disciplines in AI-native product development:

- 🎯 **Product managers** use AI for artifacts and analysis, own the decisions
- 🛠️ **Engineers** use AI for implementation, own the architecture and quality
- 🎨 **Designers** use AI for exploration, own the user experience

No AI-generated artifact should leave your hands without your judgment applied.

---

## 📚 Reference Guides

| Document | What It Is |
|---|---|
| **[CLAUDE.md](CLAUDE.md)** | Core behavioral guidelines — always loaded, governs how Claude operates as your PM partner |
| **[GETTING-STARTED.md](GETTING-STARTED.md)** | Your first session — from setup to producing a real artifact in 15 minutes |
| **[FRAMEWORKS.md](FRAMEWORKS.md)** | PM frameworks adapted for AI-native speed — JTBD, RICE, Kano, story splitting, SaaS metrics |
| **[TEMPLATES.md](TEMPLATES.md)** | Artifact templates — PRDs, epics, features, stories, experiments, stakeholder updates, readiness checklists |
| **[AGENTIC-WORKFLOWS.md](AGENTIC-WORKFLOWS.md)** | Autonomous agents on a cadence — competitive intel, analytics, feedback monitoring, and more |
| **[AI-NATIVE-WORKFLOW.md](AI-NATIVE-WORKFLOW.md)** | How PM changes when your whole team uses AI — handoffs, readiness, enterprise tooling |
| **[EXAMPLES.md](EXAMPLES.md)** | Before/after demonstrations of each core principle |

---

## ✅ Core Principles

1. **Start With the Problem, Not the Solution** — Ground every artifact in the user problem and evidence
2. **Write for Builders** — Specs should be unambiguous and directly actionable by engineers and designers
3. **Define Done Before Starting** — Measurable success criteria before work begins
4. **Scope Ruthlessly** — Ship the smallest thing that tests the hypothesis
5. **Stay Evidence-Based** — Distinguish between what data says, what it suggests, and what is assumption

---

<details>
<summary>🤝 Contributing</summary>

To add a new skill, create `skills/<skill-name>/SKILL.md` following the format in existing skills:

```
---
name: skill-name
description: One-line trigger description (under 200 chars)
---
# Title
## When to Use / When NOT to Use
## The AI-Native Approach
## Process (stepped, with prompt examples)
## Output
## Common Pitfalls
## Related Skills
```

When updating behavioral guidelines, keep these in sync:
- `CLAUDE.md` — Full guidelines
- `.cursor/rules/product-manager-guidelines.mdc` — Cursor rules (condensed)

</details>

---

## 📄 License

MIT
