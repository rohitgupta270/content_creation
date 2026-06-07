# Why Your Fraud Detection Is Too Tight (And Costing You Money)

Most payment teams treat fraud like a zero-sum game: Lower fraud = better.

Wrong. Fraud costs money two ways:
- Actual fraud losses (chargebacks, disputes)
- Good customers rejected by overly strict rules

And the second cost? Usually 10x bigger. Teams optimize for the visible loss and ignore the invisible one.

I've watched this pattern at three payment companies. Fraud detection gets tighter, fraud losses drop 2-3%, but legitimate transaction rejections climb 8-12%. Nobody measures it as a cost. It just shows up as "cart abandonment" or "churn."

Here's the math:

At a company I advised (Payments SaaS for marketplaces), fraud loss was $2M/year on $500M volume. That's 0.4% — industry average.

Their fraud team wanted to tighten rules. Estimate: reduce fraud to 0.2%. Cost to implement: $400K. Expected fraud savings: $1M.

Sounds like a win. Until we measured what tightening actually costs:

Legitimate transactions getting rejected: 1.2% (up from 0.3% today)
Average customer value: $4,000/year
Rejection rate hitting accounts: $4,800/year per 1,000 accounts
Annual cost: $2.4M in lost revenue.

Net impact: Save $1M in fraud, lose $2.4M in legitimate business. Net loss: $1.4M.

**Square learned this the hard way.** In 2015, they tightened fraud detection across SMB merchants. Fraud dropped 30%. Merchant churn spiked 18% because legitimate transactions were getting blocked. They spent 18 months untangling it.

**Stripe got this right early.** They set fraud detection to optimize for the economic tradeoff, not fraud minimization. Result: 0.5% fraud loss (slightly higher than competitors), but 99.8% legitimate approval rate. Merchants stick around because transactions don't mysteriously fail.

**Here's the uncomfortable truth:**

If your fraud loss is below 1%, your fraud detection is probably TOO TIGHT.

You're optimizing for the wrong metric. The real metric is "legitimate customer experience preserved while managing fraud within acceptable risk."

That's a different conversation than "how low can we get fraud?"

Most teams never have it.
