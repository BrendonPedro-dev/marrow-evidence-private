# Vietnam co-branding census - verdict

Market nine in the region-by-region series (Taiwan v2, Japan, Korea, Malaysia, Thailand, Singapore, Hong Kong, Philippines precede it).
Identical definition, identical ownership test, identical pinned edge cases, so this market compares row-for-row with the other eight.
Table: `findings/census/vietnam/campaigns.md`.
Run date 2026-07-29.
**n = 47 curl-verified rows.** 94 of the 97 source URLs cited in the table and its exclusion/rejection sections returned HTTP 200 at verdict build time; the three failures are all `dantri.com.vn` and are addressed in section 5.

**This market does not reach the ~80-row floor, and the shortfall is the finding rather than a gap in the work.**
The target explicitly permits a documented coverage ceiling in place of the floor, and section 5 documents one at measurement grade rather than as an impression.
The short version, stated up front because everything below rests on it: a sweep of **2,607,744 Vietnamese article URLs across 28 publishers** returns 47 rows, and the same sweep shows that Vietnamese consumer press in this window writes about roughly **five character properties** with any regularity while **23 properties that anchor multiple rows in Taiwan, Japan, Korea and Thailand appear zero times**.
Vietnam is a genuinely thinner co-branding market at this date, not an under-swept one.

Two further facts shape everything below and are stated here rather than buried.
First, **both Vietnamese marketing trade titles (`brandsvietnam.com`, `advertisingvietnam.com`) are unreachable from this client at any path**, and those are precisely the titles that would carry creator-credited campaign write-ups.
Second, **the domestic independent character layer is one row**, and that single row is the most consequential number in this file.

---

## 1. The ratio

**Overall - the quotable numbers:**

| Class | Rows | Share |
|---|---|---|
| PORTFOLIO | 43 | **91.5%** |
| INDEPENDENT | 4 | **8.5%** |
| UNCLEAR | 0 | 0.0% |

**The number behind the number, and it is the one that matters for Vietnam.**
Three of the four independent rows are **Vietnamese fine artists licensing an artwork or a design** (rows 15, 38, 39), not character IP.
Exactly **one** row in the entire census is a domestic independent **character** IP inside a brand campaign: **Thỏ Bảy Màu x Liên Quân Mobile (row 7)**.
So the headline 8.5% and the underlying **independent-character share of 1 in 47 (2.1%)** are different claims, and only the second one answers the question this market was opened to answer.
**2.1% is the lowest independent-character share in the nine-market series**, and no earlier market required this distinction to be drawn, because in the earlier markets the independent rows were overwhelmingly character IP already.

