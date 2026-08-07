# Taiwan x `lt_10k` independent collaborations - verified rows

Task: `tasks/tw-lt10k-independent.md`.
Goal: documented brand collaborations in Taiwan, 2023-2026, where the partner IP is an INDEPENDENT (or MIXED) character that stood at or under 10,000 followers.
The ten-market census (`findings/census/taiwan-v2/ip_scale_bands.md`) holds **zero** `lt_10k` Taiwan rows at whole-row level - the single `lt_10k` reading in that file is a per-creator sub-band inside two-creator row 76 (臺灣印事).
This file is the dedicated hunt for the missing cell.

**Status: in progress. Build 1 of the run - 2 verified rows of a 25-row stop condition. Retrieval date for everything below: 2026-08-07.**

---

## Why the census found none, and what that implies for the search

The census was built from press coverage (UDN, ETtoday, LTN, WalkerLand, cava.tw and similar roundups).
Press coverage is itself a scale filter: a Taiwanese outlet writes up a 聯名 when the IP is already recognisable, so the press-indexed population starts at roughly `10k_50k` and runs up.
A sub-10k IP that gets a real brand deal leaves its trace on **the brand's own commerce surface**, not in the press.

That reframes the search. The productive index is not a news archive - it is a **brand-run licensing directory**: a Taiwanese consumer brand that publishes one page per IP partner and keeps every partner page live.
Build 1 found and swept one such directory in full (see Vein A).

---

## Veins tested

