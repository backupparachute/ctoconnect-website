---
title: "SOC 2 Won't Make You Secure"
description: "Compliance proves you have a process. It doesn't prove the process is any good. Know which one you're buying."
author: "Kyle Miller"
members_only: true
teaser: "SOC 2 is a sales tool. Useful, expensive, and routinely confused for security. Passing the audit and being hard to break into are different projects."
tags:
  - security
  - standards
  - pragmatism
---

A while back I wrote that SOC 2 comes later, after the basics. Here's the later part.

SOC 2 proves you wrote down a process and followed it. That's the whole claim. An auditor checks your stated controls exist and that you have evidence of them running. If your control is "we review access quarterly" and you have four tickets showing you did, you pass.

Notice what nobody checked. Whether quarterly is often enough. Whether the reviewer understands what they're approving.

You can pass SOC 2 with a SQL injection on your login page. It happens.

That doesn't make it worthless. Enterprise buyers require it, so it unblocks deals, and the process forces you to write down what only lived in one engineer's head. Just put it in the right budget. It's a sales expense with a security side effect.

The failure I see is sequencing. Teams spend nine months on the audit while running backups they've never restored and API keys sitting in a repo. They bought the certificate before the thing it describes.

Do the fundamentals first. Then get the letters when a deal needs them.
