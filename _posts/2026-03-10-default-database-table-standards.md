---
title: "Default Standards Every Database Table Should Follow"
description: "Most database headaches come from inconsistent conventions established in the first month. A few defaults prevent years of pain."
author: "Kyle Miller"
members_only: false
teaser: "Most database messes start with inconsistent basics. A few simple defaults prevent years of pain."
tags:
  - database
  - architecture
  - standards
---

One table uses `createdAt`. Another uses `created_at`. A third has no timestamp at all. Primary keys are `id` here, `userId` there, and `user_id` somewhere else. Every developer who touches the database has to guess the convention. They guess differently.

This kind of inconsistency seems minor early on. It becomes a real problem at scale. Queries are harder to write. Migrations are riskier. Onboarding takes longer because nothing is predictable.

The fix is boring and effective. Establish a small set of defaults and stick to them.

Every table gets an `id` column. Pick UUID or auto-increment. Pick one and use it everywhere. Every table gets `created_at` and `updated_at` timestamps. No exceptions. Use `snake_case` for all column and table names. Add an index on any column you regularly filter or sort by.

One more convention I swear by. Use `_at` for datetime fields and `_date` for date-only fields. `published_at` vs `birth_date`. It reads clearly and you always know what type you're working with. I also prefer datetime fields over booleans. Instead of `is_verified` as a boolean, use `verified_at` as a nullable timestamp. If it's present, it's true. If it's null, it's false. You get the same logic plus you know exactly when it happened. A boolean can't tell you that.

Put these standards in a shared doc. Better yet, build a migration template that pre-fills the defaults so developers don't have to remember them.

None of this is exciting. That's the point. Boring consistency in your schema means fewer surprises in your queries, your migrations, and your 3am debugging sessions.
