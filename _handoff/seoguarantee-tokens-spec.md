# C6 — BRAND CARD (RECORD ONLY) — seoguarantee

**Slug:** `seoguarantee` · **Authored:** 2026-08-12 · **Handoff member:** C6 of 12
**Closes:** P7 readiness blocker 1 (one of the four missing handoff members)
**Encoding:** UTF-8, no BOM

---

## WHAT THIS FILE IS, AND WHAT IT IS NOT

**This is a RECORD of the brand as it EXISTS TODAY.** Every value below was measured from the client's own live site or supplied by the owner at intake. Nothing here was chosen, derived, harmonised or improved.

**This file DESIGNS NOTHING.** Prep has zero design governance (PF4, 2026-06-23). There is deliberately no token system here: no roles, no light/dark surface system, no derived tints, no radius scale, no shadow scale, no spacing rhythm, no type scale. Those are the BUILD's P8 job — P8 overhauls, upgrades or creates the brand card and designs the token system from these recorded rails.

If you are reading this looking for the palette roles or the type scale, you are in the wrong file and the thing you want does not exist yet.

**Companion file:** `visual-direction.md` (C7) carries the design INPUTS — the measured brand signature, the owner's tonal direction, the captured references and the asset-supply window. Also inputs only.

---

## §1 — Logo assets (as they exist on disk)

Every logo below was recovered by the P0.0 scrape of the live site on 2026-08-11. The owner supplied no logo files directly.

| id | file | measured dims | bytes | status |
|---|---|---|---|---|
| LOGO-PRIMARY | `assets/seoguarantee.com_wp-content_themes_theme-child_images_seog-logo.png` | 403 x 85 | 2,957 | PRESENT-MARGINAL |
| LOGO-SHORT | `assets/…images_seog-short-logo.png` | 103 x 103 | 2,150 | PRESENT-MARGINAL |
| LOGO-1STPAGE | `assets/…images_1stpagelogo.png` | 400 x 200 | 4,632 | PRESENT-MARGINAL |
| LOGO-WHITE | `assets/…images_seoguarantee-logo-w.png` | 250 x 122 | 3,099 | PRESENT-MARGINAL |
| LOGO-OG | `assets/…storage.googleapis.com_uploads_2021_03_Logo-copy-2.png` | (the `og:image` logo) | — | PRESENT |
| LOGO-VECTOR | none | — | — | **NEEDS-OWNER** |

**Recorded observations, not judgements about what to do:**

- **No vector source exists anywhere.** No `.ai`, `.svg` or `.eps` appears in any scraped or supplied source. This is recorded at `D-BRAND-RAILS-001` and as an OPEN asset row in `decisions-ledger.md`.
- **The largest raster is 403px wide.** At that size the mark cannot render crisply in a retina header. Every logo file is placeholder-grade.
- **Consequence already recorded elsewhere:** the missing vector blocks hero Concept B entirely (`D-007` re-open condition 3). If a vector lands in `_inbox/`, Concept B returns as a candidate.

---

## §2 — Colour, as measured

These are the brand's EXISTING colours. They are recorded as a flat list of measured hexes with the observation that produced each one. No role is assigned to any of them here.

| hex | what it is, as observed | evidence |
|---|---|---|
| `#7f2199` | Purple. The dominant authored brand colour. | 10 occurrences across `index.html`, `services-suite.html`, `industries-dental.html`. Also the live booking plugin's configured `primaryColor` and both gradient stops' origin. |
| `#ffba00` | Gold. | Recorded at `D-BRAND-RAILS-002`. Present as a full-bleed band on the live home page measured at `rgb(229,156,2)` (501px tall). |
| `#a13cbc` | Secondary purple. | `D-BRAND-RAILS-002`. The live booking plugin uses it as the second gradient stop against `#7f2199`. |
| `#ffffff` | White. The ground. | The live `body` background computes to `rgb(255,255,255)`. |

**Owner statement on the palette** `[OWNER — rank 2]`, verbatim from `_inbox/seoguarantee-intake.md` line 90:

> "I want this redesign to have a majority white clean feel with the purple and gold accents from the current live site. I am aiming for a clean, modern, hip look"

