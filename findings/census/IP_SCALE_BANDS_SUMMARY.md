# IP scale bands - ten-market summary

Consolidates the ten `findings/census/<market>/ip_scale_bands.md` files produced by the ip_scale_band enrichment pass.
Every INDEPENDENT row in every market census now carries a follower-scale band or an explicit `unknown`, with an evidence basis and a source per row.

Band vocabulary is exactly `lt_10k` / `10k_50k` / `50k_200k` / `200k_1m` / `gt_1m` / `unknown`, matching the /start intake's `follower_band` codes character-for-character.
Band reads the IP's PRIMARY single channel at campaign time, never a cross-platform total.
No `campaigns.md` was modified by this pass.

**The denominator is 235 independent rows, not the ~190 the task brief assumed.**
That correction was made in the first iteration by parsing all ten census tables rather than trusting the estimate, and it holds: 131 REP=yes, 58 REP=unclear, 46 REP=no.

## 1. Coverage per market

| Market | Independent rows | Banded at-campaign | Banded current-proxy | Unknown | Banded total | Banded % |
|---|---|---|---|---|---|---|
| vietnam | 4 | 1 | 2 | 1 | 3 | 75.0% |
| philippines | 7 | 2 | 5 | 0 | 7 | 100% |
| singapore | 7 | 0 | 7 | 0 | 7 | 100% |
| hongkong | 13 | 1 | 12 | 0 | 13 | 100% |
| thailand | 17 | 1 | 14 | 2 | 15 | 88.2% |
| indonesia | 14 | 1 | 12 | 1 | 13 | 92.9% |
| malaysia | 31 | 6 | 23 | 2 | 29 | 93.5% |
| taiwan-v2 | 38 | 5 | 32 | 1 | 37 | 97.4% |
| japan | 51 | 2 | 43 | 6 | 45 | 88.2% |
| korea | 53 | 4 | 45 | 4 | 49 | 92.5% |
| **All ten** | **235** | **23** | **195** | **17** | **218** | **92.8%** |

By representability tier, which is the tier order the brief asked the pass to prioritise:

| REP | Rows | at-campaign | current-proxy | unknown | Banded |
|---|---|---|---|---|---|
| yes | 131 | 15 | 109 | 7 | 124 |
| unclear | 58 | 5 | 46 | 7 | 51 |
| no | 46 | 3 | 40 | 3 | 43 |

The priority instruction was followed in effect rather than by literal tier-first sweeping: markets were completed whole, and because REP=yes is 56% of every market's independent rows, the REP=yes set finished at 94.7% banded, the highest of the three tiers.

## 2. Band distribution

**Per market, banded rows only.**

| Market | `lt_10k` | `10k_50k` | `50k_200k` | `200k_1m` | `gt_1m` | Banded |
|---|---|---|---|---|---|---|
| vietnam | 2 | 0 | 0 | 0 | 1 | 3 |
| philippines | 1 | 4 | 2 | 0 | 0 | 7 |
| singapore | 2 | 3 | 0 | 2 | 0 | 7 |
| hongkong | 0 | 4 | 0 | 9 | 0 | 13 |
| thailand | 2 | 8 | 4 | 1 | 0 | 15 |
| indonesia | 0 | 4 | 2 | 7 | 0 | 13 |
| malaysia | 4 | 13 | 5 | 6 | 1 | 29 |
| taiwan-v2 | 0 | 6 | 10 | 11 | 10 | 37 |
| japan | 1 | 5 | 13 | 22 | 4 | 45 |
| korea | 4 | 6 | 8 | 26 | 5 | 49 |
| **Pooled** | **16** | **53** | **44** | **84** | **21** | **218** |

**The pooled row is row-weighted, and that is a real distortion, not a rounding artefact.**
Three things bias it and all three must travel with the number:

1. **Census depth differs by an order of magnitude.** Korea contributes 53 rows and Vietnam 4, so the pooled shape is mostly Korea, Japan and Taiwan - the three CJK markets, which also happen to be the markets with the largest character IPs.
2. **Repeat IPs are not deduplicated.** 235 rows resolve to roughly 170 distinct IPs before cross-market dedup, and the concentration is extreme in places: 망그러진곰 is 8 of Korea's 53 rows (all `200k_1m`), Bugcat Capoo is 8 of Taiwan's 38 (8 of its 10 `gt_1m` rows), LuLu the Piggy is 6 of Hong Kong's 13. Japan is the exception at 44 distinct IPs from 51 rows, so its row-level and IP-level shapes nearly coincide. **At IP level the `gt_1m` column shrinks hardest**, because the biggest IPs are precisely the ones licensed repeatedly.
3. **At least five IPs recur across markets** and would be double-counted in any IP-level pool built naively from these files: mofusand (singapore, taiwan-v2, japan), Dinotaeng (taiwan-v2, korea), Opanchu Usagi (japan, korea), Esther Bunny (japan, korea), Kanahei (taiwan-v2, japan).

