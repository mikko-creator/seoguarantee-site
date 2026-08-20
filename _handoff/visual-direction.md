# C7 — VISUAL DIRECTION (design INPUTS) — seoguarantee

**Slug:** `seoguarantee` · **Authored:** 2026-08-12 · **Handoff member:** C7 of 12 — **MANDATORY**
**Closes:** P7 readiness blocker 1. The PREP to BUILD seam fails closed without this file: `emit-handoff-receipt.mjs` errors cleanly when it is absent, because a real client build with no bound visual direction must FAIL rather than silently invent the look.
**Encoding:** UTF-8, no BOM.

---

## READ THIS FIRST — THIS FILE IS INPUTS, NOT A LOCKED DESIGN

Prep designs nothing (PF4). This file carries the design **INPUTS the build designs FROM**: the measured brand signature, the owner's stated tonal direction, the captured references, the hard per-vertical constraints, and the asset-supply window.

It carries **no token system** — no colour roles, no light/dark surface system, no derived tints, no corner or elevation scale, no spacing rhythm, no type scale. All of that is the build's P8 job. The companion brand card `seoguarantee-tokens-spec.md` (C6) is likewise a record, not a design.

**And one thing here is explicitly NOT settled: the hero.** See §1.

---

## §0 — BRAND VISUAL IDENTITY (the TONE SOURCE)

The tone below comes from the owner's OWN existing site, area-weighted from a rendered capture — not from competitors and not from the vertical's generic mood. It ranks ABOVE the vertical blueprint on tone.

- **`surface_dominance`: `balanced`** — neither canvas clears roughly 60% of page area.
- **`dark_ratio`: `0.25`**
- **`energy`: `bold`** — big type, high-contrast bands, saturated accents, confident founder imagery.
- **Signature moves to MODERNIZE and KEEP:** `dark-hero` · `big-stat-bands` · `dark-purple-chrome` · `gold-cta-band` · `founder-video-hero`. The build modernizes their EXECUTION; it does not delete the move.
- **Existing-site render READ:** `_spec/visual-refs/current-home-desktop.png`

**How `balanced` was arrived at, and why it is not `light` and not `dark`.** The extractor's raw verdict was `light`; that was CORRECTED on 2026-08-11 and the correction is load-bearing. The extractor area-weights background COLOUR only, and seoguarantee.com delivers much of its darkness through background IMAGES, which score as transparent. Verified live against computed styles: the `body` background is `rgb(255,255,255)` and there ARE large light bands below the fold — a 611px white magazine strip, a 964px band at `rgb(227,227,227)`, a 2,056px band at `rgb(242,242,242)` — so `dark` would also be wrong. But the dark purple is structural and unmistakable: header `rgb(53,1,81)`, `section-james` `rgb(75,6,112)` over 660px, sub-footer `rgb(75,6,112)` over 527px, footer `rgb(75,6,112)` over 602px, plus roughly 3,530px of full-bleed sections whose background is a dark IMAGE and therefore uncounted, plus a 501px gold band at `rgb(229,156,2)`.

Of roughly 9,601px of measurable non-wrapper section height: **20.2% explicitly dark, 37.8% explicitly light, 5.2% gold, 36.8% image-backed and unmeasured.** `balanced` is the honest reading.

**Why this matters downstream:** a `balanced` brand NEVER inverts, so the owner's white-dominant direction is legitimate with NO tone-pivot ratification required — while `signature_moves` still tells the build that dark purple chrome and a dark hero are brand signature and must not be discarded wholesale.

**MACHINE BLOCK** — real values, copied from `brand-visual-signature.json`. Consumed by the tone gate `verify-visual-direction-grounded.mjs`, which parses `surface_dominance` from here and compares it to §2's `primary_surface` line.

<!-- BRAND-SIGNATURE {"surface_dominance": "balanced", "dark_ratio": 0.25, "energy": "bold", "signature_moves": ["dark-hero", "big-stat-bands", "dark-purple-chrome", "gold-cta-band", "founder-video-hero"], "existing_site": "_spec/visual-refs/current-home-desktop.png", "notes": "CORRECTED 2026-08-11 from the extractor's raw verdict of surface_dominance='light'. The extractor area-weights background-COLOR only; seoguarantee.com delivers much of its darkness through background IMAGES, which score as transparent. Verified live via computed styles: body background is rgb(255,255,255) and there ARE large light bands below the fold (611px white magazine strip, 964px rgb(227,227,227), 2056px rgb(242,242,242)) - so 'dark' would also be wrong. But the dark purple is structural and unmistakable: header rgb(53,1,81), section-james rgb(75,6,112) 660px, sub-footer rgb(75,6,112) 527px, footer rgb(75,6,112) 602px, plus ~3,530px of full-bleed sections whose background is a dark IMAGE (e.g. wedo-section-bg.jpg) and therefore uncounted, plus a 501px gold band rgb(229,156,2). Of ~9,601px of measurable non-wrapper section height: 20.2% explicitly dark, 37.8% explicitly light, 5.2% gold, 36.8% image-backed and unmeasured. 'balanced' is the honest reading. This matters downstream: the gate treats 'balanced' as never-inverting, so the owner's white-dominant direction is legitimate WITHOUT a tone-pivot marker, while the build is still told in signature_moves that dark purple chrome and a dark hero are brand signature and must not be discarded wholesale."} -->

**Owner's tonal direction, verbatim** `[OWNER — rank 2]` (`_inbox/seoguarantee-intake.md` line 90):

> "I want this redesign to have a **majority white clean feel with the purple and gold accents** from the current live site. I am aiming for a **clean, modern, hip** look"

**Owner's second tonal instruction** `[OWNER — rank 2]` (`_inbox/` line 143): capture and keep **James Sutton's imagery** in order to *"maintain the quirky brand tone"*. The quirk is a stated brand asset. It lives in the photography and the voice — never in punctuation, capitals or emoji, all of which the same owner banned outright.

