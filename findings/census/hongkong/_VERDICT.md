# Hong Kong co-branding census - verdict

Market seven in the region-by-region series (Taiwan v2, Japan, Korea, Malaysia, Thailand, Singapore precede it).
Identical definition, identical ownership test, identical pinned edge cases, so this market compares row-for-row with the other six.
Table: `findings/census/hongkong/campaigns.md`.
Run date 2026-07-29.
**n = 93 curl-verified rows.** All 138 source URLs in the table returned HTTP 200 at build time.

Hong Kong is the second market, after Singapore, to run both keyword classes from birth.
It is the first market in the series where **the method itself broke and had to be rebuilt mid-run**, twice, and both breaks are load-bearing on how the numbers below should be read.
The WP-REST portal vein that built the six earlier markets does not exist here; the Google News RSS vein that replaced it was resolvable only through Google's `batchexecute` endpoint, which hard-blocked this client after 302 of 781 candidates.
The consequence is stated up front rather than in section 5: **this table was built in two tranches on two different instruments, and the second tranche was deliberately pointed at the artist-side and label-name queries first.** Section 1 gives both numbers.

---

## 1. The ratio

**Overall - the quotable numbers:**

| Class | Rows | Share |
|---|---|---|
| PORTFOLIO | 78 | **83.9%** |
| INDEPENDENT | 13 | **14.0%** |
| UNCLEAR | 2 | 2.2% |

**And the number that must be quoted beside it.** The 93 rows are not one sample.
Rows 1-77 came from generic brand-side queries worked in date order - an unbiased pass - and hold **2 independent rows in 77 (2.6%)**.
Rows 78-93 came from a second tranche that worked the artist-side and label-name queries *first, on purpose*, and hold **11 independent rows in 16 (68.8%)**.

Neither figure is Hong Kong's indie share.
The first is a floor produced by an instrument that demonstrably cannot see the layer; the second is a ceiling produced by an instrument aimed straight at it.
**The honest statement is that HK's true independent share is materially above 2.6%, that 14.0% is the best available estimate and is biased upward, and that the size of the gap - a 26-fold difference in hit rate between two query classes on the same market in the same window - is itself this census's largest finding.** No other market in the series produced a spread anything like it.

**Per year** (the per-year caveat carries and is sharper here than usual, because the two tranches did not land evenly across years - 2026YTD is also only seven months):

| Year | Rows | PORTFOLIO | INDEPENDENT | UNCLEAR | Indie share |
|---|---|---|---|---|---|
| 2024 | 39 | 33 | 4 | 2 | 10.3% |
| 2025 | 30 | 28 | 2 | 0 | 6.7% |
| 2026YTD | 24 | 17 | 7 | 0 | 29.2% |

**Do not read a trend off this.** The 2026YTD indie share is 29.2% because five of the seven 2026 independent rows are LuLu the Piggy and LeonLollipop campaigns that the second tranche went looking for, and the 2025 share is 6.7% because the second tranche found fewer 2025 artist-side candidates before the run ended, not because 2025 was a portfolio year.
The year split measures reading order, and this is the market where that is most true.

**Where Hong Kong sits in the series.** At 14.0% the headline indie share sits mid-table - above Singapore (8.6%), below Taiwan-v2, Korea (34.0%) and Japan, close to Malaysia's post-re-sweep figure.
But the shape underneath is unlike any of them:

- **Portfolio concentration is the most extreme in the series.** Three licensors account for 34 of 93 rows (36.6%): **Chiikawa 12 rows, Disney 12, Sanrio 11**, with row 44 counted once as a Sanrio x Chiikawa joint line. Add Doraemon (7), Harry Potter (4), Crayon Shin-chan (3), Snoopy (3) and Pokémon (3) and the imported-portfolio core is **54 of 93 rows (58.1%)**.
- **Chiikawa alone is 12.9% of every campaign in this market**, across McDonald's twice, Sushiro twice, Giordano, Chow Tai Fook, MINISO, Niko-Niko, Harbour City, K11 MUSEA, Star Ferry and MOKO. No single IP in any earlier market approaches that share. The pinned ナガノマーケット rule (creator-originated by ナガノ, IP business run by 講談社 / ちいかわ製作委員会) therefore does more classification work in Hong Kong than anywhere else in the series, and a meaningful part of HK's portfolio share is a Chiikawa artefact.
- **The independent layer is one label plus five individuals.** Six of the thirteen indie rows are a single property - LuLu the Piggy - and the other seven are spread across six unrelated creators with one row each (Plastic Thing has two). Section 2 is where that matters.

