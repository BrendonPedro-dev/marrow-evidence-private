# Co-branding census - five-market comparison (Taiwan / Japan / Korea / Malaysia / Thailand)

> **SUPERSEDED (2026-07-30) by [`TEN_MARKET_COMPARISON.md`](TEN_MARKET_COMPARISON.md)** (presentation version: [`ten-market-comparison.html`](ten-market-comparison.html)).
>
> The ten-market document adds Singapore, Hong Kong, the Philippines, Vietnam and Indonesia, taking the series from 649 rows to **1,054**, from 190 independent rows to **234**, and from 103 addressable rows to **130**.
> **Every five-market figure in this document is carried forward unchanged**, so this is a supersession of scope rather than a correction of numbers, with two exceptions that are recorded rather than silently fixed:
>
> 1. **The "continuous 1.7x band" framing in section 1 no longer holds for the series.** Across ten markets the band is 8.5% to 34.9%, a 4.1x range, and the five markets here are its upper half. The ten-market document tests a two-tier reading of that range and rejects it, and reports what survives instead.
> 2. **The Japan REP=unclear figure in section 5 ("10 of 51 indie rows") pairs a pre-re-sweep count with a post-re-sweep denominator.** `japan/campaigns.md` gives **16 of 51**, which is the 10 in the verdict's section 5 plus the 6 added by its addendum (rows 132, 135, 137, 138, 139, 142). The ten-market document uses 16.
>
> Kept in place unedited for the audit trail. Quote the ten-market document for any cross-market figure.

As of 2026-07-29, post artist-side re-sweep.

**This document supersedes `census-comparison.md`** (the three-market Taiwan/Japan/Korea comparison, built 2026-07-24 on pre-re-sweep numbers).
Every headline figure in that document has since moved, in one direction, for a reason that is now understood.
Nothing here is a new measurement.
This is a synthesis of five completed censuses: no new rows, no new sources, no new sweeping.

Sources, on record:

- Taiwan v2: `taiwan-v2/_VERDICT.md` (incl. Post-re-sweep addendum) + `taiwan-v2/campaigns.md` (138 rows).
- Japan: `japan/_VERDICT.md` (incl. Post-re-sweep addendum) + `japan/campaigns.md` (146 rows).
- Korea: `korea/_VERDICT.md` (incl. Post-re-sweep addendum) + `korea/campaigns.md` (158 rows, 2 public-body rows excluded from the split, classifiable base 156).
- Malaysia: `malaysia/_VERDICT.md` (incl. Post-re-sweep addendum) + `malaysia/campaigns.md` (124 rows).
- Thailand: `thailand/_VERDICT.md` + `thailand/campaigns.md` (83 rows, artist-side from the start, no addendum needed).
- Cross-market: `RESWEEP_SUMMARY.md`.

**Method note on this document.**
Every number below traces to one of those files.
Two figures are *derived by this document* from the campaign tables rather than carried from a verdict, and both are marked `[derived]` at the point of use: Japan's distinct addressable-creator count (which `RESWEEP_SUMMARY.md` records as "not re-counted") and Thailand's distinct addressable-creator count (which its verdict does not state separately).
Both were derived by reading the REPRESENTABLE column of the market's own `campaigns.md` and de-duplicating creator names, and the contributing row numbers are cited so the derivation is auditable.
Where the markets' vocabularies differ (format buckets in particular), the mapping is shown or the merge is refused, and Section 4 says which.
**No discrepancy was found between the commissioning task's stated figures and the files.**
JP 34.9% / KR 34.0% / TW 27.5% / MY 25.0% / TH 20.5%, and the breadth moves KR 7 -> 17 and MY 4 -> 14, all check out against the verdicts as written.
The one place the task's framing needed adjusting is Japan's distinct-creator count, which the files record as not re-counted rather than as a number; it is derived here and flagged rather than asserted.

---

## 1. The headline table

**Post-re-sweep, one instrument, five markets.**

| Market | Total rows | Classifiable n | PORTFOLIO | INDEPENDENT | UNCLEAR | Addressable (REP=yes) rows | Addressable share of census | Distinct REP=yes creators |
|---|---|---|---|---|---|---|---|---|
| **Japan** | 146 | 146 | 94 (64.4%) | 51 (**34.9%**) | 1 (0.7%) | 26 | **17.8%** | 25 entries `[derived]` |
| **Korea** | 158 | 156 | 96 (61.5%) | 53 (**34.0%**) | 7 (4.5%) | 28 | **17.7%** | **17** |
| **Taiwan v2** | 138 | 138 | 95 (68.8%) | 38 (**27.5%**) | 5 (3.6%) | 18 | **13.0%** | **17 of 25 distinct indie IPs** |
| **Malaysia** | 124 | 124 | 92 (74.2%) | 31 (**25.0%**) | 1 (0.8%) | 20 | **16.1%** | **14** |
| **Thailand** | 83 | 83 | 66 (79.5%) | 17 (**20.5%**) | 0 (0.0%) | 11 | **13.3%** | 9 `[derived]` |

Denominator notes, because they differ and the difference is small but real:

- Korea's indie/portfolio split runs on the classifiable base of 156 (the 2 government/public-body IP rows are excluded per the pinned Kumamon rule), while its addressable share runs on all 158 campaigns (28/158 = 17.7%), which is how the Korea verdict states it both pre and post re-sweep.
- Every other market's classifiable base is its full row count; no rows are excluded from any other split.
- Japan's distinct count is `[derived]`: 26 REP=yes rows resolve to 25 distinct entries once ヒグチユウコ's two rows (6, 42) are merged. Four of those 25 are multi-illustrator rosters rather than single creators (row 19, the 18-illustrator Loft "Creator meets"; row 77, a 12-illustrator capsule; row 52, three illustrators; row 140, the four-illustrator Pixio roster), and one roster member (イコモチ, row 52) also holds a solo row (134), so a stricter creator-level count is 24 named entities plus roughly 34 further illustrators inside the rosters. Pre-re-sweep the same derivation gives 21 rows / 20 entries.
- Thailand's distinct count is `[derived]`: 11 REP=yes rows (10, 48, 51, 55, 56, 58, 74, 76, 77, 80, 81) resolve to 9 distinct creators, because BABYBOY/StupidnoobMacc holds rows 10 and 81 and Bad Meaw holds rows 48 and 51.
- Taiwan is stated by its own verdict on a distinct-IP basis rather than a distinct-creator basis (17 of 25 distinct indie IPs are REP=yes, up from 13 of 21), and is left in that unit rather than converted.

