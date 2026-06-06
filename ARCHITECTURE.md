# System Architecture — Visual Overview

## How the System Works

```
┌─────────────────────────────────────────────────────────────────┐
│                     DAILY WORKFLOW (8:00 AM)                    │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. GENERATE 5 POSTS (one per pillar)                           │
│     ↓                                                            │
│     posts/2026-06-XX-batch/                                     │
│     ├── batch-manifest.md (index + recommendations)             │
│     ├── 01-real-time-liquidity/ (Payments)                      │
│     ├── 02-travel-personalization/ (Travel)                     │
│     ├── 03-ai-product-orgs/ (AI×PM)                             │
│     ├── 04-identity-decisions/ (Leadership)                     │
│     └── 05-learning-from-failure/ (Personal)                    │
│                                                                 │
│  2. PICK 1-2 POSTS TO PUBLISH                                   │
│     (Check pillar diversity, audience interest, your energy)    │
│     ↓                                                            │
│  3. COPY TEXT → LINKEDIN → PUBLISH (8:30 AM)                    │
│     ↓                                                            │
│  4. ENGAGE (comment within 10 min, reply to comments)           │
│     ↓                                                            │
│  5. ALGORITHM AMPLIFIES (depends on early engagement)           │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

## File Dependencies

```
┌──────────────────────────────────────────────────────────────┐
│              CORE CONFIGURATION (Read by Claude)             │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  CLAUDE.md (Master config)                                   │
│    ↓                                                          │
│    └─→ context/                                              │
│        ├── profile.md (Who you are)                          │
│        ├── business.md (What you do)                         │
│        ├── strategy.md (5 pillars: 40/25/15/10/10)           │
│        └── images/ (Your personal photos)                    │
│                                                              │
│    └─→ reference/                                            │
│        ├── WRITE-BETTER.md (10 writing rules)               │
│        ├── REAL-EXAMPLES-REQUIRED.md (Real data standard)    │
│        ├── rohit-voice-guide.md (Authentic voice)            │
│        └── curated-industry-sources.md (40+ sources)         │
│                                                              │
└──────────────────────────────────────────────────────────────┘
         ↓
┌──────────────────────────────────────────────────────────────┐
│              POST GENERATION (Claude Creates)                │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  posts/2026-06-XX-batch/                                     │
│  ├── batch-manifest.md (index of 5 posts)                    │
│  ├── 01-real-time-liquidity/                                 │
│  │   ├── post.md (ready to copy-paste)                       │
│  │   ├── image.png (personal photo or infographic)           │
│  │   └── References section (links to sources)               │
│  ├── 02-travel-personalization/                              │
│  ├── 03-ai-product-orgs/                                     │
│  ├── 04-identity-decisions/                                  │
│  └── 05-learning-from-failure/                               │
│                                                              │
└──────────────────────────────────────────────────────────────┘
         ↓
┌──────────────────────────────────────────────────────────────┐
│              PUBLISHING & ARCHIVE (You Control)              │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  LinkedIn (published daily)                                  │
│     ↓                                                         │
│  posts/published/ (archive of what you posted)               │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

## Content Pillars (5 Categories)

```
YOUR LINKEDIN STRATEGY
├── Payments (40%)          Real-time payments, embedded finance, working capital
│   └── Audience: Treasury, payments, fintech leaders
│
├── Product Leadership (25%) Identity, frameworks, decision-making, scaling
│   └── Audience: Product managers, founders, CTOs
│
├── AI × Product (15%)       AI adoption, rethinking processes, product orgs
│   └── Audience: Product leaders, CTOs
│
├── Travel (10%)            Personalization, NDC, AI in travel, booking
│   └── Audience: Travel tech, marketplace leaders
│
└── Personal (10%)           Learning, failures, wisdom, human side
    └── Audience: Founders, leaders (vulnerability builds trust)
```

## Quality Control Pipeline