Per-market IP-level distributions exist inside the taiwan-v2, japan and korea files, which are the three markets where the row/IP gap matters most.
A cross-market IP-level pool is deliberately not computed here: it needs an IP identity key that the census tables do not carry, and inventing one by string matching would produce silent merges across markets.

**What the distribution says, read cautiously.** The modal band is `200k_1m` (84 of 218, 38.5%), and `50k_200k` plus `200k_1m` together are 58.7% of all banded rows. The tails are thin: 16 rows below 10K and 21 above 1M. That shape is consistent across the three deepest markets and inverts in the Southeast Asian ones - Thailand, Malaysia and the Philippines cluster in `10k_50k`, which is where 53 of the pass's rows sit.

## 3. Cross-tab PREVIEW - band x brand identity

**PREVIEW ONLY. The real derivation happens at import.**
These tables are computed from the band files joined to the census `Brand` and `Format` columns by row number, with brand categories assigned by keyword over brand plus format.
The category assignment is a convenience heuristic, not a curated taxonomy, and the 36-row "other" bucket is where it breaks down.
Nothing downstream should treat these counts as the derivation.

**Band x brand category, banded rows only (n=218):**

| Brand category | `lt_10k` | `10k_50k` | `50k_200k` | `200k_1m` | `gt_1m` | Total |
|---|---|---|---|---|---|---|
| fashion / apparel | 2 | 15 | 8 | 22 | 2 | 49 |
| retail / pop-up / venue | 6 | 10 | 8 | 17 | 3 | 44 |
| other (uncategorised) | 0 | 9 | 9 | 8 | 10 | 36 |
| cafe / drinks | 1 | 5 | 6 | 13 | 2 | 27 |
| beauty | 2 | 5 | 6 | 8 | 0 | 21 |
| finance / tech / game | 3 | 4 | 3 | 4 | 2 | 16 |
| food | 1 | 2 | 2 | 4 | 0 | 9 |
| convenience store | 1 | 1 | 1 | 4 | 2 | 9 |
| sports club | 0 | 2 | 1 | 4 | 0 | 7 |

**Brands that ran more than one banded independent IP, and the bands they ran at.**
Only 13 brands in the entire pass did so, which is the first thing the cross-tab reveals: brand-level band comparison has almost no within-brand variance to work with yet.

| Market | Brand | Banded rows | Bands run | Band spread |
|---|---|---|---|---|
| malaysia | Rip Curl Malaysia | 4 | `10k_50k` x3, `50k_200k` | 2 tiers |
| taiwan-v2 | 7-ELEVEN Taiwan | 3 | `200k_1m` x2, `50k_200k` | 2 tiers |
| japan | Village Vanguard | 3 | `50k_200k` x2, `10k_50k` | 2 tiers |
| korea | LG 트윈스 (LG Twins, KBO) | 3 | `gt_1m`, `200k_1m`, `50k_200k` | 3 tiers |
| malaysia | Secret Recipe | 2 | `200k_1m`, `10k_50k` | 3 tiers |
| malaysia | Touch 'n Go | 2 | `50k_200k`, `10k_50k` | 2 tiers |
| taiwan-v2 | 清心福全 | 2 | `gt_1m`, `50k_200k` | 3 tiers |
| japan | FamilyMart | 2 | `200k_1m`, `10k_50k` | 3 tiers |
| japan | バンダイ ガシャポン | 2 | `gt_1m`, `200k_1m` | 2 tiers |
| japan | CASETiFY | 2 | `gt_1m`, `50k_200k` | 3 tiers |
| japan | Lawson | 2 | `200k_1m` x2 | 1 tier |
| korea | CU | 2 | `200k_1m` x2 | 1 tier |
| korea | 스파오 (SPAO) | 2 | `200k_1m` x2 | 1 tier |

**The strongest signal in the pass is band x REPRESENTABLE, not band x brand.**

| REP | `lt_10k` | `10k_50k` | `50k_200k` | `200k_1m` | `gt_1m` | Banded |
|---|---|---|---|---|---|---|
| yes | 8 | 41 | 32 | 42 | 1 | 124 |
| unclear | 8 | 11 | 8 | 20 | 4 | 51 |
| no | 0 | 1 | 4 | 22 | 16 | 43 |

