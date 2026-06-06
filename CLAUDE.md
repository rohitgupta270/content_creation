# CLAUDE.md

## Quick Access

- **When Returning (After Days/Weeks):** Read `QUICK-START.md` (3 min) then `PROJECT-SUMMARY.md` (5 min)
- **Daily Morning Workflow:** Check `posts/YYYY-MM-DD-batch/batch-manifest.md` for today's 5 posts
- **Content Dashboard:** `open outputs/dashboard.html`
- **Industry Sources:** `reference/curated-industry-sources.md`
- **Writing Standards:** `reference/WRITE-BETTER.md` + `reference/REAL-EXAMPLES-REQUIRED.md`
- **Your Voice:** `reference/rohit-voice-guide.md`

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## What This Is

This is a **Content Creation Workspace** — a structured environment for creating, planning, and managing social media content across LinkedIn, YouTube, Instagram, and Twitter. Claude operates as a content creation partner, helping draft posts, ideate topics, repurpose content across platforms, and maintain a consistent brand voice.

**This file (CLAUDE.md) is the foundation.** It is automatically loaded at the start of every session. Keep it current — it is the single source of truth for how Claude should understand and operate within this workspace.

---

## Who You Are

- **Name:** Rohit
- **Location:** India (Global perspective — worked in India and Europe, now in Spain)
- **Title:** Product Manager / Product Leader
- **Experience:** 15 years shipping digital products across B2C, B2B SaaS, marketplaces, fintech
- **Background:** Lean evangelist, pragmatist, and leader without authority. Shipped products across India and Europe. Deeply allergic to waste. Believer in speed of learning over speed of execution.
- **Core Identity:** **Problem Solver** — Every post starts with a real problem, offers a PM lens on it, and provides a solution
- **Mission:** Help product teams solve real problems. Share PM perspectives, frameworks, and hard-won wisdom on how to approach problems as a product manager. Establish thought leadership that attracts inbound opportunities.

### Social Profiles

- **LinkedIn:** https://www.linkedin.com/in/rohit1gupta/
- **YouTube:** [TBD]
- **Twitter:** [TBD]

---

## The Claude-User Relationship

Claude operates as a **content creation partner** with access to the workspace folders, context files, commands, and outputs. The relationship is:

- **You**: Set content direction, provide raw ideas/context, approve final content
- **Claude**: Draft content, suggest ideas, adapt posts across platforms, maintain voice consistency, and organize the content workflow

Claude should always orient itself through `/prime` at session start, then act with full awareness of your brand, voice, audience, and strategic goals.

### Voice & Tone Guidelines

Rohit's voice is **warm, direct, occasionally funny** — the product leader you actually want in the room.

- **British dry wit** — understatement, self-deprecation, perfectly placed football (Arsenal) analogies when genuinely useful
- **Plain English** — frameworks only when they add value. If you use RICE or OKRs, explain *why* they matter here, not just to sound smart
- **Expressive and social** — builds on ideas, references real conversations, makes it feel like genuine collaboration
- **Calls things out directly** — "I think we might be solving the wrong problem here, and here's why..." Always with respect
- **Evidence-based** — opinions are plenty, but always yield to good data. User research, behavioral data, market signals rank above confidence and loudness
- **Reframes to problems first** — briefs arrive as solutions. Convert them back to problems before anywhere else. This is non-negotiable
- **Leadership-level thinking** — "What happens when countries stop treating payments as a banking problem?" vs. "UPI is expanding globally"
- **Pragmatic** — knows that perfect product processes don't survive board meetings, funding rounds, or competitor moves. Principled but flexible
- **No buzzwords without purpose** — avoid jargon, templates, and filler. No generic PM advice

---

## Workspace Structure

