# Landing Page Builder Skill

A 6-step workflow for creating high-converting landing pages with AI. Includes integrated deep research for evidence-based best practices.

## What's Different About This Skill?

Most landing page tutorials use a single search query for research. This skill uses a **multi-source research protocol** that:

- Searches 5 query variations in parallel
- Triangulates findings across authoritative sources
- Marks claims as [Verified] (2+ sources) or [Single source]
- Notes contradictions instead of hiding them
- Cites every tactic with URLs

The result: Research-backed landing pages, not AI-generated guesses.

## Installation

### Option 1: Clone to Skills Directory

```bash
# Navigate to your Claude Code skills directory
cd ~/.claude/skills

# Clone this repository
git clone https://github.com/YOUR_USERNAME/landing-page-builder.git
```

### Option 2: Manual Installation

1. Download this repository as a ZIP
2. Extract to `~/.claude/skills/landing-page-builder/`
3. Restart Claude Code

## The 6-Step Workflow

```
1. DEEP RESEARCH → 2. COPY → 3. INSPIRATION → 4. BUILD → 5. ITERATE → 6. DEPLOY
```

| Step | What Happens | Time |
|------|--------------|------|
| **1. Deep Research** | Multi-source research on current best practices | 15-30 min |
| **2. Copy** | Generate all landing page text from product brief | 15-30 min |
| **3. Inspiration** | Collect branding JSON + screenshot from example site | 5-10 min |
| **4. Build** | Combine all inputs to generate HTML/CSS/JS | 10-20 min |
| **5. Iterate** | Refine in Cursor with element selection | 15-30 min |
| **6. Deploy** | Push live with Netlify or Vercel CLI | 5-10 min |

**Total**: ~1.5-2 hours for a complete, research-backed landing page.

## Usage

In Claude Code, simply say:

```
/landing-page-builder
```

Or describe what you want:

```
Build me a landing page for my product
```

The skill will guide you through each step.

## File Structure

```
landing-page-builder/
├── SKILL.md                 # Main skill file (6-step workflow)
├── README.md                # This file
└── references/
    ├── deep-research-protocol.md  # Research methodology
    ├── prompts.md                 # All prompt templates
    └── tools.md                   # Tool setup guides
```

## Prerequisites

- [Claude Code](https://claude.ai/code) installed
- [Cursor](https://cursor.com) (for Step 5 - $20/mo recommended)
- Netlify or Vercel account (for Step 6 - free tier works)
- Optional: [Firecrawl](https://firecrawl.dev) account (for Step 3 - free tier)

## Deep Research for Other Topics

This skill includes a simplified version of the Deep Research system for landing page research.

For comprehensive research on **any** topic, see the full system:

- [Claude Code Deep Research](https://github.com/anthropics/claude-code-deep-research)
- 7-phase process with Graph of Thoughts
- Multi-agent orchestration
- Hypothesis testing and verification

## Credits

- Landing page workflow adapted from proven conversion optimization practices
- Deep research methodology from [Claude Code Deep Research](https://github.com/anthropics/claude-code-deep-research)
- Original concept by Ankit at [MyBCAT](https://mybcat.com)

## License

MIT License - Use freely, modify as needed.
