# Fill-me-in checklist for blazewallick.com

Everything is in one file: **`index.html`**. Open it and search for `EDIT:` to jump to each spot.
No build step, no framework install — just edit and push. GitHub Pages redeploys automatically.

## 1. Photos  📸
The gallery holds **six** photos, in `/photos` as `photo1 … photo6` (each `.webp` + `.jpg`).
Any slot whose file is missing **hides itself automatically**, so the grid never looks broken.

**Current status:** only `photo3` (the Japan shrine shot — the one you said to keep) is in place.
The other five come from images you pasted into chat, and pasted images don't reach the build
environment as files — so I couldn't drop them into `/photos` myself. Getting them in takes ~30s:

### How to add your 5 photos (pick one)
- **Easiest — GitHub web:** open the repo → the `photos/` folder → **Add file ▸ Upload files**,
  drag your originals in, and commit to branch `claude/fervent-brahmagupta-prmb7o`. Then tell me
  "photos uploaded" and I'll auto-resize/compress them into the right `photoN.webp/.jpg` names.
- **Or** commit them yourself with these exact names (any size — but smaller loads faster):
  `photo1.jpg photo2.jpg photo4.jpg photo5.jpg photo6.jpg`.

### The mapping I built the captions around
| Slot | Photo you sent | Caption |
|------|----------------|---------|
| photo1 | Eating an exotic fruit on the dock | "Trying every fruit I can find 🍈" |
| photo2 | Holding the white French bulldog | "Borrowing someone's dog 🐾" |
| photo3 | **(kept)** Japan shrine gate | "Wandering, somewhere in Japan ⛩️" |
| photo4 | At the cafe with a friend | "Good people, good coffee ☕" |
| photo5 | At the tech conference | "Nerding out at a tech conference 👋" |
| photo6 | Balcony portrait (patterned shirt) | "Cleaned up 🌴" |

Swap any caption in `index.html` (search the alt text). Photos are auto-optimized to ~1 MB total
so the page stays fast on a phone.

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
