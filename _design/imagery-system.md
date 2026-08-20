# IMAGERY SYSTEM - seoguarantee

Status: PLANNED, NOT GENERATED. This document plus `_images.json` are the reviewable
plan for the IMAGERY stage. No image has been generated and no spend has been
authorised by the owner. `generate-images.mjs` has been run with `--dry-run` only.

Derived from, and never inventing beyond:

* `_handoff/visual-direction.md` (C7) sections 0, 2, 4, 5, 8.3, 8.5
* `_handoff/sitemap.yaml` (the 26 pages and their types)
* `_handoff/briefs/*.md` (the per page visual slots)
* `_handoff/client-rules.json` and `_handoff/content-bible.md` (the claim perimeter)
* `.claude/skills/client-site-build/SKILL.md` IMAGERY STAGE, rule 1a and rule 5
* `.claude/design-system-unified/00-globals/specs/_COMPOSITION-LAWS.md` R8

---

## 1. TREATMENT - the look every generated photo obeys

One sentence: a white dominant studio world, deep royal purple as the structural
colour, warm gold as punctuation, lit hard and dramatically, composed as editorial
still life or architecture, carrying no information of any kind.

| input | source | what it forces |
|---|---|---|
| `energy: bold` | C7 section 0 | dramatic, high contrast, confident. C7 section 4 bars "timid fade-ins and washed-out stock", so every prompt carries `no washed out pastel stock look` and `no low contrast haze` in its negatives. |
| `primary_surface: light`, white is the ground | C7 section 2 | every frame is white dominant. Purple is a structural plane or a bound object; gold is a single accent. |
| Purple and gold are ACCENTS, not the field | C7 section 2 | no image is majority purple. The two `texture-*` macros are the only frames where a single accent fills the frame, and they are accents by definition. |
| No stock wash | C7 section 2 and section 4 | no image is authored to sit at low opacity behind text. Every slot is a FRAMED media object inside a designed section. |
| Palette described as mood, never as a value | IMAGERY-GENERATION-SPEC section 2 | no hex code appears in any prompt. The palette is written as "a white dominant world with deep royal purple as the structural color and warm gold as punctuation". |
| No text baked into an image | C7 section 5, D-BRAND-RAILS-006/007 | every prompt ends with `no text, no watermark` and additionally negates logos, signage, brand marks, numbers and lettering. The exclamation mark and emoji bans apply to any string baked into an image, so no image carries a string at all. |

Composition rules that follow from the treatment:

1. **No people in any generated frame.** Not a face, not a hand, not a body. The
   founder and the team are the only people on this site and they are carried by
   real owner supplied photographs (section 7). Every prompt negates `no people`
   and `no faces`.
2. **No interiors that could read as premises.** Where a subject risked reading as
   an office, a clinic, a treatment room or a client's building, the prompt is
   pinned to `studio still life with no room context`. This is why there is no
   generated "our office" image on `about` and no generated "clinic" image on the
   persona pages.
3. **Blank means blank.** Documents, dials, notepads, card stock and book spines
   are specified unprinted and unlettered, so the frame cannot carry a claim.

---

## 2. THE LOCKED SET

25 slots. Every row below has a matching entry in `<buildDir>/_images.json` with
the same `id`. `out` is always `assets/<id>.jpg`, relative, never absolute.

### 2a. Split row media (18 slots, `portrait_4_3`, frame `aspect-ratio: 3/4`)

C7 section 8.5: "framed editorial images inside split rows are the natural slot for
generated business imagery". These are that slot and nothing else.