**What to LEAVE BEHIND** — the dated EXECUTION, never the brand's energy: shouting capitals and exclamation marks (owner-banned), the saturated direct-response density, the thin unlinked press wall, and the bare percentage tiles. Losing those is a gain in credibility, and credibility is the product here.

---

## §1 — Hero — PROVISIONAL, EXPLICITLY NOT LOCKED  *(heading SUPERSEDED 2026-08-13 — the hero is now RATIFIED. The heading is kept verbatim as the record of this section's status from 2026-08-11 to 2026-08-13; read the note directly below it first.)*

**⚑ RATIFICATION NOTE — 2026-08-13.** The owner has now seen Concept A animated at final render quality (`_spec/visual-refs/hero-concept-A-climb-1080.mp4`, verified present on disk 2026-08-13) and ruled, verbatim: *"ratify the hero, lock it in"*. **Concept A, "The Climb", is the ratified hero.** The condition `D-007` reserved — seeing the concept animated before finalising — was satisfied BEFORE §6's `direction_locked` was moved to `true`, so that flag records a ratification that happened rather than asserting one that did not. The ratification is recorded as `D-011` in `decisions-ledger.md`, and `D-011` is the authority on its scope.

**What the ratification does not change.** `D-008` still governs HOW the hero ships and is untouched: short seamless loop plus poster frame, never the LCP element, lazy-loaded after LCP, reduced motion receives the still, lighter or no variant on mobile, hard byte budget. Concept B remains blocked on the logo vector, which is still owed. Nothing here waives an asset — §6's `waived` stays `false` and `real_image_count` stays 15 — and nothing here opens the seam: `ready_for_build` stays `false` while readiness blocker 15 is open.

**Everything below this note is preserved verbatim as the record of what was reserved and why.** It is history now rather than an open decision, and that includes the binding "no phase may treat Concept A as final" instruction, which described the pre-ratification state.

**This section is the one place where C7 deliberately does NOT hand the build a settled answer.** `D-007` is recorded in `decisions-ledger.md` as `PROVISIONAL — EXPLICITLY NOT LOCKED`, and nothing in this file may upgrade it.

**Current standing selection: Concept A, "The Climb"** — a search-result card rising into position one, displacing the greys, with a gold rank chip and underline. Rendered still: `_spec/visual-refs/hero-concept-A-climb.png`.

**Owner, verbatim:**

> "okay let's go with option A for now but do not lock it as I might want to update it as we go along, I want to see how this will be displayed in the hero section with actual animation before I finalize. For now let's proceed"

**The three explicit re-open conditions, carried forward intact:**

1. The owner has seen **stills only**. Final selection requires seeing it **animated, in a hero layout**, at the build's FEEL gate.
2. Concept **C, "The Meter"** remains live as a hero alternative and as the recurring site-wide motif. It is strategically the sharper idea — it dramatises the payment mechanic, which no competitor can show — and was set aside only because its blockout render was the roughest. Still: `_spec/visual-refs/hero-concept-C-meter.png`.
3. Concept **B, "The 1st Mark"** is **blocked, not rejected.** It requires the logo vector (`.ai` / `.svg` / `.eps`), which exists in no supplied or scraped source. If one lands in `_inbox/`, B returns as a candidate. Still: `_spec/visual-refs/hero-concept-B-mark.png`.

**Binding instruction to the build:** no phase may treat Concept A as final. The hero slot must be described and built in terms that **survive a concept swap** — the surrounding layout, type posture and CTA placement must not be load-bearing on which of the three animations occupies the slot.

**The one hero rule that IS locked** — `D-008`, an engineering constraint rather than a preference: whichever concept wins ships as a **short seamless loop plus a poster frame**, never a video file dropped into the hero. The poster paints first so the animation can NEVER be the LCP element; the loop lazy-loads after LCP; reduced-motion receives the still; mobile gets a lighter variant or none; a hard byte budget applies. The rationale is not generic performance hygiene: the client sells SEO, prospects run PageSpeed on the vendor's own site as basic due diligence, and `D-MARKET-002` actively teaches buyers to do so. A hero animation that damages Core Web Vitals would turn the homepage into an argument against the offer.

**Hero energy constraint (from §0):** the brand's energy is `bold`. Whatever concept wins must read at that energy — a confident, dramatic hero with large type. It must NOT be quieted into a timid image-and-copy split. Equally, per the owner's direction, it sits on the light canvas declared in §2 rather than reproducing the live site's dark hero wholesale.

---

## §2 — Surface and palette INPUTS

**PRIMARY SURFACE — the canvas that dominates the page.** This is the literal line the tone gate reads:

primary_surface: light

**Why `light` is legitimate against a `balanced` brand, with no ratification marker.** §0 measures `surface_dominance: balanced`, and a balanced brand never inverts — only a truly dark-dominant brand handed a light direction (or the reverse) is the regression the tone gate exists to catch. A balanced brand may legitimately lead with either canvas. The owner chose light explicitly and in his own words ("majority white clean feel"), and that choice is recorded as `D-006` in `decisions-ledger.md`. **No `TONE-PIVOT-RATIFIED` marker is required and none is present** — adding one would misrepresent a legitimate choice as a pivot away from the brand.

**Existing brand colours, as measured** (recorded in full in C6; repeated here as an input, with NO role assigned to any of them):

| hex | as observed |
|---|---|
| `#7f2199` | purple — the dominant authored brand colour |
| `#ffba00` | gold |
| `#a13cbc` | secondary purple |
| `#ffffff` | white — the ground |

Further measured live values, recorded because the build needs to know they exist: header `rgb(53,1,81)`; the `section-james`, sub-footer and footer bands all at `rgb(75,6,112)`; a full-bleed gold band at `rgb(229,156,2)`.

**Direction the build designs FROM (inputs, not a specification):**

- White is the ground. Purple and gold are **accents**, per the owner's own sentence.
- The dark purple chrome and at least one dark full-bleed moment are **brand signature** (§0 `signature_moves`) and must survive in modernized execution. A build that strips the purple wholesale to achieve "clean" has lost the brand.
- Gold is the brand's punctuation colour. On the live site it carries the CTA band. That association is worth keeping.
- The four hexes above are the EXISTING brand values, not a designed palette. P8 assigns roles, derives any tints it needs, and checks contrast.

