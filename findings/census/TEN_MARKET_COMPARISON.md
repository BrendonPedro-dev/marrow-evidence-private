# Co-branding census - ten-market comparison (full series)

Taiwan v2 / Japan / Korea / Malaysia / Thailand / Singapore / Hong Kong / Philippines / Vietnam / Indonesia.

As of 2026-07-30, with the Indonesia census closed.

**This document supersedes `FIVE_MARKET_COMPARISON.md`** (the five-market Taiwan/Japan/Korea/Malaysia/Thailand comparison, built 2026-07-29), which in turn superseded `census-comparison.md` (three markets, pre-re-sweep).
Nothing here is a new measurement.
This is a synthesis of ten completed censuses: no new rows, no new sources, no new sweeping.

Sources, on record:

- Taiwan v2: `taiwan-v2/_VERDICT.md` (incl. Post-re-sweep addendum) + `taiwan-v2/campaigns.md` (138 rows).
- Japan: `japan/_VERDICT.md` (incl. Post-re-sweep addendum) + `japan/campaigns.md` (146 rows).
- Korea: `korea/_VERDICT.md` (incl. Post-re-sweep addendum) + `korea/campaigns.md` (158 rows, 2 public-body rows excluded from the split, classifiable base 156).
- Malaysia: `malaysia/_VERDICT.md` (incl. Post-re-sweep addendum) + `malaysia/campaigns.md` (124 rows).
- Thailand: `thailand/_VERDICT.md` + `thailand/campaigns.md` (83 rows, artist-side from the start, no addendum needed).
- Singapore: `singapore/_VERDICT.md` + `singapore/campaigns.md` (81 rows, both keyword classes from birth).
- Hong Kong: `hongkong/_VERDICT.md` + `hongkong/campaigns.md` (93 rows, two tranches on two instruments).
- Philippines: `philippines/_VERDICT.md` + `philippines/campaigns.md` (82 rows, two adjudication tranches).
- Vietnam: `vietnam/_VERDICT.md` + `vietnam/campaigns.md` (47 rows, three tranches, documented coverage ceiling in place of the row floor).
- Indonesia: `indonesia/_VERDICT.md` + `indonesia/campaigns.md` (102 rows, three tranches).
- Cross-market: `RESWEEP_SUMMARY.md`.

Presentation version of this document: `ten-market-comparison.html`.

---

## Method note on this document

Every number below traces to one of those files.
Three classes of figure are *derived by this document* rather than carried from a verdict, and each is marked at the point of use.

1. **Two distinct-creator counts are `[derived]`**, both carried forward from the five-market document with their derivations intact: Japan's (which `RESWEEP_SUMMARY.md` records as "not re-counted") and Thailand's (which its verdict does not state separately).
Both were re-verified for this document by reading the `REPRESENTABLE` column of the market's own `campaigns.md` and de-duplicating creator names, and the contributing row numbers are cited so the derivation is auditable.
2. **The addressable share of census for the five new markets is `[derived arithmetic]`**: their verdicts state a REP=yes row count and an `n` but not the quotient, so the share is the quotient of two stated numbers (REP=yes rows divided by total rows).
The five original markets' shares are carried from their verdicts as written.
3. **The full REPRESENTABLE split (yes / no / unclear) for all ten markets is `[derived]`** from each market's own `campaigns.md` `REPRESENTABLE` column.
The independent-row total produced by that derivation matches the independent-row count stated in every one of the ten verdicts, with no exceptions, which is the check that makes the derivation safe to use.

**Where this document's commissioning framing disagrees with the files, the files win.**
Eight discrepancies were found and each is resolved in favour of the files:

- **The two-tier hypothesis does not survive contact with the files.** It was tested as instructed and is reported as tested-and-rejected in section 2, with what does survive in its place. The largest gap inside the proposed "East Asia machinery" tier (Korea 34.0% to Taiwan 27.5%, 6.5 points) is exactly equal to the largest gap between the proposed tiers (Thailand 20.5% to Hong Kong's two-tranche 14.0%, floor 2.6%, 6.5 points), so the distribution is not bimodal on the numbers.
- **Indonesia's fifth-mechanism candidate was predicted as "thin indexing" and its verdict rejects that prediction outright**: "The prediction is wrong on both halves, and the answer to the fifth-pattern question is yes but not that pattern." Indonesian press is "enormous, fully open to HTTP, and names creators readily". The pattern its verdict names is **two-channel licensing**, and that is the pattern carried here.
- **Vietnam was framed as "possibly single digits" and is confirmed at 8.5%**, but its verdict supplies a sharper number the framing did not anticipate: an independent-**character** share of 1 row in 47 (2.1%).
- **Malaysia and Thailand were framed as "the gradient" between two tiers.** On the numbers they are not a bridge between two modes, because there are no two modes to bridge (see above).
- **Hong Kong's caveat has two formulations in its own verdict and both are carried here**, because they are not the same statement: section 1 of that verdict gives the two tranche hit rates as 2.6% (2 of 77, brand-side) and 68.8% (11 of 16, artist-side-first), a 26-fold spread; its named hole 2 states "The indie share is bounded below at 2.6% and above at 14.0% and this run cannot narrow it further." This document quotes 14.0% only alongside both.
- **Hong Kong's verdict states Japan's REP=no share of independent rows as "~29%" in a cross-market comparison, and that figure does not reconcile with `japan/campaigns.md`, which gives 9 REP=no rows of 51 independent rows (17.6%).** The table figure is used here. Hong Kong's own figure (6 of 13, 46.2%) and Taiwan's (17 of 38, 44.7%) both check out exactly against their tables, so the discrepancy is confined to that one comparison.
- **Indonesia's tranche drift runs downward** (21.9% at 32 rows, 13.1% at 61, 12.7% at 102), which complicates the five-market document's statement that the correction direction is one-sided. It is not a counter-example to that statement but a different operation, and section 3 draws the distinction rather than smoothing it.
- **The `ip_scale_band` enrichment named in section 8 appears in no census file.** It is carried as a forward pointer from the commissioning task, labelled as such, and no number in this document depends on it.

One figure in the superseded five-market document is corrected here rather than carried.
It stated that "10 of 51 indie rows are REP=unclear" in Japan, which pairs a pre-re-sweep count with a post-re-sweep denominator.
`japan/_VERDICT.md` §5 gives 10 REP=unclear rows on the pre-re-sweep base of 40 indie rows, and its addendum adds six more by row number (132, 135, 137, 138, 139, 142).
`japan/campaigns.md` gives **16 of 51**, which is 10 plus 6, and 16 is the figure used here.

Where the markets' vocabularies differ (format buckets in particular), the mapping is shown or the merge is refused, and section 5 says which.

**The Hong Kong caveat is a contract of this document.**
The figure 14.0% never appears anywhere below without its two-tranche composition attached.

---

## 1. The headline table

**Ten markets, one instrument, 1,054 curl-verified rows.**

| Market | Total rows | Classifiable n | PORTFOLIO | INDEPENDENT | UNCLEAR | Addressable (REP=yes) rows | Addressable share of census | Distinct REP=yes creators |
|---|---|---|---|---|---|---|---|---|
| **Japan** | 146 | 146 | 94 (64.4%) | 51 (**34.9%**) | 1 (0.7%) | 26 | **17.8%** | 25 entries `[derived]` |
| **Korea** | 158 | 156 | 96 (61.5%) | 53 (**34.0%**) | 7 (4.5%) | 28 | **17.7%** | **17** |
| **Taiwan v2** | 138 | 138 | 95 (68.8%) | 38 (**27.5%**) | 5 (3.6%) | 18 | **13.0%** | **17 of 25 distinct indie IPs** |
| **Malaysia** | 124 | 124 | 92 (74.2%) | 31 (**25.0%**) | 1 (0.8%) | 20 | **16.1%** | **14** |
| **Thailand** | 83 | 83 | 66 (79.5%) | 17 (**20.5%**) | 0 (0.0%) | 11 | **13.3%** | 9 `[derived]` |
| **Hong Kong** | 93 | 93 | 78 (83.9%) | 13 (**14.0%**, see caveat) | 2 (2.2%) | 5 | **5.4%** `[derived arithmetic]` | **6** |
| **Indonesia** | 102 | 102 | 88 (86.3%) | 13 (**12.7%**) | 0 (0.0%), 1 MIXED (1.0%) | 11 | **10.8%** `[derived arithmetic]` | **8** |
| **Singapore** | 81 | 81 | 74 (91.4%) | 7 (**8.6%**) | 0 (0.0%) | 1 | **1.2%** `[derived arithmetic]` | **1** |
| **Philippines** | 82 | 82 | 75 (91.5%) | 7 (**8.5%**) | 0 (0.0%) | 6 | **7.3%** `[derived arithmetic]` | **14 named creator entities** |
| **Vietnam** | 47 | 47 | 43 (91.5%) | 4 (**8.5%**) | 0 (0.0%) | 4 | **8.5%** `[derived arithmetic]` | **4** |

### The Hong Kong caveat, which travels with the number

Hong Kong's 93 rows are **not one sample**, and its verdict states this in section 1 rather than in a footnote.

- Rows 1-77 came from generic brand-side queries worked in date order, an unbiased pass, and hold **2 independent rows in 77 (2.6%)**.
- Rows 78-93 came from a second tranche that worked the artist-side and label-name queries *first, on purpose*, and hold **11 independent rows in 16 (68.8%)**.

Its verdict's own words:

> Neither figure is Hong Kong's indie share.
> The first is a floor produced by an instrument that demonstrably cannot see the layer; the second is a ceiling produced by an instrument aimed straight at it.
> **The honest statement is that HK's true independent share is materially above 2.6%, that 14.0% is the best available estimate and is biased upward, and that the size of the gap - a 26-fold difference in hit rate between two query classes on the same market in the same window - is itself this census's largest finding.**

And separately, in its named holes:

> **The indie share is bounded below at 2.6% and above at 14.0% and this run cannot narrow it further.**

Both statements are the verdict's own and both are carried.
**14.0% is not quotable on its own.**
The reason is a named tooling failure rather than a judgement about the market: 781 candidates were harvested, 302 were resolved before Google's `batchexecute` endpoint hard-blocked this client, and **479 candidates still hold a title, a publisher and a date but no URL.**

### Denominator and counting-convention notes, because they differ

- **Korea** runs its indie/portfolio split on the classifiable base of 156 (the 2 government/public-body IP rows are excluded per the pinned Kumamon rule), while its addressable share runs on all 158 campaigns (28/158 = 17.7%), which is how the Korea verdict states it both pre and post re-sweep.
- **Every other market's classifiable base is its full row count**; no rows are excluded from any other split.
- **Indonesia carries one MIXED row** (row 2, Shopee's Garfield x Si Juki collection, a global portfolio IP paired with a creator-owned domestic character). Counting it on its Si Juki side gives 14 of 102 (13.7%), which its verdict names as "the upper bound of any reasonable counting convention here", and adds a 12th addressable row (12/102 = 11.8%). The 12.7% / 11 addressable rows in the table above is the base convention.
- **Malaysia's honest range is 18.4% to 25.0%**, depending on whether commissioned original artwork on a co-branded premium counts as licensed illustration IP. The census's own standing rule says it does. A reader who draws the line at pre-existing character IP gets n=114, 21 indie, 18.4%.
- **Indonesia's headline is bracketed 12.7% to 13.7% on activation strictness** (a stricter franchise-local reading demotes up to 7 portfolio rows, raising the share to 13/95), and its verdict instructs: "Read 12.7% as a floor with a soft ceiling near 20%."
- **Hong Kong's borderline rows move the number the other way**: removing rows 47, 69 and 71 moves the indie share from 14.0% to 14.4%.
- **Philippines and Vietnam both state stricter-reading sensitivities that do not change the conclusion**: PH dropping rows 51, 78 and 82 takes n to 79; PH dropping row 19 raises the indie share to 8.6%; VN dropping rows 28, 34 and 41 takes n to 44 and raises the indie share to 9.1%.
- **Japan's distinct count is `[derived]`**: 26 REP=yes rows (6, 8, 16, 19, 21, 23, 39, 42, 45, 50, 52, 66, 77, 78, 80, 84, 90, 110, 117, 118, 123, 133, 134, 136, 140, 141) resolve to 25 distinct entries once ヒグチユウコ's two rows (6, 42) are merged. Four of those 25 are multi-illustrator rosters rather than single creators (row 19, the 18-illustrator Loft "Creator meets"; row 77, a 12-illustrator capsule; row 52, three illustrators; row 140, the four-illustrator Pixio roster), and one roster member (イコモチ, row 52) also holds a solo row (134), so a stricter creator-level count is 24 named entities plus roughly 34 further illustrators inside the rosters.
- **Thailand's distinct count is `[derived]`**: 11 REP=yes rows (10, 48, 51, 55, 56, 58, 74, 76, 77, 80, 81) resolve to 9 distinct creators, because BABYBOY/StupidnoobMacc holds rows 10 and 81 and Bad Meaw holds rows 48 and 51.
- **Taiwan is stated in a different unit by its own verdict** (17 of 25 distinct indie *IPs* are REP=yes, up from 13 of 21) and is left in that unit rather than converted.
- **The Philippines' 14 is a count of distinct named creator *entities*, not of rows**, because three of its six REP=yes rows are multi-creator: row 74 names five artists, row 75 names two Ang INK members with further members unnamed, row 81 names four. Its verdict calls 14 "a floor, not an estimate of the addressable pool".
- **Hong Kong's 6 distinct creators sit on 5 rows** for the same reason: row 82 is three named illustrators in one mall campaign.

### Series totals

| | Value |
|---|---|
| Total curl-verified rows, ten markets | **1,054** |
| Total INDEPENDENT rows | **234** |
| Total addressable (REP=yes) rows | **130** |
| Total PORTFOLIO rows | 801 |
| Total UNCLEAR rows | 16 (plus 1 Indonesian MIXED row) |

The accounting closes: 801 + 234 + 16 + 1 MIXED + Korea's 2 excluded public-body rows = 1,054.
Counting Indonesia's MIXED row on its Si Juki side gives 235 independent and 131 addressable.

**A pooled cross-market indie share is REFUSED, for the same reason the five-market document refused it, restated.**
The censuses differ in depth (47 to 158 rows) and in denominator convention (Korea's two excluded public rows, Indonesia's MIXED row), so a pooled ratio would weight Japan's and Korea's deeper sweeps against Vietnam's documented-ceiling census and read as a market fact rather than a sampling accident.
The addition of Vietnam makes this worse, not better: 47 rows against 158 is a 3.4x depth spread, and Vietnam's verdict argues at measurement grade that 47 is close to exhaustive for its market while Hong Kong's argues that 93 is roughly two thirds of what its own harvest already holds.
**The per-market shares are the numbers.**

**A series-wide distinct-creator total is also refused**, and this one is a units problem rather than a weighting problem.
Taiwan's count is in distinct indie *IPs*; the Philippines' is in creator *entities* including collectives with unnamed members; Japan's includes four multi-illustrator rosters.
Creators also recur across markets: mofusand appears as an independent row in both Japan and Singapore, Gloomy/Mori Chack is a Japanese creator inside Hong Kong's table, Juju/CJ Hendry is Australian inside it, and Taiwan's addressable bench is explicitly "split domestic/inbound" with eight foreign indies in it.
Adding the ten figures would produce neither a headcount nor a share.

---

## 2. The two-tier question - tested, and rejected

The five-market band read 20.5% to 34.9%, continuous.
The commissioning framing for this document proposed that the five new markets split the region: East Asia's machinery markets (TW/JP/KR, 27-35%) against thin-layer maritime SEA (SG/PH and possibly VN at single digits), with MY (25.0%) and TH (20.5%) as the gradient between them.
That framing was tested against the ten verdicts.
**It does not survive, on four separate grounds, and this section reports what does.**

### 2.1 The distribution is not bimodal

Sorted, with the gap to the market below:

| Rank | Market | Indie share | Gap to next |
|---|---|---|---|
| 1 | Japan | 34.9% | 0.9 |
| 2 | Korea | 34.0% | **6.5** |
| 3 | Taiwan v2 | 27.5% | 2.5 |
| 4 | Malaysia | 25.0% | 4.5 |
| 5 | Thailand | 20.5% | **6.5** |
| 6 | Hong Kong | 14.0% *(2.6% floor / biased upward)* | 1.3 |
| 7 | Indonesia | 12.7% *(floor, soft ceiling near 20%)* | 4.1 |
| 8 | Singapore | 8.6% | 0.1 |
| 9 | Philippines | 8.5% | 0.0 |
| 10 | Vietnam | 8.5% *(2.1% on character IP)* | - |

The full range is **8.5% to 34.9%, a 4.1x band**.
The largest gap in the distribution is 6.5 points and it occurs **twice**: once between Korea and Taiwan, which sits *inside* the proposed upper tier, and once between Thailand and Hong Kong, which is the proposed tier boundary.
A boundary that is no wider than the widest gap inside one of the groups it separates is not a boundary.
On the numbers alone this is a continuous distribution with a wide range, not two clusters.

### 2.2 Two of the five low markets cannot be placed in a tier at all, by their own verdicts

- **Hong Kong is unplaceable.** Quoted at its brand-side floor (2.6%) it falls below Vietnam; quoted at its artist-side tranche hit rate (68.8%) it is top of the series; its verdict's bound on the share is 2.6% to 14.0% and calls the indie picture "provisional". Its verdict states the depth asymmetry directly: "Depth: adequate for the portfolio picture, provisional for the indie picture, and the difference is the whole of this section."
- **Indonesia's verdict instructs a floor reading with a soft ceiling near 20%**, which would place it at Thailand's level, and identifies one open ownership question (the INFIA call, worth ten rows) whose other resolution gives 23/102 = **22.5%**, above Thailand and Malaysia both. Its own words: "If that turned out to be so, ten rows move to INDEPENDENT, the overall share becomes 23/102 = 22.5%, and Indonesia reads as the healthiest independent market in this batch rather than a consolidated one. The whole verdict hangs on this call."

Two of the five markets the hypothesis assigns to the lower tier carry stated ranges that reach into the upper tier.

### 2.3 Geography does not predict membership

Hong Kong is an East Asian market and sits sixth.
Thailand is a mainland SEA market and sits fifth, above it.
Malaysia and Thailand are the two SEA markets in the upper group, and neither has the machinery the "East Asia machinery" label is built on - a point the five-market document already established and which the new markets do not disturb.
"East Asia" and "maritime SEA" are not the cut.

### 2.4 The ordering changes when you tier on addressability instead of the ratio

| Rank | Market | Addressable share of census |
|---|---|---|
| 1 | Japan | 17.8% |
| 2 | Korea | 17.7% |
| 3 | Malaysia | 16.1% |
| 4 | Thailand | 13.3% |
| 5 | Taiwan v2 | 13.0% |
| 6 | Indonesia | 10.8% |
| 7 | Vietnam | 8.5% |
| 8 | Philippines | 7.3% |
| 9 | Hong Kong | 5.4% |
| 10 | Singapore | 1.2% |

Taiwan drops from 3rd to 5th, Hong Kong from 6th to 9th, Vietnam rises from 9th to 7th, and Singapore separates from the Philippines by 6.1 points after being 0.1 points apart on the ratio.
The largest gap here is 4.2 points (Hong Kong to Singapore) and the range is 14.8x, wider than the ratio's 4.1x and still continuous.
**Tier membership depends on which number you tier on, which is the plainest evidence that the tiers are not a property of the markets.**

### 2.5 What survives: a division by the *form* of the independent layer, not by geography

Something real does divide the ten markets, and three of the five new verdicts found it independently, in three different languages, without coordinating.
It is not where the market is.
It is **what kind of thing the independent rows are.**

Vietnam's verdict is the one that names the distinction and also names why the earlier five never needed it:

> So the headline 8.5% and the underlying **independent-character share of 1 in 47 (2.1%)** are different claims, and only the second one answers the question this market was opened to answer.
> **2.1% is the lowest independent-character share in the nine-market series**, and no earlier market required this distinction to be drawn, because in the earlier markets the independent rows were overwhelmingly character IP already.

Indonesia's verdict draws the same line, independently:

> And eleven of the fourteen independent-or-mixed rows are an **individual artist licensing artwork onto a product or a space**, not a character IP with a name of its own that a brand programme can be built around.
> The only creator-owned *character* IPs in the census are Si Juki (rows 2, 68) and the three comic IPs on row 77, and none of them has a repeat brand programme inside the window.

And the Philippines' verdict draws it a third time, in its breakdown of the addressable fourteen:

> **Seven fine-art and children's-book illustrators** (the Looking for Juan five plus the named Ang INK two) reaching consumers through licensed-artwork product lines rather than character licensing.

That is the structure that holds.
Four groups, each with its verdict's own explanation quoted rather than invented:

**Group A - character-IP markets with a measured addressable bench (Japan 34.9%, Korea 34.0%, Taiwan 27.5%, Malaysia 25.0%, Thailand 20.5%).**
The independent rows are predominantly named character or illustration IP with repeat licensing behaviour, and the addressable bench was measured with the artist-side instrument in hand.

**Group B - a character-IP market whose measurement is unresolved (Hong Kong, 2.6% to 14.0%).**
Hong Kong's independent layer *is* character IP: LuLu the Piggy, Plastic Thing, the iSQUARE trio, LeonLollipop, BUCKET MAN. Its low position is a measurement state, not an IP-form state, and its verdict says so.
This is the one new market where the constraint is the instrument.

**Group C - artwork-licence markets (Vietnam 8.5%, Indonesia 12.7%, Philippines 8.5%).**
The independent layer exists, is press-visible, is properly credited, and licenses *artwork* rather than character properties.
Vietnam: 1 of 4 independent rows is character IP.
Indonesia: 3 of 14 independent-or-mixed rows are character IP, and the two that could carry a repeat programme are held by an IP investment company, not a creator.
Philippines: seven of the addressable fourteen are fine-art and children's-book illustrators licensing artwork, its komiks scene produced zero rows, and its verdict's conclusion is "Philippine komiks is a publishing, festival and convention culture, not yet a licensing culture."

**Group D - direct-to-consumer substitution (Singapore, 8.6%).**
The creator-owned character layer exists and is commercially visible, and it does not license at all.
Its verdict:

> Singapore's creator-owned character layer exists and is commercially visible, but it routes to consumers through its own storefronts and pop-ups instead of through brand licensing.
> There is little creator attribution to erase in brand-side coverage because there are few creator-licensed brand campaigns to attribute.

### 2.6 The competing explanations, tested

The commissioning framing offered four candidate explanations for membership.
Each was tested against what the verdicts say.

| Candidate explanation | Verdict |
|---|---|
| **The machinery thesis** (sticker and loyalty economies manufacture indie rows) | **Fails as a discriminator.** Singapore and Hong Kong both run dense collectible and loyalty machinery - Singapore's plushie appetite runs to "more than twenty campaigns" of brand-owned collectibles, Hong Kong's mall-atrium economy is the densest single-format concentration in the series at 57.0% - and both sit low. Machinery manufactures *rows*; whether those rows are independent depends on whether the market has creator-owned character IP under non-captive management to put into them. The five-market document had already narrowed this thesis to "format-shaped rather than institutional"; the new five narrow it further. |
| **Market maturity** | **Fails.** Singapore is the richest market in the series and is second-lowest on the ratio and lowest on addressability. Vietnam is the least mature and ties Singapore's ratio. Maturity predicts campaign *density*, not independent share: Singapore produced 81 rows from five portals in 31 months in a country of six million. |
| **Press indexing / creator attribution** | **Fails, and this is the most instructive failure.** Every one of the five new markets credits creators well. Hong Kong names illustrators in the headline exactly as Taiwan does. The Philippines carries the creator's name in the headline or lede in six of its seven independent rows. Vietnam carries it in the URL slug in three of four. Indonesia names creators "readily and often in the headline" and its verdict rates that "markedly better here than in the Thailand and Malaysia erasure pattern". Four markets with excellent attribution sit in the bottom five. Attribution behaviour and independent share are close to unrelated across ten markets. |
| **Creator-scene depth** | **Fails except in Vietnam.** Indonesia has "a large domestic illustration scene", the Philippines has a visible, prolific, press-covered komiks and illustration scene, Singapore has Tasty Toastys, Tap Space, Play Nation and Mr. Merlion & Friends, Hong Kong is the art-toy label capital. Only Vietnam genuinely lacks the scene, and its verdict says so at measurement grade. Scene depth without licensable, non-captive character properties does not produce independent rows. |
| **What does discriminate: the form of the IP and the channel it sits in** | The independent layer's *form* (character property versus one-off artwork commission), and whether that property is captive, consolidated, or routing direct to consumers. This is section 2.5, and it is the files' own framing in three independent verdicts. |

---

## 3. The measurement story

This section exists so an external reader can check the instrument before checking the result.

### 3.1 One definition, applied ten times

Every market was built on the identical ownership test (who owns the IP, not who runs the brand), the identical pinned edge cases, and the identical `REPRESENTABLE` sub-tag on every independent row.
The pinned cases travel by name across all ten `campaigns.md` headers: Miffy/Mercis and Peanuts/Sony as estate-or-controlling-stake PORTFOLIO; Sanrio, San-X, Pokemon-Nintendo, Disney-Marvel, Warner Bros, KAKAO FRIENDS and LINE FRIENDS/BT21 as platform- or studio-owned PORTFOLIO; government/public-body-owned mascots excluded entirely (the Kumamon rule); a brand's own mascot not counted; co-owned/JV resolved to whoever holds control, with genuine 50/50 sent to UNCLEAR.

The cross-market precedent chain is what makes the ten comparable row for row, and it is cited by row number in every market:

- **Butterbear is PORTFOLIO in Thailand on the Malaysia row 8 call** (a corporate-owned mascot licensed out).
- **LuLu the Piggy is INDEPENDENT/REP=no on the Taiwan-v2 row 5 call**, carried into Thailand, and then carried into Hong Kong across six rows *in the label's home market* without modification.
- **Venue-hosted properties are rows and the licensor's own retail is not, on the Taiwan-v2 row 126 call**, applied in every one of the ten markets: POP MART's own stores excluded in Singapore, Hong Kong, the Philippines, Vietnam and Indonesia; POP MART hosted by a third-party mall counted in all five.
- **Authorship is not ownership, on the Molly Factory precedent.** Applied to MOLLY in Singapore row 54, to Kasing Lung/THE MONSTERS in Hong Kong row 85 and to Kenny Wong restyling Snoopy in Hong Kong row 83, to MOLLY and MEGA SPACE MOLLY in Vietnam rows 25 and 31.
- **Estates are PORTFOLIO, on the Miffy/Mercis rule.** This is what places the Philippines' National Artists (row 68) on the portfolio side despite being Filipino illustration, and what classifies Vietnam's UNIQLO x KAWS x Andy Warhol (row 8).
- **Artwork licences are in scope on the illustration-IP limb**, on the Taiwan-v2 rows 120/127 and Korea rows 78/79 precedent, extended by the adidas Philippines x Aral Cru precedent, which is what admits Vietnam's rows 15, 38 and 39.
- **A creator-founded studio is the creator; a third-party IP investment company holding the asset is portfolio.** Indonesia's Si Juki/Pionicon call against its Tahilalats/INFIA call is the sharpest statement of that line in the series.

### 3.2 Every row is curl-verified against a live, dated source

Not a claim about a campaign, a fetched page: HTTP 200, with the year tag read off machine-readable page markup or a stated campaign window, never inferred.

- Thailand re-verified all 97 cited URLs at build time and went from a claimed 85 rows to a verified 83.
- Singapore re-verified all 95 source URLs at HTTP 200 on 2026-07-29, "each with a machine-readable `datePublished` in the page's JSON-LD. No row rests on an inferred date."
- Hong Kong re-verified all 138 source URLs, and cites no `news.google.com` URL anywhere: "Google News is the index and the publisher page is the evidence."
- The Philippines verified all 117 source URLs, and discovered a verification trap worth carrying: BusinessMirror serves a Cloudflare interstitial returning 403 to a *randomly rotating* subset of requests, so "a single-pass verifier would produce a misleading dead-link count."
- Vietnam verified 94 of 97, with the three failures all `dantri.com.vn` under a standing client-side block, and no row resting on a dantri source alone.
- Indonesia verified all 174 distinct URLs, and adds a dating rule the series needed: year tags come from the stated campaign window or the article's own `datePublished`, and on flat-sitemap hosts never from metadata at all.

Phantom entries are the named failure class in every build.

### 3.3 The Thailand keyword discovery, which reset the series

Thailand was the first market swept with artist-side keywords, and it found the effect inside a single build.
Pass 1 on brand-side Thai terms (คอลแลบ, คาแรกเตอร์, ลิขสิทธิ์, มาสคอต, entity names) returned 4 indie rows in 43, or **9.3%**.
Pass 2 added three artist-side terms (ศิลปินไทย, นักวาด, ครีเอเตอร์) against the *same two trade titles* and returned 13 more, taking the census to 17 indie in 83 rows, or **20.5%**.
Same sources, same geography, same definition, same window.
Brand-side PR names the licensor and omits the creator, so indie rows are structurally invisible to a brand-side query.
Thailand's own verdict flagged the consequence before anyone acted on it, and rated the claim "indie share is below the Japan/Taiwan/Korea band" at **Low** confidence for exactly this reason.

### 3.4 The four-market re-sweep, and its one-directional correction

Each re-sweep appended rows to the existing table under the existing definition.
No table was rebuilt.
No existing row was reclassified, re-dated or edited in any of the four markets, which is stated explicitly in all four addenda and is itself a consistency check: where a new row touched an existing licensor relationship, the new evidence agreed with the recorded call.

| Market | Pre-re-sweep n | Pre indie share | Post-re-sweep n | Post indie share | Correction | Rows added (indie / portfolio / unclear) |
|---|---|---|---|---|---|---|
| Thailand *(reference, artist-side from the start)* | 83 | 20.5% | 83 | **20.5%** | - | - |
| Japan | 131 | 30.5% | 146 | **34.9%** | +4.4 | 11 / 4 / 0 |
| Korea | 133 classifiable | 24.8% | 156 classifiable | **34.0%** | +9.2 | 20 / 2 / 1 |
| Taiwan v2 | 129 | 27.1% | 138 | **27.5%** | +0.4 | 3 / 6 / 0 |
| Malaysia | 103 | 12.6% | 124 | **25.0%** | +12.4 | 18 / 3 / 0 |

68 rows were added across the four re-swept markets: 52 INDEPENDENT, 15 PORTFOLIO, 1 UNCLEAR.
Portfolio rows caught by the artist-side net were appended rather than dropped in every market, even where they reduced the correction, and Malaysia's addendum states the arithmetic cost of that honesty in the open (without its three Touch 'n Go portfolio rows the correction would read 12.6% to 25.6% rather than 25.0%).

### 3.5 Instrument sensitivity across all ten markets, with the comparisons kept apart

The ten markets do **not** share one before-and-after measurement, and merging them into one chart or one aggregate would be an invented number.
Four markets have a keyword-class re-sweep; Thailand has a within-build two-pass comparison; three have adjudication-tranche splits; two have tranche drift across corpus expansions.
The table below states which comparison each market carries, so the numbers are readable without being pooled.

| Market | What the comparison is | Low | High | Movement |
|---|---|---|---|---|
| Thailand | Pass 1 brand-side vs pass 2 with artist-side terms, same two titles | 9.3% (4 of 43) | 20.5% (17 of 83) | 2.2x |
| Japan | Pre vs post artist-side re-sweep | 30.5% | 34.9% | +4.4 pts |
| Korea | Same | 24.8% | 34.0% | +9.2 pts |
| Taiwan v2 | Same | 27.1% | 27.5% | +0.4 pts, a null |
| Malaysia | Same | 12.6% | 25.0% | +12.4 pts, the largest re-sweep correction |
| Singapore | Both classes from birth; the artist-side class added exactly one row | - | 8.6% | +1.2 pts attributable to the artist-side class, a null |
| Hong Kong | Tranche 1 brand-side, date order vs tranche 2 artist-side-first | 2.6% (2 of 77) | 68.8% (11 of 16) | **26x hit-rate spread**; pooled 14.0%, biased upward |
| Philippines | Tranche 1 score order vs tranche 2 artist-side tag class | 5.8% (3 of 52) | 13.3% (4 of 30) | 2.3x; pooled 8.5%, mildly biased upward |
| Vietnam | Three tranches over three successively larger corpora, artist-side net repaired and rescored in tranche 3 | 8.3% (2 of 24) | 8.5% (4 of 47) | Stable: 8.3%, 8.1%, 8.5% |
| Indonesia | Three tranches over successively wider instruments, including one aimed at the independent-artist channel | 12.7% (13 of 102) | 21.9% (7 of 32) | **Drifted down**: 21.9%, 13.1%, 12.7% |

Three things follow that the five-market document could not see.

**Hong Kong's 26-fold spread is the taxonomy's most extreme datapoint by an order of magnitude.**
The next largest keyword-class effect in the series is Thailand's 2.2x and the Philippines' 2.3x.
No other market produced a spread anything like it, and the verdict is explicit that this spread, not the ratio, is Hong Kong's largest finding.

**Vietnam is the series' second null result, and it is a different kind of null from Taiwan's.**
Taiwan's null is a coverage null: the two query classes return overlapping result sets because zh-TW trade press already embeds 插畫家 and 原創IP in ordinary brand-side copy.
Vietnam's is a supply null, and it is the best-evidenced null in the series because it was measured on the largest corpus: tranche 3's repaired artist-side pass returned 194 artist-shaped candidates after dedupe and produced exactly one row.
Singapore's is a third kind, also a supply null but for a different reason: "The two query classes do not overlap here at all - the artist-side class returns a completely different corpus - but that corpus is not brand-collaboration coverage."

**Indonesia is the one market where widening the instrument moved the ratio down, and this qualifies the five-market document's one-directional claim without contradicting it.**
The one-directional claim is about *adding a keyword class to the same sources*: brand-side querying undercounts indie, never the reverse.
That still holds in every market where it has been tested, including the three new markets that tested it (Singapore +1.2, Hong Kong upward, Philippines upward).
Indonesia's drift is a different operation, *adding publishers*, and its verdict states the mechanism: "Every widening of the instrument surfaced more portfolio licensing than independent licensing, including the widening that was specifically aimed at the independent-artist channel and that added five independent rows in one tranche."
Widening a corpus adds portfolio-heavy veins faster than it adds the independent channel, because the portfolio channel is what most publishers cover.
**Adding a keyword class and adding a publisher tier are not the same experiment, and this document does not report them under one heading.**

### 3.6 The mechanisms taxonomy, tested across ten markets

The re-sweep's premise was that brand-side keywords erase creators everywhere the way they do in Thailand.
That held in one of four markets, and the five-market document replaced the premise with a four-mechanism taxonomy.
**Five new markets produced five new mechanisms.**
The taxonomy did not saturate at four, and reporting it as though it had would misrepresent the series.

| # | Mechanism | Market(s) | What it is | Instrument effect |
|---|---|---|---|---|
| 1 | **Erasure** | Thailand, Malaysia | Brand-side PR names the licensor and omits the creator. Malaysia's densest local-creator format, the festive packet given with purchase at Raya and CNY, is reported brand-side as a promotion with the illustrator named nowhere; the attribution exists in one trade publication's annual design roundups (8 rows rest on two URLs). | TH +11.2, MY +12.4 |
| 2 | **Channel** | Japan | Campaigns *named after the artist* are unreachable by a brand-side query by construction: the illustrator pop-up circuit, standing brand creator-collaboration programmes, transport and tourism tie-ins. | JP +4.4 |
| 3 | **Segregation** | Korea | The indie coverage exists in full, in a creator-facing character-industry trade magazine (아이러브캐릭터) indexed by creator and IP owner rather than by brand, which no brand-side query class touches. 17 of Korea's 23 new rows came from it. | KR +9.2 |
| 4 | **None of the above** (coverage null) | Taiwan v2 | zh-TW trade press names the illustrator in the headline as a selling point, so the two query classes return heavily overlapping result sets. The control that proves the instrument. | TW +0.4 |
| 5 | **Direct-to-consumer substitution** (supply null) | Singapore | The creator-owned character layer exists, is commercially visible, and monetises through its own retail and its own pop-ups rather than by licensing into someone else's campaign. There is little attribution to erase because there are few creator-licensed campaigns to attribute. The two independent IPs in the table were found by **brand-side** queries, "the exact inverse of Thailand". | +1.2 pts |
| 6 | **Crowding-out** | Hong Kong | The taxonomy's own diagnostics all say Hong Kong should be Taiwan: press names illustrators in the headline, creator-fronted campaigns run in the same titles with the same vocabulary, no segregated trade publication exists. It behaves like Japan anyway. | 26x |
| 7 | **Naming and retrievability as separate variables** | Philippines | Press names creators willingly and well, and a brand-side-only sweep still misses roughly 40% of the independent layer, because the *brands* doing independent work are small, purpose-led or category-specific and invisible to a brand-name keyword net. Three of four second-tranche independent rows came from brands on no brand-side list this series uses (Looking for Juan, UNICEF Philippines, New Era). | 2.3x |
| 8 | **Pre-formation** | Vietnam | Credit behaviour is healthy, brand appetite is real, mall and retail infrastructure is in place, and a domestic character IP demonstrably reaches a domestic FMCG brand (Wolfoo x Bibica). What is missing is a population of creator-owned licensable character properties. | Stable, no movement |
| 9 | **Two-channel licensing** (bibliographic invisibility) | Indonesia | Two licensing economies in one market that barely touch: a portfolio channel reported by mainstream news, business and brand trade press, and an independent channel reported *only* in the youth-lifestyle portal network, continuously since at least 2020. They overlap in exactly one place in 102 rows. | Drifted down |

**Hong Kong's crowding-out is worth quoting in full, because it is the mechanism that breaks the taxonomy's diagnostic logic:**

> **Crowding-out.
> The creators are named, in the same publications, in the same words - and are still invisible to a brand-side query, because the market's portfolio volume saturates every generic result set before a creator-fronted campaign can rank.**

The evidence is direct rather than inferred.
135 queries returned 5,125 articles; Google News caps a query at 100 items, which is why every high-yield keyword had to be split by year.
In a market where Chiikawa is 12.9% of all campaigns and Chiikawa, Disney and Sanrio together are 37.6%, a query for 聯乘 香港 in a given year returns a hundred Chiikawa, Sanrio and Disney items and stops.
The iSQUARE, Plastic Thing and LeonLollipop articles were **in the harvested pool the whole time**.
The practical implication its verdict draws: "in a market with extreme licensor concentration, brand-side keyword census methods systematically under-count the local creator layer even when the local press is fully creator-attributive.
Taiwan's null result is what 'no mechanism' actually looks like; Hong Kong looks like Taiwan on every press diagnostic and behaves like Japan on the numbers.
The difference between them is not journalism.
It is portfolio density."

**Indonesia answers the fifth-pattern question directly, and rejects the pattern it was asked about:**

> **The prediction is wrong on both halves, and the answer to the fifth-pattern question is yes but not that pattern.**

Indonesian press is not thin: it is "enormous, fully open to HTTP, and names creators readily and often in the headline".
Its distinction from erasure is precise and worth carrying, because it changes what an operator does about it:

> Erasure means the campaign is reported and the creator is not named.
> Here the creator is named, the campaign is reported, and the *report itself* is filed in a publication tier that a brand-side or trade-side sweep never opens.
> The invisibility is bibliographic, not editorial, and it is invisibility to the researcher rather than to the consumer.
> This distinction is load-bearing for anyone acting on the number: in Thailand the fix is to ask the creator because the press will not tell you, and in Indonesia the fix is to ask a different publisher.

### 3.7 The keyword is not the classifier

Artist-side keywords are a self-presentation detector, not an ownership detector, and they fail in both directions in every market where they have been run.
Taiwan's dtto friends bills itself as 「原創角色品牌」and is Dcard platform-owned; Japan's BLUE HAMHAM is framed as one creator's work but is © CHOCOLATE, and ナガノマーケット self-presents as the creator's own market but is portfolio under the pinned Chiikawa rule.
Korea produced the mirror image: 틴틴팅클 self-presents as an indie instatoon and its IP business is run by Iconix, while 먼작귀 appears in LG's own release as a "글로벌 인기 캐릭터 IP" with no mention of Nagano at all, yet is creator-originated.
Singapore added tokidoki (row 26), a creator-founded brand that self-presents through Simone Legno's authorship and is a corporate lifestyle brand holding a multi-character portfolio.
Hong Kong added three at once (rows 85, 53/63, 83), and Indonesia added the one that decides ten rows: Tahilalats, whose creator Indonesian press consistently calls a `komikus`, classed PORTFOLIO on four independent pieces of evidence about INFIA Corp's holding.
The pinned per-IP ownership test did the classification work in every case.
Accepting self-description would have inflated Taiwan alone from 27.5% to 31.9%.

### 3.8 The rule, carried verbatim

> **any concentration claim made from a brand-side census should be assumed to be a query artefact until it has been tested against an artist-side sweep.**

That rule applies to this document too, and section 5.3 applies it by name to the concentration findings in the new five markets, including the ones it kills.

---

## 4. The breadth and addressability picture

### 4.1 Distinct addressable creators per market

| Market | Distinct addressable (REP=yes) creators | Addressable rows | Status of the number |
|---|---|---|---|
| **Japan** | 25 entries `[derived]` (24 named entities plus ~34 roster illustrators) | 26 | 20 to 25 across the re-sweep; verdict records "not re-counted" |
| **Korea** | **17**, up from **7** | 28, up from 19 | Corrected upward by the re-sweep |
| **Taiwan v2** | **17 of 25 distinct indie IPs**, up from 13 of 21 | 18, up from 15 | Highest open-rate per distinct IP in the series |
| **Malaysia** | **14**, up from **4** | 20, up from 8 | Corrected upward by the re-sweep |
| **Philippines** | **14 named creator entities** | 6 | Explicitly "a floor, not an estimate" |
| **Thailand** | 9 `[derived]` | 11 | Single pass, artist-side from the start |
| **Indonesia** | **8** | 11 | Explicitly a floor; channel found in the final tranche |
| **Hong Kong** | **6** | 5 | Verdict: "The realistic ceiling is above 6 and the reason is named" |
| **Vietnam** | **4** | 4 | Floor, but "a much harder floor than the equivalent numbers in the earlier markets" |
| **Singapore** | **1** | 1 | Verdict: "That is the number, and it should be quoted as-is rather than softened"; realistic ceiling 3 |

### 4.2 The re-sweep corrections, kept as history

**Korea: 7 to 17.**
The original build resolved its 19 REP=yes rows to 7 distinct addressable creators and read that as "real breadth, but with two names doing much of the volume."
The 28 REP=yes rows now resolve to 17.
Ten of the eleven new names had never been seen by the original pass; only one of the nine new REP=yes rows (SSG x 가나디) belongs to a creator it already knew.

**Malaysia: 4 to 14.**
The original verdict's phrase was "four names, not a scene": Bichi Mao, Yellobanana, QuirkyQing, Bear Boss Buddies.
The post-re-sweep table names fourteen distinct creator-owned IPs that reached a national brand inside the window, ten of them new.
Only one of the twelve new REP=yes rows belongs to a creator the original pass already knew.

Both markets' concentration findings were written in good faith off a census that could not see most of the creators, and neither survived contact with an artist-side sweep.

### 4.3 What the new five add: the corrected-thin / measured-thin distinction, and why it needs a third category

The five-market document's addressability story was a correction story: thin benches turned out to be query artefacts.
The five new markets force the distinction the commissioning framing asks for, and then force a third category, because three of the five new verdicts refuse to call their own number thin.

**Corrected-thin - the thinness was a query artefact, and the correction has been made.**
Korea (7 to 17) and Malaysia (4 to 14).
Neither market's original number was wrong about the rows it had; both were wrong about the market.

**Measured-thin - the thinness was measured on the full instrument, and the verdict stands behind it.**
Singapore and Vietnam, and only these two.

- **Singapore is measured-thin at 1.** Both keyword classes ran from birth. Ten artist-side keywords across five portals over 31 months surfaced exactly one brand x local-illustrator campaign. Its verdict is unusually direct about not softening it: "That is the number, and it should be quoted as-is rather than softened." The direction of correction is one-way upward and the ceiling is stated: "the ceiling on it is bounded by the fact that ten artist-side keywords across five portals over 31 months surfaced exactly one brand x local-illustrator campaign."
- **Vietnam is measured-thin at 4, on the largest corpus in the series.** 2,607,744 distinct article URLs across 28 publishers, greped end to end for named indie properties rather than only searched. Its verdict: "it is a much harder floor than the equivalent numbers in the earlier markets, because the corpus that produced it is the largest in the series by an order of magnitude."

**Instrument-bounded - the number is a floor set by a named, quantified instrument limit, and the verdict says so.**
Hong Kong, the Philippines and Indonesia.
Calling these three "measured-thin" would misreport all three verdicts.

- **Hong Kong's 6 is bounded by 479 unresolved candidates**, each holding a title, a publisher and a date, with the title-search recovery route demonstrably working. Its verdict names the ceiling and the specific creators behind it: "Six named HK creators sit in those two rejections alone."
- **The Philippines' 14 is bounded by `spot.ph`** being unreachable at any URL, twelve further titles returning 403/401/404, and Instagram, Facebook and TikTok entirely unswept in the market where "PH illustrators overwhelmingly announce their own brand work on social rather than to press". Its verdict: "It does **not** support a claim that the addressable Filipino creator pool is 14; that is the floor a press-only, `spot.ph`-less, social-media-less instrument could reach."
- **Indonesia's 8 is bounded by the channel it was found in.** Tranche 3 asked eleven publishers the first two tranches had never asked and multiplied the independent row count fivefold, and the same eleven publishers hold six further independent-artist brand campaigns that fall just outside the window (Coach x Muklay 2022, Acer Predator x Darbotz 2020, bateeq x Monez 2022, Specs x Stereoflow 2022, Botanical Essentials x Darbotz 2023, ATARU x Muklay 2023). Its verdict: "**Eight is a floor, and the artist-side non-press channels named in section 5 are where the rest of the number is.**"

**Why the three-way distinction matters and not the two-way one.**
A two-way corrected/measured split would put Hong Kong, the Philippines and Indonesia on the "measured" side and licence a reader to treat their numbers as market facts.
All three verdicts forbid that, in their own words, with named and quantified holes.
Only Singapore and Vietnam earn the measured-thin label, and both earn it the same way: they ran the artist-side instrument at full width and it came back nearly empty.
**Thinness measured on the full instrument is a market fact.
Thinness measured through a blocked vein is not, and the difference is the whole of this subsection.**

### 4.4 The Philippines inverts the usual reading, and it is the most instructive new datapoint

The Philippines holds **14 named addressable creator entities**, tied with Malaysia's post-correction 14 and second in the series only to Japan's derived 25.
It holds them on **6 addressable rows in 82 (7.3%)**, third-lowest in the series.
So the Philippines is creator-rich and campaign-poor: a broad addressable bench where each creator has essentially one campaign, three of the six rows carry multiple creators, and the market's high-distribution formats are shut.

That combination breaks the reflex reading of a low independent share.
A low share does not imply a thin creator layer.
In the Philippines it implies the opposite: a visible, prolific, press-credited creator layer with almost no commercial bridge into brand campaigns.
Its verdict names the shape precisely, and the shape is three scenes rather than one: two art-toy and designer-object creators, four streetwear-and-graphics illustrators, and seven fine-art and children's-book illustrators.
The single sharpest item in that section is a creator with no campaign at all: "Maria", the art toy by Klaris Orfinada, "an independently-owned Filipino art-toy character explicitly benchmarked against Labubu and Sonny Angel in its own press coverage - and it has **no brand campaign attached anywhere in this sweep**."

### 4.5 The REPRESENTABLE split, all ten markets

`[derived]` from each market's own `campaigns.md` `REPRESENTABLE` column; the independent-row totals match all ten verdicts.

| Market | Independent rows | REP=yes | REP=no | REP=unclear | REP=no share of independent rows |
|---|---|---|---|---|---|
| **Hong Kong** | 13 | 5 | **6** | 2 | **46.2%** |
| **Taiwan v2** | 38 | 18 | **17** | 3 | **44.7%** |
| **Singapore** | 7 | 1 | 2 | 4 | 28.6% |
| **Korea** | 53 | 28 | 10 | 15 | 18.9% |
| **Japan** | 51 | 26 | 9 | 16 | 17.6% |
| **Thailand** | 17 | 11 | 1 | 5 | 5.9% |
| **Malaysia** | 31 | 20 | 1 | 10 | 3.2% |
| **Philippines** | 7 | 6 | 0 | 1 | **0.0%** |
| **Vietnam** | 4 | 4 | 0 | 0 | **0.0%** |
| **Indonesia** | 13 | 11 | 0 | 2 | **0.0%** |

Three readings, each grounded in a verdict.

**The captivity spectrum is real and it tops out in the two art-toy label economies.**
Hong Kong's verdict predicted it would lead the series on REP=no share and it does, at 46.2%, "narrowly ahead of Taiwan-v2's ~44.7%".
That prediction is confirmed against the tables.
But the two markets get there by different arrangements, and the difference is commercial: "Taiwan's comparable number is a creator self-licensing (Bugcat Capoo through 卡特島創意, 8 of 17 REP=no rows). Hong Kong's is a creator channelled through someone else's label. Those are different objections to representability: the first is a competitor, the second is an incumbent contract."

**Zero captivity is not openness, and two verdicts say so independently.**
The Philippines, Vietnam and Indonesia all return 0 REP=no rows.
Vietnam's reading: "That is not a positive finding about openness; it is a consequence of there being almost no local character IP under commercial management to hold."
Indonesia's reading of the same zero: "Zero `no` is a real finding rather than an absence of scrutiny: no Indonesian independent row in this census sits behind a label, platform or studio that captures the IP, which is the opposite of the Toyzeroplus-style label-captive pattern."
Read together: a zero means either that the market has no consolidating layer worth capturing its creators (Vietnam) or that it has one and its creators have so far stayed outside it (Indonesia, where consolidation happens at the character-IP level instead, through INFIA).

**Singapore's unclear rate is the highest in the series (4 of 7, 57.1%) and it is structural, not sloppy.**
Its verdict: "a straightforward consequence of Singapore's indie rows being carried by *young local companies* rather than by *named individual illustrators*: a company's exclusivity arrangements are private in a way an individual artist's brand-collab history is not."
Resolving Play Nation and Mr. Merlion & Friends is the cheapest high-value follow-up in the series, "a two-document job (ACRA filings, or a direct ask) rather than another sweep", and would move Singapore's distinct addressable count from 1 to as many as 3.

### 4.6 What the breadth picture means, ten markets on

The addressable indie supply exists in every one of the ten measured markets, and in nine of the ten the verdict states its own number is a floor.
Korea more than doubled its addressable bench and Malaysia more than tripled it without a single new source type being invented, without the definition moving, and without anything changing in the markets themselves.

The structural point for an evidence-led agency follows directly, and it does not require an outcome claim to make.
Brands source IP through the same channels a brand-side query reaches: licensor PR, agency rosters, the trade press that covers campaigns brand-first.
That is precisely the channel set in which this addressable supply is invisible - and the ten-market evidence now shows it is invisible in **at least five distinguishable ways** (sections 3.6, mechanisms 1, 3, 5, 6, 7, 9), not one.
The gap is not a supply gap and it is not an appetite gap in eight of the ten markets.
It is a **visibility gap between an addressable creator layer that demonstrably reaches national brands and the channels through which brands look for IP.**

The two exceptions are named rather than absorbed, because they matter to any operator acting on this.
**In Vietnam it is a supply gap**, and its verdict says so: the work is not to make existing creators visible but that "the licensable properties have not been built yet."
**In Singapore it is a routing difference**, not a gap at all: the creator-owned layer exists and has chosen direct-to-consumer over licensing.

---

## 5. Market structure divergences

### 5.1 The closed-formats finding, tested across all ten

Thailand's sharpest cut was never its headline ratio.
It was that **the formats that scale are 100% portfolio**: retail/CVS/e-commerce (11 rows), banking/fintech (6 rows), 17 rows in total, zero indie, while experiential rows were 42.9% indie.
Thailand rated it **Medium-high** on the honest grounds that 17 rows is a small base.

**The evidentiary form of this finding improved substantially with the new five.**
When the five-market document tested it, only Thailand carried a counted format-by-class table and only Malaysia carried a counted format table at all (and Malaysia's is pre-re-sweep, n=103, never recomputed).
**Now five of the ten markets carry a counted format table cut by IP class** (Thailand, the Philippines, Vietnam, Indonesia, and Hong Kong via its stated independent-row-by-format list), and Singapore carries a counted format table without a class cut.
Taiwan, Japan and Korea still record format structure as targeted-vein observations.

**A merged ten-market format-by-class table remains not derivable and is not presented.**
The bucket vocabularies do not map: Singapore splits QSR, BBT and themed café into three buckets where Hong Kong has QSR/F&B and themed café as two and Indonesia has one "F&B menu and QSR"; Indonesia files two F&B rows under other formats and says so; Taiwan's 集點 waves, Japan's kuji and gashapon and Korea's Olive Young rollout machine have no counterpart bucket anywhere else.
What follows is per-market, in each market's own vocabulary.

| Market | Evidence on high-distribution formats | Verdict |
|---|---|---|
| **Philippines** | **The most complete closure in the series.** Mall/venue 26 rows, **0 independent**. Ticketed live show 12 rows, **0**. Device 6 rows, **0**. Telco loyalty 2 rows, **0**. QSR/convenience/F&B 10 rows, 1 independent and that one REP=unclear (a book publisher, not a creator). Counted table, cut by class. | **Supports, most strongly in the series.** Its verdict: the closure is "complete rather than partial". |
| **Vietnam** | Mall/department-store/venue 10 rows, **0 independent**, nine of the ten POP MART, Bandai Namco, Disney or Fujiko. F&B chain 3 rows, **0**. Device/vehicle 3 rows, **0**. Convenience and QSR: **zero rows of any kind**, from any IP, after all of Circle K, WinMart, GS25, FamilyMart, Ministop, KFC, Lotteria, Jollibee, McDonald's Vietnam and Popeyes were swept by name across three waves. Counted table, cut by class. | **Supports**, and adds a category the series had not seen: a format so absent that it produces no rows at all. |
| **Indonesia** | F&B menu and QSR **0 of 9**. Licensed beauty and personal care **0 of 7**. Convenience chain **0 of 2**. Banking and cards **0 of 1**. Game and in-game **0 of 3**. **Telco and e-wallet: no rows at all** after Telkomsel, Indosat, Tokopedia and Blibli were queried across three instruments and three tranches. Counted table, cut by class. | **Supports**, and its beauty finding is the sharpest single line: "Indonesian beauty brands license Sanrio, Pokémon and Barbie, never a domestic illustrator, despite Indonesia having a large domestic illustration scene and beauty being the category most likely to commission one." |
| **Thailand** | Retail/CVS/e-comm 0 of 11 indie; banking/fintech 0 of 6. Counted table, cut by class. | **Supports.** The finding's origin. |
| **Korea** | "Finance/card, telecom, travel/hospitality, bakery/dessert, mobile-game, snack/beverage packaging, and premium eyewear came back essentially 100% portfolio", and the addendum confirms the artist-side pass did not dent it: "no artist-side query returned a single finance, telecom, hospitality or snack-packaging indie row." | **Supports, and it survived the re-sweep** - still the strongest form of this finding among the original five, because it was re-tested with a better instrument and held. |
| **Japan** | "The gaming/payment/telecom vein came back 100% portfolio on targeted search"; indies "largely absent from gacha, card-skins, telecom points, and national vending." Vein observation, not a counted table. | **Supports**, in weaker evidentiary form. |
| **Hong Kong** | **Splits by format.** **No independent row appears in the venue/attraction/transit bucket** at all - MTR, Star Ferry, Ocean Park, Ngong Ping 360 and the Disneyland-adjacent campaigns are all portfolio. But independents reach mall (5 of 13 indie rows), retail (3), FMCG (2), café (1), QSR/F&B (1) and banking (1, BUCKET MAN on HSBC, the market's only banking row). | **Supports in transit and attraction, contradicts in mall and banking.** Its verdict: "Transit and attraction licensing in Hong Kong is a closed door to local creators in this window, and that is a cleaner statement of the addressability problem than the ratio is." |
| **Singapore** | No class-cut table. Its one independently-owned property reached the market's newest high-distribution format: row 75, SimplyGo x Mr. Merlion & Friends, a transit-payments loyalty campaign, which its verdict names as "where the one independently-owned SG property reached its largest brand". That row is REP=unclear. | **Marginal contradiction on n=1.** The loyalty/platform/banking bucket did not exist in Singapore before 2025 and is where the independent property landed when it did. |
| **Taiwan v2** | **Contradicts.** Bugcat Capoo, a creator-owned indie, carried a 7-ELEVEN x 國立故宮博物院 flagship 全店精品集點 wave across 7,100+ stores; also 華南金控 (listed financial holding company, shareholder gift), 中華郵政 (national postal service) and CTBC. | **Contradicts.** The highest-distribution retail-loyalty format in the country was headlined by an indie IP. |
| **Malaysia** | **Contradicts.** The payments/platform vein is 11 rows and 6 of them are indie: Touch 'n Go x QuirkyQing (95, REP=yes), KTM Komuter x Bichi Mao (100, REP=yes), foodpanda x Yellobanana (90, REP=yes), Lalamove x Yellobanana (94, REP=yes), Touch 'n Go x Loka Made (106, REP=unclear), Maxim x five Sabah/Sarawak illustrators (121, REP=unclear). | **Contradicts**, and in the format Thailand found most closed. |

**The synthesis, ten markets on.**
"High-distribution formats are closed to indie IP" now holds in seven markets (Thailand, Japan, Korea, the Philippines, Vietnam, Indonesia, and Hong Kong in transit and attraction) and fails in two (Taiwan, Malaysia), with Singapore a marginal third exception on a single REP=unclear row.
The five new markets substantially strengthened it, because three of them measured it with counted class-cut tables and all three found complete rather than partial closure.
Where it holds, the closure is in *corporate-premium, screen-IP-driven and infrastructure* channels: finance cards, telecom points, national vending, snack packaging, mall operators, transit, devices, beauty.
Where it breaks, it breaks through a specific instrument: a national retail-loyalty programme that chose an indie IP on its merits (Taiwan), a stored-value card line that treats creator artwork as a product category (Malaysia), and a transit-payments loyalty programme in its first year (Singapore, n=1).
Both of the real exceptions are existence proofs that the closure is a market convention rather than a structural impossibility.

**One convergent result is worth stating separately, because it repeats in all five new markets without a merged denominator.**
In Singapore, Hong Kong, the Philippines, Vietnam and Indonesia, the F&B/QSR bucket contains **zero REP=yes rows**, market by market.
Hong Kong's one independent F&B row (蓮香樓 x LuLu) is REP=no; Singapore's (Starbucks x mofusand) is REP=no; the Philippines' (Jollibee x Adarna House) is REP=unclear; Vietnam's and Indonesia's buckets are 0 of 3 and 0 of 9.
That is five markets stated five times rather than one pooled figure, because the buckets are not identically defined.

### 5.2 Format mix per market, and where the vocabularies refuse to merge

| Market | What leads | Evidence |
|---|---|---|
| **Hong Kong** | **Leasable atrium.** Mall pop-up and mall campaign 32 rows plus retailer and department-store pop-up 21 = **53 of 93 (57.0%)**; add café and venue and it is 71.0%. Festival Walk hosts eight rows, Langham Place five. | Counted table, `hongkong/_VERDICT.md` §3. "The densest single-format concentration measured in the series." |
| **Indonesia** | **Malls are the spine.** Mall, venue and themed-space activation **28 of 102 (27.5%)** across at least fourteen distinct operators. | Counted table, `indonesia/_VERDICT.md` §3. Also "the most accessible format for an independent, holding 3 of the 14 independent-or-mixed rows." |
| **Philippines** | **Mall operators.** Mall/venue pop-up, installation and activation **26 of 82 (31.7%)**, zero independent. SM Supermalls, Ayala Malls, Robinsons, Megaworld, Araneta, Fisher Mall. | Counted table, `philippines/_VERDICT.md` §3. "Mall-operator density is this market's defining structural feature and it is a completely closed format to indies." |
| **Singapore** | **Character IP as footfall infrastructure.** Venue/attraction/airport/touring 16 plus mall 15 = **31 of 81 (38.3%)**; add themed cafés and it is 48.1%. Changi Airport four times, Wong Fu Fu four times. | Counted table, `singapore/_VERDICT.md` §3. "No other market in the series concentrates this heavily in venue formats." |
| **Vietnam** | **Licensed retail drops**, 17 of 47 (36.2%); mall/venue second at 10 (21.3%). | Counted table, `vietnam/_VERDICT.md` §3. |
| **Thailand** | **Licensed goods and mall experience, not F&B.** Product/licensed goods 38.6%, experiential 25.3%, F&B 10.8%. | Counted table, `thailand/_VERDICT.md` §3. "The sharpest format divergence from the prior markets in the series." |
| **Malaysia** | **Retail and FMCG, not F&B.** Retail/FMCG/supermarket 25 rows, cafe/bubble tea 21, convenience 13, mall/venue 13, QSR 12. | Counted table, `malaysia/_VERDICT.md` §3, **pre-re-sweep n=103, not recomputed**. |
| **Taiwan v2** | Convenience-store 集點, handshake-drink chains, cosmetics, plus a venue/pop-up circuit the re-sweep partly opened. | Vein description, `taiwan-v2/_VERDICT.md` §5 + addendum. |
| **Japan** | Lifestyle retail (Loft, Village Vanguard, Don Quijote, Kiddy Land), illustrator apparel/stationery, CVS art capsules, cosmetics/variety, plus the illustrator pop-up circuit, standing brand creator-programmes and transport/tourism from the re-sweep. | Vein description, `japan/_VERDICT.md` §4 + addendum. |
| **Korea** | Beauty (the Olive Young rollout machine), apparel (SPAO), convenience, and distinctively KBO/K-League sports-club merch, plus mid-market apparel, hardware/houseware, cinema exhibition and K League from the re-sweep. | Vein description, `korea/_VERDICT.md` §3-4 + addendum. |

**Mall-led is now the dominant shape of the series' second half, and the mall is simultaneously the most divergent bucket in it.**
All five new markets are mall-or-venue-led.
And the same bucket has opposite class composition across the ten:

- **First-class independent channel:** Thailand, where Siam Piwat, The Mall Group, Central, ICONSIAM, Future Park and Jungceylon account for most of the market's 9 independent experiential rows, and "Thai malls are a first-class licensing channel in a way they were not in Malaysia."
- **Open:** Hong Kong (5 of 13 independent rows are mall), Indonesia (3 of 28, its most accessible format), Taiwan (the venue/pop-up circuit supplied 7 of the 9 rows its re-sweep added).
- **Completely closed:** the Philippines (0 of 26) and Vietnam (0 of 10), in two of the densest mall scenes in the region.
- **Portfolio-driven growth:** Malaysia, where mall/venue growth is "driven almost entirely by POP MART's nine-store footprint and the Pokemon Truck tour".
- **Marginal:** Singapore, whose one independent mall row (33, Mr Merlion Hawker Fest) is REP=unclear.

Same format bucket, opposite class composition, in ten markets on one definition.
**That is why the merged table is refused above and why the per-market cut is the only honest presentation of it.**

**The recurring non-lifestyle format is still the most agency-shaped thing the series has found**, and it did not extend into the new five.
Japan has Pixio (four named freelance illustrators), CyberAgent's Pigg Party (寺田てら) and Superbag (mame), which Japan's addendum calls "the single most PBC-shaped format found in the whole Japan build."
Korea has Epson Korea's label-printer editions with three named illustrators, 락앤락 x 벌룬프렌즈 and 프린팅박스 x 해요.
Malaysia has Rip Curl's quarterly "Artist of the Search", Skechers' SkechVibe and Montigo x Humana Art.
No standing, recurring, individually-contracted creator programme of this shape appears in Singapore, Hong Kong, the Philippines, Vietnam or Indonesia.
Indonesia has the nearest thing and it is not standing: its independents are commissioned one-off by "mid-size Indonesian consumer brands that need a look", against portfolios licensed by "large brands that need a face".

### 5.3 Concentration, and the verbatim rule applied to the new five

Two concentration findings from the original five were tested against an artist-side instrument and held.

**Thailand: Butterbear, 17 of 83 rows (20.5% of the census).**
Measured on an artist-side instrument from the start, so not exposed to the query-artefact rule.
1 row in 2024, 12 in 2025, 4 in 2026YTD, across 15 distinct licensee brands, each separately sourced, spanning eleven categories.
Rated **High** confidence as a genuine structural feature.
Note what it is: a corporate-owned mascot licensed out, PORTFOLIO under the pinned Malaysia row 8 call, not an indie success story.

**Taiwan: Bugcat Capoo.**
8 of 35 indie rows pre-re-sweep, and post-re-sweep still 8 of the 17 REP=no rows.
Taiwan's re-sweep was the null result, so this concentration was measured with the artist-side net in hand and did not dissolve.
Capoo is creator-owned, and the concentration matters because the owner runs licensing through his own captive studio (卡特島創意), which is what makes Taiwan's most prominent indie IP unaddressable.

**The new five change the series record on the portfolio side, and Hong Kong takes it.**

Hong Kong's portfolio concentration is "the most extreme in the series" and the numbers are counted, not asserted: three licensors account for 34 of 93 rows (36.6%), namely **Chiikawa 12, Disney 12, Sanrio 11**; adding Doraemon (7), Harry Potter (4), Crayon Shin-chan (3), Snoopy (3) and Pokémon (3) gives an imported-portfolio core of **54 of 93 rows (58.1%)**.
(Its verdict gives the three-licensor figure twice, as 36.6% in section 1 with the Sanrio x Chiikawa joint line at row 44 counted once, and as 37.6% in section 4a without that merge. The merged figure is used here and the unmerged one appears only inside the quotation below.)
**Chiikawa alone is 12.9% of every campaign in the market.**
Its verdict draws the classification consequence: "The pinned ナガノマーケット rule therefore does more classification work in Hong Kong than anywhere else in the series, and a meaningful part of HK's portfolio share is a Chiikawa artefact."

Vietnam's is second and differently shaped: five licensor families account for **31 of 47 rows (66.0%)** with no row counted twice, and the most-used single IP by Vietnamese brands is Liên Quân Mobile (4 rows), a Tencent/TiMi title published locally by Garena.
Its verdict: "a brand wanting a character in Vietnam is choosing from a very short list."

**Two independent-side concentration findings appear in the new five, and the verbatim rule cuts them differently.**

**Hong Kong: LuLu the Piggy, 6 of 13 independent rows, one label.**
The rule does not dissolve this one, because the artist-side instrument was aimed straight at it - but that same fact is a caveat in the opposite direction, and Hong Kong's verdict states it: "five of the seven 2026 independent rows are LuLu the Piggy and LeonLollipop campaigns that the second tranche went looking for."
So Hong Kong's independent concentration is query-shaped, and uniquely in the series the query artefact runs *toward* concentration rather than away from it.
What the rows themselves show is unaffected: six rows across a silverware house, a suburban mall, a Halloween pop-up, a LOG-ON shrine, a century-old Cantonese teahouse and Hong Kong's first LuLu café.
And the label-economy finding is a negative one worth carrying: **How2work, Kennyswork and ToyQube produced zero adjudicable campaign rows in either tranche**, so Hong Kong's captivity number is "one label, not a label economy".

**Indonesia: Muklay 4 of 14, two creators 43% of the independent side.**
**This one the rule kills, and Indonesia's own verdict agrees.**
Its independent channel was discovered in the final tranche and immediately produced five of thirteen independent rows; six further independent campaigns by the same creators sit just outside the window in the same publisher tier; the verdict's instruction is "read the addressable count of eight as a floor".
A concentration claim measured on a channel found in the last tranche of three is exactly the class of claim the rule was written for.
What survives is the *portfolio*-side consolidation finding, which is counted and which is Indonesia's real structural result: **Tahilalats appears on ten rows** spanning airline livery, aircraft interior, carmaker campaign, metro retail store, mall installation, FMCG packaging, footwear, motorcycle, state tourism activation and taxi brand, and "No independent creator in this census appears on more than four, and none appears in more than three formats."
Its conclusion: "Domestic character IP in Indonesia is commercially strong, reaches the top of the market, and gets there **after** being aggregated."

**The Philippines has no concentration finding to test**, and that is itself a result: 0 REP=no rows, no Toyzeroplus-equivalent, and "there is no PH agency or label holding a stable of local character IP under exclusive commercial terms that this sweep could find."

**The pattern across ten markets is legible.**
Concentration claims about a *portfolio* IP's licensing footprint (Butterbear, Chiikawa, Tahilalats, Liên Quân Mobile) survive, because brand-side querying sees those things well.
Concentration claims about a *named, already-visible* indie's captivity (Capoo, LuLu) survive, for the same reason.
Concentration claims about *the size of the addressable creator bench* do not survive (Korea, Malaysia, and now Indonesia), because that is precisely what brand-side querying cannot see.

### 5.4 The own-mascot exclusion as a market feature

The Philippines' verdict named this and it turns out to be a cross-market variable rather than a Philippine quirk.

**The Philippines has the largest excluded own-mascot class in the series**, and the exclusion "removes more of this market's most visible character marketing than in any of the seven earlier markets": Jollibee's own stable (Jollibee, Hetty, Popo, Yum, Twirlie, Bee Happy) across Kids Meal, JolliBINI and anniversary programmes; Jollibee licensed *out* to Good Smile Company as a Nendoroid; McDonald's Philippines' own blind box.
The sharpest single case in the series sits here: **Potato Corner x Baby POCO blind boxes** (2026-04, P149, five plush designs, 100 Golden Pocos), where "the exclusion removes a campaign running the exact blind-box mechanic the census exists to count, purely because the brand owns the character."
Its verdict is careful about the direction: the excluded mascots are all brand-owned, so the exclusion removes only portfolio-adjacent campaigns and does not suppress the independent count.

**Singapore's analogue is the food-plushie wave, and its verdict calls it out as load-bearing on how 8.6% is read.**
More than twenty campaigns (MILO, KitKat, Magnolia, Skippy, Tai Sun, Gardenia, Prima Flour, Pizza Hut, Genki Sushi, McDonald's Prosperity Pals and Pocket Pouch, Toast Box x Horlicks, LiHO, Haidilao, Beutea, CHAGEE Bestea, Yeo's x FairPrice zodiac) are excluded because no third-party character licensor is involved.
Its reading: "Singapore has an enormous collectible-plushie appetite that is being met by brands' own in-house design rather than by licensing a creator's character.
That is the commercial shape of the same finding as section 4a."

**Vietnam and Indonesia both applied the rule and both report it as small.**
Vietnam: Vietjet's "Amy" panda, and "smaller in this market than in the Philippines, because Vietnamese brands run fewer proprietary character mascots than Philippine QSR does."
Indonesia: applied and tested at row 72, where KFC's own Chaki would not count but the licensed-in Bobo character does.

**The pattern is worth naming because it is not accidental.**
The two markets with the thinnest addressable layers on the full instrument (Singapore, 1 addressable creator; the Philippines, 6 addressable rows in 82) are also the two markets where the largest excluded class is brands designing their own characters instead of licensing one.
That is a demand-side observation, not an outcome claim: the appetite for collectible character marketing is present in both markets and is being met in-house.

### 5.5 Where the vocabularies do not map, and what is refused

Three merges are refused in this document, each with the mapping problem stated rather than solved.

1. **A pooled cross-market indie ratio** (section 1): depth spread 47 to 158 rows, two different denominator conventions.
2. **A series-wide distinct-creator total** (section 1): three different units and creators recurring across markets.
3. **A merged ten-market format-by-class table** (section 5.1): bucket vocabularies that do not correspond, one market's table computed on a superseded row set (Malaysia, n=103), and three markets that never produced a counted table at all.

One further merge is refused in section 3.5: **a single before-and-after instrument-sensitivity chart across ten markets**, because four markets carry a keyword-class re-sweep, one carries a within-build two-pass comparison, three carry adjudication-tranche splits and two carry corpus-expansion drift, and those are four different experiments.

---

## 6. Per-market one-page reads

### Japan - n = 146

- **Shares:** PORTFOLIO 94 (64.4%) / INDEPENDENT 51 (**34.9%**) / UNCLEAR 1 (0.7%). Correction +4.4 from 30.5%.
- **Addressable:** 26 REP=yes rows, **17.8% of all campaigns**. `[derived]` distinct: 25 entries, four of them multi-illustrator rosters. REP split 26 yes / 9 no / 16 unclear.
- **Mechanism: channel.** Campaigns named after the artist are unreachable by a brand-side query by construction.

Sharpest findings:

1. **Fame does not equal representability.** The viral SNS-character indies (mofusand, Opanchu Usagi, Kanahei, Colorful Peach) are exactly the ones locked to captive studios or master licensors and score REP=no. The cleanly addressable pool is the quieter individual-illustrator tier doing open non-exclusive brand collabs.
2. **Indies reach the largest brands, repeatedly.** Higuchi Yuko, a living self-owned painter, ran campaigns with both Lawson and Morinaga. foxco reached Calbee; foxy reached CASETiFY; Yuhachi reached Bandai Gashapon; Oono Taro reached 3COINS.
3. **The re-sweep opened two formats the original pass had no read on**: standing brand creator-collaboration programmes (Pixio, Pigg Party, Superbag) and transport/tourism (JR東海's 推し旅 built a prefecture-wide campaign around one illustrator).

Caveats:

- **The largest artist-side yield in Japan was not indie.** It was portfolio IP paired with a commissioned illustrator, excluded by rule and named campaign by campaign.
- **REPRESENTABLE is the softer call**: 16 of 51 indie rows are REP=unclear because exclusivity is rarely public, so 17.8% is a conservative floor.
- **Aggregator dependence rose in the re-sweep**: 9 of the 15 new rows rest on collabo-cafe alone, each flagged.
- **No 2024 rows were added**, so 2024 is the only year the correction did not touch.
- One marginal format was admitted and flagged (row 142's promotional shopper bags); a stricter reading gives 34.5%.

### Korea - n = 158 (classifiable 156)

- **Shares:** PORTFOLIO 96 (61.5%) / INDEPENDENT 53 (**34.0%**) / UNCLEAR 7 (4.5%). Correction +9.2 from 24.8%.
- **Addressable:** 28 REP=yes rows, **17.7% of all campaigns**. **17 distinct creators, up from 7.** REP split 28 yes / 10 no / 15 unclear.
- **Mechanism: segregation.** A creator-facing trade magazine indexed by creator and IP owner, which no brand-side query class touches.

Sharpest findings:

1. **The missing campaigns were in an untouched *publication*, not an untouched format.** 아이러브캐릭터 supplied 17 of the 23 appended rows, and essentially none appear in the ko lifestyle/beauty/brand press the original pass swept.
2. **The dual portfolio wall is distinctive and untouched by the re-sweep**: foreign licensors (Sanrio, Pokemon, Disney, and newly Netflix screen IP) plus domestic platform owners (Kakao Friends, LINE Friends/IPX, Iconix, SAMG, HYBE, Devsisters).
3. **Indie IP reaches professional sport and national retail.** 무직타이거 on a first-division K-League match-day kit (Ulsan HD); 최고심 with LG Twins and 깜자 with SSG Landers (KBO); 망곰이 across Olive Young, SPAO and CU.

Caveats:

- **"Indie share sits at about a quarter" is superseded by the census's own addendum**: it is about a third.
- **Single-publication dependence is worse than Japan's**: 17 of 23 new rows rest on one outlet.
- **Ownership evidence is thinner on the appended block**: 9 of the 20 new indie rows are REP=unclear, and one row is IP-class UNCLEAR.
- **2024 remains the thin, under-corrected year** (only 3 of 23 new rows).
- **Window-boundary caveat:** several of the most representable indies ran their biggest institutional collabs *before* the 2024-01 window, so their true footprint is larger than this window captures.
- Two marginal formats admitted and flagged; a stricter reading gives 33.1%. 틴틴팅클 (row 152) is flagged rather than buried.

### Taiwan v2 - n = 138

- **Shares:** PORTFOLIO 95 (68.8%) / INDEPENDENT 38 (**27.5%**) / UNCLEAR 5 (3.6%). Correction +0.4 from 27.1%.
- **Addressable:** 18 REP=yes rows, **13.0% of the census**, but **17 of 25 distinct indie IPs (68%)**, the highest open-rate per distinct IP in the series. REP split 18 yes / 17 no / 3 unclear, a 44.7% captivity rate second only to Hong Kong.
- **Mechanism: none of the above.** The control case, and a *coverage* null.

Sharpest findings:

1. **The volume/distinct gap is the whole Taiwan story.** Only 13.0% of campaigns are addressable, because Bugcat Capoo (self-licensed through 卡特島創意) drives 8 of 17 REP=no rows, and Kanahei, mofusand, 黃阿瑪, Kusama and LuLu are each captive in their own way.
2. **Indies win Taiwan's highest-prestige formats.** A 7-ELEVEN x 國立故宮博物院 7,100-store 集點 wave, a listed FHC's shareholder gift, the national postal service, 台北101's observatory, CeraVe and Sulwhasoo.
3. **The addressable bench is split domestic/inbound**: roughly five open Taiwan-origin creator IPs plus eight foreign indies active in Taiwan.

Caveats:

- **v2 was a re-classification, not a re-discovery** (until the re-sweep), so it inherits v1's coverage.
- **Sample skew likely understates rather than overstates indie share.**
- **Dateless indie candidates remain excluded and listed**, so 27.5% is a floor. One dated row is left unclassified rather than guessed.
- **REPRESENTABLE is directional guidance, not a legal finding** - the Capoo=no call drives most of the "no" volume.

### Malaysia - n = 124

- **Shares:** PORTFOLIO 92 (74.2%) / INDEPENDENT 31 (**25.0%**) / UNCLEAR 1 (0.8%). Correction **+12.4** from 12.6%, the largest in the series.
- **Addressable:** 20 REP=yes rows, **16.1% of the census**. **14 distinct creators, up from 4.** REP split 20 yes / 1 no / 10 unclear.
- **Mechanism: erasure**, plus the Japan channel mechanism imported through brand creator-programmes.

Sharpest findings:

1. **The undercount was an entire format and an entire channel.** The festive packet (sampul Raya, CNY angpao given with purchase) is Malaysia's densest local-creator format and its brand-side coverage names no illustrator anywhere; eight rows rest on two URLs.
2. **"Four names, not a scene" was a brand-side artefact.** Fourteen distinct creator-owned IPs reached a national brand inside the window.
3. **Malaysia has no creator-facing character-industry trade publication**, and that absence is itself the finding. Its payments-card vein is unique in the series for depth, and unlike Thailand's it is open to indie IP.

Caveats - Malaysia is the least settled of the original five:

- **The honest range is 18.4% to 25.0%.** Ten of the 18 new indie rows are the definitional frontier. Both ends of that range destroy the pre-re-sweep finding.
- **The dateless backlog grew rather than closed**: seven Touch 'n Go creator cards plus roughly seven further social-evidence-only campaigns, worth about four points.
- **Source concentration is the structural weakness**: 72 of the original 103 rows from everydayonsales.com (69.9%); 8 of 21 new rows on two Marketing-Interactive URLs; 9 of 21 single-source.
- **The 2026 skew is an artefact, not a surge.**
- **The zh-language Malaysian press was swept only lightly.**
- **Social-only evidence remains uncounted and it censors indie rows specifically.**
- Four BM-language rows carry translation-confidence flags (confidence high in each). **The format table in its verdict is pre-re-sweep (n=103)** and was not recomputed.

### Thailand - n = 83

- **Shares:** PORTFOLIO 66 (79.5%) / INDEPENDENT 17 (**20.5%**) / UNCLEAR 0. No correction: artist-side from the start, and the reference market for the whole series.
- **Addressable:** 11 REP=yes rows, **13.3% of the census**; `[derived]` 9 distinct creators, 10 of the 11 rows Thai. REP split 11 yes / 1 no / 5 unclear.
- **Mechanism: erasure** - the market where it was discovered.

Sharpest findings:

1. **The keyword finding itself**, the most transferable result in the series: 9.3% brand-side, 20.5% with artist-side terms added, same two trade titles.
2. **The channels that scale are closed**: retail/CVS/e-comm, banking and fintech are 17 rows and 0 indie, while experiential is 42.9% indie. Thai malls are the buy side for indie IP.
3. **The addressable layer is domestic, individual and named in the press**, and two creators recur across four large corporates: BABYBOY/StupidnoobMacc (LG, CPF) and Bad Meaw (Samsung, AIS). Both recurrences are ad-hoc, with no agency named in any of the four sources.

Caveats:

- **The thinnest census of the original five** - 83 rows against 124-158 - and its verdict says a credible sample of a market that would support 120-140 rows.
- **Single-source rate 73 of 83 (87.9%).**
- **8 rows carry a `TH-src (low conf)` translation flag**, two on indie class calls. Reclassifying both moves 20.5% to 18.1%; dropping all four illustration-IP rows moves it to 17.7%. The finding survives both stress tests.
- **Named holes:** brand Facebook pages completely unswept (the largest known gap and the one most likely to *suppress* the indie share); two of four trade titles unsweepable; LINE Creators Market rosters unswept; Lotus's contributes zero rows, which is not a plausible true value.
- One judgement call is named as contestable rather than hidden (Watsons x Artstory by Autistic Thai, excluded as a CSR art programme).

### Hong Kong - n = 93

- **Shares:** PORTFOLIO 78 (83.9%) / INDEPENDENT 13 (**14.0%, floor 2.6% / bounded above at 14.0%, biased upward**) / UNCLEAR 2 (2.2%).
- **The tranche composition, which travels with the number:** rows 1-77 brand-side, date order, **2 independent in 77 (2.6%)**; rows 78-93 artist-side-first, **11 independent in 16 (68.8%)**. A **26-fold** hit-rate spread on the same market in the same window, which its verdict calls the census's largest finding.
- **Addressable:** 5 REP=yes rows, **5.4% of the census** `[derived arithmetic]`; **6 distinct creators**, five of them Hong Kong creators and all six named individuals. REP split 5 yes / 6 no / 2 unclear, the highest captivity rate in the series at 46.2%.
- **Mechanism: crowding-out**, a fifth pattern the four-mechanism taxonomy did not contain.

Sharpest findings:

1. **The census's own instrument broke twice and was rebuilt mid-run.** The WP-REST portal vein that built six earlier markets does not exist in Hong Kong; the Google News RSS vein that replaced it was resolvable only through Google's `batchexecute` endpoint, which hard-blocked this client after 302 of 781 candidates.
2. **Portfolio concentration is the most extreme in the series.** Chiikawa 12 rows (12.9% of all campaigns), Disney 12, Sanrio 11; three licensors 36.6%; imported-portfolio core 54 of 93 (58.1%).
3. **The label-captive hypothesis is confirmed and is one label, not a label economy.** All six REP=no rows are Toyzeroplus/LuLu. How2work, Kennyswork and ToyQube produced zero adjudicable campaign rows in either tranche.
4. **Transit and attraction licensing is a closed door to local creators**, and its verdict calls that "a cleaner statement of the addressability problem than the ratio is."

Caveats:

- **The two-tranche composition is not a footnote, it is the number.** Never quote 14.0% without it.
- **479 of 781 harvested candidates were never resolved** to a publisher URL. They still hold a title, publisher and date, and the title-search route works, so "**That, and only that, is why n is 93 rather than 130.**"
- **Do not read a trend off the per-year table.** "The year split measures reading order, and this is the market where that is most true."
- 57 of 93 rows single-source (61.3%), materially better than Singapore's 90.1%. Six rows carry a non-HK publisher flag; three carry thin-source or venue-thin flags.
- **Two UNCLEAR ownership rows**, both 2024, both resolvable in principle: a third (row 16) was resolved during the run by an unrelated 2026 row.
- **The rejection the cross-border rule cost is listed rather than quietly kept**: OCTO Gambol x 寂寞鱷魚, an HK label's first collaboration with a named HK illustrator, rejected because the only located source is Taiwanese with NT$ pricing. Six named HK creators sit in two rejections.
- Blocked or unsweepable: Marketing-Interactive; brand, mall and creator Instagram/Facebook entirely unswept (two of the six addressable creators use IG/FB as their primary announcement channel); site-wide search unavailable on eighteen further named titles.
- Removing three flagged borderline rows moves the indie share from 14.0% to 14.4%.

### Indonesia - n = 102

- **Shares:** PORTFOLIO 88 (86.3%) / INDEPENDENT 13 (**12.7%**) / MIXED 1 (1.0%) / UNCLEAR 0. Counting the MIXED row on its Si Juki side gives 14 of 102 (13.7%), the upper bound of any reasonable counting convention. Read 12.7% as **a floor with a soft ceiling near 20%**.
- **Addressable:** 11 REP=yes rows, **10.8% of the census** `[derived arithmetic]` (12 rows / 11.8% counting the MIXED row). **8 distinct REP=yes creators**: Muklay, Darbotz, Hari Prast, Abenk Alter, Arkiv Vilmansa, Ykha Amelz, ARDNEKS, Faza Meonk. REP split 11 yes / 0 no / 2 unclear.
- **Mechanism: two-channel licensing** - the answer to the fifth-pattern question, and not the pattern that was predicted.

Sharpest findings:

1. **Two licensing economies in one market that barely touch.** A portfolio channel (global IP plus domestic IP aggregated into a corporate holder) reported by mainstream news, business and brand trade press; an independent channel (individually practising illustrators and art-toy artists licensing artwork to mid-size brands) reported **only** in the youth-lifestyle portal network, continuously since at least 2020. They overlap in exactly one place in 102 rows: row 2, where Shopee put Si Juki next to Garfield.
2. **Consolidation is the second half of the mechanism and it is well evidenced.** Tahilalats appears on **ten rows** across ten formats under INFIA Corp; no independent creator appears on more than four rows or in more than three formats. "Domestic character IP in Indonesia is commercially strong, reaches the top of the market, and gets there **after** being aggregated."
3. **The closed formats are measured, not assumed**: F&B/QSR 0 of 9, beauty 0 of 7, convenience 0 of 2, banking 0 of 1, games 0 of 3, and telco/e-wallet **no rows at all** after three instruments and three tranches. Independents get commissioned by "mid-size Indonesian consumer brands that need a look"; portfolios get licensed by "large brands that need a face".

Caveats:

- **The tranche caveat is the verdict's own headline caveat.** 32 rows, then 61, then 102: "Two of the three tranches produced their rows from an instrument the previous tranche had recorded as unavailable, and in both cases the record was an untested assumption rather than a measurement. That is the single most important caveat on everything below."
- **The INFIA call is the load-bearing uncertainty and it is worth ten rows.** Classed PORTFOLIO on four independent pieces of evidence, with the residual doubt recorded: "If that turned out to be so, ten rows move to INDEPENDENT, the overall share becomes 23/102 = 22.5%... The whole verdict hangs on this call and it should be flagged as such to anyone using the number."
- **The independent layer is artwork, not character IP.** Eleven of the fourteen independent-or-mixed rows are an individual artist licensing artwork onto a product or a space. The only creator-owned character IPs are Si Juki (rows 2, 68) and the three comic IPs on row 77, and none has a repeat brand programme in the window.
- **Concentration on the independent side is extreme and is a query artefact by the series' own rule**: Muklay 4 of 14, two creators 43%, seven of twelve creators appearing exactly once, on a channel discovered in the final tranche.
- **Single-source rate 72 of 102 (70.6%)**, and partly structural: "Indonesian brand PR is distributed to many outlets that reproduce it near-verbatim, so a second source is often the same press release rather than independent confirmation."
- **Translation confidence high on all 102 rows, no row flagged lower.** Bahasa Indonesia has no diacritics, so Vietnam's whole class of accent-collapse false friends does not exist; the Indonesian risk is semantic (`karakter` usually means personality) and was handled at the filter.
- **Activation flags:** 7 rows flagged (2 weak, 5 moderate), all PORTFOLIO. Strict and permissive readings bracket the headline at 12.7% to 13.7%; a permissive reading of six held-out global campaigns gives 12.0%.
- **Named holes:** artist-side non-press channels (Instagram, TikTok, Behance, creator newsletters) entirely unswept and the hole that matters most; the INFIA ownership question; `tribunnews.com` and `kumparan.com` unswept; mall operators' own channels; INFIA's own pipeline; Alfamart measured empty across three instruments but "unproven rather than established"; four marketing trade titles partly or wholly unreachable; regional and non-Jakarta activity thin, and "the hole most likely to hide *independent* rows other than the artist-channel hole".

### Singapore - n = 81

- **Shares:** PORTFOLIO 74 (91.4%) / INDEPENDENT 7 (**8.6%**) / UNCLEAR 0. Zero UNCLEAR ownership rows, "a property of the market, not of the effort".
- **Addressable:** 1 REP=yes row, **1.2% of the census** `[derived arithmetic]`; **1 distinct creator**, Tobyato (Toby Tan). REP split 1 yes / 2 no / 4 unclear, the highest unclear rate in the series at 57.1%. Realistic ceiling 3 creators and 5 of 7 rows if Play Nation and Mr. Merlion & Friends resolve to non-exclusive.
- **Mechanism: direct-to-consumer substitution** - closest to the Taiwan-class null but by the opposite route.
- **First market in the series to run both keyword classes from birth.** "That makes Singapore's indie number the series' first number that was never corrected upward."

Sharpest findings:

1. **A supply null, not a coverage null.** The two query classes do not overlap at all in Singapore: the artist-side class returns a completely different corpus, and that corpus is not brand-collaboration coverage. Ten artist-side keywords across five portals over 31 months returned **exactly one** brand x local-illustrator campaign in the window.
2. **The creator-owned character layer exists and does not license.** Tasty Toastys, Tap Space, Play Nation and Mr. Merlion & Friends all appear in the press as founder profiles, and every one monetises through its own retail and its own pop-ups. The two independent IPs that made the table were found by **brand-side** queries, "the exact inverse of Thailand".
3. **Character IP as footfall infrastructure.** 31 of 81 rows (38.3%) are mall, airport, attraction or touring pop-up; 48.1% adding themed cafés. Changi Airport four times.
4. **The collectible appetite is met in-house.** More than twenty brand-own food-plushie campaigns excluded under the own-mascot rule, which its verdict says directly "matters for how the 8.6% is read".

Caveats:

- **The mechanism read is provisional on one blocked vein.** Marketing-Interactive, Singapore's principal marketing trade title, serves a JS-rendered search and exposes no WP REST endpoint. "The mechanism finding in section 4a is provisional on this: a channel or erasure correction from that title is possible and would raise the indie share. Nothing else in this run would move the headline number as much."
- **73 of 81 rows single-source (90.1%), the highest rate in the series**, a structural consequence of five portals that rarely cover the same campaign twice.
- **The regional-HQ trap is this market's specific failure mode** and roughly a fifth of raw brand-side hits fell to it or to the out-of-market rule. Seven named rejections are listed; row 61 is retained despite being regional because Singapore is named with a launch date. "The test is activation evidence, not campaign geography."
- **Five reachable veins out of roughly a dozen candidate titles** is why n is 81 rather than 130. Mothership, The Straits Times, SethLui, Daniel Food Diary, TimeOut Singapore, AugustMan and HoneyKids Asia all blocked.
- **Brand and mall social accounts entirely unswept**; design and illustration press, artist Instagram, Singapore Art Book Fair and Pop Toy Show rosters and local designer-toy shops all unswept, "and if the indie layer is licensing-facing anywhere, it is there."
- **2024 is thin at 13 rows** versus 43 for 2025 and should not be quoted on its own.
- Two ownership questions are open and cheap to close (Play Nation, Mr. Merlion & Friends), and closing them is a threefold move on the number this census exists to produce.

### Philippines - n = 82

- **Shares:** PORTFOLIO 75 (91.5%) / INDEPENDENT 7 (**8.5%**, mildly biased upward) / UNCLEAR 0.
- **Tranche caveat, milder than Hong Kong's:** rows 1-52 hold 3 independent in 52 (5.8%); rows 53-82 hold 4 in 30 (13.3%). Roughly 2.3x, against Hong Kong's 26x. "A purely brand-side census of this market would have reported something closer to 6%."
- **Addressable:** 6 REP=yes rows, **7.3% of the census** `[derived arithmetic]`; **14 named distinct creator entities**, explicitly a floor. REP split 6 yes / 0 no / 1 unclear.
- **Mechanism: naming and retrievability as separate variables.**

Sharpest findings:

1. **No independent row is label-captive** - 0 REP=no rows, and no Toyzeroplus-equivalent exists. The one non-`yes` row is `unclear` for the opposite reason: Jollibee x Adarna House puts the rights with an independent *publisher* managing many authors' work, so there is no single creator to represent.
2. **Press names creators well and a brand-side sweep still misses ~40% of the independent layer**, because the *brands* doing independent work (Looking for Juan, UNICEF Philippines, New Era) are on no brand-side list this series uses. Six of the seven independent rows carry the creator's name in the headline or lede.
3. **The closure of the high-distribution formats is the most complete in the series.** Mall 26 rows and zero independent; live show 12 and zero; device 6 and zero; telco 2 and zero. "The one telco campaign that did reach for Filipino illustration reached for dead illustrators" - Globe AT HOME licensed four deceased National Artists from their estates.
4. **Komiks is not yet a licensing culture.** Tarantadong Kalbo, Zsazsa Zaturnnah, Diwata Komiks and the Komiket circuit all surfaced repeatedly and not one attached to a brand campaign in the window.
5. **The own-mascot exclusion removes more of this market's most visible character marketing than in any earlier market**, and the sharpest case in the series sits here: Potato Corner x Baby POCO blind boxes, "the exact blind-box mechanic the census exists to count, purely because the brand owns the character."

Caveats:

- **`spot.ph` is unreachable at any URL from this client** - not just the REST endpoint - and it is the leading Philippine lifestyle title for this beat. "This is the single largest hole in the coverage claim."
- **Thirteen further named titles returned 403, 401 or 404**, leaving 20 portals of which 14 contributed: "the narrowest instrument of any market in this series that used the WP-REST method."
- **Instagram, Facebook and TikTok entirely unswept**, and this matters more here than anywhere else in the series because PH illustrators announce brand work on social rather than to press. The 14 is a press-only floor.
- **65 of 82 rows single-source (79.3%)**, a direct consequence of press-release-driven PH campaign news.
- **Regional and provincial press outside Metro Manila is thin**; provincial activations are almost certainly under-counted.
- **BusinessMirror requires retry, not a dead-link verdict** (randomly rotating 403s).
- Three rows carry runs beginning after the run date and are flagged in place. Row 19 (Space of BTS) is flagged as the census's weakest "character" call; dropping it raises the indie share to 8.6%.
- **The most important name in the addressable section has no campaign attached**: "Maria" by Klaris Orfinada, benchmarked against Labubu and Sonny Angel in its own press coverage.

### Vietnam - n = 47

- **Shares:** PORTFOLIO 43 (91.5%) / INDEPENDENT 4 (**8.5%**) / UNCLEAR 0. And the sharper number: **independent-character share 1 of 47 (2.1%)**, the lowest in the series, because three of the four independent rows are Vietnamese fine artists licensing an artwork or a design rather than character IP.
- **Addressable:** 4 REP=yes rows, **8.5% of the census** `[derived arithmetic]`; **4 distinct creator entities**. REP split 4 yes / 0 no / 0 unclear, the only market in the series with no captive and no unclear independent rows.
- **Mechanism: pre-formation.** "The market's credit behaviour and its distribution channels are ready before its independent IP supply is."
- **This market does not reach the ~80-row floor and the shortfall is the finding.** The target permits a documented coverage ceiling in place of the floor, and section 5 of its verdict documents one at measurement grade.

Sharpest findings:

1. **The coverage ceiling is measured on three independent quantitative lines.** Marginal yield is stable at roughly **one row per 110,000 Vietnamese article URLs**, holding to within 6% across two independent corpus expansions; reaching 80 rows would require ~3.6 million further URLs "from Vietnamese publishers that do not exist". The press vocabulary is about five names (Labubu 239, Baby Three 171, Barbie 114, Hello Kitty 66, capybara 45, then a cliff). And **23 properties that anchor multiple rows in Taiwan, Japan, Korea or Thailand appear not once in 2.6 million Vietnamese URLs.** "An instrument that can find one property 239 times and 23 others zero times is not failing to see; it is reporting an absence."
2. **The ratio did not move when the artist-side net was repaired.** 8.3% at 24 rows, 8.1% at 37, 8.5% at 47; tranche 3's artist-side pass returned 194 candidates after dedupe and produced exactly one row. "That stability is the strongest single piece of evidence that 8.5% is the market's number and not the instrument's."
3. **The counter-example that changes the read: Wolfoo (Sconnect) reaches a domestic FMCG brand's packaging** and scores PORTFOLIO. "The four independent creators are not blocked by a missing commercial bridge. They are on the wrong side of a **corporate-form** threshold: the domestic character IP that crosses into brand campaigns in Vietnam is the one owned by an animation studio with a rights department."
4. **Three creator-owned Vietnamese character properties have real public profiles and zero brand campaigns** in the window: Pikalong, Mèo Mốc, and Thỏ Bảy Màu outside row 7. The most-covered character-IP story of the window is not a campaign at all but the Sconnect v. Entertainment One litigation.
5. **Convenience and QSR produce zero rows of any kind** after twelve chains were swept by name across three waves, in the format that is the single densest in Taiwan, Japan and Korea.

Caveats:

- **Both Vietnamese marketing trade titles are 403 to this client at every path** (`brandsvietnam.com`, `advertisingvietnam.com`), retried with different user-agents and language headers, and a US-indexed web search reaches their article URLs so the content exists and the block is client-specific. "The mechanism call above therefore rests on consumer-press evidence alone." This is the Vietnamese form of the Thailand Positioning-Mag lesson.
- **Source concentration is worse than any earlier market's**: 13 distinct publisher domains, `kenh14.vn` alone supplying 24 of 97 cited URLs, 14 rows resting on kenh14 alone, and **27 of 47 rows (57.4%) resting entirely on titles inside the VCCorp network**, which share an editorial pipeline.
- **Republication is 30% of the candidate pool.** Deduplicating 3,486 fetched titles by normalised headline collapsed them to 2,436 distinct campaigns.
- **A dating trap applies throughout**: VCCorp article IDs normally encode publication date but aFamily's 236-prefixed IDs do not, and `kilala.vn` serves placeholder `datePublished` on a flat undated sitemap. Two convincing candidates proved to be 2021 on reading the body.
- **6 of 47 rows carry a translation-confidence flag** (2 high, 3 medium, 1 folklore-distinction). Both flags that matter for the verdict's conclusions are high and both are on independent rows.
- **The `linh vật` finding is worth carrying to the series**: it was carried into the lexicon as "mascot" and in Vietnamese practice almost always means municipal Tết statuary, so the Kumamon rule removes the largest character-adjacent category in the corpus.
- 32 of 47 rows single-source (68.1%), lower than the Philippines' rate as an artefact of republication.
- **Named holes:** the two trade titles; all social channels unswept, plausibly a larger share of campaign communication here than in any earlier market; the cinema-chain combo programme (zero rows, "a coverage gap, not a market finding"); the chain-coffee format's zero rows, "genuinely ambiguous" with MIXUE x Liên Quân Mobile the one data point on the other side; `vnexpress.net` effectively unswept; `dantri.com.vn` blocked; nine further titles unsweepable; the score 11-12 residual band of 429 entries unread.
- Three rows carry weaker VN-specificity and are flagged; dropping all three takes n to 44 and raises the independent share to 9.1%.

---

## 7. Caveats, carried verbatim and not softened

### 1. Per-year slices within markets are NOT trend-readable. The overall per-market shares are the numbers to quote.

From `RESWEEP_SUMMARY.md`:

> **The overall per-market shares are the numbers to quote across markets.
> The year trends within a market should not be read as growth.**

From `malaysia/_VERDICT.md`, on its own 2026 figure:

> Thirteen of 21 new rows are 2026YTD, and 2026's indie share jumps to 39.1%.
> That is almost entirely because the festive-packet roundups exist for CNY 2026 and Raya 2026 and were not found for 2024 or 2025.
> **The per-year trend line (16.0 -> 17.0 -> 39.1) should not be read as growth.** The overall 25.0% is the number to quote; the year series is now less trustworthy than it was before this pass, not more.

From `japan/_VERDICT.md`, on its pagination artefact:

> **No 2024 rows were added.** The artist-side index pages that carried this vein (collabo-cafe tag pagination) run newest-first and the pages read reached back to 2025-02.
> [...] so the 2024 vs 2025 gap in the per-year table is even more of a coverage artifact than before, not less.

From `thailand/_VERDICT.md`, whose per-year line reads as a collapse and recovery:

> **Do not report that as a market trend.** It is far more likely a sampling artefact, and the honest read is that this census cannot resolve a year-on-year indie trend for Thailand at all.

From `hongkong/_VERDICT.md`, where the artefact is reading order rather than pagination:

> **Do not read a trend off this.** The 2026YTD indie share is 29.2% because five of the seven 2026 independent rows are LuLu the Piggy and LeonLollipop campaigns that the second tranche went looking for, and the 2025 share is 6.7% because the second tranche found fewer 2025 artist-side candidates before the run ended, not because 2025 was a portfolio year.
> **The year split measures reading order, and this is the market where that is most true.**

From `singapore/_VERDICT.md`:

> the per-year-slices caveat carries: 2024 has only 13 rows and 2026 is seven months, so **the overall shares above are the quotable numbers** and the per-year splits are directional only

From `philippines/_VERDICT.md`:

> The trend line is upward across all three years, but on n=2, n=3, n=2 it is not a trend - it is three small numbers pointing the same way.

From `vietnam/_VERDICT.md`:

> On n=2, n=1, n=1 there is no trend to read and none is claimed.
> The only defensible per-year statement is that the independent layer is present in all three years and never exceeds two rows in any of them.

From `indonesia/_VERDICT.md`, which adds a market-specific form of the artefact:

> The Indonesia-specific addition is that the per-year split here is partly an artefact of *which instrument found which year*, not only of what the market did.
> [...] The honest reading of the per-year table is that the market's independent share is somewhere in the 8 to 20 per cent band with no established direction, not that it fell by half in 2025.

Korea's 2024 slice carries the same warning (only 3 of 23 new rows are 2024), and Taiwan's, Singapore's, Hong Kong's, the Philippines', Vietnam's and Indonesia's 2026YTD are all partial seven-month years.
**No per-year figure from any of the ten markets should be quoted as a trend.**

### 2. The instrument is common, but not uniformly deep - and the ten-market version of this caveat is stronger than the five-market one.

From `RESWEEP_SUMMARY.md`:

> The first caveat is that the instrument is common but not uniformly deep.
> Taiwan's leg added 9 rows and Korea's added 23, not because Taiwan has less indie activity but because Taiwan's brand-side pass had already caught most of it; the residual risk is that a market with a low correction was well-swept and a market with a high correction may still be under-swept.

> **The direction is right and the mechanism is evidenced; the magnitude is not a confidence interval.**

**The corrected-thin / measured-thin / instrument-bounded distinction (section 4.3) is the ten-market form of this caveat, and it must travel with any use of the addressability numbers.**
Only Singapore's 1 and Vietnam's 4 are measured on a full instrument.
Korea's 17 and Malaysia's 14 are corrections of numbers that were query artefacts.
Hong Kong's 6, the Philippines' 14 and Indonesia's 8 are floors set by named, quantified instrument limits, and all three verdicts say so.

**Three markets' instruments differ in kind, not only in depth, and that is new with this document:**

- **Hong Kong's instrument was rebuilt mid-run, twice**: "It is the first market in the series where **the method itself broke and had to be rebuilt mid-run**, twice, and both breaks are load-bearing on how the numbers below should be read." 479 of 781 candidates remain unresolved.
- **The Philippines' instrument is the narrowest in the series** among the markets that used the WP-REST method: "The census rests on 20 portals of which 14 contributed candidates - the narrowest instrument of any market in this series that used the WP-REST method", with `spot.ph` absent entirely.
- **Vietnam's instrument is a different method altogether** - a three-wave sitemap archive sweep of 2,607,744 URLs across 28 publishers, because both the WP-REST portal sweep and the Google News RSS fallback are dead there.

Malaysia remains the least settled of the original five (honest range **18.4% to 25.0%**, plus a named backlog worth about four points).
Each re-sweep and each tranche is also, by construction, a targeted vein rather than a random sample.
Japan's and Korea's addenda both say so in the same words: the post-re-sweep figure should be read as *the ratio after adding a channel (or a press vein) the first pass under-covered*, not as a random-sample correction of a biased estimate.
Indonesia says the same thing about its own three tranches, and adds the sharpest version of it in the series: "Two of the three tranches produced their rows from an instrument the previous tranche had recorded as unavailable, and in both cases the record was an untested assumption rather than a measurement."

### 3. These are sample censuses, not exhaustive counts.

Every one of the ten verdicts says this in its own opening lines.
Shares are estimates from a structured sample of press-visible campaigns, not population parameters.
Recall bias runs toward campaigns that got covered, and each verdict states which direction that biases its own number: Japan and Korea judge it a slight *inflation* of indie share (indie collabs skew press-friendly), Taiwan and Thailand judge it a *suppression*, Singapore, Hong Kong, the Philippines and Indonesia all state the direction of any correction as one-way upward, and Vietnam is the single exception that argues its own census is close to exhaustive - at measurement grade, on three quantitative lines, rather than as an impression.

Single-source rates, which are the clearest single index of per-row confidence, vary by 29 points across the series:

| Market | Single-source rows | Rate |
|---|---|---|
| Singapore | 73 of 81 | **90.1%** |
| Thailand | 73 of 83 | 87.9% |
| Philippines | 65 of 82 | 79.3% |
| Indonesia | 72 of 102 | 70.6% |
| Vietnam | 32 of 47 | 68.1% |
| Hong Kong | 57 of 93 | **61.3%** |

Japan, Korea, Taiwan and Malaysia do not state a single-source rate in the same form; Malaysia states that 9 of its 21 new rows are single-source and that 72 of its original 103 rows came from one domain (69.9%).

### 4. No outcomes anywhere.

From `RESWEEP_SUMMARY.md`:

> **What is not claimed anywhere in any of these censuses:** no outcome, no sell-through, no royalty, no performance figure, for any row in any market.

Each of the five new verdicts restates it independently.
The Philippines: "It does **not** support any claim about campaign outcomes, sales, footfall or performance - none is made anywhere in this file or the table."
Vietnam: "It does **not** support any claim about campaign outcomes, sales, footfall or performance. None is made anywhere in this file or the table."
Hong Kong adds the operational form of the rule: "where a source reported sales figures, queues or resale prices (rows 38, 60, 76, 85), the Notes say so and the figure is not carried."

This comparison inherits that standard without exception.
Nothing above is a claim about whether any campaign worked.
Every figure here counts *campaigns that provably happened and who owned the IP in them*, and nothing else.
Where a creator is described as reaching a national brand, that is a statement about a campaign existing, not about how it performed.

---

## 8. What's next

**The immediate next run is the `ip_scale_band` enrichment**, and it is the prerequisite for any banding use of this data.
Nothing in this document depends on it, and it is named here as a forward pointer from the commissioning task rather than from a census file: **`ip_scale_band` appears in no `_VERDICT.md`, no `campaigns.md` and not in `RESWEEP_SUMMARY.md`.**
Until it exists, the ten censuses support statements about ownership class, addressability and format closure, and they do not support statements banded by IP scale.

**The per-market named holes, in each market's own words.**

| Market | The holes that would move its numbers |
|---|---|
| **Thailand** | Brand **Facebook** pages completely unswept, the largest known gap and the one most likely to *suppress* the indie share; **LINE Creators Market** rosters unswept; two of four trade titles unsweepable (JS-rendered search, HTTP 403); Lotus's contributes zero rows, "which is not a plausible true value". |
| **Malaysia** | The **dateless backlog**, seven Touch 'n Go creator cards plus roughly seven social-evidence-only campaigns, worth about four points; the **zh-language Malaysian press**, swept only lightly; social-only evidence, which "censors indie rows specifically". |
| **Philippines** | **`spot.ph`**, unreachable at any URL and "the single largest hole in the coverage claim"; thirteen further titles returning 403/401/404; **Instagram, Facebook and TikTok** entirely unswept, in the market where illustrators announce brand work on social rather than to press; provincial press thin. |
| **Hong Kong** | The **479 unresolved candidates**, "the single biggest hole in this census, and they are recoverable" - each holds a title, publisher and date, the title-search route works, and working them "would plausibly take this market past the 120-140 target"; the **label economy beyond Toyzeroplus** (How2work, Kennyswork, ToyQube), "the highest-value question in the market and it is a two-or-three-document job"; **social entirely unswept**, biting harder than in Singapore because two of six addressable creators use IG/FB as their primary channel; **Marketing-Interactive** unreachable; eighteen further titles with no sweepable search. |
| **Indonesia** | **Artist-side non-press channels** (Instagram, TikTok, Behance, creator newsletters), "the hole that matters most"; the **INFIA ownership question**, "the one hole that could move the headline number by more than ten points in a single stroke", needing a share register or a licensing agreement rather than more press; `tribunnews.com` and `kumparan.com`; mall operators' own channels; four marketing trade titles; **regional and non-Jakarta activity**, "the hole most likely to hide *independent* rows other than the artist-channel hole". |
| **Singapore** | **Marketing-Interactive**, on which the mechanism finding is explicitly provisional and which "would move the headline number as much" as nothing else in the run; **design and illustration press, artist Instagram, art-book-fair and toy-show exhibitor rosters, local designer-toy shops** - "if the indie layer is licensing-facing anywhere, it is there"; the **two open ownership questions** (Play Nation, Mr. Merlion & Friends), a two-document job that moves the distinct addressable count from 1 to as many as 3. |
| **Vietnam** | **`brandsvietnam.com` and `advertisingvietnam.com`**, 403 at every path, "the two Vietnamese titles most likely to carry creator-credited campaign write-ups", with the mechanism call made without them; **all social channels**, plausibly carrying a larger share of campaign communication than in any earlier market; the **cinema-chain combo programme** (zero rows, "a coverage gap, not a market finding"); the **chain-coffee format**'s zero rows, genuinely ambiguous; `vnexpress.net` effectively unswept; the 429-entry score 11-12 residual band. |
| **Japan / Korea / Taiwan** | Japan's 2024 slice, untouched by the artist-side correction; Korea's 2024 slice and its single-publication dependence; Taiwan's dateless indie candidates and its one unclassified dated row. |

**Two structural follow-ups are named by the files rather than by this document, and both are cheap.**

1. **The two Singapore ownership questions and the Hong Kong label archives are document jobs, not sweeps.** Singapore's verdict: "it is a two-document job (ACRA filings, or a direct ask) rather than another sweep." Hong Kong's: "a two-or-three-document job - the labels' own release archives - rather than another sweep." Between them they resolve the addressable count in two markets.
2. **Indonesia's INFIA question is a share-register question worth ten rows and about ten points.** It is the single largest open number in the series.

**This document re-renders if markets are added or holes are filled.**
The ten markets measured here are the ones swept.
Every one of the nine mechanisms in section 3.6 is now a testable per-market prediction for any eleventh market, and the new question this document adds to that list is section 2.5's: **is the market's independent layer character IP or artwork, and if it is character IP, is it captive, consolidated, or routing direct to consumers?**
That question would have predicted four of the five new markets' positions before they were swept.