| id | subject | orientation | where it is used |
|---|---|---|---|
| `split-contract-terms` | open deep purple folio, blank unprinted pages, gold pen laid across | `portrait_4_3` | `guarantee` s2 contract terms and s5 how key phrases are named; `index` s5 named metrics block; `seo-services` s3 what we are contracted to deliver; `las-vegas-seo` s6 |
| `split-monthly-assessment` | twelve identical blank white cards in a row, one lifted and gold edged | `portrait_4_3` | `guarantee` s7 what happens in a month off target; `ui-ux-design` s8, `web-development` s9, `graphic-design` s8, `branding` s8 (how this is assessed and billed) |
| `split-seo-method` | white architectural wall of empty shelf compartments, one purple lined and gold lit | `portrait_4_3` | `seo-services` s5 what the SEO work covers |
| `split-web-design-craft` | blank paper stock samples, purple drafting rule, gold set square | `portrait_4_3` | `web-design` s4 what we build |
| `split-ui-ux-craft` | blank index cards pinned in a column, purple pins, gold outlined card, purple cord | `portrait_4_3` | `ui-ux-design` s4 what we design |
| `split-web-development-craft` | white modular architectural block model, one purple block, one gold edge | `portrait_4_3` | `web-development` s4 what we build |
| `split-cro-craft` | two identical blank forms side by side, gold cube and purple cube | `portrait_4_3` | `cro-services` s5 what the CRO work covers |
| `split-graphic-design-craft` | nine plain uncut paper squares in white, purple and gold, laid in a grid | `portrait_4_3` | `graphic-design` s3 what the design work covers |
| `split-branding-craft` | unprinted packaging forms, purple cloth bound book, blind gold edge | `portrait_4_3` | `branding` s4 what brand work covers |
| `split-one-fee-consolidation` | scatter of thin white folders beside one thick purple folio banded in gold | `portrait_4_3` | `full-suite` s4 what the one fee replaces; `index` s7 inclusion value |
| `split-trade-specificity` | tall column of tools from five different trades on a purple runner | `portrait_4_3` | `industries` s2 why this trade is different |
| `split-dental-materials` | plain white ceramic dish and two smooth ceramic forms on folded white cloth, deep purple ceramic block | `portrait_4_3` | `industries-dental` s3 the dental phrase ledger |
| `split-law-materials` | stack of unlettered cloth bound volumes, gold ribbon marker | `portrait_4_3` | `industries-law-firm` s3 practice area and jurisdiction phrase map |
| `split-medspa-materials` | white ceramic, brushed steel and clear glass group, purple panel, gold band | `portrait_4_3` | `industries-medical-spa` s3 treatment phrase demand map |
| `split-hvac-materials` | copper and steel pipe sections, gauge with a blank unmarked dial | `portrait_4_3` | `industries-hvac` s3 emergency and seasonal phrase structure |
| `split-contracting-materials` | rolled blank drafting paper, steel rule, plumb bob | `portrait_4_3` | `industries-contracting` s3 the search to estimate path |
| `split-las-vegas-desert` | empty desert highway to bare mountains, purple sky, low gold horizon band | `portrait_4_3` | `las-vegas-seo` s3 our home market; `our-locations` s2 how we work a market we are not physically in |
| `split-consultation-table` | white table set with a blank notepad and gold pen, one purple chair back | `portrait_4_3` | `contact-us` s3 what happens on the call; `thank-you` s2 what happens next |

### 2b. Card grid headers (5 slots, `landscape_4_3`, frame `aspect-ratio: 4/3`)

The only genuine card grid on this site that may carry photography is the blog
index. `seo-blog` s3 states the library is FIVE posts and "the layout must not look
empty at five", so each of the five cards carries its own distinct header.

| id | subject | orientation | where it is used |
|---|---|---|---|
| `card-blog-authority` | heavy polished gold sphere on a white plinth, purple panel | `landscape_4_3` | `seo-blog` s3 card header, post "Authority and Search Rankings" |
| `card-blog-essentials` | five white river stones in a cairn, purple top stone, gold light line | `landscape_4_3` | `seo-blog` s3 card header, post "5 Important SEO Tips and Tricks" |
| `card-blog-starting-out` | plain closed white box, purple ribbon, gold wax seal with no emblem | `landscape_4_3` | `seo-blog` s3 card header, post "Beginner SEO Tips and Tricks" |
| `card-blog-toolkit` | row of small polished steel precision tools, purple strip, one gold handle | `landscape_4_3` | `seo-blog` s3 card header, post "13 SEO Chrome Extensions That Are Free" |
| `card-blog-factors` | exploded tiers of white geometric blocks, purple edges, one gold block | `landscape_4_3` | `seo-blog` s3 card header, post "Search Engine Optimization Factors" |

