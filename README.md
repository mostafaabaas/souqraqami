# Souq Raqami — souqraqami.com (static launch site, v1)

The digital e-market («ماركت ديجتال الكتروني») of **influUGC** — a marketplace for
digital products and services. Concept set by the owner Nov 5, 2026. This v1 is
the **launch / content site** for the market; the full marketplace build
(catalogue, seller storefronts, checkout) is a later phase. Built Nov 6, 2026.
**Files only — not deployed.**

## Design direction (network rule, owner Nov 5, 2026 — 23:57)

All network satellite sites use the **main influUGC identity**:

- Black background `#000`, neon lime accent `#C8FF00`, dark panels, bold heavy
  typography — the www.influugc.com feel. Stylesheet is the shared network base
  (same as prinfluencer) extended with `.guide` styles for the long-form guides.
- Brand lockup: `Souq Raqami.` wordmark with the subline "The digital e-market
  of influUGC" (Arabic: «الماركت الرقمي الإلكتروني من influUGC»).
- Only real company data: est. 2020, Arab League St Agouza (Giza 12651),
  Egypt + Saudi/Gulf, real client names (Riyadh Season, Saudi Tourism Authority,
  flynas, Saudia, realme, Domino's, TikTok Live, Zanussi). No prices, no invented
  figures or statistics, no testimonials, no stock imagery (CSS/text only).

## Content model (owner order, Nov 6, 2026 — 00:24)

Network sites lead with useful **content** — tips/guides/information that search
engines and AI answers surface — with influUGC's services and real work woven
in, not pure company brochures. On this site that is the **«أدلة السوق الرقمي»**
guides section: three substantive, answer-first on-page guides (what a digital
product is and how to sell it · how to price a digital product · how buyers stay
safe in digital marketplaces), written with no invented statistics.

## Pages built (3 HTML pages, 2 languages)

| File | What |
|---|---|
| `index.html` | Arabic-first launch page (RTL): hero (what the digital market is; launching soon), client proof strip, 4 category previews (digital products, creative services, content & media services, templates & assets), 3 full content guides, early-seller («للبائعين») section with 4-step joining process, waitlist CTA band, why influUGC (with the in-body editorial link to influugc.com), 6-question answer-first FAQ, network footer. |
| `en.html` | Full English mirror (LTR), same structure, guides and FAQ. |
| `404.html` | Branded not-found page (Arabic). |

Plus: `styles.css`, `favicon.svg` (black + lime SR mark), `sitemap.xml`
(hreflang-annotated), `robots.txt`, `llms.txt`, `render.yaml` (static-site
blueprint, same pattern as the sibling satellites).

## SEO / GEO

- Canonical base `https://souqraqami.com/` (the real domain — if this site is
  first deployed to an `onrender.com` URL before the domain attaches, switch all
  canonical/OG/sitemap/robots/llms bases in one pass, same as the ugccompany
  rule in `../DEPLOY.md` §2).
- Title/meta target "digital market / ماركت رقمي" + digital products & services
  + Egypt / Saudi Arabia in both languages; OpenGraph + Twitter cards;
  hreflang ar/en both ways.
- JSON-LD: `Organization` (with `parentOrganization: influUGC`, postal address,
  areaServed, the four real social profiles), `WebSite` (Arabic page), and
  `FAQPage` matching each page's visible FAQ.

## CTAs (all carry the satellite UTM set)

- Booking / waitlist → `https://www.influugc.com/book?utm_source=souqraqami&utm_medium=satellite&utm_campaign=network`
- WhatsApp (client line) → `https://wa.me/201029979797?utm_source=souqraqami&utm_medium=satellite&utm_campaign=network`
- Footer legal line: "Part of the influUGC network" linking to the hub.
- No local forms or alternate contact routes anywhere on the site.

## What remains (not done here)

1. **Deploy** — static folder; any static host or a Render Static Site (free
   tier per the network rule; `render.yaml` blueprint included). No
   server/admin in this v1: the brief scoped a static launch site.
2. **Domain attach** — point `souqraqami.com` DNS at the host (same checklist
   pattern as `../DEPLOY.md` §4: apex A + www CNAME from the host's screen; no
   MX changes — mail stays on influugc.com).
3. **Full marketplace build (later phase)** — product catalogue, seller
   storefronts, checkout/payments, licence delivery and reviews are NOT part of
   v1; the launch site collects waitlist and founding-seller interest centrally
   (booking + WhatsApp) until that phase is built.
4. After go-live: dedicated Google Search Console property + submit
   `sitemap.xml`; verify both pages return 200 and the FAQ renders; grow the
   guides section into standalone guide pages if search data supports it.

## Deploy status (Nov 6, 2026)

- **Repo**: https://github.com/mostafaabaas/souqraqami (private, branch `main`) — source pushed Nov 6, 2026.
- **Hosting**: PENDING-DASHBOARD — the Render Static Site service has **not** been created yet.
  Creating it requires the Render dashboard (no Render API key is available to the
  automation): Render Dashboard → New → Static Site → connect this repo — the repo's
  `render.yaml` blueprint pre-fills the service name (`souqraqami`) and publish path (`.`).
  Expected live URL once created: https://souqraqami.onrender.com
- **Domain attach**: separate later batch (see "What remains" item 2 above).
