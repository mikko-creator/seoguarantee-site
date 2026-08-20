# BRIEF — privacy-policy
type: T-LEGAL
legal_variant: trust
funnel_role: Compliance and trust support for the lead-capture forms. Footer-linked from every page and linked adjacent to the form on contact-us. It has no conversion role, carries no offer content, and is the one page on the site where the brand deliberately says nothing about itself.
primary_cta: none on-page — no CALL US band and no offer language. The only contact route is the plain privacy-contact line in §6.
links_to: contact-us, index
title: Privacy Policy – Interim Notice While Counsel Finalises
meta_description: Our privacy policy is being finalised by counsel. The site is not yet collecting under it. Data questions in the meantime go to support@seoguarantee.com.
primary_keyword: privacy policy (informational intent)

<!-- MACHINE BLOCK RECONCILED TO THE §1 SSOT on 2026-08-13 (owner decision D-012), by the QC-016
     reconciliation pass. This settles the debt this brief itself recorded below under "Flagged, and
     owed OUTSIDE this file" — that note said the mismatch was owed to whoever owns the SSOT
     artifacts. `seo-enrichment.md` §1 and `sitemap.yaml` have now both been reconciled to the
     interim strings, which left THIS machine block as the last place on disk still publishing the
     launch strings. Leaving it would have kept a live path to emitting the one string D-012 forbids,
     if the build reads per-page meta from the brief rather than from §1.

     SUPERSEDED LAUNCH STRINGS — PRESERVED VERBATIM, NOT DELETED. These are the RESTORE TARGET and
     must go back when counsel's text lands (the replacement is a copy edit, not a rebuild):
       title:            "Privacy Policy – How First Page SEO Guarantee Uses Data"   (55 chars)
       meta_description: "How First Page SEO Guarantee collects, uses, stores and shares the
                          information you submit through our contact and consultation forms."

     Why they could not stay live: both describe how data is handled and promise a policy the interim
     page does not contain. D-012 is explicit — "No sentence that makes any representation about how
     data is handled." The interim strings above carry only D-012's three sanctioned statements.
     Identical, byte for byte, to `seo-enrichment.md` §1 and `sitemap.yaml` (title 55, meta 153).

     UNCHANGED by this edit: type, legal_variant, funnel_role, primary_cta, links_to, primary_keyword,
     the six section slots, the footer link, and blocker 15's status — still WAIVED-not-closed and
     LAUNCH-BLOCKING. The noindex question below stays OPEN and is still a build decision, not ruled
     on here; D-012 rules on copy, not robots. -->


## ⚠ INTERIM — THIS PAGE IS NOT LAUNCH-READY. READ THIS BEFORE ANYTHING ELSE.

**Added 2026-08-13 by owner decision D-012. Nothing below this banner was deleted; the pre-existing brief is intact and annotated in place.**

The owner, verbatim: *"use lorem ipsum for now for the privacy policy, it is still being finalised"*.

The intent is to unblock the BUILD with a placeholder. The counsel-supplied policy lands before LAUNCH. What ships in the meantime is an **honest interim notice** — not fake legal text, and not Latin.

**Why the instruction is implemented as a notice rather than literally.** Two reasons, and the mechanical one is decisive.

1. Mechanical. `client-site-build/scripts/verify-no-ship-debris.mjs:24` tests `/lorem\s+ipsum/i` against the page's **visible** copy and fails the build closed. Line 31 strips HTML comments *before* that scan, so the phrase is sanctioned inside an HTML comment and forbidden in rendered text. Literal Latin in the rendered page would stop the very build this decision exists to unblock.
2. Substantive. A page of fake Latin under a "Privacy Policy" heading, footer-linked from all 26 pages of a site that collects six PII fields through its lead form, reads to a visitor — or to a regulator — as a real policy. That is worse than an honest "being finalised" notice. The interim notice is **not a downgrade of the owner's instruction**; it is the only version of it that can pass the build.