### 2c. Texture accents (2 slots, `square_hd`, no fixed frame, NEVER a split column filler)

Both are marked `"generic": true` in `_images.json`. They are the ONLY declared
members of the generic pool.

| id | subject | orientation | where it is used |
|---|---|---|---|
| `texture-purple-material` | macro of a single swept deep purple pigment smear on a bright white ground: polished centre carrying one raking highlight, granular spattered crust around the perimeter with scattered specks | `square_hd` | small square accent beside stat and quote moments, cross page |
| `texture-gold-edge` | macro of a polished gold edge meeting a white matte plane | `square_hd` | small square accent beside stat and quote moments, cross page |

### 2d. Slots deliberately NOT generated, and why

This list is part of the spec. Each line is a place a builder will be tempted to
add a generated image, and each is refused on a source.

| slot | refused because |
|---|---|
| Every page HERO on all 26 pages | Every hero is a MOTION slot governed by D-008 (poster frame first, short loop after, never the LCP element, still under reduced motion). Stated per page at `briefs/index.md:43`, `briefs/guarantee.md:38`, `briefs/full-suite.md:21`, `briefs/industries.md:23`, `briefs/our-locations.md:22`, `briefs/las-vegas-seo.md:18`, and every T-FEATURE and T-PERSONA brief. The poster comes from the ratified hero concept render, not from fal. |
| Full bleed bands and image dividers, all pages | C7 section 8.5: the full bleed bands "are where a real photograph earns its keep, which points at Sutton". Generated imagery does not take that slot. Because the five founder files are web resolution only (largest 571 x 462, C7 section 4), the bands are composed to work at the scale the real photograph supports, per C7 section 5 "where a real asset does not exist, the section is composed to work without it". This is why the set contains ZERO `landscape_16_9` entries. |
| `results` case study cards | Every metric on the results page is an owner placeholder pending section G-6 permission. A generated image on a case card would read as depicting a client or a result. Barred by C7 section 8.5 hard limit 1 and `briefs/index.md:43`. |
| `our-locations` metro index cards (25 metros) | A city image beside a metro name implies a presence there. `briefs/about.md:61` and `briefs/index.md:210` ban any claim of offices in the coverage metros. Cards are type led. |
| `about` office and founder slots | The founder is a real named person. `briefs/index.md:45`, `briefs/index.md:175` and `briefs/guarantee.md:254` all state that a generated stand in is NOT acceptable for him. An "our office" image would imply a fact. Real assets only, see section 7. |
| `videos` card posters | 17 real YouTube poster frames already exist in `assets/`. Owner supplied assets take precedence. |
| `privacy-policy` | `briefs/privacy-policy.md:56` requires prose in the legal document measure with no image in the body, enforced by `verify-legal-is-document.mjs`. |
| `index` s6 pause mechanic and s8 capability switcher, `full-suite` s3, `industries` s3, `index` s10 | `briefs/index.md:101` specifies a month by month billing timeline DIAGRAM, and s8 is eight XS panels. C7 section 5 sets the technique ceiling as "crafted CSS diagrams that explain the mechanic", spent "explaining it rather than decorating around it". These are token built diagrams and type led tiles, not photographs. |
| Client mockups, client logos, press logos | Rights blocked. C7 section 6: section G-6 permission is not on file for the 8 mockups and 3 client logos, and the 4 press logos are marked DO NOT SHIP. They appear in no slot, generated or real. |

---

## 3. THE HONESTY PERIMETER - what generated imagery may never do

These two limits come from C7 section 5 by way of section 8.5, and they survive
regardless of how the `waived` flag resolves.

1. **No generated image may depict a client, a result, a ranking, a dashboard, a
   SERP, a chart, an analytics screen, or a person presented as a real client or
   team member.** That is fabricated proof, not decoration. Barred by C7 section 5
   first hard rule and `briefs/index.md:43`.
