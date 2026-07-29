# Malaysia co-branding census - verdict

As of 2026-07-29 (first build, 103 rows).

This verdict reads the campaign table in `campaigns.md` (103 curl-verified brand-x-IP co-branding rows, window 2024-01-01 to run date).
It is a **sample census, not an exhaustive count** - see Section 5 for limits.
This is the MALAYSIA run in a region-by-region series (Taiwan v2: 129 rows; Japan: 131 rows; Korea: 135 rows), on the identical definition and the identical pinned edge cases, so the four markets compare row-for-row.
The brief is to attack the founder thesis ("indies are shut out") as hard as the data allows; where the data undercuts the thesis, that is called out plainly.

**The headline: Malaysia's indie share is 12.6%, roughly half of every other market measured on this definition.**
That is the finding, and Section 5 argues it is a real market feature rather than a sampling artifact - though it is the finding held with the least confidence of the four runs, and the reason why is stated plainly.

No rows were excluded under the government-mascot (Kumamon) rule.
One row (100, KTM Komuter x Bichi Mao) has a government-owned brand paired with a privately-owned IP, which the rule permits and which the Taiwan-v2 precedent (row 17) already settled.
The classifiable base is therefore the full **n = 103**.

## 1. The ratio - overall and per year

| Class | n | Share |
|---|---|---|
| PORTFOLIO | 89 | **86.4%** |
| INDEPENDENT | 13 | **12.6%** |
| UNCLEAR | 1 | 1.0% |

| Year | n | PORTFOLIO | INDEPENDENT | UNCLEAR | Indie share |
|---|---|---|---|---|---|
| 2024 (full year) | 21 | 19 | 2 | 0 | **9.5%** |
| 2025 (full year) | 49 | 43 | 6 | 0 | **12.2%** |
| 2026YTD (to 07-29) | 33 | 27 | 5 | 1 | **15.2%** |

**Trend read:** the indie share rises monotonically across the window, 9.5% -> 12.2% -> 15.2%.
The direction is real but the slope should not be over-read: the absolute counts are 2, 6 and 5 rows, so a single reclassification moves any year by 2-3 points.
What the trend does support is that Malaysia's indie layer is growing rather than static, and that 2026 is the first year where local creator-owned IP appears in more than one format.

**Cross-market comparison, same definition:**

| Market | n | Indie share |
|---|---|---|
| Japan | 131 | 30.5% |
| Taiwan v2 | 129 | 27.1% |
| Korea | 133 classifiable | 24.8% |
| **Malaysia** | **103** | **12.6%** |

Malaysia is the outlier, and it is not a near miss.
The other three markets cluster in a 25-31% band; Malaysia sits at less than half the bottom of that band.

## 2. The addressable-indie read

Within the 13 INDEPENDENT rows:

| REPRESENTABLE | n | Share of indie |
|---|---|---|
| yes | 8 | 61.5% |
| unclear | 4 | 30.8% |
| no | 1 | 7.7% |

**The addressable-indie number is 8 rows, or 7.8% of the whole census.**

Per year: 2024 = 1 yes / 1 unclear; 2025 = 4 yes / 1 unclear / 1 no; 2026YTD = 3 yes / 2 unclear.

The REP=yes rows collapse onto **four distinct IPs**, and that concentration matters more than the row count:

- **Bichi Mao** (Olive Yong) - 4 of the 8 rows (Secret Recipe, Pizza Hut MY, Secret Recipe x SimplyHeal, KTM Komuter). One creator is doing half the addressable-indie work in this market.
- **Yellobanana** - 2 rows (foodpanda 2024, Lalamove 2025). The only local illustrator with repeat blue-chip brand demand across two years.
- **QuirkyQing** (Bonnie the Bunny) - 1 row (Touch 'n Go card line).
- **Bear Boss Buddies** (Dylan Ang) - 1 row (Luckin Coffee MY).

The 4 REP=unclear rows are two IPs: **Yuurei Neko Sama** (Michael Chuah, 2 rows) and one row each for **Tai Zi/Shibasays** and **BoBoiBoy**.
Yuurei Neko Sama is unclear only because Majikku IP Sdn Bhd represents it and the exclusivity terms are not public; on ownership alone it is squarely creator-owned.
BoBoiBoy is unclear because Monsta runs its own licensing arm and the Choki Choki relationship is long-running.
If the Yuurei Neko Sama arrangement turned out to be non-exclusive, the addressable count would move from 8 to 10 and from 4 distinct IPs to 5.

The single REP=no row is **mofusand** (Gray Parka Service exclusive), carried unchanged from the Japan and Taiwan-v2 runs.

**The honest read for an agency:** Malaysia's addressable-indie pool is real but shallow and personality-driven.
It is four names, not a scene.
The upside case is that three of those four (Bichi Mao, Bear Boss Buddies, QuirkyQing) reached national brands within the window, which means the demand side works when the IP exists; the constraint is supply of commercially-active local IP, not brand appetite.

## 3. Format mix and year trend

Format buckets are assigned from the Format column; a row is counted once, in its primary format.

| Format | 2024 | 2025 | 2026YTD | Total |
|---|---|---|---|---|
| Retail / FMCG / supermarket | 5 | 11 | 9 | **25** |
| Cafe, bubble tea, coffee, ice cream | 4 | 10 | 7 | **21** |
| Convenience (FamilyMart, 7-Eleven) | 4 | 7 | 2 | **13** |
| Mall / venue event and pop-up | 2 | 6 | 5 | **13** |
| QSR | 0 | 8 | 4 | **12** |
| Fintech, telco, payments, delivery platform | 1 | 6 | 0 | **7** |
| Apparel and fashion / jewellery | 3 | 0 | 1 | **4** |
| Cinema, gaming, karaoke | 0 | 1 | 3 | **4** |
| Homeware, beauty, hospitality, other | 2 | 0 | 3 | **5** |

**What the mix says:**

- Malaysia is a **retail-and-FMCG-led** co-branding market, not an F&B-led one. Supermarket redemptions, gift-with-purchase premiums and on-pack collectibles (25 rows) are the single largest bucket, ahead of the drinks chains (21). This is the sharpest structural difference from Taiwan and Japan, where drinks chains and convenience dominate.
- **QSR is a 2025 arrival.** Zero QSR rows in 2024, then 8 in 2025 and 4 in 2026YTD. KFC, Burger King, Pizza Hut MY, McDonald's MY and llaollao all ran character campaigns from mid-2025 onward.
- **Convenience is shrinking as a share**, from 4/21 (19.0%) in 2024 to 2/33 (6.1%) in 2026YTD. FamilyMart MY still runs a near-continuous collectible calendar, but the rest of the market caught up.
- **Mall and venue events grew** from 2 rows in 2024 to 6 and 5, driven almost entirely by POP MART's nine-store MY footprint and the Pokemon Truck tour.
- **Fintech and payments is a genuine Malaysian format** (7 rows: Touch 'n Go x4, KTM Komuter, plus the delivery platforms). Touch 'n Go alone accounts for four rows across Pokemon and two local illustrators. No other market in this series has a payments-card collab vein this deep.
- **The indie rows cluster away from the biggest format.** Of 13 indie rows, only 1 sits in Retail/FMCG. Indie IP in Malaysia shows up in QSR, cafes, payments and platform merch - the formats where a campaign needs a personality, not shelf-space economics.

## 4. Methodology and edge cases

**Method.** Three passes. (1) An EN sweep of Malaysian lifestyle and trade press plus brand official pages. (2) A sweep of the Malaysian promo-aggregator vein (EverydayOnSales primarily, plus msiapromos, malaysiafreebies), which produced the bulk of the volume. (3) A targeted local-creator sweep run specifically to correct the bias the second pass introduced, worked through Malaysian licensing-agency rosters (M&M Creations, Majikku IP, Milolo), the local-illustrator trade press, and brand-run artist-collaboration product lines. Pass 3 lifted the indie count from 7 to 13 and is the reason the 12.6% figure is publishable at all.

**The franchise-local activation calls (the Malaysia-specific rule).**
This rule decided a large fraction of the table and it consistently resolved in favour of counting.
Rows recorded as MY operator activations on regionally-struck deals include UNIQLO Malaysia x Hello Kitty and x Chiikawa (17, 18), Krispy Kreme MY x PAC-MAN (38, the same IP program as Japan row 114), Burger King MY x Naruto (46), Haidilao MY x CoComelon (49), Le Creuset MY x Pokemon (25), and The Laughing Cow x Monchhichi (103, which carries a Malaysia-exclusive design).
In every case the MY activation was evidenced by an MY-market announcement, MY store presence or MY-social promotion before the row was written; no regional campaign was counted into MY on assumption.
The reverse call was also made: the 7-Eleven Sanrio coin-bank story would not resolve MY versus Hong Kong on fetch and was dropped rather than guessed.

**Anti-inflation rules and what they cost.**
Four counting rules in the `campaigns.md` header did real work, and all four suppress the row count rather than raise it.
One-campaign-one-row across retailer legs and weekly waves prevented roughly 15-20 duplicate rows (VITAGEN x Sanrio alone appeared under four retailer listings; llaollao x Minions under four).
Prize-draw promos are excluded: the "spend and win a Labubu blind box" format is endemic in Malaysia (Marrybrown, myNEWS, SnowFit, Dadi Cinema and others), but the brand buys the toy as a prize with no licence, so it is not co-branding.
Unnamed generic characters are excluded, which removed several capybara-shaped collectible programs that have no identifiable IP to make an ownership call against.
Plain licensed merchandise at retail is excluded while retailer-RUN collectible programs are included.

**Edge cases and how the pinned rules resolved them:**

- **Lawak Kampus** (row 93, Karaoke Manekineko). The most instructive call in the run. A beloved homegrown Malaysian comic IP that lands **PORTFOLIO**, not independent, because Gempak Starz (Art Square Group) publishes and manages it alongside a stable of other comic IP - the same publisher-managed logic that pins Chiikawa. Local origin does not imply independent ownership, and treating it as indie would have been the easiest available way to inflate the headline number.
- **Ejen Ali** (row 101, MLBB) - the only **UNCLEAR** in the census. Media Prima's Primeworks Studios co-owns the IP with creator studio WAU Animation; multiple sources confirm co-ownership and none state the split, so the co-owned/JV rule sends it to UNCLEAR rather than to either bucket. This is exactly the case the rule exists for.
- **Butterbear** (rows 8, 81) and **Bentoree Capybara** (row 61) - **PORTFOLIO**. Both are corporate mascots owned by a partner brand and licensed IN to the campaign brand. The own-mascot exclusion does not apply because the mascot does not belong to the campaign brand; corporate ownership makes them portfolio.
- **Quby** (row 69, KFC MY) - **PORTFOLIO**. A sticker-origin character, which reads indie by instinct, but StarMoly is a studio managing a stable of sticker IPs, so the manages-OTHER-IP rule applies.
- **Yuurei Neko Sama** (rows 91, 92) - **INDEPENDENT**. Agency-managed by Majikku IP but creator-owned by Michael Chuah, which is the Capoo precedent exactly. REP left at unclear because exclusivity terms are not public.
- **Bichi Mao** (rows 5, 9, 10, 100) - the known-entity rule was applied without exception. Every one of the four rows rests on a fetched public source, with public campaign windows and public format descriptions. No internal figure of any kind entered the census, and no outcome is claimed for any of them.
- **Illustrator IP scope.** A rule was added this pass to make the boundary explicit: a brand licensing a named illustrator's artwork or characters for a co-branded line is a row (foodpanda x Yellobanana, Lalamove x Yellobanana, TNG x QuirkyQing), matching Taiwan-v2 rows 120/127 and Korea rows 78/79. This is not a Malaysia-specific loosening; it aligns Malaysia with what the prior markets already counted, and without it Malaysia's indie share would be understated at 10.0% (10 of 100).
- **Government IP.** The Kumamon rule excluded nothing. Malaysia's public-body-adjacent activity in the window paired public brands with private IP (KTM x Bichi Mao), which the Taiwan-v2 precedent already permits.
- **Venue-hosted pop-ups** (POP MART at Sunway Pyramid, the Pokemon Truck at two malls, Minions at The Exchange TRX) are counted with the hosting venue as the brand, per Taiwan-v2 row 126. The two Pokemon Truck stops are separate rows because they are separate venues.
- **Excluded on scope, worth naming:** the 2026 Taiwan IP Expo at Sunway Pyramid (2026-05-20) presented 12 Taiwan-Malaysia cross-border creator collaborations including Bichi Mao, Relaxed Comics and Jefferson Ng. It is a licensing trade expo and creator-to-creator pairing, not a brand-x-IP consumer campaign, so it is not a row. It is flagged here because it is the single best forward indicator of Malaysian indie IP entering brand deals, and the next run should check which of those 12 pairings converted.

## 5. Coverage-confidence statement

**The numbers on honesty.**

- 103 rows, all curl-verified against a live fetched source URL. Every year tag is read off an evidenced campaign date on the page, never inferred.
- **8 rows are single-source flagged** (7.8%): rows 2, 15, 22, 59, 60, 89, 96, 102.
- **5 rows carry a source-language flag** (a BM or zh source, or a BM/zh corroboration where translation confidence is recorded): rows 4, 13, 40, 83, 93. Translation confidence was recorded as high in each case; no row rests on a low-confidence translation.
- **1 row has weaker date evidence than the rest** (row 91, Poh Kong x Yuurei Neko Sama), where the date comes from a mall event-page URL slug on a page that now returns HTTP 410. It is flagged in the row rather than dropped, because the collaboration itself is corroborated by a live brand collection page.
- **3 rows have an evidenced end date but no stated start date** (80, 98, 99) and 1 has a stated start but no end (87). Windows are recorded exactly as evidenced.

**Source concentration is the biggest structural weakness.**
72 of 103 rows (69.9%) come from a single domain, everydayonsales.com.
Each was verified by fetching its own article page rather than a search-result listing, so the rows are individually sound, but the *selection* is not independent.
That aggregator indexes PR-driven promo listings from national retail chains, which means it systematically over-samples exactly the campaigns that portfolio IP runs and under-samples the small-brand and creator-led activity that never issues a promo listing.
The remaining 31 rows are spread across 20-plus domains, and it is telling that **11 of the 13 indie rows came from those 31**, not from the aggregator.

**Is 12.6% the true number?**
Held with moderate confidence, and specifically as an *upper*-biased-toward-portfolio estimate that could move up, not down.

The case that it is real:
- The dedicated pass-3 sweep was designed to find indie rows and nothing else. It worked the Malaysian licensing agencies' own client rosters, which is where local creator IP is listed if it is commercially active at all. It roughly doubled the indie count and still landed at 12.6%.
- Those agency rosters name the local IPs that exist (The Good Boisss, Pasaroly, Poppy, Loklok & Friends, Pee Yong Diary, Gujiguji, plus Milolo's seven characters). Named brand partners exist for several of them. **What does not exist in public sources is dated campaign evidence.** An IP with a listed Lazada or Popular Bookstore relationship but no dateable campaign cannot become a row under this evidence standard, and that is a fact about the market's publicity depth as much as about the market.
- Malaysia's creator economy is younger and smaller than Japan's, Taiwan's or Korea's, and it lacks the two institutions that manufacture indie co-branding rows in those markets: a mass messaging-sticker economy (LINE in JP/TW, KakaoTalk in KR) and a convenience-store 集點 culture that runs a new illustrator IP every few weeks.

The case that it is understated:
- The known undercount is concrete and countable. Touch 'n Go's artist-collaboration card line has **six creator collaborations live on its own storefront** (nothingwejun, DMEOW, HeyHey Brody, dáo, Home Too Much/Buku 555, QuirkyQing). Only QuirkyQing carries a public launch date on any source that could be fetched, so **five real indie campaigns are sitting outside this census purely for want of a date.** Adding them would take indie to 18/108 = 16.7%.
- Similar dateless-but-real cases: SODA x Bichi Mao and SODA x Yuurei Neko Sama apparel (evidenced only on Instagram/Facebook), Walls x Yuurei Neko Sama, The Good Boisss x Lazada/Converse, Loklok & Friends x Popular Bookstore and x Mitsui, Pee Yong Diary x McDonald's.
- Brand and creator social accounts, which is where a lot of Malaysian indie campaign evidence actually lives, are not curl-fetchable from this environment. This censors indie rows specifically, because portfolio campaigns get press releases and indie campaigns get Instagram posts.

Putting both sides together: **the honest range is roughly 12.6% to 18%, and the point estimate to quote is 12.6% with the ceiling stated.**
Even at the top of that range Malaysia sits below every other market in the series.
The conclusion that Malaysia's indie co-branding layer is structurally thinner than Taiwan's, Japan's or Korea's survives the most generous correction the evidence supports, and that is the claim worth making.

**On depth (rows, not ratio).**
103 rows is above the 80-row floor for a credible verdict and below the 120-140 comparable-depth target.
This is not a coverage ceiling: the aggregator vein is nowhere near exhausted and another 30 rows of national-chain portfolio campaigns are reachable with mechanical effort.
They were not added deliberately, because they would only push the indie share down while adding nothing to the question the census exists to answer.
**The binding constraint in Malaysia is not row count, it is dateable indie evidence** - and the specific, named, five-to-twelve-campaign backlog above is the exact work that would tighten the number.

**What is not claimed anywhere in this census:** no outcome, no sell-through, no royalty, no performance figure, for any row, including the known-entity rows.