**Status of this page in three lines.**
- It is NOT launch-ready. It must be replaced before launch. There is no version of "ship it as-is" that is acceptable.
- The replacement is a **copy edit, not a rebuild** — same page, same TYPE, same document layout, same footer link, same route. Counsel's text drops into the six slots below and the interim notice comes out whole.
- Blocker 15 is **WAIVED FOR BUILD ONLY** by D-012. It is not closed and not fixed. It is LAUNCH-BLOCKING, and the four facts plus the policy text listed at the foot of this brief are still owed.

### The rendered interim notice — VERBATIM. This is the copy that ships.

Every line below is true, plainly stated, and asserts no legal position. It carries no ⚠ marker, no bracketed slot, no Latin, and no exclamation mark, so it clears the debris gate and the owner's rails. Build it as prose in the legal document measure — no card stack, no icon, no image, no hero, per `verify-legal-is-document.mjs` (P1 requires the `.bw-legal` prose measure; P2 forbids an `<img>` in the body). If the notice is set apart visually, set it apart with type and space, never with a decorated callout.

```text
Privacy Policy

This page is not the policy yet.

First Page SEO Guarantee is having its privacy policy written by counsel.
Until that text is published here, no privacy policy is in force on this
site, and nothing on this page should be read as one. This notice carries
no effective date, because it is not the document that will replace it.

What the forms on this site collect

The consultation form asks for six things: your name, your email address,
your phone number, whether you currently have a website, your website
address, and what you are interested in. That is the list of fields you can
see and fill in.

What this notice does not tell you

It does not tell you how long that information is kept, who else it is
shared with, or which analytics and advertising services run on this site.
Those belong in the finished policy, and they are left out here rather than
guessed at. The finished policy will state them.

Third-party content on this site

Some pages load content from other companies: YouTube video players on the
videos page, a Google Maps embed on the contact page, and a Google reviews
rating widget. Those companies can set cookies in your browser when that
content loads or plays. This covers embedded content only. It is not a list
of the analytics or advertising services this site runs, which is one of the
things the finished policy will set out.

Questions about your information

Write to support@seoguarantee.com, or to First Page SEO Guarantee,
6905 W Charleston Blvd, Las Vegas, NV 89117, USA. Use that route whether you
want to ask what has been recorded about you, correct it, or have it removed.
The finished policy will name the legal entity responsible and give the same
route.

This notice will be replaced by the full privacy policy. If you are reading
it, the policy is not finished.
```

**Copy rules the build may not relax.** No sentence may be added to soften it, no heading may be reworded to imply a policy exists, the h1 stays "Privacy Policy" so the footer link's destination is unambiguous, and the line "This page is not the policy yet." sits immediately beneath it at no less than body size — the page must read correctly in a screenshot, not only to someone who scrolls.

### Where the owner's word "lorem ipsum" is allowed to live

Inside an HTML comment at the top of the page body, and nowhere else. This comment is the audit trail; the debris gate strips comments before scanning, so it ships safely. Embed it byte-for-byte:

```html
<!-- INTERIM PRIVACY NOTICE — owner decision D-012, 2026-08-13.
     Owner, verbatim: "use lorem ipsum for now for the privacy policy, it is still being finalised".
     Implemented as an honest interim notice, not literally. verify-no-ship-debris.mjs:24 tests
     /lorem\s+ipsum/i against VISIBLE copy and fails the build; line 31 strips HTML comments first,
     so the phrase is legal here and illegal in rendered text.
     LAUNCH-BLOCKING: replace this whole page body with the counsel-supplied policy before launch.
     Owed with it: registered legal entity name, processor list, retention period, and the
     analytics/advertising tags actually deployed. -->
```

### One thing this pass does NOT do, deliberately

It does not declare `legal_draft: competitor-referenced` on this brief, and no one should add it. That mode exists for an adapted best-effort **draft policy body** shipped behind the "DRAFT / NEEDS LEGAL REVIEW" banner. This page carries no draft policy body at all — it carries a notice saying there is none — so that banner would assert something untrue in the other direction. Default mode stays.