2. **Generated imagery is ATMOSPHERE AND COMPOSITION ONLY. It may never stand in
   for evidence.** Where an image would imply something factual, the slot is
   composed to work without a photo instead. Section 2d is the list of every slot
   where that ruling was applied.

Mechanically, every prompt in `_images.json` carries this negative set:
`no people, no faces, no screens, no dashboards, no charts, no graphs, no logos,
no signage, no washed out pastel stock look, no low contrast haze, no text, no
watermark`, with per slot additions (`no numbers`, `no percentages`, `no bodies`,
`no before and after`, `no buildings`, `no city skyline`, `no browser`, `no code`,
`no user interface`, `no brand marks`, `no printed artwork`).

### 3a. THE NO TEXT RULE (owner, 2026-08-13). Two halves, both binding.

**Owner instruction, verbatim in substance: no generated image may carry text in
the actual render; what appears must be images only.** That covers two different
failures and both are enforced here.

**HALF ONE: no lettering in the PIXELS.** Every prompt already ended with
`no text, no watermark` in the first generation pass, and flux drew markings
anyway: gold foil pseudo lettering along a book spine in `split-branding-craft`,
a stamped mark plus embossed pseudo lettering on the tools in
`split-trade-specificity`, and engraved lettering around the gauge bezel in
`split-hvac-materials` (the dial FACE was correctly blank, so the prompt was
honoured exactly where it was specific and ignored on the surface next to it).

The lesson, recorded because it will recur on the next build: **a negative prompt
does not bind the model. Only SUBJECT CHOICE plus verification does.** Asking for
a book without a title still produces a spine, and a spine attracts foil. So the
rule is now:

> Do not specify an object whose real world counterpart CARRIES a marking, then
> ask for it to be blank. Specify an object that has no surface for a mark.

Mark bearing subjects to avoid: books and book spines, branded or manufactured
hand tools, instruments, gauges and dials, rulers and any measuring edge, swatch
fans, packaging with a face, keyboards, screens, signage, plaques. Mark free
substitutes that carry the same meaning: raw material stock (timber, copper,
steel, ceramic, cable), blank unprinted paper and card, plain glazed ceramic,
smooth unmarked metal, folded cloth, plain geometric forms.

Every regenerated prompt additionally negates the artefact class by name:
`no engraving, no stamped marks, no maker marks, no foil lettering, no embossing,
no labels, no printing of any kind, no numerals, no tick marks`.

**HALF TWO: no text OVER a generated image, in any template or page.** A
generated image is a picture, not a text bed. Downstream phases (COPY, per TYPE
TEMPLATES, BULK, HOME) MUST NOT:

* overlay a headline, sub head, label, badge, price, statistic or quote on top of
  a generated image;
* place text inside a generated image's frame using absolute or negative offsets;
* use a generated image as a full bleed background behind copy (that is also the
  C7 section 4 "no stock wash" ban, arrived at from the other direction).

Text sits BESIDE the image in the adjacent column of the split, or ABOVE or BELOW
it in the flow, never on it. The one permitted overlay is the scrim plus caption
already specified for owner supplied photography in section 7, which applies to
REAL photographs and never to generated imagery.

**Verification standard for half one, learned the expensive way.** A no text
guarantee cannot be given from a contact sheet. The gauge bezel lettering was
invisible at 800px per image and only decidable at 4x device scale. Any future
claim that this set is text free must rest on a 4x pass over every slot, not on
a thumbnail read and not on the presence of `no text` in the prompt.

Vertical specific additions honoured in the prompts:

* `industries-medical-spa` (`briefs/industries-medical-spa.md:21` and `:73`):
  clinic and interface imagery only, no faces, no bodies, no procedure imagery, no
  before and after. `split-medspa-materials` is a material still life with an
  explicit `no skin`, `no bodies`, `no before and after` negative and no room.
* `industries-contracting` (`briefs/industries-contracting.md:21`): no stock
  construction heroics and no photographs of finished projects that could read as
  this agency's client work. `split-contracting-materials` negates
  `no buildings`, `no construction site`, `no finished project`.