65.3% of REP=yes rows band at `50k_200k` or below, and exactly one REP=yes row in ten markets bands `gt_1m`.
88.4% of REP=no rows band at `200k_1m` or above.
That is a two-to-three tier separation, and it is the one finding in this summary that is robust to the proxy problem described below, because proxy error moves a band by one tier at most and never by two.
Read plainly: **the independent IPs that are still representable are systematically an order of magnitude smaller than the independent IPs that are already locked up.**

## 4. Honesty

### 4.1 The current-proxy share is the headline caveat

**195 of 235 rows (83.0%) are `current-proxy`, and 195 of 218 banded rows (89.4%) are.**
Only 23 rows (9.8%) carry an at-campaign band.
A `current-proxy` band means the count was read on 2026-07-30 and the campaign happened earlier, so the band is the IP's scale *now*, presented as the best available stand-in for its scale then.

The gaps are not small. Across the ten files they run from **1 month to 31 months**, and the pass's convention is that proxy gap, not follower count, is what decides whether a near-edge band is trustworthy.
The named worst cases, all recorded in their market files' watch-lists:
- korea rows 21/87/126/127 (무직타이거): 203K is **1.5% over the `200k_1m` floor** at gaps of 7-20 months. Four rows, and `50k_200k` is genuinely live for all of them.
- korea row 2 (망그러진곰): **31-month gap** on an IP that grew across exactly that window.
- japan row 90: 29.5-month gap, 20% over the `200k_1m` floor, on an account opened in 2021.
- taiwan-v2 rows 18/53/68 (Kanahei) and row 107 (Dinotaeng, 30-month gap).
- korea row 136 (에스더버니): 26-month gap on a 30K account, so `lt_10k` is live.
- malaysia rows 9/10 (Bichi Mao 995K) and hongkong row 73 (CJ Hendry 996K), both fractions of a percent under `gt_1m` with the unrounded count unobtainable.

Roughly 15 rows across the pass sit within about 12% of a band edge.
Every one is flagged in its market file rather than silently rounded, and the drift rule applied throughout is that a count read *after* the campaign overstates the at-campaign figure, so the lower band is the safe call where a rounded figure straddles an edge.

### 4.2 Why at-campaign evidence is so scarce

This is structural in the region, not a research shortfall.
A whole-corpus grep of every census source URL in all ten markets for follower words returned **6 usable hits in roughly 270 sources**: SHEWSHEEP (thailand, an animation-trade conference feature), Bichi Mao (malaysia, and a trap - a cross-platform total), matsui and mofusand (taiwan-v2, both channel-named), 寺田てら (japan), 빵빵이 and 비야 (korea, both channel-named).
Five markets returned zero hits.
Brand PR simply does not state a licensed IP's following.

What did produce at-campaign bands, in descending order of yield:
1. **Bracketing** (korea rows 93, 155): a dated figure before the campaign plus a live figure after it, both inside the same band. Drift cannot move a band it is already bracketed inside. This is the strongest construction the pass found and it is available whenever any dated figure exists.
2. **At-campaign by proximity** (philippines, malaysia): a current count read while the campaign is live or just ended. Malaysia used it at 11, 7 and 2 days; malaysia row 123 is the pure case, read mid-window.
3. **Channel-named press floors** ("over 100,000", "近10萬"): usable only when both drift directions land in the same band, which is the same test the Indonesian influencer listicles are held to.
4. **Dated platform milestones** (japan row 95, via cited ja.wikipedia YouTube milestones bracketing the campaign window).

### 4.3 Which markets were hardest, and why

- **Japan (6 unknowns, the most).** Two causes: multi-creator rosters too large to evidence (row 77 at 1-of-12 creators, row 19 at 2-of-18, both refused under the roster rule rather than banded off whoever happened to be findable), and Japanese illustrator handles bearing no relation to the creator's name (28 name-guesses across 19 IPs produced 2 hits).
- **Korea (4 unknowns) was cheap to research but produced the pass's only *measurement* failure.** Row 152's handle is confirmed (`@luv_nan2`) and the count is still unobtainable: the profile returns HTTP 200 with no `og:description` to any crawler UA while 30 other Korean accounts in the same file return counts normally. Every prior unknown in the pass was an identification failure; this one is not, which means the Instagram route is not universal.
- **Thailand and Vietnam were hardest per row.** Thai trade press links no creator accounts at all, and both Thai unknowns are inbound IPs whose real audience sits on Weibo and Xiaohongshu, which nothing in this pass can read.
- **Fine artists and published works are a malformed question, not a hard one.** taiwan-v2 row 65 (Yayoi Kusama) and korea row 117 (the 2002 manhwa 궁) have no channel concept: all candidate accounts are fan pages, institutions or unrelated people. Three of the pass's 17 unknowns are this type and no amount of further search would resolve them.
- **Platforms that stayed closed:** Facebook profile counts under every user-agent tried, which leaves live exposure on taiwan-v2's Capoo, LAIMO, 白爛貓 and Mr. STRIKE and on malaysia's Shiba Says; Weibo and Xiaohongshu entirely; Naver blog/cafe, which is the plausible primary channel for Korea's webtoon-origin IPs; and KakaoTalk emoticon popularity, which has no follower analogue at all and is the origin format for six Korean IPs.
- **Two owed reworks are still owed and the summary should not be read as if they were done.** TikTok turned out to be curl-verifiable after six market files were written assuming otherwise (risk confined to animation and comic IPs, since illustrators run an order of magnitude smaller on TikTok), and X turned out to be curl-verifiable via the fxtwitter API after eight files were written stating it was not. One X-exposed case has been retired (Kanahei, band unchanged) and Korea was checked end-to-end on both platforms, but the other eight files' non-illustrator rows have not been swept.

