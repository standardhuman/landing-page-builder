# Prompt Templates

## Step 0: Brainstorm Product/Offer

Use these questions one at a time to clarify the product before research.

### Opening

```
I'll help you build a landing page. First, let's get clear on what you're selling.

What are you selling? Give me a quick description.
```

### Follow-up Questions (one at a time)

```
Who is this for?

Let's get specific:
- What's their job or situation?
- Age range?
- What are they struggling with right now?
```

```
What problem does this solve?

Dig into the pain:
- What's frustrating them?
- What have they tried that didn't work?
- What would their life look like if this problem was solved?
```

```
What makes this different from alternatives?

Options to consider:
1. It's faster than alternatives
2. It's simpler/easier
3. It gets better results
4. It's more affordable
5. Something else entirely

Which resonates, or is it something different?
```

```
What's included? What do they actually get?

List out the deliverables, features, or components.
```

```
Any pricing or positioning context I should know?

- Price point (or range)?
- Premium vs. accessible positioning?
- Any competitors to be aware of?
```

### Confirmation

```
Let me make sure I've got this right:

**What you're selling**: [summary]
**Who it's for**: [summary]
**Problem solved**: [summary]
**What makes it different**: [summary]
**What's included**: [summary]

Did I capture that correctly, or should we adjust anything?
```

---

## Step 1: Deep Research Prompt

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

## Step 2: Brainstorm Messaging/Copy

Use after deep research to make messaging decisions informed by findings.

### Phase 1: Review Research

```
Based on the research, here are the top insights for YOUR product:

1. [Research finding] → Here's how we could apply it: [application]
2. [Research finding] → Here's how we could apply it: [application]
3. [Research finding] → Here's how we could apply it: [application]

Let's use these to shape the messaging. First question...
```

### Phase 2: Messaging Decisions (one at a time)

```
Which pain point should we lead with?

Based on your product brief, here are the angles:
1. [Pain point A] - focuses on [aspect]
2. [Pain point B] - focuses on [aspect]
3. [Pain point C] - focuses on [aspect]

I'd recommend #[X] because [reasoning]. What do you think?
```

```
What's the headline approach?

Options (applying [research tactic]):
1. "[Headline option A]" - [why it works]
2. "[Headline option B]" - [why it works]
3. "[Headline option C]" - [why it works]

I'd lean toward #[X]. Which resonates with you?
```

```
What social proof do you have available?

- Testimonials from customers?
- Numbers (users, results, years)?
- Logos (clients, media, partners)?
- Reviews or ratings?

Tell me what you've got and we'll figure out the best placement.
```

```
What objections might visitors have?

Based on your product, likely concerns:
1. [Objection A]
2. [Objection B]
3. [Objection C]

Any others? Let's discuss how to address each.
```

```
What's the primary CTA?

Options:
1. "[Action verb] + [outcome]" (e.g., "Start Your Free Trial")
2. "[Simple action]" (e.g., "Get Started")
3. "[Urgency angle]" (e.g., "Claim Your Spot")

The research suggests [tactic]. Which fits your product best?
```

### Phase 3: Generate Copy

```
Now I'll write the full landing page copy based on our decisions:

- Pain point: [chosen]
- Headline: [chosen]
- Social proof: [what's available]
- Objection handling: [approach]
- CTA: [chosen]

Applying these research-backed tactics:
- [Tactic 1]
- [Tactic 2]
- [Tactic 3]

Writing at a 5th grade reading level...

[GENERATE FULL COPY]
```

### Legacy: Direct Copy Generation (Skip Brainstorming)

If you need to skip brainstorming and go straight to copy:

```
Create the copy for a landing page based on this product brief.

RULES:
- Write at a 5th grade reading level
- Use short sentences and simple words
- Only write the TEXT - no code
- Include all standard landing page sections

<product_brief>
[INSERT BRIEF]
</product_brief>
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
