---
title: "Stop Rewriting Your App"
date: 2026-03-10
description: "The rewrite temptation is real. Here's why it's almost always the wrong call and what to do instead."
author: "Kyle Miller"
members_only: true
teaser: "Every founder hits the moment where the codebase feels irredeemable. The rewrite fantasy is seductive. But I've watched teams burn through millions on rewrites that never shipped. Here's what actually works."
tags:
  - architecture
  - technical-debt
---

## The Rewrite Fantasy

You're staring at a codebase that makes you cringe. Every feature takes 3x longer than it should. New hires look at it and wince. You start thinking: what if we just started over?

I've been in this exact conversation hundreds of times. And the answer is almost always the same: don't do it.

## Why Rewrites Fail

The code you're looking at took years to write. It has edge cases baked in that nobody remembers deciding on. It handles weird customer scenarios that aren't documented anywhere.

When you rewrite, you lose all of that. And you spend 12-18 months (minimum) rebuilding what you already had. Meanwhile your competitors are shipping features.

## What To Do Instead

Start with the strangler fig pattern. Pick one module. One service boundary. Rewrite that piece. Deploy it alongside the old system. Route traffic gradually.

This gives you:
- Immediate wins you can show the team
- Lower risk (you can roll back)
- Continuous delivery (you're still shipping features)

## When A Rewrite Actually Makes Sense

There are rare cases. If the tech stack is truly dead (no community, no security patches), if the architecture fundamentally can't support what you need, or if the codebase is so small that a rewrite is a 2-week project, then maybe.

But those cases are much rarer than founders think.
