---
title: "The AI Was the Cheap Part"
description: "A client was sold a company-wide AI reporting system. The model turned out to be the smallest line item. Nobody had priced the data underneath it."
author: "Kyle Miller"
members_only: true
teaser: "Ingest everything, let agents learn it, ask any question in plain English. The demo was impressive. Nobody had priced the ingress, the storage, the scans, or the compute."
tags:
  - ai
  - cost
  - pragmatism
---

A client called me about a company-wide AI reporting system they'd been sold. Pull data from every internal system, let agents ingest and learn it, then ask any question in plain English and get an answer back. The demo was impressive.

Nobody had priced the plumbing.

The model is rarely where the money goes. Here's where it goes.

**Moving the data.** Every source system has to be pulled continuously, not once. Some vendors bill per API call or per record exported, and that meter runs forever.

**Storing the data.** You don't store it once. There's the raw copy, the cleaned copy, the warehouse copy, and the embeddings. That's the same information four times, growing every month, and none of it gets smaller on its own.

**Querying the data.** Warehouses bill by bytes scanned. "Compare the last eighteen months against the same months two years ago across every cost center" reads an enormous number of rows to produce one number.

**Running the agent.** It doesn't answer a question like that in one shot. It plans, queries, reads the result, queries again, aggregates, and holds all of it in context. One business question becomes dozens of calls. Now picture eleven managers asking that same question every Monday morning.

Before you sign anything, do this. Pick three questions your team already asks. Price each one end to end, including the storage and the scans, not just the model call. Multiply by how many people will ask and how often they'll ask it.

Then work out which of those three a scheduled report would have answered for close to nothing.

Sometimes you genuinely need the system. More often you needed four dashboards and someone who knows SQL.
