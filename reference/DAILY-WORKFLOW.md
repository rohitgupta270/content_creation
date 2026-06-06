# Daily Content Workflow: 8 AM Trend Scraping & Post Generation

**Purpose:** Automate trend monitoring and post generation at 8 AM daily

---

## 🎯 The Workflow (8 AM Daily)

### Step 1: Scrape Industry Sources (Automated)
**Time:** 8:00 AM - 8:05 AM
- System scrapes all 40+ sources from `reference/curated-industry-sources.md`
- Identifies trending topics/signals
- Summarizes key developments

### Step 2: Analyze Trends & Identify Post Opportunities
**Time:** 8:05 AM - 8:15 AM
- Claude analyzes scraped data
- Finds patterns, non-obvious insights, contrarian takes
- Identifies which pillar (AI, Payments, Travel, PM) the trends map to

### Step 3: Generate Post (Leadership-Level)
**Time:** 8:15 AM - 8:25 AM
- Creates 1 post using **Rohit's PM lens**
- Includes: Pattern recognition, uncomfortable truth, specific example, systems thinking
- Grounded in real trend data (not invented)
- Leadership-level depth (15+ years signal)

### Step 4: Notify & Store
**Time:** 8:25 AM - 8:30 AM
- Post saved to `posts/NNN-slug/`
- Dashboard rebuilt
- Notification sent: "Post ready for review at [time]"

---

## 📊 What Gets Captured Each Day

### Daily Signal Log
**File:** `outputs/trend-signals-YYYY-MM-DD.md`

```markdown
# Trend Signals — [DATE]

## AI & ML Signals
- [Signal 1]: [What's trending, why it matters]
- [Signal 2]: ...

## Payments & Fintech Signals
- [Signal 1]: ...
- [Signal 2]: ...

## Travel & Commerce Signals
- [Signal 1]: ...
- [Signal 2]: ...

## Product Management Signals
- [Signal 1]: ...
- [Signal 2]: ...

## Cross-Category Patterns
- Pattern 1: [How signals connect across categories]
- Pattern 2: ...

## Post Generated Today
- **Title:** [Post title]
- **Pillar:** [Which content pillar]
- **Source Trend:** [Which signal triggered this post]
- **File:** posts/NNN-slug/
```

### Weekly Pattern Review
**Every Friday:**
- Review 5 daily signal logs (Mon-Fri)
- Identify emerging patterns
- Plan next week's content angles
- Identify contrarian takes or non-obvious insights

---

## 🗂️ Source Categories & Monitoring

### Tier 1: Daily Monitoring (Top 5 per category = 20 sources)
**Time commitment: 15-20 minutes/day**

| Category | Sources | Time |
|----------|---------|------|
| **AI/ML** | The Batch, Superhuman, Import AI, AI Breakfast, Prompt Engineering Daily | 5 min |
| **Payments** | FinTech Inside, The Block, Fintech Futures, Paytech Daily, Circle | 5 min |
| **Travel** | PhocusWire, Skift, Routehappy, Hopper, IATA | 4 min |
| **PM** | Reforge, Maven, Lenny's, April Dunford, Teresa Torres | 4 min |

### Tier 2: Weekly Dives (Additional 20 sources)
**Time commitment: 30 minutes/week**
- Deep dives on specific topics
- Cross-category research
- Emerging signals not yet in mainstream

---

## 💡 Post Generation Criteria

### Every Post Must Have:

1. **Grounded in Real Trend** ✓
   - Must cite or respond to actual source content
   - Not invented or generic

2. **Pattern Recognition** ✓
   - "I've seen this pattern..." OR "This is the 3rd time I've seen..."
   - Shows 15 years of experience

3. **PM Lens** ✓
   - How does a product manager think about this?
   - What's the strategic implication?

4. **Uncomfortable Truth** ✓
   - What do most people get wrong?
   - Non-obvious insight

5. **Specific Example** ✓
   - Real story from your experience
   - Real numbers/outcomes

6. **Actionable for Readers** ✓
   - What should other PMs think about differently?

---

## 📈 Content Pipeline

```
Sources → Daily Signals → Weekly Patterns → Post Ideas → Posts Published
          ↓
      outputs/trend-signals-YYYY-MM-DD.md
      (stored for history & pattern review)
```

### Example Content Flow:

**Monday 8:05 AM:** Scrape discovers Gen Z payment preferences trending across 3 sources
→ Captured in `trend-signals-2026-06-09.md`

**Tuesday 8:05 AM:** Real-time payments featured in 2 more sources + regulatory news
→ Pattern emerges: "Real-time payments are about liquidity, not speed"

**Wednesday 8:15 AM:** AI agents for commerce trending + Ant Group diaspora payments
→ Post generated: "The hidden competition in payments isn't who's fastest, it's who understands liquidity"

**Friday 5 PM:** Weekly review identifies emerging theme
→ Next week: 3 posts planned around this theme

---

## 🚀 How to Use This Daily

### For Rohit (You):

**Daily (8:30 AM):** 
- Check notification
- Review generated post (2 min)
- Approve, request changes, or skip
- Post goes to LinkedIn when ready

**Weekly (Friday 5 PM):**
- Review all 5 signal logs
- Identify patterns
- Plan next week's content angles
- Note: "Which signals feel contrarian or valuable?"

**Monthly (1st of month):**
- Review all 30 signal logs from month
- Identify your strongest patterns/themes
- Plan content sprints around emerging topics
- Update sources if needed (add/remove)

### For Claude (Me):

**Daily 8 AM:**
- Scrape all 40 sources
- Analyze trends
- Identify post opportunity
- Generate post with your voice + leadership depth
- Store signals and post

**Weekly:**
- Review patterns across all signals
- Identify cross-category connections
- Flag emerging themes

---

## 📝 Sources to Add

**You can add more sources as you discover them:**

1. Find a good source (newsletter, blog, publication)
2. Add to `reference/curated-industry-sources.md`
3. Add URL to `reference/sources-urls-for-subscriptions.txt`
4. On next 8 AM run, it gets included in scraping

**Categories we monitor:**
- AI & ML
- Payments & Fintech
- Travel & Commerce
- Product Management

---

## 🎯 Success Metrics

**How to know this is working:**

1. ✓ Posts are grounded in real trends (not invented)
2. ✓ Posts feel like they come from your 15 years (not junior advice)
3. ✓ Readers see non-obvious insights (pattern recognition)
4. ✓ You're seeing 3-5 signals/day from sources
5. ✓ Weekly patterns emerge naturally
6. ✓ Posts generate meaningful engagement from target audience

---

## 🔧 Technical Setup

**Daily 8 AM Automation:**
- [ ] Schedule system scraping of 40 sources
- [ ] Trigger Claude analysis of scraped data
- [ ] Generate post if pattern detected
- [ ] Save to posts/ folder
- [ ] Update trend signals log
- [ ] Notify you when ready

**See:** `/schedule` command for setting up the daily 8 AM task

---

## Next Steps

1. **Read** `reference/sources-quick-reference.md` (5 min)
2. **Subscribe** to top 20 sources using `reference/sources-urls-for-subscriptions.txt` (20 min)
3. **Set up** daily 8 AM automation using `/schedule` (10 min)
4. **Confirm** workflow with first day's signals and post (30 min)

Then: **System runs daily. You review & approve posts at 8:30 AM.**
