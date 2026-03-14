---
title: "Dev and Ops Shouldn't Be Separate Teams"
description: "Separating development and operations creates a war nobody wins. The best teams own the whole pipeline."
author: "Kyle Miller"
members_only: false
teaser: "When devs throw code over the wall to ops, everyone loses. The teams that ship fastest own the whole pipeline."
tags:
  - devops
  - team-structure
  - process
---

Here's how it usually works. Developers write code. They toss it to an operations team. Ops deploys it and keeps it running. Devs get rewarded for shipping fast. Ops gets rewarded for keeping things stable.

These goals are in direct conflict. Every deployment is a risk to stability. So ops slows things down. Devs get frustrated. Blame starts flowing. Deployments become a negotiation.

The fix is simple but uncomfortable. Teams own their code in production. You build it, you run it. When the person who wrote the code is also the person who gets paged at 2am, code quality improves fast.

I watched a team go from monthly deployments with a change advisory board to daily deployments with no approval process. Everyone expected more incidents. Incidents actually dropped by 40%. Turns out smaller, more frequent changes are easier to debug than massive monthly releases that touch everything.

Stability and speed aren't opposites. They come from the same set of habits. Small changes, fast feedback, and ownership of the outcome.
