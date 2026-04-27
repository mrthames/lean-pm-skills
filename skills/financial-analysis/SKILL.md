---
name: financial-analysis
description: Run ROI, IRR, NPV, payback period, and cost-benefit analysis for product investments. Use when you need to quantify the financial case for building something.
---

# Financial Analysis

Quantify the financial case for a product investment using the methods finance teams and executives actually use — ROI, IRR, NPV, payback period, and cost-benefit analysis. Claude runs the models and sensitivity analysis. You provide the assumptions and defend the numbers.

## When to Use

- Leadership wants to know the ROI of a proposed initiative
- You're competing for budget against other teams' proposals
- Finance requires a business case before approving headcount or spend
- You need to compare two investment options on a financial basis
- Quarterly or annual planning requires investment justification
- A build-vs-buy decision needs financial modeling beyond TCO

## When NOT to Use

- You're comparing build vs. buy holistically (not just financially) — use Build vs. Buy
- You need to set pricing — use Pricing & Packaging
- You're communicating tech debt cost — use Tech Debt Communication (though it may reference this skill)

## The AI-Native Approach

| Step | Time | Claude Does | You Do |
|---|---|---|---|
| Define the investment | 15 min | Structure costs, timeline, and assumptions | Provide estimates, validate with finance/engineering |
| Model the returns | 20 min | Calculate revenue impact, cost savings, risk reduction | Validate assumptions about adoption, conversion, retention |
| Run financial metrics | 15 min | Calculate ROI, IRR, NPV, payback period | Choose discount rate and time horizon with finance |
| Sensitivity analysis | 15 min | Model best/base/worst scenarios, identify key variables | Decide which assumptions to stress-test |
| Build the case | 15 min | Draft investment summary for leadership/finance | Review numbers, add strategic context |

## Process

### Step 1: Define the Investment (15 minutes)

```
I need to build a financial case for [initiative].

Investment costs:
- Development: [engineering headcount × duration, or contractor cost]
- Design: [design resources needed]
- Infrastructure: [hosting, tooling, third-party services]
- Opportunity cost: [what the team can't build while building this]
- Ongoing maintenance: [annual cost to keep it running — typically 15-20% of build cost]
- Other: [training, migration, change management]

Timeline:
- Build duration: [weeks/months]
- Time to first value: [when does the investment start generating returns?]
- Full value realization: [when does it reach steady-state impact?]
- Analysis horizon: [1 year / 2 years / 3 years / 5 years]

Help me structure all costs into a year-by-year cash flow model.
Distinguish between one-time costs and recurring costs.
```

### Step 2: Model the Returns (20 minutes)

This is where most financial cases are won or lost — the quality of your return assumptions.

```
Model the financial returns for this investment:

Revenue impact:
- New revenue: [new customers, upsells, or expansion enabled by this]
  - Estimated new ARR: [amount] with [adoption rate] assumption
- Revenue retention: [churn prevented, renewals saved]
  - At-risk ARR: [amount] with [save rate] assumption
- Revenue acceleration: [faster sales cycles, higher conversion rates]
  - Current conversion: [rate] → projected: [rate]

Cost savings:
- Operational efficiency: [manual work eliminated, headcount avoided]
  - Hours saved per [week/month]: [amount] × loaded cost per hour
- Infrastructure savings: [reduced hosting, vendor consolidation]
- Support cost reduction: [ticket volume reduction, faster resolution]

Risk reduction (quantify where possible):
- Compliance: [cost of non-compliance × probability]
- Security: [breach cost × probability reduction]
- Technical: [outage cost × frequency reduction]

For each return:
- What's the assumption behind this number?
- How confident are we? (high / medium / low)
- When does this return start? (month/quarter after launch)
- Does it grow over time or stay flat?
```

### Step 3: Run Financial Metrics (15 minutes)

