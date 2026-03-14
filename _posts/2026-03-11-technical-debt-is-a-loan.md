---
title: "Technical Debt Isn't a Bug, It's a Loan"
description: "Technical debt gets treated like a mistake. Sometimes it's the smartest decision you can make. The problem is when you stop tracking it."
author: "Kyle Miller"
members_only: false
teaser: "Technical debt gets treated like a failure. Sometimes taking on debt is the smartest move. The problem is when you stop tracking what you owe."
tags:
  - technical-debt
  - architecture
  - engineering-leadership
---

Engineers talk about technical debt like it's always bad. It isn't. Debt is a tool. You take out a mortgage to buy a house you can't afford with cash. You take on technical debt to ship something before the market moves on.

The problem isn't the debt. It's when teams stop tracking what they owe.

A shortcut you take deliberately with a plan to fix it later is a strategic decision. A shortcut nobody documents that three new hires build on top of is a liability. The difference is awareness.

I tell teams to keep a debt register. Not a Jira backlog that nobody reads. A short list of intentional shortcuts with two columns. What did we skip and what happens if we don't fix it. Review it every quarter. Some of that debt will never matter because the feature got deprecated. Some of it will be quietly compounding interest that's about to break something.

The worst technical debt isn't in the code. It's in the knowledge gaps. The engineer who wrote the workaround left six months ago. Nobody knows why that config flag exists. The README says "temporary fix" with a date from 2019.

Take on debt when it makes sense. Write it down. Pay it back before the interest buries you.
