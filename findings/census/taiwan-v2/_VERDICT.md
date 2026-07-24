# Taiwan co-branding census (v2 re-run) - verdict

As of 2026-07-24 (v2 re-run, 129 rows).

This verdict reads the campaign table in `taiwan-v2/campaigns.md` (129 curl-verified brand-x-IP co-branding rows, window 2024-01-01 to run date).
It is a **sample census, not an exhaustive count** - see Section 5 for limits.
This is the **v2 re-run** of Taiwan, rebuilt on the IDENTICAL ownership test, pinned edge cases, and REPRESENTABLE sub-tag now used for Japan (131 rows, `findings/census/japan/`) and Korea (135 rows, `findings/census/korea/`), so all three markets compare cleanly.
The brief is to attack the founder thesis ("indies are shut out") as hard as the data allows; where the data undercuts the thesis, that is called out plainly.

**The central v2 question - does the ~27% indie share hold under the stricter definition, or do the edge cases move it?** It holds. Re-scoring all 129 rows moved exactly three (Miffy indie->portfolio, OSAMU unclear->portfolio, Kusama unclear->indie); the indie count is unchanged at 35/129 and the overall indie share is unchanged at **27.1%**. The tightening hit the UNCLEAR bucket (7 -> 5), not the indie share.

No government/public-body-OWNED IP appears in Taiwan (every IP here is privately owned even where the *brand* is public - rows 17/32/39), so nothing is excluded from the split and the classifiable base is the full **n = 129** (unlike Korea, which excluded 2 public rows).

## 1. The ratio - overall and per year

**Overall (n = 129):**

| Class | Count | Share |
|---|---|---|
| PORTFOLIO | 89 | 69.0% |
| INDEPENDENT | 35 | 27.1% |
| UNCLEAR | 5 | 3.9% |

**Per year:**

| Year | n | PORTFOLIO | INDEPENDENT | UNCLEAR | Indie share | (v1 indie share) |
|---|---|---|---|---|---|---|
| 2024 (full year) | 37 | 27 | 9 | 1 | **24.3%** | (21.6%) |
| 2025 (full year) | 60 | 41 | 18 | 1 | **30.0%** | (31.7%) |
| 2026YTD (to 07-24) | 32 | 21 | 8 | 3 | **25.0%** | (25.0%) |

**v1 -> v2 delta:** three rows moved bucket (see `campaigns.md` "Reclassification delta"). Miffy (row 79, 2025) INDEPENDENT->PORTFOLIO under the estate rule; OSAMU GOODS (row 35, 2026YTD) UNCLEAR->PORTFOLIO under the deceased-creator/estate rule; Kusama (row 65, 2024) UNCLEAR->INDEPENDENT under the fine-artist precedent. Net indie count: **35 -> 35 (unchanged)**. The one indie removed (Miffy) and the one added (Kusama) cancel.

**Trend read:** the indie share is essentially **flat across the window - 24.3% (2024) -> 30.0% (2025) -> 25.0% (2026YTD)** - hovering around a quarter, with 2025 (the deepest slice, n=60) the high point at 30.0%.
The 2026YTD dip to 25.0% is not a genuine decline: 2026 is a partial year (7 months) and its three UNCLEAR rows (OBJECT/SOSO, Kung Fu, 乖乖) are borderline Korean-brand / brand-x-brand cases that, if excluded, lift the 2026 indie-of-classifiable share back toward the 2025 level.
The honest synthesis: **indie IP is a stable ~27% of Taiwan co-branding campaigns (27.1% overall, 30.0% in the best-sampled year 2025), neither shrinking nor a small share - roughly a quarter to a third of the market.**

This puts Taiwan in a tight band with the other two markets on the same definition: **Taiwan 27.1% / Korea 24.8% / Japan (best-sampled-year) ~26.7%.** All three land at "about a quarter indie" - the finding is consistent across East Asia, not a Taiwan quirk.

## 2. The addressable number (the market-entry read)

Of the 35 INDEPENDENT rows, the REPRESENTABLE tag splits:

| REPRESENTABLE | Count | Share of indie rows | Share of all 129 |
|---|---|---|---|
| yes | 15 | 42.9% | 11.6% |
| no | 17 | 48.6% | 13.2% |
| unclear | 3 | 8.6% | 2.3% |

