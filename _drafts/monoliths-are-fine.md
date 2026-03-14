---
title: "Monoliths Are Fine"
description: "Microservices solve scaling problems most teams don't have yet. A well-structured monolith will take you further than you think."
author: "Kyle Miller"
members_only: true
teaser: "Microservices are a scaling solution, not a starting point. Most teams adopt them way too early and pay the price for years."
tags:
  - architecture
  - pragmatism
  - technical-debt
---

Somewhere around 2016, the industry decided monoliths were bad. If you weren't breaking your app into microservices, you were doing it wrong. Conference talks made it sound inevitable. Blog posts made it sound easy.

It's neither.

Microservices solve a specific problem. When your organization is large enough that teams step on each other, when you need to scale one part of your system independently, when deploy coordination across teams becomes the bottleneck. That's when microservices earn their complexity.

Most startups and mid-size teams don't have those problems. They have a single team working on a single product. A monolith lets that team move fast. One repo. One deploy pipeline. One place to debug. Shared models, shared types, function calls instead of network requests.

The moment you go to microservices, you inherit distributed systems problems. Network latency. Service discovery. Data consistency across boundaries. Distributed tracing. Each of these is a discipline on its own. Your team just went from building product to building infrastructure.

I've seen five-person teams running twelve services. Every feature requires changes to three repos. Deploys take coordination meetings. They built Netflix's architecture for an app with 500 users.

Start with a monolith. Structure it well. Extract a service when you have a real reason, not because a blog post told you to.