**Further measured values from the live site**, recorded because they are real and load-bearing for the build's understanding of the existing brand, NOT because they are being proposed:

- Header background `rgb(53,1,81)` — a darker purple than any of the four rails above.
- The `section-james`, sub-footer and footer bands all compute to `rgb(75,6,112)`, occupying 660px, 527px and 602px of page height respectively.
- Roughly 3,530px of full-bleed sections carry a dark background IMAGE (for example `wedo-section-bg.jpg`) rather than a background colour.
- Large light bands exist below the fold: a 611px white magazine strip, a 964px band at `rgb(227,227,227)`, a 2,056px band at `rgb(242,242,242)`.

**Correction on the record.** An earlier intake pass reported "no authored brand palette exists; the only plausible candidates are `#0caa41` green and `#ffba00` amber", and recorded that in `intake-manifest.json`. That finding was WRONG and is withdrawn — see `intake-brief.md` §G-7, closed by the owner's own answer. The green was a WordPress block-editor default, not a brand colour. The four hexes in the table above supersede it.

---

## §3 — Type, as it exists

**Owner rail** `[OWNER — rank 2]`, verbatim (`_inbox/seoguarantee-intake.md` line 92):

> "try to use sans serrif family font"

Recorded at `D-BRAND-RAILS-003` as: **sans-serif family**.

**Families currently loaded on the live site** (observation only):

| family | role on the LIVE site | classification |
|---|---|---|
| Montserrat | display | sans-serif |
| Roboto | body | sans-serif |
| Roboto Slab | accent | slab serif |
| Lato | loaded by the booking plugin | sans-serif |

**The one live rail that cuts against the owner's instruction:** Roboto Slab is a slab serif, so the owner's "sans-serif family" instruction excludes it.

**Final family selection is the BUILD's P8 job.** `D-BRAND-RAILS-003` states this explicitly. Nothing above is a selection, and no sizes, weights, line-heights or scale steps are recorded anywhere in this file, by design.

---

## §4 — Voice, as ruled

Recorded from `content-bible.md` §1 and the `D-BRAND-RAILS-*` registry. These are RULES the owner set, not a tone this file invented.

- **Plainspoken and specific, not loud.** The offer is a billing term. Terms are stated, not shouted.
- **Zero exclamation marks. Zero emoji.** `[OWNER — rank 2]`, verbatim: *"remove all exclamation points and emojis"*. This supersedes the earlier agent-derived "one per page" allowance — the owner said ALL. The live site is saturated with both; none survive. (`D-BRAND-RAILS-006`, `D-BRAND-RAILS-007`.)
- **Founder-direct, and quirky is permitted.** The owner asked to keep James Sutton's imagery to "maintain the quirky brand tone". Warmth and personality live in the VOICE and the PHOTOGRAPHY, never in punctuation or capitals. (`D-FOUNDER-PRESENCE`.)
- **Contractual over promotional.** Describe the guarantee in the language of terms: what is agreed, over what period, and what happens to the invoice if it is not delivered.
- **Numbers always carry their frame.** A percentage without a time period, a baseline and a named source is not usable copy. Hard rule.
- **Say the condition and the promise together.** "First page for the phrases that matter" may only appear alongside "or you don't pay". The promise never travels alone.

**Voice register on file:** `hybrid` (`D-BRAND-RAILS-004`, agent-derived). The justification recorded at `D-BRAND-RAILS-005`: the live register is high-energy direct-response — heavy caps, exclamation marks, founder-first, low formality — and that register is *also* what the category's scam pitches sound like, which actively undermines the one thing this brand needs the reader to believe. Keep the founder-first directness and conviction, shed the shouting, let the contractual specifics carry the persuasion.

**Status flag:** the owner has not confirmed the `hybrid` register against a rendered specimen. Intake field `d4` remains open.

---

## §5 — Naming, tagline and canonical phrases

- **Brand name / wordmark:** First Page SEO Guarantee
- **Domain:** `seoguarantee.com`
- **Category line** `[OWNER — rank 2, LOCKED verbatim]`:

  > "A marketing agency that guarantees you'll be in the first page of Google on key phrases that matter or you don't pay"

  Given by the owner at `_inbox/seoguarantee-intake.md` lines 19 and 21 — the identical sentence for BOTH "One sentence: what is it?" and "We are a ___". Recorded at `D-OFFER-003`.