* `graphic-design` and `web-design` and `branding` (`briefs/graphic-design.md:19`,
  `briefs/branding.md:19`): any client artwork requires written permission. The
  three craft slots show unprinted MATERIAL, never a work sample, and negate
  `no printed artwork` and `no brand marks`.

---

## 4. PER-TOPIC LAW AND THE REUSE CAP

This section is the build agnostic discipline from `SKILL.md` IMAGERY STAGE rule 5,
applied to this build.

**PER-TOPIC.** A page draws topic relevant imagery generated FOR its own slots. It
does not reach into a shared generic pool for something that "kind of fits". When a
new page or section needs a picture, ADD a slot to `_images.json` and re-run the
generator. The generator is idempotent, so existing images are never re-spent.

This is why the eight T-FEATURE pages carry eight DIFFERENT craft images rather
than one shared "agency at work" photo, and why the five T-PERSONA pages carry five
different trade material still lifes rather than one shared industry image.

**THE GENERIC POOL is exactly two members**, both `square_hd` texture accents:
`texture-purple-material` and `texture-gold-edge`. Everything else in the set is
TOPIC imagery. The two mechanic images (`split-contract-terms`,
`split-monthly-assessment`) appear on several pages, and they are still TOPIC
imagery rather than filler: the contract and the month by month assessment ARE this
brand's subject, they are the one thing C7 section 5 says technique should be spent
explaining, and they are not a grab bag stand in.

**THE HARD REUSE CAP**, enforced by `verify-image-reuse-cap.mjs` (G-IMG-CAP) on
every page write:

* No single NON-HERO photo repeats more than about 2 times within a page. The HERO
  is exempt. On this build the hero is a motion poster rather than a photo, so the
  exemption is not load bearing here and every generated image is subject to the
  cap.
* A page with 4 or more images must be diverse: distinct assets at or above
  `ceil(total / 2)`.
* No generic pool concentration: on a page with 4 or more images, a majority of the
  distinct NON-HERO assets must NOT be `"generic": true` members. With only two
  generic members in the whole build, any page that reaches four images is already
  carried by topic imagery.

Planned per page distribution, checked against the cap:

| page | generated images planned | distinct | cap check |
|---|---|---|---|
| `index` | `split-contract-terms`, `split-one-fee-consolidation`, `texture-purple-material` | 3 | under the 4 image diversity floor, no repeat |
| `guarantee` | `split-contract-terms`, `split-monthly-assessment`, `texture-gold-edge`, `texture-purple-material` | 4 | distinct 4 of 4, generic 2 of 4 is not a majority |
| `seo-blog` | five distinct card headers | 5 | distinct 5 of 5 |
| every T-FEATURE page | its own craft image plus at most one mechanic image plus at most one texture | 2 to 3 | under the diversity floor, no repeat |
| every T-PERSONA page | its own trade material image plus at most one texture | 1 to 2 | no repeat |
| `results`, `our-locations`, `videos`, `about`, `privacy-policy`, `404` | none generated | n/a | see section 2d |

---

## 5. ORIENTATION TABLE (DS LAW R8)

A media slot's `image_size` is DICTATED by the section pattern the slot lives in.
It is not a free per image choice. Source:
`.claude/design-system-unified/00-globals/specs/_COMPOSITION-LAWS.md` R8 and
`SKILL.md` IMAGERY STAGE rule 1a. The frame `aspect-ratio` must MATCH.

