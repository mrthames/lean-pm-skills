---
name: analytics-insights
description: Deep dive into product analytics — investigate a question, surface insights, build a data narrative. Use when you need to go beyond dashboards to understand what's happening.
---

# Analytics & Insights

Go beyond dashboards to answer a specific product question in 1-2 hours. Claude helps you structure the investigation, identify the right cuts of data, spot patterns, and build a narrative that drives action. You provide the product context that turns numbers into meaning.

## When to Use

- You have a specific question that your dashboards don't answer
- A metric moved and you need to understand why
- You're building a data-backed case for a product decision
- Leadership asked "what are the numbers telling us?" and you need depth, not a screenshot
- You need to segment data to understand different user behaviors
- Pre-launch baseline analysis or post-launch impact measurement

## When NOT to Use

- You're doing a routine weekly check — use Metrics Review
- You're diagnosing a specific churn or retention problem — use Growth & Retention Diagnostics
- You need to design an experiment — use Experiment Design

## The AI-Native Approach

| Step | Time | Claude Does | You Do |
|---|---|---|---|
| Frame the question | 10 min | Sharpen vague questions into specific, answerable investigations | Provide the business context and what decisions hinge on this |
| Design the analysis | 15 min | Identify metrics, segments, time ranges, and comparison groups | Confirm data availability and source reliability |
| Analyze the data | 30 min | Structure the analysis, spot patterns, flag anomalies | Provide the actual data, add qualitative context |
| Build the narrative | 20 min | Draft audience-specific narrative with insights and recommendations | Validate interpretation, add "so what" and "now what" |

## Process

### Step 1: Frame the Question (10 minutes)

Vague questions get vague answers. Start by making the question specific enough to answer with data.

```
I need to investigate: [vague question — e.g., "How are users engaging with the new feature?"]

Help me sharpen this into specific, answerable questions:

For each question:
- What metric answers this?
- What segments matter? (user type, cohort, geography, plan tier, etc.)
- What time range is relevant?
- What comparison would be meaningful? (before/after, segment A vs. B, us vs. benchmark)
- What would a "good" answer look like? What would a "bad" answer look like?

What decision will this analysis inform?
What would we do differently based on what we find?
```

### Step 2: Design the Analysis (15 minutes)

```
For each question, design the analysis:

Data needed:
- Metric: [what we're measuring]
- Source: [where the data lives — analytics tool, database, export]
- Segments: [how to cut the data]
- Time range: [start, end, comparison period]
- Granularity: [daily, weekly, monthly]

Analysis approach:
- Trend analysis: how has this metric changed over time?
- Segment comparison: how do different user groups behave?
- Cohort analysis: how do users who started at different times compare?
- Funnel analysis: where are users dropping off?
- Correlation: what other metrics move with this one?

Known limitations:
- Data quality issues to watch for
- Segments that are too small for meaningful comparison
- External factors that could confound the analysis
```

### Step 3: Analyze the Data (30 minutes)

```
Here's the data: [paste data, describe charts, or share exports]

Analyze:
- What's the headline? (one sentence summary of the finding)
- What patterns are visible? (trends, seasonality, step changes)
- What anomalies stand out? (unexpected spikes, drops, or divergences)
- How do segments differ? (which groups behave differently, and how)
- What's statistically meaningful vs. just noise?

Dig deeper:
- Can we identify a root cause or contributing factor?
- Is this a one-time event or a structural change?
- What would we need to investigate further to be confident?

Flag:
- Where the data is strong (large sample, clean measurement)
- Where the data is weak (small sample, proxy metric, known instrumentation issues)
- What we still don't know
```

### Step 4: Build the Narrative (20 minutes)

Numbers don't drive action. Stories backed by numbers do.

```
Build an insights narrative for [audience — team, leadership, board]:

Structure:
1. The question we investigated and why it matters
2. Headline finding (one sentence — what did we learn?)
3. Supporting evidence (2-3 key data points with context)
4. What this means (interpretation — connect data to product/business impact)
5. What we should do (specific recommendation with expected impact)
6. What we don't know yet (gaps, caveats, next investigations)

Tone:
- For the team: detailed, include methodology, show your work
- For leadership: headline first, evidence second, ask/recommendation third
- For board: strategic frame, biggest number, trend direction, confidence level

Include:
- Data visualizations recommendations (what chart type best tells this story)
- Comparison context (benchmarks, historical, goals)
- Confidence level (how sure are we about this finding?)
```

## Output

- Sharpened investigation questions tied to decisions
- Analysis design with metrics, segments, and methodology
- Pattern analysis with anomaly detection and root cause hypotheses
- Audience-specific narrative with insights and recommendations

## Common Pitfalls

1. **Answering the wrong question.** "How many users clicked the button?" is easy to answer but rarely useful. "Did the button change user behavior in a way that moves our success metric?" is the real question. Start with the decision, work backward to the data.
2. **Cherry-picking data.** It's tempting to highlight the metric that supports your thesis. Show the full picture — including the metrics that didn't move or moved the wrong way. Credibility comes from honesty.
3. **Confusing correlation with causation.** Two metrics moving together doesn't mean one caused the other. Be explicit about whether you're showing correlation, suggesting causation, or proving it with an experiment.
4. **Drowning in data.** More data doesn't mean better insights. Pick the 3-5 metrics that answer the question. Everything else is appendix material.
5. **Insights without action.** "Activation is down 5%" is an observation. "Activation is down 5% because new users aren't completing onboarding step 3 — we should investigate why and test a simplified flow" is an insight. Always end with "so what" and "now what."

## Related Skills

- [Metrics Review](../metrics-review/SKILL.md) — for routine weekly product health checks
- [Growth & Retention Diagnostics](../growth-retention-diagnostics/SKILL.md) — for specific churn/retention investigations
- [Experiment Design](../experiment-design/SKILL.md) — when the analysis surfaces a hypothesis worth testing
- [Stakeholder Alignment](../stakeholder-alignment/SKILL.md) — when the insights need to drive a cross-functional decision