### Flagged, and owed OUTSIDE this file — not fixed here

The `meta_description` in the machine block above describes the finished policy ("collects, uses, stores and shares…"). It is accurate for the page that replaces this one and inaccurate for the interim page. Two consequences, both unresolved as of this pass and neither of them mine to close in this file:
- The interim page should carry `noindex` so that inaccurate snippet never reaches a SERP, and the directive comes off when counsel's text lands. **Unverified whether the build honours a per-page robots directive** — that is a build-side question, not a prep assertion.
- If the page is indexed anyway, the mismatch is recorded here rather than left to be discovered. `sitemap.yaml` and `seo-enrichment.md` are owned elsewhere; reconciling them to an interim/noindex state is owed to whoever owns them.

> **⚠ THE META HALF OF THIS NOTE IS NOW SETTLED — 2026-08-13, QC-016 reconciliation pass. Nothing above is retracted; it was correct when written and it is the reason the debt got paid.** The three artifacts named here have been reconciled to the interim strings and now agree byte for byte: `seo-enrichment.md` §1 (the declared SSOT), `sitemap.yaml` (re-propagated from §1 per its own header rule), and **this brief's own machine block**, which was the last place on disk still publishing the launch strings. The superseded launch title and meta are preserved verbatim as the restore target in the comment beside the machine block — so the "accurate for the page that replaces this one" point this note makes is kept, not lost.
>
> **The `noindex` half is NOT settled and stays open.** Whether the interim page carries a robots directive remains a build-side decision, and whether the build honours a per-page directive remains **unverified**. D-012 ruled on copy, not on robots, and this pass did not manufacture a ruling it was not given.

## Outcome
FEATURE -> DO -> MEANS: FEATURE: a plain-language policy that names the exact six fields the consultation form collects, the third parties embedded on the site, and who to contact to have the data deleted -> DO: see what filling in a lead form actually costs you, before you fill one in -> MEANS: the lead capture is disclosed rather than assumed, which is the minimum standard for a firm whose entire position is that its terms are written down in advance.

## HOW TO READ THIS BRIEF — the ship rule
This page ships ONLY with owner- or counsel-supplied text. The site's fallback proof strategy — real first, clearly-swappable representative content where real content is missing — DOES NOT EXTEND TO LEGAL TEXT. Representative privacy copy is a liability rather than a placeholder, because a policy that misdescribes actual data handling is worse than having no policy at all. No agent-authored legal sentence may ship.

The six sections below are therefore SLOTS the owner or counsel fills. What this brief contributes is the verified inventory of what the site genuinely collects and loads, which is exactly what counsel needs and what prep can supply honestly. Each section states the inventory as input, and marks the policy language itself as owner-supplied.

Net-new confirmed: none of the 138 live URLs contains "privacy" or "terms". There is no existing policy to carry forward and nothing to diff against.

> **⚠ AMENDED 2026-08-13 BY OWNER DECISION D-012 — for the INTERIM STATE ONLY. The rule above is preserved verbatim and is NOT retracted; it is the reason the interim page must be replaced.**
>
> What the owner amended: the page may now ship **before** counsel's text exists. What the owner did **not** amend, and what still binds every word on the page: **no agent-authored legal sentence ships.** The interim notice is consistent with the original rule rather than an exception to it, because it contains no legal sentence — it makes no representation about purpose, sharing, retention, lawful basis or compliance. It states three kinds of fact only: (a) that the policy does not exist yet, (b) the verified inventory of what the forms collect and what the page loads, and (c) where to write. Every one of those is a fact prep verified, not a position prep took.
>
> The distinction to hold on to: *representative privacy copy* — the thing the rule bans — is copy that **stands in for** a policy and is read as one. The interim notice **refuses to stand in for** the policy and says so in its first line. That is why it can ship and Latin cannot.
>
> This amendment expires the moment counsel's text arrives. It grants nothing else and extends to no other page.

