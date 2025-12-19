---
name: landing-page-builder
description: Build high-converting landing pages with AI using a 6-step workflow. Use when user wants to create a landing page, build a product page, make a marketing page, or convert visitors. Triggers on requests like "build me a landing page", "create a page for my product", "I need a landing page for...", or "help me build a marketing page". Covers deep research, copywriting, design inspiration, building, iteration, and deployment.
---

# Landing Page Builder

A 6-step workflow for creating landing pages that convert.

## The System

```
1. DEEP RESEARCH → 2. COPY → 3. INSPIRATION → 4. BUILD → 5. ITERATE → 6. DEPLOY
```

Each step feeds the next. Don't skip steps.

---

## Step 1: Deep Research

Research current landing page best practices using multi-source verification.

**Key**: This isn't a single search - it's a structured research protocol that triangulates findings across multiple authoritative sources.

### Quick Start

Run this research prompt:

```
Research the best practices for creating highly converting landing pages
as of today's date ([INSERT TODAY'S DATE]).

Execute Type B Synthesis research:
1. Search 5 query variations (see deep-research-protocol.md)
2. Prioritize: Unbounce, ConversionXL, Nielsen Norman, HubSpot
3. For each tactic, find 2+ sources to verify
4. Note any contradictions between sources
5. Only include actionable, current tactics (last 18 months)

Output format: Use the Playbook template from deep-research-protocol.md
Mark each claim as [Verified] or [Single source]
Include full URLs for every citation
```

### What Makes This Different

| Old Approach | Deep Research Approach |
|--------------|------------------------|
| Single search query | 5 parallel searches |
| Trust first result | Verify with 2+ sources |
| No citations | Every claim has URL |
| Generic advice | Current, dated tactics |
| Hidden conflicts | Contradictions noted |

See [deep-research-protocol.md](references/deep-research-protocol.md) for the full methodology.

**Output**: Save as `landing-page-conversion-playbook-[YEAR].md`

**Time**: 15-30 minutes (vs 5 min for shallow research)

---

## Step 2: Copy

Generate all landing page text before touching code.

**Key**: Request 5th grade reading level for clarity. Copy before code.

### Collect the Brief

Ask the user for their product details:

```
I need the following information about your product:

1. **Product Name**: What's it called?

2. **What It Is**: Plain description (1-2 sentences)

3. **Problem It Solves**: What pain point does this address?

4. **Who It's For**: Target audience (demographics + psychographics)

5. **What's Included**: List of features/deliverables
```

### Generate Copy

Once you have the brief:

```
Create the copy for a landing page based on this product brief.

RULES:
- Write at a 5th grade reading level
- Use short sentences and simple words
- Only write the TEXT - no code yet
- Include all sections: headline, subhead, features, social proof, CTA

<product_brief>
[INSERT BRIEF HERE]
</product_brief>
```

See [prompts.md](references/prompts.md#copywriting-prompt) for full prompt with example.

**Output**: Save as `[product-name]-landing-page-copy.md`

**Critical**: Review copy carefully before continuing. This is the foundation.

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

### Attach These 4 Files

1. Research playbook (Step 1)
2. Copy document (Step 2)
3. Branding JSON (Step 3)
4. Screenshot (Step 3)

### Build Prompt

```
You're an expert developer. Create a beautiful, well-structured
landing page for my product.

I'm providing:
1. Research on landing page best practices (attached)
2. The copy for my site (attached)
3. Design inspiration - branding JSON and screenshot (attached)

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
2. Hover over the page - blue boxes highlight sections
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
| Research | `landing-page-conversion-playbook-[YEAR].md` |
| Copy | `[product-name]-landing-page-copy.md` |
| Branding | `www.[site].com.json` |
| Screenshot | `[site]-screenshot.png` |

---

## Common Mistakes

1. **Shallow research** → Use the deep research protocol, not a single search
2. **Rushing copy** → Weak foundation; spend time here
3. **No inspiration** → Generic AI output
4. **Too many chat iterations** → AI quality degrades; move to Cursor
5. **Not using element selection** → Unfocused edits across whole page
6. **Skipping date in research** → Outdated tactics

---

## Quick Reference

| Step | Time | Output |
|------|------|--------|
| 1. Deep Research | 15-30 min | `landing-page-conversion-playbook-[YEAR].md` |
| 2. Copy | 15-30 min | `[product-name]-landing-page-copy.md` |
| 3. Inspiration | 5-10 min | JSON + Screenshot |
| 4. Build | 10-20 min | Initial HTML |
| 5. Iterate | 15-30 min | Refined HTML |
| 6. Deploy | 5-10 min | Live URL |

**Total**: ~1.5-2 hours for a complete, research-backed landing page.

---

## Deep Research for Other Topics

This skill uses a simplified version of the Deep Research system for Step 1.

For comprehensive research on any topic (not just landing pages), see the full system:
- [Claude Code Deep Research](https://github.com/anthropics/claude-code-deep-research)
- 7-phase process with Graph of Thoughts
- Multi-agent orchestration
- Hypothesis testing and verification
