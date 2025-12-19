# Prompt Templates

## Deep Research Prompt

Use in Step 1 for comprehensive, multi-source research.

### Quick Version

```
Research the best practices for creating highly converting landing pages
as of today's date ([INSERT DATE]).

I need:
- Current tactics only (last 18 months)
- Multiple sources to verify each claim
- Specific, actionable advice
- Full citations with URLs

Topics to cover:
- Copywriting (headlines, CTAs, value props)
- Page structure (above fold, layout)
- Visual design (colors, typography, imagery)
- Psychology (social proof, urgency, trust)
- Conversion optimization (forms, friction reduction)

Mark each tactic as [Verified] (2+ sources) or [Single source].
Note any contradictions between sources.
```

### Full Automated Version

```
Execute Type B Synthesis research for landing page best practices.

Search Strategy (run in parallel):
1. "landing page best practices 2024 2025 conversion rate optimization"
2. "high converting landing page copy structure psychology"
3. "landing page design trends [CURRENT YEAR] above fold"
4. "landing page CRO case studies real examples"
5. "landing page mistakes to avoid expert advice"

Source Priority:
- A-tier: Unbounce, ConversionXL, Nielsen Norman Group, HubSpot
- B-tier: Hotjar, Crazy Egg, VWO (with data)
- C-tier: Practitioner case studies, agency content
- Avoid: Generic listicles, pre-2023 content, SEO-farm articles

Verification:
- 2+ sources = [Verified]
- 1 source = [Single source]
- Conflicting sources = Note both views

Output Structure:
1. Executive Summary (3-5 bullets)
2. Above the Fold (headline, hero, CTA)
3. Copy & Messaging (value prop, social proof)
4. Visual Design (layout, colors, imagery)
5. CRO Tactics (forms, friction, urgency)
6. What to Avoid (common mistakes)
7. Sources Consulted (full bibliography)

Budget: Max 8 searches, 10 fetches
Save to: landing-page-conversion-playbook-[YEAR].md
```

---

## Copywriting Prompt

Use in Step 2 to generate landing page copy.

```
Create the copy for a landing page based on this product brief.

RULES:
- Write at a 5th grade reading level
- Use short sentences and simple words
- Only write the TEXT - no code
- Include all standard landing page sections

SECTIONS TO INCLUDE:
1. Headline (attention-grabbing, benefit-focused)
2. Subheadline (clarifies the headline)
3. Hero description (1-2 sentences)
4. Problem statement (what pain you solve)
5. Solution (how your product helps)
6. Features/Benefits (3-5 key points)
7. Social proof (testimonials, numbers, logos)
8. Objection handling (address concerns)
9. CTA (clear call to action)
10. Footer CTA (final push)

<product_brief>
Product Name
[Your product name]

What It Is
[Plain description of what you're selling]

The Problem It Solves
[What pain point does this address?]

Who It's For
[Target audience demographics and psychographics]

What's Included
[List of features/deliverables]
</product_brief>
```

### Example Brief (For Reference)

```
Product Name
Decline All

What It Is
A weekend retreat where we take your phone and laptop. You don't get them
back until Sunday. No calendar. No Slack. No Zoom. Just nature, good food,
and quiet.

The Problem It Solves
Most people spend their week in back-to-back meetings. They're tired.
They're burnt out. They never get real work done. They dream of a break
but feel guilty taking one. Decline All gives them permission to disconnect.

Who It's For
Mid-level managers and team leads at tech companies. Usually 30-45 years old.
They manage 5-15 people. Their calendars are full from 9am to 5pm most days.
They make good money but have no time.

What's Included
- 2 nights at the Decline All retreat center
- All meals (fancy but simple)
- Guided walks and journaling sessions
- A "meeting audit" workshop on Saturday
- Your devices locked in a box until checkout
```

---

## Build Prompt

Use in Step 4 after attaching all input files.

```
You're an expert developer. Create a beautiful, well-structured
landing page for my product.

I'm providing 4 files:
1. Research on landing page best practices
2. The copy for my site
3. Branding JSON (colors, fonts, styles from inspiration site)
4. Screenshot of inspiration site

YOUR TASK:
- Build the page in HTML, CSS, and JavaScript
- Use ALL the copy I've provided
- Match the visual style from the inspiration
- Apply the conversion tactics from the research
- Make it responsive (mobile-friendly)

OUTPUT:
- Single HTML file with embedded CSS/JS
- Clean, readable code
- Comments for major sections

If you need anything else before starting, ask first.
```

---

## Iteration Prompts

Use in Cursor (Step 5) for focused edits.

### Element-Specific Edit

```
[After selecting an element with the element selector]

Change this section to:
- [Describe the specific change]
- [Be precise about what you want]
```

### Style Adjustment

```
Adjust the styling of this section:
- [Color change]
- [Spacing change]
- [Font change]
```

### Content Swap

```
Replace this content with:
- [New headline/text]
- Keep the same styling
```

---

## Deployment Prompts

Use in Cursor (Step 6) for deployment.

### Netlify

```
Use the Netlify CLI to connect to my instance and deploy this code live.

If the CLI isn't installed, install it first.
Walk me through the authentication if needed.
```

### Vercel

```
Use the Vercel CLI to deploy this landing page.

If the CLI isn't installed, install it first.
Walk me through the authentication if needed.
```

### Subdomain Setup

```
I need to create a subdomain for my landing page.
My domain provider is [PROVIDER NAME].
Walk me through the process step-by-step.
Make sure your instructions match the current UI as of [TODAY'S DATE].
```