## §1 policy header and effective date — S
OWNER-SUPPLIED. Slot for the policy title, the legal entity name the policy is issued under, and the effective date.

Inventory this brief supplies: the trading name is First Page SEO Guarantee. ⚠OWNER — the registered legal entity name is not recorded anywhere in the spec and must be supplied; a trading name is not necessarily the controller's legal name, and guessing one is exactly the failure mode this page must avoid.

Do not date the policy with a date the owner has not approved. An effective date that predates the page going live is a false statement on its face.

Presentation rule for the whole page: plain, legible, generously spaced body text with a clear heading hierarchy and a readable measure. The "trust" treatment means the owner's text is presented so it can actually be read — it does not mean the agency writes reassuring language around it.

**INTERIM (D-012).** *When counsel supplies it:* the policy title, the registered legal entity name, and an owner-approved effective date. *What renders in the meantime:* the h1 "Privacy Policy", then the line "This page is not the policy yet.", then the paragraph naming counsel as the author of the pending text. **No effective date and no legal entity name appear**, and the notice says explicitly that it carries no effective date — which converts the two missing facts from silent omissions into stated ones. The ⚠OWNER above is unchanged and still outstanding.

Required data: D-OFFER-001, D-BRAND-RAILS-006

## §2 what we collect — M
OWNER-SUPPLIED policy language. Verified inventory supplied by prep, extracted from the live form markup — these are the six fields the consultation form actually collects, and the policy must cover exactly these:

1. Name.
2. Email address.
3. Phone number.
4. Whether you currently have a website.
5. Website address.
6. What you are interested in.

Also to be covered, and to be confirmed by the owner rather than assumed by prep: anything the hosting stack or forms plugin records incidentally alongside a submission, such as IP address, timestamp, browser user agent or referring page. Prep can confirm the visible field set from the markup; it cannot confirm what the form processor stores behind it, and must not assert it either way.

**INTERIM (D-012).** *When counsel supplies it:* the collection clause, covering the six fields plus whatever the stack records incidentally. *What renders in the meantime:* the six fields, listed in prose, under the heading "What the forms on this site collect" — the one section of the interim notice that is genuinely informative, because it is the one thing prep verified from markup rather than inferred. The interim copy closes that paragraph with "That is the list of fields you can see and fill in", which is the honest boundary of what prep checked: it does **not** claim the six fields are everything recorded. The incidental-capture question stays open and is named as owed in the finished policy.

Required data: D-BRAND-RAILS-016, D-OFFER-009

## §3 how we use it and who we share it with — M
OWNER-SUPPLIED policy language. The honest purpose statement is narrow and the owner should be able to confirm it in a sentence: the information submitted through the form is used to contact the person who submitted it in order to arrange and hold a consultation, and to prepare for that conversation.

⚠OWNER — the processor list. Name only processors the owner confirms in writing. Prep does not know the email, CRM, hosting or analytics vendors in use and will not guess them.

One correction prep can supply with certainty: the client portal must NOT be described as a live destination for client data. That URL is being retired in this release with no replacement, and describing a retired system as active would misdescribe the data flow on the first day the policy is published.

**INTERIM (D-012).** *When counsel supplies it:* the purpose statement and the named processor list. *What renders in the meantime:* **nothing affirmative — by design.** This is the section the interim notice deliberately declines to fill, under the heading "What this notice does not tell you". The purpose sentence above is plausible and prep believes it, but the owner has not confirmed it in writing, and an unconfirmed purpose statement on a live page is precisely the misdescription the ship rule forbids. Sharing is named as unanswered rather than answered. The ⚠OWNER on the processor list is unchanged. The retired client portal is not mentioned at all, which satisfies the correction above by omission and needs no interim wording.

Required data: D-OFFER-006, D-OFFER-019

## §4 retention and your choices — M
OWNER-SUPPLIED policy language covering how long submissions are kept, and how a person asks for a copy of their data, a correction, or deletion.