---

## 2. The addressable-indie read

Thirteen INDEPENDENT rows, resolving to **seven distinct independent IPs**:

| IP | Rows | REP | Ownership evidence | Why this REP call |
|---|---|---|---|---|
| 罐頭豬 LuLu the Piggy (TOYZEROPLUS) | 78, 79, 81, 89, 91, 92 | **no** | Creator-owned (designer Cici); sources consistently name TOYZEROPLUS as the *partner label* rather than the author - "本地玩具品牌TOYZEROPLUS", "潮流文化公司TOYZEROPLUS" | Indie by ownership, exclusively channelled through the Toyzeroplus label - the pinned Taiwan-v2 row 5 / Thailand row 12 call, applied here **in the label's home market** |
| Plastic Thing (為食妹 / 肥妹) | 16, 93 | **yes** | Character brand of HK illustrator Yan Ip, self-described "100% Plastic Made in Hong Kong"; no label, studio or corporate parent in any source | Creator-owned, no exclusive channel evidenced, and a documented history of open commissions across unrelated clients (SOGO, LOG-ON, Golden Elephant) - the Tobyato profile |
| 圓DUM DUR, Hello Wong, 豚豚 (three creators, one row) | 82 | **yes** | Three named HK illustrators licensing their own characters into a mall campaign; no agency, label or parent named for any of them | Creator-owned; commissioned brand work with no exclusivity signal |
| LeonLollipop | 88 | **yes** | HK artist working under his own name, interviewed at length in the second source about his authorship of the campaign characters and of the 托腮貓 Gloomie mural character | Creator-owned; takes open commissions (East Point City, and the rejected THE SOUTHSIDE project) |
| BUCKET MAN (馮德倫 Stephen Fung) | 87 | **yes** | Source states the IP was created by 馮德倫, who appeared as its founder; no studio, label or platform parent named | Non-exclusive on the evidence: Michael Lau figure at ComplexCon HK, HSBC, Grade10, Comic Con - different partner each time |
| Gloomy The Naughty Grizzly (Mori Chack) | 90 | **unclear** | Source states Mori Chack drew the collaboration illustrations himself and owns the character; no parent named | Creator-owned but no representation arrangement is public, and Mori Chack is not an HK creator |
| Juju (CJ Hendry) | 73 | **unclear** | Australian artist working under her own name with a named creative production partner; no corporate or platform parent | Creator-owned with no label parent evidenced, but no representation arrangement stated either way, and she is a foreign artist licensed *into* an HK campaign |

**Distinct addressable (REP=yes) creator count: 6** - Yan Ip / Plastic Thing, 圓DUM DUR, Hello Wong, 豚豚, LeonLollipop, and 馮德倫 / BUCKET MAN.
Five of the six are Hong Kong creators; all six are named individuals rather than companies.

**REP split within the indie rows: no 6 (46.2%), yes 5 (38.5%), unclear 2 (15.4%).**

### The label-captive hypothesis: confirmed, and by a single label

The brief predicted that Hong Kong's REP=no share of indies would be the highest in the series, because HK is the art-toy label capital.
**It is - at 46.2%, narrowly ahead of Taiwan-v2's ~44.7% and roughly double Singapore's 28.6% and Japan's ~29%.** The prediction holds.

But the mechanism is not the one the hypothesis assumed, and the difference matters commercially:

