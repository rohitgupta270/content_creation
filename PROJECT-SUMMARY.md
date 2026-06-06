# LinkedIn Content Creation System — Project Summary

**Built:** June 5, 2026  
**Status:** Ready for daily use  
**Next Action:** Daily morning post generation at 8:00 AM

---

## What We've Built

A **complete LinkedIn content creation system** for Rohit that generates 5 ready-to-publish posts daily (one per content pillar) with:

- ✅ Diversified content across 5 pillars (Payments 40%, Leadership 25%, AI×PM 15%, Travel 10%, Personal 10%)
- ✅ Leadership-level writing (15-year PM expertise, specific examples, real data)
- ✅ Real company names + concrete metrics (Wise, Stripe, Hopper with 31% lifts, $11B valuations, etc.)
- ✅ Consistent voice & tone (warm, direct, witty, evidence-based)
- ✅ Quality standards enforced (no em dashes, active voice, specific examples)
- ✅ Date-organized batch folders (posts/YYYY-MM-DD-batch/)
- ✅ Daily manifests showing all 5 posts + recommendations
- ✅ Reference sources for deeper context (FinTech Inside, PhocusWire, McKinsey, etc.)

---

## Critical Files (Must Know These)

### **Daily Workflow Files**

| File | Purpose | When to Use |
|------|---------|------------|
| `posts/2026-06-05-batch/batch-manifest.md` | Index of all 5 posts + recommendations | Every morning — read to pick which posts to publish |
| `posts/2026-06-05-batch/0X-post-slug/post.md` | Ready-to-publish post text | Copy text → paste into LinkedIn |
| `posts/2026-06-05-batch/0X-post-slug/` | Complete post folder (text + images + references) | For visual preview + learning |

### **Core Configuration Files**

| File | Purpose | Change When |
|------|---------|-------------|
| `CLAUDE.md` | Master project config — identity, voice, strategy, commands | You update settings; Claude reads for context |
| `context/profile.md` | Who you are (15 years, expertise areas, personality) | Update if background/focus changes |
| `context/business.md` | What you do (personal branding, target audience, pain points) | Update if positioning changes |
| `context/strategy.md` | Where you're going (pillars 40/25/15/10/10, publishing strategy) | Update if strategy shifts |

### **Quality Standards (Non-Negotiable)**

| File | Purpose | For Whom |
|------|---------|----------|
| `reference/WRITE-BETTER.md` | 10 writing rules + 1 examples rule | Claude checks EVERY post against this |
| `reference/REAL-EXAMPLES-REQUIRED.md` | Real company names, metrics, market data standard | Claude uses this to generate quality posts |
| `reference/rohit-voice-guide.md` | Your authentic voice (warm, direct, witty) | Claude uses this to write in your voice |
| `reference/curated-industry-sources.md` | 40+ industry sources (Tier 1 & 2) | Claude pulls examples and data from these |

### **Context & Intelligence Files**

| File | Purpose | Contains |
|------|---------|----------|
| `context/images/` | Your personal photos | Use for text + personal photo posts |
| `reference/curated-industry-sources.md` | FinTech Inside, PhocusWire, Skift, McKinsey, etc. | Data sources for real examples + metrics |

### **Dashboard & Outputs**

| File | Purpose |
|------|---------|
| `outputs/dashboard.html` | Visual preview of all posts (open in browser) |
| `posts/published/` | Archive of posts you've already published |

---

## How to Run the Project — Daily Workflow

### **Every Morning (8:00-8:30 AM)**

1. **Generate 5 new posts** (Claude will do this automatically if automated, or you request it):
   ```bash
   # Posts will be saved to posts/YYYY-MM-DD-batch/ folder
   ```

2. **Review the batch**:
   ```bash
   # Read the index
   cat posts/2026-06-XX-batch/batch-manifest.md
   ```

