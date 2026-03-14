---
title: "Complex Designs Are Easy. Simple Systems Are Hard."
description: "Adding complexity feels productive. Keeping things simple takes real discipline."
author: "Kyle Miller"
members_only: false
teaser: "Anyone can architect something complicated. Building something simple that actually works takes discipline most teams skip."
tags:
  - architecture
  - pragmatism
  - technical-debt
---

More layers. More abstractions. More services. More configuration. It feels productive. The architecture diagram looks impressive. The tech talks write themselves.

But every layer is a failure point. Every abstraction is something a new hire has to understand. Every service boundary is a network call that can timeout, fail, or behave differently under load.

Simple systems are harder to build because they require you to say no. No to "what if we need this later." No to the clever pattern you read about last week. No to the abstraction that handles a case you don't have yet.

Here's a test I use. Can a new developer understand this system in a week? If the answer is no, it's probably too complex for what it actually does. Not every product needs microservices. Not every API needs an abstraction layer. Not every database needs a caching tier.

I've watched teams spend months building sophisticated architectures for products that serve 200 users. The architecture could handle millions. But they didn't need millions. They needed to ship features faster.

Sophistication is easy to add and almost impossible to remove. Start simple. Stay there as long as you possibly can.
