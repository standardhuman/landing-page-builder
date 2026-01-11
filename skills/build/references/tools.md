# Tools Reference

## Firecrawl (Step 3)

Extract branding data from any website for design inspiration.

### Setup

1. Go to [firecrawl.dev](https://firecrawl.dev)
2. Sign up / log in (free tier available)
3. Navigate to **Playground** in the left sidebar

### Usage

1. Paste your inspiration site's URL
2. **Important**: Uncheck "markdown", check "branding"
3. Click "Start Scrape"
4. Download the JSON file

### What You Get

The JSON contains:
- Theme colors (primary, secondary, accent)
- Button styles and shapes
- Typography (fonts, sizes)
- Image references

### Example Output

```json
{
  "colors": {
    "primary": "#2563eb",
    "secondary": "#1e40af",
    "accent": "#f59e0b",
    "background": "#ffffff",
    "text": "#1f2937"
  },
  "fonts": {
    "heading": "Inter",
    "body": "Inter"
  },
  "buttons": {
    "radius": "8px",
    "style": "solid"
  }
}
```

**Cost**: Free tier available

---

## Full-Page Screenshots (Step 3)

Capture entire landing pages using Chrome's built-in tool.

### Steps

| Step | Mac | Windows |
|------|-----|---------|
| 1. Open DevTools | `Cmd + Option + I` | `Ctrl + Shift + I` |
| 2. Open Command Palette | `Cmd + Shift + P` | `Ctrl + Shift + P` |
| 3. Type | `screenshot` | `screenshot` |
| 4. Select | "Capture full size screenshot" | (same) |

Chrome automatically scrolls the page and downloads a full-page PNG.

### Why Full-Page?

- Captures the complete visual hierarchy
- Shows the entire content flow and structure
- Gives AI better context than a viewport-only screenshot

### Tips

- Wait for the page to fully load before capturing
- Some sites with lazy-loading may need manual scrolling first
- If the screenshot is too large, crop to key sections

---

## Cursor (Step 5)

AI-powered code editor for refining your landing page.

### Setup

1. Download from [cursor.com](https://cursor.com)
2. Subscribe to Pro ($20/mo) for best models
3. Sign in

### Project Setup

1. Create a folder on your desktop (e.g., `landing-page/`)
2. Download the HTML from your chat
3. Move the HTML file into the folder
4. Open Cursor → File → Open Folder → Select your folder

### Browser Preview

1. Click the globe icon in the toolbar to open preview
2. If you see an error, share it with AI to fix
3. Once working, you'll see live updates as you edit

### Element Selection (Key Feature)

This is the most important feature for landing page iteration.

1. Click the **mouse icon with a box** ("Select element")
2. Hover over the preview - blue boxes highlight sections
3. Click on the section you want to edit
4. The AI now focuses ONLY on that section's code
5. Describe your change
6. Accept the edit

**Why this matters**: Without element selection, AI might make changes across the entire file. With it, changes are focused and predictable.

### Recommended Workflow

```
1. Select element
2. Use a high-end model (Claude Opus, GPT-4+)
3. Describe the change clearly
4. Accept changes
5. Check the preview
6. Repeat

After 2-3 edits, start a fresh chat (click + button)
```

### Model Selection

For landing page work, use:
- **Claude Opus 4** (best quality)
- **GPT-4** (good alternative)
- **Claude Sonnet** (good balance of speed/quality)

Avoid cheaper models for design work - they make more mistakes.

---

## Deployment

### Netlify (Recommended for Static Sites)

Free hosting with easy CLI deployment.

#### Setup

1. Create account at [netlify.com](https://netlify.com)
2. Create your subdomain in your domain provider first

#### CLI Deployment

In Cursor, open a new chat and say:

```
Use the Netlify CLI to connect to my instance and deploy this code live.
```

The AI will:
1. Install the Netlify CLI if needed (`npm install -g netlify-cli`)
2. Prompt you to authenticate (opens browser)
3. Link your project to Netlify
4. Deploy your code
5. Return the live URL

#### Custom Domain

After deployment, in the Netlify dashboard:
1. Go to Site settings → Domain management
2. Add your custom domain
3. Follow the DNS instructions

**Cost**: Free tier is generous for landing pages

---

### Vercel (Alternative)

Popular for frontend projects, similar workflow to Netlify.

#### Setup

1. Create account at [vercel.com](https://vercel.com)
2. Create your subdomain in your domain provider first

#### CLI Deployment

In Cursor, open a new chat and say:

```
Use the Vercel CLI to deploy this landing page.
```

The AI will:
1. Install the Vercel CLI if needed (`npm i -g vercel`)
2. Prompt you to authenticate
3. Deploy your code
4. Return the live URL

#### Vercel vs Netlify

| Feature | Vercel | Netlify |
|---------|--------|---------|
| Ease of use | Excellent | Excellent |
| Free tier | Generous | Generous |
| CLI | `vercel` | `netlify` |
| Best for | React/Next.js | Static HTML |

For simple landing pages, both work equally well. Use whichever you prefer.

**Cost**: Free tier available

---

### Subdomain Setup

If you need help setting up a subdomain for your landing page, ask:

```
I need to create a subdomain [product].mydomain.com.
My domain provider is [PROVIDER NAME].
Give me step-by-step instructions for the current UI.
```

Common providers:
- Cloudflare
- GoDaddy
- Namecheap
- Google Domains
- Route 53 (AWS)

The AI will walk you through creating a CNAME record pointing to your Netlify/Vercel deployment.

---

## AI Chat Platforms (Steps 1-4)

Use the best model available for each step.

### Recommended Models

| Platform | Best Model | When to Use |
|----------|------------|-------------|
| Claude | Opus 4.5 | Research, copy, building |
| Claude | Sonnet | Quick iterations |
| OpenAI | GPT-4+ | Alternative for all steps |

### Extended Thinking/Reasoning

For Steps 1 (Research) and 4 (Build), enable extended thinking if available:
- Claude: Extended thinking mode
- OpenAI: High reasoning mode

This produces higher quality output for complex tasks.

### Iteration Limit

Do **1-2 iterations** in chat, then move to Cursor.

> The more conversation history in a chat, the less context the AI has
> for your actual request. Fresh chats = better output.

---

## File Organization

Keep your landing page project organized:

```
landing-page-[product]/
├── research/
│   └── landing-page-conversion-playbook-2025.md
├── copy/
│   └── [product-name]-landing-page-copy.md
├── inspiration/
│   ├── www.example.com.json
│   └── example-screenshot.png
└── build/
    └── index.html
```

This makes it easy to:
- Reference materials when iterating
- Share the project with others
- Version control with git
