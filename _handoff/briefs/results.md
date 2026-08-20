# BRIEF — results

type: T-INDEX
funnel_role: F4 — the evidence page. It is where a sceptical reader goes after the guarantee terms to check whether any of this has actually happened, in their trade, on a date they can read. It carries the site's entire proof load and closes only after the reader has verified something.
primary_cta: CALL US -> contact-us (book a consultation)
links_to: guarantee, full-suite, industries, industries-dental, industries-law-firm, industries-medical-spa, industries-hvac, industries-contracting, contact-us
filter_fields: category, tags, date
sort: date, most recent campaign end month first
filter_field_mapping: category -> data-cat (the trade) · tags -> data-tags (the service mix that ran) · date -> data-date (campaign end month, YYYY-MM)
reconcile_upstream: sitemap.yaml line 88 declares filter_fields: [vertical] for this slug. That single field is wrong twice over — it under-declares the toolbar and it uses a name the build engine does not bind. This brief is the authority: vertical becomes category, the service mix becomes tags, and the campaign end month becomes date because the toolbar offers date-ordering. sitemap.yaml must be updated to match.

page_title (from seo-enrichment master table): "SEO Case Studies – Named Clients, Dates And Method" · primary keyword "SEO case studies" · intent commercial.
title_conflict_to_reconcile: sitemap.yaml carries "Results | Named Client Outcomes With Dates And Method". The seo-enrichment row is the P5 decision and wins.

## Outcome

FEATURE -> DO -> MEANS: FEATURE: every published client outcome carries its date range, the method that produced it, the tool it was measured in, and written permission on file -> DO: check a named result in your own trade, and check when it happened, before you ever speak to us -> MEANS: you are judging the guarantee on evidence you can date and verify rather than on a percentage tile with no period attached.

## §1 hero-filter — XS

Slim title hero, then the filter toolbar. No animation, no marquee treatment — this page earns attention by being checkable, and a hero that performs undercuts that.

One line of framing above the toolbar, and it is the most important sentence on the page: every result below carries the months it covers, the method that produced it, the tool it was measured in, and written client permission. Anything that cannot carry all four is not published here.

If the offer is restated in the hero at all, the payment condition travels with it in the same breath. Do not restate the full mechanic — that is the guarantee page's job, and this page routes there.

Toolbar renders three controls: category (the trade), tags (the service mix that ran), and a date sort. A filter value that has zero qualifying items does not render at all — an empty state on a proof page reads as an absence of proof.

Required data: D-OFFER-003, D-POSITION-W2, D-BRAND-RAILS-009

## Item template — the repeating result card (uncounted, deliberately carries no section number)

This is the repeating item template. It is declared once, it does not get a numbered section of its own, and it does not count toward the section window. The build binds the toolbar to these per-item fields.

Declared field set per card, all of it required:
- client name (only with written permission on file)
- data-cat — the trade, one of the five site verticals or a genuine "other"
- data-tags — the service mix that actually ran on the account
- data-date — campaign end month, YYYY-MM, the field the sort orders on
- start and end month, stated as a range, not a duration alone
- the named key phrase or phrases that moved, and the geography they moved in
- the method paragraph: what was actually done, in plain language
- the measurement tool the position or metric was read in
- "Published with permission" flag, visible on the card

Hard rendering rule: a card missing ANY of date range, method, or permission does not render. It is held back, not softened, not paraphrased into vagueness, not shipped with the missing field quietly dropped. That rule is what makes the whole page worth reading, and it is the one instruction on this page a builder must not soften to fill a grid.

Card hierarchy: the named phrase and its page movement LEAD the card. The percentage, if there is a permissioned one with a period and a tool, sits underneath as supporting detail. This inverts the live site, where the tile leads and the phrase is buried — the phrase-plus-movement shape is far stronger evidence and it is the shape the guarantee is actually written against.

Under the fabricated-fallback proof strategy, representative cards may stand in so the layout can be built and reviewed, but every representative card ships visibly marked as representative and none of them may carry a real client's name.

Required data: D-OFFER-020, D-BRAND-RAILS-013

## §2 featured-pinned-case — S

ONE pinned case at the top of the grid, chosen because it is the most COMPLETELY EVIDENCED, not because it has the biggest number. Say that selection rule on the page in one line — it is itself a trust signal, and it pre-empts the reader's assumption that the featured case is the flattering one.

It must carry all four required fields plus the phrase and the geography. Model the structure on the strongest competitor proof pattern in the research: named client, paired metric, and a paragraph explaining what was actually done to produce it. Reject that same competitor's aggregate mega-number habit entirely — no site-wide conversion counters, no revenue totals, no "campaigns run" tallies.

The frame that makes the pin work: the metric shown is the one that was NAMED IN THE CONTRACT before the work started. That is what separates a result from a screenshot. Write it explicitly — this was the agreed metric, here is the month it was agreed, here is the month it was reached.

Recommended pin from verified live material, subject to permission: Lifetime Dental Rancho. The live portfolio copy carries a hire month and year, a stated duration, a named key phrase, a geography, and a page movement — the only card on the site that comes close to complete. It still needs the measurement tool and written permission before it ships.

Second candidate: Advanced Dental Wellness, which carries a hire month and year and two named phrases. Katy Dental Experts carries a strong page movement on named phrases but its hire month has NO YEAR attached — it is dated by the owner or it is dropped, never guessed.

