---
name: business-case
description: Build a complete business case for a product investment — strategic rationale, financial model, risk assessment, and recommendation. Use when you need executive approval for a major initiative.
---

# Business Case

Build a compelling, rigorous business case for a product investment in 2-4 hours. This goes beyond pure financial analysis to include strategic alignment, market context, risk assessment, alternatives considered, and an implementation plan. Claude structures the case and runs the numbers. You provide the strategic judgment and organizational context that makes the case persuasive.

## When to Use

- Requesting significant budget, headcount, or resources for a new initiative
- Annual or quarterly planning requires formal investment proposals
- Expanding into a new market, segment, or product line
- A major platform investment needs executive sign-off
- You need to justify continuing (or killing) a significant existing investment
- Board or C-suite review requires a structured proposal

## When NOT to Use

- You only need the financial model — use Financial Analysis
- You're comparing build vs. buy — use Build vs. Buy (it includes its own business case structure)
- You're communicating tech debt specifically — use Tech Debt Communication
- The investment is small enough that an informal pitch or Slack message suffices

## The AI-Native Approach

| Step | Time | Claude Does | You Do |
|---|---|---|---|
| Frame the opportunity | 20 min | Structure the strategic rationale and market context | Provide the insight and evidence that sparked this |
| Model the economics | 30 min | Build financial model with ROI, NPV, scenarios | Validate assumptions with finance and engineering |
| Assess alternatives | 20 min | Structure option comparison with trade-offs | Add the options you've already considered and ruled out |
| Map risks and dependencies | 20 min | Categorize risks and propose mitigations | Add organizational and political risks |
| Assemble the case | 30 min | Draft the complete business case document | Review, add executive context, rehearse the pitch |

## Process

### Step 1: Frame the Opportunity (20 minutes)

A business case that starts with "we should build X" has already lost. Start with the opportunity or problem, then build to the proposal.

```
I need to build a business case for [initiative].

The opportunity:
- What's the problem or opportunity? [describe in business terms, not technical]
- Who does it affect? [customers, internal teams, the market]
- How big is it? [TAM, affected users, revenue at stake, cost impact]
- Why now? [what changed — market shift, customer demand, competitive pressure, regulatory deadline]

Strategic alignment:
- Which company goal or strategic pillar does this support?
- How does this fit with our product vision and roadmap?
- What happens if we don't do this? [cost of inaction]

Evidence:
- Customer evidence: [feedback, churn data, win/loss, NPS]
- Market evidence: [competitor moves, analyst reports, industry trends]
- Internal evidence: [operational costs, team productivity, system limitations]

Help me frame this as a compelling strategic narrative — not "we should build X" but "here's the opportunity, here's what's at stake, and here's how we capture it."
```

### Step 2: Model the Economics (30 minutes)

```
Build a financial model for this business case:

Investment required:
- One-time costs: [development, design, infrastructure setup, migration]
- Recurring costs: [maintenance, hosting, support, licensing]
- People costs: [headcount needed — new hires or reallocation]
- Timeline: [phases and when costs are incurred]

Expected returns:
- Revenue impact: [new revenue, retained revenue, expansion revenue]
- Cost impact: [savings, efficiency gains, avoided costs]
- Risk impact: [compliance, security, technical risk reduction]
- Strategic impact: [market position, competitive advantage — quantify where possible]

Model over [3 / 5] years. Calculate:
- Year-by-year cash flow (investment vs. returns)
- ROI, NPV (at [discount rate]%), IRR, payback period
- Break-even point
- Three scenarios: conservative, base, optimistic

For each assumption: state it explicitly, rate confidence (H/M/L), and note the source.
```

### Step 3: Assess Alternatives (20 minutes)

Executives don't just ask "should we do this?" They ask "compared to what?"

```
Evaluate alternatives to this investment:

Option 1: Do nothing (status quo)
- What happens over the next [1-3 years] if we don't act?
- Quantify the cost of inaction (lost revenue, increasing costs, growing risk)

Option 2: [The proposed investment — your recommendation]
- Summary of investment and expected returns from Step 2

Option 3: [Lighter alternative — partial investment, phased approach, or partner]
- What would a scaled-down version look like?
- What do we give up vs. the full investment?
- Financial model for this option

Option 4: [Different approach — alternative solution to the same problem]
- How else could we address this opportunity?
- What are the trade-offs?

Comparison matrix:
| Criteria | Do Nothing | Full Investment | Lighter Option | Alternative |
|---|---|---|---|---|
| 3-year NPV | | | | |
| Time to value | | | | |
| Risk level | | | | |
| Strategic fit | | | | |
| Reversibility | | | | |

Recommended option and why.
```