**By row count, only ~43% of indie campaigns are plausibly addressable (15 of 35) - and the reason is concentration, not scarcity.** The single biggest driver of "no" is **Bugcat Capoo 貓貓蟲咖波**: 8 of the 17 REP=no rows are Capoo, whose owner 亞拉 runs licensing through his own captive studio 卡特島創意 (Carter Island). The most prominent indie IP in Taiwan is therefore effectively self-represented and NOT an open PBC target. The other structural "no" blocks are creator-owned but exclusively tied up: Kanahei (exclusive master licensor, 3 rows), mofusand (Gray Parka Service, 2 rows), 黃阿瑪/Fumeancats (own captive operation, 2 rows), plus Kusama (locked to gallery/own-studio representation) and LuLu the Piggy (ToyzeroPlus/52TOYS).

**By DISTINCT IP the addressable read is much stronger: 13 of the 21 distinct indie IPs (~62%) are REP=yes.** The addressable roster:

- **Taiwan-origin (5):** 爽爽貓 SongSongMeow (SECOND), 馬來貘 LAIMO (Cherng), 星期一的布魯斯 Monday Bruce, 露咖貓 LOOKA CAT, 臺灣印事 & 腋毛人 Yemao.
- **Foreign indie active in Taiwan (8):** noodoll (UK), ZERO PER ZERO (KR), MIND.A.DAY/CoverCat (KR), Dinotaeng (KR), KKOTKA/YOUNG FOREST (KR), matsui (JP), 俵谷哲典 Tetsunori Tawaraya (JP), unpis (JP).

