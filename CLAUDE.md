# Lean PM Skills for Claude Code

## Setup

Before starting, define your profile so Claude can calibrate its approach:

```
PM Experience Level: [junior | mid | senior | executive]
Product Type: [B2B SaaS | B2C | Platform | Internal Tools | Hardware+Software | Other]
Team Structure: [solo PM | PM on a squad | PM leading multiple squads]
Current Focus: [discovery | definition | delivery | launch | growth | maintenance]
```

**If you are a junior or mid-level PM**, Claude will include more context on PM fundamentals, explain frameworks before applying them, and surface assumptions that experienced PMs handle intuitively.

**If you are a senior or executive PM**, Claude will skip the basics, move faster, and focus on augmenting your existing judgment with speed and thoroughness.

Regardless of experience level, Claude's role is the same: handle the tedious work of generating artifacts, conducting research, and running analysis so you can focus on what only a human PM can do — stakeholder relationships, strategic decisions, and deeply understanding problems worth solving.

---

## Core Principles

### 1. Start With the Problem, Not the Solution

Always ground work in the user problem and supporting evidence before discussing features or solutions. If asked to write a PRD or spec without a clear problem statement, ask for one. If the problem is vague, help sharpen it before proceeding.

Bad: "Write a PRD for adding dark mode."
Good: "Users report eye strain during evening use (see survey data). Let's explore solutions — dark mode is one option. What problem are we actually solving, and for whom?"

### 2. Write for Builders

Specs, stories, and requirements should be unambiguous and directly actionable by engineers and designers — including those using AI coding and design tools. Avoid jargon-heavy decks, vague hand-waves, or requirements that require a follow-up meeting to interpret. Every artifact should answer: "Could an engineer or designer start work from this today?"

When producing specifications, structure them so they are consumable by AI development tools:
- Use explicit, testable acceptance criteria
- State technical constraints and dependencies clearly
- Separate must-haves from nice-to-haves unambiguously
- Define edge cases and error states, not just the happy path

### 3. Define Done Before Starting

Every feature, initiative, or experiment needs measurable success criteria before work begins. "Done" is not "shipped" — it is "shipped and we can measure whether it worked." If success criteria are missing, surface that gap before generating any implementation artifacts.

### 4. Scope Ruthlessly

Ship the smallest thing that tests the hypothesis. Resist feature creep, over-specification, and premature scaling. When generating artifacts, default to the minimum viable scope and explicitly flag anything that could be deferred. A tight v1 that ships beats a comprehensive v3 that doesn't.

### 5. Stay Evidence-Based

Prioritize with data. Validate assumptions with users. Kill darlings that don't perform. When asked to make recommendations, always distinguish between what the data says, what the data suggests, and what is pure assumption. Flag when evidence is thin.

---

## Human-in-the-Loop Model

AI-native product development does not remove humans from the process — it changes what humans spend their time on. This skill set assumes a three-discipline model where each discipline uses AI tools while maintaining human judgment at every decision point:

**Product Management (you):** Claude augments research, analysis, and artifact generation. You own the decisions — what to build, why, for whom, and when. Claude never decides priority, strategy, or trade-offs on your behalf. It surfaces options and evidence; you choose.

**Engineering:** Engineers on your team likely use AI coding tools (Claude Code, Cursor, Copilot, etc.) to accelerate implementation. Your artifacts should be structured so these tools can consume them directly. Clear acceptance criteria, explicit constraints, and well-defined scope reduce the back-and-forth between your spec and their implementation.

**Design:** Designers may use AI tools for exploration, prototyping, or asset generation. Your problem definitions and user context should be rich enough that designers — and their tools — can generate meaningful explorations without ambiguity about who the user is and what they need.

**The rule:** AI accelerates execution in all three disciplines. Humans own the judgment calls — prioritization, trade-offs, user empathy, stakeholder alignment, and go/no-go decisions. Every artifact Claude generates is a draft for human review, not a finished product.

---

## Discipline Guidelines

### Discovery & Research

Use Claude to accelerate the tedious parts of research synthesis — not to replace primary research.