```
CLAUDE GENERATES POST
    ↓
CHECK #1: Real Examples Standard
├─ Real company names? (Wise, Stripe, Hopper)
├─ Specific metrics? (31%, 45%, $11B)
├─ Market context? (B2B SMBs, segments, geographies)
└─ Data sources cited? (McKinsey, Phocuswire, etc.)
    ↓
CHECK #2: Writing Quality
├─ No em dashes? ✓
├─ Active voice? ✓
├─ No hedging? ✓
├─ Leadership-level thinking? ✓
└─ Authentic voice (Rohit, not generic)? ✓
    ↓
CHECK #3: Ready to Publish
├─ Specific over generic? ✓
├─ Proofs included (case studies)? ✓
├─ Evidence-based (not opinion)? ✓
└─ Self-sufficient (no CTAs for follow-up)? ✓
    ↓
APPROVED → posts/2026-06-XX-batch/0X-slug/
```

## Decision Tree: Which Post to Publish Today?

```
          START: Read batch-manifest.md
                    ↓
    ┌───────────────┼───────────────┐
    ↓               ↓               ↓
Did you post   Pick different   Check what
Payments       pillar today?     resonates
yesterday?         ↓              with you
    ↓              ↓                ↓
   Yes            Yes             Strong
    ↓              ↓              hook &
Post Travel/   Look for       specific
AI×PM/         Leadership/     examples
Leadership/    Personal        → PUBLISH
Personal
    ↓              ↓
PUBLISH        PUBLISH
```

## Files You'll Use Daily vs. Rarely

**Daily (Every Morning):**
```
posts/2026-06-XX-batch/batch-manifest.md     ← Read this
posts/2026-06-XX-batch/0X-slug/post.md       ← Copy-paste from this
```

**Weekly:**
```
reference/curated-industry-sources.md        ← Refresh industry data
```

**Monthly:**
```
context/strategy.md                           ← Review if strategy shifts
reference/WRITE-BETTER.md                     ← Consistency check
```

**Rarely (If at all):**
```
CLAUDE.md                                     ← Master config (rarely changes)
context/profile.md                            ← Update if background changes
reference/rohit-voice-guide.md                ← Reference if voice drifts
```

## How to Monitor Progress

```
Weekly Check:
├─ How many posts did I publish? (aim: 7)
├─ Which pillar got best engagement? (track which resonate)
├─ Which time performed best? (8:30 AM vs. other times)
└─ Am I engaging with comments? (first hour critical)

Monthly Review:
├─ Follower growth (should be consistent)
├─ Top 3 posts (pattern: what works?)
├─ Engagement rate (replies, shares, reshares)
└─ Inbound interest (DMs, inquiries, opportunities)

Quarterly (if continuing):
├─ Refine strategy based on engagement data
├─ Update audience pain points in business.md
├─ Refresh industry sources if stale
└─ Adjust pillar mix if one pillar outperforms
```

## Tech Stack (Behind the Scenes)

Claude generates posts using:
- ✓ Your 15-year PM experience (from context/)
- ✓ Industry sources (from curated-industry-sources.md)
- ✓ Writing standards (WRITE-BETTER.md, REAL-EXAMPLES-REQUIRED.md)
- ✓ Authentic voice (rohit-voice-guide.md)
- ✓ Real company examples (Wise, Stripe, Hopper, etc.)
- ✓ Market data (McKinsey, Phocuswire, earnings reports)

No AI-generated slop. All posts:
- Leadership-level thinking (pattern recognition from 15 years)
- Specific examples (real companies, real numbers)
- Rohit's authentic voice (warm, direct, witty, pragmatic)
- Evidence-based (data > opinion)

## Success Metrics

**Month 1-2 (Build Consistency):**
- ✓ Publishing 1-2 posts daily
- ✓ Engaging within first hour
- ✓ Building small engaged follower base

**Month 3+ (Build Authority):**
- ✓ Consistent engagement rate (2-5% on text posts)
- ✓ Pattern: which content resonates?
- ✓ Inbound: DMs from prospects, opportunities, collaboration requests

**Month 6+ (Thought Leadership):**
- ✓ 1-2 posts per week are viral (1000+ interactions)
- ✓ Followers in key audience (PMs, founders, CTOs)
- ✓ Inbound opportunities: speaking, partnerships, roles
- ✓ Authority established in your pillars (Payments, AI×PM, Leadership)

---

**Status: READY FOR DAILY USE**

You have all the scaffolding in place. Posts are generated automatically. Your job: pick, publish, engage.

Consistency + 30-60 days = visible traction.