- **Primary CTA label:** "CALL US" · **primary action:** "Book a consultation" `[OWNER — rank 2]` (`D-BRAND-RAILS-009`, `D-OFFER-006`). One primary action per page. The earlier agent-derived CTA set is withdrawn.

- **Phrases to MIRROR** (`D-BRAND-RAILS-018`, real and cited): "Everything Else Is Complementary" (home) · "guaranteeing results" (`/our-locations/las-vegas-seo/`) · "first page" (passim) · "Full Suite" (`/services/suite/`).

- **Phrases to AVOID** (`D-BRAND-RAILS-019`): "desireable" (a misspelling in the live copy at `/services/suite/`) · "WHY OUR MARKETING IS AMAZING?" (broken headline grammar, live across `/industries/*`). Both corrected in the new build.

- **Canonical terms** (`content-bible.md` §5): "first page" never "#1" · "key phrases" never "keywords" · "the guarantee" always singular and definite · "or you don't pay" is the owner's phrase and is preferred over any paraphrase · "Full Suite" capitalised · "complementary" never "complimentary".

---

## §6 — Founder identity on the record

`[OWNER — rank 2, ruled 2026-08-12]` — closes `§G-13`.

- **James Sutton IV**, **FOUNDER**. The live site also titles him "Managing Partner"; **both hold** — the owner outranks the live site, and the two titles are not in conflict.
- **Company started 2015** — 11 years in business as of 2026. Stated plainly. Positioning §4 rules DO-NOT-COMPETE on longevity against `D-MARKET-001` ("since 2005").
- Captured as `D-FOUNDER-JAMES-SUTTON`, `D-FOUNDER-FOUNDED` and `D-FOUNDER-PRESENCE` in `intake-brief.md` §H.
- The founder is the brand's primary human asset — he appears in the hero video, the team block and the magazine imagery across the live site.

**Still thin, and flagged rather than invented:** why the guarantee model exists (the origin of the entire differentiator, and the single highest-value sentence missing from the spec), the founder's background before 2015, and team size. The `about` brief carries owner-placeholder markers for these rather than authoring a plausible-sounding history about a real, named person.

---

## §7 — Canonical NAP

`[OWNER — rank 2, ruled 2026-08-12]` — closes `§G-8`. Rendered byte-identically everywhere it appears: the footer on all 26 pages, `contact-us`, `about`, and the LocalBusiness structured data.

- **6905 W Charleston Blvd, Las Vegas, NV 89117, USA**
- **+1 (702) 420-7272**
- **support@seoguarantee.com**

Open follow-ups recorded in `decisions-ledger.md`: whether the directories' "#110" suite number belongs in the NAP is an unresolved owner decision, and — outside the build — the live map embed and the Yelp listing still show a different street and must be corrected at source.

---

## §8 — What this file deliberately does NOT contain

Listed explicitly so a later reader does not mistake absence for oversight. Every item below is the BUILD's P8 responsibility:

- Colour ROLES (which hex is background, ink, accent, muted, border) — §2 records hexes only, with no role assigned.
- A light/dark surface system, or any dark-surface flip.
- Derived tints, shades, or any colour ramp.
- A type scale, size steps, weights, line-heights or measure.
- A spacing rhythm or base unit.
- Corner-rounding values or an elevation scale.
- Any CSS at all, in any form.
- Motion timings or easing.

Prep records the brand. The build designs the system. That separation is the point of this file.

---

## Sign-off

**Authored by:** client-site-prep P7 remediation pass · **Date:** 2026-08-12
**Source rank of every value above:** owner rank 2 where marked `[OWNER]`; otherwise rank 3 (the client's own live site, snapshot-locked, measured 2026-08-11) — authoritative for what the brand currently *is*, per `content-bible.md` §4.
**Owner-confirmed:** the palette, type rail, punctuation policy, CTA, founder facts and NAP are owner-answered. The `hybrid` voice register is not yet confirmed against a rendered specimen.