### Step 4: Map Risks and Dependencies (20 minutes)

```
Identify risks and dependencies for the recommended option:

Execution risks:
- Can we actually build this? (technical feasibility, team capability)
- Can we build it on time? (historical accuracy of our estimates)
- Do we have the right people? (hiring risk, key-person dependency)

Market risks:
- Could the opportunity disappear? (market shift, regulation change)
- Could a competitor get there first? (competitive timing)
- Could customer demand be overstated? (validation risk)

Financial risks:
- What if costs overrun? (model impact at 25%, 50%, 100% overrun)
- What if returns are lower? (break-even assumption analysis)
- What if timeline slips? (delayed revenue impact)

Organizational risks:
- Dependencies on other teams or initiatives
- Political or cultural barriers to adoption
- Change management requirements

For each risk:
| Risk | Probability | Impact | Mitigation | Owner |
|---|---|---|---|---|
| [Risk] | [H/M/L] | [H/M/L] | [What we'd do] | [Who owns it] |

What's our exit strategy if this doesn't work? At what point do we cut losses?
```

### Step 5: Assemble the Case (30 minutes)

```
Draft the complete business case:

1. Executive summary (half page max):
   - The opportunity in one sentence
   - The ask: [investment amount, timeline, resources]
   - The return: [headline financial metric — e.g., "3.2x ROI over 3 years"]
   - The risk if we don't act

2. Strategic context:
   - Opportunity description and evidence
   - Market and competitive landscape
   - Alignment to company strategy

3. Proposed solution:
   - What we're proposing (scope and approach)
   - Why this approach vs. alternatives
   - Implementation timeline and milestones

4. Financial model:
   - Investment summary
   - Returns model (year-by-year)
   - Key metrics: ROI, NPV, IRR, payback
   - Scenario analysis (conservative / base / optimistic)

5. Alternatives considered:
   - Comparison matrix
   - Why the recommended option wins

6. Risk assessment:
   - Top 5 risks with mitigations
   - Exit criteria

7. Ask:
   - Specific decision needed
   - Resources required
   - Decision deadline
   - Success milestones (when to check if it's working)

Format for [presentation / document / memo] for [audience].
```

## Output

- Strategic opportunity framing with evidence
- Financial model with ROI, NPV, IRR, payback, and scenarios
- Alternatives comparison matrix
- Risk assessment with mitigations
- Complete business case document ready for executive review

## Common Pitfalls

1. **Leading with the solution.** Executives care about the opportunity and the return, not your preferred technical approach. Lead with the "why" and the numbers. The "how" is supporting detail.
2. **No "do nothing" option.** Every business case should quantify what happens if we don't invest. Sometimes the cost of inaction is the most persuasive argument.
3. **Ignoring alternatives.** If you only present one option, it looks like you've already decided and are looking for rubber-stamp approval. Show that you considered alternatives and explain why this option wins.
4. **Optimism bias on timeline.** Software projects are historically late. Use your actual track record for estimates, not your hopes. If you've never shipped on time, don't model as if you will this time.
5. **No exit criteria.** Every investment should have a "if we see X by date Y, we continue; if not, we reassess" checkpoint. This builds confidence that you're not asking for a blank check.
6. **Death by appendix.** The executive summary should stand alone. If someone only reads the first page, they should understand the ask, the return, and the risk. Details go in appendices, not the narrative.

## Related Skills

- [Financial Analysis](../financial-analysis/SKILL.md) — for the detailed financial modeling that feeds into the business case
- [Stakeholder Alignment](../stakeholder-alignment/SKILL.md) — when the business case needs buy-in from competing priorities
- [Product Strategy & Vision](../product-strategy-vision/SKILL.md) — when the business case needs strategic context
- [Build vs. Buy](../build-vs-buy/SKILL.md) — when the business case involves a make-or-buy decision