**Per year** (the per-year caveat carries: 2026YTD is only seven months, and row 38's Tết run begins after its 2025 announcement date, tagged 2025 on the same rule applied to row 15):

| Year | Rows | PORTFOLIO | INDEPENDENT | Indie share | Of which character IP |
|---|---|---|---|---|---|
| 2024 | 20 | 18 | 2 | 10.0% | 1 (row 7) |
| 2025 | 18 | 17 | 1 | 5.6% | 0 |
| 2026YTD | 9 | 8 | 1 | 11.1% | 0 |

On n=2, n=1, n=1 there is no trend to read and none is claimed.
The only defensible per-year statement is that the independent layer is present in all three years and never exceeds two rows in any of them.
The 2026YTD row count (9 in seven months, against 20 and 18 in the full prior years) is **not** evidence of a contracting market; it is the standard lag of a press-indexed instrument on the most recent months, and the same shape appears in the earlier markets in this series.

**No tranche caveat is needed here, which is itself worth recording.**
The 47 rows came from three adjudication tranches over three successively larger corpora, and the independent share was 2 in 24 (8.3%) after tranche 1, 3 in 37 (8.1%) after tranche 2 and 4 in 47 (8.5%) after tranche 3.
Unlike Hong Kong, where a second tranche moved the ratio 26-fold, and unlike the Philippines, where an artist-side tranche moved it 2.3-fold, **Vietnam's ratio did not move when the artist-side net was repaired, rescored on accented titles and pushed across the fashion glossies**.
Tranche 3's artist-side pass returned 194 artist-shaped candidates after dedupe and produced exactly one row.
That stability is the strongest single piece of evidence that 8.5% is the market's number and not the instrument's.

**Where Vietnam sits in the series:**

| Market | n | Independent share |
|---|---|---|
| Japan | 131 | 30.5% |
| Taiwan v2 | 129 | 27.1% |
| Korea | 135 | 24.8% |
| Thailand | 83 | 20.5% |
| Hong Kong | 93 | 14.0% |
| Malaysia | 103 | 12.6% |
| Singapore | 81 | 8.6% |
| Philippines | 82 | 8.5% |
| **Vietnam** | **47** | **8.5%** |

Vietnam ties the series floor on the headline ratio and sits alone underneath it on the character-IP reading.
The right comparison is not Singapore, whose 8.6% comes from a small, rich, import-driven market with a developed licensing trade, but a market that has not yet formed a character-licensing supply side at all.

---

## 2. The addressable-indie read

**REPRESENTABLE split across the 4 independent rows:**

| REP | Rows | Row numbers |
|---|---|---|
| yes | 4 | 7, 15, 38, 39 |
| no | 0 | - |
| unclear | 0 | - |

**No Vietnamese independent row is label-captive**, and no Vietnamese equivalent of the Toyzeroplus arrangement was found anywhere in the corpus.
There is no Vietnamese agency or label holding a stable of local character IP under exclusive commercial terms.
That is not a positive finding about openness; it is a consequence of there being almost no local character IP under commercial management to hold.

**The addressable number: 4 rows, 4 distinct named creator entities.**

| Row | Brand | Creator entity (REP=yes) | What was licensed |
|---|---|---|---|
| 7 | Liên Quân Mobile / Garena Vietnam | **Huỳnh Thái Ngọc** (họa sĩ, creator of Thỏ Bảy Màu) | A creator-owned webcomic character, licensed into an in-game skin |
| 15 | VIB | **Bùi Công Khánh** | A specific artwork ("Trăm sông về biển lớn") licensed onto a customer gift |
| 38 | Sapporo Việt Nam | **Khim Đặng** | A commissioned design carried across a Tết can line |
| 39 | Jadify | **Vương Linh** | An oil painter's rendering of a folk figure, licensed onto a product |

**Four is the count of distinct named creator entities with at least one evidenced brand campaign in the window and no captive arrangement.**
It is a floor set by a press-only instrument, and section 5 names the veins that would raise it.
But it is a much harder floor than the equivalent numbers in the earlier markets, because the corpus that produced it is the largest in the series by an order of magnitude and was greped end to end for named indie properties, not only searched.

**Of those four, exactly one is a character IP and three are artwork licences.**
That distinction is not pedantry for a licensing thesis.
An artwork licence is a one-shot commission with no franchise behind it: Bùi Công Khánh, Khim Đặng and Vương Linh each licensed a single piece for a single seasonal product, and none of the three has a character with a name, a canon or a merchandising line.
Only Huỳnh Thái Ngọc holds a property that can be licensed repeatedly, and the corpus shows him monetising it through **publishing** rather than licensing: Thỏ Bảy Màu's only other 2024-2026 appearance is a new exclusive edition of the comic itself, announced 2026-04-08.

**The most important names in this section are the ones with no brand campaign attached.**
The census found three creator-owned Vietnamese character properties with real public profiles and **zero** brand campaigns in the window:
- **Pikalong** (họa sĩ Bùi Đình Thăng / Thăng Fly), covered as a culture feature across all three sweep waves and never as a campaign partner.
- **Mèo Mốc**, present as a webcomic property and absent from every brand-side query.
- **Thỏ Bảy Màu itself outside row 7**, which is the same property returning to books rather than to brands.

**And the counter-example that changes the read.**
**Wolfoo (Sconnect Việt Nam)** reaches a domestic FMCG brand's packaging (row 29, Bibica "Zoo" jelly candy) and a full film-campaign activation.
Wolfoo scores **PORTFOLIO** on the ownership test, because Sconnect is a company with a slate rather than a creator, so it does not move the independent count by a single row.
What it establishes is that **a domestic-owned Vietnamese character IP can and does reach a domestic Vietnamese brand at scale**, and that the bridge from local character to local brand is therefore built and passable.
The four independent creators are not blocked by a missing commercial bridge.
They are on the wrong side of a **corporate-form** threshold: the domestic character IP that crosses into brand campaigns in Vietnam is the one owned by an animation studio with a rights department, and the creator-owned properties are the ones that do not cross.
That is the single most useful sentence in this file for an argument about representation.

---

## 3. Format mix

| Format bucket | Rows | Share | Independent rows |
|---|---|---|---|
| Licensed retail collection / drop (apparel, eyewear, jewellery, beauty, stationery, gift product) | 17 | 36.2% | 1 (row 39) |
| Mall / department-store / venue pop-up, installation and exhibition | 10 | 21.3% | **0** |
| FMCG packaged goods (on-pack, limited-edition packaging, licensed confectionery) | 8 | 17.0% | 1 (row 38) |
| Game / platform in-game collaboration | 4 | 8.5% | 1 (row 7) |
| F&B chain (chain-wide drinks and merchandise programmes) | 3 | 6.4% | **0** |
| Device / vehicle | 3 | 6.4% | **0** |
| Banking and loyalty | 2 | 4.3% | 1 (row 15) |

### The closed-formats cut

Vietnam's independent rows do not cluster in one format the way the Philippines' clustered in retail drops.
They are **one row in each of four different formats**, which means this market has no open format and no closed format in the statistical sense: it has four isolated instances.
What can be said with the evidence, and stated as closure rather than as a rate:

- **Mall, department-store and venue formats: 10 rows, zero independent.** Vincom, AEON Mall, Crescent Mall, Lotte Mall West Lake, Thiso Mall Sala, SC VivoCity, Gigamall, Lotte Department Store and Vinpearl Harbour between them account for over a fifth of the census. Every character they hosted is portfolio-owned, and **nine of the ten** are POP MART, Bandai Namco, Disney or Shogakukan/Fujiko properties; the tenth (row 4, ZOOKiZ) is a multi-IP animation studio whose nationality the Vietnamese source does not state. **Vietnamese mall operators have licensed no creator-owned Vietnamese character in the window.** This is the same complete closure the Philippines showed, in a market with a comparably dense mall scene.
- **F&B chain: 3 rows, zero independent.** Starbucks Vietnam twice and MIXUE once, licensing Sanrio, Warner and a Tencent game roster. The Vietnamese chain-coffee scene that the task named as the density play (Highlands Coffee, Phúc Long, The Coffee House, KATINAT, Phê La, Cộng) produced **zero rows in the entire census**, from any IP, portfolio or independent. That absence is discussed in section 5 as a coverage question, but repeated targeted sweeps of those brand names across 2.6M URLs did not surface a character campaign for any of them.
- **Device and vehicle: 3 rows, zero independent.** Honda Vietnam x Marvel, vivo x POP MART ZSIGA, Ulike x Kuromi. All three are global or regional licensor programmes given a Vietnamese launch channel.
- **Convenience and QSR: zero rows of any kind.** Circle K, WinMart, GS25, FamilyMart, Ministop, Bách Hóa Xanh, Co.opmart, KFC, Lotteria, Jollibee, McDonald's Vietnam and Popeyes were all swept by name across three waves. The only things the sweep returned were a FamilyMart loyalty-consulting agreement with no character IP and a KFC Tết music video, both rejected. **In Vietnam the convenience-store and QSR character campaign, which is the single densest format in Taiwan, Japan and Korea, does not appear in press at all.**
- **The formats that are open, such as they are:** licensed retail drops (the largest bucket and the one that took row 39), FMCG packaging (row 38), games (row 7) and banking loyalty (row 15).

**The cut for the pitch:** Vietnam has no format in which an independent creator has a demonstrated repeatable route to a brand campaign.
It has four one-off crossings in four different formats, and the highest-distribution formats in the market (mall, F&B chain, convenience, QSR, device) are closed without exception.

### The IP-concentration cut, which is specific to this market

| Licensor family | Rows |
|---|---|
| Disney / Pixar / Marvel | 10 |
| POP MART (Labubu, MOLLY, DIMOO, ZSIGA, Hirono, SKULLPANDA) | 7 |
| Garena-operated game platforms (Liên Quân Mobile roster, Free Fire IP crossovers) | 7 |
| Sanrio | 4 |
| Warner Bros. Discovery (Harry Potter) | 3 |

**Five licensor families account for 31 of 47 rows (66.0%), with no row counted twice.**
The Garena bucket is the one that needs a footnote: it groups by the platform running the campaign rather than by the IP owner, and it includes row 7, whose licensed-in IP (Thỏ Bảy Màu) is independent.
Two facts follow.
First, the Vietnamese licensing market is a Disney-and-POP MART market with a games layer, and a brand wanting a character in Vietnam is choosing from a very short list.
Second, and less obviously, **the most-used single IP by Vietnamese brands is Liên Quân Mobile**, which appears in four rows (7, 13, 14, 47) fronting instant noodles, feminine-care packaging, a 1,000-store drinks chain and a webcomic collaboration.
It is a Tencent/TiMi title published locally by Garena, so it scores PORTFOLIO, but functionally it is the closest thing Vietnam has to a national character roster in brand campaigns.
That is where a domestic property would have to compete, and it is also, in row 7, the only door a domestic independent character has actually walked through.

---

## 4. Methodology and edge cases

### 4a. Which mechanism Vietnam exhibits - the naming question, answered

The task's taxonomy prediction was that Vietnam would behave like **TH/MY (erasure: brand PR omits the creator)** or like **KR (segregation: a creator-facing scene invisible to brand press)**.
**Vietnam exhibits neither. It is a third mechanism, and the evidence for that is unusually direct.**

**It is not erasure. Vietnamese press names creators, and names them in the headline and the URL slug.**
- Row 39: the article slug is `jadify-hop-tac-hoa-si-vuong-linh-...`. The creator's name and profession are in the URL.
- Row 15: the slug is `vib-ket-hop-bui-cong-khanh-...`. Same.
- Row 38: the headline is `bia sapporo hợp tác với nghệ sĩ Việt...`, the artist is named in the lede, quoted in the first person about their own concept, and the collaboration is titled after that concept.
- Row 7: the slug is `...cha-de-cua-tho-bay-mau-len-tieng` and the body identifies **họa sĩ Huỳnh Thái Ngọc** as "cha đẻ" of the character, unambiguous authorship language in Vietnamese.
**Three of the four independent rows carry the creator's name in the URL slug itself, and the fourth carries the creator's name and the authorship term in the body.**
Credit behaviour in Vietnamese consumer press is, on this evidence, better than in Thailand or Malaysia.

The point holds inside portfolio rows too, which is where erasure markets usually give themselves away.
Row 32 credits **nghệ sĩ Kasing Lung** as Labubu's creator inside a POP MART mall pop-up write-up.
Row 26 credits the Thai illustrator **Kanyada Phatan** by name inside a UNIQLO x Studio Ghibli licence, alongside producer Toshio Suzuki.
A market that erases creators does not name the third-party illustrator inside a global corporate licence.

**It is not segregation either, and this is the harder half of the call.**
The Korean pattern is a large creator-facing scene that brand press does not cover.
Vietnam has a large, active, well-covered **họa sĩ** press vein: once the artist-side net was repaired with token-boundary matching and rescored on accented titles, it returned a consistent result set across all three waves.
But that vein is **fine-art gallery coverage**: solo shows, group shows, museum retrospectives and painting competitions.
It is not a character-licensing scene held apart from brand press.
Tranche 3 tested this directly by pushing the artist-side net across `elle.vn`, `bazaarvietnam.vn`, `lofficielvietnam.com` and `kilala.vn`, which are exactly where a creator-credited campaign write-up would sit if one existed.
194 artist-shaped candidates after dedupe produced **one** row.
There is no hidden creator economy, because there is barely one to hide.

**The mechanism Vietnam exhibits is absence of supply, not suppression of it.**
Naming norms are healthy, the brand-side appetite for characters is real and growing, the mall and retail infrastructure is in place, and a domestic character IP demonstrably reaches a domestic FMCG brand (Wolfoo x Bibica).
What is missing is a population of creator-owned, licensable Vietnamese character properties.
The one that exists and has crossed (Thỏ Bảy Màu) crossed into a game, not into retail, and has since gone back to publishing.
**Call it the pre-formation mechanism: the market's credit behaviour and its distribution channels are ready before its independent IP supply is.**
That is a materially different diagnosis from Thailand's and Malaysia's, and it has the opposite implication for representation: in an erasure market the work is to make existing creators visible, and in Vietnam the work is that the licensable properties have not been built yet.

**One structural caveat on this call, stated plainly.**
The two titles that would most directly test it, `brandsvietnam.com` and `advertisingvietnam.com`, are 403 to this client at every path across two attempts with different user-agents and language headers.
A US-indexed web search reaches their article URLs, which proves the block is client-specific rather than a robots policy, and proves the content exists.
**The mechanism call above therefore rests on consumer-press evidence alone.**
This is the Vietnamese form of the Thailand Positioning-Mag lesson and it is repeated in section 5 as a named hole.

### 4b. The domestic character scene - where the addressable count was lost

The task predicted the local sticker/chibi/illustrator-merch scene would be where the addressable-indie read is won or lost.
**It was lost, and the loss is measurable rather than inferred.**

A whole-corpus grep of all **2,607,744 URLs** for named Vietnamese indie character properties, run after the corpus was rebuilt to persist every URL rather than only lexicon matches, returns a scene that exists in culture coverage and does not exist in campaign coverage.
Pikalong, Mèo Mốc and Thỏ Bảy Màu are all present, all covered, all creator-owned, and between them hold one brand campaign in two and a half years.

The most-covered Vietnamese character-IP story of the entire window is not a campaign.
It is the **Sconnect v. Entertainment One (Peppa Pig) copyright litigation** over Wolfoo, carried repeatedly by VietnamNet and VTC News.
A market whose largest character-IP news story is a dispute about a domestic property, rather than a licensing deal using one, is a market at the stage this census found it at.

### 4c. Vietnam-specific edge cases applied

- **The own-mascot exclusion**, applied to **Vietjet's "Amy" panda** aircraft mascot. Smaller in this market than in the Philippines, because Vietnamese brands run fewer proprietary character mascots than Philippine QSR does.
- **The own-retail exclusion**, applied to **at least seven POP MART Vietnam store openings** (Crescent Mall, Vạn Hạnh Mall, Hà Nội, Thiso Mall Sala and others) and to **LEGO Playground** at Crescent Mall. The venue precedent keeps the contrast clean: a licensor property hosted by a third-party venue as a limited run is a row (17, 22, 23, 25, 31, 32, 37), the licensor's own permanent store is not.
- **The self-promotion limb of the own-mascot rule**, applied to the **Doraemon check-in space at Đường Sách TP.HCM**: the rights-holder promoting its own film, at a municipal book street, with no third-party brand licensing the character in. Row 23 is the contrast, where the same IP sits in a commercial mall under a third-party host.
- **The Kumamon rule, and it removes the largest character-adjacent category in the Vietnamese corpus.** The annual **Tết zodiac `linh vật` statuary** on đường hoa Nguyễn Huệ and its provincial equivalents is commissioned by provincial People's Committees, so the whole class is excluded even where the press names the designer. This is worth flagging for the series: `linh vật` was carried into the lexicon as "mascot" and in Vietnamese practice it almost always means municipal Tết statuary, which inverts the assumption the brand-side lexicon was built on.
- **The cross-border rule**, applied to reject Sky x Cinnamoroll, POP MART x Lazada, STARLUX x PEANUTS, Maje x Hot Wheels, Samsung Z Flip6 Doraemon (Hong Kong-only), Clinique x Hello Kitty (yen-priced), SK-II x CRYBABY and UNIQLO's MAGIC FOR ALL. Each was covered in Vietnamese with no Vietnamese store, date, venue or VND price.
- **A rejection class specific to Vietnam and larger than any single rejection: grey-import limited editions.** Honda's Thai and Japanese subsidiaries run a steady character-licensed limited-run motorcycle programme (Super Cub Disney, Giorno+ Disney Fantasia, Monkey Star Wars, Scoopy Hello Kitty / Kuromi / Cinnamoroll), Vietnamese motoring press covers all of it, and the Vietnamese bodies state in each case that the bikes arrive through private importers and non-authorised dealers rather than Honda Việt Nam. Ten or forty grey-imported units is retail arbitrage, not a campaign run in Vietnam. **Row 40 is the contrast that makes the line clean**: an Honda Vietnam product, announced by Honda Vietnam, in a stated 4,000-unit Vietnamese run.
- **Per-IP ownership test applied even where one creator sits on both sides** (Molly Factory precedent), which is what holds MOLLY and MEGA SPACE MOLLY at PORTFOLIO in rows 25 and 31 despite Kenny Wong's authorship.
- **Estates and foundations are PORTFOLIO**, which is what classifies row 8 (UNIQLO x KAWS x Andy Warhol). This is the market's clearest mixed-ownership row: the Warhol half is foundation-held, the KAWS half is a living creator, and it is classified on the controlling licensor.
- **Artwork licences are counted on the illustration-IP limb of the definition** (the adidas PH x Aral Cru precedent), which is what admits rows 15, 38 and 39. Section 1 records why they are then held apart from character IP in the reading.
- **A folklore edge case worth carrying forward.** Row 39's subject is Sơn Tinh - Thủy Tinh, a Vietnamese public-domain legend. The IP licensed is **the artist's rendering**, not the legend, and the Vietnamese phrasing "hình tượng ... trong tác phẩm" is what carries that distinction. Public-domain folklore rendered by a named living artist is the artist's IP; the folklore itself is not a row.
- **The anti-inflation merge, used heavily, and it does more work in Vietnam than in any earlier market.** The VCCorp network (kenh14, cafef, soha, afamily, cafebiz) republishes one PR under near-identical slugs at the highest rate in this series: deduplicating 3,486 fetched titles by normalised headline collapsed them to 2,436 distinct campaigns, so roughly **30% of the Vietnamese candidate pool is one campaign wearing several bylines**. Merges applied: the Conan 30th HCMC and Hà Nội legs into one row (5), the Solite x Disney product launch and character event into one row (11), the Kotex announcement and tournament into one row (14), and the Fahasa summer-programme Pokémon announcement into row 46 rather than a row of its own.
- **A dating trap applied throughout.** VCCorp article IDs normally encode publication date, but aFamily's 236-prefixed IDs do not, and `kilala.vn` serves placeholder `datePublished` values on a flat undated sitemap. Two convincing "UNIQLO x IP now in Vietnam" candidates found on kilala proved to be 2021 on reading the body. **Year tags in this census come from the stated campaign window or the article's own `datePublished`, never from the URL id, and on flat-sitemap hosts never from metadata at all.**

---

## 5. Coverage-confidence statement

**What this census is.**
A sample census of 47 curl-verified rows, every one confirmed against a live Vietnamese source returning HTTP 200 with the campaign detail in the page body, read in Vietnamese, with evidenced dates and no outcomes claimed anywhere.

**Honest depth.**
The instrument is a three-wave sitemap archive sweep, not a search API.
Both the WP-REST portal sweep that built seven earlier markets and the Google News RSS fallback that built Hong Kong are dead in Vietnam, and native site search is closed.
What worked instead: the VCCorp/Epi publishing stack exposes the entire back archive as dated sitemap chunks, and Vietnamese slugs are unaccented ASCII, so a lexicon can be matched against slugs with no search endpoint at all.
- **Wave 1:** 10 portals, 3,322 chunks, 1,729,767 URLs.
- **Wave 2:** 5 portals (lifestyle and marketing trade tier), 1,517 chunks, 335,736 URLs.
- **Wave 3:** 12 portals (news, verticals, fashion glossies), 1,109 chunks, 750,647 URLs.
- **Corpus: 2,607,744 distinct article URLs across 28 publishers, 2024-01-01 to run date.**
Candidates were scored twice: recall on the unaccented slug, then precision on the **accented title and `og:description`** fetched from the first 180 KB of each candidate, which is the only reliable way to separate `họa sĩ` from `khóa SIM`, `Kinh Đô` from `kinh doanh`, `San-X` from `sản xuất` and `Liên Quân` from `liên quan`.
The residual unread band is the score 11-12 tier of the wave-2/3 accented-title shortlist, 429 entries after dedupe, dominated by the `dân chơi` and `quy tụ` false friends and by film-release coverage.
Its expected yield is low but not zero, and it is the one part of the adjudication queue not read end to end.

**The coverage ceiling, measured. This is the section that replaces the ~80-row floor.**
Three independent lines of evidence, all quantitative:

1. **Marginal yield is stable and low.** Waves 2 and 3 added 1,086,383 URLs, a 72% increase on the corpus, including every Vietnamese lifestyle, fashion and marketing title with a reachable sitemap. They returned **10 rows**. The measured rate is roughly **one row per 110,000 Vietnamese article URLs**, and it held to within 6% across two independent expansions (one per 117,000 in tranche 2, one per 109,000 in tranche 3). Reaching 80 rows at that rate would require roughly **3.6 million further URLs**, which is 1.4 times the entire swept corpus again, from Vietnamese publishers that do not exist.
2. **The press vocabulary is about five names.** Grepping all 2,607,744 URLs for 45 character-IP name tokens that are staples of the eight earlier markets returns Labubu 239, Baby Three 171, Barbie 114, Hello Kitty 66, capybara 45, and then falls off a cliff: MOLLY 16, KAKAO 16, Sanrio 8, Peppa Pig 7, Kuromi 6, Cinnamoroll 6, CRYBABY 5, Miffy 4, Gudetama 4, Smiski 3, Sonny Angel 2, Shin-chan 2, Hot Wheels 2, and one each for ZSIGA, Moomin, Monchhichi, Hirono and DIMOO.
3. **Twenty-three properties return literally zero.** Chiikawa, Sumikko Gurashi, Rilakkuma, mofusand, LINE FRIENDS, BT21, Loopy, Tuzki, Pusheen, Care Bears, Bluey, PAW Patrol, Sylvanian Families, SKULLPANDA, Pucky, HACIPUPU, My Melody, Pochacco, Keroppi, nyanko, Butterbear, Bellygom and wiggle wiggle appear **not once in 2.6 million Vietnamese URLs**, and every one of them carries multiple rows in Taiwan, Japan, Korea or Thailand.

**This is a ceiling in the market, not in the instrument, and (2) and (3) are what prove the difference.** The same sweep, over the same publishers, in the same window, finds Labubu 239 times. An instrument that can find one property 239 times and 23 others zero times is not failing to see; it is reporting an absence.

**Single-source count: 32 of 47 rows (68.1%).**
15 rows carry two or more independent sources.
The single-source rate is lower than the Philippines' 79.3%, which is a direct artefact of VCCorp republication: where a campaign is covered at all, it is often covered three times.

**A source-concentration caveat that no earlier market required.**
The 47 rows draw on only **13 distinct publisher domains**, and `kenh14.vn` alone supplies 24 of the 97 cited URLs.
**14 rows rest on `kenh14.vn` alone, and 27 of 47 rows (57.4%) rest entirely on titles inside the VCCorp network** (kenh14, cafef, soha, afamily, cafebiz).
Those five titles share an editorial pipeline and a press-release intake, so the census's independence-of-sources assumption is weaker in Vietnam than in any earlier market.
It is stated here rather than smoothed over.

**Translation confidence.**
Every row rests on a Vietnamese-language source read in Vietnamese, and no row rests on machine translation alone.
**6 of 47 rows (12.8%) carry an explicit translation-confidence flag** in Notes: rows 7 and 38 at **high** (unambiguous authorship and commissioning language, "cha đẻ" and "hợp tác với nghệ sĩ đương đại ... để tạo nên một thiết kế mới"), rows 10, 34 and 41 at **medium** (the Vietnam activation rests on syntax or on the brand's own Vietnamese channel rather than on a stated VN on-sale date), and row 39 flagged for the folklore-versus-rendering distinction that the phrase "hình tượng ... trong tác phẩm" carries.
The two flags that matter for the verdict's conclusions are both **high**, and both are on independent rows.

**Named holes, in order of size:**

1. **`brandsvietnam.com` and `advertisingvietnam.com` are unreachable from this client at every path.** Brands Vietnam returns 200 on its bare homepage only, 403 on every path with a query string and on all four of its own advertised sitemaps, and the homepage HTML carries no article links. Advertising Vietnam returns 403 to everything including the homepage. Both were retried with a Safari user-agent and vi-VN language headers. A US-indexed web search reaches their article URLs, so the content exists and the block is client-specific. **These are the two Vietnamese titles most likely to carry creator-credited campaign write-ups, and the section 4a mechanism call is made without them.** This is the single largest hole in this census and the direct Vietnamese analogue of the Thailand Positioning-Mag lesson.
2. **Brand, mall and creator Facebook, Instagram and TikTok accounts are entirely unswept**, and in Vietnam these carry a very large share of campaign communication - larger, plausibly, than in any earlier market in this series, because Vietnamese brands run campaign comms on social first and press second. Section 2's count of four addressable creators is a floor set by a press-only instrument.
3. **The cinema-chain character combo programme cannot be reached at evidence grade.** CGV and Lotte Cinema both run film-tie-in combos with licensed character merchandise, one of them a Demon Slayer tag-bag combo at a stated VND price, but that programme lives on the chains' apps, ticketing pages and voucher aggregators and appears in no swept title. It is a real Vietnamese format this census does not cover. The census has **zero cinema-format rows** and that is a coverage gap, not a market finding.
4. **The chain-coffee format returned zero rows, and this one is genuinely ambiguous.** Highlands Coffee, Phúc Long, The Coffee House, KATINAT, Phê La, Cộng Cà Phê, Trung Nguyên, ToCoToCo and Gong Cha were swept by name across all three waves and produced no character campaign. The task named this as a density play and it did not materialise. Two readings are available and the evidence does not separate them: either Vietnamese chain coffee runs its character work on social and in-store only, or it does not run character work at scale. **Row 47 (MIXUE x Liên Quân Mobile, 1,000+ stores) is the one data point on the other side**, and it is the strongest F&B row in the census, which mildly favours the first reading.
5. **`vnexpress.net` is present at a small fraction of its true archive.** Its historical daily sitemaps 302-redirect to the homepage and only the most recent days resolve. VnExpress is one of Vietnam's largest titles and this census has effectively not swept it.
6. **`dantri.com.vn` is under a standing client-side block.** Three cited URLs time out at 60 seconds on every attempt, and have done so across two tranches and a day, where they returned HTTP 200 in tranche 1. **No row rests on a dantri.com.vn source alone**: two of the three are secondary sources on rows 21 and 35 which carry other live sources, and the third is a rejection note. `tuoitre.vn` degrades the same way under concurrency and must be re-fetched at five threads or fewer.
7. **Nine further Vietnamese titles could not be swept at all:** `laodong.vn` (JavaScript cookie interstitial), `24h.com.vn` (empty urlset), `doisongphapluat.com.vn` (index with no dated chunks), and `gamek.vn`, `yan.vn`, `sport5.vn`, `ttvn.toquoc.vn`, `markettimes.vn`, `harpersbazaar.vn`, `style-republik.com`, `nhipsongthitruong.vn` (404, redirect loop or no response). `marketingai.vn`, the closest reachable substitute for the trade titles, publishes only **1,095 articles across the whole 2024-2026 window**, about one a day, so it is a real title but not a volume substitute for the trade press.
8. **Three rows carry weaker VN-specificity than the rest and are flagged in place** rather than quietly kept: row 28 (Free Fire x Squid Game, a global event with no VN-only hook, counted because Garena Vietnam operates the VN server and issued the Vietnamese announcement), row 34 (UNIQLO x Labubu, no stated Vietnamese on-sale date) and row 41 (vivo x ZSIGA, same). **If a stricter cross-border reading dropped all three, n falls to 44 and the independent share rises to 9.1%.** The ratio is not sensitive to them.

**What this census can and cannot support.**

It supports the claim that the Vietnamese independent share of evidenced brand-x-character campaigns is **8.5%**, and that this figure is stable across three tranches and three corpus expansions including one that specifically targeted the artist-side vein.

It supports the much sharper claim that the **independent-character** share is **1 row in 47 (2.1%)**, the lowest in the nine-market series, and that the other three independent rows are one-off artwork commissions rather than licensable properties.

It supports the claim that **Vietnamese press credits creators properly** where there is a creator to credit, and therefore that the constraint in this market is IP supply rather than press erasure or scene segregation.

It supports the claim that the market's highest-distribution formats - **mall, F&B chain, convenience, QSR, device** - are closed to independent creators, and that the convenience and QSR formats are closed to character campaigns entirely at the level this instrument can see.

It supports, at measurement grade rather than as an impression, the claim that **47 rows is close to what an exhaustive press-based census of Vietnam 2024-2026YTD would return**, on the marginal-yield rate, the five-name press vocabulary and the 23 zero-count properties together.

It does **not** support any claim about campaign outcomes, sales, footfall or performance. None is made anywhere in this file or the table.

It does **not** support a claim that the addressable Vietnamese creator pool is four. That is the floor a press-only instrument reached with both trade titles blocked and all social channels unswept, and section 2 names three creator-owned Vietnamese character properties with no brand campaign attached that a social-media sweep would start from.

It does **not** support a claim that Vietnamese chain coffee and Vietnamese cinema run no character campaigns. Both formats have identified, named instrument gaps, and both are recorded as gaps rather than as findings.
