# Taiwan x `lt_10k` independent collaborations - verified rows

Task: `tasks/tw-lt10k-independent.md`.
Goal: documented brand collaborations in Taiwan, 2023-2026, where the partner IP is an INDEPENDENT (or MIXED) character that stood at or under 10,000 followers.
The ten-market census (`findings/census/taiwan-v2/ip_scale_bands.md`) holds **zero** `lt_10k` Taiwan rows at whole-row level - the single `lt_10k` reading in that file is a per-creator sub-band inside two-creator row 76 (臺灣印事).
This file is the dedicated hunt for the missing cell.

**Status: in progress.
Build 2 of the run - 10 verified rows of a 25-row stop condition.
Retrieval date for everything below: 2026-08-07.**

---

## Why the census found none, and what that implies for the search

The census was built from press coverage (UDN, ETtoday, LTN, WalkerLand, cava.tw and similar roundups).
Press coverage is itself a scale filter: a Taiwanese outlet writes up a 聯名 when the IP is already recognisable, so the press-indexed population starts at roughly `10k_50k` and runs up.
A sub-10k IP that gets a real brand deal leaves its trace on **the brand's own commerce surface**, not in the press.

That reframes the search.
The productive index is not a news archive - it is a **brand-run licensing directory**: a Taiwanese consumer brand that publishes one page per IP partner and keeps every partner page live.
Build 1 found and swept one such directory in full (Vein A, DEVILCASE).
Build 2 found a second, better-instrumented one (Vein E, RHINOSHIELD Design Studio) that publishes each creator's Instagram handle and launch date itself - which is what broke build 1's real blocker, handle discovery.

---

## Veins tested

