# Single Post Generation

Generate 1 ready-to-publish LinkedIn post. The post is self-sufficient — no "comment X for free resource" CTAs, no dependency on external links or follow-ups. It can be copied, pasted, and published immediately.

## Content Method & Format

Choose ONE method for idea generation:
- **Viral Replication** — Find a proven viral post, steal the packaging, adapt the substance
- **Trend Surfing** — What's trending RIGHT NOW in your niche
- **Pain Points** — Deep audience problems with actionable solutions

Choose ONE format for content delivery:
- **Text + Personal Photo** — Post text + photo from `context/images/` matching the vibe
- **Text + AI Infographic** — Post text + Kie.ai generated infographic with reference image
- **Carousel (PDF)** — 7-11 slide carousel generated with `scripts/generate-carousel.py`

---

## CRITICAL RULES

### Quality Standards
- Write in Adam Robinson's style (see `reference/adam-robinson-writing-style.md`)
- Strong hook — first 2 lines are 80% of the work
- Deliver real value — not fluff
- Use YOUR real context: company name, real numbers, real experiences
- Specific numbers over vague claims

### Self-Sufficiency (NON-NEGOTIABLE)
- NO "Comment X and I'll send you..." CTAs (these require follow-up)
- NO "Link in comments" (LinkedIn penalizes external links)
- NO "DM me for..." (requires manual follow-up)
- Acceptable CTAs: "Follow for more", "Repost to help your network", "Save this for later", "What's your experience with...?"
- The value must be IN the post, not gated behind an action

---

## Step-by-Step Execution

### Phase 1: Ideation

1. **Read context files** to refresh understanding:
   - `context/profile.md`, `context/business.md`, `context/strategy.md`, `context/metrics.md`
   - `reference/adam-robinson-writing-style.md` (skim for voice)
   - Check last 5 posts in `posts/` to avoid recent topic repetition

2. **Generate 1 idea:**
   - Ask user which method: Viral Replication, Trend Surfing, or Pain Points
   - Ask user which format: Personal Photo, AI Infographic, or Carousel
   - (Or suggest method/format if user wants Claude to choose)
   - For Viral Replication: find a proven post and document the hook/body/visual structure to replicate
   - For Trend Surfing: find what's trending NOW and connect to user's expertise
   - For Pain Points: identify a real audience pain and frame as pain → insight → solution

3. **Assign format:**
   - For personal photo posts: pre-select which photo from `context/images/` matches the post's vibe
   - For infographics: pick which reference image to use (ref-1, ref-2, ref-3)
   - For carousels: plan slide count and illustration styles

4. **Proceed immediately to generation** — do NOT wait for user approval.

### Phase 2: Content Generation

**Determine the post number:**
- Check existing `posts/` folders for the highest NNN number
- Start new post at NNN+1

**For Text + Personal Photo post:**
1. Write the full post text in Adam Robinson's style
2. Copy the pre-selected photo from `context/images/` as `image.png`
3. Save `post.md` with metadata + copy-paste ready text

**For Text + AI Infographic post:**
1. Write the full post text
2. Generate infographic using Kie.ai with `reference_image` parameter:
   - Use one of the reference images (ref-1, ref-2, or ref-3)
   - Use the standard style prefix in the prompt
   - Describe specific layout matching the content
3. Download and save as `image.png`
4. Save `post.md`

**For Carousel post:**
1. Write the slide content (title, 5-9 numbered points with heading/subtitle/takeaway)
2. Create content JSON file
3. Run `python3 scripts/generate-carousel.py --json <file> --output posts/NNN-slug/carousel.pdf`
4. Write the companion post text (preview the carousel, don't duplicate it)
5. Save `post.md` with the post text

### Phase 3: Finalize

1. **Rebuild dashboard:** `python3 scripts/build-dashboard.py`
2. **Visual verification (MANDATORY):** Verify the post has:
   - `image.png` (for personal photo and AI infographic posts), OR
   - `carousel.pdf` + `carousel-slides/` with slide PNGs (for carousel posts)
3. **Quality check:** Verify the post has:
   - Proper post.md format with "## Post Text (copy-paste ready)" header
   - Format field in post.md matches the actual visual
4. **Report** what was created:
   - Post number, title, method, format
   - Open the dashboard: `open outputs/dashboard.html`

---

## Post Storage Format

Post in `posts/NNN-slug/`:

```
post.md           # Metadata + copy-paste ready text (MUST have "## Post Text (copy-paste ready)" header)
image.png          # For photo/infographic posts
carousel.pdf       # For carousel posts
original.md        # Original viral post (if viral replication)
original-image.jpg # Original image (if viral replication)
```

### post.md Template

```markdown
# [Post Title]

**Date created:** YYYY-MM-DD
**Method:** [Viral Replication / Trend Surfing / Pain Point]
**Format:** [Text + Personal Photo / Text + AI Infographic / Carousel]
**Platform:** LinkedIn
**Status:** Ready to publish

## Post Text (copy-paste ready)

[The actual post text goes here — ready to copy and paste into LinkedIn]

## Image Notes

[Description of the image/carousel, which reference was used, photo filename, etc.]

## Original Post (if applicable)

[Link to original, author, engagement metrics]
```
