# CTO Connect Website

The site for [ctoconnect.io](https://ctoconnect.io). Jekyll and Bootstrap 5, hosted on GitHub Pages.

## What the site sells

Three services, in order of how involved Kyle is:

| Service | Price | What it is |
|---|---|---|
| CTO Deep Dive | $600 one-time | One 90-minute working session on one problem. Booked and paid directly through Calendly. |
| CTO Advisory | $1,800/month | One 90-minute session every week. Nothing between sessions. Starts with a diagnostic call. |
| Fractional CTO | from $4,000/month | Kyle involved in the company and delivering the work a CTO delivers. Scoped on a diagnostic call. |

Every page funnels to the **free 20-minute diagnostic call**. It is a fit conversation, not a free consulting session.

There is no membership, no login and no paid content tier. Some articles are marked `members_only: true` in their front matter. Those show a teaser and a newsletter form. Subscribing opens the article in that browser.

## Integrations

Everything external lives in `_config.yml`:

| Key | Used for |
|---|---|
| `diagnostic_call_url` | Calendly event for the free 20-minute call. **TODO: replace the placeholder.** |
| `deep_dive_url` | Calendly event for the paid Deep Dive. Stripe payment is collected at booking. |
| `newsletter_endpoint` | Where the newsletter form posts. **TODO: replace the placeholder.** |

### Newsletter endpoint contract

`_includes/newsletter-form.html` sends:

```
POST <newsletter_endpoint>
Content-Type: application/json

{"email": "you@company.com", "source": "/articles/some-slug/"}
```

Any 2xx response counts as subscribed. The form then sets `localStorage.ctoc_subscribed = "1"` and reveals every `[data-gated]` element on the page (see the gate script in `_layouts/default.html`). Anything else shows an inline error and keeps the form. A hidden `website` field is a honeypot. If it is filled, the form pretends to succeed and never posts.

The endpoint is expected to handle double opt-in and add the contact to Resend.

Analytics are Fathom. Button clicks fire `fathom.trackEvent(...)`.

## Local development

```bash
bundle install
LANG=C.UTF-8 LC_ALL=C.UTF-8 bundle exec jekyll serve
```

The locale matters. Without UTF-8 the Sass converter fails on the theme's stylesheet.

If `bundle exec jekyll` says the command is not found, run it through the gem path:

```bash
LANG=C.UTF-8 LC_ALL=C.UTF-8 bundle exec ruby "$(bundle show jekyll)/exe/jekyll" serve
```

## Project structure

```
_config.yml              Site settings and the integration URLs above
_layouts/default.html    Head, nav, footer, newsletter gate script
_layouts/article.html    Article page. Handles the subscriber gate.
_layouts/articles-index.html
_includes/nav.html
_includes/cta-diagnostic.html   Closing call-to-action band used on service pages
_includes/newsletter-form.html  Signup form plus the reveal logic
_includes/testimonials.html     Renders _data/testimonials.yml
_includes/article-card.html
_data/testimonials.yml
_posts/                  Published articles
_drafts/                 Unpublished articles
index.html               Homepage
pricing.html             /pricing/  Services comparison
deep-dive.html           /deep-dive/  (redirects from /private-session/)
advisory.html            /advisory/
fractional-cto.html      /fractional-cto/
about.html
ai.html, build.html, craft.html   Unlinked landing pages used for outreach experiments
```

## Writing an article

Add a file to `_posts/` named `YYYY-MM-DD-slug.md`:

```yaml
---
title: "Title"
description: "One sentence. Used for SEO and the article card."
author: "Kyle Miller"
members_only: false     # true shows a teaser and the newsletter form
teaser: "Optional. Shown above the gate on subscriber articles."
tags:
  - architecture
---
```

## Deployment

Push to `main`. GitHub Pages builds and deploys. The custom domain is set in `CNAME`.

## Contact

kyle@ctoconnect.io
