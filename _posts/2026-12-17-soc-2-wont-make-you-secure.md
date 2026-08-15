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

SOC 2 proves you wrote down a process and followed it. That's the whole claim. An auditor checks that your stated controls exist and that you have evidence of them running. If your stated control is "we review access quarterly," and you have four tickets showing you did, you pass.

Notice what nobody checked. Whether quarterly is often enough. Whether the reviewer understands what they're approving. Whether the system you're reviewing access to is the one that matters.

You can pass SOC 2 with a SQL injection on your login page. It happens.

None of that makes it worthless. Enterprise buyers require it, so it unblocks deals, and going through it forces you to write down what only lived in one engineer's head. That's real value. Just put it in the right budget. It's a sales expense with a security side effect, not the reverse.

The failure I see is sequencing. A team spends nine months and $60k on the audit while running database backups they've never restored and API keys sitting in a repo. They bought the certificate before the thing the certificate is supposed to describe.

Do the fundamentals first. Then, when a deal needs the letters, go get the letters. You'll pass faster and spend less, because the controls will already describe what you do rather than what you promised to start doing.