**The market-entry read:** the addressable pool is real but modest and split two ways. There is a genuine domestic bench of ~5 representable Taiwan creator IPs (爽爽貓, 馬來貘, Monday Bruce, 露咖貓, plus 文博會-surfaced illustrators), several of which already land big brands (馬來貘 x CeraVe/L'Oréal; Monday Bruce x 台北101). But the single dominant Taiwan indie (Capoo) is already self-licensed and closed. The other half of the addressable pool is foreign indies (KR/JP/UK) that entered Taiwan via drink chains, department-store pop-ups and beauty - a channel PBC could plausibly play on either side (representing inbound foreign indies, or Taiwan indies outbound).

## 3. Indie prominence - breadth or a few recycled names?

**Both, with a clear concentration head and a long tail.**
The 35 indie rows span **21 distinct IPs** - real breadth - but one IP dominates the volume:

- **Bugcat Capoo 貓貓蟲咖波 - 8 rows (23% of all indie rows).** The runaway Taiwan indie: 清心福全, Sushiro, 中華郵政 (national post + themed post offices), 華南金控 (a listed financial holding co, shareholder gift), CTBC (12th-annual free outdoor ice rink), 7-ELEVEN x 故宮 (flagship 7,100-store 集點 wave), plus two mobile-game launch collabs. Capoo alone lands more big-brand co-brands than most portfolio IPs.
- **Kanahei 卡娜赫拉 - 3 rows** (7-11 集點, EasyCard, 新光三越 pop-up). Creator-owned but exclusively licensed.
- **白爛貓 Lan Lan Cat - 3 rows** (tourism festival, mobile game, 7-11 CNY wave).
- **爽爽貓 SongSongMeow, 黃阿瑪 Fumeancats, mofusand, KKOTKA - 2 rows each.**
- **13 IPs appear once** (noodoll, Kusama, LAIMO, ZERO PER ZERO, MIND.A.DAY, matsui, Dinotaeng, Monday Bruce, 露咖貓, 俵谷哲典, unpis, LuLu, 臺灣印事/腋毛人) - the long tail of one-off indie collabs.

**Do indies land big brands? Yes, repeatedly - this is the strongest counter-evidence to "indies are shut out":**
- Capoo x **華南金控** (major listed FHC) and x **中華郵政** (national postal service) - indie IP on institutional/corporate premiums.
- Capoo x **7-ELEVEN x 國立故宮博物院** - an indie IP carrying a flagship full-store (7,100+ stores) 集點 wave, the format usually reserved for Sanrio/Disney/Chiikawa.
- 馬來貘 LAIMO x **CeraVe** (L'Oréal-owned) - big global beauty x Taiwan indie.
- ZERO PER ZERO x **雪花秀 Sulwhasoo** (AmorePacific) - luxury K-beauty x indie design studio.
- mofusand x **UNIQLO**; 俵谷哲典 x **Decathlon**; Monday Bruce x **台北101 觀景台**; KKOTKA x **新光三越 / 統一時代百貨**.

**Also notable (kept OUT of the counted table but evidence of indie strength):** the LuLu the Piggy x Capoo joint product line (2026-06) is an **IP-x-IP** pairing of two Taiwan indies - a sign the indie scene is now big enough to co-brand with itself, not just ride on brands.

The picture is a healthy indie ecosystem with one breakout star (Capoo), a handful of repeat players, and a wide one-off tail - not "a few recycled names," but also not evenly distributed.

## 4. The thesis read

**Verdict: Taiwan REFINES the founder thesis - "indies are shut out" is too strong; "indies are a substantial minority, roughly a quarter, and the biggest one is self-licensed" is the accurate read.**

- **Against a hard "shut out" thesis:** indie IP is a stable **27.1%** of Taiwan co-branding, and indies demonstrably win the highest-prestige formats - a listed FHC's shareholder gift, the national post office, a 7,100-store 7-11 集點 wave, a Taipei 101 flagship exhibition, and big-beauty collabs (CeraVe, Sulwhasoo). The share held (not fell) under the stricter v2 definition. Indies are not shut out of Taiwan.
- **For a softened thesis:** portfolio IP still owns **69%** of campaigns and utterly dominates the highest-frequency channels - convenience-store 集點 (7-11/全家), drink chains, and cosmetics are overwhelmingly Sanrio / Disney / Pokemon / Chiikawa / anime-committee properties. And the addressable-by-PBC slice is thin by volume (15 of 35 indie rows, 11.6% of all campaigns), heavily because the single dominant indie (Capoo) is already captive.
- **The sharpest nuance for PBC:** the gap between "indie IP exists" (27%) and "indie IP is addressable" (~12% of campaigns, but ~62% of distinct indie IPs) is the real market-entry signal. Taiwan has indie IP and indies win big brands - but the flagship domestic indie is self-represented, so PBC's realistic bench is the ~5 open Taiwan creators plus the inbound foreign-indie channel.

**Strongest single counter-example to the founder thesis, quoted from the data:** row 51 - **7-ELEVEN Taiwan x 國立故宮博物院 featuring 貓貓蟲咖波 Bugcat Capoo**, a creator-owned indie IP carrying a flagship 全店精品集點 wave across 7,100+ stores (翠玉白菜毯, 肉形石地墊). If a solo illustrator's cat can headline the single largest retail-loyalty format in the country alongside the National Palace Museum, "indies are shut out" does not hold in Taiwan.

## 5. Method limits (stated plainly)

- **Re-run, not re-find.** v2 re-classifies and enriches the 129 v1 rows; it did NOT run a fresh discovery sweep. So v2 inherits v1's coverage exactly - it corrects classification and adds REPRESENTABLE, but does not widen the sample. The row set, sources and dates are unchanged from v1; only three buckets and the REP column changed.
- **Sample census, recall bias toward covered campaigns.** Rows come from zh-TW lifestyle/food/beauty press, convenience-store event archives, and licensing coverage - formats and IPs that get press are over-represented; quiet or regional collabs are under-counted. This biases toward big brands and famous IPs (i.e. toward portfolio), so the true indie share could be modestly HIGHER than 27% if small/local indie collabs are systematically under-covered.
- **Window.** 2024-01-01 to 2026-07-24. 2024 (n=37) and especially 2026YTD (n=32, a partial 7-month year) are thinner than 2025 (n=60); read 2025 as the most reliable single-year slice (30.0% indie).
- **Format skew.** The sample over-indexes convenience-store 集點, handshake-drink chains, and cosmetics (all heavily portfolio) and under-indexes some indie-friendly channels (indie pop-ups, stationery, gaming) that were only partially swept. This too likely understates indie share.
- **Where ownership was hard to establish (the UNCLEAR rate is itself a finding).** UNCLEAR fell from 7 to 5 in v2 (OSAMU and Kusama resolved). The remaining 5 are: three borderline-scope brand-x-brand / film-licence rows (乖乖, 功夫, and the Korean OBJECT/SOSO), plus two Korean character brands (Bunni Konbiny, Brunch Brother) whose ownership could not be pinned under queries run. At 3.9%, the unclear rate is low - most calls were confident.
- **REPRESENTABLE is a judgement call, not a legal finding.** REP=yes/no reflects public signals about whether an IP is captive (own studio, exclusive licensor) or open; it is directional market-entry guidance, not confirmation that any creator is contractually free. The Capoo=no call in particular (which drives most of the "no" volume) rests on Carter Island being a functioning captive licensing studio - a defensible read, but PBC should confirm case by case. The single-source rows (flagged in Notes) and the reliance on zh-TW secondary press for ownership are the main confidence limits.