**The band.**
The five markets now sit between 20.5% and 34.9% indie: a **continuous 1.7x band** with no gaps and no outliers.
Japan and Korea land within a point of each other at the top, Taiwan and Malaysia within 2.5 points of each other in the middle, Thailand alone at the bottom.

**What the band replaces.**
The pre-re-sweep table read Japan 30.5%, Taiwan 27.1%, Korea 24.8%, Thailand 20.5%, Malaysia 12.6%: a **2.4x range** with Malaysia at less than half the bottom of an apparent 25-31% cluster.
That table invited the reading that these are five structurally different markets.
It was partly measuring press convention rather than market structure.
Four of the five markets had been swept with brand-side keywords only; the fifth (Thailand) had been swept with artist-side keywords and had already shown, inside its own build, that the same market reads 9.3% indie on brand-side keywords and 20.5% on brand-side plus artist-side, with no change of source type, geography, definition or window.
Re-sweeping the other four on the same added keyword class moved every one of them up and none of them down.

**The correction, per market** (`RESWEEP_SUMMARY.md`):

| Market | Pre-re-sweep n | Pre indie share | Post-re-sweep n | Post indie share | Correction | Rows added (indie / portfolio / unclear) |
|---|---|---|---|---|---|---|
| Thailand *(reference, artist-side from the start)* | 83 | 20.5% | 83 | **20.5%** | - | - |
| Japan | 131 | 30.5% | 146 | **34.9%** | +4.4 | 11 / 4 / 0 |
| Korea | 133 classifiable | 24.8% | 156 classifiable | **34.0%** | +9.2 | 20 / 2 / 1 |
| Taiwan v2 | 129 | 27.1% | 138 | **27.5%** | +0.4 | 3 / 6 / 0 |
| Malaysia | 103 | 12.6% | 124 | **25.0%** | +12.4 | 18 / 3 / 0 |

68 rows were added across the four re-swept markets: 52 INDEPENDENT, 15 PORTFOLIO, 1 UNCLEAR.
The direction was one-sided in all four: brand-side querying undercounts indie, never the reverse.

**Scale of the whole series:** 649 curl-verified rows across five markets, 190 of them INDEPENDENT, 103 of them REPRESENTABLE=yes.
A pooled five-market indie share is deliberately **not** quoted: the censuses differ in depth (83 to 158 rows) and in denominator convention (Korea's two excluded public rows), so a pooled ratio would weight Japan and Korea's deeper sweeps against Thailand's thinner one and read as a market fact rather than a sampling accident.
The per-market shares are the numbers.

---

## 2. The measurement story - why these numbers can be trusted

This section exists so an external reader can check the instrument before checking the result.

**One definition, applied five times.**
Every market was built on the identical ownership test (who owns the IP, not who runs the brand), the identical pinned edge cases, and the identical REPRESENTABLE sub-tag on every independent row.
The pinned cases travel by name across all five `campaigns.md` headers: Miffy/Mercis and Peanuts/Sony as estate-or-controlling-stake PORTFOLIO; Sanrio, San-X, Pokemon-Nintendo, Disney-Marvel, Warner Bros, KAKAO FRIENDS and LINE FRIENDS/BT21 as platform- or studio-owned PORTFOLIO; government/public-body-owned mascots excluded entirely (the Kumamon rule); a brand's own mascot not counted; co-owned/JV resolved to whoever holds control, with genuine 50/50 sent to UNCLEAR.
Cross-market precedents are cited by row: Butterbear is PORTFOLIO in Thailand on the Malaysia row 8 call; LuLu the Piggy is INDEPENDENT/REP=no in Thailand and Taiwan on the Taiwan-v2 row 5 call; venue-hosted pop-ups are rows in Thailand and Malaysia on the Taiwan-v2 row 126 call; illustrator-artwork licensing is in scope in Malaysia on the Taiwan-v2 rows 120/127 and Korea rows 78/79 precedent.
This is what makes the markets comparable row for row rather than five rulebooks compared by eye.

**Every row is curl-verified against a live, dated source.**
Not a claim about a campaign, a fetched page: HTTP 200, with the year tag read off machine-readable page markup or a stated campaign window, never inferred.
Thailand re-verified all 97 cited URLs at build time.
Malaysia dropped a 7-Eleven Sanrio row rather than guess whether it was MY or HK.
Thailand went from a claimed 85 rows to a verified 83 because two did not survive the rules.
Phantom entries are the known failure class in every build and are named as such.

**The brand-side undercount discovery (Thailand).**
Thailand was the first market swept with artist-side keywords, and it found the effect inside a single build: pass 1 on brand-side Thai terms (คอลแลบ, คาแรกเตอร์, ลิขสิทธิ์, มาสคอต, entity names) returned 4 indie rows in 43, or 9.3%.
Pass 2 added three artist-side terms (ศิลปินไทย, นักวาด, ครีเอเตอร์) against the *same two trade titles* and returned 13 more, taking the census to 17 indie in 83 rows, or 20.5%.
Same sources, same geography, same definition, same window.
Brand-side PR names the licensor and omits the creator, so indie rows are structurally invisible to a brand-side query.
Thailand's own verdict flagged the consequence before anyone acted on it, and rated the claim "indie share is below the Japan/Taiwan/Korea band" at **Low** confidence for exactly this reason.

**The artist-side re-sweep corrected all four other markets, one-directionally.**
Each re-sweep appended rows to the existing table under the existing definition.
No table was rebuilt.
No existing row was reclassified, re-dated or edited in any of the four markets, which is stated explicitly in all four addenda and is itself a consistency check: where a new row touched an existing licensor relationship, the new evidence agreed with the recorded call.
Portfolio rows caught by the artist-side net were appended rather than dropped, in every market, even where they reduced the correction: Japan appended 4, Taiwan 6, Korea 2, Malaysia 3.
Malaysia's addendum states the arithmetic cost of that honesty in the open (without its three Touch 'n Go portfolio rows the correction would read 12.6% -> 25.6% rather than 25.0%).