| section pattern the slot fills | orientation | `_images.json image_size` | frame `aspect-ratio` | slots in this build |
|---|---|---|---|---|
| Media in ONE column of a SPLIT or feature card (`SECTION-COMPONENTS.md` #11 / #12 / #16, media beside a copy column) | PORTRAIT | `portrait_4_3` | `3/4`, with a capped `max-height` so the media column never dwarfs the copy column (G-DENSITY safe) | all 18 `split-*` slots |
| Full bleed HERO or image divider (`SECTION-COMPONENTS.md` #58) | LANDSCAPE | `landscape_16_9` | `16/9` | NONE. Reserved for real photography per C7 section 8.5, see section 2d |
| Capability, product, proof or case study CARD header in a grid | LANDSCAPE 4:3 | `landscape_4_3` | `4/3` for a consistent row of card headers | all 5 `card-blog-*` slots |
| Texture or material ACCENT, never a split column filler | SQUARE | `square_hd` | none fixed, sized as a small square accent | `texture-purple-material`, `texture-gold-edge` |

Two rules that travel with the table:

1. Every stretched grid track media frame carries `width: 100%` and `min-width: 0`
   (the media fits track law, R8's companion, enforced by
   `verify-media-fits-track.mjs`).
2. A square texture is NEVER dropped into a split column. That is the exact failure
   R8 was written to stop: a square asset under fills a 4:3 or 3:4 split box.

---

## 6. FAL EXTEND ALLOWANCE - how to add more on brand

The generator is `.claude/skills/client-site-build/scripts/generate-images.mjs`,
fal `flux/dev`, about $0.025 per image, concurrency 3, idempotent.

To add a slot:

1. Confirm the need is a REAL visual need in a brief, not decoration.
2. Run it through section 3. If the image would imply a fact, compose the section
   without a photo instead.
3. Pick the `image_size` from the section 5 table by the SECTION PATTERN, never by
   taste.
4. Write the prompt on the recipe in
   `.claude/skills/client-web-mockup/references/IMAGERY-GENERATION-SPEC.md`
   section 2: subject, then the treatment language from section 1 above, then the
   palette as MOOD with no hex, then `editorial premium brand photography, clean`,
   then the negative tail, ending with `no text, no watermark`.
5. Append the entry to `_images.json` and add a row to section 2 above and to
   section 5 if it introduces a new pattern.
6. Re-run the generator. Existing images are skipped, so there is no re-spend.

**Spend is owner gated on this build.** C7 section 6 records `waived: false` and
`real_image_count: 15`, and D-010 authorises generated imagery as a SOURCE without
waiving the asset supply window. Run `--dry-run` and take the estimate to the owner
before any billable run.

**Operator QA is a separate required gate.** A green generator exit means the files
are PRESENT, not that they are GOOD. Open every generated image and confirm it is
on subject, on palette, and clean: no stray text, no logo artifact, no watermark,
no person, no screen, no chart. Delete any miss and re-run to regenerate only that
one.

---

## 7. OWNER SUPPLIED ASSETS TAKE PRECEDENCE

Per P7.5 ASSET-INTAKE and C7 section 6. The generator fills gaps; it never
displaces a real asset.

| asset | measured | how it may be used |
|---|---|---|
| `...full-suite-image.jpg` | 1920 x 1216 | the ONE true hero resolution image recovered. Already placed in the locked chrome's mega panel featured zone. Do not re-place it as a page hero. |
| 5 James Sutton photographs | largest 571 x 462; `james-image-highres.jpg` is 543 x 614 despite its name | deliberate small to medium scale only. CANNOT lead a full bleed band and CANNOT carry a hero (C7 section 4). Required, and a generated stand in is refused, for `index` s12 stance line, `guarantee` s15 founder close, `about` s2, `las-vegas-seo` s4, `videos` s1. |
| 9 team portraits | 350 x 400 each | a small grid only. `about` team block. |
| 17 YouTube poster frames | various | `videos` card posters. |
| 8 client mockups, 3 client logos, 4 press logos | 1500 x 1000 and smaller | RIGHTS BLOCKED. Section G-6 permission is not on file and the press logos are marked DO NOT SHIP. They appear in NO slot. |

---

## 8. SIGN OFF

| item | state |
|---|---|
| Slots planned | 25 |
| `portrait_4_3` | 18 |
| `landscape_4_3` | 5 |
| `square_hd` | 2 |
| `landscape_16_9` | 0, deliberately, see section 2d |
| Marked `"generic": true` | 2 |
| Images generated | 0 |
| Spend to date | $0.00 |
| Owner authorisation to spend | NOT GIVEN |
