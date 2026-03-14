---
title: "Goodhart's Law Is Quietly Breaking Your Engineering Metrics"
description: "When a measure becomes a target it stops being a good measure. This explains most of your broken dashboards."
author: "Kyle Miller"
members_only: false
teaser: "When a measure becomes a target, it ceases to be a good measure. This one sentence explains most broken dashboards."
tags:
  - metrics
  - engineering-leadership
  - process
---

Charles Goodhart wrote it in 1975 about monetary policy. It applies to software teams just as well.

"When a measure becomes a target, it ceases to be a good measure."

Set a code coverage target of 80%? Developers write tests that execute lines but assert nothing. Coverage goes up. Quality doesn't.

Set a velocity target? Story points inflate. The chart looks great. Delivery stays the same.

Set a deploy frequency target? Teams push empty commits and config changes. Deploys per week goes up. Value delivered doesn't move.

The pattern is always the same. A metric starts as a useful signal. Someone turns it into a target or a KPI. Behavior shifts to hit the number. The metric stops reflecting reality. Now you have a dashboard full of green numbers and a product that isn't getting better.

The fix isn't to stop measuring. It's to use metrics as conversation starters instead of scorecards. "Why did cycle time spike this week?" is a useful question. "Your cycle time needs to be under five days" is Goodhart's Law waiting to happen.

Watch your numbers. The moment one starts looking too good, ask what actually changed.