**Four mechanisms, not one.**
The re-sweep's premise was that brand-side keywords erase creators everywhere the way they do in Thailand.
That held in one of the four markets.
What the run found instead is that the size of the correction tracks *how much of a market's creator activity is documented outside the channels a brand-side query reaches*, and that varies for four distinct, non-exclusive reasons.

| Mechanism | Markets | What it is | Correction |
|---|---|---|---|
| **Erasure** | Thailand, Malaysia | Brand-side PR names the licensor and omits the creator. Malaysia's densest local-creator format, the festive packet given with purchase at Raya and CNY, is reported brand-side as a promotion with the illustrator named nowhere; the attribution exists in one trade publication's annual design roundups (8 rows rest on two URLs). | TH +11.2, MY +12.4 |
| **Channel** | Japan | Campaigns *named after the artist* are unreachable by a brand-side query by construction: the illustrator pop-up circuit, standing brand creator-collaboration programmes, transport and tourism tie-ins. | JP +4.4 |
| **Segregation** | Korea | The indie coverage exists in full, in a creator-facing character-industry trade magazine (아이러브캐릭터) indexed by creator and IP owner rather than by brand, which no brand-side query class touches. 17 of Korea's 23 new rows came from it. | KR +9.2 |
| **None of the above** | Taiwan | zh-TW trade press names the illustrator in the headline as a selling point. One new row's source is the brand's own CNA release, headlined 「清心福全攜手台灣插畫家」. | TW +0.4 |

The mechanism is not exclusive to one market: the Japan channel mechanism supplied four Malaysian rows through Rip Curl Malaysia's quarterly "Artist of the Search" programme, and Malaysia's absence of a Korean-style creator trade publication is recorded as a positive finding rather than an omission.

**Taiwan's null result is the control that proves the instrument.**
This is the part that makes the other four numbers trustworthy rather than merely larger.
If the artist-side keyword class simply inflated indie counts wherever it was applied, Taiwan would have moved too.
It moved +0.4 points, inside noise, and its verdict explains why in terms of the sources themselves: the zh-TW vocabulary for co-branding (原創IP, 插畫家, 圖文作家) is already embedded in ordinary brand-side coverage, so the two keyword classes return heavily overlapping result sets.
Taiwan's new rows were a *channel* correction (7 of 9 are venue pop-ups, a gap its own Section 5 had already flagged) landing roughly proportionally across both classes: 3 indie, 6 portfolio.
An instrument that finds nothing where there is nothing to find, and finds a lot where a mechanism predicts a lot, is measuring something.

**The keyword is not the classifier.**
Artist-side keywords are a self-presentation detector, not an ownership detector, and they fail in both directions.
Taiwan's dtto friends bills itself as 「原創角色品牌」and is Dcard platform-owned; Japan's BLUE HAMHAM is framed as one creator's work but is © CHOCOLATE, and ナガノマーケット self-presents as the creator's own market but is portfolio under the pinned Chiikawa rule.
Korea produced the mirror image: 틴틴팅클 self-presents as an indie instatoon and its IP business is run by Iconix, while 먼작귀 appears in LG's own release as a "글로벌 인기 캐릭터 IP" with no mention of Nagano at all, yet is creator-originated.
The pinned per-IP ownership test did the classification work in every case.
Accepting self-description would have inflated Taiwan alone from 27.5% to 31.9%.

