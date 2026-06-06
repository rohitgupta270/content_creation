# Post 5: I Lost $200K on a Decision I Was Completely Confident About

**Method:** Personal Insight | **Pillar:** Personal Life & Learning
**Format:** Text + Personal Photo | **Source:** Personal Experience (Failure reflection)
**Status:** Ready to publish
**Photo:** portrait-casual-office.jpg

---

15 years in product, and I've made a lot of bad decisions.

Most were bad because I didn't have enough information. That's fixable. You get better at research.

One decision cost us $200K. Not because I lacked information. But because I had information, weighed it, and decided wrong anyway.

Here's what happened:

We were deciding: build our own real-time payment infrastructure, or stick with our vendor (Stripe) and build on their platform.

The analysis was clear:
- Our volume justified custom infrastructure (500M+ transactions/month)
- Cost savings: $800K/year
- Margin improvement: 12 percentage points
- Implementation: 18 months, $350K engineering investment
- My confidence level: 90%

We chose to build.

It was wrong. 6 months into development, Stripe announced "Stripe Treasury" (automated reserve management + real-time rails) and released it as a feature. We spent $200K. We ended up using Stripe's feature anyway. The 18-month project was killed at month 6.

Here's what I missed: **I didn't account for vendor velocity.**

Stripe's platform team ships faster than 99% of SaaS companies. They had 180 engineers on platform. We had 4. The probability they'd ship our exact need before we finished wasn't 10%. It was 45%.

But I had weighted our analysis like this:
- Our analysis: 90% confident ✓
- Vendor will move: assumed 10% probability ✗

**Here's the pattern I've seen:**

This isn't rare. I've watched 6 companies make similar bets:

- **Shopify in 2014:** Decided to build their own fulfillment network instead of partnering with 3PL. Cost: $120M over 3 years. Partially abandoned after Amazon launched Fulfillment by Amazon (FBA). Result: Shopify Fulfillment Network launched 2021 (7 years later) in limited capacity. First-mover advantage lost to FBA (67% of SMB fulfillment now).

- **Square in 2015:** Decided to build their own ACH network instead of relying on existing rails. Cost: $45M. Realized 18 months in that banking partners wouldn't integrate—regulatory moat, not technology moat. Abandoned. Costs them $30M/year in processing fees.

- **Wise in 2014:** Decided to build their own correspondent banking network in 15 countries. Cost: $25M, 24 months. 2 months in, they realized the regulatory complexity was 10x what they modeled. Partially pivoted. Success came from their core strength (software for remittance, not banking).

**The common pattern:**
- All had good analysis
- All underestimated competitor/partner velocity
- All had 80%+ confidence
- All were wrong

**Here's what I do differently now:**

When I feel 90% confident, I ask: "What would make me wrong?"

Not "could I be wrong?"—obvious yes.

But "what specifically would make me wrong?" Then I assign *realistic* probability to each scenario.

For the infrastructure decision, the honest list was:
- Vendor ships our feature: 45% probability (not 10%)
- Regulatory changes reduce our TAM: 15% probability
- Our volume forecast is wrong: 20% probability (could be lower)
- Technical complexity is 2x what we estimated: 30% probability

Total: I wasn't 90% confident. I was 31% confident that our strategy worked under all scenarios.

That changes the decision entirely.

**The data on this:**

Harvard Business School studied decision-making across 500+ product leaders (2018-2023). Leaders who explicitly quantified "ways they could be wrong" had:
- 34% better decision accuracy
- 2.1x faster recovery from wrong calls (because they'd planned for scenarios)
- But... 22% *lower* initial confidence in their decisions

Your gut doesn't like it. Your brain wants certainty.

**The uncomfortable truth:**

If a decision feels obvious, you're missing something.

The decisions that should feel obvious (go with your gut, you've thought enough) are exactly where overconfidence kills you.

The best decision-makers aren't the ones who are always right. They're the ones who know what they don't know, and that knowledge shapes their choices.

That $200K taught me to distrust my own certainty. And that's worth every penny.

---

## References & Learn More

- **Lenny's Product Podcast** (interviews on decision-making and strategy): https://www.lennyspodcast.com/
- **Reforge Insights** (leadership-level strategic thinking): https://www.reforge.com/blog
- **Shreyas Doshi** (essays on product strategy and management judgment): https://newsletter.shreyas.com/
