# New Ignatian Educator FAQ

A searchable onboarding guide for new faculty and staff — **New Ignatian Educators (NIE)** — at Regis Jesuit High School. Built by RJ Ed Tech.

**Live site:** https://rjedtech.github.io/New-Ignatian-Educator-FAQ/

## What it is

A single-page, self-contained web app that helps new employees find answers fast during their first weeks at RJ. It covers onboarding action items, tech and accounts, teaching and Canvas, classroom life, schedule and bell times, HR and benefits, safety, mission and Ignatian formation, and the classroom tools RJ uses.

## Features

- **Instant search** across every question, answer, and tag (press `/` to jump to the search box)
- **Browse by topic** — 16 topic cards, no exact wording needed
- **"Start here" set** of the questions almost every new hire asks first
- **Before-day-one checklist** and a quick **help panel** (IT, Facilities, and common requests)
- **Deep links** — every question has a shareable `#q-…` anchor
- **Light / dark mode** with a one-tap toggle
- **Fast and offline-friendly** — one HTML file, no build step, no tracking, no external dependencies. All content lives in the page; nothing is collected from the reader.

## Files in this repo

| File | Purpose |
| --- | --- |
| `index.html` | The entire app — markup, styles, content, and logic in one file. |
| `favicon.ico`, `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png` | Site icons (same set used across RJ Ed Tech pages). |

The Regis Jesuit wordmark and crest are embedded directly in `index.html`, so no logo image files are needed.

## Deploying

Hosted with **GitHub Pages** from the `main` branch root. In the repo, go to **Settings → Pages**, set the source to `main` / `/ (root)`, and the site publishes at the live URL above.

## Updating the content

All questions live in the `DATA` array inside `index.html`. Each entry looks like:

```js
{ id:"unique-id", cat:"topic-id", tags:["search","terms"],
  q:`The question`,
  a:`<p>The answer, in HTML.</p>`,
  w:LINK,                 // optional "official source" button(s)
  src:`Where it came from`,
  confirm:true }          // optional — shows a "Confirm with HR" badge
```

Topics are defined in the `CATS` array, and the "Start here" list is `START_IDS`. Edit, save, and commit — there's no build step.

## About the content

This is a **living, unofficial guide** maintained by RJ Ed Tech to help new employees get oriented. It points to My RJ and other official sources for authoritative, current details, and some items are marked *Confirm with HR*. It is not a substitute for the Employee Handbook or official school policy.

## Maintainer

RJ Ed Tech — Jason Beyer, Director of Educational Technology, Regis Jesuit High School.
Suggestions and corrections: jbeyer@regisjesuit.com