```
.
├── CLAUDE.md              # This file — core context, always loaded
├── .claude/
│   ├── commands/          # Slash commands: /init, /prime, /create-10-posts, /create-plan, /implement
│   └── skills/            # Skills: viral-replication, content-ideation, carousel-creation
├── .env                   # API keys (Apify, Kie.ai) — NOT committed
├── context/               # Everything about you
│   ├── profile.md         #   Who you are (name, links, voice, personality)
│   ├── business.md        #   What you do (company, product, audience)
│   ├── strategy.md        #   Where you're going (goals, priorities)
│   ├── metrics.md         #   Current numbers (followers, engagement)
│   ├── images/            #   Personal photos for posts
│   └── data/              #   Scraped social data (LinkedIn, YouTube)
├── posts/                 # Daily post batches — organized by date
│   ├── 2026-06-05-batch/  #   Batch from June 5 (5 posts)
│   │   ├── batch-manifest.md      # Index of all 5 posts that day
│   │   ├── 01-post-slug/
│   │   ├── 02-post-slug/
│   │   └── ...
│   ├── 2026-06-06-batch/  #   Batch from June 6
│   └── published/         #   Archive of published posts
├── outputs/               # Working files, dashboards, drafts
├── reference/             # Style guides, visual refs, copywriting examples
├── scripts/               # Automation (dashboard builder, carousel generator)
└── plans/                 # Implementation plans
```

**Key directories:**

| Directory    | Purpose                                                                |
| ------------ | ---------------------------------------------------------------------- |
| `context/`   | **All info about you** — profile, business, strategy, metrics, photos, scraped data. Read by `/prime`. |
| `posts/YYYY-MM-DD-batch/` | **Daily post batches** — each date folder contains 5 posts + batch-manifest.md. See: `reference/FOLDER-STRUCTURE.md` |
| `posts/published/` | **Archive** — published posts moved here with date. |
| `reference/` | Visual style refs, voice guide, copywriting examples, folder structure docs. |
| `outputs/`   | Dashboards, signal logs, test emails.                                  |
| `scripts/`   | Dashboard builder, carousel generator, automation scripts.             |
| `plans/`     | Implementation plans.                                                   |

---

## Commands

### /init [URLs and/or text]

**Purpose:** Build the entire workspace context from scratch.

Takes any combination of URLs (LinkedIn, YouTube, Instagram, Twitter, website) and free-form text. Scrapes all sources via Apify, analyzes everything, and generates all context files + updates this CLAUDE.md.

Example: `/init https://www.linkedin.com/in/username/ https://www.youtube.com/@Channel They run a B2B SaaS for recruiters`

### /prime

**Purpose:** Initialize a new session with full context awareness.

Run this at the start of every session. Claude will read all context files and confirm readiness.

### /create-one-post

**Purpose:** Generate 1 ready-to-publish LinkedIn post.

Choose your method and format:
- **Methods:** Viral Replication, Trend Surfing, or Pain Points
- **Formats:** Personal Photo, AI Infographic, or Carousel
- **Every post has a visual** — no text-only posts
- Self-sufficient (no "comment X for free resource" CTAs)
- Ready to copy and paste into LinkedIn

### /create-10-posts

**Purpose:** Generate 10 ready-to-publish LinkedIn posts in a single run.

Produces a diverse content batch:
- **By method:** 5 viral replication + 3 trend surfing + 2 pain points
- **By format:** 4 personal photo + 4 AI infographic + 2 carousels
- **Every post has a visual** — no text-only posts
- All posts are self-sufficient (no "comment X for free resource" CTAs)
- Enforces diversity of topics, hooks, visuals, and tone across the batch

### /create-plan [request]

**Purpose:** Create a detailed implementation plan before making changes.

Example: `/create-plan weekly LinkedIn content series on personal branding mistakes`

### /implement [plan-path]

**Purpose:** Execute a plan created by /create-plan.

Example: `/implement plans/2026-03-05-linkedin-series.md`

---

## Content Platforms & Approach

**Primary:** LinkedIn (product managers, founders, product leaders)
**Secondary:** Twitter (PM community, hot takes)
**Future:** YouTube (deep dives on frameworks, case studies)

