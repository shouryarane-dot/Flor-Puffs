# FLŌR. Website

Static site. No build step, no dependencies. Double-click `index.html` to preview it locally.

## What's in this folder

```
florpuffs-website/
├── index.html                the entire site: all text, layout and styling
├── images/                   logo, 28 g pack shots (Classic Salt, Peri Peri), coming-soon packs (Cocoa, Amaranth Bites), founders portrait
├── ART-DIRECTION-BRIEF.md    photography brief for the next stage
└── README.md                 this file (notes only, not part of the site)
```

**Both `index.html` and the `images` folder must go to GitHub.** The site loses every picture without `images/`.

## Uploading an update to GitHub

1. Open your repo on github.com
2. **Add file → Upload files**
3. Open the `florpuffs-website` folder, select `index.html` and, if any picture changed, the `images` folder
4. Scroll down → green **Commit changes**

Don't drag the `florpuffs-website` folder itself; go inside it first. Vercel redeploys on its own within about 30 seconds.

GitHub keeps every previous version, so if a change goes wrong you can open the repo, click `index.html`, then **History**, and restore an earlier one.

## Design system

Every colour is sampled from the pack artwork or the logo. Don't introduce others.

| | Hex | Where it comes from |
|---|---|---|
| Chocolate (primary type) | `#522F19` | logo ink |
| Body copy | `#5E4634` | softened chocolate |
| Muted type | `#8A7663` | softened chocolate |
| Ivory (main background) | `#F7F2E8` | pack cream, lightened |
| Pack cream (section 2) | `#EFE7D8` | pouch face |
| Mist (section tone) | `#E3E4E1` | blue softened into ivory |
| Blue (accent) | `#1F4368` | Classic Salt tab |
| Deep blue (panels) | `#16324C` | Classic Salt band |

**Blue is structural, not decorative.** It appears as the hero block, the full-width Shop panel, the hairline under each flavour name, the rule beneath the table headers, and the nav hover underline. Small text stays chocolate.

**Type:** Cormorant Garamond for headlines (up to 104px), DM Sans for navigation, labels and body copy at 17px. The gap between those sizes is deliberate; avoid filling it with mid-sized text.

**The wordmark** is wrapped in `<span class="flor">FLŌR</span>` wherever it appears in running text. That sets it in Cormorant, which renders the Ō correctly. DM Sans does not. Keep the span when editing text.

## Layout notes

- `--blue-w` controls both the hero block's width and where the nav links begin, so they always share one vertical line. Change it in one place.
- `--nav-h` keeps the blue block below the nav row, so navigation always sits on ivory.
- The hero pouch sits inside the blue block and is centred by flex, capped at 76% of the block's height. Don't switch it back to viewport units.

## Editing text

Everything is in `index.html`. Open it in Notepad, Ctrl+F for the sentence, change it, save, re-upload. No em dashes anywhere; use a full stop or a comma.

## Still to do

- [ ] **Confirm the fibre claim.** The site and packs say "a source of fibre" (needs at least 3 g per 100 g under EU 1924/2006). "High in fibre" has been removed.
- [ ] **Vegan / vegetarian / gluten-free.** Removed from the table until confirmed against final product specs. Add rows back to the table in `index.html` once confirmed.
- [ ] **Shop buttons** open a pre-filled order email. Swap the two `mailto:` links for real product page URLs once a shop exists.
- [ ] **Confirm `hello@florpuffs.com` receives mail.** It is the only call to action on the site.
- [ ] **Privacy policy** — needed once you collect any personal data.
- [ ] **Product photography** — see `ART-DIRECTION-BRIEF.md`. The single biggest upgrade available to this page.
- [ ] Connect the domain: Vercel → Project → Settings → Domains → add `florpuffs.com`, then copy the DNS records it shows into your registrar.

## Structure (Nov 2026 brief)

Five sections, in this order: What is FLŌR, The Puffs (product, flavours, table), Shop, About Us, Coming Soon. No sustainability section; avoid sustainability claims (EU green-claims rules).

## Moving to Shopify later

Copy, colours and images all carry over. You would rebuild the layout as Liquid sections and move DNS from Vercel to Shopify. For a Dutch store the stack is Shopify → Mollie (iDEAL) → Sendcloud → PostNL.
