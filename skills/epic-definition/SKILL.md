---
name: epic-definition
description: Define an epic with strategic context, feature breakdown, milestones, and success metrics. Use when scoping a large body of work for planning and tracking.
---

# Epic Definition

Structure a well-defined epic in about an hour — strategic context, feature decomposition, milestones, dependencies, and success metrics. Claude handles the structuring and completeness checks. You provide the strategic intent and make the scoping calls.

## When to Use

- Breaking a PRD or initiative into an executable epic
- Kicking off a multi-sprint body of work that needs formal definition
- Multiple teams or stakeholders need visibility into a workstream
- Planning season requires epics tied to OKRs for roadmap alignment
- An existing epic is vague and needs to be tightened before engineering starts

## When NOT to Use

- The work fits in a single sprint — use Story Writing directly
- You need to write the full requirements first — use PRD Writing
- You're prioritizing which epic to do next — use RICE/ICE in FRAMEWORKS.md

## The AI-Native Approach

| Step | Time | Claude Does | You Do |
|---|---|---|---|
| Strategic framing | 10 min | Structure the objective, key result, and theme | Confirm alignment to company goals |
| Feature decomposition | 20 min | Break the epic into features with descriptions and owners | Validate completeness, cut scope |
| Success metrics | 10 min | Propose outcome metrics and guardrails | Confirm baselines and targets |
| Dependencies & risks | 10 min | Map cross-team dependencies and risk profile | Add political and organizational context |
| Timeline & milestones | 10 min | Propose phased milestones with feature groupings | Validate with engineering leads |

## Process

### Step 1: Strategic Framing (10 minutes)

Every epic exists to serve a goal. If you can't connect the epic to a company objective, question whether it belongs on the roadmap.

```
I need to define an epic for [body of work].

Strategic context:
- Objective: [what this epic achieves — tied to a company or product goal]
- Key result it drives: [measurable outcome — e.g., "Reduce onboarding drop-off from 40% to 25%"]
- Theme: [product pillar — e.g., Growth, Retention, Platform, Compliance]

Problem it addresses:
- [The user or business problem, grounded in evidence]

Evidence:
- [Data point 1 — source, date]
- [Data point 2]

Help me frame this as a tight epic description — one paragraph that any stakeholder could read and understand why we're investing in this.
```

### Step 2: Feature Decomposition (20 minutes)

Break the epic into independently deliverable features. Each feature should be meaningful on its own — not just a task.

```
Break this epic into features:

For each feature:
- Name and one-line description
- Why it's included (what problem it solves within the epic)
- Status: Not Started | In Design | In Development | Complete
- Owner: [name or team]
- Rough size: S / M / L
- Can it ship independently? (yes = good feature boundary)

Then:
- What's explicitly out of scope for this epic?
- Are any features dependent on each other? (must Feature A ship before Feature B?)
- Which feature delivers the most value fastest? (candidate for first delivery)
```

### Step 3: Success Metrics (10 minutes)

```
Define success metrics for this epic:

| Metric | Target | Baseline | Measurement Method |
|---|---|---|---|
| [Primary outcome metric] | [target] | [current] | [how measured] |
| [Secondary metric] | [target] | [current] | [how measured] |
| [Guardrail — must not degrade] | [threshold] | [current] | [how measured] |

How do we know this epic succeeded vs. just shipped?
What's our evaluation timeline after the last feature ships?
```

### Step 4: Dependencies & Risks (10 minutes)

```
Map dependencies and risks for this epic:

Dependencies:
| Dependency | Team/System | Status | Needed By |
|---|---|---|---|
| [What we need] | [from whom] | [resolved/pending] | [date] |

Risks:
| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| [What could go wrong] | [H/M/L] | [H/M/L] | [What we'd do] |

Flag any dependency that is unresolved and could block the first milestone.
```

### Step 5: Timeline & Milestones (10 minutes)

```
Propose a phased timeline for this epic:

| Milestone | Target Date | Features Included | What's Demoable |
|---|---|---|---|
| [e.g., "Design complete"] | [Date] | [Features 1-2] | [What stakeholders can see] |
| [e.g., "Beta launch"] | [Date] | [Feature 1] | [What users can do] |
| [e.g., "GA launch"] | [Date] | [All features] | [Full experience] |

For each milestone: what's the minimum viable deliverable?
Which milestone de-risks the most uncertainty?
```

## Output

- Epic description with strategic alignment
- Feature breakdown table with owners, sizes, and dependencies
- Success metrics with baselines and targets
- Dependency map and risk register
- Phased milestone timeline

## Common Pitfalls

1. **Epics without outcomes.** "Build notification system" is an output. "Reduce notification-driven churn by 15%" is an outcome. Tie the epic to a measurable result.
2. **Features that can't ship alone.** If a feature only makes sense when combined with three other features, it's not a feature — it's a task. Redraw the boundaries.
3. **No explicit scope boundary.** An epic without an out-of-scope section will grow until it collapses under its own weight. Define the edges early.
4. **Missing the first deliverable.** If the first milestone is 8 weeks away, the epic is too big or the milestones aren't granular enough. Aim for something demoable within 2 weeks.
5. **Orphan epics.** An epic that doesn't connect to an OKR or company goal will lose priority the moment something urgent arrives. Anchor it.

## Related Skills

- [PRD Writing](../prd-writing/SKILL.md) — when you need the full requirements before defining the epic
- [Feature Specification](../feature-specification/SKILL.md) — for detailed specs on individual features within the epic
- [Story Writing](../story-writing/SKILL.md) — for breaking features into developer-ready stories
- [Roadmap Planning](../roadmap-planning/SKILL.md) — for sequencing epics across a quarter or half
- Reference: [TEMPLATES.md](../../TEMPLATES.md) — Epic template for formatting
