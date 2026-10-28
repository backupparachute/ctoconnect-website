---
title: "Legacy Code Used to Take Ten Years"
description: "A codebase goes legacy when nobody left understands it. AI cut that from a decade to a quarter."
author: "Kyle Miller"
members_only: false
teaser: "Legacy code used to take a decade of turnover. Now it shows up in three months, and nobody understood it in the first place."
tags:
  - ai
  - architecture
  - technical-debt
---

A codebase goes legacy when nobody left can explain it. That used to take a decade. Two rounds of turnover, the founder leaves, and nobody knows how billing works.

Now it takes a quarter.

I've worked in codebases four months old that nobody can explain. The code is clean. The tests pass. Nobody knows why the retry logic sits where it does, or which of the two user lookups is the real one. The agent that wrote it forgot when the session ended. The person who approved the pull requests skimmed them.

## You'll see it in the agent first

It builds a second version of something that already exists, because it never found the first. It fixes a bug by stacking a guard clause on last week's guard clause. It rewrites working code because the file is too big to hold at once.

The system outgrew the memory of whatever maintains it. Bigger models raise that ceiling. They don't remove it.

## Run this test

Point a fresh agent at your repo. No context, no README. Ask it one question: "How does a refund work here?"

If it can't trace the path, or it invents one, your next hire gets the same week.

## What helps

Keep it small. Deleting a module counts as shipping.

Write down why a boundary sits where it does. Put the note next to the code, where the next session will find it.

Review the seams. You won't read every line an agent writes. Read the interfaces and the places where money moves.

Keep one person who can draw the system from memory. Old legacy code had someone who understood it once. Yours might never have had anyone.