**Hard constraints on the dark sections (accessibility, not taste).** These are recorded because the trap is recurring, and they are constraints rather than design:

- Any dark panel placed inside a section that is not itself a dark section must re-assert its own text colour explicitly rather than inherit it. Dark text on a dark panel is the failure mode.
- Any light card dropped into a dark section must carry an explicit light surface value. White-on-white is the mirror failure.
- Neither accent colour may be used as body text on either canvas. The floors are WCAG AA: 4.5:1 for body, 3:1 for large text. The build's render-verify contrast audit enforces this.

**Gradients and overlays:** permitted but rationed. The live booking plugin already runs a `#7f2199` to `#a13cbc` gradient, so a gradient is in-brand. What is forbidden is the 12%-opacity stock wash over a photograph — the flat-cheap trap.

---

## §3 — Corner, spacing and elevation — DELIBERATELY ABSENT

The template slot that once held signature radius, spacing and shadow tokens carries **nothing** here, and the absence is the point.

Prep records the brand; it does not design the system. Corner rounding, spacing rhythm, elevation and the type scale are all designed at the build's P8 from the inputs above. Recording them here would be prep designing, which the `verify-prep-no-design` gate blocks and which PF4 forbids.

---

## §4 — Motion and image treatment INPUTS

**Energy match (mandatory).** §0 records `energy: bold`. Motion and imagery must read at that energy, not below it. A bold brand earns expressive, confident motion and dramatic, high-contrast imagery. Do not hand this brand timid fade-ins and washed-out stock.

**Motion budget:** expressive is permitted and appropriate, bounded by two hard rules:

1. **Reduced motion must be honoured.** Transitions zero out under a reduced-motion preference; the hero animation degrades to its still.
2. **`D-008` governs the hero specifically** — loop plus poster frame, never the LCP element, lazy-loaded after LCP, hard byte budget, lighter or no variant on mobile.

**Scroll-reveal:** permitted. If enabled, below-fold content starts transparent — note this for render-verify, because a static full-page capture will read empty unless the reveal is forced or the capture scrolls.

**Image treatment inputs:**

- **Founder photography is a stated brand asset**, not decoration. The owner asked for it explicitly to hold the quirky tone. It should be used at a scale that reads as deliberate.
- **Resolution reality (measured, not assumed):** every founder image on file is web resolution. The largest is 571 x 462. The file named `james-image-highres.jpg` is **543 x 614 despite its filename**. None of them can lead a full-bleed section or carry a hero. Compose for the resolution that exists, or the owner supplies real photography.
- **The one true hero-resolution image recovered** is `full-suite-image.jpg` at 1920 x 1216.
- **No stock wash.** No 12%-opacity photograph behind text as a substitute for a designed section.
- **The 8 client mockups at 1500 x 1000 are the strongest assets recovered** and are genuinely good. They are also **rights-blocked**: each depicts a named third-party client and §G-6 written permission is not on file. They may not ship until it is, however good they look.

---

## §5 — Per-vertical hard rules the build MUST obey

**Sector:** professional-services (marketing agency / lead-generation variant).

**The vertical supplies HARD CONSTRAINTS and a technique ceiling ONLY. It does not supply tone.** Tone comes from §0. Where they differ, the BRAND wins on tone and the VERTICAL wins on its hard rules.

**Hard rules (non-negotiable):**

- **No fabricated claims, and no unevidenced proof.** This is the governing constraint of the entire project, not a stylistic preference. The claim discipline lives in `client-rules.json` (C3) and `content-bible.md` (C4); visually it means: no invented percentage tiles, no fabricated rank charts, no logo wall without linked coverage, no client name without permission on file.
- **Real imagery only.** Where a real asset does not exist, the section is composed to work without it rather than filled with stock that implies something untrue.
- **Contrast floors:** WCAG AA — 4.5:1 body, 3:1 large text — on every surface.
- **Zero exclamation marks and zero emoji in rendered copy.** Owner-ruled, and it applies to any text baked into an image or animation just as it applies to prose.
- **No published price anywhere**, including "from" figures — `D-001`, quote-gated. This is a visual constraint too: no pricing table, no tier cards, no figure in a graphic.
- **The site must model the service it sells** (M§5.1). This client sells SEO; prospects will run PageSpeed and a crawl against this very site as due diligence. Core Web Vitals, crawlability and clean structured data are a positioning requirement here, not hygiene.

**Technique ceiling for this sector:** confident editorial layout, full-bleed brand bands, purposeful motion, crafted CSS diagrams that explain the mechanic. The mechanic itself is the most persuasive thing this brand owns, so technique should be spent explaining it rather than decorating around it.

**Forbidden patterns:** stock-photo hero with a translucent overlay band · generic centred hero with a gradient blob · unlinked logo walls · bare stat tiles with no frame · countdown or scarcity devices · anything that reads as a direct-response scam pitch, since that register is precisely what undermines the one thing this brand needs the reader to believe.

**Tone confirmation:** this build ships **light-canvas, bold-energy**, keeping dark purple chrome and a dark full-bleed moment as brand signature. That reading comes from §0 and the owner's own words, and it overrides any generic "agency sites feel like X" instinct.

---

## §6 — Asset-supply window

The build's P7.5 gate `verify-asset-intake.mjs` parses the machine block below.

**`real_image_count: 15` — how it was counted, and what was deliberately excluded.** The count is REAL, on-brand, rights-clear imagery the build can actually use today:

| counted | n | note |
|---|---|---|
| `full-suite-image.jpg` | 1 | 1920 x 1216, the only true hero-resolution image recovered |
| founder photography | 5 | 543 x 614, 504 x 722, 571 x 462, 537 x 465, 380 x 430 — all web resolution |
| team portraits | 9 | 350 x 400 each; adequate for a small grid, nothing larger |
| **total** | **15** | |

