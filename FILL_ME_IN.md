# Fill-me-in checklist for blazewallick.com

Everything is in one file: **`index.html`**. Open it and search for `EDIT:` to jump to each spot.
No build step, no framework install — just edit and push. GitHub Pages redeploys automatically.

## 1. Photos  📸
Your web-optimized photos live in **`/photos`** (`photo1`, `photo2`, `photo3`, each as `.webp` + `.jpg`).
To change a photo, replace those files and keep the same names. If you only have a new `.jpg`,
that's fine — the page falls back to `.jpg` when there's no `.webp`.

> The original full-size images you provided were ~11 MB total (too heavy for a phone on cellular).
> I resized/compressed them to ~1 MB total. Captions are under each `<figcaption>` in `index.html`.

## 2. Your name & tagline  ✍️  → search `EDIT: HERO`
- Headline text and the short intro paragraph (the "lede").

## 3. Your story / community  → search `EDIT: ABOUT`
- The two paragraphs about what you're building.
- The interest "pills" (Fitness, Building things, …).
- The three "values" cards.

## 4. The six fun questions  → search `EDIT: QUESTIONS`
- Each card has a **question** (front) and **your answer** (back, marked `EDIT:`).
- Replace every `EDIT: e.g. …` with your real answer.
- Add or remove cards freely — the grid just reflows.

## 5. Contact details  → search `EDIT: CONTACT`
- **Email:** replace `blaze@blazewallick.com` (appears in the link text and `mailto:`).
- **LinkedIn:** replace `https://www.linkedin.com/in/blazewallick` and the visible `in/blazewallick`.
- **Phone:** set the real number in `data-tld="+1-555-000-0000"`. It stays hidden until a visitor
  taps "Tap to reveal" (light protection against scraper bots). Currently a placeholder.

## 6. Save-contact card (.vcf)  → search `EDIT: VCARD`
- Update `FN`, `EMAIL`, `TEL`, and the LinkedIn `URL` to match section 5 so the downloaded
  contact card is correct.

---

## Notes on privacy & security
- **Phone number:** shown only after a tap and assembled in JavaScript rather than sitting in the
  raw HTML, so basic scrapers won't grab it. This is *light* protection, not a guarantee — anything
  on a public page can ultimately be read. If you'd prefer the number never be public, leave the
  placeholder and let people get it from the `.vcf` after they email you, or point them to a form.
- **No secrets in this repo.** It's a static site — there are no API keys, tokens, or passwords, so a
  **public** repo is fine (and required for free GitHub Pages on a user/project site). Keep it public.
- **Nothing is submitted anywhere.** There's no form posting to a server, no trackers, no third-party
  analytics — just links you control. If you later add a contact form, use a reputable service
  (e.g. Formspree) and never paste credentials into the HTML.
- **Custom domain:** `CNAME` still points to `blazewallick.com`. In your repo's
  *Settings → Pages*, keep "Enforce HTTPS" enabled.

## Local preview
```bash
python3 -m http.server 8000   # then open http://localhost:8000
```