3. **Pick which post(s) to publish**:
   - Read 1-5 posts from the batch
   - Choose based on:
     - Topic (what fits today's audience conversation?)
     - Pillar diversity (did you post Payments yesterday? Pick Travel/AI/Leadership/Personal today)
     - Your energy (which one resonates with you?)

4. **Publish to LinkedIn**:
   - Open the post file: `cat posts/2026-06-XX-batch/0X-post-slug/post.md`
   - Copy the post text
   - Paste into LinkedIn
   - Add image if available (stored in the post folder)
   - Schedule or post immediately
   - Post at 8:30 AM your time (or 10-11 PM ET if US audience)

5. **Engage** (critical for algorithm):
   - Reply to your own post within 10 minutes (adds a comment, kickstarts engagement)
   - Spend 30 min replying to others' comments on your post
   - This matters more than the post itself for LinkedIn reach

### **Example: First Morning**
```
Morning 1: Read batch-manifest.md
→ Post 1 (Payments): "Everyone Says Real-Time Payments Are About Speed"
   (strong strategic content, good hook)
→ Post 4 (Leadership): "Your Biggest Product Decisions Aren't About Features"
   (high engagement potential, identity clarity resonates)
```

```
Morning 2: Read NEW batch-manifest.md
→ Different 2 posts from new batch (rotate pillars)
```

```
Morning 3: Post 1 post per day (less is more)
→ Pick the strongest one from that day's batch
```

---

## How to Run When You Return (After Days/Weeks Away)

### **Step 1: Orient Yourself (5 min)**
```bash
cd /Users/rohit.gupta/claudecode/personal_projects/content_linkedin/content-creation-template

# Run primer to load all context
# In Claude: "/prime"
```

This loads:
- Who you are (profile.md)
- What you do (business.md)
- Your strategy (strategy.md)
- Your voice (rohit-voice-guide.md)
- Quality standards (WRITE-BETTER.md, REAL-EXAMPLES-REQUIRED.md)

### **Step 2: Check What's Ready**
```bash
# See latest batch
ls -la posts/ | grep batch | tail -1

# Read today's manifest
cat posts/2026-06-XX-batch/batch-manifest.md
```

This shows you:
- 5 posts ready to go
- Which pillar each covers
- Key insight + difficulty level
- Recommendations for what to post

### **Step 3: Pick & Publish**
- Read posts you like
- Copy text → LinkedIn
- Post at 8:30 AM
- Engage in first hour (comment, reply)

### **Step 4: Track What You've Published**
```bash
# Move published posts to archive (optional, for tracking)
mv posts/2026-06-XX-batch/0X-post-slug posts/published/

# Or just keep them in the batch folder and remember which you posted
```

---

## Weekly Tasks (Optional But Recommended)

### **Every Friday: Refresh Industry Sources**
```bash
# Review curated-industry-sources.md
# Scan Tier 1 sources (FinTech Inside, PhocusWire, The Batch, etc.)
# Note emerging trends/companies/numbers
```

This keeps posts current and data-backed.

### **Every 2 Weeks: Review Your Engagement**
```bash
# Check LinkedIn analytics
# Which posts got best engagement?
# Which pillar resonates most?
# Update strategy if needed
```

---

## Important Commands Reference

When you return and want to work with Claude:

```bash
# Start fresh session
/prime              # Load all context, confirm readiness

# Generate posts
/create-one-post    # Generate 1 post (choose method + format)
/create-10-posts    # Generate 10 posts (all pillars + formats)

# Check existing posts
ls posts/
cat posts/2026-06-XX-batch/batch-manifest.md
cat posts/2026-06-XX-batch/0X-post-slug/post.md

# View dashboard
open outputs/dashboard.html
```

---

## File Structure at a Glance

```
content-creation-template/
├── CLAUDE.md                                      # Master config
├── PROJECT-SUMMARY.md                            # This file
├── context/
│   ├── profile.md                                # Your bio
│   ├── business.md                               # Your positioning
│   ├── strategy.md                               # 5 pillars + strategy
│   └── images/                                   # Your photos
├── posts/
│   ├── 2026-06-05-batch/                        # Today's posts
│   │   ├── batch-manifest.md                    # Index of 5 posts
│   │   ├── 01-real-time-liquidity/              # Post 1 (Payments)
│   │   ├── 02-travel-personalization/           # Post 2 (Travel)
│   │   ├── 03-ai-product-orgs/                  # Post 3 (AI×PM)
│   │   ├── 04-identity-decisions/               # Post 4 (Leadership)
│   │   └── 05-learning-from-failure/            # Post 5 (Personal)
│   └── published/                                # Archive of published posts
├── reference/
│   ├── WRITE-BETTER.md                          # 10 writing rules
│   ├── REAL-EXAMPLES-REQUIRED.md                # Real data standard
│   ├── rohit-voice-guide.md                     # Your voice
│   └── curated-industry-sources.md              # 40+ industry sources
└── outputs/
    └── dashboard.html                            # Visual preview
```

---

## Quality Checklist (Before Publishing Any Post)

Every post Claude generates will have these:

- ✅ Real company names (Wise, Stripe, Hopper — not "a startup")
- ✅ Specific metrics (31% lift, 45% growth, $11B — not "improved")
- ✅ Market context (B2B SMBs, emerging markets, 67% of travelers)
- ✅ Real case studies (both wins and losses)
- ✅ Data sources cited (McKinsey 2024, Phocuswire report)
- ✅ No em dashes (replaced with comma, colon, or restructure)
- ✅ Active voice (subject performs action, not receives it)
- ✅ No hedging language ("I think", "maybe", "arguably" — removed)
- ✅ Evidence-based (yields to data, not opinion)
- ✅ Leadership-level thinking (pattern recognition from 15 years, not "7 tips")
- ✅ Rohit's authentic voice (warm, direct, witty, pragmatic)

---

## Common Questions When You Return

**Q: How do I generate new posts?**  
A: Run `/prime` to load context, then Claude will generate 5 new posts daily in `posts/YYYY-MM-DD-batch/`

**Q: Which posts should I publish?**  
A: Read `batch-manifest.md` for recommendations. Pick based on: (1) topic relevance, (2) pillar diversity, (3) your energy level.

**Q: How do I make posts perform better?**  
A: Engage in the first hour (your own comment + replying to others). Algorithm rewards early engagement more than post quality.

**Q: Should I post every day?**  
A: Start with 1-2 per day. Test what sticks. You have 5 per day ready, so choose quality over quantity.

**Q: What if I want to change a post?**  
A: Edit the `post.md` file before publishing. After publishing, it's live — changes don't matter.

**Q: How do I track what I've published?**  
A: Move published posts to `posts/published/` folder OR just keep notes in a simple txt file (e.g., "June 5: Post 1, 4").

---

## Next Steps (When You're Ready)

1. ✅ **Today:** Pick 1-2 posts from the 2026-06-05 batch and publish
2. ✅ **Tomorrow:** Review new batch, pick different pillars
3. ✅ **This week:** Test engagement patterns (timing, CTA, response rate)
4. ⏳ **Next week:** Evaluate which pillars get best engagement, adjust strategy if needed
5. ⏳ **Ongoing:** Every 2 weeks, refresh industry sources for fresh examples/data

---

## Contact & Support

If you need Claude to:
- **Generate new posts** — Run `/prime` then request new batch
- **Change voice/style** — Update `reference/rohit-voice-guide.md` or `WRITE-BETTER.md`
- **Update strategy** — Edit `context/strategy.md` (pillar mix, target audience, etc.)
- **Add new sources** — Update `reference/curated-industry-sources.md`

**All changes are version-controlled in git, so you can always roll back if needed.**

---

**Project Status: READY FOR DAILY USE**

You have 5 posts per day ready. Pick which to publish each morning. Engage. Watch engagement compound over 30-60 days.

Consistency + real examples + authentic voice = thought leadership.

Good luck. 🚀