| Vein | What it is | Verdict |
|---|---|---|
| **A. DEVILCASE 惡魔防摔殼 `/crossover/<id>`** | Taiwanese phone-case brand; one live page per IP partner, sequential integer ids | **WORKS - primary vein.** 236 partner pages recovered, overwhelmingly Taiwanese indie illustrators. Full sweep of ids 1-360 |
| **B. 慢慢挑 PianoPianoPick** | Taiwanese drinkware brand licensing illustrator characters onto cups/bags (`聯名款` in every product title) | Enumerable (~30 illustrators) but **scale-filtered upward**: every partner resolved so far sits 24K-941K (灰塵魚 24K, Littdlework 24K, 包大山 32K, weiweiboy 43K, 屎蛋唐尼 82K, 馬卡龍腳趾 98K, 咻咻熊 111K, KINGJUN 113K, 爽爽貓 169K, 地呱球 205K, 馬來貘 941K). Kept as a comparator, not a source of `lt_10k` rows |
| **C. LINE STORE sponsored-sticker showcase** | `store.line.me/stickershop/showcase/sponsor|event|free/zh-Hant` | **DEAD** - all three paths return 404. Sponsored stickers are not exposed on the web storefront |
| **D. 文創股長 STARup hub** (Gamania's ~100-creator illustrator incubator, `illustrators.gamania.com`) | Would be an ideal directory - a brand-collab arm over a roster of small creators | **UNREACHABLE from here** - `illustrators.gamania.com` does not resolve (DNS `ENOTFOUND`) on either curl or WebFetch. `blog.shopping.gamania.com` resolves but serves a React shell. Owed to a later build |

---

## Method

### 1. Enumerating the partner directory (Vein A)

`https://devilcase.com.tw/crossover/<n>` for n = 1..360, swept directly.
A live partner page is identified by its `<title>` matching `<IP name> X 惡魔防摔殼｜...`; 236 of 360 ids resolve to a partner. `robots.txt` is fully permissive.
The page carries the IP's own bio in `<meta name="description">` but **no date and no creator social link**, so both year and follower count have to come from outside the page.

### 2. Dating a collaboration (no date on the page)

Wayback CDX over the whole path:

```
http://web.archive.org/cdx/search/cdx?url=devilcase.com.tw/crossover/*&output=text&fl=original,timestamp&collapse=urlkey&filter=statuscode:200
```

273 numeric ids carry a capture. **First-capture is an upper bound on launch, not the launch date.** But because the ids are assigned sequentially and the archive crawls this directory in whole-block sweeps, the ids can be *bracketed* between two consecutive sweeps, which is much tighter than a bare upper bound:

| Sweep | New ids first captured |
|---|---|
| 2025-12-05 | 262-267 |
| 2026-01-19 | 269-273 |
| 2026-02-12 | 275-285 |
| 2026-03-09 | 268-288 |
| 2026-04-14 | 289-302 |
| 2026-05-09 | 303-309 |
| (none yet) | 310-326 |

So id 308 launched **after 2026-04-14 and on or before 2026-05-09**, and ids 310-326 launched **after 2026-05-09** (no snapshot exists yet, and id 309 was swept on that date).

The window floor is equally firm: the December-2023 bulk crawl swept the directory in one pass and its **highest id is 135**. Every id at 136 or above was therefore created after 2023-12-04, which puts the whole of the 136-326 range inside the task's 2023-2026 window with no further work.

Three dating bases are used and always stated per row:

- `wayback-bracket` - bounded between two consecutive sweeps. The strong case.
- `wayback-first-capture` - earliest 200 snapshot only, where the preceding sweep does not bracket cleanly (the crawl is patchy below id ~250: id 142 was first captured 2024-11 while id 149 was captured 2024-08, so ids in that range can be older than their first capture).
- `id-sequence` - ids above 309, dated by monotonicity against the 2026-05-09 sweep rather than by a snapshot of their own.

### 3. Resolving the IP's channel and follower count

No handle on the partner page, so: DuckDuckGo HTML endpoint (`https://html.duckduckgo.com/html/`, POST `q`) queried as `<IP name> instagram 插畫`, then every `(@handle)` in a result title and every `instagram.com/<handle>` in the result body is taken as a candidate, and each candidate is fetched:

```
curl -H 'User-Agent: Mozilla/5.0 (compatible; Googlebot/2.1; ...)' https://www.instagram.com/<handle>/
```

Instagram serves `og:description` = `"<N> Followers, <N> Following, <N> Posts - See Instagram photos and videos from <display name> (@<handle>)"` to that UA. Both halves matter: the count **and** the display name.

### 4. The handle-squat trap (mandatory guard)

Guessing a handle from a romanised brand name produces a plausible-looking tiny account that is **not the IP**, and every one of those would fabricate an `lt_10k` row. Proven on this run:

| Guessed handle | What it actually is | Real IP channel |
|---|---|---|
| `@sweetpotatoball` (118) | untitled account | 地呱球 is `@sweet.potato.ball`, **205K** |
| `@tonystan` (96, "Tony Assogba"), `@tonystan_` (199, "Ufoh Anthony") | unrelated people | 屎蛋唐尼 is `@tonystan8787`, **82K** |
| `@baozi` (93, "Rita Bao") | unrelated person | 包大山 is `@baodashan`, **32K** |
| `@littleyellowroom` (25) | untitled account | 小黃間 - unresolved |
| `@digua_ball` (61, "梅子地瓜球") | unrelated account | - |

**Rule enforced on every row in this file: the `og:description` display name must carry the IP's own name.** A count from an account whose display name does not name the IP is discarded, not recorded.

### 4b. Two further traps this vein sets, both of which manufacture false `lt_10k` rows

**The regional-account trap.** An IP that has entered Taiwan through a local distributor often runs a Taiwan-only Instagram account that is an order of magnitude smaller than its home channel. 胡子碰碰 OHIGE no PON (crossover 325) reads **7,769** on `@ohigenopon_tw` and **1,195 / 2,904 / 1,649** on its HK / TH / English accounts - but the creator's own account `@ohigenopon` reads **53K**. Banding off the local account would have produced an `lt_10k` row for an IP that is nowhere near `lt_10k`. Same shape as the LuLu the Piggy `@luluthepiggy_hk` case already recorded in `findings/census/hongkong/ip_scale_bands.md`. **Every candidate is checked for a bare, un-suffixed handle before the band is accepted.**

**The VTuber trap.** 29 of the 142 in-scope, in-window partner pages are VTubers or VTuber groups, identifiable from the partner-page bio (直播 / Twitch / YouTube / 頻道 / 實況). A VTuber's primary channel is YouTube or Twitch, never Instagram, so an Instagram-only read understates them by tiers and is not a band at all under the census's primary-channel rule. 塔芭絲可 (crossover 143) reads 8,904 on Instagram but is a MIROLIVE first-generation talent whose streaming channels were not measured. **VTuber rows are held out of this file rather than banded off Instagram** - see Rejected candidates.

### 5. Follower-count basis

Counts are read live and are therefore `current-proxy` against a campaign that launched earlier, exactly as in `findings/census/taiwan-v2/ip_scale_bands.md`.
Social accounts grow, so a **current** count under 10,000 is a *conservative* reading for a past campaign: the at-campaign figure was almost certainly lower still. That is the safe drift direction for this cell, and it is the reason a current-proxy count is admissible here.
Every row states its retrieval date.

---

## Rows

**Build 1: 2 verified rows.** Both are proposals for human accept; nothing here has been written to any database.

| # | brand_name | ip_name | market | year | year basis | source_ref | follower_band | count seen | representable | ip_class | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | DEVILCASE 惡魔防摔殼 | 茶包先生 Mr. Teabag | TW | 2026 | `wayback-bracket` - crossover id 308, first captured 2026-05-09, and the preceding directory sweep on 2026-04-14 captured only up to id 302, so the partnership went live between those two dates | https://devilcase.com.tw/crossover/308 (HTTP 200, 2026-08-07) | `lt_10k` | **8,288** Instagram followers, `@mr.teabag_`, read 2026-08-07 | yes | INDEPENDENT | Solo Taiwanese illustrator brand - three characters (茶包, 栽栽, 捲捲) described on the partner page as unrelated brothers, no studio or parent named anywhere. Handle name-match is exact: `og:description` display name reads `茶包先生｜文博會S057｜插畫 · 旅遊 ᴾᴸᴼᴳ`, i.e. the account states its own 文博會 (Creative Expo Taiwan) booth number **S057** - the creator is a CET exhibitor, which is the same population as `findings/expo/cet2026-*`. `current-proxy` count against a campaign roughly 3 months older, so the at-campaign figure was lower, not higher |
| 2 | DEVILCASE 惡魔防摔殼 | Wasabi Bear 芥末熊 / 와사비베어 | TW | 2026 | `id-sequence` - crossover id 321 has no Wayback snapshot at all, while id 309 was swept 2026-05-09; ids are sequential, so 321 went live after 2026-05-09 | https://devilcase.com.tw/crossover/321 (HTTP 200, 2026-08-07) | `lt_10k` | **4,252** on `@wasabibear_tw` (芥末熊 Wasabi Bear), the largest of three evidenced channels - Korean home account `@wasabibear.official` (와사비베어) reads **3,882** and `@wasabibear_japan` (ワサビベア【日本公式】) reads **3,973**. All read 2026-08-07 | unclear | INDEPENDENT | Korean creator-owned: the character is a handmade doll made by Sugar Rain (Kim Dan-bi) in September 2021, per the Korean-language NamuWiki entry - no conglomerate parent found. **Band is robust against the regional-account trap for once**: unusually, all three country accounts sit under 10K and the *home* account is the smallest of the three, so no choice of primary channel leaves `lt_10k`. `@wasabibear` (56) and `@wasabi.bear` (100) are squats and were rejected. REP=`unclear` because the character is retailed through LINE FRIENDS SQUARE, so an exclusive licensor may already sit in the chain - ownership is independent, addressability is not established |

**Read on both rows:** these are foreign-and-domestic micro-IP getting a real Taiwanese consumer-brand product line, on a brand that runs 236 such partnerships. That is the shape of the missing census cell, not an exception to it.

---

## Rejected candidates

**Build 1 rejected: 11 named, plus the population-level rejections below.**

| Candidate | Where found | Reason |
|---|---|---|
| 胡子碰碰 OHIGE no PON (crossover 325) | Vein A | **Regional-account trap.** TW account 7,769 but creator account `@ohigenopon` = 53K. Band is `50k_200k`, not `lt_10k` |
| 塔芭絲可 Tabasuko (crossover 143) | Vein A | **VTuber.** Instagram 8,904 but primary channel is streaming, unmeasured. Also MIROLIVE first-generation talent, so IP class is likely not INDEPENDENT either. Held out, not banded |
| 霓NEO(n) (crossover 149) | Vein A | **VTuber group** under 子午計畫 Meridian Project. Same reason; the 1,221-follower `@neoneon_n` ("霓羊 Neon") is in any case not a confirmed name-match |
| 蝦米浣糕 RACCAKE (crossover 322) | Vein A | Too large - `@raccake222` = **50K**. (Worth noting for a later build: it also has a second, non-DEVILCASE Taiwanese brand tie-up, 蝦米浣糕 x ViewFinder apparel, but viewfinder.com.tw returns 403 to curl) |
| 安怎？ Ann Nua (crossover 324) | Vein A | Too large - `@ann_nua_handmade` = **20K** |
| 好吧星期一 Ok Mondays (crossover 312) | Vein A | Too large - `@okmondays` = **16K** |
| 日頭 LITTOP (crossover 323) | Vein A | Too large - `@littop_design` = **46K**. The sub-10K hits the search returned (`@lichtope` 4,036, `@little_tyo` 8,063) fail the name-match rule |
| 稻乙緹 (crossover 139) | Vein A | Too large - `@iitifox_` = **30K** (name-matched). `@draw_taigachan` (118) is unrelated |
| 懶貓子 Rumi (crossover 138) | Vein A | Too large - `@lanmewko` = **38K** |
| 玩什麼鬼啦 (crossover 142) | Vein A | Too large - `@playwhat_the` = **48K**. `@taipeideer1101` (2,850) fails the name-match rule |
| 慢慢挑 x 地呱球 / 屎蛋唐尼 / 灰塵魚 / Littdlework / 包大山 / weiweiboy / 馬卡龍腳趾 / 咻咻熊 / KINGJUN / 爽爽貓 / 馬來貘 (11 collaborations) | Vein B | All above 10K - the range is 24K to 941K. Vein B is scale-filtered upward and yields no `lt_10k` rows |

**Population-level rejection.** Of the 236 partner pages: **41** are licensed properties or otherwise out of scope (Sanrio's eight characters, Moomin, Garfield, Rilakkuma, Gundam, Monster Hunter, HUNTERxHUNTER, 神魔之塔, 傳說對決, Hatsune Miku, 貓福珊迪, 吉伊卡哇, 卡娜赫拉, 白爛貓, ㄇㄚˊ幾兔, 好想兔, a government mascot, a temple, a car-review channel and similar) and were excluded before any follower work; and **70** sit at ids 1-135, dated only as "on or before 2023-12-04", so they fall outside the task's 2023-2026 window. That leaves **142 in-scope, in-window partner pages** as the working population - the denominator every completeness claim in this file is against.

---

## Source verification log

Every URL below was curl-verified on **2026-08-07**.

| URL | Status | Role |
|---|---|---|
| https://devilcase.com.tw/crossover | 200 | Vein A directory index |
| https://devilcase.com.tw/crossover/308 | 200 | Row 1 `source_ref` |
| https://devilcase.com.tw/crossover/321 | 200 | Row 2 `source_ref` |
| https://www.instagram.com/mr.teabag_/ | 200 | Row 1 follower count |
| https://www.instagram.com/wasabibear_tw/ | 200 | Row 2 follower count (largest evidenced channel) |
| https://www.instagram.com/wasabibear.official/ | 200 | Row 2 home-channel corroboration |
| https://www.instagram.com/wasabibear_japan/ | 200 | Row 2 third-channel corroboration |
| `web.archive.org/cdx/.../crossover/308` | `20260509143058 200` | Row 1 dating |
| `web.archive.org/cdx/.../crossover/309` | `20260509133320 200` | Row 2 dating (the sweep that 321 post-dates) |
| `web.archive.org/cdx/.../crossover/321` | empty | Row 2 dating (confirms no snapshot exists) |
| https://www.pianopianopick.com/categories/illustrators | 200 | Vein B index |
| https://store.line.me/stickershop/showcase/sponsor/zh-Hant | 404 | Vein C, dead |
| https://illustrators.gamania.com/clients/ | DNS `ENOTFOUND` | Vein D, unreachable |

---

## What build 1 leaves owed

1. **The resolution sweep reached 42 of the 142 in-scope, in-window partner pages, and only 7 of those 42 returned any candidate handle from the automated search** (four more - 茶包先生, 蝦米浣糕, 安怎？, 好吧星期一 - were resolved by hand). So roughly **107 of 142 partner pages are still unbanded**, and each one is a live `lt_10k` candidate. The blocker is search access, not the vein: DuckDuckGo's HTML endpoint answers about ten queries then serves empty result sets permanently, and Brave Search answers reliably at one worker but drops to roughly a 20% hit rate at three concurrent workers. The next build should run **one** worker with a longer delay, and must re-attempt the ids that logged an empty candidate list rather than treating them as resolved.
2. **The 29 VTuber partners need a YouTube/Twitch read**, not an Instagram one, before they can be accepted or rejected. `https://www.youtube.com/@<handle>` yields a subscriber count from the channel-header accessibility label, per the method already used for Fumeancats in `findings/census/taiwan-v2/ip_scale_bands.md`.
3. **Brand diversity.** Both build-1 rows carry the same brand. The rows are real, but a cell that rests on one licensee is thin for a prospect page. Vein D (文創股長 STARup hub) is the best untried source of a *second* brand-side directory, and 蝦米浣糕 x ViewFinder is a live lead into apparel.
4. **Ids 1-135 are undated.** If the 2023 slice matters, they need a second dating source - DEVILCASE's own Facebook/Instagram launch posts are the obvious candidate.
