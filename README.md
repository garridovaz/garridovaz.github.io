# garridovaz.com — new site

## Setup

```bash
bundle install
bundle exec jekyll serve --livereload
```

Open http://localhost:4000

## Before going live, carry over from the old repo

- `CNAME` — copy your existing one so the custom domain keeps working
- `assets/` (old images) — only if any blog posts/pages reference them
- Old `_posts` / `_drafts` — intentionally NOT included; they're in your
  local backup folder if you want to bring any back later

## Things drafted for you to review/edit

- `services.md` — the four service cards are drafted from your CV's
  areas of expertise, not things you told me to offer. Edit copy,
  add pricing/engagement model if you want it public.
- `contact.md` — currently just an email + LinkedIn link, no working
  form (a static Jekyll site has no backend to receive submissions —
  see note below).

## Contact form

You asked for a contact form. A plain Jekyll/GitHub Pages site can't
process form submissions itself (no backend). Two common ways to add
a real one:
1. **Formspree** (or similar) — free tier, you get an endpoint URL,
   drop it into a `<form action="https://formspree.io/f/xxxxx">`.
2. **mailto link** (what's there now) — zero setup, opens the user's
   email client.

Let me know if you want me to wire up Formspree once you've made an account.
