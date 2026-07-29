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

## Post-re-sweep addendum (artist-side keyword pass, 2026-07)

This section is appended, not merged.
Sections 1-5 above describe the census as it stood at 103 brand-side rows and are left intact so the two passes stay auditable.
Everything below reads rows 1-124.

**Why this pass ran.** The Thailand run established that brand-side keywords can structurally erase creators, and Taiwan, Japan and Korea were each re-swept before Malaysia on the same logic.
Malaysia was swept brand-side only, so its 12.6% was suspected of being understated.
Section 5 above already predicted this in concrete terms and named the backlog that would move it.

### The headline movement

| | Pre-re-sweep (n=103) | Post-re-sweep (n=124) |
|---|---|---|
| PORTFOLIO | 89 (86.4%) | 92 (74.2%) |
| INDEPENDENT | 13 (**12.6%**) | 31 (**25.0%**) |
| UNCLEAR | 1 (1.0%) | 1 (0.8%) |

**Malaysia's indie share moves 12.6% -> 25.0%, a +12.4pt correction - the largest in the five-market series, larger even than Thailand's +11.2.**

Per year:

| Year | Pre n | Pre indie | Pre share | Post n | Post indie | Post share |
|---|---|---|---|---|---|---|
| 2024 | 21 | 2 | 9.5% | 25 | 4 | 16.0% |
| 2025 | 49 | 6 | 12.2% | 53 | 9 | 17.0% |
| 2026YTD | 33 | 5 | 15.2% | 46 | 18 | 39.1% |

