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

The expensive mistake here is deciding the code is garbage and needs a rewrite. Sometimes it is. You can't tell yet, and neither can the engineer who started Monday.

Spend the first month on control instead.

Get the keys. Every account, every domain, every deploy credential, in your name and not the agency's. Do this before anything else. Agencies go out of business.

Prove you can deploy. Not "the agency deployed it." You, pushing a small change to production and watching it land.

Prove you can restore. Take the backup, load it somewhere else, confirm the data is there.

Then read the code with one question. Ask what happens when a customer signs up, and follow that path all the way through. You'll learn more from one path than a week of skimming files.

Rewrite decisions come later. Most of the time you'll find code that's fine and documentation that never existed.
