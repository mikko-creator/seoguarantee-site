# DECISIONS LEDGER — seoguarantee

**Purpose:** the running record of owner decisions and their status. This is **C5** in the PREP→BUILD handoff set.
**Status key:** `LOCKED` = settled, downstream may rely on it · `PROVISIONAL` = chosen but explicitly re-openable · `OPEN` = unresolved, blocking something.

---

## D-001 · Pricing presentation — `LOCKED`
**Decision:** quote-gated. No prices published anywhere on the site, including "from $X".
**Owner, verbatim (intake line 127):** *"DO NOT show any pricing yet, pricing depends on the need of the client which varies from business to business"*
**Date:** 2026-08-11 · **Consequence:** no pricing page in the 26-page set; the trust burden shifts onto the guarantee page.

## D-002 · Proof strategy — `LOCKED`
**Decision:** fabricated-fallback. Real owner data is authoritative wherever supplied and is never overridden; where content is missing, prep authors clearly-swappable representative content so no gap stalls the build. Nothing invented ships as fact.
**Date:** 2026-08-11

## D-003 · The offer mechanic — `LOCKED`
**Decision:** monthly retainer agreed up front · assessed **month by month** against agreed metrics · if off-target, **billing PAUSES and RESUMES** when results are back on track, and **the work continues throughout** · key phrases **proposed by the agency, signed by the client** — no client veto or substitution right.
**Owner, verbatim (intake lines 19/21):** *"A marketing agency that guarantees you'll be in the first page of Google on key phrases that matter or you don't pay"*
**Date:** 2026-08-11 · **Ratified through four explicit rulings** the same day.
**Consequence:** copy may say "your billing stops"; it may **never** say refund / money-back / risk-free.

## D-004 · Site plan — `LOCKED`
**Decision:** 138 live URLs → **26 pages**. 25 city leaves consolidate to one coverage page plus a real Las Vegas page; 14 internal ops pages and 3 test pages are 410'd, not redirected; 20 portfolio items merge into `/results/` reversibly; the 5 nested `/industries/` URLs change slug under the flat build schema.
**Owner, verbatim:** *"site plan is now approved"*
**Date:** 2026-08-11 · **Scope explicitly NOT covered:** §G-6 claims substantiation, §G-8 canonical NAP.

## D-005 · Mega menu — `LOCKED`
**Decision:** nav slot 2 becomes a mega menu over 7 service pages — SEO Services · Web Design · UI/UX Design · Web Development · CRO Services · Graphic Design · Branding — with `full-suite` as the hub parent.
**Date:** 2026-08-11 · **Consequence:** partially reverses the anti-sprawl ruling; mitigated by requiring every service page to state the service is included in the one agreed fee.

## D-006 · Visual direction — `PROVISIONAL`
**Decision:** white-dominant ground with purple and gold as accents, keeping the dark purple chrome as brand signature.
**Owner, verbatim (intake line 90):** *"I want this redesign to have a majority white clean feel with the purple and gold accents from the current live site. I am aiming for a clean, modern, hip look"*
**Status:** the owner leaned this way in discussion but has **not** confirmed against a rendered specimen. Final confirmation happens at the build's **FEEL** gate.
**Tone source:** `brand-visual-signature.json` records `surface_dominance: "balanced"` — so a light-leaning direction needs **no** tone-pivot ratification, and `signature_moves` preserves `dark-purple-chrome` + `dark-hero` so the build cannot strip the purple wholesale.

## D-007 · Hero animation concept — `PROVISIONAL — EXPLICITLY NOT LOCKED` · **SUPERSEDED IN PART 2026-08-13 — the hero slot is now RATIFIED, see D-011**
**Decision:** proceed with **Concept A — "The Climb"** (a search-result card rising into position one, displacing the greys; gold rank chip and underline).
**Owner, verbatim:** *"okay let's go with option A for now but do not lock it as I might want to update it as we go along, I want to see how this will be displayed in the hero section with actual animation before I finalize. For now let's proceed"*
**Date:** 2026-08-11
**Explicit re-open conditions — this decision is NOT settled:**
1. The owner has seen **stills only**. Final selection requires seeing it **animated, in a hero layout**, at the build's FEEL gate.
2. Concept **C — "The Meter"** remains live as the recurring site-wide motif and as a hero alternative. It is strategically the sharper idea (it dramatises the payment mechanic, which no competitor can show) and was only set aside because its blockout render was the roughest.
3. Concept **B — "The 1st Mark"** is blocked, not rejected. It requires the logo vector (`.ai`/`.svg`/`.eps`), which does not exist in any supplied asset — only web PNGs. If that lands in `_inbox/`, B returns as a candidate.
**Downstream instruction:** no phase may treat Concept A as final. Briefs and the visual direction must describe the hero slot in terms that survive a concept swap.

