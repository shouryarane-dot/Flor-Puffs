# FLŌR — website

Static site. No build step, no dependencies. Double-click `index.html` to preview it locally.

## What's in this folder

```
florpuffs-website/
├── index.html      the entire site — all text, layout and styling
├── images/         logo, three pack shots, harvest illustration, lotus line art
└── README.md       this file (notes only — not part of the site)
```

**Both `index.html` and the `images` folder must go to GitHub.** The site loses every picture without `images/`.

## Uploading an update to GitHub

1. Open your repo on github.com
2. **Add file → Upload files**
3. Open the `florpuffs-website` folder, select `index.html` **and** the `images` folder, drag both in together
4. Scroll down → green **Commit changes**

Don't drag the `florpuffs-website` folder itself — go inside it first. Vercel redeploys on its own within ~30 seconds.

## Sections

Hero → What is FLŌR → The Puffs → Shop → Sustainability → About → Footer

Navigation: sticky top bar on desktop with the current section underlined in terracotta; hamburger menu on mobile; back-to-top button appears after scrolling.

## Editing text

Everything is in `index.html`. Open it in Notepad, use Ctrl+F to find the sentence you want, change it, save, re-upload. The text sits between the `<!-- ============ SECTION ============ -->` comment markers.

## Colours (sampled from the pack artwork)

| | Hex |
|---|---|
| Brand brown (logo ink) | `#522F19` |
| Page cream | `#FAF6EC` |
| Band cream | `#EFE7D7` |
| Classic Salt navy | `#1F4368` |
| Peri Peri terracotta | `#B94A36` |
| Cocoa burgundy | `#6B2938` |

## Still to do

- [ ] **Confirm the fibre claims.** The packs say "Source of fibre" on all three. The site's table also claims "High in fibre" for Classic Salt and Peri Peri. Both are regulated under EU 1169/2011 — verify against final nutritionals before publishing.
- [ ] **Confirm `hello@florpuffs.com` receives mail.** It appears three times on the site.
- [ ] **Privacy policy** — needed once you collect any personal data.
- [ ] Add an `og-image.jpg` (1200×630) for nicer link previews when shared.
- [ ] Connect the domain: Vercel → Project → Settings → Domains → add `florpuffs.com`, then copy the DNS records it shows into your registrar.

## A note on the sustainability copy

The section is written as ambition — "we're exploring", "our ambition is", "we're honest about what we haven't figured out". That framing is what keeps it clear of EU green-claims rules. Keep it that way as the sourcing and packaging work progresses; switching to definite claims would need evidence behind each one.

## Moving to Shopify later

Copy, colours and images all carry over. You'd rebuild the layout as Liquid sections and move DNS from Vercel to Shopify. Nothing here is wasted.