```
Calculate the following financial metrics from the cash flow model:

1. ROI (Return on Investment):
   Formula: (Net returns - Total investment) / Total investment × 100
   Calculate for: 1-year, 2-year, 3-year horizons
   
2. NPV (Net Present Value):
   Discount rate: [company's WACC or hurdle rate — typically 8-15%]
   Calculate the present value of all future cash flows minus the initial investment
   Interpretation: positive NPV = investment creates value

3. IRR (Internal Rate of Return):
   The discount rate that makes NPV = 0
   Interpretation: if IRR > hurdle rate, the investment is financially justified

4. Payback Period:
   How many months until cumulative returns exceed cumulative investment
   Both simple payback and discounted payback

5. Cost-Benefit Ratio:
   Total discounted benefits / Total discounted costs
   Interpretation: ratio > 1.0 = benefits exceed costs

Present as a summary table with all five metrics.
Include the year-by-year cash flow model showing investment, returns, cumulative, and discounted values.
```

### Step 4: Sensitivity Analysis (15 minutes)

Every financial model is only as good as its assumptions. Show what happens when they're wrong.

```
Run sensitivity analysis on the financial model:

Three scenarios:
- Best case: [optimistic but defensible assumptions]
- Base case: [most likely assumptions — use this as the primary case]
- Worst case: [pessimistic but plausible assumptions]

For each scenario, recalculate: ROI, NPV, IRR, payback period

Key variable sensitivity:
For each critical assumption, show the impact of ±20% variance:
- Adoption rate: what if 20% higher / lower?
- Development timeline: what if it takes 50% longer?
- Revenue per customer: what if 20% higher / lower?
- Churn impact: what if save rate is 20% higher / lower?

Identify:
- Break-even assumptions: at what point does NPV go negative?
- The single variable that swings the model the most
- Which assumptions we should validate before committing
```

### Step 5: Build the Case (15 minutes)

```
Draft an investment summary for [audience — leadership / finance / board]:

1. Investment overview: what we're proposing and why (2-3 sentences)
2. Total investment: [amount] over [timeline]
3. Expected returns: [primary return driver and magnitude]
4. Financial metrics summary table (ROI, NPV, IRR, payback)
5. Scenario analysis table (best / base / worst)
6. Key assumptions and confidence levels
7. Key risks and what changes the math
8. Recommendation: invest / don't invest / invest with conditions
9. Decision needed by: [date]

Tone: quantitative, honest about uncertainty, focused on the decision.
Lead with the headline number. Support with the model. Acknowledge the risks.
```

## Output

- Year-by-year cash flow model (investment and returns)
- Financial metrics: ROI, NPV, IRR, payback period, cost-benefit ratio
- Three-scenario sensitivity analysis
- Key assumption register with confidence levels
- Investment summary document for leadership or finance

## Common Pitfalls

1. **Inflated return assumptions.** The most common way to get a project approved and then miss targets. Be conservative on returns and specific about assumptions. Finance will challenge vague numbers.
2. **Ignoring opportunity cost.** The team building this can't build something else. Include the value of the next-best alternative as a cost.
3. **Forgetting ongoing costs.** Build cost is one-time. Maintenance, infrastructure, and support are forever. Model the full lifecycle, not just the build.
4. **Single-scenario thinking.** A model with one set of assumptions is a guess. Three scenarios with sensitivity analysis is a decision framework. Always show the range.
5. **NPV without context.** Positive NPV doesn't mean "do it." It means "this creates value at the assumed discount rate." If another initiative has higher NPV for the same investment, that's the better bet. Always compare against alternatives.
6. **Precision theater.** A model showing $1,247,832.47 in Year 3 returns implies false precision. Round to meaningful figures and focus on the order of magnitude and the direction.

## Related Skills

- [Build vs. Buy](../build-vs-buy/SKILL.md) — when the financial analysis is part of a make-or-buy decision
- [Tech Debt Communication](../tech-debt-communication/SKILL.md) — when quantifying the cost of not investing in infrastructure
- [Business Case](../business-case/SKILL.md) — when you need the full business case beyond just the financials
- [Pricing & Packaging](../pricing-packaging/SKILL.md) — when the financial model feeds into pricing decisions
