---
title: "Make It Work. Make It Pretty. Make It Fast."
description: "There's a sequence to building software that most teams get wrong. Respecting the order saves weeks of wasted effort."
author: "Kyle Miller"
members_only: false
teaser: "Most teams get the order wrong. They polish before they prove. There's a better sequence."
tags:
  - process
  - architecture
  - pragmatism
---

I see teams spend three weeks polishing a UI for a feature that doesn't work yet. Or tuning database queries before anyone has validated that the feature is worth building. They're solving the wrong problem at the wrong time.

There's a simple order that works.

First, make it work. Get the logic right. Ugly code is fine. Hardcoded values are fine. The only question is "does this thing do what it's supposed to do?" If the answer is no, nothing else matters.

Then make it pretty. Clean up the code. Build the real UI. Refactor the parts that are hard to read. This is where craftsmanship lives, but only after the thing actually works.

Then make it fast. Profile it. Find the actual bottlenecks. Optimize the queries that are slow in production, not the ones you think might be slow someday. You'll be surprised how little actually needs optimization.

Most premature optimization and most wasted design effort comes from doing these steps out of order. Build the proof first. Make it beautiful second. Make it fast last.
