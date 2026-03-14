---
title: "The Security Checklist Nobody Follows Until It's Too Late"
description: "Most startups skip basic security practices until something breaks. These are the basics that should be in place before you launch."
author: "Kyle Miller"
members_only: true
teaser: "Most startups skip basic security until something breaks. These are the fundamentals that should be in place before you have something worth stealing."
tags:
  - security
  - architecture
  - standards
---

Nobody thinks about security until something goes wrong. Then it's the only thing anyone thinks about.

I'm not talking about SOC 2 or penetration testing. Those come later. I'm talking about the basics that most teams skip because they're "too early" for security. You're never too early for the fundamentals.

HTTPS everywhere. No exceptions. Not even for internal services. Free with Let's Encrypt. There is no excuse.

Secrets out of your code. No API keys in your repo. No database passwords in config files that get committed. Use environment variables or a secrets manager. If you grep your repo and find a password, fix it today.

Dependency audits. Run `npm audit` or `bundle audit` or whatever your ecosystem has. Do it in CI so it can't be skipped. Outdated dependencies with known vulnerabilities are the easiest attack vector that exists.

Rate limiting on authentication endpoints. Login, password reset, signup. If someone can hit your login endpoint a million times, they will.

Principle of least privilege. Your application database user doesn't need DROP TABLE permissions. Your staging environment doesn't need access to production data. Give everything the minimum access it needs to function.

Backups that you've actually tested restoring. Having backups is not the same as being able to recover. If you've never done a restore drill, you don't have backups. You have hope.

None of this is glamorous. All of it will save you when something eventually goes sideways.