**The excluded classes were named campaign by campaign, and they push in opposite directions.**
Japan's artist-side net returned, in volume, portfolio IP paired with a commissioned illustrator for goods drops (初音ミク x 望月けい, ダンガンロンパ x lack, サンリオ x necömi and a dozen more); counting them would have pushed Japan's indie share *down*.
Korea's returned brands commissioning illustrators to redraw the brand's *own* mascots (궁중비책 x 윰마, Starbucks Korea's art-contest goods); counting them would have pushed Korea's indie share *up*.
Both classes are excluded under standing rules and both are itemised in the respective `campaigns.md` method notes, so the boundary of each census is auditable rather than asserted.

---

## 3. The breadth correction - the finding that matters most

The ratio moved.
The breadth number moved more, and it is the finding most likely to matter downstream.

| Market | Distinct addressable (REP=yes) creators, pre -> post | REP=yes rows, pre -> post |
|---|---|---|
| **Korea** | **7 -> 17** | 19 -> 28 |
| **Malaysia** | **4 -> 14** | 8 -> 20 |
| Taiwan v2 | 13 of 21 -> **17 of 25** distinct indie IPs | 15 -> 18 |
| Japan | 20 -> 25 entries `[derived]`; verdict records "not re-counted" | 21 -> 26 |
| Thailand | 9 `[derived]`, single pass, no pre/post | 11 |

**Korea: 7 -> 17.**
The original build resolved its 19 REP=yes rows to 7 distinct addressable creators and read that as "real breadth, but with two names doing much of the volume."
The 28 REP=yes rows now resolve to 17.
Ten of the eleven new names (스튜디오버튼, 노이신, 제이샤/미스터두낫띵, 하이다나, 김잼, 김현주, 나무13, 엔리케, 마인드어데이, Project624/벌룬프렌즈) had never been seen by the original pass; only one of the nine new REP=yes rows (SSG x 가나디) belongs to a creator it already knew.
망곰이 and 무직타이거 went from 12 of 19 addressable rows to 12 of 28.

**Malaysia: 4 -> 14.**
The original verdict's phrase was "four names, not a scene": Bichi Mao, Yellobanana, QuirkyQing, Bear Boss Buddies.
The post-re-sweep table names fourteen distinct creator-owned IPs that reached a national brand inside the window, ten of them new (Kirin Sharom / Bunga dan Bintang, KATUN, Janggutbear, Nas Suha, Jean Lynn, Ame Lukis, Yatt, Perempuan Melawan Art / Finn Anuar, Humana Art / Vanissa Foo, Cloakwork).
Only one of the twelve new REP=yes rows belongs to a creator the original pass already knew.

**These were query artefacts, not market structure.**
Both markets' concentration findings were written in good faith off a census that could not see most of the creators.
Neither survived contact with an artist-side sweep.

**The rule, carried verbatim from `RESWEEP_SUMMARY.md`:**

> **any concentration claim made from a brand-side census should be assumed to be a query artefact until it has been tested against an artist-side sweep.**

That rule applies to this document too, including to the concentration claims in Section 4 that *did* survive: they survived because the instrument was pointed at them, not because they were never suspect.

**What the breadth correction means.**
The addressable indie supply exists in every measured market, at a materially larger headcount than a brand-side view of that market shows.
Korea more than doubled its addressable bench and Malaysia more than tripled it without a single new source type being invented, without the definition moving, and without anything changing in the markets themselves.
The creators were there the whole time.
What changed is that somebody queried in a way that could see them.

The structural point for an evidence-led agency follows directly, and it does not require an outcome claim to make.
Brands source IP through the same channels a brand-side query reaches: licensor PR, agency rosters, the trade press that covers campaigns brand-first.
That is precisely the channel set in which this addressable supply is invisible.
The gap is not a supply gap and it is not an appetite gap.
It is a **visibility gap between an addressable creator layer that demonstrably reaches national brands and the channels through which brands look for IP** - and it is measurable, in five markets, on one instrument.

---

## 4. Market structure divergences - what stays different after the correction

The correction narrowed the ratios.
It did not make the markets the same.

### 4.1 The machinery thesis, revised

The pre-re-sweep explanation for Malaysia's outlier position was institutional, and it is stated in Malaysia's own Section 5: Malaysia lacks the two institutions that manufacture indie co-branding rows in the northern markets, **a mass messaging-sticker economy** (LINE in JP/TW, KakaoTalk in KR) and **a convenience-store 集點 collectible culture** that cycles a new illustrator IP every few weeks.

**What survives.**
The machinery is real and it is visible in the addressable benches.
Korea's addressable tier is explicitly emoticon-origin: 망곰이 is a self-run emoticon-origin IP, 깜자 is a KakaoTalk-emoticon artist, and the verdict describes the addressable pool as "the individual emoticon/illustrator tier."
Taiwan's flagship indie carried a 7-ELEVEN 全店精品集點 wave across 7,100+ stores.
Both machines still do what the thesis said they do.

**What the re-sweep broke.**
The machinery thesis was doing double duty as the explanation for the *gap*, and at 25.0% Malaysia no longer has the gap the thesis was invented to explain.
Malaysia acquired neither a sticker economy nor a 集點 culture between the two passes.
It went from 12.6% to 25.0% because two formats and a channel were found: festive collateral, brand creator-programmes, and the corporate newsroom as an attribution source.
Malaysia's own addendum states the consequence: the market is thin "by degree, not by kind."
What survives of the claim is narrower and format-shaped rather than institutional - **Malaysia's indie campaigns are smaller in format**, festive packets and capsule tees rather than nationwide drink series and pop-up circuits.

**Thailand is the case that always contradicted the machinery thesis and is worth keeping in view.**
Thailand has LINE at national scale, and its sticker-creator scene barely surfaced in the census at all.
The pinned sticker-ownership rule (creator owns the character even though LINE hosts the stickers) was written to decide the Thai indie bucket and "in practice it decided almost nothing."
Every one of the 11 Thai indie creators in the census is an illustrator, street artist, digital artist or art-toy designer; none was recorded licensing out from a sticker-first position.
Thailand's visible indie economy is an **illustrator-and-art-toy economy, not a sticker economy** - and its verdict is careful that this is a statement about trade-press visibility, not a claim that the sticker economy is commercially inactive, because LINE Creators Market rosters remain unswept.

### 4.2 The closed-formats finding, and whether it travels

Thailand's sharpest cut is not its headline ratio.
It is that **the formats that scale are 100% portfolio**: retail/CVS/e-commerce (11 rows), banking/fintech (6 rows), 17 rows in total, zero indie.
Every one runs on Disney, Sanrio, LINE FRIENDS, POP MART, Marvel, Shin-chan or Butterbear.
Meanwhile experiential rows are 42.9% indie (9 of 21).
Thailand's own confidence rating on this is **Medium-high**, on the honest grounds that 17 rows is a small base.
The framing that follows is the sharper version of the founder thesis: indie creators are not absent from the Thai market, they are absent from its highest-distribution formats.

**Does it travel? Partly, and the exceptions are as informative as the rule.**

First, a vocabulary problem that has to be stated rather than solved.
Only Thailand and Malaysia carry a per-format table in their verdicts, and only Thailand's is cut by IP class.
Malaysia's format table is pre-re-sweep (n=103) and was not recomputed after the re-sweep.
Taiwan, Japan and Korea record format structure as targeted-vein observations rather than as counted format-x-class tables, and their bucket vocabularies differ from each other and from Thailand's (Taiwan's 集點 waves and handshake-drink chains, Japan's kuji and gashapon, Korea's Olive Young rollout machine and KBO club merch).
**A merged five-market format-x-class table is therefore not derivable and is not presented.**
What follows is per-market, in each market's own vocabulary.

