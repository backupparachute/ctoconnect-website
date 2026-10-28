---
title: "Every Line of Code Is a Liability"
description: "You count code as an asset. Every line you write is something you'll pay to keep running."
author: "Kyle Miller"
members_only: false
teaser: "Writing code got cheap. Owning it didn't. Every line you ship is a bill that comes due later."
tags:
  - technical-debt
  - pragmatism
  - cost
---

You count your code as an asset. Look at it from the other side. Every line you write is something you now have to maintain.

That line has to keep working when you upgrade the framework. Someone has to read it before they change the code next to it. It needs tests, and the tests need upkeep. When it breaks at 2 AM, someone has to understand it.

You don't see any of that the day you write it. You pay it every month after.

AI made this worse. Writing code used to be the slow part, so teams wrote less of it. Now an agent turns out a thousand lines before lunch. The cost to write dropped close to zero. The cost to own stayed where it was.

You can measure it. Track how long a small change takes from ticket to production, and watch that number as the codebase grows. Past a certain size, the tool you bought to go faster starts costing you time.

Treat new code like a new hire. Before you add it, ask whether you'd pay to keep it around for three years.

## Keep the bill down

Delete what nobody uses. Old feature flags. Admin screens nobody opens. Put the lines you removed in the sprint review, next to the lines you added.

Buy what isn't your product. Someone else pays to maintain it.

The best code is the code you never wrote. The next best is the code you deleted.
