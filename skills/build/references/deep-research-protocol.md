# Deep Research Protocol for Landing Pages

This protocol is adapted from the [Claude Code Deep Research](https://github.com/anthropics/claude-code-deep-research) system. It provides a structured, multi-source approach to researching landing page best practices.

## When to Use

**Step 1 of the Landing Page Builder** uses this protocol to gather current, verified best practices instead of relying on a single search query.

## Research Type Classification

For landing page research, this is classified as:
- **Type B: Synthesis** - Multiple facts requiring aggregation
- **Intensity: Standard** - 3-5 search queries, 15-30 min
- **Depth: 2** - Enough to cross-reference but not exhaustive

---

## The Protocol

### Phase 1: Question Scoping (Automatic)

For landing page research, the question is pre-scoped:

```
Research Question: What are the current best practices for creating
high-converting landing pages as of [TODAY'S DATE]?

Scope:
- Geographic: Global (with US/EU emphasis)
- Timeframe: Last 12-18 months (current tactics only)
- Topics: Copywriting, structure, design, psychology, CRO
- Excluded: Enterprise B2B, app store pages, SEO-only tactics

Output: Actionable playbook with cited sources
```

### Phase 2: Multi-Source Search Strategy

Execute these search queries in parallel:

```
Query Set:
1. "landing page best practices 2024 2025 conversion rate optimization"
2. "high converting landing page copy structure psychology"
3. "landing page design trends [CURRENT YEAR] above fold"
4. "landing page CRO case studies real examples"
5. "landing page mistakes to avoid expert advice"
```

**Source Priority:**
- A-tier: Unbounce, ConversionXL, Nielsen Norman Group, HubSpot research
- B-tier: Industry blogs with data (Hotjar, Crazy Egg, VWO)
- C-tier: Practitioner case studies, agency content
- Avoid: Generic listicles, outdated content (pre-2023), SEO-farm articles

### Phase 3: Source Triangulation

For each tactic found, verify with the **2-source rule**:
- If only 1 source mentions it → mark as `[Single source]`
- If 2+ sources agree → mark as `[Verified]`
- If sources conflict → note the disagreement and present both

### Phase 4: Synthesis Template

Structure the research output as:

```markdown
# Landing Page Conversion Playbook [YEAR]

> Research compiled: [DATE]
> Sources consulted: [COUNT]
> Verification status: [X verified / Y single-source]

## Executive Summary
[3-5 bullet points of the most important findings]

## Above the Fold
### Headline [Verified/Single source]
- Tactic: [Description]
- Why it works: [Psychology/data]
- Source: [Citation with URL]
- Counter-evidence: [If any]

### Hero Section [Verified/Single source]
...

## Copy & Messaging
### Value Proposition
...

### Social Proof
...

## Visual Design
### Layout Patterns
...

### Color & Contrast
...

## CRO Tactics
### Forms
...

### CTAs
...

## What to Avoid
[Common mistakes with citations]

## Sources Consulted
[Full bibliography with URLs and access dates]

## Methodology Note
This research followed the Type B Synthesis protocol from the
Landing Page Builder skill, requiring 2+ independent sources
for verified claims.
```

### Phase 5: Quality Checks

Before finalizing:
- [ ] Every claim has at least one source URL
- [ ] Verified claims have 2+ independent sources
- [ ] No advice older than 18 months (unless timeless principle)
- [ ] Contradictions are acknowledged, not hidden
- [ ] Actionable: Each section has specific "do this" guidance

---

## Agent Prompt (For Automation)

If using Claude Code's Task tool to automate this research:

```
Task: "Landing Page Best Practices Research - [YEAR]"

Execute Type B Synthesis research for landing page best practices.

1. Run 5 parallel searches (queries provided above)
2. Prioritize A-tier sources (Unbounce, ConversionXL, NNG, HubSpot)
3. Extract specific tactics with supporting data
4. Triangulate: Mark claims as [Verified] if 2+ sources agree
5. Structure output using the Playbook template
6. Include full source URLs for every claim
7. Note any contradictions between sources

Budget: Max 8 WebSearch calls, 10 WebFetch calls
Output: Save to `landing-page-conversion-playbook-[YEAR].md`

IMPORTANT:
- Include today's date in searches to get current tactics
- Reject advice that lacks supporting data or examples
- If sources conflict, present both views
```

---

## Standalone Deep Research

This protocol is a simplified subset of the full Deep Research system.

For comprehensive research on any topic (not just landing pages), see:
- [Claude Code Deep Research](https://github.com/anthropics/claude-code-deep-research)
- Full 7-phase process with Graph of Thoughts
- Multi-agent orchestration for complex investigations
- Hypothesis testing and Red Team verification

The full system supports:
- Type A: Lookup (1-2 min)
- Type B: Synthesis (15-30 min) ← **Used here**
- Type C: Analysis (30-60 min)
- Type D: Investigation (2-4 hours)