⚠OWNER — retention period. No retention practice is recorded anywhere in the spec. This is a slot, not an inference; prep will not write "we keep it as long as necessary" as a stand-in, because that sentence is a legal position rather than a placeholder.

⚠COUNSEL — do not assert compliance with any regime, named or implied, unless counsel confirms it. No GDPR statement, no CCPA or CPRA statement, no "we are fully compliant" line, and no certification badge of any kind.

**INTERIM (D-012).** *When counsel supplies it:* the retention period and the formal rights-and-requests clause. *What renders in the meantime:* the retention period is named as **not stated** ("It does not tell you how long that information is kept"), and the "your choices" half is met not with a rights clause but with a **route**: the reader is told to write to the canonical address whether they want to ask what has been recorded, correct it, or have it removed. A route is a fact about where mail goes. A rights clause is a legal position. The interim page ships the first and not the second. **The ⚠COUNSEL rule above binds the interim copy exactly as written** — the notice names no regime, claims no compliance, and carries no badge; verify this by reading it, because a single reassuring clause added here would turn an honest notice into the fabricated policy this page exists to avoid.

Required data: D-OFFER-020, D-BRAND-RAILS-013

## §5 cookies, analytics and embedded third parties — M
OWNER-SUPPLIED policy language. Verified inventory supplied by prep — these are the third parties the rebuilt site will still load, and the policy must account for them:

- YouTube — 17 video embeds on the videos page. These set third-party cookies when a video is played, and the build should load them on click rather than on page load, which is both a performance and a disclosure improvement.
- Google Maps — an embed on contact-us. §G-8 closed 2026-08-12, so the embed is repointed to the canonical address, 6905 W Charleston Blvd, Las Vegas, NV 89117, USA, rather than withheld. If the embed is dropped from the build for any other reason, this line comes out of the policy rather than staying in as an aspiration.
- The Google reviews rating widget — on contact-us and las-vegas-seo.
- ⚠OWNER — analytics and advertising tags. Whatever the owner actually runs, named individually. Prep has not verified which tags are deployed and will not list a plausible set.

**INTERIM (D-012).** *When counsel supplies it:* the full cookie and third-party clause, including the deployed analytics and advertising tags named individually. *What renders in the meantime:* the three verified embeds, named — YouTube, Google Maps, the Google reviews widget — with the plain statement that those companies can set cookies when their content loads or plays. **The conditional in the Maps bullet above governs the interim notice too:** the notice names only what the built page actually ships, so if an embed is dropped from the build, its mention comes out of the notice in the same edit. The analytics and advertising tags are the ⚠OWNER gap, and the interim copy makes the gap explicit rather than silent — "This covers embedded content only. It is not a list of the analytics or advertising services this site runs." A reader is told what was not checked. That sentence is load-bearing and may not be cut for brevity.

Required data: D-OFFER-016, D-IA-TIER3

## §6 who to contact about your data — S
OWNER-SUPPLIED. The controller identity block and a single contact route for data questions. Plain text, no form, no CALL US band, no phone-first framing — this page's contact line exists for a legal purpose, not a commercial one.

The contact address for data questions, closed alongside the canonical NAP on 2026-08-12: **support@seoguarantee.com** (`intake-brief.md` §I, `content-bible.md`). It is printed here byte-identically to the footer and to contact-us. Prep no longer holds a placeholder for it — but the policy language wrapped around it is still owner- or counsel-supplied.

The controller's postal address, §G-8 closed 2026-08-12: **6905 W Charleston Blvd, Las Vegas, NV 89117, USA** — byte-identical to the footer, contact-us and about. The two contested addresses on record are wrong and neither may be printed. ⚠OWNER remains on the legal ENTITY the address is attributed to (see §1): the address is settled, the registered entity name is not, and a controller block naming the right address under a guessed entity is still a false statement on its face.

