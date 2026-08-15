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

Nobody had measured it either. Every layer bills separately.

**Moving the data.** Pulled continuously, not once. Some vendors bill per API call or per record, and that meter never stops.

**Storing the data.** Raw copy, cleaned copy, warehouse copy, embeddings. The same information four times, growing monthly.

**Querying the data.** Warehouses bill by bytes scanned. "Compare eighteen months against the same months two years ago across every cost center" reads an enormous number of rows to return one.

**Running the agent.** Not one shot. It plans, queries, reads, queries again. One question becomes dozens of calls, times eleven managers every Monday. The AI layer is not cheap either.

The sync alone was tens of thousands in engineering. Warehouse, ingress, storage and backups added a four figure monthly bill before a single AI query ran.

Maybe the vendor had it costed. The client couldn't tell me, which is the real problem. If you can't separate model spend from data spend, you can't tell whether a quote is complete.

So know your limits first. What's a material monthly bill at your size? How much data do you have? Which questions get asked often enough to justify this?

I offered them something else. Tell me the questions and I'll write the SQL and build the dashboards. That's what we did, at a fraction of the quote.

The platform might be right one day. Find out what a few queries and a dashboard cover first. Usually that's most of it.
