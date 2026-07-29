# TASK: Five-market consolidation - the cross-market co-branding comparison (post-re-sweep edition)

Rebuild the cross-market comparison document across Taiwan, Japan, Korea, Malaysia, and Thailand, on the post-re-sweep tables. This supersedes the three-market comparison doc. It is a SYNTHESIS run, not a mining run: no new rows, no new sources, no web sweeping - everything comes from the five findings/census/<market>/ folders (campaigns.md + _VERDICT.md incl. the Post-re-sweep addenda) and findings/census/RESWEEP_SUMMARY.md. If a number cannot be derived from those files, it does not appear.

## Deliverables

1. `findings/census/FIVE_MARKET_COMPARISON.md` - the record version
2. `findings/census/five-market-comparison.html` - the presentation version (self-contained HTML, print-safe, zero external deps, chart-like visuals built from the real numbers only - same discipline as the prior comparison doc)

The old three-market comparison doc: leave in place, add a superseded-by header line pointing at this one.

## Structure (sections in this order)

### 1. The headline table
Post-re-sweep, one instrument: per market - n, portfolio/indie/unclear shares, addressable-indie (REP=yes) share of whole census, distinct REP=yes creator count. The publishable numbers: JP 34.9% / KR 34.0% / TW 27.5% / MY 25.0% / TH 20.5% (verify against the files, do not trust this task's memory). State plainly: a continuous 1.7x band, measured on a common query instrument; the pre-re-sweep 2.4x range was partly press-convention artefact.

### 2. The measurement story (why these numbers can be trusted)
Short section: identical definition, identical pinned edge cases, curl-verified rows, the brand-side undercount discovery (TH), the artist-side re-sweep correcting all markets one-directionally, and the four-mechanisms taxonomy (erasure TH/MY, channel JP, segregation KR, none TW - with the TW null result as the control that proves the instrument). This section doubles as the methodology credibility statement for any external reader.

### 3. The breadth correction - the finding that matters most
The addressable-creator counts: KR 7 -> 17, MY 4 -> 14 (and TW/JP as the files state). The prior "thin bench" concentration claims were query artefacts. Carry the rule verbatim: any concentration claim from a brand-side census should be assumed a query artefact until tested against an artist-side sweep. Frame what this means: the addressable indie supply exists in every measured market; it is invisible to brands through brand-side channels - which is the structural gap an evidence-led agency occupies.

### 4. Market structure divergences (what stays different after the correction)
- The machinery thesis, revised: sticker/集點 economies (TW/JP/KR) vs their absence (MY) vs TH's illustrator/art-toy visible economy - what the re-sweep changed and what survived.
- TH's closed-formats finding: high-distribution formats (retail/CVS/e-comm, banking, fintech) 100% portfolio - indies present in the market, absent from the formats that scale. Check whether the other markets' tables support or contradict a parallel cut (derive per-market format x class if the data allows; if a market's format vocabulary doesn't map cleanly, say so rather than forcing it).
- Format mix per market (TH licensed-goods/mall-led vs F&B-led elsewhere; the mall-as-indie-buy-side finding).
- Concentration where it genuinely survives artist-side sweeping (TH's Butterbear 20.5% of rows - a real structural feature; any parallels).

### 5. Per-market one-page reads
For each market: n, the shares, the addressable read, its mechanism (from the taxonomy), its 2-3 sharpest market-specific findings from its verdict, and its honesty caveats (MY: the 18.4-25.0 range + the dateless backlog; single-source rates; translation-flag rates). These are the pages a pitch pulls from.

### 6. Caveats (carried verbatim, not softened)
- Per-year slices within markets are NOT trend-readable (the MY 2026 festive-roundup artefact, JP's newest-first pagination) - overall per-market shares are the numbers to quote.
- The instrument is common but not uniformly deep (low-correction markets were well-swept; high-correction markets may still be under-swept; MY least settled).
- Sample censuses, not exhaustive counts.
- No outcomes, no sell-through, no royalties, no performance figures anywhere - the comparison inherits every census's evidence standard.

### 7. What's next (one short paragraph)
Named, not promised: SG/HK/ID/VN/PH as future markets (artist-side from birth, per-market mechanism predictions from the taxonomy), the MY dateless backlog, the zh-Malaysian press light sweep, TH's FB/LINE holes. This doc re-renders as markets join.

## Rules

Every number traceable to a file in findings/census/. No invented aggregates - where markets' vocabularies differ (format buckets, REP conventions), reconcile explicitly and show the mapping, or present per-market without forcing a merged number. The HTML version's charts render only real numbers, direct-labelled. No outcome claims. Where this task's own stated figures disagree with the files, THE FILES WIN - flag the discrepancy in the doc's method note.

Out of scope: any new market sweeping, any Cortex import, any change to the census tables themselves.