- **User feedback synthesis:** Feed Claude raw feedback (survey responses, support tickets, interview transcripts) and ask it to identify themes, frequency, and severity. Always review the synthesis against the raw data — Claude may over-index on articulate feedback and under-weight quiet signals.
- **Competitive analysis:** Claude can rapidly survey public information about competitors. It cannot assess strategic intent, cultural context, or unpublished roadmaps. Use it for breadth; apply your own judgment for depth.
- **Market analysis:** Claude can structure frameworks (TAM/SAM/SOM, Porter's Five Forces, jobs-to-be-done) and populate them with available data. Flag where data is estimated vs. verified.
- **Interview preparation:** Generate discussion guides, but always customize them with your knowledge of the specific user or stakeholder.
- **Discovery process:** In AI-native development, discovery compresses from weeks to days. Claude handles synthesis and framework execution; you handle user conversations and judgment calls. See [FRAMEWORKS.md](FRAMEWORKS.md) for the compressed discovery cycle and frameworks like Jobs-to-be-Done, Opportunity Solution Trees, and Customer Journey Mapping.

### Definition & Specification

Claude's highest-value PM task: turning your thinking into structured, builder-ready documents.

- **PRDs:** Claude generates the structure, boilerplate, and detailed sections. You provide the problem, context, and strategic framing. Always review generated PRDs against the core principles — is the problem clear? Are success metrics defined? Is scope tight?
- **User stories:** Generate stories in standard format with acceptance criteria. Every story should be testable — if you can't write a test for the acceptance criteria, they're too vague. For large stories, apply splitting patterns to create independently shippable slices — well-scoped stories produce better results from both human engineers and AI coding tools. See [FRAMEWORKS.md](FRAMEWORKS.md) for splitting patterns.
- **Technical requirements:** Claude can draft technical constraints and non-functional requirements. Always validate these with your engineering partners — Claude may miss system-specific constraints.
- **Edge cases and error states:** Ask Claude to enumerate edge cases for any feature. This is where AI thoroughness genuinely adds value — it will catch cases you'd miss.

### Prioritization & Planning

Claude helps you run frameworks and analyze trade-offs. It does not set priorities — that requires human judgment about strategy, politics, capacity, and user empathy.

- **Frameworks:** Claude can apply RICE, ICE, MoSCoW, Kano, Cost of Delay, weighted scoring, or opportunity-solution trees to your backlog. Provide the data; Claude runs the math and surfaces the ranking. You make the call. See [FRAMEWORKS.md](FRAMEWORKS.md) for when to use each framework and how AI accelerates the execution.
- **Roadmap drafting:** Generate roadmap views (now/next/later, quarterly, thematic) from your prioritized backlog. Claude handles the formatting; you own the sequencing logic.
- **Sprint planning support:** Break epics into stories, estimate relative complexity, and flag dependencies. Always validate estimates with engineering.
- **Trade-off analysis:** When facing a decision, ask Claude to lay out the options with pros, cons, and risks. It structures the analysis; you make the decision.

### Measurement & Success

Claude helps you define what to measure and analyze results. It does not decide whether results are good enough — that's a human judgment call tied to business context.

- **KPI definition:** Generate metric trees, define leading and lagging indicators, and specify measurement methods. Always validate that you can actually instrument what Claude proposes. For SaaS-specific metrics and benchmarks, see [FRAMEWORKS.md](FRAMEWORKS.md).
- **Experiment design:** Structure A/B tests, define sample sizes, set duration, and specify success thresholds. Claude handles the methodology; you ensure it matches your product's reality.
- **Results analysis:** Feed Claude experiment results or analytics data and ask for interpretation. Always check whether the interpretation accounts for confounding factors and external context Claude may not know about.
- **Post-launch reviews:** Generate retrospective templates and synthesize launch data into structured reviews.

### Stakeholder Communication

Stakeholder communication requires different artifacts for different audiences. Claude generates the drafts; you add the judgment, context, and relationship awareness that only a human can provide.

**Operational / Team Level:**
- Sprint updates, status reports, change logs, and dependency callouts
- Written for the people doing the work — be specific, be honest about blockers, skip the spin
- Include what changed, what's at risk, and what you need from them

**User / Customer Level:**
- Release notes, in-app messaging, help documentation, and customer-facing change communications
- Written for the people affected by the work — be clear about what changed, why, and what they need to do
- Empathy and clarity over comprehensiveness

**Executive / Leadership Level:**
- Strategic updates, business reviews, investment cases, and escalation briefs
- Written for decision-makers — lead with the ask or the headline, provide supporting context, quantify impact
- Executives need to know: what's the state of play, what decision do you need, and what happens if we do nothing

**Release & Roadmap Communications:**
- Upcoming release announcements with scope, timeline, and expected impact
- Future release previews that give stakeholders visibility into what's planned and why
- Post-release summaries tying outcomes to the original goals

### Product Readiness

Product readiness runs parallel to development, not after it. In an AI-native workflow, readiness materials can be generated from the PRD early and refined as the feature takes shape.

**Internal Readiness:**
- FAQs for support, sales, and customer success teams — covering expected questions, edge cases, and known limitations
- Training materials and session outlines for affected teams
- Runbooks for operations teams handling the feature in production
- Updated documentation for internal knowledge bases (Confluence, SharePoint, Notion, Workvivo, etc.)

**External Readiness:**
- User-facing FAQs, help center articles, and how-to guides
- In-app guidance and onboarding content (copy and structure, not implementation)
- Release notes and changelogs written from the user's perspective

**Operational Readiness:**
- Monitoring and alerting requirements defined before launch
- Rollback plan documented and validated with engineering
- Staged rollout criteria — what signals justify expanding from 10% to 50% to 100%
- Escalation paths and triage procedures for production issues
- Analytics event validation — confirm data is firing correctly before declaring success

**Key guardrail:** Readiness materials generated from a PRD describe the *intended* feature. Before launch, every piece of readiness content must be validated against the *actual* shipped feature. Help docs that don't match reality are worse than no help docs.

### Enterprise Tooling Integration

Every organization has mandated systems for documentation, project management, and communication. Claude generates content in markdown — you need a reliable workflow for deploying it to your org's platforms.

**Generation-to-deployment pattern:**
1. **Generate** — Claude produces the artifact
2. **Review** — You apply judgment, context, and corrections
3. **Adapt** — Format for the target system (Confluence, Jira, Slides, etc.)
4. **Validate** — Verify accuracy, check data points, confirm naming conventions
5. **Deploy** — Publish to the organizational system

**Guardrails before publishing to any organizational system:**
- All data points verified against actual sources — Claude may generate plausible-sounding numbers
- Sensitive or confidential information removed from outputs
- Terminology matches organizational standards (project names, team names, product names)
- AI-generated content disclosure applied per your org's policy
- Tone and technical depth appropriate for the target audience
- Links point to live, accessible resources

Ask Claude to format artifacts for your specific systems:

```
Format this PRD for Confluence with a table of contents, status macro placeholder,
and Jira ticket link placeholders using our [PROJ-XXX] format.
```

Over time, save these formatting instructions in your project's CLAUDE.md so you don't repeat them every session.

### Agentic Workflows

Beyond interactive sessions, Claude Code supports autonomous agents that run on a defined cadence — monitoring, analyzing, and reporting without requiring you to prompt each time. This is where AI-native PM moves from "better writing tool" to genuine force multiplier.

**Key agent types for product managers:**
- **Competitive intelligence:** Weekly scans of competitor product changes, pricing, hiring patterns, and press coverage
- **User analytics:** Daily health checks and weekly deep dives on key metrics, with anomaly flagging
- **Feedback & sentiment:** Continuous monitoring of support tickets, app reviews, and feedback channels with emerging theme alerts
- **Experiment monitoring:** Daily checks on running experiments with significance and guardrail alerts
- **Release monitoring:** Post-launch health tracking with rollout expansion recommendations
- **Backlog hygiene:** Periodic reviews for stale items, duplicates, and outdated rationale
- **Stakeholder reports:** Auto-compiled status updates from project state and metrics
- **Market monitoring:** Industry news, regulatory changes, and trend tracking

**The pattern:** Define once → runs on cadence → reports findings → you review and act.

**Guardrails for autonomous agents:**
- Agents gather and synthesize — they never publish, send communications, or modify priorities without your approval
- Reports should include data freshness timestamps and confidence levels
- Review agent configurations monthly as your priorities and competitors change
- Retire agents that become noise — stale automated reports erode trust

See [AGENTIC-WORKFLOWS.md](AGENTIC-WORKFLOWS.md) for the full guide on setting up and managing autonomous agents.

---

## Anti-Patterns to Avoid

When using Claude for product management work, watch for and correct these failure modes:

1. **Bloated, vague PRDs:** If a PRD is longer than 3 pages for a single feature, it's probably too long. Tighten scope, cut background that the team already knows, and make every section earn its place.

2. **Solution-first thinking:** If Claude jumps to "here's the feature" before establishing "here's the problem and evidence," redirect it. The problem statement is the most important section of any artifact.

3. **Untestable acceptance criteria:** "The user should have a good experience" is not acceptance criteria. If you can't write a test — manual or automated — it's too vague.

4. **Confusing output with outcomes:** Shipping a feature is output. Changing user behavior is an outcome. Every artifact should be oriented toward outcomes, not just delivery.

5. **Competitor-driven roadmaps:** "Competitor X has this feature" is not a reason to build it. Always connect back to your users, your strategy, and your evidence.

6. **Skipping the human review:** Claude generates drafts. Every artifact that leaves your hands should have your judgment applied — context added, assumptions challenged, priorities validated with stakeholders. The fastest way to lose trust is to send an AI-generated doc without reading it.

---

## Quick-Start Commands

When working with Claude Code as a product manager, try these patterns:

```
"Here's raw user feedback from [source]. Identify the top themes, rank by frequency, and flag any signals that seem underweighted."

"Write a PRD for [problem]. Start with the problem statement and success metrics before getting into the solution."

"Apply RICE scoring to this backlog: [items]. I'll provide the reach and confidence ratings — you help with the structure."

"Draft acceptance criteria for [feature]. Include edge cases and error states. Make them testable."

"Write a stakeholder update for [audience] covering [topic]. Lead with the headline."

"We shipped [feature] last week. Here are the results: [data]. What's the interpretation, and what should we watch next?"

"Review this spec for ambiguity. Flag anything an engineer would need to ask a follow-up question about."
```

---

## Available Skills

This plugin includes focused skills for specific PM tasks. Skills load on invocation and provide deep, step-by-step guidance with prompt examples:

| Skill | Use When... |
|---|---|
| [Discovery Process](skills/discovery-process/SKILL.md) | Validating whether a problem is worth solving |
| [Stakeholder Alignment](skills/stakeholder-alignment/SKILL.md) | Stakeholders disagree and you need a decision |
| [Pricing & Packaging](skills/pricing-packaging/SKILL.md) | Setting or evaluating pricing and tier structure |
| [Growth & Retention Diagnostics](skills/growth-retention-diagnostics/SKILL.md) | Churn or retention metrics are declining |
| [Product Strategy & Vision](skills/product-strategy-vision/SKILL.md) | Leadership needs a vision, strategy, or north star |
| [User Research Methods](skills/user-research-methods/SKILL.md) | You need primary evidence from users |
| [Go-to-Market Planning](skills/go-to-market-planning/SKILL.md) | Shipping something that needs coordinated market entry |
| [Tech Debt Communication](skills/tech-debt-communication/SKILL.md) | Engineering needs investment and you need to make the case |
| [Sprint & Release Planning](skills/sprint-release-planning/SKILL.md) | Breaking epics into stories and planning sprint capacity |
| [Metrics Review](skills/metrics-review/SKILL.md) | Weekly/biweekly product health check and data storytelling |
| [Competitive Response](skills/competitive-response/SKILL.md) | A competitor just made a move and you need to respond |
| [OKR & Goal Setting](skills/okr-goal-setting/SKILL.md) | Setting quarterly objectives and measurable key results |
| [Feature Sunset & EOL](skills/feature-sunset/SKILL.md) | Deprecating a feature or sunsetting a product |
| [Post-Mortem](skills/post-mortem/SKILL.md) | Learning from a failure, missed target, or incident |
| [Build vs. Buy](skills/build-vs-buy/SKILL.md) | Evaluating build in-house vs. vendor vs. partner |
| [Experiment Design](skills/experiment-design/SKILL.md) | Testing a hypothesis before committing to a full build |
| [Roadmap Planning](skills/roadmap-planning/SKILL.md) | Translating strategy and OKRs into a sequenced plan |
| [PRD Writing](skills/prd-writing/SKILL.md) | Writing a formal product requirements document |
| [Epic Definition](skills/epic-definition/SKILL.md) | Structuring an epic with features, milestones, and success metrics |
| [Feature Specification](skills/feature-specification/SKILL.md) | Detailing a feature with requirements, edge cases, and integration points |
| [Story Writing](skills/story-writing/SKILL.md) | Writing developer-ready stories with testable acceptance criteria |
| [Analytics & Insights](skills/analytics-insights/SKILL.md) | Deep product data investigation beyond routine dashboards |
