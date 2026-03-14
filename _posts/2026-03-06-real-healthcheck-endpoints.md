---
title: "Why Every Production App Needs a Real Healthcheck Endpoint"
description: "If your healthcheck only confirms the process is running, it's hiding the problems that actually take you down."
author: "Kyle Miller"
members_only: true
teaser: "If your healthcheck just returns 200 OK, it's lying to you. A real healthcheck tests the things that actually break."
tags:
  - devops
  - architecture
  - reliability
---

Most healthcheck endpoints look like this. Hit `/health`. Get back `{ "status": "ok" }`. Load balancer sees a 200. Everything looks fine.

Meanwhile the database connection pool is exhausted. Redis is full. The payment API is timing out. Your app happily reports healthy because the process is still running.

A real healthcheck tests the things that actually break. Can we connect to the database? Is the cache responding? Are critical third-party services reachable? If any of these fail, the healthcheck should return a degraded or unhealthy status.

Keep it fast though. Don't run full queries or heavy operations inside the healthcheck. Just ping the connections. Verify they respond. The healthcheck itself shouldn't cause load or slow down under pressure.

Some teams add a `/health/ready` endpoint that's more thorough and a `/health/live` endpoint that's lightweight. The liveness check tells the orchestrator the process is running. The readiness check tells the load balancer it can handle traffic. Both are useful.

Your load balancer can only route traffic correctly if it knows the truth about your app. Tell it the truth.
