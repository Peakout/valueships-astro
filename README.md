# Valueships - State of Pricing 2026

Interactive diagnostic tool for Valueships. Users answer 6 questions and receive their pricing archetype, MRR leakage estimate, and priority moves. Email gate before results feeds Brevo via Make.com webhook.

**Live:** [peakout.com/state-of-pricing](https://peakout.com/state-of-pricing) (staging)
**Target:** valueships.com/state-of-pricing

## Stack

- [Astro](https://astro.build) v5 - static site generator
- Hosted via [Webflow Cloud](https://webflow.com/cloud) connected to this repo
- Email capture - Make.com webhook - Brevo list

## Local development

```bash
npm install
npm run dev
# http://localhost:4321/state-of-pricing/
```

To test on mobile (same WiFi network):

```bash
npm run dev -- --host
# http://<your-mac-ip>:4321/state-of-pricing/
```

## Deploy

Push to `main` - Webflow Cloud deploys automatically (~2 min).

## Key files

| File | What |
|------|------|
| `src/pages/index.astro` | Everything - HTML, CSS, JS in one file |
| `public/favicon.png` | Valueships favicon |
| `public/krzysztof.jpeg` | Photo for consultation CTA |
| `public/colors_and_type.css` | Valueships design tokens |
| `astro.config.mjs` | Base path `/state-of-pricing` |

## Before going live on valueships.com

- [ ] Remove `noindex` meta tag (`src/pages/index.astro` line 11)
- [ ] Add OG image to `public/` and update meta tags
- [ ] Swap Make.com webhook URL to Valueships account
- [ ] Swap Brevo list to Valueships account
- [ ] Add canonical URL meta tag
- [ ] Connect this repo to Valueships Webflow Cloud

## Contacts

- **Ola Romańczyk** - Head of Growth, Valueships (asset owner)
- **Brian** - Backpack AI (account lead)
- **Leszek** - Backpack AI (tech lead)
