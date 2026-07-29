# Artist-side keyword re-sweep - five-market summary

Run completed 2026-07-29.
Covers the artist-side re-sweep of Taiwan v2, Japan, Korea and Malaysia, with Thailand carried unchanged as the reference market.

**What the re-sweep was.** The Thailand census was the first in the series to be swept with artist-side keywords, and it found that brand-side queries had been undercounting indie campaigns by more than half - 9.3% on brand-side keywords alone, 20.5% once artist-side terms were added, with no change of source type, geography, definition or window.
The four earlier markets had been swept brand-side only.
This run re-swept each of them with the artist-side keyword class added, appending rows to the existing tables under the existing identical definition.
No table was rebuilt and no existing row was reclassified.

## Before and after

| Market | Pre-re-sweep n | Pre indie share | Post-re-sweep n | Post indie share | Correction | Rows added (indie / portfolio / unclear) |
|---|---|---|---|---|---|---|
| Thailand *(reference - artist-side from the start)* | 83 | **20.5%** | 83 | **20.5%** | - | - |
| Japan | 131 | 30.5% | 146 | **34.9%** | +4.4 | 11 / 4 / 0 |
| Korea | 133 classifiable | 24.8% | 156 classifiable | **34.0%** | +9.2 | 20 / 2 / 1 |
| Taiwan v2 | 129 | 27.1% | 138 | **27.5%** | +0.4 | 3 / 6 / 0 |
| Malaysia | 103 | 12.6% | 124 | **25.0%** | +12.4 | 18 / 3 / 0 |

Addressable indie (REPRESENTABLE = yes) as a share of the whole census:

| Market | Pre | Post | Distinct REP=yes creators, pre -> post |
|---|---|---|---|
| Japan | 16.0% | 17.8% | not re-counted |
| Korea | 14.1% | 17.7% | 7 -> 17 |
| Taiwan v2 | 11.6% | 13.0% | 13 of 21 -> 17 of 25 distinct indie IPs |
| Malaysia | 7.8% | 16.1% | 4 -> 14 |

68 rows were added across the four markets: 52 INDEPENDENT, 15 PORTFOLIO, 1 UNCLEAR.
Every appended row is curl-verified against a live dated source, marked `re-sweep 2026-07` in its Notes column, and carries a REPRESENTABLE tag if indie.

## Four mechanisms, not one

The re-sweep's own premise was that brand-side keywords erase creators the way they do in Thailand.
That held in one of the four markets.
What the run actually found is that the size of the artist-side correction tracks **how much of a market's creator activity is documented outside the channels a brand-side query reaches** - and that varies by market for four distinct and non-exclusive reasons.

- **Erasure (Thailand, Malaysia).** Brand-side PR names the licensor and omits the creator.
Malaysia's dominant local-creator format - the festive packet given with purchase at Raya and CNY - is reported brand-side as a promotion with no illustrator named anywhere; the attribution exists only in one trade publication's annual design roundups.
Largest corrections: TH +11.2, MY +12.4.
- **Channel (Japan).** Campaigns *named after the artist* are unreachable by a brand-side query by construction - the illustrator pop-up circuit, standing brand creator-collaboration programmes, transport and tourism tie-ins.
JP +4.4.
The same mechanism supplied four Malaysian rows via Rip Curl Malaysia's quarterly "Artist of the Search" programme.
- **Segregation (Korea).** The indie coverage exists in full, in a creator-facing character-industry trade magazine (아이러브캐릭터) indexed by creator and IP owner rather than by brand, which no brand-side query class touches. 17 of Korea's 23 new rows came from it.
KR +9.2.
- **None of the above (Taiwan).** zh-TW trade press names the illustrator in the headline as a selling point - one new row's source is the brand's own CNA release headlined 「清心福全攜手台灣插畫家」.
TW +0.4, a null result.

Two secondary findings recurred across markets and are worth carrying forward.
First, **artist-side keywords are a self-presentation detector, not an ownership detector**, and they fail in both directions: Taiwan's dtto friends and Japan's BLUE HAMHAM and ナガノマーケット self-present as creator IP but are portfolio-owned, while Korea's 틴틴팅클 is an indie-presenting instatoon whose IP business is run by the Pororo company and 먼작귀 appears in LG's release with no mention of Nagano at all.
The pinned per-IP ownership test, not the keyword, did the classification work in every case.
Accepting self-description would have inflated Taiwan alone from 27.5% to 31.9%.
Second, **each market's artist-side net returned a large excluded class, and the classes push in opposite directions** - Japan's was portfolio IP x commissioned illustrator goods (would have lowered the indie share), Korea's was brands commissioning illustrators to redraw the brand's own mascots (would have raised it).
Both were named campaign by campaign in the method notes rather than silently dropped.

