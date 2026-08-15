---
title: "A New Hire Is Your Best Bug Report"
description: "The first week a new engineer spends on your codebase exposes every broken assumption in your setup. Write it down while they still notice."
author: "Kyle Miller"
members_only: true
teaser: "Your setup doc works for exactly one person. You. A new hire finds every gap in it during week one, then forgets they were ever confused."
tags:
  - team-culture
  - standards
  - process
---

Every new engineer runs the same experiment. They clone the repo, follow your setup instructions, and hit a wall. Some environment variable nobody documented. A service that has to run first. A migration that fails on a fresh database.

They figure it out in a day or two, ask a teammate, and move on. The knowledge goes into their head and nowhere else. Six months later the next hire hits the identical wall.

That first week is the only time anyone sees your project with fresh eyes. Use it.

Make the setup doc the new person's first pull request. Not as busywork. They follow it exactly as written, and every place it fails, they fix the doc. They're the only person qualified to write it, because everyone else stopped noticing the gaps years ago.

The same goes for whatever confused them. Why does the billing service have its own database? What does that queue do? Those questions feel obvious to you and invisible to them. Both of you are wrong about which parts are hard.

Good onboarding docs pay for themselves in a number you can measure. Time from clone to running app. If a competent engineer can't get your app running in an afternoon without asking anyone, that's a bug. Track it like one.

The team that can onboard someone in a day can also survive a key person leaving. Those turn out to be the same problem.
