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

A client called me about a company-wide AI reporting system they'd been sold. Pull from every internal system, let agents learn it, then ask any question in plain English. The demo was impressive.

What they had asked for, without realizing it, was a full ERP data integration. "AI across all our data" is one sentence in a meeting and a staffed project at a large company. Tens of millions in revenue, not hundreds. They had ordered a big system at big system prices and nobody said so.

Nobody had measured any of it either. Every layer below bills separately.

**Moving the data.** Every source system has to be pulled continuously, not once. Some vendors bill per API call or per record, and that meter runs forever.

**Storing the data.** You store it more than once. Raw copy, cleaned copy, warehouse copy, embeddings. The same information four times, growing every month, and none of it shrinks.

**Querying the data.** Warehouses bill by bytes scanned. "Compare the last eighteen months against the same months two years ago across every cost center" reads an enormous number of rows to return one.

**Running the agent.** It doesn't answer that in one shot. It plans, queries, reads the result, and queries again. One question becomes dozens of calls, and eleven managers ask it every Monday. The AI layer is not cheap either.

Building the sync came to tens of thousands in engineering. Warehouse, ingress, storage and backups looked like a four figure monthly bill before a single AI query ran.

Maybe the vendor had it all costed. The client couldn't tell me, and that's what should worry you. If you can't separate model spend from data spend, you can't tell whether a quote is complete.

So know your limits before you take that meeting. What's a material monthly bill at your size? How much data do you have? Which questions does your team ask often enough to justify this?

I made them a different offer. Tell me the questions you want answered and I'll write the SQL and build the dashboards. That's what we did, at a fraction of the quote.

The platform might be right for you one day. Find out what a few queries and a dashboard cover first. It's usually most of it.