| Vein | What it is | Verdict |
|---|---|---|
| **A. DEVILCASE 惡魔防摔殼 `/crossover/<id>`** | Taiwanese phone-case brand; one live page per IP partner, sequential integer ids | **WORKS, and re-instrumented in build 2.** **238** partner pages (not 236), now class-labelled by the site's own `?cate=` taxonomy and each exactly dated from its asset-upload filenames - see `devilcase-categories-and-dates.md`. In-scope working population **143**. Still handle-blocked |
| **B. 慢慢挑 PianoPianoPick** | Taiwanese drinkware brand licensing illustrator characters onto cups/bags (`聯名款` in every product title) | Enumerable (~30 illustrators) but **scale-filtered upward**: every partner resolved so far sits 24K-941K (灰塵魚 24K, Littdlework 24K, 包大山 32K, weiweiboy 43K, 屎蛋唐尼 82K, 馬卡龍腳趾 98K, 咻咻熊 111K, KINGJUN 113K, 爽爽貓 169K, 地呱球 205K, 馬來貘 941K). Kept as a comparator, not a source of `lt_10k` rows |
| **C. LINE STORE sponsored-sticker showcase** | `store.line.me/stickershop/showcase/{sponsor,event,free}/zh-Hant` | **DEAD** - all three paths return 404. Sponsored stickers are not exposed on the web storefront |
| **D. 文創股長 STARup hub** (Gamania's ~100-creator illustrator incubator, `illustrators.gamania.com`) | Would be an ideal directory - a brand-collab arm over a roster of small creators | **UNREACHABLE from here** - `illustrators.gamania.com` does not resolve (DNS `ENOTFOUND`) on either curl or WebFetch. `blog.shopping.gamania.com` resolves but serves a React shell. Owed to a later build |
| **E. RHINOSHIELD 犀牛盾 Design Studio** `rhinoshield.tw/design-studio/collections/@<slug>` | Taiwan-storefront artist-collection programme; one collection page per creator, each backed by real SKUs | **WORKS - best vein found so far, and strictly better instrumented than Vein A.** 180 creators, and the brand publishes each one's **Instagram handle** and a **declared launch timestamp** itself. 8 of build 2's rows come from here. Full roster: `rhinoshield-design-studio-roster.md` |

---

## Method

### 1. Enumerating the partner directory (Vein A)

`https://devilcase.com.tw/crossover/<n>` for n = 1..360, swept directly.
A live partner page is identified by its `<title>` matching `<IP name> X 惡魔防摔殼｜...`; 236 of 360 ids resolve to a partner.
`robots.txt` is fully permissive.
The page carries the IP's own bio in `<meta name="description">` but **no date and no creator social link**, so both year and follower count have to come from outside the page.

### 2. Dating a collaboration (no date on the page)

Wayback CDX over the whole path:

```
http://web.archive.org/cdx/search/cdx?url=devilcase.com.tw/crossover/*&output=text&fl=original,timestamp&collapse=urlkey&filter=statuscode:200
```

273 numeric ids carry a capture.
**First-capture is an upper bound on launch, not the launch date.** But because the ids are assigned sequentially and the archive crawls this directory in whole-block sweeps, the ids can be *bracketed* between two consecutive sweeps, which is much tighter than a bare upper bound:

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

The window floor is equally firm: the December-2023 bulk crawl swept the directory in one pass and its **highest id is 135**.
Every id at 136 or above was therefore created after 2023-12-04, which puts the whole of the 136-326 range inside the task's 2023-2026 window with no further work.

Three dating bases are used and always stated per row:

- `wayback-bracket` - bounded between two consecutive sweeps. The strong case.
- `wayback-first-capture` - earliest 200 snapshot only, where the preceding sweep does not bracket cleanly (the crawl is patchy below id ~250: id 142 was first captured 2024-11 while id 149 was captured 2024-08, so ids in that range can be older than their first capture).
- `id-sequence` - ids above 309, dated by monotonicity against the 2026-05-09 sweep rather than by a snapshot of their own.

### 3. Resolving the IP's channel and follower count

No handle on the partner page, so:
DuckDuckGo HTML endpoint (`https://html.duckduckgo.com/html/`, POST `q`) queried as `<IP name> instagram 插畫`, then every `(@handle)` in a result title and every `instagram.com/<handle>` in the result body is taken as a candidate, and each candidate is fetched:

```
curl -H 'User-Agent: Mozilla/5.0 (compatible; Googlebot/2.1; ...)' https://www.instagram.com/<handle>/
```

Instagram serves `og:description` = `"<N> Followers, <N> Following, <N> Posts - See Instagram photos and videos from <display name> (@<handle>)"` to that UA.
Both halves matter: the count **and** the display name.

### 4. The handle-squat trap (mandatory guard)

Guessing a handle from a romanised brand name produces a plausible-looking tiny account that is **not the IP**, and every one of those would fabricate an `lt_10k` row.
Proven on this run:

| Guessed handle | What it actually is | Real IP channel |
|---|---|---|
| `@sweetpotatoball` (118) | untitled account | 地呱球 is `@sweet.potato.ball`, **205K** |
| `@tonystan` (96, "Tony Assogba"), `@tonystan_` (199, "Ufoh Anthony") | unrelated people | 屎蛋唐尼 is `@tonystan8787`, **82K** |
| `@baozi` (93, "Rita Bao") | unrelated person | 包大山 is `@baodashan`, **32K** |
| `@littleyellowroom` (25) | untitled account | 小黃間 - unresolved |
| `@digua_ball` (61, "梅子地瓜球") | unrelated account | - |

**Rule enforced on every row in this file: the `og:description` display name must carry the IP's own name.** A count from an account whose display name does not name the IP is discarded, not recorded.

### 4b. Two further traps this vein sets, both of which manufacture false `lt_10k` rows

**The regional-account trap.** An IP that has entered Taiwan through a local distributor often runs a Taiwan-only Instagram account that is an order of magnitude smaller than its home channel. 胡子碰碰 OHIGE no PON (crossover 325) reads **7,769** on `@ohigenopon_tw` and **1,195 / 2,904 / 1,649** on its HK / TH / English accounts - but the creator's own account `@ohigenopon` reads **53K**.
Banding off the local account would have produced an `lt_10k` row for an IP that is nowhere near `lt_10k`.
Same shape as the LuLu the Piggy `@luluthepiggy_hk` case already recorded in `findings/census/hongkong/ip_scale_bands.md`.
**Every candidate is checked for a bare, un-suffixed handle before the band is accepted.**

**The VTuber trap.** 29 of the 142 in-scope, in-window partner pages are VTubers or VTuber groups, identifiable from the partner-page bio (直播 / Twitch / YouTube / 頻道 / 實況).
A VTuber's primary channel is YouTube or Twitch, never Instagram, so an Instagram-only read understates them by tiers and is not a band at all under the census's primary-channel rule. 塔芭絲可 (crossover 143) reads 8,904 on Instagram but is a MIROLIVE first-generation talent whose streaming channels were not measured.
**VTuber rows are held out of this file rather than banded off Instagram** - see Rejected candidates.

### 5. Follower-count basis

Counts are read live and are therefore `current-proxy` against a campaign that launched earlier, exactly as in `findings/census/taiwan-v2/ip_scale_bands.md`.
Social accounts grow, so a **current** count under 10,000 is a *conservative* reading for a past campaign: the at-campaign figure was almost certainly lower still.
That is the safe drift direction for this cell, and it is the reason a current-proxy count is admissible here.
Every row states its retrieval date.

### 6. Vein E - the directory that publishes its own handles (build 2)

Build 1's blocker was never the vein, it was **handle discovery**: 107 of 142 DEVILCASE partners sat unbanded because no reachable search engine would map a Chinese character name to an Instagram handle.
Build 2 opened the search battery again and found it worse, not better - `html.duckduckgo.com` and `lite.duckduckgo.com` now fail at the connection layer (curl exit 000, no HTTP response at all), `search.brave.com` returns 429, Ecosia 403s, five SearXNG public instances return 429, and Yandex 302s to a challenge.
`www.bing.com/search?...&format=rss` **does** answer over plain curl with HTTP 200 and real results - a genuinely useful discovery - but it silently ignores the `site:` operator and falls back to single-character matching on Chinese queries (`蝦米浣糕 RACCAKE` returns shrimp recipes), so it cannot do handle discovery for this population.

The fix was to stop searching.
The right index is **a directory that publishes the creator's social handle itself**, and RHINOSHIELD's Design Studio is one.

1. `https://rhinoshield.tw/robots.txt` is permissive and explicitly `Allow`s ClaudeBot; it names `https://rhinoshield.tw/sitemap.xml`.
2. That index fans out to `sitemap/design/1-30.xml`, which between them carry **414 distinct `design-studio/collections/<slug>` paths**. 182 of those slugs literally begin with `@` - those are the independent creators; the remaining ~232 are licensed properties (`24-hours-of-le-mans`, Disney and so on).
3. Any single collection page carries a **Nuxt flat payload listing the entire creator roster**, not just that creator. Five pages spread across the alphabet each returned 179-180 records and union to **180**. Each record holds: uuid, slug, display name, the brand's own bio line, a `socialMedia` array (Facebook / Instagram / Threads / X URLs), and `firstLaunchedAt` as a millisecond epoch.
4. So the two fields that cost build 1 the most - the handle and the date - both come from the licensee's own database. **159 of 180 creators carry a declared Instagram handle**; 157 of those resolved a live follower count.

This removes the handle-squat trap entirely for Vein E.
Build 1's rule was "the `og:description` display name must carry the IP's own name", which was a defence against a *guessed* handle; here the handle is asserted by the counterparty, and the display-name check merely corroborates it.
Every accepted row below passes both.

**Dating.** `firstLaunchedAt` is a declared first-launch date from the brand, which is stronger evidence than the archive inference used in Vein A.
Where Wayback has any capture of the collection page it is consistent (launch always precedes first capture:
`@ilovemyselfself` declares 2023-07-06 against a 2025-09-15 first capture, `@lorenaxangelina` 2024-12-20 against 2025-09-15).
Wayback coverage of this path is thin, so it corroborates rather than confirms.

**Is this a Taiwan-market row?** Two facts, both checked, and both stated on every Vein E row.
The seller is the NTD-denominated `rhinoshield.tw` storefront, whose own footer names the operating entity as **新加坡商犀牛盾科技股份有限公司台灣分公司** (統一編號 83203375) - a Singapore parent's Taiwan branch, not a wholly Taiwanese company.
The rows say that rather than calling RHINOSHIELD Taiwanese.
But the roster is **not global**:
`@pluddie`, `@hueiheijibai` and `@mrtom_design` all return **404 on `rhinoshield.com`** and **200 on `rhinoshield.jp`**.
So these collections are a Taiwan/Japan-region selection sold on the Taiwan storefront, not a worldwide catalogue that happens to be visible from Taiwan.

**What counts as a character.** The task asks for an independent *character*.
RHINOSHIELD's roster mixes character owners with illustrators who license artwork but own no character.
The line drawn here is evidential, not editorial: a row is accepted only where **the brand's own bio line names a character**.
Sub-10k creators whose bio describes only the artist are recorded below as held, not as rows - see Rejected candidates.

### 7. Vein A re-instrumented (build 2)

Two things build 1 missed on the DEVILCASE pages, both recorded in full in `devilcase-categories-and-dates.md`:

- **The directory publishes its own taxonomy.** `crossover/?cate=1..6` pages it by class. Real counts: 熱門經典角色 17, 三麗鷗 25, **臺灣創作與角色 127**, **海外創作與角色 16**, **VTuber 39**, 遊戲與動漫 14 - **238** partners, not the 236 the id sweep found. The working `lt_10k` population is cate 3 + cate 4 = **143**. Build 1's bio-keyword heuristic put the VTuber block at 29; it is **39**, so ten pages build 1 would have banded off Instagram are not Instagram-primary at all.
- **Every page dates itself.** Crossover art is served from `i.devilxxxx.com/uploads/crossover/<YYYYMMDDHHMMSS>.jpg` - the filename is the upload timestamp. All 238 partner pages carry one. It collapses build 1's 3-week Wayback bracket on crossover 308 to a single day (2026-04-29, inside the 04-14/05-09 bracket). The caveat is self-diagnosing: where art has been refreshed the timestamp is a refresh date, visible because it postdates the Wayback first capture (crossover 1 was live in the 2023-12-04 crawl but reads 2025-10-29).

---

## Rows

**Build 1: 2 verified rows.** Proposals for human accept; nothing here has been written to any database.

| # | brand_name | ip_name | market | year | year basis | source_ref | follower_band | count seen | representable | ip_class | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | DEVILCASE 惡魔防摔殼 | 茶包先生 Mr. Teabag | TW | 2026 | `wayback-bracket` - crossover id 308, first captured 2026-05-09, and the preceding directory sweep on 2026-04-14 captured only up to id 302, so the partnership went live between those two dates | https://devilcase.com.tw/crossover/308 (HTTP 200, 2026-08-07) | `lt_10k` | **8,288** Instagram followers, `@mr.teabag_`, read 2026-08-07 | yes | INDEPENDENT | Solo Taiwanese illustrator brand - three characters (茶包, 栽栽, 捲捲) described on the partner page as unrelated brothers, no studio or parent named anywhere. Handle name-match is exact: `og:description` display name reads `茶包先生｜文博會S057｜插畫 · 旅遊 ᴾᴸᴼᴳ`, i.e. the account states its own 文博會 (Creative Expo Taiwan) booth number **S057** - the creator is a CET exhibitor, which is the same population as `findings/expo/cet2026-*`. `current-proxy` count against a campaign roughly 3 months older, so the at-campaign figure was lower, not higher |
| 2 | DEVILCASE 惡魔防摔殼 | Wasabi Bear 芥末熊 / 와사비베어 | TW | 2026 | `id-sequence` - crossover id 321 has no Wayback snapshot at all, while id 309 was swept 2026-05-09; ids are sequential, so 321 went live after 2026-05-09 | https://devilcase.com.tw/crossover/321 (HTTP 200, 2026-08-07) | `lt_10k` | **4,252** on `@wasabibear_tw` (芥末熊 Wasabi Bear), the largest of three evidenced channels - Korean home account `@wasabibear.official` (와사비베어) reads **3,882** and `@wasabibear_japan` (ワサビベア【日本公式】) reads **3,973**. All read 2026-08-07 | unclear | INDEPENDENT | Korean creator-owned: the character is a handmade doll made by Sugar Rain (Kim Dan-bi) in September 2021, per the Korean-language NamuWiki entry - no conglomerate parent found. **Band is robust against the regional-account trap for once**: unusually, all three country accounts sit under 10K and the *home* account is the smallest of the three, so no choice of primary channel leaves `lt_10k`. `@wasabibear` (56) and `@wasabi.bear` (100) are squats and were rejected. REP=`unclear` because the character is retailed through LINE FRIENDS SQUARE, so an exclusive licensor may already sit in the chain - ownership is independent, addressability is not established |

**Build 2: 8 further verified rows, all from Vein E.** Same status - proposals for human accept, nothing written to any database.

For every row below: `brand_name` = RHINOSHIELD 犀牛盾 (Design Studio), `market` = TW, `ip_class` = INDEPENDENT, and `source_ref` = `https://rhinoshield.tw/design-studio/collections/@<slug>`, curl-verified 200 on 2026-08-07.
`year` basis is the same on all eight: the brand's own `firstLaunchedAt` epoch in the roster payload - **a licensee-declared launch date**, not an archive inference.
Follower counts are Instagram `og:description` reads on 2026-08-07 against the handle **the brand itself publishes** for that creator, so the count is `current-proxy` and, per section 5, conservative for a past campaign.

| # | ip_name | year | source_ref (`@slug`) | declared launch | follower_band | count seen | live SKU designs | representable | notes |
|---|---|---|---|---|---|---|---|---|---|
| 3 | 小女孩和花花獅 / PLUDDIE Studio | 2025 | `@pluddie` | 2025-10-24 | `lt_10k` | **4,284**, `@pluddiestudio`, display name 小女孩和花花獅工作室 | 15 | yes | The clearest character row in the file. The brand's own bio names two characters and their relationship: 小女孩, and 花花獅 as "her best friend and most faithful companion". One-studio operation, no parent or agent named |
| 4 | 灰黑集白 / 黑貓馬路 Maru | 2025 | `@hueiheijibai` | 2025-12-30 | `lt_10k` | **4,443**, `@aasta_blacknwhite`, display name 灰黑集白｜黑貓馬路 Maru | 19 | yes | Named character: a bobtail black cat, 馬路 (Maru). Creator-run, no label |
| 5 | Cheesy Duck | 2026 | `@cheesyduck` | 2026-03-05 | `lt_10k` | **6,088**, `@cheesyduck_unstop`, display name Cheesy_duck | 6 | yes | Bio is explicit about the ownership shape: "Creator of Cheesy Duck, a cheerful character who loves small adventures" - a single creator who owns a single character. Launched under 3 months before retrieval, so the current-proxy gap is small |
| 6 | 湯姆先生 MR. TOM | 2025 | `@mrtom_design` | 2025-06-26 | `lt_10k` | **6,142**, `@mrtom_design` (handle equals the collection slug), display name 湯姆先生MR. TOM | 7 | yes | Named character with a stated design rule - "every object in the world has a soul, just add eyes". Camping/outdoors theme |
| 7 | 迪普西 Dipsy | 2025 | `@dipsy` | 2025-11-28 | `lt_10k` | **6,801**, `@dipsydisplay`, display name 迪普西 。Dipsy | **48** | yes | The largest SKU count of any accepted row - 48 distinct designs off a 6.8K-follower creator, which is the single sharpest datum in this file against "small IP gets token deals" |
| 8 | LilyandStarsStudio / Bun and Bear | 2025 | `@lilyandstarsstudio` | 2025-08-04 | `lt_10k` | **7,586**, `@lilyandstarsstudio` (handle equals slug), display name LilyandStarsStudio | 12 | yes | Two named characters, Bun and Bear |
| 9 | ilovemyselfself | 2023 | `@ilovemyselfself` | 2023-07-06 | `lt_10k` | **3,460**, `@ilovemyselfself` (handle equals slug), display name Ilovemyselfself | 8 | yes | **The earliest in-window row in the file** and the only 2023 one. Bio self-describes as 獨立設計品牌 - an independent design brand built on a 厭世 dog character and a one-person `#ihatemondayclub`. Wayback first capture of the collection page is 2025-09-15, consistent with (and much later than) the declared 2023 launch |
| 10 | sillysally 실리샐리 | 2024 | `@sillysally` | 2024-09-10 | `lt_10k` | **3,113**, `@sillysally.official`, display name sillysally 실리샐리 | 27 | yes | Korean creator, same import shape as row 2. The character is the brand name itself; the bio names no separate character, so this is the weakest of the eight on the character test and is flagged as such rather than dropped. 27 live designs |

**Read on the ten rows.** Build 1 could say the cell exists.
Build 2 can say what it looks like: a second, independent Taiwanese-market licensee - larger, better documented, and reached by a completely different route - lands eight more sub-10k character deals, one of them running 48 SKUs.
Two brands, ten rows, and in Vein E's case the *licensee's own database* asserts both the creator's handle and the launch date.
The census's zero was a property of press indexing, and that is now shown twice over rather than argued once.

**The population statistic, which may matter more than the rows.** Vein E is the first source in this run where the denominator is exactly known, so the sub-10k share of a real Taiwanese-market licensing roster can be stated rather than estimated.
Of the 157 RHINOSHIELD Design Studio creators whose follower count resolved:

| band | creators | share |
|---|---|---|
| `lt_10k` | 21 | 13.4% |
| `10k_50k` | 91 | 58.0% |
| `50k_200k` | 38 | 24.2% |
| `200k_1m` | 7 | 4.5% |
| `gt_1m` | 0 | 0% |

**One in seven creators on this brand's roster is sub-10k, and the press-built census recorded that band at zero.** The gap is the measurement, not the market.
(The 21 are the pool build 2 adjudicated down to 8 rows; the other 13 are itemised in Rejected candidates below.)

---

## Rejected candidates

**Total rejected across both builds: 24 named (11 in build 1, 13 in build 2), plus the population-level rejections below.**

### Build 1 rejected: 11 named

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

### Build 2 rejected: 13 named from Vein E, all of them sub-10k and all of them rejected on class rather than on scale

These are the 21 sub-10k RHINOSHIELD creators minus the 8 accepted.
Every count below was read on 2026-08-07 from the handle the brand itself publishes, so none of these is a discovery failure - they are adjudications.

| Candidate | Followers | Declared launch | Reason |
|---|---|---|---|
| 樂成宮｜月緣室 Yuanfen Factory (`@yuanfenfactory`) | 2,494 | 2026-02-10 | **Not a character, and institutional.** A 200-year-old Taichung city-designated heritage temple (旱溪媽祖廟) licensing under a 月緣室 sub-brand. Same class as DEVILCASE crossover 257 (新竹天王寺財神廟), rejected there too |
| 財團法人黑潮海洋文教基金會 (`@kuroshio1998`) | 7,399 | 2025-11-28 | **Not a character, and institutional.** A registered non-profit marine foundation, Hualien, est. 1998. A real independent licensor and a genuinely interesting row for a different cell, but not a character IP |
| Jin Jin Tattoo (`@jinjintattoo`) | 3,207 | 2025-09-10 | **Not a character.** A tattoo artist licensing flash designs |
| 墨流書法 InkFlowCalligraphy (`@inkflowcalligraphy`) | 7,295 | 2026-03-22 | **Not a character.** Calligraphy. Also creator-resident in Australia |
| 窩窩頭 (`@wowohead_2023`) | 2,154 | 2025-01-21 | **Character not evidenced.** Hand-carved stamp studio; the bio describes stories hidden in stamps, names no character |
| 時薪一加侖鮮奶 (`@gallon_milk14`) | 2,423 | 2025-12-11 | **Character not evidenced.** Food illustrator; the name is a joke about being paid in milk, not a character |
| 阿薛 Hsueh (`@hsueh.illu`) | 2,428 | 2025-12-02 | **Character not evidenced.** Botanical illustrator |
| HLTOO 曾湘玲 (`@hl.t_oo`) | 5,613 | 2025-09-13 | **Character not evidenced.** Fine-art illustrator working under her own name |
| 舒媞 SHUTI (`@ti_illustration`) | 9,170 | 2025-09-01 | **Character not evidenced.** Tainan-born freelance illustrator, Cambridge School of Art children's-book MA. Bio explicitly describes brand work, so this is a real licensing creator - but no character |
| 旅貓實驗室 (`@travelpaint.cat`) | 1,785 | 2025-12-02 | **Character not evidenced.** Photographs and draws real cats rather than an original character |
| AndreaCat (`@andreacat805`) | 1,055 | 2025-12-01 | **Character not evidenced.** The bio describes the creator ("a cat-loving illustrator"), not a character |
| LorenaxAngelina (`@lorenaxangelina`) | 2,704 | 2024-12-20 | **Character not evidenced.** German fantasy artist |
| 1nsp0 (`@1nsp0.1_0`) | **18** | 2025-02-20 | **Character not evidenced, and the count is not trustworthy.** 18 followers over 11 posts, and the Instagram `og:description` carries no display name at all - almost certainly a dormant or secondary account rather than the creator's working channel. Recorded rather than banded, because an 18-follower reading would be the most extreme datum in the file and the account cannot carry it |

Two further RHINOSHIELD creators (`@hanomanga`, `@1982kids`) returned an Instagram `og:description` with no follower substring at all and are **unresolved, not rejected**; 21 more publish no Instagram handle in the roster and were never banded.

**Population-level rejection.** Of the 236 partner pages:
**41** are licensed properties or otherwise out of scope (Sanrio's eight characters, Moomin, Garfield, Rilakkuma, Gundam, Monster Hunter, HUNTERxHUNTER, 神魔之塔, 傳說對決, Hatsune Miku, 貓福珊迪, 吉伊卡哇, 卡娜赫拉, 白爛貓, ㄇㄚˊ幾兔, 好想兔, a government mascot, a temple, a car-review channel and similar) and were excluded before any follower work; and **70** sit at ids 1-135, dated only as "on or before 2023-12-04", so they fall outside the task's 2023-2026 window.
That leaves **142 in-scope, in-window partner pages** as the working population - the denominator every completeness claim in this file is against.

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

### Build 2 additions (all curl-verified 2026-08-07)

| URL | Status | Role |
|---|---|---|
| https://rhinoshield.tw/robots.txt | 200 | Vein E access basis - permissive, explicitly `Allow`s ClaudeBot |
| https://rhinoshield.tw/sitemap.xml → `sitemap/design/1-30.xml` | 200 | Vein E enumeration - 414 collection slugs, 182 of them `@`-prefixed creators |
| https://rhinoshield.tw/design-studio/collections/%40pluddie | 200 | Row 3 `source_ref` (15 designs) |
| https://rhinoshield.tw/design-studio/collections/%40hueiheijibai | 200 | Row 4 `source_ref` (19 designs) |
| https://rhinoshield.tw/design-studio/collections/%40cheesyduck | 200 | Row 5 `source_ref` (6 designs) |
| https://rhinoshield.tw/design-studio/collections/%40mrtom_design | 200 | Row 6 `source_ref` (7 designs) |
| https://rhinoshield.tw/design-studio/collections/%40dipsy | 200 | Row 7 `source_ref` (48 designs) |
| https://rhinoshield.tw/design-studio/collections/%40lilyandstarsstudio | 200 | Row 8 `source_ref` (12 designs) |
| https://rhinoshield.tw/design-studio/collections/%40ilovemyselfself | 200 | Row 9 `source_ref` (8 designs) |
| https://rhinoshield.tw/design-studio/collections/%40sillysally | 200 | Row 10 `source_ref` (27 designs) |
| instagram.com/{pluddiestudio, aasta_blacknwhite, cheesyduck_unstop, mrtom_design, dipsydisplay, lilyandstarsstudio, ilovemyselfself, sillysally.official} | 200 (all 8) | Rows 3-10 follower counts |
| rhinoshield.**com**/design-studio/collections/%40{pluddie, hueiheijibai, mrtom_design} | **404** (all 3) | Market evidence - the roster is not a global catalogue |
| rhinoshield.**jp**/design-studio/collections/%40{pluddie, hueiheijibai, mrtom_design} | **200** (all 3) | Market evidence - TW/JP-region selection |
| `web.archive.org/cdx/.../design-studio/collections/@ilovemyselfself` | `20250915133002 200` | Row 9 dating corroboration (postdates the declared 2023-07-06 launch, as it must) |
| https://devilcase.com.tw/crossover/?cate=1..6 | 200 (all 6) | Vein A taxonomy - 238 partners, 143 in-scope, 39 VTubers |
| https://creator.amuse.com.tw/ | 200 | RHINOSHIELD's creator platform (`<title>Creator Platform`); serves a JS shell, so noted as existing, not read |
| https://www.bing.com/search?q=...&format=rss | 200 | Working curl-able search endpoint - but unusable for Chinese handle discovery (see method §6) |
| html.duckduckgo.com, lite.duckduckgo.com | **curl exit 000** | Search battery - no HTTP response at all |
| search.brave.com | 429 | Search battery |
| www.ecosia.org | 403 | Search battery |
| searx.be, priv.au, searxng.site, opnxng.com, search.inetol.net, baresearch.org | 429 / empty | Search battery - five of six SearXNG instances rate-limit |

---

## What build 2 leaves owed

**10 of 25 rows.** The stop condition is not met and the sources are not exhausted - build 2 opened a new vein rather than closing the old one, and both are still producing.

1. **Vein A is still 100+ pages unbanded, and the handle problem there is now the *only* problem.** Dating and classification are solved (`devilcase-categories-and-dates.md`), so all that is missing for 143 in-scope DEVILCASE partners is a name-to-handle map - and build 2 established that no reachable search engine will supply one. The route that worked for Vein E is the route to try: find whether DEVILCASE publishes handles anywhere itself (its own Instagram `@devilcaseig` tags partners; its Facebook posts are Googlebot-readable per `follower-count-verification-channels`). Failing that, **cross-join the two rosters** - any creator appearing in both directories inherits the RHINOSHIELD-declared handle, which is free and exact.
2. **Vein E's 21 handle-less creators and 2 unresolved reads.** 21 of 180 publish no Instagram in the roster payload; several have Facebook or Threads entries in the same `socialMedia` array that build 2 did not parse. Cheap and likely to add rows.
3. **The 39 VTubers still need a YouTube/Twitch read** - unchanged from build 1, but the count is 39 not 29, and cate 5 gives the exact list.
4. **A third brand.** Two licensees now, both phone accessories. That is a category, not a market. The same sitemap-then-payload technique should be tried on other Taiwanese consumer brands with artist programmes; `creator.amuse.com.tw` suggests the RHINOSHIELD roster is run on a reusable creator platform that may serve other brands too.
5. **Representability is asserted, not tested.** Every Vein E row is marked `representable: yes` because no agent, label or parent is named for any of the eight anywhere in the brand's own roster record - which is an absence-of-evidence basis, not a positive finding. Two things point the same way without proving it: `creator.amuse.com.tw` ("Creator Platform") exists and serves every artist asset, and `/design-studio` carries a public 聯名合作許願池 inbound form. Note that the 許願池 is **consumer-facing** ("有夢幻聯名想要我們幫你實現嗎？") - a request-a-collab suggestion box, not a creator application - so it is evidence the programme takes inbound, not evidence a creator can apply. A build that wants a real REP finding should try to read past the `creator.amuse.com.tw` JS shell. Until then this should be said out loud on any prospect page that uses these rows.

## What build 1 left owed

1. **The resolution sweep reached 42 of the 142 in-scope, in-window partner pages, and only 7 of those 42 returned any candidate handle from the automated search** (four more - 茶包先生, 蝦米浣糕, 安怎？, 好吧星期一 - were resolved by hand). So roughly **107 of 142 partner pages are still unbanded**, and each one is a live `lt_10k` candidate. The blocker is search access, not the vein: DuckDuckGo's HTML endpoint answers about ten queries then serves empty result sets permanently, and Brave Search answers reliably at one worker but drops to roughly a 20% hit rate at three concurrent workers. The next build should run **one** worker with a longer delay, and must re-attempt the ids that logged an empty candidate list rather than treating them as resolved.
2. **The 29 VTuber partners need a YouTube/Twitch read**, not an Instagram one, before they can be accepted or rejected. `https://www.youtube.com/@<handle>` yields a subscriber count from the channel-header accessibility label, per the method already used for Fumeancats in `findings/census/taiwan-v2/ip_scale_bands.md`.
3. **Brand diversity.** Both build-1 rows carry the same brand. The rows are real, but a cell that rests on one licensee is thin for a prospect page. Vein D (文創股長 STARup hub) is the best untried source of a *second* brand-side directory, and 蝦米浣糕 x ViewFinder is a live lead into apparel.
4. **Ids 1-135 are undated.** If the 2023 slice matters, they need a second dating source - DEVILCASE's own Facebook/Instagram launch posts are the obvious candidate.
