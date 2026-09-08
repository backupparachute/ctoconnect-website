---
title: "Legacy Code Used to Take Ten Years"
description: "A codebase goes legacy when nobody left understands it. AI cut that timeline from a decade to a quarter."
author: "Kyle Miller"
members_only: false
teaser: "Legacy code used to arrive after a decade of turnover. Now it shows up in three months, and nobody understood it in the first place."
tags:
  - ai
  - architecture
  - technical-debt
---

A codebase goes legacy when the people who understood it are gone. That used to take a decade. Two rounds of turnover, a founder leaves, and nobody can explain the billing module. You had years of warning.

Now it takes a quarter.

I've been in codebases four months old that nobody can explain. The code isn't bad. It's clean and the tests pass. But nobody knows why the retry logic sits where it does, or which of the two user lookup paths is the real one. The agent that wrote it forgot when the session ended. The human who approved the pull requests skimmed them.

## The failure mode has a shape

You notice when your agent starts spinning.

It builds a second version of something that already exists, because it never found the first. It fixes a bug by stacking a guard clause on the guard clause it wrote last week. It rewrites working code because the file is too big to hold at once, so it reasons about half and breaks the rest.

You spend a week untangling it.

Same problem every time. The system outgrew the working memory of whatever maintains it. Bigger models raise that ceiling. They don't remove it.

## Size stopped being a matter of taste

Keeping a system small used to be an argument senior engineers lost. It sounded like preference. Nobody could price the cost of ignoring it, so teams ignored it.

You can price it now. Measure how long a small change takes end to end, and how often the agent makes things worse before better. Past a certain size, the tool you bought to go faster starts costing you time.

## A test you can run this week

Point a fresh agent at your repo with no context and no README. Ask it one question. "How does a refund work here?"

Read what comes back. If it can't trace the path, or it invents a flow that doesn't exist, your next hire is in for the same week. Twenty days of onboarding feedback in twenty seconds.

## What helps

Cap the surface area. Deleting a module counts as shipping. Name what you removed last quarter.

Write decisions down where the next session finds them. Short notes beside the code about why a boundary sits where it does.

Review the seams. You will never read every line an agent writes. You can read the interfaces and the places where money moves.

Keep someone who can draw the system from memory. When that person leaves and nobody replaces them, you own code no human has ever understood. Worse than any legacy system you've inherited. Someone understood those once.