| Market | Evidence on high-distribution formats | Verdict |
|---|---|---|
| **Thailand** | Retail/CVS/e-comm 0 of 11 indie; banking/fintech 0 of 6. Counted table, cut by class. | **Supports.** The only market with a counted format-x-class cut. |
| **Japan** | "The gaming/payment/telecom vein came back 100% portfolio on targeted search"; indies "largely absent from gacha, card-skins, telecom points, and national vending." Stated as vein observation, not a counted table. | **Supports**, in weaker evidentiary form. |
| **Korea** | "Finance/card, telecom, travel/hospitality, bakery/dessert, mobile-game, snack/beverage packaging, and premium eyewear came back essentially 100% portfolio." The addendum confirms the artist-side pass did not dent it: "no artist-side query returned a single finance, telecom, hospitality or snack-packaging indie row." | **Supports, and it survived the re-sweep** - the strongest form of this finding in the series, because it was re-tested with a better instrument and held. |
| **Taiwan** | **Contradicts.** Bugcat Capoo, a creator-owned indie, carried a 7-ELEVEN x 國立故宮博物院 flagship 全店精品集點 wave across 7,100+ stores; also 華南金控 (listed financial holding company, shareholder gift), 中華郵政 (national postal service) and CTBC. Taiwan's verdict names this as its single strongest counter-example to "indies are shut out". | **Contradicts.** The highest-distribution retail-loyalty format in the country was headlined by an indie IP. |
| **Malaysia** | **Contradicts.** The payments/platform vein is 11 rows and 6 of them are indie: Touch 'n Go x QuirkyQing (95, REP=yes), KTM Komuter x Bichi Mao (100, REP=yes), foodpanda x Yellobanana (90, REP=yes), Lalamove x Yellobanana (94, REP=yes), Touch 'n Go x Loka Made (106, REP=unclear), Maxim x five Sabah/Sarawak illustrators (121, REP=unclear). Its verdict calls fintech/payments "a genuine Malaysian format" with no equivalent depth in any other market in the series. | **Contradicts**, and in the format Thailand found most closed. |

**The synthesis.**
"High-distribution formats are closed to indie IP" is a real finding in Thailand, Japan and Korea and a false one in Taiwan and Malaysia.
Where it holds, the closure is in *corporate-premium and screen-IP-driven* channels (finance cards, telecom points, national vending, snack packaging).
Where it breaks, it breaks through a specific instrument: a national retail-loyalty programme that chose an indie IP on its merits (Taiwan), and a stored-value card line that treats creator artwork as a product category (Malaysia).
Both exceptions are, in agency terms, the more interesting cases - they are existence proofs that the closure is a market convention rather than a structural impossibility.
Korea's is the version to be most careful about disputing, because it is the only one re-tested with the artist-side instrument and still returning zero.

### 4.3 Format mix per market

| Market | What leads | Evidence |
|---|---|---|
| **Thailand** | **Licensed goods and mall experience, not F&B.** Product/licensed goods 38.6%, experiential 25.3%, F&B 10.8%. | Counted table, `thailand/_VERDICT.md` §3. Called "the sharpest format divergence from the prior markets in the series". |
| **Malaysia** | **Retail and FMCG, not F&B.** Retail/FMCG/supermarket 25 rows, cafe/bubble tea 21, convenience 13, mall/venue 13, QSR 12. QSR is a 2025 arrival (0 rows in 2024). | Counted table, `malaysia/_VERDICT.md` §3, **pre-re-sweep n=103, not recomputed**. |
| **Taiwan** | Convenience-store 集點, handshake-drink chains, cosmetics, plus a venue/pop-up circuit the re-sweep partly opened. | Vein description, `taiwan-v2/_VERDICT.md` §5 + addendum. |
| **Japan** | Lifestyle retail (Loft, Village Vanguard, Don Quijote, Kiddy Land), illustrator apparel/stationery, CVS art capsules, cosmetics/variety - plus, new from the re-sweep, the illustrator pop-up circuit, standing brand creator-programmes and transport/tourism. | Vein description, `japan/_VERDICT.md` §4 + addendum. |
| **Korea** | Beauty (the Olive Young rollout machine), apparel (SPAO), convenience, and distinctively KBO/K-League sports-club merch - plus, new from the re-sweep, mid-market apparel below the SPAO tier, hardware/houseware, cinema exhibition and K League. | Vein description, `korea/_VERDICT.md` §3-4 + addendum. |

**The mall-as-indie-buy-side finding is Thai and has one partial analogue.**
Siam Piwat, The Mall Group, Central, ICONSIAM, Future Park and Jungceylon between them account for most of Thailand's 9 indie experiential rows: "Thai malls are a first-class licensing channel in a way they were not in Malaysia."
The nearest analogue is Taiwan's venue/pop-up channel (華山, 松菸, AIPXA LAND, 西門地下市, 新光三越), which supplied 7 of the 9 rows its re-sweep added.
Malaysia's mall/venue growth runs the other way: it is driven almost entirely by POP MART's nine-store footprint and the Pokemon Truck tour, which are portfolio.
Same format bucket, opposite class composition, which is exactly why the merged table is refused above.

**A recurring non-lifestyle format is worth naming across markets**, because it is the most agency-shaped thing the re-sweep found: hardware and durable-goods brands running standing, recurring, individually-contracted creator programmes.
Japan has Pixio (2nd instalment, four named freelance illustrators), CyberAgent's Pigg Party (3rd, 寺田てら) and Superbag (4th, mame), which Japan's addendum calls "the single most PBC-shaped format found in the whole Japan build."
Korea has Epson Korea's label-printer editions with three named illustrators, 락앤락 x 벌룬프렌즈 and 프린팅박스 x 해요.
Malaysia has Rip Curl's quarterly "Artist of the Search", Skechers' SkechVibe and Montigo x Humana Art.
Three markets, the same shape, and none of the three original brand-side passes had any read on it.

### 4.4 Concentration where it genuinely survives

Two concentration findings were tested against an artist-side instrument and held.

**Thailand: Butterbear, 17 of 83 rows (20.5% of the census).**
This is the only concentration figure in the series measured on an artist-side instrument from the start, so it is not exposed to the query-artefact rule.
The distribution is 1 row in 2024, 12 in 2025, 4 in 2026YTD, across 15 distinct licensee brands, each separately sourced, spanning FMCG, telco, fintech, banking, electronics, apparel, houseware, QSR, pet food, optics and travel retail.
Its verdict rates it **High** confidence as a genuine structural feature rather than a data error.
Note what it is: a **corporate-owned mascot licensed out**, PORTFOLIO under the pinned Malaysia row 8 call, not an indie success story.
Thailand's IP concentration overall is severe - Butterbear, the POP MART stable (11 rows), Sanrio (11) and the Disney family (10) cover 49 of 83 rows.

