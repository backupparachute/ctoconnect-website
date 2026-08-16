---
title: "Your Team Has Stopped Reading the Alerts"
description: "An alert nobody acts on is worse than no alert. It teaches your team that pages are noise."
author: "Kyle Miller"
members_only: true
teaser: "Forty alerts a day means zero alerts. Your team learned months ago that most of them mean nothing, and now they miss the one that matters."
tags:
  - devops
  - reliability
  - process
---

Check your alert channel. Count how many fired last week. Now count how many made someone do something.

If the second number is under a tenth of the first, your team has already learned to ignore alerts. You haven't noticed because the outage hasn't happened yet.

Alert fatigue works like a callus. The first week everyone jumps. By week four they glance and go back to work. By week twelve the channel is muted on everyone's phone, and the one page that meant something scrolled past at 3 AM with the rest.

Every alert passes one test. If this fires at 3 AM, is there something a human should do right now? Disk at 71 percent is not that. A deploy finishing is not that.

Delete them. Not tune them, not route them somewhere quieter. Delete them. Anything you want to watch without waking someone belongs on a dashboard.

What's left should be rare enough that when one fires, people move.

The teams with the best incident response have less monitoring than you, pointed at things that matter.
