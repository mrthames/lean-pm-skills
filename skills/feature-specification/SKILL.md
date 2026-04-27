---
name: feature-specification
description: Write a detailed feature spec with requirements, edge cases, and technical constraints. Use when a feature needs formal documentation before engineering begins.
---

# Feature Specification

Detail a feature from concept to builder-ready spec in 30-60 minutes. Claude enumerates the requirements, edge cases, error states, and integration points that humans typically miss. You provide the user context and make the trade-off calls on complexity vs. value.

## When to Use

- A feature within an epic needs detailed specification before development
- Engineers or AI coding tools need unambiguous requirements to start building
- The feature touches multiple systems and needs explicit integration requirements
- Design and engineering need a shared reference for what "done" looks like
- A feature is being handed off to another team or contractor

## When NOT to Use

- The work is small enough for a single user story — use Story Writing
- You need the full initiative-level document — use PRD Writing
- You're defining the strategic wrapper around multiple features — use Epic Definition

## The AI-Native Approach

| Step | Time | Claude Does | You Do |
|---|---|---|---|
| Define the feature | 10 min | Structure the feature description, user value, and context | Confirm the framing matches intent |
| Detail requirements | 15 min | Draft functional and non-functional requirements | Validate with engineering, flag unknowns |
| Enumerate edge cases | 10 min | Systematically identify edge cases and error states | Decide which to handle in v1 vs. defer |
| Define acceptance criteria | 10 min | Write testable acceptance criteria for each requirement | Confirm they match what "done" means |
| Document integration points | 10 min | Map API contracts, data flows, and system dependencies | Verify with engineering leads |

## Process

### Step 1: Define the Feature (10 minutes)

```
I need to spec out a feature: [feature name]

Context:
- Epic it belongs to: [epic name/link]
- User segment: [who uses this]
- User value: [what job it does for the user — in their words]
- Business value: [why the business cares]

Current state:
- What exists today: [current experience or workaround]
- What changes: [what's new or different]

Constraints known upfront:
- [Technical constraints, platform limitations, compliance requirements]
- [Timeline constraints — when does this need to ship?]
```

### Step 2: Detail Requirements (15 minutes)

```
Draft the requirements for this feature:

Functional requirements (what it must do):
- [Requirement 1] — [why]
- [Requirement 2] — [why]
- [Requirement 3] — [why]

For each requirement, specify:
- Input: what triggers this behavior
- Output: what the user sees or what the system does
- Rules: business logic, validation, calculations

Non-functional requirements:
- Performance: [latency, throughput targets]
- Scale: [expected usage volume, growth projections]
- Security: [authentication, authorization, data handling]
- Accessibility: [WCAG level, specific accommodations]
- Compatibility: [browsers, devices, OS versions, screen sizes]
```

### Step 3: Enumerate Edge Cases (10 minutes)

This is where AI adds disproportionate value. Humans tend to spec the happy path. Claude catches the rest.

```
For each functional requirement, enumerate edge cases:

- Empty states: what does the user see before any data exists?
- Error states: what happens when the request fails, times out, or returns unexpected data?
- Boundary conditions: what happens at the minimum, maximum, and zero values?
- Permission states: what happens when the user doesn't have access?
- Concurrent states: what happens when two users modify the same data?
- Interruption states: what happens when the user abandons mid-flow, loses connection, or navigates away?
- Migration states: what happens for existing users vs. new users?
- Degraded states: what happens when a dependency is slow or unavailable?

For each edge case: what should the user see, and what should the system do?
```

### Step 4: Define Acceptance Criteria (10 minutes)

```
Write acceptance criteria for each requirement and key edge case:

Format:
Given [precondition]
When [action]
Then [expected result]

Rules:
- Every criterion must be testable — if you can't write a manual or automated test, rewrite it
- Include both positive cases (it works) and negative cases (it handles failure)
- Specify exact values where possible, not "appropriate" or "reasonable"
- Include performance criteria where relevant (e.g., "responds within 200ms")
```

### Step 5: Document Integration Points (10 minutes)

```
Map the integration points for this feature:

For each system this feature touches:
- System: [name]
- Integration type: [API call, event, webhook, database query, file transfer]
- Direction: [reads from / writes to / both]
- Contract: [endpoint, payload format, authentication]
- Failure mode: [what happens when this integration fails]
- Owner: [team responsible for the other side]

Data flow:
- What data does this feature create, read, update, or delete?
- Where does it come from and where does it go?
- What's the source of truth?
- Any data retention or privacy implications?
```

## Output

- Feature description with user and business value
- Functional and non-functional requirements
- Edge cases and error states enumerated
- Testable acceptance criteria (Given/When/Then)
- Integration map with contracts and failure modes

## Common Pitfalls

1. **Happy path only.** The feature works great when everything goes right. What about when it doesn't? Edge cases and error states are where user trust is built or broken.
2. **"Intuitive" as a requirement.** Delete the word "intuitive" from your spec. Replace it with specific, measurable criteria for what the user can accomplish and how.
3. **Missing the migration case.** Existing users with existing data will encounter this feature differently than new users. Spec both paths.
4. **No performance criteria.** "Fast" is not a requirement. "Responds within 200ms at p95 under 1000 concurrent users" is. Get numbers from engineering.
5. **Specifying implementation.** The feature spec describes *what* and *why*, not *how*. Leave the technical approach to engineering unless there's a constraint that forces a specific implementation.

## Related Skills

- [Epic Definition](../epic-definition/SKILL.md) — for the strategic wrapper around multiple features
- [Story Writing](../story-writing/SKILL.md) — for breaking this feature into developer-ready stories
- [PRD Writing](../prd-writing/SKILL.md) — when you need the full initiative-level document
- Reference: [TEMPLATES.md](../../TEMPLATES.md) — Feature template for formatting
