# Improved Folder Structure for Daily Post Batches

**Problem:** Posts numbered 001-005 don't show WHEN they were created. Which batch is from June 5? June 15?

**Solution:** Date-based batch folders with clear organization.

---

## New Structure

```
posts/
├── 2026-06-05-batch/          ← Batch from June 5
│   ├── batch-manifest.md       ← Index of all 5 posts that day
│   ├── 01-india-peak-safety/
│   │   ├── post.md
│   │   └── image.jpg
│   ├── 02-bot-traffic-fraud/
│   │   ├── post.md
│   │   └── image.jpg
│   ├── 03-gen-z-wallets/
│   │   ├── post.md
│   │   └── image.jpg
│   ├── 04-embedded-finance/
│   │   ├── post.md
│   │   └── image.jpg
│   └── 05-realtime-liquidity/
│       ├── post.md
│       └── image.jpg
│
├── 2026-06-06-batch/          ← Batch from June 6
│   ├── batch-manifest.md
│   ├── 01-[new-post]/
│   ├── 02-[new-post]/
│   └── ...
│
├── 2026-06-15-batch/          ← Batch from June 15
│   ├── batch-manifest.md
│   ├── 01-[new-post]/
│   └── ...
│
└── published/                 ← Archive of published posts
    ├── 2026-06-05-peak-safety.md
    └── ...
```

---

## What's in batch-manifest.md

**File:** `posts/2026-06-05-batch/batch-manifest.md`

```markdown
# Daily Batch — June 5, 2026

**Generated:** 2026-06-05 @ 8:00 AM  
**Status:** Ready for review  

---

## 5 Posts Available Today

### 1️⃣ India's Peak Safety Paradox
- **Pillar:** Product Leadership + Payments
- **Source:** FinTech Inside
- **Difficulty:** High
- **Length:** ~550 words
- **Audience:** Risk/CFO leaders
- **File:** `01-india-peak-safety/post.md`

### 2️⃣ Bot Traffic Reality
- **Pillar:** AI × PM + Payments
- **Source:** AI Weekly
- **Difficulty:** High
- **Length:** ~550 words
- **Audience:** Engineering leaders
- **File:** `02-bot-traffic-fraud/post.md`

### 3️⃣ Gen Z Wallet Shift
- **Pillar:** Future of Payments
- **Source:** PYMNTS
- **Difficulty:** Medium
- **Length:** ~550 words
- **Audience:** Commerce/payment teams
- **File:** `03-gen-z-wallets/post.md`

### 4️⃣ Embedded Finance Wave
- **Pillar:** Product Leadership + Payments
- **Source:** Fintech Futures
- **Difficulty:** High
- **Length:** ~600 words
- **Audience:** SaaS founders/PMs
- **File:** `04-embedded-finance/post.md`

### 5️⃣ Real-Time Payments Liquidity
- **Pillar:** Future of Payments
- **Source:** Fintech Inside
- **Difficulty:** Medium-High
- **Length:** ~500 words
- **Audience:** Treasury/finance leaders
- **File:** `05-realtime-liquidity/post.md`

---

## 📊 Quick Stats

- **Total posts:** 5
- **Avg length:** ~550 words
- **By difficulty:** 3 High, 1 Medium-High, 1 Medium
- **By pillar:** 3 Payments, 2 Leadership, 1 AI+PM
- **Sources used:** 5 different industry sources

---

## 🎯 Your Action Items

1. Read one or more posts
2. Choose which to publish: "Publish Post 1"
3. I'll copy to published folder
4. Next batch tomorrow at 8:00 AM

---

## 📁 File Locations

All posts for today:
- `01-india-peak-safety/post.md`
- `02-bot-traffic-fraud/post.md`
- `03-gen-z-wallets/post.md`
- `04-embedded-finance/post.md`
- `05-realtime-liquidity/post.md`

Open any post.md to read the full post and copy to LinkedIn.
```

---

## How You'll Use This

**Every morning:**

1. **Open:** `posts/2026-06-05-batch/` (or whatever date)
2. **Read:** `batch-manifest.md` (see all 5 posts at a glance)
3. **Pick:** Which post to publish
4. **Copy:** The text from `post.md`
5. **Paste:** Into LinkedIn

**Later, when you publish:**
- I move it to `published/` folder
- Marked as "published on [date]"

---

## Benefits

✅ **Clear date organization** — "June 5 batch" vs "June 15 batch"  
✅ **One-file index** — See all 5 posts at a glance in batch-manifest.md  
✅ **Easy lookup** — Want June 10 posts? Open `2026-06-10-batch/`  
✅ **Archive system** — Published posts move to separate folder  
✅ **Historical record** — Can always see what was available each day  

---

## Example: Finding June 15 Posts

```bash
cd posts/2026-06-15-batch/
open batch-manifest.md          # See all 5 posts from that day
open 02-[post-name]/post.md     # Read the full post you want
```

No confusion. No searching. Clear dates.

---

## Next Steps

1. Reorganize existing 5 test posts into `2026-06-05-batch/`
2. Create `batch-manifest.md` for today
3. Update this system for all future batches
4. Move published posts to `published/` archive

Ready to implement?