**Deliberately EXCLUDED from the count, with reasons:**

- **The 8 client mockups at 1500 x 1000 and the 3 client logos** — the strongest assets on disk, but they depict named third-party clients and §G-6 written permission is NOT on file. Rights-blocked assets are not "available to the build".
- **The 4 press logos** — marked DO NOT SHIP; third-party marks with no linked coverage and no usage rights.
- **The 5 logo rasters** — brand marks rather than imagery, and every one is placeholder-grade at a maximum 403px wide.
- **The theblez mockup** at 525 x 350 — both rights-blocked and far smaller than the other eight.

**`waived: false`.** The owner has NOT accepted a generated or AI fallback for imagery. No such waiver exists in `decisions-ledger.md`, and recording one that the owner never gave would be exactly the fabrication this project is built to prevent.

**`direction_locked: true` as of 2026-08-13 — RATIFIED BY THE OWNER, not assumed.** The owner viewed hero Concept A, "The Climb", animated at final render quality (`_spec/visual-refs/hero-concept-A-climb-1080.mp4`, verified present on disk 2026-08-13) and ruled, verbatim: *"ratify the hero, lock it in"*. That is precisely the event `D-007` reserved and `D-009` was holding for, and it happened **before** this flag moved. The flag therefore RECORDS a ratification that occurred; it does not manufacture one, and that distinction is the whole point of `D-009`. The ratification is recorded as `D-011` in `decisions-ledger.md`, dated and attributed.

**What this ratification does NOT do — stated because the temptation to over-read it is exactly the failure this file guards against.** `waived` is untouched and remains **`false`**, and `real_image_count` remains **15**. The asset-supply window described in this section is NOT waived by a hero ratification: the logo vector and real founder photography at print or retina resolution are still owed, exactly as `D-010` records ("this decision authorises a source, it does not waive the asset-supply window"). Changing either flag would be a separate owner decision that has not been made.

**Consequence now.** The specific check quoted in `D-009` — `verify-handoff-complete.mjs:98`, `const lockOk = j.direction_locked === true;` — passes on this flag from 2026-08-13, and the build's `verify-asset-intake.mjs` no longer blocks the first P8 design write on it. **That does not open the seam.** `ready_for_build` stays `false` and the verdict stays NO-GO while readiness blocker 15 (the counsel-supplied privacy policy, `readiness-verdict.md` §3 row 15) is open, no `HANDOFF-KICKOFF.json` may be written, and the seam copy must not run.

**[HISTORICAL — the two paragraphs below state the position as it stood from 2026-08-12 until the ratification above. They are preserved rather than corrected because they record why prep was right to REFUSE to flip this flag while the owner had seen stills only.]**

**`direction_locked: false` — and this is CORRECT, not an omission.** `D-007` is `PROVISIONAL — EXPLICITLY NOT LOCKED`: the owner has seen hero stills only and reserved the right to change concept after seeing it animated in a hero layout. §1 of this file cannot be described as final while that is true. Setting this flag to `true` today would assert an owner ratification that has not happened.

**Consequence, stated plainly:** with `direction_locked: false`, `verify-asset-intake.mjs` will BLOCK the first P8 design write, and PHASE A of `verify-handoff-complete.mjs` will fail this member. **That is the gate working, not a defect in this file.** It resolves when the owner sees Concept A (or C) animated in a hero layout at the FEEL gate and rules — an `[OWNER-DECISION]`, and one already on the readiness verdict's shopping list ("is the hero archetype lockable yet"). This file must not pre-empt it.

<!-- ASSET-INTAKE {"real_image_count": 15, "waived": false, "assets": ["assets/seoguarantee.com_wp-content_themes_theme-child_images_full-suite-image.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_james-image-highres.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_james-approved.png", "assets/seoguarantee.com_wp-content_themes_theme-child_images_james-undercut.png", "assets/seoguarantee.com_wp-content_themes_theme-child_images_james-fpsg-footer.png", "assets/seoguarantee.com_wp-content_themes_theme-child_images_james-mag.png", "assets/seoguarantee.com_wp-content_themes_theme-child_images_team_bryan.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_team_cherwin.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_team_danico.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_team_hazel.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_team_james.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_team_jeff.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_team_karen.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_team_miko.jpg", "assets/seoguarantee.com_wp-content_themes_theme-child_images_team_mj.jpg"], "direction_locked": true} -->

**Path note:** the paths above are relative to the prep slug root `Code/client-site-prep/seoguarantee/`, and every one was verified to exist on disk on 2026-08-12. They are source paths rather than build-tree paths because the build tree `Code/client-sites/seoguarantee/` has never been created. The seam re-points them when it runs.

**Still NEEDS-OWNER on the asset side:** the logo vector (blocks hero Concept B and forces a raster logo in the header) · real founder photography at print or retina resolution · §G-6 written permission for the 8 mockups and 3 client logos · press article URLs plus usage rights, or the wall is deleted.

---

## §7 — Captured references

**The brand's own site (the tone source, ranked above everything else here):**

- `_spec/visual-refs/current-home-desktop.png` — the rendered capture READ to produce §0.

**Hero concept renders (all three, because the decision is open):**

- `_spec/visual-refs/hero-concept-A-climb.png` — Concept A, the standing selection.
- `_spec/visual-refs/hero-concept-C-meter.png` — Concept C, live alternative and site-wide motif.
- `_spec/visual-refs/hero-concept-B-mark.png` — Concept B, blocked on the logo vector.
- `_spec/visual-refs/blender-pipeline-test.png` — the render-pipeline proof, not a design candidate.

**Competitor captures** (rank 4 — they inform technique and objection-handling, and are explicitly NOT a tone source):

- `_spec/market-intel/thriveagency.md` (`D-MARKET-001`) — pairs every metric with the campaign description that produced it. That proof pattern is worth learning from; the scale signals are not, since positioning rules DO-NOT-COMPETE on scale.
- `_spec/market-intel/webfx.md` (`D-MARKET-002` / `D-INCUMBENT-001`) — publishes the argument against ranking guarantees. It shapes what this site must answer, never how it should look.