**Taiwan: Bugcat Capoo.**
8 of 35 indie rows pre-re-sweep (23% of all indie rows), and post-re-sweep still 8 of the 17 REP=no rows.
Taiwan's re-sweep was the null result, so this concentration was measured with the artist-side net in hand and did not dissolve.
It is a different *kind* of concentration from Thailand's: Capoo is creator-owned, and the concentration matters because the owner runs licensing through his own captive studio (卡特島創意), which is what makes Taiwan's most prominent indie IP unaddressable.
That is why Taiwan's addressable read is stronger by distinct IP (17 of 25, 68%) than by row volume (13.0% of the census).

**The two that dissolved** are in Section 3: Korea's "a few recycled names" and Malaysia's "four names, not a scene".
The pattern is legible.
Concentration claims about a *portfolio* IP's licensing footprint (Butterbear) or about a *named, already-visible* indie's captivity (Capoo) survived, because brand-side querying sees those things well.
Concentration claims about *the size of the addressable creator bench* did not survive, because that is precisely what brand-side querying cannot see.

---

## 5. Per-market one-page reads

### Japan - n = 146

- **Shares:** PORTFOLIO 94 (64.4%) / INDEPENDENT 51 (**34.9%**) / UNCLEAR 1 (0.7%). Correction +4.4 from 30.5%.
- **Addressable:** 26 REP=yes rows, **17.8% of all campaigns**, about one campaign in six. `[derived]` distinct: 25 entries, four of them multi-illustrator rosters.
- **Mechanism: channel.** Campaigns named after the artist are unreachable by a brand-side query by construction.

Sharpest findings:

1. **Fame does not equal representability.** The viral SNS-character indies (mofusand, Opanchu Usagi, Kanahei, Colorful Peach) are exactly the ones locked to captive studios or master licensors and score REP=no. The cleanly addressable pool is the quieter individual-illustrator tier doing open non-exclusive brand collabs.
2. **Indies reach the largest brands, repeatedly.** Higuchi Yuko, a living self-owned painter, ran campaigns with both Lawson and Morinaga. foxco reached Calbee; foxy reached CASETiFY; Yuhachi reached Bandai Gashapon; Oono Taro reached 3COINS.
3. **The re-sweep opened two formats the original pass had no read on at all**: standing brand creator-collaboration programmes (Pixio, Pigg Party, Superbag - recurring, non-exclusive, individually contracted) and transport/tourism (JR東海's 推し旅 built a prefecture-wide campaign around one illustrator).

Caveats:

- **The largest artist-side yield in Japan was not indie.** It was portfolio IP paired with a commissioned illustrator, excluded by rule and named campaign by campaign. In Japan, イラストレーター and 描き下ろし overwhelmingly credit a *hired* artist on someone else's IP.
- **REPRESENTABLE is the softer call**: 10 of 51 indie rows are REP=unclear because exclusivity is rarely public, so 17.8% is a conservative floor.
- **Aggregator dependence rose in the re-sweep**: 9 of the 15 new rows rest on collabo-cafe alone, each flagged in Notes.
- **No 2024 rows were added** (the artist-side index paginates newest-first and reached back only to 2025-02), so 2024 is now the only year the correction did not touch.
- One marginal format was admitted and flagged (row 142's promotional shopper bags); a stricter reading gives 34.5%.

### Korea - n = 158 (classifiable 156)

- **Shares:** PORTFOLIO 96 (61.5%) / INDEPENDENT 53 (**34.0%**) / UNCLEAR 7 (4.5%). Correction +9.2 from 24.8%.
- **Addressable:** 28 REP=yes rows, **17.7% of all campaigns**. **17 distinct creators, up from 7.**
- **Mechanism: segregation.** A creator-facing trade magazine indexed by creator and IP owner, which no brand-side query class touches.

Sharpest findings:

1. **The missing campaigns were in an untouched *publication*, not an untouched format.** 아이러브캐릭터 supplied 17 of the 23 appended rows, and essentially none of them appear in the ko lifestyle/beauty/brand press the original pass swept. The original Section 5 named "recall bias toward covered campaigns" as a limit; this is the concrete form that bias took.
2. **The dual portfolio wall is distinctive and untouched by the re-sweep.** Korea's portfolio majority is built from two stacks: foreign licensors (Sanrio, Pokemon, Disney, and newly Netflix screen IP across HiteJinro, Nongshim, Ottogi, Paris Baguette) and domestic platform owners (Kakao Friends, LINE Friends/IPX, Iconix, SAMG, HYBE, Devsisters). Both new portfolio rows are foreign-licensor rows.
3. **Indie IP reaches professional sport and national retail.** 무직타이거 on a first-division K-League match-day kit (Ulsan HD); 최고심 with LG Twins and 깜자 with SSG Landers (KBO); 망곰이 across Olive Young, SPAO and CU. The re-sweep added 광주FC and 메가박스 to that channel list.

Caveats:

- **"Indie share sits at about a quarter" is superseded by the census's own addendum**: it is about a third.
- **Single-publication dependence is the quality cost, and it is worse than Japan's**: 17 of 23 new rows rest on one outlet, each flagged.
- **Ownership evidence is thinner on the appended block**: 9 of the 20 new indie rows are REP=unclear, and one row is IP-class UNCLEAR because the owning entity could not be established.
- **2024 remains the thin, under-corrected year** (only 3 of 23 new rows), so the 2024-vs-2025 gap is still largely a coverage artefact.
- **Window-boundary caveat on the addressable read:** several of the most representable indies ran their biggest institutional collabs *before* the 2024-01 window (우리카드 x 다이노탱 2021, IBK x 무직타이거 2021, 우리카드 x 망그러진곰 2023, 신한카드 x 최고심 2022), so their true footprint is larger than this window captures.
- Two marginal formats admitted and flagged; a stricter reading gives 33.1%.
- 틴틴팅클 (row 152) is flagged rather than buried: INDEPENDENT/REP=no on the pinned test, but a reasonable analyst could move it to PORTFOLIO.

### Taiwan v2 - n = 138

- **Shares:** PORTFOLIO 95 (68.8%) / INDEPENDENT 38 (**27.5%**) / UNCLEAR 5 (3.6%). Correction +0.4 from 27.1%.
- **Addressable:** 18 REP=yes rows, **13.0% of the census**, but **17 of 25 distinct indie IPs (68%)** - the highest open-rate per distinct IP in the series.
- **Mechanism: none of the above.** The control case.

Sharpest findings:

1. **The volume/distinct gap is the whole Taiwan story.** Only 13.0% of campaigns are addressable, because Bugcat Capoo (self-licensed through 卡特島創意) drives 8 of 17 REP=no rows, and Kanahei, mofusand, 黃阿瑪, Kusama and LuLu are each captive in their own way. By distinct IP the market is the most open measured.
2. **Indies win Taiwan's highest-prestige formats.** A 7-ELEVEN x 國立故宮博物院 7,100-store 集點 wave, a listed FHC's shareholder gift, the national postal service, 台北101's observatory, CeraVe and Sulwhasoo.
3. **The addressable bench is split domestic/inbound.** Roughly five open Taiwan-origin creator IPs (爽爽貓, 馬來貘, Monday Bruce, 露咖貓, 臺灣印事/腋毛人) plus eight foreign indies active in Taiwan (KR/JP/UK), with the re-sweep adding Nuomi 諾米, Mia 林孜育, 好球先生 Mr. STRIKE and mikko.

Caveats:

- **v2 was a re-classification, not a re-discovery** (until the re-sweep), so it inherits v1's coverage: the row set, sources and dates are v1's.
- **Sample skew likely understates rather than overstates indie share** - the sample over-indexes convenience-store 集點, drink chains and cosmetics (heavily portfolio) and under-indexes indie pop-ups, stationery and gaming.
- **Dateless indie candidates remain excluded and listed** (BONNY&READ x Kurt Wu; 寶島眼鏡/K-DESIGN x 爽爽貓), so 27.5% is a floor.
- One dated row is left unclassified rather than guessed (SEMO'S / Second Morning), logged as a hole.
- Two new rows are single-source flagged.
- **REPRESENTABLE is directional guidance, not a legal finding** - the Capoo=no call in particular drives most of the "no" volume and rests on a defensible read of a captive studio.

### Malaysia - n = 124

- **Shares:** PORTFOLIO 92 (74.2%) / INDEPENDENT 31 (**25.0%**) / UNCLEAR 1 (0.8%). Correction **+12.4** from 12.6%, the largest in the series.
- **Addressable:** 20 REP=yes rows, **16.1% of the census**. **14 distinct creators, up from 4.**
- **Mechanism: erasure**, plus the Japan channel mechanism imported through brand creator-programmes.

Sharpest findings:

1. **The undercount was an entire format and an entire channel, not the named backlog.** The festive packet (sampul Raya, CNY angpao given with purchase) is Malaysia's densest local-creator format and its brand-side coverage names no illustrator anywhere; the attribution exists in one trade publication's annual design roundups. Eight rows rest on those two URLs.
2. **"Four names, not a scene" was a brand-side artefact.** Fourteen distinct creator-owned IPs reached a national brand inside the window.
3. **Malaysia has no creator-facing character-industry trade publication**, and that absence is itself the finding: attribution lives in general marketing trade press, in brand newsrooms, and on brand-official artist landing pages. Its payments-card vein is also unique in the series for depth, and unlike Thailand's it is open to indie IP.

Caveats - Malaysia is the least settled market in the series and its honesty caveats are the heaviest:

- **The honest range is 18.4% to 25.0%.** Ten of the 18 new indie rows are the definitional frontier - commissioned original artwork on a co-branded premium rather than a pre-existing licensed character. They are counted because the census's own standing rule was written for that exact shape (rows 90 and 94). A reader who draws the line at pre-existing character IP gets n=114, 21 indie, **18.4%**. Both ends of that range destroy the pre-re-sweep finding.
- **The dateless backlog grew rather than closed.** All 160 releases in Touch 'n Go's press-release index were enumerated and not one artist card has a press release; two further undated cards were discovered (ThatDania, Jepah Studio), so the backlog goes from five campaigns to **seven**. Adding all seven would give 38/131 = 29.0%. A further set (SODA x Bichi Mao, SODA and Walls x Yuurei Neko Sama, The Good Boisss x Lazada and x Converse, Loklok & Friends x Popular Bookstore and x Mitsui, Pee Yong Diary x McDonald's) is still undated and still listed. Roughly another four points sit there.
- **Source concentration is the structural weakness, and the re-sweep swapped one dependence for another.** 72 of the original 103 rows came from everydayonsales.com (69.9%); 8 of the 21 new rows rest on two Marketing-Interactive URLs. Nine of the 21 are single-source overall.
- **The 2026 skew is an artefact, not a surge** - see Section 6.
- **The zh-language Malaysian press was swept only lightly.** Any Malaysian-Chinese creator whose coverage is zh-only is likely still missing.
- **Social-only evidence remains uncounted and it censors indie rows specifically**, because portfolio campaigns get press releases and indie campaigns get Instagram posts.
- Four BM-language rows carry translation-confidence flags (confidence recorded high in each); one row is dated from a Shopify `created_at` timestamp; five new rows have an announcement date but no stated window.
- **The format table in its verdict is pre-re-sweep (n=103)** and was not recomputed.

### Thailand - n = 83

- **Shares:** PORTFOLIO 66 (79.5%) / INDEPENDENT 17 (**20.5%**) / UNCLEAR 0. No correction: artist-side from the start, and the reference market for the whole series.
- **Addressable:** 11 REP=yes rows, **13.3% of the census**; `[derived]` 9 distinct creators, 10 of the 11 rows Thai.
- **Mechanism: erasure** - the market where it was discovered.

Sharpest findings:

1. **The keyword finding itself**, which is the most transferable result in the series and reset four other markets: 9.3% brand-side, 20.5% with artist-side terms added, same two trade titles.
2. **The channels that scale are closed** (Section 4.2): retail/CVS/e-comm, banking and fintech are 17 rows and 0 indie, while experiential is 42.9% indie. Thai malls are the buy side for indie IP.
3. **The addressable layer is domestic, individual and named in the press**, and two creators recur across four large corporates: BABYBOY/StupidnoobMacc (LG, CPF) and Bad Meaw (Samsung, AIS). Both recurrences are ad-hoc, with no agency named in any of the four sources.

Caveats:

- **This is the thinnest census in the series** - 83 rows against 124-158 elsewhere - and its verdict says so plainly: a credible sample of a market that would support 120-140 rows.
- **Single-source rate is the highest in the series: 73 of 83 rows (87.9%).** Only 10 rows carry a second corroborating URL.
- **8 rows carry a `TH-src (low conf)` translation flag**, two of them on indie class calls (rows 53, 59). Reclassifying both would move 20.5% to 18.1%; dropping all four illustration-IP rows would move it to 17.7%. The finding survives both stress tests.
- **Named holes:** brand Facebook pages completely unswept (the largest known gap, and the one most likely to *suppress* the indie share); two of four trade titles unsweepable with the available tooling (JS-rendered search, HTTP 403); LINE Creators Market rosters unswept; Lotus's contributes zero rows, which is not a plausible true value.
- **Per-year slices are not trend-readable** - see Section 6.
- One judgement call is named as contestable rather than hidden: Watsons x Artstory by Autistic Thai was excluded as a CSR art programme; a different reading would admit it as an indie row.

---

## 6. Caveats, carried verbatim and not softened

**1. Per-year slices within markets are NOT trend-readable. The overall per-market shares are the numbers to quote.**

From `RESWEEP_SUMMARY.md`:

> **The overall per-market shares are the numbers to quote across markets.
> The year trends within a market should not be read as growth.**

From `malaysia/_VERDICT.md`, on its own 2026 figure:

> Thirteen of 21 new rows are 2026YTD, and 2026's indie share jumps to 39.1%.
> That is almost entirely because the festive-packet roundups exist for CNY 2026 and Raya 2026 and were not found for 2024 or 2025.
> Equivalent campaigns almost certainly ran in both earlier years.
> **The per-year trend line (16.0 -> 17.0 -> 39.1) should not be read as growth.** The overall 25.0% is the number to quote; the year series is now less trustworthy than it was before this pass, not more.

From `japan/_VERDICT.md`, on its pagination artefact:

> **No 2024 rows were added.** The artist-side index pages that carried this vein (collabo-cafe tag pagination) run newest-first and the pages read reached back to 2025-02. 2024 remains the thin, format-skewed slice Section 5 describes, and is now *also* the only year the artist-side correction did not touch - so the 2024 vs 2025 gap in the per-year table is even more of a coverage artifact than before, not less.

From `thailand/_VERDICT.md`, whose per-year line reads as a collapse and recovery:

> **Do not report that as a market trend.** It is far more likely a sampling artefact, and the honest read is that this census cannot resolve a year-on-year indie trend for Thailand at all.

Korea's 2024 slice carries the same warning (only 3 of 23 new rows are 2024, because the trade magazine's index paginates newest-first), and Taiwan's 2026YTD is a partial seven-month year.
**No per-year figure from any of the five markets should be quoted as a trend.**

**2. The instrument is common, but not uniformly deep.**

> The first caveat is that the instrument is common but not uniformly deep.
> Taiwan's leg added 9 rows and Korea's added 23, not because Taiwan has less indie activity but because Taiwan's brand-side pass had already caught most of it; the residual risk is that a market with a low correction was well-swept and a market with a high correction may still be under-swept.

Malaysia is explicitly the least settled of the five: its honest range is **18.4% to 25.0%**, and a named backlog of seven Touch 'n Go creator cards plus roughly seven further social-evidence-only campaigns remains excluded purely for want of a date - dating them would add about another four points.
Each re-sweep is also, by construction, a targeted vein rather than a random sample.
Japan's and Korea's addenda both say so in the same words: the post-re-sweep figure should be read as *the ratio after adding a channel (or a press vein) the first pass under-covered*, not as a random-sample correction of a biased estimate.
**The direction is right and the mechanism is evidenced; the magnitude is not a confidence interval.**

**3. These are sample censuses, not exhaustive counts.**

Every one of the five verdicts says this in its own opening lines.
Shares are estimates from a structured sample of press-visible campaigns, not population parameters.
Recall bias runs toward campaigns that got covered, and each verdict states which direction that biases its own number: Japan and Korea judge it a slight *inflation* of indie share (indie collabs skew press-friendly), Taiwan and Thailand judge it a *suppression* (small and regional indie collabs are under-covered, and Thailand's unswept Facebook vein is the gap most likely to contain small-brand x indie campaigns).

**4. No outcomes anywhere.**

> **What is not claimed anywhere in any of these censuses:** no outcome, no sell-through, no royalty, no performance figure, for any row in any market.

This comparison inherits that standard without exception.
Nothing above is a claim about whether any campaign worked.
Every figure here counts *campaigns that provably happened and who owned the IP in them*, and nothing else.
Where a creator is described as reaching a national brand, that is a statement about a campaign existing, not about how it performed.

---

## 7. What's next

The five markets measured here are the ones swept, not the ones that matter.
**Singapore, Hong Kong, Indonesia, Vietnam and the Philippines** are the named next markets, and they should be built artist-side from birth rather than swept brand-side and corrected later - the four-mechanism taxonomy in Section 2 is now a set of testable per-market predictions (does the local trade press credit creators in-headline; is there an artist-named-campaign channel; is there a segregated creator-facing trade publication; is the dominant local-creator format one whose brand-side coverage omits the creator), and each new market either confirms or breaks it.
Three named pieces of unfinished work sit inside the existing five: **Malaysia's dateless backlog** (seven Touch 'n Go creator cards plus roughly seven social-evidence-only campaigns, worth about four points), **the zh-language Malaysian press**, swept only lightly because EN and BM filled the leg, and **Thailand's unswept Facebook and LINE Creators Market veins**, which are that market's largest known holes and the ones most likely to raise its number.
This document re-renders as markets join and as those holes close.
