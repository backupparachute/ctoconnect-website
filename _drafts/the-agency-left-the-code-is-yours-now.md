---
title: "The Agency Left. The Code Is Yours Now."
description: "You paid an agency to build your product and now you own a codebase nobody on your team has read. Here's the first month."
author: "Kyle Miller"
members_only: true
teaser: "The agency shipped, invoiced, and moved on. You own a working product and nobody who knows why any of it works that way."
tags:
  - technical-debt
  - architecture
  - pragmatism
---

The product works. Customers use it. And every person who knows why it was built that way has moved to another client.

This is a normal way to start. It's also where founders make an expensive mistake, which is deciding the code is garbage and needs a rewrite. Sometimes it is garbage. You can't tell yet, and neither can the engineer you hired last week who has been reading it since Monday.

Spend the first month on control instead.

Get the keys. Every account, every domain, every deploy credential, every third party service, in your name and not the agency's. Do this before anything else. Agencies go out of business.

Prove you can deploy. Not "the agency deployed it." You, or someone you employ, pushing a small change to production and watching it land. If you can't do that, nothing else on this list matters.

Prove you can restore. Take the backup, load it somewhere else, confirm the data is there.

Then read the code with a specific question. Not "is this good." Ask what happens when a customer signs up, and follow that path all the way through. You'll learn more about the architecture from one path than from a week of skimming files.

Write down what you find as you go. You're the last person who will ever see this codebase without knowing how it works.

Rewrite decisions come later, once you understand what you have. Most of the time you'll find code that's fine and documentation that never existed.