**Where the visual direction must NOT come from:** the vertical's generic mood, or either competitor's look. §0 is the tone source. This is recorded because deriving tone from competitors plus a vertical blueprint is the exact failure this file's gate exists to prevent.

**One further reference, owner-chosen and structural rather than tonal:** see §8. It ranks BELOW §0 on tone (§0 remains the tone source) and it is captured for STRUCTURE, not for palette.

---

## §8 — OWNER-CHOSEN STRUCTURAL REFERENCE (captured 2026-08-13)

**Status: an INPUT, exactly like §0 and §7.** This section records a page the owner picked and what he picked it FOR. It is not a locked design, it authors no token system, and it does not touch §1 or `direction_locked`. §3 stands unamended: corner, spacing and elevation remain deliberately absent from this file, and nothing observed below populates them.

### 8.1 What was chosen, and what for

- **URL:** `https://carlcelinodspnza.github.io/previews/dispenza/_design/_tournament/foundation-1-measured-column/`
- **Captured:** 2026-08-13.
- **Durable local snapshot:** `_spec/visual-refs/reference-foundation-1/` — `index.html` plus the five stylesheets it loads (`dispenza-tokens.css`, `dispenza-chrome.css`, `dispenza-structural.css`, `dispenza-fonts.css`, `hero-section.css`). Copied into the spec deliberately: the reference is a third-party preview URL that can change or disappear, and a dangling link is not a captured reference. Every observation in §8 was read from these local files.
- **Owner's instruction, verbatim** `[OWNER — rank 2]`:

> use this as the reference for "the site structure, the look, the site architecture and the imagery. The only difference is that we are going to use the purple and gold from the live site as accents while maintaining a mostly white site, and then the imagery is a mixture of fal generated images and James Sutton."

So the owner is buying the reference's **architecture and rhythm**, and explicitly NOT its palette. Two things follow, and they are the whole point of this section: the surface inverts (8.2), and several of the reference's most prominent devices are claims this client may not make (8.4).

**A naming caution.** The folder is called `foundation-1-measured-column`, but its hero stylesheet records a later same-day revision to a pinned scroll stage; the previous measured-column hero is preserved elsewhere in the reference's own tree. The BODY is the measured column the name advertises. The HERO is a heavier later revision layered on top of it. Do not read the folder name as describing the hero.

### 8.2 THE SURFACE INVERSION — read this before anything else in §8

**The reference is a DARK site.** Its page canvas is `#15161a`, its default ink `#f5f3f9`, and its two other grounds are `#1b1d22` and `#222429` — three near-blacks about seven units apart. There is no light band anywhere in it: a search for a white or `#fff` background across all five stylesheets returns zero matches, and `index.html` carries no inline style block. Its own gradient token named for "paper" fades TO `#15161a`, so even the word "paper" means near-black there. **Any automated summary describing this reference as a mostly-white page is wrong, and that error has already been made once on this project.**

**This client inverts it.** Per §2, `primary_surface: light`, and the owner restated it in the instruction above ("maintaining a mostly white site"). This is consistent, not a new decision — §2's light canvas was already recorded from the owner's earlier "majority white clean feel" line, and §0's `surface_dominance: balanced` means no tone-pivot ratification is required.

**The accents are the CLIENT's, not the reference's.** The reference's accent is `#8d3fe8`, deepened to `#420f7b`, with `#e9af43` as a warning colour its own token file marks as a framework default and NOT brand. **None of those three hexes belong to this client and none may be carried across.** This client's accents are the §2 measured values, `#7f2199` purple and `#ffba00` gold.

**Why this is more than a find-and-replace, stated as the trap it is.** Every contrast decision visible in that reference is a dark-ground decision, and the arithmetic reverses on white. Two concrete illustrations, recorded because they are the ones a builder will hit first:

- The reference lightens its violet for text — its token file records the raw `#8d3fe8` measuring 3.45:1 on its canvas and 2.96:1 on its panels, both under the 4.5:1 floor, so a paler violet is substituted wherever the colour becomes small text. On a white ground that whole manoeuvre runs backwards: a paler violet is the FAILING direction. This client's purple and gold must be measured fresh against white at P8. Do not inherit a single ratio from the reference.
- The reference's most distinctive hero effect paints its headline so that moving light only ever ADDS brightness over a solid ink floor. That safety argument depends on the floor being dark. Against dark ink on white, added light REDUCES contrast, and the guarantee inverts into its opposite.

**What DOES survive the inversion, as a method rather than a value:** the reference measures every text role against the worst-case pixel it could land on, deletes the roles that fail, and then writes the result down as a rule — over a photograph it permits heading ink and body ink only, and bars its accent and muted inks entirely. Adopting that METHOD is compatible with §5's contrast floors. Adopting its NUMBERS is not.

### 8.3 What the owner is buying — the reference's structure, as observed

Recorded as observations of that page. They are not a specification for this one; P8 designs this client's own values.

**Section sequence** (from `index.html`, in order): fixed floating header pill · hero · client-logo marquee · a statement-heading section with four figures · a services section of alternating text/media split rows · a full-bleed photographic band · a pricing section · a second full-bleed photographic band carrying one pull-quote · a closing call-to-action band · an inset rounded footer card. **Ten blocks** — corrected 2026-08-13; the sentence above enumerates ten and previously miscounted them as nine. Counted from source: 1 `site-header` + 8 `<section>` + 1 `site-footer`, plus a mobile-only `sticky-cta` that is chrome rather than a block. The shape underneath is content-driven and polarity-free: opener, borrowed credibility, own numbers, what we do, proof event, the offer, breath, ask.

**The measure.** One text column width, `min(68ch, 640px)`, declared once and pinned to the same left axis from hero to close. It does not widen for a wider section, does not re-centre, and does not change when a photograph arrives beside it. The reference allows itself exactly one documented exception (its price table, on the stated grounds that a table is not prose), and it argues the single exception is what makes the measure read as a decision elsewhere. **This is the strongest transferable idea in the reference and it is entirely polarity-free.**