- **The HK number is one label, not a label economy.** All six REP=no rows are Toyzeroplus/LuLu. **How2work, Kennyswork and ToyQube - the other three labels the brief named - produced zero adjudicable campaign rows in either tranche.** Their names appear in this sweep only inside trade-show coverage and licensor's-own-retail coverage, both of which the definition excludes.
- **Taiwan's comparable number is a creator self-licensing** (Bugcat Capoo through 卡特島創意, 8 of 17 REP=no rows). Hong Kong's is a creator channelled through someone else's label. Those are different objections to representability: the first is a competitor, the second is an incumbent contract.
- **The one Toyzeroplus property is doing extraordinary work.** Six rows across a silverware house, a suburban mall, a Halloween pop-up, a LOG-ON shrine at New Town Plaza, a century-old Cantonese teahouse and HK's first LuLu café - 2024 through 2026, four formats, six different brand partners. LuLu is the only IP in this table, portfolio or independent, that reaches a heritage dim-sum restaurant and a jewellery brand and a mall atrium.

So the honest reading of the label-capital call is: **indie-by-ownership but captive-by-channel is real in Hong Kong and it is the single largest block on addressability here - but it is concentrated in one property rather than distributed across the label economy, and the rest of the label economy did not appear in consumer campaign coverage at all.** Whether that absence is supply or coverage is the sharpest open question in section 5.

### What the addressable six actually look like

The six REP=yes creators are individually small and commercially unmistakable:

- **Plastic Thing** is the closest thing HK has to a repeat licensor-grade indie: two rows here, a resolved 2024 UNCLEAR (row 16, LOG-ON's 25th-anniversary campaign, where 為食妹 was the lead IP over MF Bear, Sonny Angel and LuLu), a 2026 FMCG redemption with Golden Elephant rice distributed through ParknShop, Wellcome and HKTVmall, and prior SOGO work outside the window.
- **The iSQUARE trio** put three creators' characters across an entire mall's Chinese New Year for six weeks - the format HK malls otherwise fill with Sanrio and Disney.
- **LeonLollipop** appears twice in this run, once as a row (East Point City, 8 commissioned horse characters, 3,000 sq ft) and once inside a rejection (THE SOUTHSIDE's street-art project). That pair is worth more than either alone: the same creator crosses the census boundary in one direction and not the other within six months, and the difference is whether his characters front the campaign.
- **BUCKET MAN** is the market's only banking row and puts an independent IP on HSBC.

**The realistic ceiling is above 6 and the reason is named.** Both artist-side near-misses in the rejection list (THE SOUTHSIDE's five HK artists; OCTO Gambol x 寂寞鱷魚) are HK brand x HK creator collaborations that failed the *definition*, not the ownership test - one because commissioned district artwork is not a character IP fronting a campaign, the other because the only located source was Taiwanese with NT$ pricing. Six named HK creators sit in those two rejections alone.

---

## 3. Format mix and year trend

Every row is assigned to exactly one format; the buckets are mutually exclusive and sum to 93.

| Format | Rows | Share | 2024 | 2025 | 2026YTD |
|---|---|---|---|---|---|
| Mall pop-up / mall campaign | 32 | 34.4% | 13 | 9 | 10 |
| Retailer and department-store pop-up / themed store | 21 | 22.6% | 15 | 4 | 2 |
| Apparel, accessory, jewellery and FMCG collection | 11 | 11.8% | 4 | 5 | 2 |
| QSR and F&B themed menu / merch drop | 10 | 10.8% | 1 | 4 | 5 |
| Venue, attraction, transit and touring exhibition | 8 | 8.6% | 2 | 4 | 2 |
| Themed café | 5 | 5.4% | 2 | 2 | 1 |
| CVS, grocery, loyalty and non-profit | 4 | 4.3% | 2 | 0 | 2 |
| Banking and airline | 2 | 2.2% | 0 | 2 | 0 |

**Retail floorspace is the Hong Kong signature: 53 of 93 rows (57.0%)** are a mall pop-up, a mall campaign, or a retailer- or department-store-led themed store.
Add themed cafés and venue formats and it is 66 of 93 (71.0%).
Hong Kong runs character IP as **leasable atrium**: Festival Walk hosts eight of these rows, Langham Place five, K11 three, Harbour City two, Hysan Place two, AIRSIDE two, plus Times Square, New Town Plaza, MOKO, Citygate, Central Market, YOHO MALL, MOSTown, iSQUARE, East Point City, Pacific Place, Kai Tak Retail Park, TKO PopCorn, Citywalk, Mira Place, The ONE, 皇室堡, Ngong Ping 360 and The Mills.
Singapore concentrated in venue formats at 38.3%; Hong Kong does it at 57.0% on mall formats alone, and it is the densest single-format concentration measured in the series.

**Two movements worth naming, both against thin year slices:**

1. **Retailer-led displaced by mall-led.** The retailer/department-store bucket falls from 15 rows in 2024 to 4 in 2025 and 2 in 2026YTD, while the mall bucket holds at 13/9/10. Part of this is real - 2024's LOG-ON, IDEAS, SOGO, APITA, Niko-Niko and kkplus activity has no 2026 equivalent in this table - and part is tranche composition, since tranche 1 read 2024 most heavily. Treat as directional.
2. **QSR rises and is where the biggest brands are.** 1 row in 2024, 4 in 2025, 5 in 2026YTD - McDonald's twice, Sushiro three times, Starbucks twice, Godiva, ABURI-EN, 蓮香樓. Every one of those is a portfolio IP except 蓮香樓 x LuLu, which is the only independent property to reach the QSR/F&B format in this market.

**The formats independents reach, and the ones they do not.** The 13 indie rows sit in: mall (5), retail (3), café (1), QSR/F&B (1), FMCG (2), banking (1).
**No independent row appears in the venue/attraction/transit bucket** - the MTR, Star Ferry, Ocean Park, Ngong Ping 360 and Disneyland-adjacent campaigns are all portfolio.
Transit and attraction licensing in Hong Kong is a closed door to local creators in this window, and that is a cleaner statement of the addressability problem than the ratio is.

---

## 4. Methodology and edge cases

### 4a. Which of the four mechanisms Hong Kong exhibits

The four-mechanism taxonomy from `FIVE_MARKET_COMPARISON.md` s2 - **erasure** (Thailand, Malaysia), **channel** (Japan), **segregation** (Korea), **none of the above** (Taiwan) - was set up as a per-market prediction. Hong Kong breaks it, and the way it breaks is informative.

**Test 1: does the press erase the creator? No.** The opposite. zh-HK consumer press names local illustrators *in the headline*, as a selling point, exactly as zh-TW does:
「iSQUARE**聯乘三大本地人氣插畫家**呈獻『福氣滿滿玩轉肥年』」 (香港文匯報);
「金象牌80周年**聯乘 Plastic Thing** 禮品同步開換」 (巴士的報);
「東港城**聯乘LeonLollipop** 創作全新8款駿馬角色」 (大紀元);
「香港服裝品牌 OCTO Gambol **攜手本地人氣插畫家 寂寞鱷魚**」.
HKET even ran a full creator interview with LeonLollipop about his authorship. This is the Taiwan pattern, and it rules erasure out.

**Test 2: is there a separate artist-named channel the brand-side queries cannot reach? No.** The creator-fronted campaigns run in the *same* titles as the portfolio ones - 文匯報, am730, 巴士的報, U Lifestyle, HKET, 大紀元 - and use the *same* vocabulary (聯乘, 期間限定, 快閃店). This is not Japan.

**Test 3: is there a segregated creator-facing trade publication? Not found.** No HK equivalent of Korea's 아이러브캐릭터 surfaced in 135 queries.

**So on all three diagnostics Hong Kong should be Taiwan - "none of the above", the control case, where the two keyword classes return overlapping sets and the artist-side class adds nothing.**

**It is not. The artist-side class added 11 of this census's 13 independent rows.**

The resolution is a mechanism the taxonomy does not contain, and Hong Kong is the market that exposes it:

> **Crowding-out.
> The creators are named, in the same publications, in the same words - and are still invisible to a brand-side query, because the market's portfolio volume saturates every generic result set before a creator-fronted campaign can rank.**

The evidence is direct. The harvest ran 135 queries and returned 5,125 articles; Google News caps a query at 100 items, which is why every high-yield keyword had to be split by year in the first place.
In a market where Chiikawa is 12.9% of all campaigns and Chiikawa, Disney and Sanrio together are 37.6%, a query for 聯乘 香港 in a given year returns a hundred Chiikawa, Sanrio and Disney items and stops.
The iSQUARE, Plastic Thing and LeonLollipop articles were **in the harvested pool the whole time** - returned by 插畫家 聯乘 香港, 本地插畫家 香港 品牌, 原創角色 香港 聯乘 - and were absent from tranche 1 only because they sat behind the blocked resolver.
The artist-side keyword class did not reach a different *corpus* here, as it did in Japan or Korea. It reached the same corpus through a **less contested query**, and that was sufficient.

This is a distinct finding from all four prior mechanisms, and it has a sharp practical implication: **in a market with extreme licensor concentration, brand-side keyword census methods systematically under-count the local creator layer even when the local press is fully creator-attributive.** Taiwan's null result is what "no mechanism" actually looks like; Hong Kong looks like Taiwan on every press diagnostic and behaves like Japan on the numbers. The difference between them is not journalism. It is portfolio density.

The honest limit on this read is in section 5 and is severe: 479 of 781 candidates were never resolved, so the crowding-out claim rests on the shape of a 302-candidate resolved set plus 16 title-resolved second-tranche rows, not on the full pool.

### 4b. The cross-border trap - the GBA edition, and the rejection it cost

Hong Kong and Greater-Bay/mainland campaigns are announced together and reported by HK media as one item, so the market's specific failure mode is counting a Shenzhen or Shanghai activation as an HK one.
The rule applied: a row requires evidenced HK activation - named HK stores or outlets, an HK launch date, an HK mall or transit venue, HK$ pricing, or .hk commerce.

Rejected under this rule (full list in `campaigns.md` section A): **MINISO x Chiikawa** in Shanghai/Beijing, Shenzhen and 福田星河COCO Park (three separate rejections, RMB pricing throughout - the HK leg of the same series activated in June and is row 11); **蠟筆小新 快閃店** at Shenzhen 南山益田假日廣場, an HK paper's 「北上」 shopping feature; **「米奇與好朋友」快閃店** in Zhongshan/Taipei; **ZO&FRIENDS pop-up, Korea** (the HK legs are rows 53 and 63); **Sonny Angel 深圳首間快閃店**; **星星人 POP BAKERY 深圳**; **澳門旅遊局 x POP MART** (Macau).

**Retained despite a non-HK source:** rows 1 (CTWANT, Taiwanese), 42 (travelerluxe, Taiwanese), 48 and 51 (Taiwanese second sources), 60 (Kyodo) and 62 (niusnews, Taiwanese) - each because the *body* evidences a named HK venue and a dated HK window.
The test is activation evidence, not the outlet's nationality.

**And the rejection the rule cost, applied in reverse: OCTO Gambol x 寂寞鱷魚** (rejection class H). An HK clothing label's first collaboration with a named HK illustrator, four SKUs - rejected because the only located source is Taiwanese, prices are NT$, and no HK venue, HK press or .hk channel is evidenced.
That is an independent HK creator row the rule removes.
It is listed rather than quietly kept, because a rule that only ever excludes mainland campaigns and never excludes a row you want is not a rule.

### 4c. Edge cases applied

- **The label-capital rule - this market's defining call.** Dug past every label to the creator: label-*owned* character = PORTFOLIO; creator-owned but exclusively label-channelled = INDEPENDENT with REP=no; creator-owned and non-exclusively label-distributed = INDEPENDENT with REP per evidence. Applied to LuLu the Piggy across six rows (78, 79, 81, 89, 91, 92): INDEPENDENT / REP=no, carrying the Taiwan-v2 row 5 and Thailand row 12 precedent into the label's home market unchanged. Applied to Plastic Thing in the other direction (rows 16, 93): creator-owned, no label, REP=yes.
- **Self-presentation is not ownership - and the Molly Factory precedent, twice.** Row 85 (UNIQLO x THE MONSTERS): the HK source calls 龍家昇 Kasing Lung a 「本地插畫家」 and the row is still PORTFOLIO, because POP MART controls the commercialisation. Row 53/63 (ZO&FRIENDS): artist-co-created with G-DRAGON and still PORTFOLIO, because IPX owns it. Row 83 (Peanuts 75th): four HK artists including **Kenny Wong, MOLLY's own creator**, commissioned to restyle Snoopy - the IP is Peanuts, so PORTFOLIO. Authorship is not ownership, in all three directions.
- **Government-owned mascots (the Kumamon rule) - applied twice on the IP side.** The Hong Kong Police Force's anti-fraud mascot 「提子」 and the 15th National Games licensing programme are both excluded. Applied in the correct column: **state-adjacent brands licensing third-party IP are normal rows** - row 9 (Hong Kong Tourism Board x LINE FRIENDS), row 46 (MTR x Disney), row 62 (Ocean Park x Sanrio), row 45 (Ngong Ping 360 x Disney), row 74 (Star Ferry x Chiikawa), row 8 (Hong Kong Red Cross x Snoopy, an NGO). Excluding these would have applied the Kumamon rule to the brand side.
- **Anti-inflation merges.** Row 90 is The ONE plus 皇室堡, two Chinese Estates malls in one campaign - **one row**. Row 60 is Sushiro across 40 branches - one row. Row 40 is ABURI-EN across 8, rows 12/17 are IDEAS across 4, row 37 is Sushiro across 4, row 33 is SOGO across 2. Row 26 folds a second wave; row 16 folds a LuLu 5th-anniversary zone into the campaign that hosted it. Unmerged, these would have added well over 60 rows for no new campaigns.
- **Licensor's own retail excluded; venue-hosted properties are rows** (Taiwan-v2 row 126 precedent). POP MART's airport store, OH!SOME, Sanrioworld+ Central and the trade-show circuit (Ani-Com & Games HK, CON-CON, Amazing Toy Show x GRADE 10, 香港潮玩嘉年華, 香港國際授權展) are all excluded. A licensor property hosted by a third-party venue is a row: row 68 (CHIIKAWA SHOP at MOKO), row 50 (CRYBABY at Festival Walk), row 63 (ZO&FRIENDS at Kai Tak Retail Park).
- **Commissioned original characters.** Row 88 (East Point City x LeonLollipop) is characters *created for* the campaign rather than an existing property licensed in. Retained as a row - a named creator's characters front the consumer campaign and the creator owns them - and flagged in the row itself, because it is a distinct commercial mechanism from licensing and a reader tallying "existing IP licensed in" should be able to remove it.
- **Borderline rows kept visible rather than quietly dropped:** row 47 (Lee Kum Kee x Bandai gashapon - the consumer-facing IP is a capsule-toy programme, not a character), row 69 (K11 x Sunkist's Joocies - a brand-owned collectible rather than a third-party licence), row 71 (759 阿信屋 / 大生 x Doraemon biscuits - closer to licensed merchandise at retail than to a campaign). Each is flagged in its Notes; removing all three moves the indie share from 14.0% to 14.4%.

---

## 5. Coverage-confidence statement

**Depth: adequate for the portfolio picture, provisional for the indie picture, and the difference is the whole of this section.**

- **n = 93** against a stated floor of ~80 and a stretch target of 120-140. The floor is met with margin; the stretch target is not.
- **The coverage ceiling is a named tooling failure, not a judgement about the market.** 781 candidates were harvested; 302 were resolved to publisher URLs before Google's `batchexecute` endpoint began returning `302 -> google.com/sorry/index` to every request from this client, including single serialised requests hours apart. **479 candidates still hold a title, a publisher and a date but no URL.** The second tranche worked around this by locating articles from their titles and then `curl`-verifying at the publisher - which preserves the evidence standard exactly, and is roughly an order of magnitude slower per candidate. **That, and only that, is why n is 93 rather than 130.** Hong Kong is not a thin market; 5,125 distinct articles across 60+ publishers say the opposite.
- **57 of 93 rows are single-source (61.3%)**, and 36 carry two or more. That is materially better corroboration than Singapore (90.1% single-source) and reflects a denser publisher set: 香港01, U Food, UHK 港生活, HKET, U Lifestyle, 星島頭條, Time Out HK, 新假期, am730, Eastweek, Popbee, on.cc, 巴士的報, 文匯報, 大公文匯網, orangenews, Yahoo HK and weekendhk all appear as sources.
- **All 138 source URLs re-verified at HTTP 200 on 2026-07-29.** No row cites a `news.google.com` URL; Google News is the index and the publisher page is the evidence. No outcome claims appear anywhere in the table - where a source reported sales figures, queues or resale prices (rows 38, 60, 76, 85), the Notes say so and the figure is not carried.
- **Two UNCLEAR ownership rows (2.2%)**, both 2024, both cases where multiple HK sources cover the campaign in full and name no creator, studio or licensor: row 5 (小燦 SHO-CHAN) and row 29 (BUNNI KONBINY). A third, row 16 (為食妹), was resolved to Plastic Thing during this run by an unrelated 2026 row - which is evidence that the remaining two are resolvable rather than genuinely unresolvable.
- **Six rows carry a non-HK publisher flag** and three carry a thin-source or venue-thin flag (29, 61, 67, 81). Row 81's venue is unresolved.

**Named holes - what would move the numbers:**

1. **The 479 unresolved candidates are the single biggest hole in this census, and they are recoverable.** They are not lost data - each has a title, a publisher name and a publication date, and the title-search route demonstrably works. Working them is mechanical, and on the tranche-2 hit rate it would plausibly take this market past the 120-140 target. **Nothing else in this run would move n as much.**
2. **The indie share is bounded below at 2.6% and above at 14.0% and this run cannot narrow it further.** Section 1 states both. Any future tranche must interleave the two query classes rather than run one to exhaustion, or the same bias reappears.
3. **The label economy beyond Toyzeroplus is unmeasured.** How2work, Kennyswork and ToyQube produced zero campaign rows. Two readings are available and this run cannot separate them: either those labels genuinely do not license into third-party consumer campaigns (they monetise through their own retail, gallery drops and the trade-show circuit - which the rejection list shows is exactly where they *do* appear), or they do and the coverage missed it. **This is the highest-value question in the market and it is a two-or-three-document job** - the labels' own release archives - rather than another sweep.
4. **Brand, mall and creator Instagram/Facebook are entirely unswept**, and this bites harder in Hong Kong than in Singapore. Two of the six addressable creators (Plastic Thing, LeonLollipop) run IG/FB as their primary announcement channel; Plastic Thing's SOGO work surfaced in this run only through a Facebook post reproduced by a deals aggregator. A social sweep would find creator-fronted campaigns that no portal covered, and it would move the indie number in one direction.
5. **Marketing-Interactive is unreachable to `curl` and unswept**, as it was in Singapore. HK's marketing trade title is the vein most likely to carry agency-side and creator-attributed campaign detail.
6. **Sites that could not be swept directly at all:** hk01, am730, holidaysmart, hk.ulifestyle, girlstyle, urbanlifehk, mamidaily, timeout, tatlerasia, elle.com.hk, esquirehk, openrice (404 on `/wp-json`); weekendhk, nmplus, orangenews, discoverhongkong (403); localiiz (526); bastillepost (503); sundaykiss (DB error on `search=`); thehoneycombers (empty array). Individual articles from these titles are reachable and `curl`-verifiable - many rows above cite them - but site-wide search is not, so nothing was found *by* searching them.
7. **The mechanism finding in 4a is provisional on hole 1.** Crowding-out is well-evidenced by what was found, but it is an argument about what a saturated result set omits, and the definitive test is the unresolved pool.

**The honest read.** The 83.9 / 14.0 split is trustworthy as a description of *Hong Kong's consumer-facing licensed-character economy*: the densest mall-led character market measured in this series, running at extreme licensor concentration, with Chiikawa alone fronting one campaign in eight.
It is a weaker description of *Hong Kong's creator economy*, and this verdict says so with a number rather than a hedge: the same market, in the same window, in the same publications, returns a 2.6% indie share to a brand-side query and a 68.8% indie share to an artist-side one.
The direction of any correction is one-way - upward - and the two rejections in class H, six named HK creators between them, are where the next of it will come from.
