# Quick Start — When You Return

**You have 5 ready-to-publish posts waiting.** Follow these steps to get them live.

---

## 30-Second Version

1. **Open batch folder:**
   ```bash
   cat posts/2026-06-XX-batch/batch-manifest.md
   ```

2. **Read a post:**
   ```bash
   cat posts/2026-06-XX-batch/0X-post-slug/post.md
   ```

3. **Copy text → LinkedIn → Paste → Publish**

4. **Comment on your own post within 10 min** (this matters for reach)

Done. The algorithm does the rest.

---

## 3-Minute Version

### Step 1: Load Context
```bash
# In Claude, run:
/prime
```

This loads your profile, voice, strategy, and quality standards.

### Step 2: See What's Ready
```bash
# See the date of the latest batch
ls posts/ | grep batch | tail -1

# Output: 2026-06-XX-batch/

# Read the manifest (index of all 5 posts)
cat posts/2026-06-XX-batch/batch-manifest.md
```

This shows:
- 5 posts (one per pillar)
- Key insight for each
- Difficulty level
- Recommendations for what to post

### Step 3: Pick One to Publish
Look at the manifest. The **recommendations** section suggests the strongest post.

Or pick based on:
- **If you posted Payments yesterday** → pick Travel, AI×PM, Leadership, or Personal today
- **If you want high engagement** → post 4 (Identity Decisions) or 3 (AI Product Orgs)
- **If you want to showcase depth** → post 1 (Payments) or 5 (Personal story)

### Step 4: Read the Post
```bash
cat posts/2026-06-XX-batch/0X-post-slug/post.md
```

The post has this structure:
```
# [Title]

**Metadata:** Method, Pillar, Format, Status

---

[Post text here — copy-paste ready]

---

## References & Learn More

[Links for readers who want deeper context]
```

### Step 5: Publish
1. **Copy the post text** (everything under "## Post Text (copy-paste ready)")
2. **Go to LinkedIn**
3. **Paste into post editor**
4. **Add image if available** (stored in the post folder as `image.png`)
5. **Schedule or publish** at 8:30 AM your time (or 10-11 PM ET if US audience)

### Step 6: Engage (Critical)
Within 10 minutes of posting:
1. **Reply to your own post** with a comment that adds context or asks a question
2. **Spend 30 min replying** to others' comments

This signals the algorithm: "real person, real engagement." Dramatically improves reach.

---

## What You'll Find in Each Post Folder

```
posts/2026-06-XX-batch/0X-post-slug/
├── post.md              # Read this — contains everything
├── image.png            # Use this if posting (personal photo or infographic)
├── carousel.pdf         # Only for carousel posts
└── References.txt       # Links to deeper sources
```

**All you need is:**
1. Read `post.md`
2. Copy the text
3. Use `image.png` (optional, but recommended)

---

## Daily Routine (5 Min)

```
Morning:
1. Read batch-manifest.md (2 min)
2. Pick a post (1 min)
3. Copy text → LinkedIn → Publish (1 min)
4. Comment on your post (1 min)

Later that day:
5. Reply to comments (30 min when you have time)
```

Repeat daily.

---

## Every Few Days

```bash
# See new posts
ls posts/ | grep batch | tail -5

# Read new batch
cat posts/YYYY-MM-DD-batch/batch-manifest.md
```

New batches are generated daily, so you always have fresh content ready.

---

## If You Want to Know More

- **Full project summary:** Read `PROJECT-SUMMARY.md`
- **Content quality standards:** See `reference/WRITE-BETTER.md` and `reference/REAL-EXAMPLES-REQUIRED.md`
- **Your voice/style:** Check `reference/rohit-voice-guide.md`
- **Industry sources:** See `reference/curated-industry-sources.md`
- **Strategy/pillars:** Read `context/strategy.md`

---

## Most Important Thing

**Consistency + Engagement = Growth**

Don't worry about perfection. Post daily. Reply to comments. Watch what resonates. Adjust.

LinkedIn algorithm rewards:
1. **Consistency** (posting regularly)
2. **Early engagement** (your comment + replies within first hour)
3. **Authenticity** (real voice, real examples, real depth)

You have all three locked in.

---

## TL;DR

```bash
cat posts/2026-06-XX-batch/batch-manifest.md
cat posts/2026-06-XX-batch/0X-post-slug/post.md
# Copy → LinkedIn → Publish
# Comment within 10 min
# Done
```

Rest is the algorithm's job.
