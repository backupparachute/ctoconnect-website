---
title: "Know Your Limits Before You Ingest Everything"
description: "A client asked for AI across all their data and unknowingly specified a full ERP integration. What they needed was some SQL and a few dashboards."
author: "Kyle Miller"
members_only: true
teaser: "They asked for a system that answers questions about all their data. What they had described, without knowing it, was a full ERP integration at full ERP prices."
tags:
  - ai
  - cost
  - pragmatism
---

A client called me about a company-wide AI reporting system they'd been sold. Pull from every internal system, let agents learn it, ask anything in plain English. The demo was impressive.

What they had asked for, without realizing it, was a full ERP data integration. "AI across all our data" is one sentence in a meeting and a staffed project at a big company. Tens of millions in revenue, not hundreds. They had ordered a big system at big system prices and nobody said so.

Every layer bills separately. Moving the data, pulled continuously and metered per call. Storing it four times over as raw, cleaned, warehoused, embedded. Querying it, where warehouses charge by bytes scanned and one question about eighteen months of cost centers reads an enormous number of rows. Then the agent, which answers that in dozens of calls, times eleven managers every Monday.

The sync alone was tens of thousands in engineering. The rest added a four figure monthly bill before a single AI query ran. Maybe the vendor had it costed. The client couldn't tell me, which is the problem.

So know your limits first. What's a material monthly bill at your size? Which questions get asked often enough to justify this?

I offered them something else. Tell me the questions and I'll write the SQL and build the dashboards. That's what we did, at a fraction of the quote.