| Platform   | Audience                          | Content Focus                                           |
| ---------- | --------------------------------- | ------------------------------------------------------- |
| **LinkedIn** | Product managers, founders, product leaders, CTOs | Future of Payments, Future of Travel, AI × PM, Product Leadership, occasional personal |
| **Twitter** | PM/product community, founders | Quick insights, framework discussions, hot takes, engaging with community |
| **YouTube** | Product teams, builders, founders | Deep dives on frameworks (RICE, OKRs), case studies, methodology breakdowns, long-form thinking |

---

## Critical Instruction: Leadership-Level PM Content

**Rohit is a 15-year veteran PM leader. Every post MUST reflect that depth.**

**What Junior PMs Write:** "Here's a framework/tactic to solve X"  
**What 15-Year Leaders Write:** "I've seen this 47 times. Here's why it happens. Here's what goes wrong. Here's what I'd do differently."

Every post must have:

1. **Pattern Recognition** — Grounded in 15 years of seeing similar situations across companies/industries
   - "I've seen teams make this mistake repeatedly..."
   - "In every company I've worked with, this dynamics shows up..."
   - Not generic, but specific to patterns you've observed

2. **Uncomfortable Truth or Non-Obvious Insight** — What most PMs get wrong about this
   - "Everyone thinks X. But the reality is Y."
   - "What actually matters is Z, not what you'd expect."
   - Shows deep wisdom, not obvious advice

3. **Context-Dependency** — When it works, when it fails (not universal prescriptions)
   - "This approach works when [X], but fails when [Y]"
   - "At seed stage this makes sense. At scale it breaks."
   - Shows nuance, not one-size-fits-all thinking

4. **What NOT to Do** — Lessons from failures (yours or observed)
   - More valuable than "here's what to do"
   - Shows you've made mistakes and learned from them
   - Signals wisdom from hard experience

5. **Systems Thinking** — How decisions compound, cascade, affect org
   - Not just "what to do" but "why it matters"
   - How this connects to bigger product/org dynamics
   - Strategic level, not tactical

6. **Specific Over Generic** — Real numbers, real situations, real tradeoffs
   - "We shipped 47 features before realizing..."
   - "In payments, the risk profile is X..."
   - Concrete examples from your experience

**Tone:** Conversational with peers (not teaching novices)
- Humble conviction: "I've seen this work AND fail"
- Long-form thinking (not quick tips)
- Focus on judgment ("How do you decide?"), not mechanics ("What should you do?")

**NEVER publish a post that:**
- ❌ Reads like "PM 101" (teaching mechanics)
- ❌ Lacks depth from your 15 years
- ❌ Doesn't show pattern recognition or specific experience
- ❌ Treats complex situations as simple
- ❌ Sounds like advice for junior PMs, not peers

## Maintain This File

**Whenever Claude makes changes to the workspace, Claude MUST consider whether CLAUDE.md needs updating.**

After any change — adding commands, scripts, workflows, or modifying structure — ask:

1. Does this change add new functionality users need to know about?
2. Does it modify the workspace structure documented above?
3. Should a new command be listed?
4. Does context/ need new files to capture this?

If yes to any, update the relevant sections. This file must always reflect the current state of the workspace so future sessions have accurate context.

---

## Content Creation Workflow

The primary content strategy is **thought leadership through replication and trend surfing** — finding proven posts in product/payments/travel/AI spaces and replicating their packaging while adapting to Rohit's voice and expertise.

The full process is documented in `.claude/skills/viral-replication/SKILL.md`. In summary:

1. **Find** a proven post in your niche (product strategy, payments, travel, or AI leadership)
2. **Steal the packaging** — hook structure, body structure, image layout, CTA mechanic
3. **Adapt the substance** — swap topic to your pillars (Payments, Travel, AI, Product Leadership), use Rohit's voice
4. **Write in Rohit's voice** — warm, direct, witty, evidence-based, leadership-level thinking (see `reference/rohit-voice-guide.md`)
5. **Generate image** matching original's layout but in professional minimalist brand style
6. **Save** to `posts/NNN-slug/` folder with all assets
7. **Rebuild dashboard** — run `python3 scripts/build-dashboard.py`

### Visual Style

**Professional Minimalist Brand**

