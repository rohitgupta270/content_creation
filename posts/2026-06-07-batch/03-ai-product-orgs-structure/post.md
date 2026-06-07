# How AI Is Reorganizing Product Teams (And Why Your Structure Is Already Broken)

Companies are reorganizing around AI in ways that have nothing to do with "add an AI person."

The structural shifts happening right now:

**Traditional structure:** Product → Design → Engineering
**Emerging AI-first structure:** Product + Data Scientist + LLM Engineer → Design → Core Engineering

Why? Because AI development is fundamentally different from feature development.

**Here's what's changing:**

At a company I advised (SaaS), they had a PM leading a feature (document summarization). Traditional waterfall:
- Discovery: 3 weeks
- Design: 2 weeks  
- Engineering: 6 weeks
- Total: 11 weeks

They reorganized: PM + Data Scientist started together in week 1. Data Scientist testing different LLM approaches (Claude, GPT-4, open source) in parallel to PM discovery. They found the right model + approach in week 3. Design didn't start until week 4 (after model approach was locked). Engineering built to the spec. Total: 6 weeks.

The acceleration came from parallelizing what used to be sequential. Product and AI engineering can't be waterfall anymore.

**Figma did this at scale.** They reorganized 2023 so every product team has a "Creative AI person" alongside the PM. That person tests feasibility while PM discovers use case. Ship velocity doubled. Not because individuals were faster. Because the structure changed.

**Stripe's structure now:** PM + LLM Engineer + Backend Engineer start together. Design follows, not parallel. Why? LLM behavior is non-deterministic. Design can't happen until you know what the model actually does.

**The uncomfortable organizational reality:**

Most companies still have Product reporting to PM, Design next, Engineering last.

AI-native companies have AI/Data science reporting to Product, not sitting separately. Why? Because the AI decision is the product decision. It's not a feature on top of the feature.

Companies reorganizing this way (Figma, Stripe, Notion with their AI features) are shipping 2-3x faster than competitors with traditional structure.

The ones that haven't reorganized yet are building AI on top of broken organization. Slower, more expensive, wrong output.

**Here's the pattern I've seen:**

When a company says "our AI features are slow to ship," it's never about the AI. It's about structure. They're forcing AI teams to fit waterfall product development. Doesn't work.

Organizations that restructured first, then built AI, are dominating.

Your product org structure determines your AI velocity more than your AI expertise.
