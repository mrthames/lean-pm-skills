---
name: story-breakdown
description: Decompose a large problem, epic, or initiative into independently shippable slices. Use when work is too big to build in one sprint and you need to find the seams.
---

# Story Breakdown

Take something large and ambiguous — a big problem, a meaty epic, a multi-sprint initiative — and systematically decompose it into slices that are independently shippable, testable, and valuable. Claude applies splitting patterns and identifies natural seams. You make the judgment calls about what constitutes a meaningful increment.

## When to Use

- An epic or initiative is too large for a single sprint and needs decomposition
- The team says "this is at least a quarter of work" and you need to find a smaller first delivery
- Stakeholders want to see incremental progress, not a big bang release
- You're looking at a complex problem and need to identify the minimum viable first slice
- Estimates are wildly uncertain because the work hasn't been broken down enough
- A story is estimated at more than 8 points (or whatever your team's threshold is)

## When NOT to Use

- You already know the stories and just need to write acceptance criteria — use Story Writing
- You need to define the strategic epic first — use Epic Definition
- You need to write the full requirements document — use PRD Writing
- You're sequencing already-broken-down stories into sprints — use Sprint & Release Planning

## The AI-Native Approach

| Step | Time | Claude Does | You Do |
|---|---|---|---|
| Map the whole | 15 min | Structure the full scope of the work into a visual map | Confirm completeness, flag what's missing |
| Identify seams | 15 min | Apply splitting patterns to find natural decomposition points | Judge which seams produce meaningful slices |
| Slice and sequence | 20 min | Propose ordered slices with rationale for each boundary | Validate that each slice is independently valuable |
| Define the first slice | 10 min | Detail the first slice into stories ready for sprint planning | Confirm it's the right starting point |

## Process

### Step 1: Map the Whole (15 minutes)

Before you can break something down, you need to see the full picture. Map everything the work involves, even if it's rough.

```
I need to break down [large problem / epic / initiative]:

[Describe the full scope — what it needs to accomplish, who it's for, what success looks like]

Help me map the full scope:

1. User capabilities: What will users be able to do when this is complete?
   List every distinct thing a user can do, grouped by workflow or journey step.

2. System changes: What needs to change under the hood?
   List backend work, data migrations, integrations, infrastructure.

3. User types: Who interacts with this? Do different roles need different things?

4. States and transitions: What are the key states this feature moves through?
   (e.g., created → submitted → reviewed → approved → completed)

5. Touch points: What existing features or systems does this interact with?

Don't optimize yet — just map everything so we can see the full picture.
```

### Step 2: Identify Seams (15 minutes)

Seams are the natural places where work can be split into independently shippable pieces. Claude applies splitting patterns; you judge which ones produce slices worth shipping.

```
Look at the full scope map and identify splitting seams using these patterns:

1. **Workflow steps** — Can we ship one step of the journey before others?
   (e.g., "create" before "edit," "submit" before "approve")

2. **User roles** — Can we ship for one user type first?
   (e.g., admin flow before end-user flow, internal before external)

3. **Happy path vs. edge cases** — Can we ship the core flow first and handle exceptions later?
   (e.g., standard checkout before gift cards, coupons, and split payments)

4. **Data operations** — Can we split by CRUD operation?
   (e.g., read-only view before create, create before update, update before delete)

5. **Simple rules vs. complex rules** — Can we ship with simple business logic first?
   (e.g., flat pricing before tiered pricing, single currency before multi-currency)

6. **Single vs. bulk** — Can we handle one item before handling many?
   (e.g., single upload before batch upload, one notification before notification preferences)

7. **Manual vs. automated** — Can we ship a manual version first?
   (e.g., admin-triggered before scheduled, human review before auto-approval)

8. **Platforms** — Can we ship on one platform first?
   (e.g., web before mobile, API before UI)

For each seam identified:
- What would the slice include?
- Is it independently valuable? (Can a user do something meaningful with just this slice?)
- What's the rough size? (S / M / L)
- What does it de-risk or validate?
```

### Step 3: Slice and Sequence (20 minutes)

Now order the slices for incremental delivery. The goal: each slice ships value and reduces uncertainty for the next one.

```
From the seams identified, propose an ordered set of slices:

For each slice:
- Name: [short descriptive name]
- What's included: [specific capabilities in this slice]
- What's NOT included: [explicitly deferred to later slices]
- User value: [what a user can do with just this slice — must be independently meaningful]
- Risk it reduces: [what uncertainty this slice resolves for future slices]
- Rough size: [S / M / L or sprint estimate]
- Dependencies: [does this slice depend on another slice shipping first?]

Sequencing criteria:
1. Does it validate the riskiest assumption? (ship uncertainty-reducers first)
2. Does it deliver user value? (every slice should be demoable)
3. Does it unblock other work? (foundation before features)
4. Is it a quick win? (small slices that build momentum early)

Flag:
- Slices that aren't independently valuable (need to be combined or redrawn)
- The minimum viable first delivery (the absolute smallest thing worth shipping)
- The "walking skeleton" — if there's a thin end-to-end slice that touches all layers
```

### Step 4: Define the First Slice (10 minutes)

The first slice matters most — it sets the pattern, validates the architecture, and gives the team a win.

```
For the first slice [name]:

Break it into developer-ready stories:
- Use standard format (As a / I want to / So that)
- Include acceptance criteria for each story (Given / When / Then)
- Flag any technical spike or investigation needed before building
- Note the definition of done for this slice specifically

Questions to validate this is the right first slice:
- Can we demo this to a stakeholder and get useful feedback?
- Does it prove the architecture works end-to-end?
- If we shipped only this and nothing else, would it still be worth it?
- Does it take less than one sprint?
```

## Output

- Full scope map of the work
- Identified splitting seams with rationale
- Ordered slices with boundaries, value statements, and sizes
- First slice broken into developer-ready stories with acceptance criteria

## Common Pitfalls

1. **Slices that aren't independently shippable.** If a slice requires the next slice to be useful, it's not a real slice — it's a task. Every slice should deliver user-facing value or resolve meaningful uncertainty on its own.
2. **Breaking down by architecture layer.** "Backend first, then frontend" isn't a good breakdown — it delivers no user value until the last slice. Slice vertically (thin end-to-end) not horizontally (layer by layer).
3. **Making the first slice too big.** The first slice should be embarrassingly small. It proves the concept, validates the architecture, and gives the team a fast win. You can always expand in the next slice.
4. **Ignoring the walking skeleton.** The most valuable first slice is often a thin end-to-end flow that touches every layer — even if it only handles one case. This validates integration points early when they're cheapest to fix.
5. **Losing sight of the whole.** As you decompose, keep the scope map visible. It's easy to lose track of how slices relate to each other and to the original goal. Every slice should trace back to the map.
6. **Equal-sized slices.** Slices don't need to be the same size. A small first slice followed by a larger second slice is fine. Optimize for value delivery and risk reduction, not uniformity.

## Related Skills

- [Epic Definition](../epic-definition/SKILL.md) — define the strategic epic before breaking it down
- [Story Writing](../story-writing/SKILL.md) — write detailed stories for each slice
- [Feature Specification](../feature-specification/SKILL.md) — detail individual features within a slice
- [Sprint & Release Planning](../sprint-release-planning/SKILL.md) — sequence the slices into sprints
- Reference: [FRAMEWORKS.md](../../FRAMEWORKS.md) — Story Splitting patterns for additional techniques