## Is the cross-market comparison now publishable?

Yes, with two stated caveats, and it was not publishable before.
The pre-re-sweep table put Japan at 30.5%, Taiwan at 27.1%, Korea at 24.8%, Thailand at 20.5% and Malaysia at 12.6%, and invited the reading that these are five different market structures spanning a 2.4x range.
The post-re-sweep table puts Japan at 34.9%, Korea at 34.0%, Taiwan at 27.5%, Malaysia at 25.0% and Thailand at 20.5% - a 1.7x range, with Japan and Korea converging to within a point of each other after having appeared six points apart, and Malaysia moving from a conspicuous outlier at half the bottom of the band to the low end of a continuous distribution.
The direction of the correction was one-sided in every market: brand-side querying undercounts indie, never the reverse.
That means the pre-re-sweep table was not measuring market structure so much as measuring press convention, and the differences it showed between markets were partly artefacts of the query class.
They are now measured on a common instrument.

The first caveat is that the instrument is common but not uniformly deep.
Taiwan's leg added 9 rows and Korea's added 23, not because Taiwan has less indie activity but because Taiwan's brand-side pass had already caught most of it; the residual risk is that a market with a low correction was well-swept and a market with a high correction may still be under-swept.
Malaysia in particular is the least settled of the five: its honest range is 18.4% to 25.0% depending on whether commissioned original artwork on a co-branded premium counts as licensed illustration IP (the census's own standing rule says it does, and says so because rows 90 and 94 were written that way), and a named backlog of seven Touch 'n Go creator cards plus roughly seven further social-evidence-only campaigns remains excluded purely for want of a date - dating them would add about another four points.
The second caveat is that per-year slices are now less trustworthy than the overall figures.
Malaysia's 2026YTD indie share reads 39.1% almost entirely because the festive-packet roundups that carry creator attribution exist for 2026 and were not found for 2024 or 2025; Japan added no 2024 rows at all because its richest artist-side vein paginates newest-first.
**The overall per-market shares are the numbers to quote across markets.
The year trends within a market should not be read as growth.**

Neither caveat touches the run's central result, which is not a ratio at all but a breadth number.
Korea's distinct addressable creators went from 7 to 17 and Malaysia's from 4 to 14, and in both markets almost every new REP=yes row belonged to a creator the original pass had never seen.
The concentration findings in the original verdicts - Korea's "a few recycled names", Malaysia's "four names, not a scene" - were themselves artefacts of brand-side querying.
That is the finding most likely to matter downstream, and it is the one a reader should be most careful not to reintroduce: **any concentration claim made from a brand-side census should be assumed to be a query artefact until it has been tested against an artist-side sweep.**

## Where each market's detail lives

| Market | Table | Verdict addendum |
|---|---|---|
| Thailand (reference) | `thailand/campaigns.md` | `thailand/_VERDICT.md` (no addendum - artist-side from the start) |
| Taiwan v2 | `taiwan-v2/campaigns.md` rows 130-138 | `taiwan-v2/_VERDICT.md` § Post-re-sweep addendum |
| Japan | `japan/campaigns.md` rows 132-146 | `japan/_VERDICT.md` § Post-re-sweep addendum |
| Korea | `korea/campaigns.md` rows 136-158 | `korea/_VERDICT.md` § Post-re-sweep addendum |
| Malaysia | `malaysia/campaigns.md` rows 104-124 | `malaysia/_VERDICT.md` § Post-re-sweep addendum |

Each market's `campaigns.md` also carries a "Re-sweep 2026-07 (artist-side keyword pass) - method note" section recording the query-class change, the anti-inflation checks run against the existing table, the excluded classes named campaign by campaign, and the dateless candidates that remain excluded but listed.

**Out of scope for this run and still owed:** Singapore (never swept), the consolidation document (which was gated on this run and is now unblocked), and the zh-language Malaysian press, which was swept only lightly because EN and BM produced enough volume to fill the leg.

**What is not claimed anywhere in any of these censuses:** no outcome, no sell-through, no royalty, no performance figure, for any row in any market.
