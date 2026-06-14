# Meta-Analysis Thesis Handbook — Dr. Abdelwahab Ghazy

A single-file website (`index.html`) — an interactive handbook for writing a
systematic-review / meta-analysis thesis, plus an author + mentoring page that
turns visitors into leads.

---

## 1. Before you publish — fill in 5 things (5 minutes)

Open `index.html`, find the block near the top marked **`EDIT ME`**
(`window.SITE_CONFIG`), and paste your details between the quotes.
**Anything you leave blank simply hides itself** — the site still works.

| Field | What to paste | If left blank |
|-------|---------------|---------------|
| `whatsapp` | Already set to `201030080342` | — |
| `calendly` | Your booking link, e.g. `https://calendly.com/drghazy/intro` | "Book a free call" button is hidden |
| `web3formsKey` | Free key (see step 2) | Contact form falls back to opening the visitor's email app |
| `social.linkedin` etc. | Full profile URLs | That icon is hidden |
| `siteUrl` | Your final URL once you have one | Canonical/SEO link skipped |

### 2. Make the contact form email you directly (optional, free)
1. Go to **https://web3forms.com**, enter your email, and get an **Access Key**.
2. Paste it into `web3formsKey` in `SITE_CONFIG`.
3. Done — form submissions now arrive in your inbox. No server needed.

### 3. Social share image
`og-image.svg` is your ready-made share banner. Most platforms (WhatsApp,
Facebook, LinkedIn) prefer **PNG**, so convert it once:
- Open `og-image.svg` in a browser → screenshot it, **or** use any free
  "SVG to PNG" converter → save as `og-image.png` in this folder.
- (The page already points to `og-image.png`.)

---

## 4. Publish it (pick ONE — all free)

### Option A — Netlify Drop (easiest, ~2 min, recommended)
1. Go to **https://app.netlify.com/drop**
2. Drag this whole folder onto the page.
3. You instantly get a live URL like `random-name.netlify.app`.
4. (Optional) In *Site settings → Change site name* to pick a nicer name.

### Option B — Cloudflare Pages
1. **https://pages.cloudflare.com** → *Create a project → Direct Upload*.
2. Upload this folder. You get `your-project.pages.dev`.

### Option C — GitHub Pages
1. Create a repo, upload these files (`index.html` must be at the root).
2. Repo *Settings → Pages → Source: `main` branch / root → Save*.
3. Live at `https://<username>.github.io/<repo>/`.

### Add a custom domain (e.g. drghazy.com)
1. Buy the domain (Namecheap, GoDaddy, Cloudflare, etc.).
2. In your host (Netlify/Cloudflare/GitHub) → *Domain settings → Add custom domain*.
3. Follow their DNS instructions (usually a `CNAME` record, or `A` records).
   Each host shows the exact values to paste at your registrar.
4. HTTPS is issued automatically (free) within a few minutes.
5. Put your final address into `siteUrl` in `SITE_CONFIG`.

---

## 5. Files in this folder
- `index.html` — the entire website (edit `SITE_CONFIG` at the top).
- `og-image.svg` — social share banner (convert to `og-image.png`).
- `robots.txt` — lets search engines index the site.
- `README.md` — this guide.

## Notes
- The site loads Tailwind & Chart.js from a CDN, so it needs an internet
  connection to render — totally fine for any normal hosting.
- No build step, no backend, no database. Just static files.
