---
title: "Big PRs Don't Get Reviewed"
description: "A forty file pull request gets an approval, not a review. Small changes get read. Large ones get a signature."
author: "Kyle Miller"
members_only: false
teaser: "Nobody reads a forty file pull request. They scroll to the bottom and click approve. Small PRs get real review. Big ones get rubber stamped."
tags:
  - process
  - team-culture
  - pragmatism
---

Open a pull request with eight files and you get comments. Open one with forty and you get "LGTM."

That's not laziness. Reviewing forty files properly takes two hours of focused attention, and your reviewer has their own work. So they skim the parts they recognize, trust you on the rest, and approve. The review happened on paper. Nobody reviewed anything.

I've watched teams treat approval counts as a quality signal while shipping enormous changes nobody read. The metric looked great. The bugs kept landing.

Small pull requests fix this without process. Under 400 lines, a reviewer can hold the whole change in their head. They spot the missing null check. They ask why you renamed that method. Above a thousand lines, they're pattern matching, and pattern matching is what your linter already does.

The objection is always the same. "This feature is big, it can't be split." Usually it can. Ship the migration first. Then the model. Then the endpoint behind a flag. Each piece merges on its own and none of them break production.

If a change genuinely can't be split, walk the reviewer through it live. Twenty minutes on a call beats a week of silence followed by an approval nobody meant.

Your CI catches the mechanical problems. Human review exists for judgment, and judgment doesn't survive contact with a forty file diff.