### 4.4 Is the banded coverage sufficient to support the comparable-bands feature honestly?

**Qualified yes, with two hard limits that must be enforced in the render rather than in a footnote.**

The case for yes:
- 218 of 235 independent rows carry a band, 92.8%, and the REP=yes core - the tier the feature actually serves - is 124 of 131, 94.7%. The feature's original blocker was that only ~5 rows recorded scale at all. That blocker is gone.
- The band tiers are wide (each spans roughly a 4-5x range), and most bands sit mid-tier rather than at an edge, so a one-tier proxy error is the exception rather than the expected case.
- Every band carries its channel, its source URL, its retrieval or publication date, its basis flag, and the rejected candidate handles. A reader can audit any single row without re-doing the research, and 17 rows honestly render nothing.
- The headline comparison the feature exists to make - that representable independent IP sits two to three tiers below locked-up independent IP - survives the proxy problem, because proxy error is a one-tier phenomenon and that separation is two to three tiers.

The two limits:
1. **No claim may rest on a single row, and no claim may turn on band adjacency.** With 89% of bands as proxies and ~15 rows within 12% of an edge, "this brand ran a `200k_1m` IP" is a defensible aggregate statement and an indefensible per-row one. The four 무직타이거 rows are the concrete case: they are 1.5% over a band floor at gaps up to 20 months, so a cross-tab cell that depends on them is not real.
2. **Do not present pooled cross-market percentages as market-neutral.** They are row-weighted, so they are mostly Korea, Japan and Taiwan, and they double-count repeat IPs (8 of Korea's rows are one IP, 8 of Taiwan's are another). Market-level breakdowns are honest; a single pooled pie chart is not.

**What is not sufficient, stated plainly:** brand-level band comparison. Only 13 brands in the entire pass ran more than one banded independent IP, and 8 of those 13 ran exactly two. There is not enough within-brand variance to answer "which brand scales ran IPs at each band" at the level of an individual brand, and the honest version of that question right now is asked of brand *categories*, where the smallest cell is 7 rows. The band x brand cross-tab in section 3 is a preview because it is genuinely thin, not merely because the derivation moves at import.

**If one thing is done next**, it is not more rows: it is converting proxies to at-campaign bands by the bracketing method in 4.2 for the ~15 near-edge rows named in 4.1, which is where the coverage is weakest and where a downstream conclusion is most likely to be wrong.

## Files

| Market | File | Rows |
|---|---|---|
| vietnam | `findings/census/vietnam/ip_scale_bands.md` | 4 |
| philippines | `findings/census/philippines/ip_scale_bands.md` | 7 |
| singapore | `findings/census/singapore/ip_scale_bands.md` | 7 |
| hongkong | `findings/census/hongkong/ip_scale_bands.md` | 13 |
| thailand | `findings/census/thailand/ip_scale_bands.md` | 17 |
| indonesia | `findings/census/indonesia/ip_scale_bands.md` | 14 |
| malaysia | `findings/census/malaysia/ip_scale_bands.md` | 31 |
| taiwan-v2 | `findings/census/taiwan-v2/ip_scale_bands.md` | 38 |
| japan | `findings/census/japan/ip_scale_bands.md` | 51 |
| korea | `findings/census/korea/ip_scale_bands.md` | 53 |

Each file additionally carries: a coverage table, a row-level band distribution, its own watch-list of near-edge and weak-identification rows, the verification method and user-agents used, and a `## Multi-creator detail` table where the market has multi-creator rows (philippines, hongkong, indonesia, malaysia, taiwan-v2, japan, korea).
Indonesia's MIXED row 2 is included on its Si Juki side as the brief requires.
