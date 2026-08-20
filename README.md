# First Page SEO Guarantee . site source

The **source** for the seoguarantee preview build. Private, because `_handoff/` carries the client's
decisions ledger, content bible and fact registry.

Built output is a separate repository and is **not** tracked here:

| | where |
|---|---|
| live preview | https://mikko-creator.github.io/squah-previews/seoguarantee/ |
| published output | https://github.com/mikko-creator/squah-previews |
| source (this repo) | you are here |

## What is in here

| path | what it is |
|---|---|
| `pages/*.content.html` | the 26 page fragments. **This is the thing you edit.** |
| `pages/index.css`, `pages/guarantee.css` | the two per-page stylesheets |
| `_design/` | the shared sheet (`seoguarantee-structural.css`), tokens, chrome CSS, and `_chrome-block.html`, the locked chrome carrier |
| `_build/_template.html` | the assembled shell. Generated. Edit `_design/_chrome-block.html` instead, see below |
| `_handoff/` | the spec: sitemap, briefs, client rules, content bible, decisions ledger, SEO enrichment |
| `_copy/` | approved copy per page |
| `assets/` | imagery, including the original capture of the live estate |
| `_approvals.json`, `_images.json`, `_published.json`, `_receipts/` | build bookkeeping |

`pages/*.html` (the built pages) are gitignored. They are derived from the fragments plus `_design/`
and are republished in full in the output repo, so tracking them here would double the repository
and produce a large diff on every build for no information.

## Building

```
node ~/Oso/.claude/skills/client-site-build/scripts/build.mjs --site .
```

It assembles every fragment into the chrome shell, stamps each stylesheet link with an md5
cache-buster, and runs the render gates. It exits non-zero and writes nothing if a gate fails.

## Two things that will bite you

**Edit chrome at the carrier, never the template.** `_build/_template.html` is generated. A
PreToolUse gate blocks edits to the chrome region there for a reason: patching it fixes the one file
you are looking at and leaves the other 25 stale. The carrier is `_design/_chrome-block.html`.

**A stylesheet change is invisible until you rebuild.** Every page links
`structural.css?v=<md5>`, and only a build restamps that query. Editing the sheet without rebuilding
leaves returning visitors on the cached previous version.

## Client rules that are enforced, not stylistic

Set in `_handoff/client-rules.json` and checked by the gate battery:

- **No em dashes and no en dashes anywhere**, including inside HTML comments. They were also once
  drawn in CSS as pseudo-element bars, which a text search cannot see, so the check has to be a
  render check.
- **No `100%`** and no spelled `100 percent`.
- Singular **guarantee**, never the plural, for the client's own offer.
- **key phrases**, never keywords. **complementary**, never complimentary.
- No exclamation marks in rendered copy, no emoji, no competitor named, no price or band, no metro
  count, no `#1` or "top of Google" outside a verbatim quotation.
- **Never invent a fact, a contract term or a biography detail.** Owner-pending content ships as
  finished copy admitting the gap, never as a `TBD` marker.

The rule that outranks the others: **contractual precision beats brevity.** If shortening a sentence
would make a checkable claim vaguer, or would remove a limit so a bigger claim stands unqualified,
the cut is refused. Removing a limit is the single edit that turns an honest page into a false one.

## Known state, recorded rather than hidden

- **111 of the 403 files in `assets/` are not images.** They are HTML error pages saved with an image
  extension when the original capture hit a CDN that refused it. No page references any of them,
  verified, so this is latent rather than live damage. They are kept because they are part of the
  capture record and re-fetching may be possible.
- `_approvals.json` has **no BULK stamp**. That is an owner checkpoint and it has not been signed.
- `_published.json` is **stale** relative to what is live; trust the output repo's git log instead.
- Four pages have no chrome footer route, blocked by the chrome parity lock.
- Eighteen footer links render 23px tall, 1px under the WCAG 2.2 AA target minimum, inside locked
  chrome.
- Inline SVG diagram labels render near 6px at 390px because `.bw-figure` has no mobile treatment.
- `.bw-table` captions are not reset in the mobile block, so a captioned table sets its caption one
  word per line at 390px.
