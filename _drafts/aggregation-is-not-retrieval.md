---
title: "Aggregation Is Not Retrieval"
description: "An AI reporting tool that lets the model add up rows returns numbers you cannot audit. Aggregation needs completeness. Retrieval only gives relevance."
author: "Kyle Miller"
members_only: false
teaser: "The total came back looking reasonable and was wrong by a factor of nine. Nothing on the screen said so, because the model summed whichever rows it happened to retrieve."
tags:
  - ai
  - architecture
  - reliability
---

Ask an AI reporting tool for total spend across every employee last quarter. The number comes back looking reasonable. It's wrong by a factor of nine and nothing on the screen says so.

This happens when the tool pulls rows into context and lets the model add them up. Two failures live in that design.

The first is arithmetic. Models are unreliable at long addition chains. Run the same question twice and get two totals.

The second is worse. Aggregation needs completeness. Retrieval gives relevance. Semantic search returns the rows most related to your question, not every row that matches it. Ask for a total across three thousand records and it may pull four hundred, sum those, and report it as final. It never knew about the rest. Similarity is not a WHERE clause.

The fix is architectural. The model translates your question into a query, the database executes it, the model reads back the result. Model at the edges, never in the middle of the arithmetic. The sum is then exact and repeatable, because a database did it.

That also gives an auditor what they need. A query you can read and rerun against source records. If raw rows go in and a total comes out, there's no artifact to inspect.

What's left is variance in query generation, and it's real. Does cost per employee include contractors? Bonuses accrued or paid? Fiscal or calendar year? An analyst makes those calls once and documents them. An agent makes them fresh every run and sounds equally sure each time.

So ask the vendor one question. When I request a total across all records, what executes the sum? If the answer involves embeddings or retrieval, walk. Then ask to see the query behind the last number they gave you.

Exploration is fine. Anything landing in a board deck or a book needs a pinned query somebody reviewed. The danger is a number that starts as exploration in March and gets quoted as fact in September.
