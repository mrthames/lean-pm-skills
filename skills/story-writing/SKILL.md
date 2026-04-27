---
name: story-writing
description: Write user stories with testable acceptance criteria, edge cases, and splitting guidance. Use when you need developer-ready stories for sprint planning.
---

# Story Writing

Write clear, testable, developer-ready user stories in minutes instead of struggling through ambiguous requirements. Claude handles the structure, acceptance criteria enumeration, and edge case coverage. You provide the user context and validate that the stories match what you actually mean.

## When to Use

- Breaking a feature or epic into sprint-ready stories
- Writing acceptance criteria that engineers (and AI coding tools) can build from directly
- Stories from the backlog are too vague for development
- Sprint planning is imminent and stories need to be refined
- You need to split a story that's too large for a single sprint

## When NOT to Use

- You need to define the feature first — use Feature Specification
- You need the strategic epic wrapper — use Epic Definition
- You're prioritizing which stories to do — use Sprint & Release Planning

## The AI-Native Approach

| Step | Time | Claude Does | You Do |
|---|---|---|---|
| Draft the story | 5 min | Structure the user story from your description | Confirm it captures the user's real need |
| Write acceptance criteria | 10 min | Enumerate testable criteria including edge cases | Validate each criterion is what you mean |
| Check for splitting | 5 min | Assess size and recommend splits if too large | Decide where to draw the boundaries |
| Add technical context | 5 min | Note constraints, dependencies, and test notes | Verify with engineering |

## Process

### Step 1: Draft the Story (5 minutes)

```
I need a user story for: [describe what the user should be able to do]

Context:
- Feature/epic it belongs to: [name]
- User: [who is performing this action — be specific about the persona or role]
- Current state: [what they do today, or what doesn't exist yet]

Write the story in standard format:
As a [specific user role],
I want to [specific action],
So that [specific outcome/value].

Challenge me if:
- The "so that" is weak or circular
- The story is actually multiple stories
- The user role is too generic
```

### Step 2: Write Acceptance Criteria (10 minutes)

```
Write acceptance criteria for this story:

Format (Given/When/Then):
Given [precondition or setup state]
When [the user takes this action]
Then [this specific, observable result occurs]

Include:
- Happy path: the thing works as intended
- Validation: what happens with invalid input
- Empty state: what the user sees before any data exists
- Error handling: what happens when something fails
- Boundary conditions: min, max, zero, and edge values
- Permission handling: what happens if the user lacks access

Rules:
- Every criterion must be testable (manual or automated)
- Use specific values, not "appropriate" or "user-friendly"
- If a criterion has the word "should," make it "must" or delete it
- Include what the system does, not just what the user sees
```

### Step 3: Check for Splitting (5 minutes)

Stories that are too large create risk — they're hard to estimate, hard to test, and hard to ship incrementally.

```
Assess this story for size:

Is this story too large for a single sprint? Check:
- More than 5 acceptance criteria → consider splitting
- Multiple user roles → split by role
- Multiple actions in the "I want to" → split by action
- "And" in the story → probably two stories
- Happy path + complex error handling → split into core + edge cases

If splitting is recommended, apply these patterns:
1. Happy path first, edge cases second
2. Create before update before delete
3. Single item before bulk/batch
4. Simple rule before complex rule
5. One user role at a time

For each split story: write the full story with its own acceptance criteria.
```

### Step 4: Add Technical Context (5 minutes)

```
Add technical context to make this story fully ready for development:

Technical notes:
- Known constraints: [platform, API, performance]
- Dependencies: [other stories, other teams, external systems]
- Test notes: [specific test scenarios, test data needs, environments]
- Design reference: [link to mockups, wireframes, or design specs]
- Analytics: [events to track, metrics to instrument]

Definition of done:
- [ ] Acceptance criteria met
- [ ] Unit tests written
- [ ] Edge cases tested
- [ ] Code reviewed
- [ ] Analytics events firing
- [ ] Documentation updated (if applicable)
```

## Output

- User stories in standard format (As a / I want to / So that)
- Testable acceptance criteria in Given/When/Then format
- Stories split to sprint-appropriate size
- Technical context and definition of done

## Common Pitfalls

1. **"As a user" is not a role.** Be specific: "As a free-tier user," "As an admin with billing access," "As a first-time visitor." The role determines the context and constraints.
2. **Untestable criteria.** "The page loads quickly" — how quickly? "Under 2 seconds at p95" is testable. If QA can't write a test for it, rewrite it.
3. **Solution-as-story.** "As a user, I want a dropdown menu" describes an implementation, not a need. "As a user, I want to filter results by category so I can find relevant items faster" describes the need — the dropdown is one possible solution.
4. **Mega-stories.** If a story has 10+ acceptance criteria, it's an epic wearing a story costume. Split it. Small stories ship faster and catch problems earlier.
5. **Missing the "so that."** The "so that" is the most important part — it's the value proposition. Without it, you're writing tasks, not stories. If you can't articulate the value, question whether the story matters.

## Related Skills

- [Feature Specification](../feature-specification/SKILL.md) — when the feature needs full specification before breaking into stories
- [Sprint & Release Planning](../sprint-release-planning/SKILL.md) — for sequencing stories into sprints
- [Epic Definition](../epic-definition/SKILL.md) — for the strategic wrapper around related stories
- Reference: [FRAMEWORKS.md](../../FRAMEWORKS.md) — Story Splitting patterns for breaking large stories
- Reference: [TEMPLATES.md](../../TEMPLATES.md) — User Story template for formatting