Required data: D-MARKET-001-PROOF, D-POSITION-W1

## §3 how-a-result-is-measured-and-permissioned — M

The honesty block, and the section that makes this page publishable at all. It is placed after the featured case and before the routing so a reader hits it while still reading evidence, not as a footnote.

It states four things plainly:
1. How a result is measured — what "first page" means here (page one of Google organic results for an agreed key phrase in an agreed geography), and in what tool the position was read.
2. That every named client gave written permission to be named, and that anything without permission is not published even when the result is good.
3. That individual results vary, and that nothing on this page is a prediction about a different business in a different market.
4. That we do not publish a success rate. Say it, do not just omit it — the absence is more persuasive stated than hidden, and it is the direct answer to the category's published attack that guarantee sellers are vague and unfalsifiable.

This section is also where the open claims-substantiation perimeter is disclosed rather than dodged. Where a historical result cannot yet be evidenced to this standard, the page says so in general terms rather than publishing the claim and hoping.

Explicitly bans, on this page and in this voice: any absolute success rate in any vertical, and any earnings-style claim about what a prospect will make. Both are live on the current site and both are unsubstantiated.

Required data: D-OFFER-023, D-BRAND-RAILS-008, D-INCUMBENT-001-OBJECTION, D-MARKET-002

## §4 category-routing — XS

Routes to the five vertical leaves — dental, law firm, medical spa, HVAC, contracting — and back to the guarantee terms and to full-suite for what is included.

Two separate mechanics that must not be confused in the build:
- The five ROUTING tiles always render, because the five vertical pages always exist. A tile says "SEO for dental practices", not "5 dental case studies".
- The category FILTER only exposes a value when at least one permissioned, dated, method-stated case exists behind it. A filter value with zero items never renders.

Taxonomy warning, verified against the live portfolio: the current live taxonomy is Dispensary, Law, Medical, Construction and Other across 20 items. That does NOT match the site's five verticals and must be RE-DERIVED, not carried over. Mapping the old values across mechanically will produce a dental filter populated by "Medical" items and a contracting filter populated by "Construction" items that may be neither. Each item is re-categorised by reading it.

Required data: D-IA-TIER3, D-IA-TIER1

## §5 closing-cta — XS

CALL US to a booked consultation. One primary action.

One line before it, and only one: an offer to show the equivalent evidence for the reader's own trade on the call — the phrases their competitors currently hold, and what it would take to take them. That is a real thing we do in a competitive review, so it can be said plainly. It is not a named free product and must not be branded as one.

No second CTA, no newsletter, no gated download. The live site's five-way CTA split is what this page eliminates.

Required data: D-OFFER-006, D-OFFER-013, D-BRAND-RAILS-009

## Claims and constraints

The governing HOLDS row for this page is the bare percentage tile: approximately 17 distinct tiles across 10 named clients — Advanced Dental Wellness, All American Law Firm, Juvly Aesthetics, Katy Dental Experts, Lifetime Dental Rancho, RAICH Law PLLC, SOUTHWEST Injury Law, Serenity Med Spa, Setiba Medical Spa and The Blez, plus DDM Garage Doors and Liquor License Agents on the homepage. Every one of them is unsubstantiated as written. The ONLY safe form is: "[Client] — [metric] +[x]% between [start] and [end], measured in [tool]. Published with permission."

Other binding rows:
- "100% success rate" in any vertical, and "Average Campaign yields 30% - 100% increase in sales" — unsubstantiated, and may not appear in any aggregate strip on this page.
- The All American Law Firm card is NOT REUSABLE AS WRITTEN. The live copy describes a law firm as "a roofing company based out of the Dallas-Fort Worth area" and carries two unflagged tiles. Held back until corrected and permissioned.
- The republished Otto B. review asserting a number-one ranking is not republished anywhere on this page.
- No press logo wall.
- Any headline framing of the guarantee carries the payment condition in the same breath.
- No "best" and no "#1". The only permitted self-rating line anywhere is "Rated 4.9 from 35 Google reviews" stated with its count.

Must NOT be said:
- Any percentage, multiple or count without its time period and its source. Hard rule, no exceptions on this page of all pages.
- Any aggregate mega-number in the competitor style — a billion-dollar revenue counter or a site-wide conversions total. Explicit do-not-copy in both competitor dossiers, and unbackable here.
- Any client name without written permission on file.
- "Guaranteed #1", or any implication that Google endorses ranking guarantees.
- Refund, money-back, risk-free, or "there is no invoice". Billing pauses and resumes; the work continues.
- Any price, band or "starting at".
- Any exclamation mark. Any emoji.

Owner-pending before this page can ship:
- Written permission from each named client, on file.
- The measurement tool for each published result.
- A year for the Katy Dental Experts hire month.
- The corrected All American Law Firm copy.
- The re-derived category value for each of the 20 merged portfolio items.

Reversibility note carried forward: the 20 individual portfolio item URLs merge into this page but the merge is reversible. If permissions and campaign data arrive in volume, the items can be restored at their original slugs without unwinding anything specified here.

Spec integrity note: positioning-plan.md on disk is Rev 2, while page-inventory.md and seo-enrichment.md both cite "positioning-plan.md Rev 3". No Rev 3 exists in _spec. The wedges relied on here are present in Rev 2, but the citation mismatch should be reconciled before owner sign-off.
