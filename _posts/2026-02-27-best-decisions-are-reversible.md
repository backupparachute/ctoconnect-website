---
title: "The Best Architecture Decision Is the One You Can Reverse"
description: "Most technical decisions aren't permanent. Treating them like they are slows everything down."
author: "Kyle Miller"
members_only: true
teaser: "Most technical decisions aren't permanent. The teams that move fastest are the ones that optimize for reversibility over correctness."
tags:
  - architecture
  - decision-making
  - pragmatism
---

Teams spend weeks debating database choices, framework migrations, and service boundaries like the decision is permanent. Most of the time, it isn't.

Jeff Bezos calls these "two-way doors." You can walk through, look around, and walk back if you don't like what you see. The problem is that engineering teams treat every decision like a one-way door. They over-analyze, over-architect, and over-plan for a future that might never happen.

The better question isn't "what's the best choice?" It's "how easily can we change this later?"

Pick the database that's good enough. Build the service boundary where it makes sense today. Choose the framework your team already knows. If any of those turn out to be wrong in a year, you'll know more then than you do now. You'll make a better decision with real data instead of hypotheticals.

The decisions that actually deserve weeks of debate are the genuinely irreversible ones. Public APIs that third parties depend on. Database schemas with millions of rows. Contracts with vendors. Those are one-way doors. Everything else is probably a two-way door dressed up as something scarier than it is.

Move quickly on reversible decisions. Save your energy for the ones that actually stick.
