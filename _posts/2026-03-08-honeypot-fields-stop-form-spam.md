---
title: "Honeypot Fields. The Simplest Way to Stop Form Spam."
description: "Before you reach for CAPTCHA, try the trick that stops 90% of bots without annoying a single real user."
author: "Kyle Miller"
members_only: false
teaser: "CAPTCHAs annoy real users. Honeypot fields catch bots without anyone noticing. Sometimes the simplest solution wins."
tags:
  - security
  - web-development
  - pragmatism
---

Your contact form gets 200 spam submissions a day. So you add reCAPTCHA. Spam drops. But so do real submissions. People hate clicking on crosswalks and traffic lights. Some give up entirely.

There's a simpler approach. Add a hidden form field. Hide it with CSS so real users never see it and never fill it in. Bots don't render CSS. They see a form field and fill it in automatically.

On the server side, check that hidden field. If it has a value, it's a bot. Reject the submission silently. Don't even return an error. Just drop it.

Implementation takes about ten minutes. Add an input field. Give it a name that sounds real, like `website` or `company`. Hide it with `display: none` or position it off-screen with CSS. Check it server-side before processing the form.

It won't stop sophisticated bots that render JavaScript and detect hidden fields. For those you'll need additional layers. But for the vast majority of automated spam, a hidden input field is enough.

Not every problem needs a complex solution.
