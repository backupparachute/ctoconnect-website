---
title: "Logs Are Not Observability"
description: "Grepping through log files at 2am is not a monitoring strategy. Logs, metrics, and traces solve different problems."
author: "Kyle Miller"
members_only: true
teaser: "If your incident response plan is 'grep the logs,' you're going to have a long night. Logs, metrics, and traces are three different tools for three different problems."
tags:
  - devops
  - reliability
  - architecture
---

Something breaks in production. The on-call engineer opens a terminal and starts grepping through log files. Twenty minutes later they're scrolling through thousands of lines looking for the one error that matters. This is not observability. This is archaeology.

Logs, metrics, and traces solve different problems. Mixing them up is why most teams spend hours debugging issues that should take minutes.

Metrics tell you something is wrong. Request latency spiked. Error rate jumped. CPU is pegged. You don't need to know why yet. You need to know where to look.

Traces tell you where it's wrong. A single request touched seven services and the third one took four seconds. Now you know which service to investigate. Without traces, you're guessing which log file to open.

Logs tell you why it's wrong. Once you know the service, the timestamp, and the request ID, logs become useful. A stack trace, a failed query, a nil pointer. That's the detail you need. But only after metrics and traces pointed you there.

There's a fourth layer worth mentioning. Error tracking services like Honeybadger, Sentry, or Bugsnag. These sit between metrics and logs. They catch exceptions in real time, group them, and give you the stack trace with context before you even know something is wrong. If you don't have full observability yet, an error tracker is the fastest win you can add.

Most teams have logs and nothing else. They bolt on a dashboard with some graphs and call it monitoring. Then an incident hits and they're back in the terminal scrolling through text files.

Invest in all three. Metrics for detection. Traces for localization. Logs for diagnosis. In that order.
