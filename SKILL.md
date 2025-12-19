---
name: landing-page-builder
description: Build high-converting landing pages with AI using a 7-step workflow. Use when user wants to create a landing page, build a product page, make a marketing page, or convert visitors. Triggers on requests like "build me a landing page", "create a page for my product", "I need a landing page for...", or "help me build a marketing page". Covers brainstorming, deep research, copywriting, design inspiration, building, iteration, and deployment.
---

# Landing Page Builder

A 7-step workflow for creating landing pages that convert. Includes brainstorming, research, and everything you need in one place.

## The System

```
0. BRAINSTORM PRODUCT → 1. DEEP RESEARCH → 2. BRAINSTORM COPY → 3. INSPIRATION → 4. BUILD → 5. ITERATE → 6. DEPLOY
```

Each step feeds the next. Don't skip steps.

---

## Step 0: Brainstorm Product/Offer

Clarify what you're selling before researching how to sell it.

**Process**: Ask questions one at a time, multiple choice when possible.

### Questions to Explore

1. **What are you selling?** (open-ended)
2. **Who is this for?** → Get specific: age, job, situation, pain level
3. **What problem does it solve?** → Dig into the actual pain
4. **What makes this different?** → vs. alternatives or doing nothing
5. **What's included?** → Deliverables, features, what they get
6. **Pricing/positioning?** → Any constraints or context

### Key Principles

- **One question at a time** - Don't overwhelm
- **Multiple choice preferred** - Easier to answer
- **Dig deeper** - Follow up on interesting answers
- **Confirm understanding** - Summarize back before moving on

### Output

Save as `[product-name]-product-brief.md`:

```markdown
# Product Brief: [Name]

## What It Is
[1-2 sentences - plain language]

## The Problem
[Pain point in customer's words]

## Who It's For
[Specific audience: demographics + psychographics]

## What Makes It Different
[Unique angle or differentiation]

## What's Included
- [Deliverable 1]
- [Deliverable 2]
- ...

## Positioning Notes
[Pricing context, constraints, market position]
```

---

## Step 1: Deep Research

Research current landing page best practices using multi-source verification.

**Key**: This isn't a single search - it's a structured research protocol that triangulates findings across multiple authoritative sources.

### Quick Start

```
Research the best practices for creating highly converting landing pages
as of today's date ([INSERT TODAY'S DATE]).

Execute Type B Synthesis research:
1. Search 5 query variations
2. Prioritize: Unbounce, ConversionXL, Nielsen Norman, HubSpot
3. For each tactic, find 2+ sources to verify
4. Note any contradictions between sources
5. Only include actionable, current tactics (last 18 months)

Mark each claim as [Verified] or [Single source].
Include full URLs for every citation.
```

### What Makes This Different

| Old Approach | Deep Research Approach |
|--------------|------------------------|
| Single search query | 5 parallel searches |
| Trust first result | Verify with 2+ sources |
| No citations | Every claim has URL |
| Generic advice | Current, dated tactics |

See [deep-research-protocol.md](references/deep-research-protocol.md) for the full methodology.

**Output**: Save as `landing-page-conversion-playbook-[YEAR].md`

**Time**: 15-30 minutes

---

## Step 2: Brainstorm Messaging/Copy

Make messaging decisions informed by research findings.

**Inputs Available**:
- Product brief from Step 0
- Research playbook from Step 1

### Phase 1: Review Research

Before asking questions, summarize the top 3-5 research insights relevant to THIS product:

> "The research shows [tactic] increases conversions. Given your product, here's how we might apply that..."

### Phase 2: Messaging Decisions (one at a time)

1. **Which pain point should we lead with?**
   - Present 2-3 angles based on the product brief
   - Recommend one with reasoning

2. **What's the headline approach?**
   - Present 2-3 options
   - Apply research-backed headline tactics

3. **What social proof do you have?**
   - Testimonials, numbers, logos, media mentions?
   - Discuss placement based on research

4. **What objections might visitors have?**
   - Brainstorm 2-3 likely objections
   - Discuss how to address each

5. **What's the primary CTA?**
   - Action word + urgency approach
   - Apply research-backed CTA tactics

### Phase 3: Generate Copy

Using the decisions above:
- Write the full landing page copy
- Apply research-backed tactics (cite which ones)
- Write at 5th grade reading level

### Output

Save as `[product-name]-landing-page-copy.md`:

```markdown
# Landing Page Copy: [Name]

## Research Tactics Applied
- [Tactic from playbook] → Applied in [section]
- [Tactic] → Applied in [section]

## Headline
[The chosen headline]

## Subheadline
[Supporting statement]

## Hero Section
[1-2 sentences that hook and explain]

## Problem
[Agitate the pain point]

## Solution
[How the product helps]

## Features/Benefits
- [Feature] → [Benefit]
- ...

## Social Proof
[Testimonials, numbers, logos]

## Objection Handling
[Address concerns]

## CTA
[Primary call to action]

## Footer CTA
[Final push]
```

---

## Step 3: Inspiration

Give AI visual references so it doesn't default to generic designs.

### Collect Two Things

**1. Branding JSON from Firecrawl**
- Go to [firecrawl.dev/playground](https://firecrawl.dev)
- Paste inspiration site URL
- Uncheck "markdown", check "branding"
- Download the JSON

**2. Full-Page Screenshot**
- Open inspiration site in Chrome
- `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Win)
- Type "screenshot" → "Capture full size screenshot"

See [tools.md](references/tools.md#firecrawl) for detailed instructions.

**Output**: `www.[site].com.json` + `[site]-screenshot.png`

---

## Step 4: Build

Combine all outputs to generate the landing page.

### Attach These 5 Files

1. Product brief (Step 0)
2. Research playbook (Step 1)
3. Copy document (Step 2)
4. Branding JSON (Step 3)
5. Screenshot (Step 3)

### Build Prompt

```
You're an expert developer. Create a beautiful, well-structured
landing page for my product.

I'm providing:
1. Product brief (context about what we're selling)
2. Research on landing page best practices
3. The copy for my site (use ALL of this)
4. Design inspiration - branding JSON and screenshot

Create the site in HTML, CSS, and JavaScript.
Include ALL the copy I've provided.
Use the visual style from the inspiration.
Apply the conversion tactics from the research.

If you need clarification before starting, ask.
```

**Model**: Use the best available (Claude Opus, GPT-4+, etc.)

**Iteration limit**: Do 1-2 iterations in chat, then move to Step 5.

---

## Step 5: Iterate

Refine in Cursor for focused edits.

### Setup

1. Download the HTML from chat
2. Create a folder on your desktop (e.g., `landing-page/`)
3. Add the HTML file to the folder
4. Open the folder in Cursor

### Key Feature: Element Selection

1. Click the mouse icon with box ("Select element")
2. Hover over the preview - blue boxes highlight sections
3. Click to select a section
4. Describe your change
5. AI edits only that section (not the whole page)

### Workflow

```
Select element → Describe change → Accept → Repeat
```

After 2-3 edits, start a fresh chat (click + button).

See [tools.md](references/tools.md#cursor) for detailed workflow.

---

## Step 6: Deploy

Deploy via Netlify or Vercel CLI.

### Prerequisites

1. Create subdomain in your domain provider
2. Create Netlify or Vercel account

### Deploy Commands

In Cursor, start a new chat:

**Netlify:**
```
Use the Netlify CLI to connect to my instance and deploy this code live.
```

**Vercel:**
```
Use the Vercel CLI to deploy this landing page.
```

AI handles CLI installation, authentication, and deployment.

See [tools.md](references/tools.md#deployment) for subdomain setup help.

---

## File Naming Conventions

| Type | Convention |
|------|------------|
| Product Brief | `[product-name]-product-brief.md` |
| Research | `landing-page-conversion-playbook-[YEAR].md` |
| Copy | `[product-name]-landing-page-copy.md` |
| Branding | `www.[site].com.json` |
| Screenshot | `[site]-screenshot.png` |

---

## Quick Reference

| Step | Time | Output |
|------|------|--------|
| 0. Brainstorm Product | 10-15 min | `[product-name]-product-brief.md` |
| 1. Deep Research | 15-30 min | `landing-page-conversion-playbook-[YEAR].md` |
| 2. Brainstorm Copy | 15-20 min | `[product-name]-landing-page-copy.md` |
| 3. Inspiration | 5-10 min | JSON + Screenshot |
| 4. Build | 10-20 min | Initial HTML |
| 5. Iterate | 15-30 min | Refined HTML |
| 6. Deploy | 5-10 min | Live URL |

**Total**: ~1.5-2.5 hours for a complete, research-backed landing page.

---

## Common Mistakes

1. **Skipping brainstorming** → Unclear product = weak copy
2. **Shallow research** → Use the deep research protocol, not a single search
3. **Ignoring research in copy** → Apply the tactics you found
4. **Rushing copy decisions** → One question at a time, explore options
5. **No inspiration** → Generic AI output
6. **Too many chat iterations** → AI quality degrades; move to Cursor
7. **Not using element selection** → Unfocused edits across whole page