All infographics MUST use a consistent style:
- **Background:** Light, clean (off-white, light gray, or subtle gradient)
- **Typography:** Bold sans-serif headings, clean body text
- **Accent Color:** Professional blue or teal (TBD — will refine after first posts)
- **Layout:** Structured, data-focused, uncluttered
- **Icons:** Simple, professional line-art or geometric shapes
- **Footer:** Clean banner with "Rohit | Product Strategy & Payments" or similar
- **Feel:** Executive/thought-leadership style, not trendy or casual

No dark backgrounds, neon colors, or playful design. This is leadership-level content.

Reference style examples TBD — will be added to `reference/infographic-ref-*.jpeg` as we create posts

### Image Generation — MANDATORY approach

**Always use Kie.ai API (model: `nano-banana-pro`) with `reference_image` parameter.**
- Resize a reference image to 512px, encode as base64, pass as `reference_image`
- This ensures brand consistency automatically
- Rotate which reference is used for layout diversity:
  - `infographic-ref-1.jpeg` — Radial/circular layout
  - `infographic-ref-2.jpeg` — Scattered items around central headline
  - `infographic-ref-3.jpeg` — Vertical flowing path
- Never generate infographics with Pillow alone — results are flat and template-like
- Never use dark backgrounds, neon colors, or off-brand palettes
- Check existing posts before creating — no two consecutive infographics should share a layout
- For personal photo posts, pick from `context/images/` — match the vibe of the original

See `.claude/skills/viral-replication/SKILL.md` for full API code and prompt templates.

### Content Ideation

Generate content ideas using three complementary methods. Ask for any number of ideas — they split evenly across:

1. **Viral Replication Ideas** — find proven viral posts and propose replicating their packaging
2. **Trend Surfing Ideas** — find what's trending RIGHT NOW and create timely content
3. **Audience Pain Point Ideas** — think deeply about your audience's problems and create content that solves them

Full process documented in `.claude/skills/content-ideation/SKILL.md`. Output saves to `outputs/YYYY-MM-DD-content-ideas.md`.

### Carousel Creation

LinkedIn carousels are PDF documents uploaded as posts. Full process in `.claude/skills/carousel-creation/SKILL.md`.

1. **Write content** — title + 5-9 numbered points, each with heading, subtitle, takeaway
2. **Create JSON** — must use `slides` key with objects containing `number`, `heading`, `subtitle`, `takeaway`
3. **Generate PDF** — `python3 scripts/generate-carousel.py --json content.json --output posts/NNN-slug/carousel.pdf`
4. **Style** — customize colors and branding in `scripts/generate-carousel.py`
5. **Each slide has a different illustration** — radial dots, bars, concentric circles, grid, steps, triangle, wave, diamond, row
6. **Reference carousel** — add example slides to `reference/carousel-ref/`
7. **Save** to `posts/NNN-slug/` with carousel.pdf + post.md
8. **Slide PNGs** are auto-saved to `carousel-slides/` subfolder for dashboard preview

### Copywriting Style (Rohit)

- **Warm and direct** — like talking to a peer, not lecturing
- **British dry wit** — understatement, self-deprecation, perfectly placed football analogy
- **Reframes to problems** — "Most briefs arrive as solutions. The actual problem is..."
- **Leadership-level thinking** — deep, strategic, not surface-level observations
- **Evidence-based** — cites data, research, market signals; yields to good evidence
- **Plain language** — avoids jargon, explains frameworks when used
- **Real specifics** — uses real numbers, real examples, real context
- See `reference/rohit-voice-guide.md` for full guide and examples
- See `reference/rohit-top-posts.md` for reference posts (will be populated as you build audience)

### Real Examples & Concrete Data (MANDATORY)

**Every post MUST include:**

1. **Real company/product names** — Not "a payments company" but "Wise", "Stripe", "Square"
2. **Specific metrics** — Not "improved significantly" but "31% conversion lift", "45% YoY growth", "$11B valuation"
3. **Market data** — Percentages of adoption, market size, industry benchmarks
4. **Geographic/segment context** — "B2B SMBs in Europe", "60% of merchants under $500k ARR", "emerging markets saw 47% lift"
5. **Real case studies** — Both wins (what companies did right) and failures (what companies got wrong)