**⚠ SUPERSEDED IN PART 2026-08-13 by D-011 — original text above preserved verbatim, nothing retracted.** Re-open condition **1 has been MET**: the owner saw Concept A animated at final quality (`_spec/visual-refs/hero-concept-A-climb-1080.mp4`) and ratified it. This decision is therefore **no longer PROVISIONAL for the hero slot** — Concept A is final and `direction_locked` is `true`. Condition **2** is spent as written: Concept C is retired as a *hero alternative*, while its separate role as the recurring site-wide motif was **not** ruled on and survives untouched. Condition **3** survives as an asset dependency — Concept B still needs the logo vector — but the vector arriving no longer reopens the hero on its own; that would take a **new** owner decision. **The downstream instruction is spent for the hero slot**, and the copy written to survive a concept swap stays exactly as written: it cost nothing, and it is the reason the swap stayed cheap right up to the moment it stopped being needed.

## D-008 · Hero animation build rule — `LOCKED` (engineering constraint, not a preference)
**Decision:** whichever concept wins ships as a **short seamless loop plus a poster frame**, never a video file dropped into the hero.
- The poster paints first, so the animation can **never** be the LCP element.
- The loop lazy-loads after LCP; `prefers-reduced-motion` receives the still.
- Mobile gets a lighter variant or none.
- A hard byte budget applies.
**Rationale:** the client sells SEO. Prospects run PageSpeed on the vendor's own site as basic due diligence, and `D-MARKET-002` actively teaches buyers to do so. A hero animation that damages Core Web Vitals would turn the homepage into an argument against the offer — the same principle (M§5.1, "the site must model the service it sells") that drove removing the 25 thin city pages.

## D-009 · C7 `direction_locked` stays FALSE — handoff deliberately waits — `LOCKED` · **DISCHARGED 2026-08-13**

**Decision:** leave `visual-direction.md`'s `ASSET-INTAKE.direction_locked` at **`false`**. The PREP→BUILD handoff does not proceed until the owner has seen the hero animated and ratified the direction at the build's **FEEL** gate.
**Owner, verbatim:** *"go with option a"* (2026-08-12), choosing to leave the flag false rather than ratify early or waive.

**The conflict this resolves.** Two gates require the flag to be `true`:
- `verify-handoff-complete.mjs` lines 98–100 — `const lockOk = j.direction_locked === true;` → `fails.push('C7 direction_locked !== true')`
- the build's `verify-asset-intake.mjs` — gates the first `_design/*.css` write on the same flag

So **the handoff fails closed even when `blocker_count` reaches 0.** That is now an intended state, not a defect.

**Why the flag was not simply flipped.** D-007 records the owner's instruction verbatim: *"do not lock it as I might want to update it as we go along, I want to see how this will be displayed in the hero section with actual animation before I finalize."* Setting `direction_locked: true` would fabricate an owner ratification that never happened — precisely the failure class the P7 audit caught three times elsewhere (the "safe" absolute claim, the overstated remedy, "Verified precedent"). The agent that authored C7 flagged the contradiction rather than resolving it silently, which was correct.

**What unblocks it:** the owner sees the hero animated in a hero layout, ratifies, and the flag is flipped **with that ratification recorded here**. Until then the spec is complete and parked, not broken.

