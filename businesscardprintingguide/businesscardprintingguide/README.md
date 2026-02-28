# businesscardprintingguide.com — Astro Site

EMD mini hub for CRST. Built with Astro + Tailwind CSS.
Powered by CRST.net | Hudson Valley, NY.

---

## Replit Setup (Do This First)

1. Create a new Replit → choose **Node.js** template
2. Upload all files from this folder into Replit
3. Open the Shell tab and run:

```bash
npm install
npm run dev
```

4. Replit will give you a preview URL — open it to see the site.

---

## Deploying to Cloudflare Pages (Recommended — Free)

1. Push this project to GitHub
2. Go to dash.cloudflare.com → Pages → Create a project
3. Connect your GitHub repo
4. Set build command: `npm run build`
5. Set output directory: `dist`
6. Deploy — Cloudflare will auto-deploy on every git push

---

## Connecting GHL Lead Form

The lead form placeholder is in:  
`src/components/LeadForm.astro`

Find the comment block:
```
<!-- GHL FORM EMBED — Replace this div with your GoHighLevel iframe embed snippet -->
```

1. Go to GHL (CRST Web) → Sites → Forms or Funnels
2. Select/create the business card quote form
3. Click Share → Embed → copy the `<iframe>` or `<script>` tag
4. Paste it inside the `<div id="ghl-form-container">` div
5. Delete the `<!-- PLACEHOLDER FORM -->` section above it

---

## File Structure

```
src/
├── layouts/
│   └── Base.astro         ← Header, footer, SEO, fonts, schema
├── components/
│   └── LeadForm.astro     ← GHL form embed (swap placeholder when ready)
└── pages/
    ├── index.astro                        ← Hub: Business Card Printing Guide
    ├── vistaprint-business-cards.astro    ← Spoke: 60,500 vol KD 0
    ├── print-business-cards.astro         ← Spoke: 12,100 vol KD 16
    ├── gotprint-business-cards.astro      ← Spoke: 5,400 vol KD 0 [VA content needed]
    ├── fedex-business-card-printing.astro ← Spoke: 1,900 vol KD 0 [VA content needed]
    ├── staples-business-card-printing.astro ← Spoke: 5,400 vol KD 13 [VA content needed]
    └── get-a-quote.astro                  ← Lead capture page
```

---

## VA Content Tasks

Three spoke pages need full articles (see placeholder notes in each file):

| Page | Target Keyword | Vol | KD | Word Count |
|---|---|---|---|---|
| gotprint-business-cards.astro | gotprint business cards | 5,400 | 0 | 800–1,000 |
| fedex-business-card-printing.astro | fedex business card printing | 1,900 | 0 | 700–900 |
| staples-business-card-printing.astro | staples business card printing | 5,400 | 13 | 700–900 |

All articles must:
- Include Key Takeaways box
- Include pricing table
- Include internal links back to hub (/) and 2–3 other spokes
- Include inline CTA → /get-a-quote/
- Pass Alex Meyerhans Content Quality Rater GPT before publishing

---

## Internal Linking Rule

Every page follows: Spoke → Hub (/) → crst.net service page → Get an Estimate

This is already wired into the hub and 2 complete spokes. Maintain it in all new articles.

---

## Colors & Brand

| Token | Value | Use |
|---|---|---|
| `ink` | #1a1a2e | Dark navy — headers, text |
| `paper` | #faf8f5 | Warm off-white — backgrounds |
| `gold` | #c9a84c | Gold accent — CTAs, highlights |
| `gold-light` | #e8d5a3 | Hover state for gold buttons |
| `muted` | #8a8fa8 | Secondary text |

Questions? Message Bryan.
