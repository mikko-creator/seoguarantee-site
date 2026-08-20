# COPY - results

page_slug: results
type: T-INDEX
funnel_role: F4, the evidence page. Where a sceptical reader goes after the guarantee terms to check whether any of this has actually happened, in their trade, on a date they can read. It closes only after the reader has verified something.
primary_cta: CALL US -> contact-us (book a consultation)
section_count: 5 (the brief declares no numbered "Section count:" line and carries S1 to S5; the repeating result card is declared once as an item template which, in the brief's own words, "does not get a numbered section of its own, and it does not count toward the section window")
rendered_section_count: 6, measured 2026-08-18 by counting top-level <section> elements in pages/results.content.html with HTML comments masked so a commented-out block cannot count.
section_count_note: WHY THE TWO NUMBERS DIFFER, and why the 5 above is still true of this document. The copy still carries S1 to S5 and not a word of it was rewritten. The BUILT page renders SIX top-level sections, because S2 featured-pinned-case was split in two at build time to clear the G-DENSITY render gate, which fails a section running past 1.65 viewports with unbalanced columns. The split half ships as its own top-level section, id s2b-field, labelled "The field". A b suffix on a SECTION id marks the second half of a split. A b suffix on a HEADING id marks a copy section folded into another section. The two look alike and mean opposite things. The page is shipped and gate-green and must NOT be edited back to five. Maintained by hand: no gate compares a copy header against the rendered page, so a stale count here cannot be caught automatically.

locked_title: SEO Case Studies | Named Clients, Dates And Method
locked_meta: Client outcomes from campaigns run under the guarantee. Every result is named, dated and paired with the method that produced it. Filter by industry.

NOTES ON THE TWO LOCKED STRINGS. The brief carries the title only, from the seo-enrichment master table; the meta is taken from the same P5 row (`seo-enrichment.md` section 1, the SSOT), which the brief names as the deciding source. The title's separator is U+2013 (en dash) in the locked string and is transcribed here as a hyphen-minus, because an en dash cannot be written into `_copy/*.md` without `verify-no-dashes.mjs` blocking the write. Nothing else is changed. The brief's `title_conflict_to_reconcile` and its `reconcile_upstream` note both stand: sitemap.yaml carries a different title for this slug and declares a single filter field, and both must be updated to this brief.

LAUNCH STATE, and the reason this page reads the way it does. No client permission is on file, no measurement tool is recorded against any historical result, and the one live case card that came closest to complete describes its client's trade incorrectly. So the grid launches empty. The page is written to be worth reading in that state, because the alternative is publishing a claim we cannot stand behind on the one page whose entire job is standing behind claims.

---

## S1 hero-filter

<!-- src: D-OFFER-003, D-POSITION-W2, D-BRAND-RAILS-009 -->

**H1.** Results, with the dates and the method attached.

**The framing line, and the most important sentence on this page.** Every result below carries the months it covers, the method that produced it, the tool it was measured in, and written client permission. Anything that cannot carry all four is not published here.

That rule is the reason this page is short. It is also the reason it is worth reading: first page on the key phrases named in your contract, or you don't pay, is a claim that only means something if the evidence behind it can be dated. Any month we are off target we keep working and your billing stops. The full terms are on the guarantee page.

**Toolbar.** Three controls: **category**, the trade. **Tags**, the service mix that actually ran. **Date**, sorting by campaign end month, most recent first. A filter value with nothing behind it does not appear at all.

**Primary CTA.** CALL US. `tel:+1 (702) 420-7272`

---

## Item template: the repeating result card

This block is declared once and is deliberately not numbered. It is the shape every card takes, and it does not count toward this page's section total.

<!-- src: D-OFFER-020, D-BRAND-RAILS-013 -->

Every card carries all of the following, and the card does not render if any of the last three is missing.

- The client's name, published only with written permission on file.
- **category**, the trade: one of the five site verticals, or a genuine other.
- **tags**, the service mix that actually ran on the account.
- **date**, the campaign end month, which is the field the sort orders on.
- The start month and the end month, stated as a range rather than as a duration.
- The key phrase or phrases that moved, and the geography they moved in.
- The method: a paragraph in plain language describing what was actually done.
- The tool the position or the metric was read in.
- A visible "Published with permission" flag.

**Card hierarchy.** The named phrase and its page movement lead the card. Any permissioned metric that carries a period and a tool sits underneath as supporting detail. This is the reverse of the current site, where the number leads and the phrase is buried, and the reversal is deliberate: the phrase and its movement are the stronger evidence, and they are the shape the guarantee is actually written against.

**A card missing the date range, the method or the permission is held back.** Not softened, not paraphrased into something vaguer, not shipped with the missing field quietly dropped. This is the one instruction on this page that must not be relaxed to fill a grid.

[OWNER PLACEHOLDER] Any card standing in the layout before real material lands is marked representative on its face and carries no real client's name.

---

## S2 featured-pinned-case

<!-- src: D-MARKET-001-PROOF, D-POSITION-W1 -->

**Heading.** The pinned case, and how it gets chosen.

**The selection rule, stated on the page because the rule is itself a trust signal.** The case pinned at the top of this grid is the most completely evidenced one, not the one with the biggest number. You should assume a featured case is the flattering one, and on this page it is not chosen that way.

The frame that makes a pin worth anything: the metric shown is the one that was named in the contract before the work started. That is the whole difference between a result and a screenshot. Here is the month it was agreed, here is the month it was reached, and here is what was done in between.

[OWNER PLACEHOLDER] **The pin is currently empty, and this is why.** The strongest candidate from the existing material carries a hire month and year, a stated duration, a named key phrase, a geography and a page movement, which is closer to complete than anything else on record. It still lacks the measurement tool and written permission from the client, and a pinned case missing either of those would break the rule stated one paragraph above on the first card a reader sees. It ships the moment both land.

---

## S3 how-a-result-is-measured-and-permissioned

<!-- src: D-OFFER-023, D-BRAND-RAILS-008, D-INCUMBENT-001-OBJECTION, D-MARKET-002 -->

**Heading.** How a result gets measured, and how it gets permission.

Four things, plainly.

**1. What is measured, and in what.** First page means page one of Google organic results for an agreed key phrase in an agreed geography. Every position published here is read in a named tool, and the tool is named on the card rather than described in general terms. [OWNER PLACEHOLDER] The tool used for each historical result is not on record and is not guessed; it is supplied per result or the result does not publish.

**2. Permission.** Every named client gave written permission to be named. Where permission is not on file the outcome is not published, and that holds even when the outcome is a good one. This costs us cards, and it is the correct trade.

**3. Individual results vary.** Nothing on this page predicts what will happen for a different business, in a different market, against a different set of competitors. A result is a record of one engagement, not a forecast for yours.

**4. We publish no overall figure for how often campaigns reach first page.** We are saying that rather than quietly leaving it out, because the omission is more persuasive stated. The published case against services like this one is that the seller is vague and unfalsifiable, and the honest answer is not a better-sounding number. It is a page where every individual claim carries a date, a method, a tool and a permission, and no aggregate is offered on top of them.

The same standard applies backwards. Where a historical result cannot be evidenced to this level, it is not published in a softer form. It is simply not published, and this section is where we say so rather than let an absence look like modesty.

Two claim families that appear on the current site are not carried forward here in any form: an absolute rate of success in any vertical, and any claim about the sales a prospect will make. Neither is substantiated, and neither belongs on an evidence page.

---

## S4 category-routing

<!-- src: D-IA-TIER3, D-IA-TIER1 -->

**Heading.** By trade.

- SEO for dental practices
- SEO for law firms
- SEO for medical spas
- SEO for HVAC businesses
- SEO for contracting businesses

These five tiles always render, because the five trade pages always exist. They are routes, not counts of anything, and they never claim a number of cases behind them.

The category filter above works differently on purpose: a value appears there only when at least one permissioned, dated, method-stated case sits behind it.

Back to **the guarantee** for the terms, or to **Full Suite** for what the one agreed monthly fee covers.

---

## S5 closing-cta

<!-- src: D-OFFER-006, D-OFFER-013, D-BRAND-RAILS-009 -->

We will show you the equivalent of this page for your own trade on the call: the phrases your competitors currently hold in your market, and what it would take to take them. That is a real part of the competitive review, which is why we can offer it plainly.

**CALL US.** `tel:+1 (702) 420-7272`