**⚠ DISCHARGED 2026-08-13 — the hold is released, by the exact event this entry named as the one that would release it.** All three steps in the line above happened, in that order: the owner saw Concept A animated at final quality, he ratified it, and the flag was flipped with the ratification recorded — see **D-011**. `ASSET-INTAKE.direction_locked` is now `true`, and both gates that read it (`verify-handoff-complete.mjs:98-100`, the build's `verify-asset-intake.mjs`) now pass.

**Nothing above is retracted, and a discharge is not a repudiation.** Every word of this entry was correct when written and remains the reason the flag was not flipped earlier. **DISCHARGED is a distinct state from both CLOSED and WAIVED:** the condition was **met**, not repaired (nothing was ever broken here) and not skipped (the owner was separately offered a D-009 waiver in `WAIVER-DRAFT.md` and **declined it**). This hold ended the honest way — by waiting until the thing it was waiting for actually arrived.

**What the discharge does NOT do.** It does not open the seam. `ready_for_build` stays `false`, the verdict stays **NO-GO**, and no `HANDOFF-KICKOFF.json` has been written, because blocker **15** is still open and G7 requires `blocker_count === 0`. It also does not waive the asset window: `ASSET-INTAKE.waived` stays `false` and `real_image_count` stays `15`.

## D-010 · Imagery sources — three-way mix, generated imagery AUTHORISED — `LOCKED`

**Decision:** site imagery comes from exactly three sources: (1) **James Sutton photography** carried over from the current site, (2) **fal-generated images** related to the business, (3) the **Blender-rendered hero animation**. Generated imagery is explicitly permitted as a first-class source, not a fallback.

**Owner, verbatim (two separate instructions, both this engagement):**
- *"for the imagery, I want to use a combination of 3 things, 1st is keeping James Sutton imagery from the current site, 2 is generated images using fal that are related to our business, and 3 I want to utilize blender ... I want a very cool eye catching video animation in the hero section"*
- *"the imagery is a mixture of fal generated images and James Sutton"* (2026-08-13, alongside the structural reference)

**Why this entry exists.** The instruction was given twice and acted on — `visual-direction.md` §6 and §8 both assume generated imagery — but **no ledger entry authorised it**. `ASSET-INTAKE.waived` stands at `false`, meaning the spec formally still demands real photography for every slot it cannot fill. That gap was found on 2026-08-13 by a mapping audit, which correctly reported the authorisation "owed". This is the same defect class as blocker 3: an owner ruling load-bearing across many artifacts, resting only on transcription. Recording it here is what makes it durable.

**The gap this decision has to cover — measured, not estimated.** The homepage brief alone declares roughly **15 image slots** (1 hero + 8 capability panels + 5 vertical tiles + 1 founder portrait). Against that, the rights-clear inventory is 15 files, of which:
- **exactly ONE** (`full-suite-image.jpg`, 1920×1216) is large enough to carry a full-bleed band,
- **5** are web-res founder crops — usable in small slots, cannot lead a page,
- **9** are team portraits with **no declared slot** anywhere in the 26 briefs,
- **8 client mockups** at 1500×1000 — the assets that would naturally fill editorial rows — are **rights-blocked** (`selling-asset-manifest.json`, usage rights not established).

So the homepage needs roughly **14 generated slots**, and the reference this client is modelling runs its entire homepage on only 5 raster slots. Generated imagery is therefore not a convenience here; without it the site cannot be built as specced.

**Constraints that travel with this authorisation:**
- Generated imagery may depict **business/abstract subject matter only**. It may **never** depict a person presented as a client, a team member, a customer, or a named business — that would be a fabricated proof, which D-002's fabricated-fallback allowance does not cover and `content-bible` §3b forbids.
- It may never be used to manufacture the appearance of case-study evidence, client premises, or results.
- Real owner photography always outranks a generated image for the same slot.
- Every generated asset is logged in C9 with its source marked, so a later reader can tell generated from photographed.

**Still owed by the owner (unchanged by this entry):** the logo vector and real founder photography at print/retina resolution. `ASSET-INTAKE.waived` stays `false` and `real_image_count` stays **15** — this decision authorises a source, it does not waive the asset-supply window.

**Cost of this choice:** none to the spec. The build simply does not start. Options rejected: ratifying the visual direction early (over-commits), and a written waiver (records a decision the owner did not make).

> **⚠ ANNOTATED 2026-08-13 — the sentence above is now historical.** "The build simply does not start" was true while D-009 held. It no longer holds: the direction was ratified on the render (D-011). The reasoning stands and was vindicated — the two rejected options were *ratifying early* and *a written waiver*, and neither was taken. What actually happened is the third option the entry was holding out for: **the owner ratified late, on the finished artifact.** The build still does not start, but now for one reason only — blocker 15.

## D-011 · Hero direction RATIFIED — `direction_locked` flipped TRUE — `LOCKED`

**Decision:** the owner has **ratified the hero**. **Concept A — "The Climb"** is the final hero treatment, and `visual-direction.md` §6 `ASSET-INTAKE.direction_locked` moves **`false` → `true`** on the strength of this ratification and nothing else.

**Owner, verbatim:** *"ratify the hero, lock it in"*
**Date:** 2026-08-13

**What was ratified — the artifact, not a description of one.** The owner ruled after seeing the finished animation, not a still and not a blockout: **`_spec/visual-refs/hero-concept-A-climb-1080.mp4`**. Measured from the file itself this pass rather than carried from the render pass's report: **1920×1080**, **88 frames at 24 fps** (3.667 s), H.264, 704,896 bytes, written 2026-08-13 01:20. *Recorded as reported and NOT independently verified: the 48-sample and raytracing render settings. Those are Blender-side parameters, they are not recoverable from the container, and nothing in `_spec` records them — so they are stated as claimed, not as measured.*

**D-007's condition was met BEFORE the flag moved, and that is the whole point of this entry.** D-007 recorded the condition verbatim: *"do not lock it as I might want to update it as we go along, I want to see how this will be displayed in the hero section with actual animation before I finalize."* That condition is now **satisfied** — he has seen it animated, at final quality, in the treatment that ships. So flipping the flag **records a ratification that actually happened; it does not fabricate one.** D-009 exists because an earlier pass correctly refused to flip the flag while the condition was unmet. This entry is the event that pass was waiting for — **not a reversal of it, and not a relitigation of it.** The distinction between recording a real ratification and manufacturing a convenient one is the reason D-009 was written, and it is stated here so a later reader can check that the order of events was right: **render first, viewing second, ruling third, flag fourth.**

**What this unblocks.** The two gates that read the flag stop failing closed: `verify-handoff-complete.mjs` lines 98–100 (`direction_locked === true`) and the build's `verify-asset-intake.mjs`, which gates the first `_design/*.css` write. **D-009 is DISCHARGED** and `blocker_count` moves **2 → 1**.

**What this does NOT unblock — read this before treating the seam as open.**
- **`ready_for_build` stays `false`; the verdict stays NO-GO.** Blocker **15** — the counsel-supplied privacy policy — is now the **SOLE remaining gate**, and G7 requires `blocker_count === 0`. **No `HANDOFF-KICKOFF.json` has been written and the seam copy has not run.**
  - > **⚠ ANNOTATED 2026-08-13 — THE FIRST CLAUSE IS SUPERSEDED BY D-012; THE LAST SENTENCE IS NOT.** `ready_for_build` is now **`true`** and the verdict is **GO — for BUILD only** (`blocker_count` reached `0`). **That is not because blocker 15 closed.** The owner waived it **for BUILD only** — *"use lorem ipsum for now for the privacy policy, it is still being finalized"* — so the privacy policy is **still missing**, the page ships an **interim notice**, and **the site must not launch with it.** The sentence about the seam **remains true as written**: no `HANDOFF-KICKOFF.json` has been written and the seam copy has not run. **This entry's identification of blocker 15 as the thing standing between the spec and a finished site was correct and is unchanged — only the gate it stands in front of moved, from BUILD to LAUNCH.**
- **The asset-supply window is NOT waived by this.** `ASSET-INTAKE.waived` stays **`false`** and `real_image_count` stays **15**. The logo vector (`.ai`/`.svg`/`.eps`) and real founder photography at print/retina resolution are **still owed**. A locked *direction* is not a supplied *asset*, and changing either flag would be a separate owner decision that this ratification is not.
- **No content rule, ban, claim perimeter or waiver disposition moves.** This is a lock flip and its paperwork. Blockers 5, 9, 12 and 13 remain **waived**, and every claim banned under them stays banned at the enforcement layer.

**⚠ A SCOPE LIMIT WORTH STATING, BECAUSE THE FLAG IS WIDER THAN THE RULING.** The owner ratified **the hero**. `direction_locked` is the C7 flag over the **whole visual direction**, so flipping it also releases the gate on `D-006` — the white-dominant ground with purple and gold accents — which **D-006 still records as `PROVISIONAL`, awaiting confirmation "against a rendered specimen" at the build's FEEL gate.** That confirmation has **not** happened and this entry does not manufacture it. **D-006 stays PROVISIONAL on its own terms.** What changed is mechanical, not evidential: the gate that would have forced the palette question before the first `_design/*.css` write is no longer armed, so the FEEL check on the palette now depends on someone actually running it rather than on a flag refusing to let the build start. **Recorded here so a later reader cannot mistake a hero ratification for a palette ratification.** `brand-visual-signature.json` still constrains the build regardless — `surface_dominance: "balanced"` and the preserved `dark-purple-chrome` / `dark-hero` signature moves mean no pass may strip the purple wholesale.

**Effect on the other two concepts.**
- **Concept C — "The Meter"** is retired **as a hero alternative**; the hero slot is settled. It was **not** ruled on as the recurring site-wide motif — D-007's other role for it — so that role stands untouched until someone rules on it.
- **Concept B — "The 1st Mark"** stays blocked on the missing logo vector, and can no longer displace A in the hero without a **new** owner decision. The vector landing in `_inbox/` reopens B as a *mark* treatment, not as the hero.

**Consequence for the build:** the hero ships per D-008's engineering constraint, which this ratification does not touch — a short seamless loop plus a poster frame, poster painting first so the animation can never be the LCP element, loop lazy-loaded after LCP, the still served to `prefers-reduced-motion`, a lighter variant or none on mobile, under a hard byte budget. **Ratifying the concept did not ratify shipping a 704 KB 3.7-second MP4 into the hero.** The 1080p render is the master the loop and poster are derived from, not the delivered asset.

## D-012 · Privacy policy ships an INTERIM NOTICE — blocker 15 WAIVED **FOR BUILD ONLY**, and **LAUNCH-BLOCKING** — `LOCKED`

**Decision:** the `privacy-policy` page ships, **for the BUILD and only for the BUILD**, as an **honest interim notice** rather than as a policy. Blocker 15 is **WAIVED**, which moves `blocker_count` **1 → 0**, `ready_for_build` **`false` → `true`** and the verdict **NO-GO → GO**. It is **not closed, not supplied, and not resolved.** It is recorded as **LAUNCH-BLOCKING**: **the site MUST NOT LAUNCH with the interim page.**

**Owner, verbatim:** *"use lorem ipsum for now for the privacy policy, it is still being finalized"*
**Date:** 2026-08-13 · **Owner's stated intent:** unblock the BUILD with a placeholder. The real counsel-supplied policy lands before LAUNCH.

**⚠ THE ONE SENTENCE THIS ENTRY EXISTS TO MAKE IMPOSSIBLE TO MISREAD.** **`ready_for_build: true` means the BUILD may start. It does NOT mean the site may launch.** Those are two different gates, and as of this entry only the first one is green. `spec-manifest.json` now carries a top-level `launch_blockers` array for exactly this reason, and this page is the only thing in it.

### Why the page does not render literal lorem ipsum — a MECHANICAL fact, measured this pass, not a softening of the instruction

The build has its own gate against authoring debris. **Measured by reading the script this pass, not recalled:** `client-site-build/scripts/verify-no-ship-debris.mjs` line **24** carries `/lorem\s+ipsum/i` in its `DEBRIS` array and tests it against a page's **visible** copy; line **31** strips HTML comments *before* that test, with the in-file comment *"drop HTML comments (placeholders live here, OK)"*. The gate exits non-zero on a hit.

So the mechanics are exact and they cut one way only:

- **Placeholder filler inside an HTML comment is SANCTIONED** by that gate, by design.
- **Literal lorem ipsum in rendered text FAILS the build** — the very build this decision was given to unblock.

Rendering the instruction literally would therefore have produced the opposite of what the owner asked for. **The interim notice is not a downgrade of the instruction; it is the only executable form of it.**

### The second reason, which would stand even if the gate did not exist

A page of fake Latin under a **"Privacy Policy"** heading, footer-linked from **all 26 pages**, on a site that collects **six PII fields** through its consultation form and loads third-party cookie-setting embeds (YouTube across 17 videos, Google Maps, a Google reviews widget), **reads to a visitor or a regulator as a real policy.** That is worse than an honest "being finalised" notice, and it is the same failure class this ledger has caught repeatedly — a thing that *looks* like evidence standing where evidence has not arrived. The gate and the substance agree here, which is why this was not a close call.

### What actually renders in the meantime

Plain, true statements and nothing else: that the policy is **being finalised by counsel**, that the site is **not yet collecting under it**, and **where to direct data questions in the meantime** — the canonical NAP email, `support@seoguarantee.com`, per `fact-registry.json` → `D-NAP-CANONICAL` (status `OWNER-RULED`).

- **No fake legal text. No Latin. No sentence that makes any representation about how data is handled.**
- Any lorem-ipsum-style filler that must exist may exist **only inside HTML comments**, where the gate permits it and no reader sees it.
- The page carries **no legal sentence**, which is precisely why it is publishable — and precisely why the rule that produced it survives intact.

### What this does to the brief's own ship rule

`briefs/privacy-policy.md` §"HOW TO READ THIS BRIEF" (line 15) states that the page ships ONLY with owner- or counsel-supplied text, that the fabricated-fallback strategy of **D-002 DOES NOT EXTEND to legal text**, and that **no agent-authored legal sentence may ship.** That rule is **AMENDED BY THIS OWNER DECISION for the interim state only** — annotated in that brief, **not deleted**, because it is the entire reason the interim page must be replaced. **The amendment is narrow and the rule is otherwise untouched:** the interim notice ships *because* it asserts nothing about data handling. The moment a sentence on that page describes what the site does with data, the original rule binds again in full and only counsel may write it.

### What is still owed — five things, and prep can produce none of them

1. **Registered legal entity name** — the trading name is *First Page SEO Guarantee*; the registered controller's legal name is recorded nowhere in the spec.
2. **Processor list** — who actually receives the data.
3. **Retention period** — how long it is kept.
4. **The analytics / ad tags actually deployed** — measured from the live property, not assumed.
5. **The counsel-supplied policy text itself.**

Items 1–4 are the owner's to gather; item 5 is a lawyer's. **Nobody inside this project can produce any of them, and that has not changed by one word.**

### What this decision does NOT do — read before treating GO as permission to publish

- **It does not close blocker 15.** It is filed in `spec-manifest.json` → `waived{}`, **not** `closed{}`, carrying `launch_blocking: true`. The underlying need is **unmet**.
- **It does not make the page launch-ready.** The replacement is a **copy edit, not a rebuild** — the page structure, the footer link and the six section slots are already built to receive counsel's text.
- **It waives nothing else.** Blockers 5, 9, 12 and 13 stay waived on their 2026-08-12 terms, with every banned claim still banned at the enforcement layer. No ration widened, no `canonical_value` un-nulled.
- **It does not touch the asset window.** `ASSET-INTAKE.waived` stays `false` and `real_image_count` stays **15**. The logo vector and real founder photography are still owed.
- **It does not touch `direction_locked`**, which was already `true` on D-011's ratification and is unrelated to this.
- **It writes no `HANDOFF-KICKOFF.json` and runs no seam copy.** Those are separate actions and were deliberately not taken in the pass that recorded this.

### How this waiver differs from the other four, and why the distinction is load-bearing

Blockers 5, 9, 12 and 13 were waived as **permanent** dispositions: the owner elected to **ship without** that evidence, the copy those waivers produced is the **final** copy, and the site can launch in that state — thinner, but honest and complete. **Blocker 15 is not that.** This waiver is **temporary by the owner's own framing** — *"for now"*, *"it is still being finalized"* — and the artifact it authorises is explicitly an **interim** one. A waiver that clears a build gate while leaving a launch gate armed is a **new shape** in this ledger, and it is recorded as such so that no later pass reads five entries in `waived{}` and infers five decisions to ship without.

**Cost of this choice:** the build starts now instead of waiting on counsel, and the project takes on exactly one obligation — **replace the interim page before launch.** Rejected alternatives: rendering literal lorem ipsum (fails `verify-no-ship-debris.mjs:24` and misleads anyone who reads it), and holding the build until counsel delivers (the outcome the owner explicitly overrode).

---

## Open items (not decisions — dependencies)

| id | item | blocks | status |
|---|---|---|---|
| §G-6 | Claims substantiation — 3 verticals of "100% success rate", ~17 percentage tiles across 10 named clients, 4 press logos | P7 GO | **OPEN** — owner committed 2026-08-11; no material supplied to `_inbox/` |
| §G-8 | Canonical NAP | — | ✅ **CLOSED 2026-08-12** — owner ruled: 6905 W Charleston Blvd, Las Vegas, NV 89117, USA. Follow-up (outside the build): the live map embed and the Yelp listing still show a different street and must be corrected at source; confirm whether the directories' "#110" suite belongs. |
| §G-2 residual | Keyphrase count, search geography, measurement method and who verifies | P6 detail | OPEN — specificity only, not blocking |
| ASSET | Logo vector (`.ai`/`.svg`/`.eps`) | Concept B; crisp logo rendering | OPEN |
| ASSET | Real James Sutton photography at usable resolution | build P7.5 asset intake | OPEN — only web-res crops scraped |
| §G-13 | Founder story facts (`D-FOUNDER-*`) | — | ✅ **PARTLY CLOSED 2026-08-12** — owner supplied: James Sutton IV, **founder**, company started **2015**. `about` brief now written and passing G6. Three softer gaps remain (see below) — none blocking. |
| **LEGAL** | **Counsel-supplied privacy policy** + 4 owner inputs: registered legal entity name · processor list · retention period · the analytics/ad tags actually deployed | **LAUNCH** *(no longer BUILD)* | 🟠 **WAIVED FOR BUILD 2026-08-13, LAUNCH-BLOCKING — see D-012.** Blocker 15 left `blocker_count` without being supplied. The page ships an **honest interim notice**, not a policy and not Latin. **The site MUST NOT LAUNCH until counsel's text replaces it.** Replacement is a copy edit, not a rebuild. |

### §G-13 · Founder story — a gate is refusing to let me invent this

**What the gate does.** The `about` page is typed `T-COMPANY` with `company_variant: founder-led`. G6 (`verify-brief-complete`) requires such a brief to cite **at least one `D-FOUNDER-*` registry id**, with this rationale in the gate source: *"the founder story MUST be CAPTURED as facts, never a thin ⚠OWNER paraphrase… forces the founder facts to exist upstream (intake §H), not be invented at brief time."*

**Current state — verified 2026-08-11:** **zero `D-FOUNDER-*` ids exist anywhere in the spec.** Everything known about him is two fields scraped from the live site:

- **"James Sutton IV"**
- **"Managing Partner"**

**Correction to my own earlier wording:** I have been calling him *founder*. The live site says **Managing Partner**. Unverified whether he founded the firm — that assumption is withdrawn until the owner confirms.

The P0.0 audit already recorded that `/our-team/` is testimonial-led with **no company story and no founding year**, and that the origin narrative is missing entirely. So there is nothing to carry forward, and the gate is correctly refusing to let a plausible-sounding history be written about a real, named person.

**What is needed** (any subset makes the brief writable; all of it makes the page good):
- Is he the founder, a co-founder, or a later partner? What is his actual role?
- What year did the firm start, and who started it?
- Why the guarantee model specifically — what happened that led to charging only for the outcome?
- Background before this firm.
- Team size and where they work from.

**RESOLVED 2026-08-12.** The owner confirmed: **James Sutton IV is the founder** and **started the company in 2015**. Captured as `D-FOUNDER-JAMES-SUTTON`, `D-FOUNDER-FOUNDED` and `D-FOUNDER-PRESENCE` in `intake-brief.md` §H. The `about` brief is written and passes G6. My earlier withdrawal of the word "founder" is itself withdrawn — the owner outranks the live site's "Managing Partner" title, and in fact both hold.

**Still thin, not blocking** (`about` carries `⚠OWNER PLACEHOLDER` markers rather than inventing anything):
1. **Why the guarantee model exists** — the origin of the entire differentiator. Still the single highest-value sentence missing from the spec.
2. The founder's background before 2015.
3. Team size.
