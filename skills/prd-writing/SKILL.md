---
name: prd-writing
description: Write a complete PRD from problem statement to builder-ready spec. Use when you need a formal product requirements document for a new initiative.
---

# PRD Writing

Turn a problem statement into a production-ready PRD in 1-2 hours instead of days. Claude handles the structure, boilerplate, edge case enumeration, and formatting. You provide the problem context, strategic framing, and the judgment calls about scope and trade-offs.

## When to Use

- Starting a new feature or initiative that needs formal documentation
- Leadership or governance requires a PRD before engineering can begin
- The scope is large enough that a user story isn't sufficient
- Multiple teams need to align on requirements before building
- You're handing off to engineers (or AI coding tools) and need an unambiguous spec

## When NOT to Use

- The work is small enough for a single user story — use Story Writing
- You need to validate whether the problem is worth solving first — use Discovery Process
- You're breaking down an approved PRD into buildable pieces — use Epic Definition or Story Writing

## The AI-Native Approach

| Step | Time | Claude Does | You Do |
|---|---|---|---|
| Frame the problem | 15 min | Structure problem statement from your raw input | Validate the framing, add evidence |
| Define success | 15 min | Propose metrics, baselines, and evaluation timeline | Confirm what "done" actually means |
| Scope the solution | 20 min | Draft v1/deferred/out-of-scope with trade-off rationale | Make the cut calls |
| Detail requirements | 30 min | Enumerate edge cases, error states, technical constraints | Validate with engineering |
| Assemble the PRD | 15 min | Format the complete document with all sections | Review and distribute |

## Process

### Step 1: Frame the Problem (15 minutes)

A PRD without a clear problem statement is a solution looking for a justification. Start here.

```
I need a PRD for [initiative]. Here's what I know:

The problem:
- Who is affected: [user segment]
- What they experience: [the pain in their words]
- How we know this: [evidence — data, support tickets, research, user quotes]
- What happens if we don't solve it: [business/user consequence]

Context:
- Strategic alignment: [which company goal or OKR this supports]
- Prior attempts: [what's been tried before, if anything]
- Urgency: [why now — is there a deadline, competitive pressure, or growing pain?]

Help me frame this as a crisp problem statement. Challenge me if the evidence is thin.
```

### Step 2: Define Success (15 minutes)

```
For this PRD, help me define success metrics:

Primary metric:
- What outcome are we trying to change? [metric]
- Current baseline: [number + source]
- Target: [number + rationale for why this target]
- Evaluation timeline: [when we assess — e.g., 30 days post-launch]

Secondary metrics:
- Supporting signals that indicate we're on track

Guardrail metrics:
- What must NOT degrade as a result of this change
- Thresholds for each guardrail

If we can't measure any of these today, flag it — we may need to instrument first.
```

### Step 3: Scope the Solution (20 minutes)

This is where lean discipline matters most. The default is to over-scope. Fight it.

```
Based on the problem and success metrics, help me scope the solution:

v1 — Ship this (minimum that tests the hypothesis):
- [Capability 1]
- [Capability 2]
- [Capability 3]

For each: why is it in v1? What would break if we cut it?

Deferred — Validated by v1 results:
- [Item] — ship if [trigger condition]

Out of scope — Explicitly not included:
- [Item] — why it's out (not "later," but "not this")

Questions to pressure-test scope:
- What's the smallest version that moves the primary metric?
- Are we bundling nice-to-haves with must-haves?
- If we had half the engineering time, what would we cut?
```

### Step 4: Detail Requirements (30 minutes)

This is where AI thoroughness adds the most value — catching the edge cases humans skip.

```
For the scoped solution, detail the requirements:

User stories:
- Draft user stories for each v1 capability with acceptance criteria
- Make every acceptance criterion testable

Edge cases and error states:
- What happens when [input is empty / invalid / extremely large]?
- What happens when [the user doesn't have permission]?
- What happens when [a dependency is unavailable]?
- What happens when [the user abandons mid-flow]?

Technical constraints:
- Platform/infrastructure constraints
- API contracts or integration requirements
- Performance requirements (latency, throughput, availability)
- Data and privacy requirements
- Accessibility requirements

Dependencies:
- What do we need from other teams, and by when?
- What are other teams waiting on from us?

Risks:
- What could go wrong? Likelihood, impact, and mitigation for each.
```

### Step 5: Assemble the PRD (15 minutes)

```
Assemble the complete PRD with these sections:

1. Problem Statement (who, what, evidence, impact)
2. Success Metrics (primary, secondary, guardrail, evaluation timeline)
3. Solution — Scope (v1, deferred, out of scope)
4. User Stories with Acceptance Criteria
5. Technical Constraints
6. Dependencies
7. Risks
8. Readiness Requirements (support FAQ, help docs, release notes, monitoring, rollback)

Format for [our documentation system — e.g., Confluence, Notion, Google Docs].
Include status field, author, engineering lead, design lead, and last updated date.
```

## Output

- Problem statement grounded in evidence
- Success metrics with baselines, targets, and evaluation timeline
- Scoped solution (v1 / deferred / out of scope)
- User stories with testable acceptance criteria
- Edge cases and error states enumerated
- Complete, formatted PRD ready for review

## Common Pitfalls

1. **Skipping the problem statement.** "We need dark mode" is not a problem statement. "Users report eye strain during evening use (34% of exit survey respondents)" is. The problem statement is the most important section — get it right.
2. **Vague acceptance criteria.** "The experience should be intuitive" is not testable. "The user can complete the flow in under 3 clicks without help text" is. If you can't write a test for it, rewrite it.
3. **Scope creep disguised as completeness.** A PRD for a single feature shouldn't be 10 pages. Every section should earn its place. If the team already knows the context, cut the background.
4. **Missing the "not doing" list.** An explicit out-of-scope section prevents scope creep during development. If it's not listed as out of scope, someone will assume it's in scope.
5. **No readiness requirements.** A PRD that doesn't include support FAQ, help docs, and monitoring requirements means those get rushed at launch. Include them upfront.

## Related Skills

- [Epic Definition](../epic-definition/SKILL.md) — when the PRD needs to be broken into epics for execution
- [Story Writing](../story-writing/SKILL.md) — for detailed story-level requirements within the PRD
- [Discovery Process](../discovery-process/SKILL.md) — when you need to validate the problem before writing the PRD
- Reference: [TEMPLATES.md](../../TEMPLATES.md) — PRD template for formatting