**INTERIM (D-012).** *When counsel supplies it:* the controller identity block — registered legal entity, address, and the formal data-request route. *What renders in the meantime:* the email and the postal address, both byte-identical to the footer, printed **under the trading name and explicitly NOT as a controller declaration.** This is the sharpest constraint in the interim notice and the easiest one to break by accident: printing the settled address under the words "data controller" would attribute controllership to an entity nobody has named, which is the §1 failure mode wearing §6's clothes. The interim copy therefore says "The finished policy will name the legal entity responsible" — the omission is stated, not hidden. No phone number appears, in keeping with the no-phone-first rule above, even though the canonical NAP carries one. The ⚠OWNER on the entity name is unchanged.

Required data: D-OFFER-024, D-BRAND-RAILS-004

## Claims and constraints

The rails still bind here, and they are the only thing prep enforces on this page.
- Zero exclamation marks. Zero emoji.
- Plain register, no reassurance copy wrapped around the owner's text, no trust-badge strip, no "your privacy matters to us" preamble authored by the agency.
- No agent-authored legal sentence ships. Every clause is owner- or counsel-supplied. **Unchanged by D-012** — the interim notice contains no legal sentence, which is the whole basis on which it is allowed to ship.

Must not appear on this page.
- The guarantee, in any form. No offer language, no "or you don't pay", no key-phrase framing, no CALL US band, no consultation pitch.
- Any price.
- Any compliance assertion (GDPR, CCPA, CPRA, any regime, any certification) unless counsel confirms it.
- Any processor the owner has not confirmed by name.
- The retired client portal described as a live data destination.
- Any street address other than the canonical one — 6905 W Charleston Blvd, Las Vegas, NV 89117, USA (§G-8, closed 2026-08-12).
- Any effective date the owner has not approved.
- **Added by D-012 — literal Latin filler in any rendered text.** It fails `verify-no-ship-debris.mjs:24` and would block the build the owner is unblocking. It is permitted inside an HTML comment only.
- **Added by D-012 — any wording that lets the interim notice be read as a policy.** No "we respect your privacy", no summary that implies a policy exists elsewhere, no "last updated" date, no rights list, no compliance badge.

Owner-pending on this page — all of it. In the order it is needed.
1. The registered legal entity name the policy is issued under.
2. The full policy text, from the owner or from counsel.
3. The processor list, named.
4. The retention period.
5. The analytics and advertising tags actually deployed.

**D-012, 2026-08-13 — none of the five above are closed. Every one of them is still owed, and all five are LAUNCH-BLOCKING.** What the decision changed is narrow and worth stating precisely: the BUILD may now proceed past this page instead of stopping at it. Blocker 15 is recorded as WAIVED for build purposes, not closed and not fixed — the underlying need is unmet, and the site MUST NOT LAUNCH with the interim notice standing where the policy belongs. Anyone reading a GO verdict downstream should read it as GO for BUILD, never as GO for LAUNCH.

Closed 2026-08-12, no longer pending on this page: the contact email address for data requests (support@seoguarantee.com) and the §G-8 canonical postal address for the controller block (6905 W Charleston Blvd, Las Vegas, NV 89117, USA). Both are printed in §6. Everything else above remains owner- or counsel-supplied, and the page still cannot ship without it. **Annotated 2026-08-13:** "cannot ship" was written when the only two outcomes on the table were counsel's text or an empty page. D-012 added a third — an interim notice that ships without pretending to be the policy. The sentence stands as the rule for the *policy*; it is the interim *notice* that ships in its place, and only until the policy arrives.

Title conflict resolved in favour of the P5 SEO row, "Privacy Policy – How First Page SEO Guarantee Uses Data"; sitemap.yaml carries "Privacy Policy | First Page SEO Guarantee" and must be reconciled to the SEO row.

Registry-trace note for the reviewer. The pre-derived structure cited ids from two per-page families — a per-page SEO-metadata family and a per-page slot family, including several privacy-specific slot ids. Verified 2026-08-11: neither family exists in any _spec artifact, so those ids are not cited here. The slots they named survive as the owner-supplied slots above; the SEO title, meta and primary keyword are printed literally in the machine block.