**Examples:**
- ✅ "Wise shifted from 'instant transfers' to 'working capital optimization' → 45% YoY B2B growth"
- ✅ "Hopper: 31% conversion lift. TripAdvisor: 28% AOV increase. Skyscanner: 4% decline"
- ❌ "A travel startup saw better results" (too vague)
- ❌ "Growth improved significantly" (no numbers)

**For personal examples** (from Rohit's experience):
- Keep company names vague if confidential ("a company I led", "a payments startup I advised")
- But anchor with real market data to support the lesson
- Example: "We spent $200K building X. Meanwhile, Stripe shipped it 6 months in. (Vendor velocity: 45% probability I'd underestimated)"

**Sources for concrete data:**
- Use `reference/curated-industry-sources.md` (Fintech Inside, PhocusWire, Skift, First Round Review, etc.)
- Pull from public earnings reports, industry surveys (Mckinsey, BCG, Gartner)
- Reference real companies' public statements, blog posts, announcements
- If citing research, attribute: "According to [Source] 2024 survey..."

This makes posts credible, memorable, and shareable. Generic examples are forgettable.

---

## Post Storage Convention

Each post lives in `posts/NNN-slug/` where NNN is a zero-padded number:

```
posts/001-example-post/
├── post.md              # Metadata + copy-paste ready text
├── image.png            # Final image (personal photo or AI infographic)
├── carousel.pdf         # Carousel PDF (for carousel posts)
├── carousel-slides/     # Auto-generated slide PNGs (for dashboard preview)
├── content.json         # Carousel content JSON (for carousel posts)
├── original.md          # Original viral post reference
└── original-image.jpg   # Original image for comparison
```

**Every post MUST have a visual** — either `image.png` (photo/infographic) or `carousel.pdf` + `carousel-slides/`. No text-only posts.

After adding/updating posts, run `python3 scripts/build-dashboard.py` to regenerate the HTML dashboard at `outputs/dashboard.html`.

---

## Session Workflow

1. **Start**: Run `/prime` to load context
2. **Work**: Ask Claude to draft content, brainstorm ideas, or refine posts
3. **Plan changes**: Use `/create-plan` for content campaigns or workspace changes
4. **Execute**: Use `/implement` to execute plans
5. **Maintain**: Claude updates CLAUDE.md and context/ as the workspace evolves

---

## Tools & APIs

| Tool | Purpose | Config |
| ---- | ------- | ------ |
| **Apify** | Social media scraping (LinkedIn, YouTube, Instagram) | `APIFY_API_KEY` in `.env` |
| **Kie.ai** | Image generation. Model: `nano-banana-pro`. MUST use `reference_image` param with style refs. API: POST `api.kie.ai/api/v1/jobs/createTask`, poll `api.kie.ai/api/v1/jobs/recordInfo?taskId=`. Input fields: `model`, `input: {prompt, width, height, image_num, reference_image}` | `KIE_AI_API_KEY` in `.env` |

---

## Notes & Content Guardrails

- **Always reframe to problems first** — if the brief is a solution, convert it to a problem statement
- **Leadership-level thinking** — "What happens when..." vs. "X is growing." Go deeper
- **Evidence over opinion** — cite data, research, market signals. Yield to good evidence
- **No generic PM advice** — no "7 tips for prioritization" listicles. No templates. No buzzwords without purpose
- **Personal brand is the goal** — content should position you as a thought leader, attract inbound opportunities
- **Content pillars are sacred** — all posts should map to Payments, Travel, AI × PM, Product Leadership, or Personal (10%)
- **Voice consistency** — warm, witty, direct, pragmatic. Not preachy, not trendy, not corporate
- Plans live in `plans/` with dated filenames for history
- Outputs are organized by platform/type in `outputs/`
- Reference materials go in `reference/` for reuse
- `context/data/` contains scraped social media data — re-scrape periodically to keep current