**Rows added: 21 (18 INDEPENDENT / 3 PORTFOLIO / 0 UNCLEAR).** The three portfolio rows (105, 107, 109 - Touch 'n Go x Hot Wheels twice and x TRANSFORMERS ONE) were appended even though they push the ratio the wrong way, because they surfaced in the same corporate-newsroom vein the artist-side query opened and honesty outranks convenience.
Without them the correction would read 12.6% -> 25.6%.

**The tighter reading, stated up front.** Ten of the 18 new indie rows are the *definitional frontier* - commissioned original artwork applied to a co-branded premium (festive packets, postcards, outlet merch) rather than a pre-existing licensed character.
They are counted because the census already counts that exact shape (rows 90 and 94, foodpanda and Lalamove x Yellobanana) and the header rule was written for it.
A reader who draws the line at pre-existing character IP gets **n=114, 21 indie, 18.4%**.
So:

**The honest range is 18.4% to 25.0%, with 25.0% as the point estimate on the census's own standing rule.** Either end of that range destroys the pre-re-sweep finding.
Section 1 above called Malaysia "the outlier, and not a near miss" against a 25-31% band; at 25.0% Malaysia sits *inside* that band and at 18.4% it is a near miss, not an outlier.

### What the artist-side keywords found that brand-side missed

Three mechanisms, and Malaysia is the first market in the series where the Thailand mechanism - true erasure - is clearly live alongside the others.

1. **Erasure in the festive-collateral format (the Thailand mechanism).** Malaysia's single densest local-creator format is the festive packet: sampul Raya and CNY angpao given with purchase.
Brand-side queries return these campaigns as *brand* stories ("BilaBila Mart Raya promotion", "CHAGEE angpao") and the illustrator's name appears nowhere in the brand's own promo listing.
The attribution exists in exactly one place - Marketing-Interactive's annual design roundups, which go brand by brand and say who drew each one.
Eight rows (112, 113, 114, 115, 117, 118, 119, 120) rest on those two URLs.
This is the Thai pattern precisely: the campaign was always visible, the creator was not.
2. **Campaigns named after the artist (the Japan mechanism).** Rip Curl Malaysia runs a standing quarterly creator-collaboration programme, "Artist of the Search", with a brand-official landing page indexed by artist name.
Four rows (108 KATUN, 110 Janggutbear, 116 Pangrok Sulap, 122 Perempuan Melawan Art) come from it.
Skechers runs the same shape as SkechVibe (row 124), and Montigo debuted a four-character line with Humana Art (row 123).
A brand-side query for "Rip Curl Malaysia promotion" reaches none of these, because the product is the artist.
3. **The corporate newsroom as a creator-attribution source.** Touch 'n Go's own press-release index carries dated, brand-official releases naming its creator partners (Loka Made, row 106).
The original pass reached only the TNG *shop*, which lists SKUs without dates - which is exactly why the original verdict logged five real indie campaigns as dateless.

Malaysia does **not** show Korea's segregation mechanism: there is no Malaysian equivalent of 아이러브캐릭터, no creator-facing character-industry trade publication.
That absence is itself the finding - Malaysian creator attribution lives in *general marketing trade press* (Marketing-Interactive), in *brand newsrooms*, and on *brand-official artist landing pages*, and the original pass used the first of those only for brand stories.

### The breadth movement - the more consequential number

Section 2 above reported the addressable-indie pool as "four names, not a scene": Bichi Mao, Yellobanana, QuirkyQing, Bear Boss Buddies.

| | Pre-re-sweep | Post-re-sweep |
|---|---|---|
| REPRESENTABLE = yes rows | 8 (7.8% of census) | 20 (16.1% of census) |
| REP = unclear | 4 | 10 |
| REP = no | 1 | 1 |
| **Distinct REP=yes creators** | **4** | **14** |

The ten new REP=yes creators are **Kirin Sharom / Bunga dan Bintang** (rows 104, 119 - the only new creator with two rows, and across two unrelated brands), **KATUN**, **Janggutbear**, **Nas Suha**, **Jean Lynn**, **Ame Lukis**, **Yatt**, **Perempuan Melawan Art / Finn Anuar**, **Humana Art / Vanissa Foo** and **Cloakwork**.
Only one of the twelve new REP=yes rows (115, Eco-Shop x YelloBanana) belongs to a creator the original pass already knew.

The six new REP=unclear rows are Loka Made (x2, corporate structure and licensing posture not public), Lihua, Pangrok Sulap (a collective with a community-redistribution model), Danial Kushairi (surfaced via a programme whose representation arrangement is not public) and the five-artist Maxim postcard row.

**This overturns Section 2's central reading.** "It is four names, not a scene" was a brand-side artefact.
Malaysia has at least fourteen distinct creator-owned IPs that reached a national brand inside the window, and the same concentration warning the Korea leg raised applies here: *a concentration finding in any of these censuses may be a query artefact rather than market structure.*

### Contradicted prior calls

**No existing row was reclassified, and no existing row's class evidence was contradicted.**

Two prior *claims* in Sections 1-5 are contradicted by the new rows and should be read as superseded:
- **Section 1, "Malaysia is the outlier, and it is not a near miss."** Superseded.
On the same definition Malaysia is now 25.0% against Japan 34.9%, Korea 34.0%, Taiwan 27.5%.
It is the lowest of the five, but it is within a few points of Taiwan and no longer a different order of magnitude.
- **Section 2, "four names, not a scene."** Superseded, as above.
- **Section 5, "the honest range is roughly 12.6% to 18%."** The realised number is above the top of that range.
The range was built on the assumption that the undercount consisted of the named dateless backlog; it did not.
The undercount consisted of an entire *format* (festive collateral) and an entire *channel* (brand creator-programmes) that no one had looked for.

One near-contradiction is flagged rather than acted on: **row 93 (Lawak Kampus, PORTFOLIO on the publisher-managed rule)** was cited in Section 4 as proof that "local origin does not imply independent ownership".
That call stands unchanged, but this pass found the opposite failure mode too - **Loka Made** and **Bunga dan Bintang** are locally-originated *and* creator-owned, and were invisible to the brand-side pass.
The lesson is not that local origin implies portfolio; it is that ownership must be tested per IP, in both directions.

### The dateless-indie backlog - result

This leg absorbed the backlog-dating sub-task.
The artist-side net was expected to be the right instrument for it.
**It was not, and the result is a clean negative.**

- **The Touch 'n Go artist-card line: still undated, and now larger.** All 160 releases in TNG's own press-release index were enumerated; not one of the artist cards has a press release.
They exist only as shop SKUs.
Two *additional* undated artist cards were discovered in the process - **ThatDania** (a two-design LED collector series) and **Jepah Studio** ("Ceria Merdeka").
**The dateless TNG backlog grows from five campaigns to seven.** The Section 5 arithmetic that "adding them would take indie to 18/108 = 16.7%" is superseded: adding all seven to the current table would give 38/131 = 29.0%.
- **SODA x Bichi Mao, SODA x Yuurei Neko Sama, Walls x Yuurei Neko Sama, The Good Boisss x Lazada and x Converse, Loklok & Friends x Popular Bookstore and x Mitsui, Pee Yong Diary x McDonald's:** all still undated.
EN, BM and zh artist-side queries returned no dated coverage for any of them.
They remain excluded and remain listed.
- **The 2026 Taiwan IP Expo's 12 TW-MY creator pairings: no conversions with dated evidence.** Only three of the twelve Malaysian creators are named in any fetched source (Bichi Mao, Relaxed Comics, Jefferson Ng); the pairings are a Crossover Art Exhibition of creator-to-creator artworks, and no fetched source reports a resulting brand campaign.
The expo's own TAICCA x Sunway Pyramid spend-and-redeem tote campaign is documented in the method note and excluded, because a 12-IP bundle admits no single ownership call.

**Why the backlog resisted, and what that says.** The dateless campaigns are all *product-page-only* relationships: a storefront listing, a Shopee SKU, an Instagram post.
The artist-side net works by finding editorial attribution, and there is no editorial attribution to find for these.
The correct read is that Malaysia's indie undercount was never mainly the named backlog - it was the campaigns nobody had thought to look for.
The backlog is still real, still uncounted, and would add roughly another 4 points on top of 25.0%.

### The REPRESENTABLE and Kumamon rules

No change.
The Kumamon rule still excludes nothing; row 100 (KTM Komuter x Bichi Mao) remains the only public-brand/private-IP pairing.
All 31 indie rows carry a REPRESENTABLE tag and all 93 non-indie rows carry '-' (verified programmatically).

### Method limits specific to this pass

1. **Source concentration got worse before it got better.** Eight of the 21 new rows rest on two Marketing-Interactive URLs, and both are single-source flagged.
Nine of the 21 are single-source overall.
The original build's problem was 70% dependence on everydayonsales.com; this pass swaps part of that for dependence on one trade publication's annual roundups.
It is a better publication for this purpose - it names creators, which is the whole point - but it is not source diversity.
2. **The 2026 skew is an artefact, not a surge.** Thirteen of 21 new rows are 2026YTD, and 2026's indie share jumps to 39.1%.
That is almost entirely because the festive-packet roundups exist for CNY 2026 and Raya 2026 and were not found for 2024 or 2025.
Equivalent campaigns almost certainly ran in both earlier years.
**The per-year trend line (16.0 -> 17.0 -> 39.1) should not be read as growth.** The overall 25.0% is the number to quote; the year series is now less trustworthy than it was before this pass, not more.
3. **Two BM-language rows carry translation-confidence flags** (104 glamlelaki.my, 108 eh.my, 110 glamlelaki.my, 121 iloveborneo.my - four in total).
Confidence was recorded as high in each; dates and brand/artist names are unambiguous in the source text.
4. **One new row has weaker date evidence** (116, Rip Curl x Pangrok Sulap), dated from a Shopify `created_at` timestamp inside the brand's own page because the page carries no editorial date.
Secondary reporting places it two months later; the earlier evidenced date is used and the discrepancy is recorded in the row.
5. **Five new rows have an announcement date but no stated campaign window** (110, 114, 115, 121, 124) and are recorded exactly as evidenced.
6. **The zh-language Malaysian press was swept only lightly.** The task list included applying Taiwan's zh terms (繪師, 插畫家, 圖文作家) to Malaysia's zh press; EN and BM produced enough volume to fill the leg, and the zh vein is not exhausted.
Any Malaysian-Chinese creator whose coverage is zh-only is likely still missing.
7. **Social-only evidence remains uncounted, and it censors indie rows specifically.** This is unchanged from Section 5 and is the reason the dateless backlog survived this pass intact.

### What this does to the cross-market table

| Market | Pre-re-sweep indie share | Post-re-sweep indie share | Correction |
|---|---|---|---|
| Thailand (reference, artist-side from the start) | 20.5% | 20.5% | - |
| Japan | 30.5% | 34.9% | +4.4 |
| Korea | 24.8% | 34.0% | +9.2 |
| Taiwan v2 | 27.1% | 27.5% | +0.4 |
| **Malaysia** | **12.6%** | **25.0%** | **+12.4** |

Malaysia's correction is the largest in the series.
The ordering of corrections is now explainable end to end: the size of the artist-side correction tracks **how much of a market's creator activity is documented outside the channels a brand-side query reaches**, and that varies with press convention (Taiwan credits creators in-headline, so nearly nothing was missed), with the size of the artist-named campaign channel (Japan), with whether a segregated creator trade press exists (Korea), and with whether the dominant local-creator format is one whose brand-side coverage omits the creator entirely (Malaysia, Thailand).

**The claim this census can now support:** Malaysia's indie co-branding layer is the thinnest of the five markets measured, but it is thin by degree, not by kind, and the "structurally thinner than Taiwan's, Japan's or Korea's" conclusion in Section 5 no longer survives at the strength it was written.
What survives is narrower and still worth saying: Malaysia's indie campaigns are *smaller in format* - festive packets and capsule tees rather than nationwide drink series and pop-up circuits - and its creator layer is far broader than the original pass could see.

**What is still not claimed anywhere in this census:** no outcome, no sell-through, no royalty, no performance figure, for any row, including the known-entity rows.