**The interval.** One vertical rhythm value paid top and bottom by every body section, no bespoke padding anywhere; full-bleed bands pay none of their own and take their height from inner padding instead. The rhythm resolves to roughly 151px at a 1440px viewport and retunes smaller below 767px. A sibling rule collapses the incoming section's top padding wherever the background does not change, which is what stops every joint paying the interval twice.

**Container and columns.** Container maximum 1120px with 24px of side padding. Rows are flexbox with per-row modifiers rather than a twelve-column grid; that is what allows the fixed measure to sit beside a media column that absorbs whatever remains.

**Type.** Display face Montserrat, body face DM Sans. The ladder has six steps with a deliberate hole in the middle — nothing between roughly 34px and 17px — and the reference states the gap IS the concept, so emphasis inside body copy is carried by ink weight rather than by an intermediate size. Negative tracking on the large sizes, strongly positive tracking on the 12px uppercase micro-type. Note a trap: one of the five stylesheets carries a SECOND, unused type scale under a header calling it scaffolding and "not the deliverable"; none of those classes appear in the page. Parsing the CSS rather than reading the page yields a wrong answer.

**Discrete spacing steps observed:** 4 / 8 / 14 / 24 / 40 / 64 / 96. **Recorded as an observation of that page only.** §3 of this file still carries no spacing rhythm for this client, and this list does not become one.

**Motion.** One gesture for the entire page: a short fade plus a small rise on one easing curve, with a small stagger on grouped items, and media adding a slight scale-in. Bands add a gentle parallax composed into the same transform so the two cannot fight. Hidden-before-reveal is scoped to a class set by a one-line script, so with no JavaScript nothing is ever hidden. Its stated absent-list — no bounce, overshoot, rotation, flip, loop or autoplay — sits comfortably inside §4. **Two motion items do NOT transfer: the count-up on its figures and the autoplay marquee** (see 8.4).

**Imagery sparsity — worth noting because it is unusual.** Only five distinct raster slots carry that entire page: two framed 4:3 editorial images inside the split rows, two full-bleed 16:9 band photographs, and one set of logos. The hero carries no photograph at all. The reference states it has no grey box and no gradient standing in for a photograph anywhere.

**Explicitly NOT transferable from the hero.** The reference's hero is a 250vh scroll track with a sticky full-viewport stage, four scripts, a particle canvas and a 3D model its own comments record as supplied at 29.94 MB and 1,001,316 triangles before optimisation. `D-008` (§1, §4) governs this slot and is LOCKED: poster frame first, animation never the LCP element, hard byte budget, lighter or no variant on mobile. **The reference's hero payload is incompatible with `D-008` and with §5's "the site must model the service it sells".** What IS worth taking from it: its media layer is absolutely positioned and contributes no height, so the object can be swapped without moving anything else on the page — which is precisely what §1's binding "must survive a concept swap" instruction needs.

### 8.4 BLOCKED DEVICES — the reference's four proof moments are all unusable here

**This is the most important part of §8.** The reference's page is built around four proof devices. **This client has none of the four**, and not through prep failing to look: readiness blockers 5, 9, 12 and 13 were WAIVED by the owner rather than evidenced, which means the site ships honestly WITHOUT those claims. A build that copies the reference section-for-section will produce four hollow slots and, if it copies the copy too, will ship claims that `content-bible.md` and the 26 briefs flatly ban.

**The mechanical gates will NOT save a builder here.** The banned-content patterns in `client-rules.json` are a partial net by that file's own admission ("Do not read this entry as full mechanical coverage"). The reference's own wording slips most of them on vocabulary alone — its headline superlative escapes the superlative pattern only because its vertical word is "MARKETING" rather than "SEO"; re-skinned toward this client it is caught. **Treat `content-bible.md` §2/§3b and the briefs as the claim perimeter; treat green gates as necessary, not sufficient.**

| # | What the reference does | Why this client cannot | Governing |
|---|---|---|---|
| 1 | Publishes a 3-row price ladder with monthly figures and per-location add-ons, standfirst "Nothing is behind a click" | No price may appear anywhere, including "from" figures. The reference's entire wedge is that its prices are printed; this client's wedge is the opposite | `D-001` LOCKED; `content-bible.md` line 84; §5 of this file; `client-rules.json` `ladder: []` — "Do not reconstruct one" |
| 2 | 12 named client logos on an autoplay marquee, alt text naming each as a client | Only 3 client logo files exist and all 3 are rights-unestablished; naming a client without written permission is a hard prohibition | §G-6; `selling-asset-manifest.json` CLIENT-LOGOS "usage rights NOT established"; `content-bible.md` line 78; §5 forbidden patterns ("unlinked logo walls") |
| 3 | Four billion-scale aggregate totals, animated counting up on scroll | The SHAPE is banned, not merely the numbers — an unbacked giant number is the exact tell the category's critic teaches buyers to look for | `briefs/results.md` line 120; `briefs/index.md` line 214; §5 forbidden patterns ("bare stat tiles with no frame") |
| 4 | Closing terms line "Top-3 local or you do not pay." | Three breaches in nine words — see below | `content-bible.md` lines 40, 41, 111; `D-003`; `client-rules.json` RP-1, RP-2 |
| 5 | Named-city result pairs, e.g. "Oceanside, CA +51.37% in the first 3 months" | Carries a duration but no date range, no method, no tool and no permission; names cities beside results | `briefs/results.md` lines 37, 46; `client-rules.json` RP-3 |

**Device 4, spelled out, because it is the one a builder will paste without noticing.** "Top-3 local or you do not pay" is superficially close to this client's own canonical sentence and is three separate breaches:

1. **"Top-3"** — the canonical term is **"first page"**. `content-bible.md` §5 line 111 bars "#1" and "top of Google"; a position promise is the same claim class and asserts a specificity the contract does not contain.
2. **"or you do not pay" standing alone** asserts a TERMINAL remedy. `D-003` as owner-ruled is a **monthly pause that resumes, with the work continuing throughout**. RP-2 requires the pause framing on the same page, at BLOCK severity. Copy may say "your billing stops"; it may never say refund, money-back or risk-free.
3. **"local"** silently narrows the geography to a local-pack claim the contract does not specify.

**The compliant pair is already written and locked** — both sentences, together, never one alone: *"We guarantee first page for the key phrases named in your contract — or you don't pay."* (`content-bible.md` line 40) paired with *"Any month we're not delivering what your contract says, we keep working and your billing stops."* (line 41). **Two live caveats a builder must carry:** that first sentence is BODY COPY ONLY and may NOT be used in structured data, page titles or metas (the JSON-LD row governs those); and whether the phrase survives unqualified at all is an open `[OWNER-DECISION]` at `readiness-verdict.md` §5 item 10. Do not treat it as finally settled.

**What honestly goes in each slot instead.** The slots are good; the occupants change. Recorded as content inputs the build designs from, not as layout instructions:

- **Slot 1 (the reference's densest section, its price ladder).** Its real job is "the one object where the reader learns exactly what they get". This client can do that honestly with a **what-is-included** ladder carrying no figures — `content-bible.md` line 46 supplies the sanctioned sentence: *"One agreed monthly fee covers SEO, web, CRO, branding and design. Quoted per business after a competitive review."* The reference's semantic-table-that-reflows-to-cards mechanic is genuinely the right pattern for structured data and is polarity-free; keep the mechanic, drop the figures. Note `D-005` puts a 7-service mega menu in the nav slot the reference gives to "Pricing".
- **Slot 2 (the logo marquee).** Its job is instant third-party credibility under the hero. The only rights-clear third-party credibility this client owns today is the Google rating. `briefs/index.md` line 51 already specifies this slot: proof by section three, "Three items, stated flat, no tiles" — *"Rated 4.9 from 35 Google reviews"* with its count always travelling with it, the offer mechanic, and the numberless coverage sentence. This also removes the autoplay-motion problem the reference flags against itself.
- **Slot 3 (the stat block).** The client's one number that is fully owned and needs nobody's permission is **the mechanic itself**. Spend the oversized-numeral treatment on the month-by-month cadence rather than on totals. `briefs/results.md` line 76 adds a genuinely strong move the reference has no equivalent of: **state that we do not publish a success rate**, rather than merely omitting it — the absence is more persuasive stated than hidden, and it is the direct answer to the incumbent's published attack that guarantee sellers are vague and unfalsifiable.
- **Slot 5 (named-city results).** The full-bleed geography moment survives; its contents invert from "cities where we won" to what is checkable — the numberless coverage sentence *"We work with clients across US metros, all from our Las Vegas office."* (`briefs/our-locations.md` line 18, verbatim and count-free) plus the objection it provokes, answered at line 30: the phrase set is local, so the work is local even when the desk is not. **A city grid still renders** — the 25 published city pages are a page-count carve-out — but a city grid **with figures** does not.

**Four smaller transplant hazards in the same page**, each banned here: the hero superlative "#1 MARKETING AGENCY IN CANNABIS"; the closing "Only Marketing Agency In Cannabis That Guarantees Results" (this client's whitespace claim must always carry its scope — *"no competitor we researched conditions its SEO fee on delivery of agreed ranking metrics"*, never stated flat, per `briefs/index.md` line 214); a "Most Popular!" badge (exclamation marks are banned outright, and scarcity devices are on §5's forbidden list); and the eyebrow **"Since 2012"**, which is the reference client's year — **this client's is 2015**, and `content-bible.md` line 68 attaches a strategic caveat: state it plainly and do not build a heritage theme on it, because the market comparator has traded since 2005.

**Also note the reference contradicts itself**, which is worth knowing before treating it as authority: its own section rationale rejects a logo wall because the marks "carry empty alt text and no confirmed right to display, so a logo wall would be a claim the build cannot yet stand behind", and its own script comment concedes "a marquee is on the owner's forbidden list because autoplay motion steals attention" — and it then ships both anyway. This client's spec resolves that contradiction in the strict direction.

### 8.5 Imagery direction — the owner's three sources, mapped to what actually exists

The owner names a mixture. Mapped against `selling-asset-manifest.json` (C9) and §6 of this file:

| Source | What exists today | Gap |
|---|---|---|
| **James Sutton photography** | 5 founder images, all web resolution; the largest 571 x 462, and the file named `james-image-highres.jpg` measures 543 x 614 despite the name | **NEEDS-OWNER.** None can lead a full-bleed section or carry a hero. Real photography at print or retina resolution is still outstanding |
| **fal-generated business imagery** | Nothing generated yet | **Ledger action owed — see the flag below** |
| **The Blender hero** | `_spec/visual-refs/blender-pipeline-test.png` (pipeline proof, not a design candidate) plus the three hero concept renders in §7 | Governed by §1 and `D-007`, still PROVISIONAL. `D-008` governs how it ships |

The reference's own image architecture maps unusually well onto this mixture, and it is worth taking: framed editorial images inside split rows are the natural slot for generated business imagery, while the full-bleed bands — where the page raises its voice — are where a real photograph earns its keep, which points at Sutton. The reference frames its editorial images and leaves its bands unframed; note that its framing treatment is a dark-page treatment and does not carry across unchanged.

**⚠ FLAG — an unresolved contradiction, recorded rather than silently resolved.** §6 of this file states `waived: false` and explains it as "the owner has NOT accepted a generated or AI fallback for imagery. No such waiver exists in `decisions-ledger.md`". **The owner's instruction in 8.1 accepts generated imagery.** That is a rank-2 owner instruction and it does contradict the stated rationale for that flag.

**⚑ SUPERSEDED IN PART on 2026-08-13 — read this before the paragraph below it.** That paragraph is preserved, not corrected, because it records why the §8 capture pass was right to refuse. What has happened since:

- **`direction_locked` is now `true`.** The owner saw Concept A animated at final render quality (`_spec/visual-refs/hero-concept-A-climb-1080.mp4`) and ruled *"ratify the hero, lock it in"*; recorded as `D-011` in `decisions-ledger.md`. Note that the route the paragraph below demands is the route that was taken: the dated, attributed `[OWNER-DECISION]` went into the ledger first, and the block was updated to match afterwards.
- **The owed ledger entry has been written.** `D-010` ("Imagery sources — three-way mix, generated imagery AUTHORISED", `LOCKED`) now carries the authorisation this paragraph said was owed, so the sentence "The ledger entry is owed" is discharged. `D-010` states in terms that `ASSET-INTAKE.waived` stays `false` and `real_image_count` stays 15, because it authorises a SOURCE and does not waive the asset-supply window. The instruction to check the ledger before reading §6's `waived: false` therefore still stands — and the ledger now answers it.
- **Unchanged:** `waived` remains `false` in the `ASSET-INTAKE` block, exactly as the paragraph below says. The hero ratification did not touch it, and the two hard limits stated after it survive regardless.

**This pass deliberately did NOT flip the flag.** The `ASSET-INTAKE` block is untouched, `waived` remains `false`, and `direction_locked` remains `false`. Changing an intake flag is a ledger action, not a capture action: the correct route is an `[OWNER-DECISION]` entry in `decisions-ledger.md` dated and attributed, after which the block is updated to match. **Until that entry exists, a builder must not read §6's `waived: false` as "no generated imagery permitted" without checking the ledger, and must not read this section as authorising generated imagery on its own.** The ledger entry is owed.

**Two hard limits survive the change regardless of how the ledger resolves**, because they come from §5 rather than from the waiver:

1. **Generated imagery may never depict a client, a result, a ranking, a dashboard, a SERP, or a person presented as real.** That is fabricated proof, not decoration, and §5's first hard rule and `briefs/index.md` line 43 both bar it.
2. **Real imagery only where the image implies something factual.** Generated imagery is permitted as atmosphere and composition; it may not stand in for evidence.

### 8.6 What this section does and does not do

**It does:** record an owner-chosen reference, its durable snapshot, the surface inversion, the observed structure the owner is buying, the devices that are blocked with what replaces them, and the imagery mapping with its outstanding flag.

**It does not:** author a token system. No colour role, no surface system, no derived tint, no corner or elevation scale, no spacing rhythm, no type scale for this client appears above. Every measurement in 8.2 and 8.3 is stated as **what that reference does**, never as what this build shall use, per PF4 and `client-rules.json`'s own note that choosing so much as an ink hex "would be DESIGN, which prep does not do". §3 remains deliberately absent and §1 remains provisional. **P8 designs this client's system, from these inputs.**

---

## Completion checklist — honest state at P7

- [x] §0 BRAND VISUAL IDENTITY filled FIRST from the owner's own existing-site render, with real measured values
- [x] §0 `BRAND-SIGNATURE` machine block filled with real values, valid JSON, UTF-8 no BOM
- [x] §2 declares `primary_surface: light`; `surface_dominance` is `balanced`, which never inverts, so no tone-pivot marker is required and none is present
- [x] §4 motion and image treatment match §0 `energy: bold`
- [x] §5 hard rules and forbidden patterns recorded as constraints, not tone
- [x] §6 `ASSET-INTAKE` block filled with real integers, booleans and verified paths
- [x] `real_image_count` (15) is at or above the gate floor of 3
- [x] File is UTF-8 with no BOM
- [x] **§1 owner-settled on the hero concept — YES as of 2026-08-13.** The owner ratified Concept A after seeing it animated at final render quality; `D-011`. **This box read `[ ] §1 FINAL and owner-settled — NO. D-007 is provisional by the owner's explicit instruction. This box cannot be ticked by prep.` from 2026-08-12 until that ruling** — quoted here verbatim rather than deleted, because the condition it named is exactly the condition that was met. What it settles is which concept occupies the hero; `D-008` still governs how it ships.
- [x] **`direction_locked: true` — YES as of 2026-08-13, and it records a ratification that happened.** See §6. **This box read `[ ] direction_locked: true — NO, and deliberately so. See §6. It flips when the owner rules on the hero at the FEEL gate.` from 2026-08-12 until the owner ruled** — preserved verbatim; the owner ruled earlier than the build's FEEL gate, on the final render, which satisfies the same condition. `waived` remains `false` and `real_image_count` remains 15, both untouched by this.
- [ ] At the seam: copied to `_handoff/visual-direction.md`, recorded as a `files[]` row plus `visual_direction_checksum` in `HANDOFF-RECEIPT.json` — the build tree does not exist yet, so this is pending.

---

## Sign-off

**Filled by:** client-site-prep P7 remediation pass · **Date:** 2026-08-12
**Status:** COMPLETE as an inputs document. **NOT locked as a direction** — §1 and the `direction_locked` flag both remain open on the owner's own instruction, and both are recorded as open rather than quietly closed.

**⚑ RATIFICATION AMENDMENT — 2026-08-13.** The status line above is preserved as the 2026-08-12 state and is superseded on one point only: the owner has seen hero Concept A animated at final render quality (`_spec/visual-refs/hero-concept-A-climb-1080.mp4`) and ruled *"ratify the hero, lock it in"*, so **§6's `direction_locked` is now `true`** and the direction IS locked. Recorded as `D-011` in `decisions-ledger.md`; `D-009`, the hold that kept the flag false, is discharged by it. **Nothing else in this file changed.** `waived` is still `false`, `real_image_count` is still 15, the asset-supply window is still open (logo vector and real founder photography still owed), §3 still carries no token system, and no content rule, ban or claim perimeter moved. **The build is still NOT cleared to start:** readiness blocker 15, the counsel-supplied privacy policy, is the sole remaining gate, `ready_for_build` stays `false`, and no handoff receipt or seam copy may be produced on the strength of this flag.
