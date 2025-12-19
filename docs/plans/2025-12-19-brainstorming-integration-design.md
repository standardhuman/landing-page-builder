# Design: Brainstorming Integration into Landing Page Builder

**Date**: 2025-12-19
**Status**: Validated

## Summary

Integrate brainstorming into the landing page builder skill at two points:
- **Step 0**: Brainstorm the product/offer before research
- **Step 2**: Brainstorm messaging/copy using research findings

## New 7-Step Workflow

```
0. BRAINSTORM PRODUCT → 1. DEEP RESEARCH → 2. BRAINSTORM COPY → 3. INSPIRATION → 4. BUILD → 5. ITERATE → 6. DEPLOY
```

## Step 0: Brainstorm Product/Offer

**Purpose**: Clarify what you're selling before researching how to sell it.

**Process**:
1. Check for existing project context (files, docs, website)
2. Ask questions one at a time, multiple choice when possible:
   - What are you selling?
   - Who is this for? (get specific)
   - What problem does it solve?
   - What makes it different?
   - What's included?
   - Pricing/positioning constraints?
3. Summarize and confirm understanding

**Output**: `[product-name]-product-brief.md`

**Output Format**:
```markdown
# Product Brief: [Name]

## What It Is
## The Problem
## Who It's For
## What Makes It Different
## What's Included
## Positioning Notes
```

## Step 1: Deep Research

Unchanged from current implementation. Uses Type B Synthesis protocol.

**Output**: `landing-page-conversion-playbook-[YEAR].md`

## Step 2: Brainstorm Messaging/Copy

**Purpose**: Make messaging decisions informed by research findings.

**Inputs**:
- Product brief (Step 0)
- Research playbook (Step 1)

**Process**:
1. Review research - summarize top 3-5 insights relevant to this product
2. Messaging decisions (one at a time, present 2-3 options each):
   - Which pain point to lead with?
   - Headline approach?
   - Social proof available?
   - Objections to address?
   - CTA wording?
3. Generate copy using decisions + research tactics
4. Write at 5th grade reading level

**Output**: `[product-name]-landing-page-copy.md`

**Output Format**:
```markdown
# Landing Page Copy: [Name]

## Research Tactics Applied
- [Tactic] → Applied in [section]

## Headline
## Subheadline
## Hero Section
## Features/Benefits
## Social Proof
## Objection Handling
## CTA
```

## Steps 3-6

Unchanged from current implementation:
- Step 3: Inspiration (Firecrawl + screenshot)
- Step 4: Build (combine all inputs)
- Step 5: Iterate (Cursor with element selection)
- Step 6: Deploy (Netlify/Vercel CLI)

## Key Principles

- One question at a time during brainstorming
- Multiple choice preferred over open-ended
- Research findings inform copy decisions (not just generated blindly)
- Each brainstorm phase has clear output document
