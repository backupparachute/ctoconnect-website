---
title: "Stop Rewriting Your App"
description: "The rewrite temptation is real. Here's why it's almost always the wrong call and what to do instead."
author: "Kyle Miller"
members_only: true
teaser: "Every founder hits the moment where the codebase feels irredeemable. The rewrite fantasy is seductive. But I've watched teams burn millions on rewrites that never shipped."
tags:
  - architecture
  - technical-debt
  - rewrites
---

You're staring at a codebase that makes you cringe. Every feature takes three times longer than it should. New hires look at it and wince. You start thinking about starting over from scratch.

I've been in this exact conversation hundreds of times. The answer is almost always the same. Don't do it.

The code you're looking at took years to build. It handles edge cases nobody remembers deciding on. It manages weird customer scenarios that aren't documented anywhere. When you rewrite, you lose all of that. You spend 12 to 18 months rebuilding what you already had while your competitors ship features.

I've watched rewrites consume $50M and never ship. I've seen teams spend a year rebuilding only to end up with the same problems because the problems were never in the code. They were in the process and the requirements.

Instead try the strangler fig pattern. Pick one module. One service boundary. Rebuild just that piece. Deploy it alongside the old system. Route traffic gradually.

You get immediate wins. Lower risk because you can roll back. The whole time, you keep shipping features.

Full rewrites make sense sometimes. If the tech stack is truly dead, if the architecture fundamentally can't support what you need, or if the codebase is so small a rewrite takes two weeks. But those cases are much rarer than founders think.
