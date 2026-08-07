# Taiwan x `lt_10k` independent collaborations - verified rows

Task: `tasks/tw-lt10k-independent.md`.
Goal: documented brand collaborations in Taiwan, 2023-2026, where the partner IP is an INDEPENDENT (or MIXED) character that stood at or under 10,000 followers.
The ten-market census (`findings/census/taiwan-v2/ip_scale_bands.md`) holds **zero** `lt_10k` Taiwan rows at whole-row level - the single `lt_10k` reading in that file is a per-creator sub-band inside two-creator row 76 (臺灣印事).
This file is the dedicated hunt for the missing cell.

**Status: in progress.
Build 3 of the run - 12 verified rows of a 25-row stop condition.
Retrieval date for everything below: 2026-08-07.**

> **Build 3 correction notice.** Build 3 re-parsed the RHINOSHIELD roster payload properly (devalue index dereferencing rather than regex scraping) and found that **build 2's per-row "declared launch" dates were the wrong field**: they are the creator's avatar-image cache-buster, an asset-upload timestamp, not the roster's `firstLaunchedAt`.
> Four of the eight build-2 row years change as a result. All four stay inside the 2023-2026 window, so no row is invalidated, but the year column below has been rewritten and the corrected and mistaken values are shown side by side.
> The follower work was independently re-run from scratch and reproduces exactly (same 21 sub-10k creators), so only the dating was wrong.
> Full detail: `rhinoshield-design-studio-roster.md`.

---

## Why the census found none, and what that implies for the search

The census was built from press coverage (UDN, ETtoday, LTN, WalkerLand, cava.tw and similar roundups).
Press coverage is itself a scale filter: a Taiwanese outlet writes up a 聯名 when the IP is already recognisable, so the press-indexed population starts at roughly `10k_50k` and runs up.
A sub-10k IP that gets a real brand deal leaves its trace on **the brand's own commerce surface**, not in the press.

That reframes the search.
The productive index is not a news archive - it is a **brand-run licensing directory**: a Taiwanese consumer brand that publishes one page per IP partner and keeps every partner page live.
Build 1 found and swept one such directory in full (Vein A, DEVILCASE).
Build 2 found a second, better-instrumented one (Vein E, RHINOSHIELD Design Studio) that publishes each creator's Instagram handle and launch date itself - which is what broke build 1's real blocker, handle discovery.

Build 3 found the generalisation of that move.
Where a *licensing* directory publishes handles you get rows; where a **trade-show exhibitor directory** publishes them you get the missing dictionary - a Chinese-name-to-Instagram-handle map that no search engine will give you (Vein F, 文博會).
The dictionary does not produce rows by itself, because exhibiting is not a collaboration.
What it does is make every other vein bandable, and it supplies the second exactly-known denominator this file now rests on.

---

## Veins tested

| Vein | What it is | Verdict |
|---|---|---|
| **A. DEVILCASE 惡魔防摔殼 `/crossover/<id>`** | Taiwanese phone-case brand; one live page per IP partner, sequential integer ids | **WORKS, and re-instrumented in build 2.** **238** partner pages (not 236), now class-labelled by the site's own `?cate=` taxonomy and each exactly dated from its asset-upload filenames - see `devilcase-categories-and-dates.md`. In-scope working population **143**. Build 3 unblocked **23** of them via Vein F; the other 120 stay handle-blocked |
| **B. 慢慢挑 PianoPianoPick** | Taiwanese drinkware brand licensing illustrator characters onto cups/bags (`聯名款` in every product title) | Enumerable (~30 illustrators) but **scale-filtered upward**: every partner resolved so far sits 24K-941K (灰塵魚 24K, Littdlework 24K, 包大山 32K, weiweiboy 43K, 屎蛋唐尼 82K, 馬卡龍腳趾 98K, 咻咻熊 111K, KINGJUN 113K, 爽爽貓 169K, 地呱球 205K, 馬來貘 941K). Kept as a comparator, not a source of `lt_10k` rows |
| **C. LINE STORE sponsored-sticker showcase** | `store.line.me/stickershop/showcase/{sponsor,event,free}/zh-Hant` | **DEAD** - all three paths return 404. Sponsored stickers are not exposed on the web storefront |
| **D. 文創股長 STARup hub** (Gamania's ~100-creator illustrator incubator, `illustrators.gamania.com`) | Would be an ideal directory - a brand-collab arm over a roster of small creators | **UNREACHABLE from here** - `illustrators.gamania.com` does not resolve (DNS `ENOTFOUND`) on either curl or WebFetch. `blog.shopping.gamania.com` resolves but serves a React shell. Owed to a later build |
| **E. RHINOSHIELD 犀牛盾 Design Studio** `rhinoshield.tw/design-studio/collections/@<slug>` | Taiwan-storefront artist-collection programme; one collection page per creator, each backed by real SKUs | **WORKS, and now EXHAUSTED.** **182** records (not 180), and the brand publishes each one's **Instagram handle** and a **declared launch timestamp** itself. 10 of the 12 rows come from here. Build 3 resolved every remaining handle-less record, so this vein has no unworked residue. Full roster: `rhinoshield-design-studio-roster.md` |
| **F. Creative Expo Taiwan 2026 exhibitor directory** `creativexpo.tw/zh-TW/exhibitor_list/<id>` | The 文博會 public exhibitor directory; one server-rendered page per exhibitor, carrying that exhibitor's own social links | **WORKS as a name-to-handle map, and is NOT a row source.** 629 exhibitor pages, **405 publishing an Instagram handle**, 402 banded. This is the CJK name-to-handle index builds 1 and 2 both concluded did not exist. It produced 1 row (via Vein E) and unblocked 23 Vein A partners. Exhibiting is not a collaboration, so nothing is sourced from it directly. Full map: `cet2026-exhibitor-handle-map.md` |

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

### 8. Vein F - the CJK name-to-handle index that builds 1 and 2 both concluded did not exist (build 3)

Both earlier builds ended blocked on the same thing and said so in the same words: no reachable search engine will map a Chinese-character IP name to an Instagram handle, so 100+ documented DEVILCASE collaborations cannot be banded.
Build 3 re-tested the search battery and it is worse again - `html.duckduckgo.com` and `lite.duckduckgo.com` still fail at the connection layer (curl exit 000), `tw.search.yahoo.com` now does too, `www.google.com/search` answers 200 but the body is a JavaScript redirect stub with `table,div,span,p{display:none}` and no results, and `mojeek.com` answers 200 with an empty result set.

The fix was again to stop searching and find a *directory*.
**The Creative Expo Taiwan (文博會) public exhibitor directory is a name-to-handle index for exactly this population.**

1. `https://creativexpo.tw/robots.txt` disallows only four SEO crawlers and carries `User-agent: * / Allow: /`.
2. `https://creativexpo.tw/zh-TW/exhibitor_list/<id>` is server-rendered (a Rails app, unlike almost everything else tried in this run) and carries the exhibitor's own social links in the page body. The list page itself shows only 15 featured exhibitors, so the directory is reached by sweeping ids, the same way Vein A was.
3. Ids 1-749 swept: **629 resolve to an exhibitor page**, **405 publish at least one Instagram handle**, 273 publish Facebook, 208 publish neither.
4. One Instagram handle and three Facebook links appear on every page and are site furniture; they were removed by a frequency rule (present on >50% of pages) before anything was computed.

Full map, with a live follower count and band for all 402 exhibitors that resolved one: `cet2026-exhibitor-handle-map.md`.

**It is not a row source.** Exhibiting at a trade show is not a brand collaboration, so no row in this file is sourced from Vein F. It is used two ways: as the handle map for the other veins, and as a second exactly-denominated Taiwanese population.

**What the join actually produced.**

- Against **Vein A (DEVILCASE)**: exact-name join on the 143 in-scope partners returns **23 handles**. One (泡芙 → 波波與小泡芙) is a false match and was rejected on inspection; one sits at exactly 10K and is rejected as boundary-ambiguous; the other 21 are all above 10K. **Zero new rows, and that is itself the finding** - see the caveat under the population table.
- Against **Vein E (RHINOSHIELD)**: 20 of the 182 roster creators are also CET2026 exhibitors, which corroborates rows independently (row 4, 灰黑集白, publishes the same handle in both directories). It also produced **row 12**, which no name join would have found - 吶吉吶吉 in one directory and 吶吉與他的搗蛋怪朋友 in the other share only a two-character run, and the identification is carried by the character set (兔人 / 鳥人 / 貓人 vs 搗蛋怪朋友), not the name.

**The join also fabricates rows if run unsupervised.** DEVILCASE's 泡芙 is a hedgehog with a sibling called 芋泥; CET's 波波與小泡芙 is a different IP whose pairing is 波波 and 小泡芙, reading 8,991 followers. A substring join accepts it and it would have been row 13. The DEVILCASE partner-page bio is what refutes it. **Every join hit is adjudicated against the source page's own description before it is used**, and a looser n-gram join was run and produced nothing but generic-token noise (工作室, 插畫, 製造所).

### 9. LINE STORE's sticker search API - the one index that answers CJK queries (build 3)

`https://store.line.me/api/search/sticker?query=<q>&offset=0&limit=40&country=TW&lang=zh-Hant` returns JSON with `totalCount` and per-item `title` and `authorName`.
The HTML search page at `store.line.me/search/sticker` is client-rendered and returns an empty shell, but sticker *product* pages (`/stickershop/product/<id>/zh-Hant`) and *author* pages (`/stickershop/author/<id>/zh-Hant`) are server-rendered.
It is the only index found in this run that answers a Chinese-character query at all.

What it gives and does not give: it resolved the author identity behind four of Vein E's handle-less creators (木木の口袋 → `mumu.b3d.pocket`, which turned out to be an Instagram handle too; 棉花糖柴柴 → "A Mix"; 胸毛公寓 → "Chest hair apartment"; 尼胖 → "Nipang"), but LINE author pages carry **no social links**, so only the first of those four converted into a follower count.
The sponsored-sticker showcase (Vein C) is still 404 on all three paths, so LINE remains an identity resolver, not a collaboration index.

---

## Rows

**Build 1: 2 verified rows.** Proposals for human accept; nothing here has been written to any database.

| # | brand_name | ip_name | market | year | year basis | source_ref | follower_band | count seen | representable | ip_class | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | DEVILCASE 惡魔防摔殼 | 茶包先生 Mr. Teabag | TW | 2026 | `wayback-bracket` - crossover id 308, first captured 2026-05-09, and the preceding directory sweep on 2026-04-14 captured only up to id 302, so the partnership went live between those two dates | https://devilcase.com.tw/crossover/308 (HTTP 200, 2026-08-07) | `lt_10k` | **8,288** Instagram followers, `@mr.teabag_`, read 2026-08-07 | yes | INDEPENDENT | Solo Taiwanese illustrator brand - three characters (茶包, 栽栽, 捲捲) described on the partner page as unrelated brothers, no studio or parent named anywhere. Handle name-match is exact: `og:description` display name reads `茶包先生｜文博會S057｜插畫 · 旅遊 ᴾᴸᴼᴳ`, i.e. the account states its own 文博會 (Creative Expo Taiwan) booth number **S057** - the creator is a CET exhibitor, which is the same population as `findings/expo/cet2026-*`. `current-proxy` count against a campaign roughly 3 months older, so the at-campaign figure was lower, not higher |
| 2 | DEVILCASE 惡魔防摔殼 | Wasabi Bear 芥末熊 / 와사비베어 | TW | 2026 | `id-sequence` - crossover id 321 has no Wayback snapshot at all, while id 309 was swept 2026-05-09; ids are sequential, so 321 went live after 2026-05-09 | https://devilcase.com.tw/crossover/321 (HTTP 200, 2026-08-07) | `lt_10k` | **4,252** on `@wasabibear_tw` (芥末熊 Wasabi Bear), the largest of three evidenced channels - Korean home account `@wasabibear.official` (와사비베어) reads **3,882** and `@wasabibear_japan` (ワサビベア【日本公式】) reads **3,973**. All read 2026-08-07 | unclear | INDEPENDENT | Korean creator-owned: the character is a handmade doll made by Sugar Rain (Kim Dan-bi) in September 2021, per the Korean-language NamuWiki entry - no conglomerate parent found. **Band is robust against the regional-account trap for once**: unusually, all three country accounts sit under 10K and the *home* account is the smallest of the three, so no choice of primary channel leaves `lt_10k`. `@wasabibear` (56) and `@wasabi.bear` (100) are squats and were rejected. REP=`unclear` because the character is retailed through LINE FRIENDS SQUARE, so an exclusive licensor may already sit in the chain - ownership is independent, addressability is not established |

**Rows 3-12: 10 verified rows from Vein E** (8 landed by build 2, 2 added by build 3). Same status - proposals for human accept, nothing written to any database.

For every row below: `brand_name` = RHINOSHIELD 犀牛盾 (Design Studio), `market` = TW, `ip_class` = INDEPENDENT, and `source_ref` = `https://rhinoshield.tw/design-studio/collections/@<slug>`, curl-verified 200 on 2026-08-07.
`year` basis is the same on all ten: the brand's own **`firstLaunchedAt`** field in the roster payload - a licensee-declared launch date, not an archive inference.
The `build 2 said` column records the value build 2 published for that field, which was in fact the avatar cache-buster; it is kept visible so the correction can be checked rather than taken on trust.
Follower counts are Instagram `og:description` reads on 2026-08-07 against the handle **the brand itself publishes** for that creator, so the count is `current-proxy` and, per section 5, conservative for a past campaign.

| # | ip_name | year | declared launch (`firstLaunchedAt`) | build 2 said | source_ref (`@slug`) | follower_band | count seen | live SKU designs | representable | notes |
|---|---|---|---|---|---|---|---|---|---|---|
| 3 | 小女孩和花花獅 / PLUDDIE Studio | **2023** | 2023-11-17 | 2025-10-24 | `@pluddie` | `lt_10k` | **4,284**, `@pluddiestudio`, display name 小女孩和花花獅工作室 | 15 | yes | The clearest character row in the file. The brand's own bio names two characters and their relationship: 小女孩, and 花花獅 as "her best friend and most faithful companion". One-studio operation, no parent or agent named. Year corrected by build 3 |
| 4 | 灰黑集白 / 黑貓馬路 Maru | 2025 | 2025-03-18 | 2025-12-30 | `@hueiheijibai` | `lt_10k` | **4,443**, `@aasta_blacknwhite`, display name 灰黑集白｜黑貓馬路 Maru | 19 | yes | Named character: a bobtail black cat, 馬路 (Maru). Creator-run, no label. **Independently corroborated by Vein F**: 灰黑集白 is CET2026 exhibitor 134 and publishes the same handle there |
| 5 | Cheesy Duck | 2026 | 2026-05-22 | 2026-03-05 | `@cheesyduck` | `lt_10k` | **6,088**, `@cheesyduck_unstop`, display name Cheesy_duck | 6 | yes | Bio is explicit about the ownership shape: "Creator of Cheesy Duck, a cheerful character who loves small adventures" - a single creator who owns a single character. The newest row in the file; the current-proxy gap is 2.5 months |
| 6 | 湯姆先生 MR. TOM | 2025 | 2025-08-21 | 2025-06-26 | `@mrtom_design` | `lt_10k` | **6,142**, `@mrtom_design` (handle equals the collection slug), display name 湯姆先生MR. TOM | 7 | yes | Named character with a stated design rule - "every object in the world has a soul, just add eyes". Camping/outdoors theme |
| 7 | 迪普西 Dipsy | **2023** | 2023-11-22 | 2025-11-28 | `@dipsy` | `lt_10k` | **6,801**, `@dipsydisplay`, display name 迪普西 。Dipsy | **48** | yes | The largest SKU count of any row here - 48 distinct designs off a 6.8K-follower creator, which is the single sharpest datum in this file against "small IP gets token deals". Year corrected by build 3, and the correction *strengthens* the row: the relationship is 2.5 years old, not 9 months. Weak on the character test - the brand's bio line ("描繪日常，用鬆餅犒賞自己") names no character, so the character claim rests on the collection name alone |
| 8 | LilyandStarsStudio / Bun and Bear | **2024** | 2024-09-06 | 2025-08-04 | `@lilyandstarsstudio` | `lt_10k` | **7,586**, `@lilyandstarsstudio` (handle equals slug), display name LilyandStarsStudio | 12 | yes | Two named characters, Bun and Bear. Year corrected by build 3 |
| 9 | ilovemyselfself | 2023 | 2023-06-30 | 2023-07-06 | `@ilovemyselfself` | `lt_10k` | **3,460**, `@ilovemyselfself` (handle equals slug), display name Ilovemyselfself | 8 | yes | **The earliest in-window row in the file.** Bio self-describes as 獨立設計品牌 - an independent design brand built on a 厭世 dog character and a one-person `#ihatemondayclub`. Wayback first capture of the collection page is 2025-09-15, consistent with (and much later than) the declared 2023 launch. Note that 2023-06-30 is shared with two other records, so it is likely the platform's own data-import date and therefore an upper bound on this creator's real start |
| 10 | sillysally 실리샐리 | **2026** | 2026-02-26 | 2024-09-10 | `@sillysally` | `lt_10k` | **3,113**, `@sillysally.official`, display name sillysally 실리샐리 | 27 | yes | Korean creator, same import shape as row 2. The character is the brand name itself; the bio names no separate character, so this is among the weakest rows on the character test and is flagged as such rather than dropped. Year corrected by build 3 - and this is the one row where the correction moves the year *later*, because its assets predate its Taiwan launch by 17 months |
| 11 | 阿7世界 (欸貓 / 櫻鵝 / 草莓狗 / 貓桃鷹) | 2023 | 2023-11-27 | - | `@chilittleworld` | `lt_10k` | **3,267**, `@chi_littleworld`, display name 阿7世界 | 6 | yes | **New in build 3.** The strongest character row in the file after row 3: the brand's own bio names four characters and their types - 熬夜系的欸貓, 佛系櫻鵝, 暖系草莓狗, 獨處系貓桃鷹 - and says they became friends. The roster publishes no handle for this creator, so the handle was guessed and then accepted only on an exact display-name match (阿7世界). The squat `@chilittleworld` (YuChi, 2 followers) is the counter-example that makes the name-match rule necessary |
| 12 | 吶吉吶吉 NAGIxNAGI | 2026 | 2026-06-12 | - | `@nagiart` | `lt_10k` | **8,105**, `@oooo_nagixnagi`, display name NAGIxNAGI!!!吶吉和他的搗蛋怪朋友｜IP雜貨 | 7 | yes | **New in build 3, and the only row in the file found by cross-referencing two independent directories.** The roster publishes no handle; the handle came from Vein F (CET2026 exhibitor 122, 吶吉與他的搗蛋怪朋友), and the identification is carried by the character set, not the name: the RHINOSHIELD bio reads 「這裡是吶吉和他的搗蛋怪朋友們，兔人、鳥人、貓人」 and the Instagram display name reads 吶吉和他的搗蛋怪朋友. The account's own bio calls itself `IP雜貨`, i.e. the creator describes themselves as running an IP. Ten handle guesses had already failed on this one |

**Read on the twelve rows.** Build 1 could say the cell exists.
Build 2 could say what it looks like: a second Taiwanese-market licensee, larger and better documented, landing eight more sub-10k character deals, one of them running 48 SKUs.
Build 3 closes Vein E (every record parsed, every resolvable handle resolved), corrects the dating basis, and adds the two rows that were hiding behind the handle gap - one of them only reachable by cross-referencing a second directory.
Two brands, twelve rows, and in Vein E's case the *licensee's own database* asserts both the creator's handle and the launch date.
The census's zero was a property of press indexing, and that is now shown three ways: two brand rosters and a trade-show floor.

**The population statistics, which may matter more than the rows.** There are now two exactly-known Taiwanese denominators, one a licensing roster and one not.

| population | n | sub-10k | share |
|---|---|---|---|
| RHINOSHIELD Design Studio creators with a resolved follower count (a **licensing roster**) | 160 | 21 | **13.1%** |
| Creative Expo Taiwan 2026 exhibitors with a resolved follower count (a **trade-show floor**) | 402 | 188 | **46.8%** |
| DEVILCASE Taiwanese/overseas-character partners resolvable via the CET map (a **licensing roster**) | 23 | 0 | **0%** (one at exactly 10K) |
| the ten-market census, Taiwan (**press-built**) | - | 0 | **0%** |

RHINOSHIELD's full band distribution:

| band | creators | share |
|---|---|---|
| `lt_10k` | 21 | 13.1% |
| `10k_50k` | 93 | 58.1% |
| `50k_200k` | 39 | 24.4% |
| `200k_1m` | 7 | 4.4% |
| `gt_1m` | 0 | 0% |

**One in seven creators on RHINOSHIELD's roster is sub-10k, nearly one in two on the 文博會 floor is, and the press-built census recorded the band at zero.**
The three numbers are a ladder of filters, not three views of one market: the trade-show floor is the creative population, the licensing roster is what survives a licensee's selection, and the press is what survives an editor's.
Each step drops the sub-10k share, and the last step drops it to nothing.
(The 21 RHINOSHIELD sub-10k creators are the pool adjudicated down to rows 3-10; the other 13 are itemised in Rejected candidates below. Rows 11 and 12 come from a different pool - the creators the roster publishes no handle for, who are outside the 160 and therefore outside the 13.1%.)

**The DEVILCASE line needs its caveat stated with it.** The 23 are the DEVILCASE partners whose handle the CET2026 directory happens to supply, and exhibiting at 文博會 plausibly correlates with scale, so that subsample is biased upward by an unknown amount. What it does establish is that the DEVILCASE Taiwanese-character roster is not a sub-10k roster: the 23 run from 8,288 to 271K with a median around 36K, and build 1's two sub-10k DEVILCASE rows are its tail, not its centre.

---

## Rejected candidates

**Total rejected across three builds: 50 named (11 in build 1, 13 in build 2, 26 in build 3), plus the population-level rejections below.**

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

Of the two RHINOSHIELD creators build 2 left unresolved, build 3 resolved one: `@1982kids` reads **18K** (its roster URL is an `instagram.com/stories/...` form, which is why build 2's handle extraction missed it). `@hanomanga` still returns an `og:description` with no follower substring and stays **unresolved, not rejected**.

### Build 3 rejected: 26 named

**a. From Vein E's handle-less block (5 rejected, 2 accepted as rows 11 and 12, 9 unresolved).**
Build 2 left 21 roster records with no published Instagram. Six are not creators (four RHINOSHIELD in-house theme collections, the 台鋼 baseball-team pair, and Plurk the social network) and are excluded rather than rejected.

| Candidate | Followers | Reason |
|---|---|---|
| MoreMoreToe 墨墨頭 (`@moremoretoe`) | **17K** | Too large. Genuinely a character IP (小毛病怪獸 series), so this is a scale rejection, not a class one |
| Mashpatooties (`@mashpatooties`, Riynn Lee) | **15K** | Too large |
| 草棉谷RONG (`@rong_art`) | **40K** | Too large. `@rongart` - the collection slug read as a handle - is a squat (Dumrong Chaicharoenwut, 48 followers) and would have fabricated a row |
| 木木の口袋 (`@mumu.b3d.pocket`) | **83K** | Too large. Handle came from the LINE STORE API's `authorName` field |
| Quintine (`@quintine1115`) | 641 | **Character not evidenced.** The roster publishes only a Threads URL; the same handle resolves on Instagram. Bio describes a Taichung graphic designer, no character. The lowest count in the file that reaches a real working account |

Nine remain unresolved after handle-guessing, LINE STORE author lookup and the CET join all failed: The Girl, Songprettybell, Chaigo, 棉花糖柴柴與廢貓阿米, 胸毛公寓, Cazador Juanito, **尼胖**, plus 好想兔 (excluded as a licensed property) and `@hanomanga`.
**尼胖 is the most costly of them**: it is the only IP in this run that appears in *both* brand directories (RHINOSHIELD 2026-06-26 and DEVILCASE crossover 276, 2026-01-20), so a resolved band would have produced two rows rather than one.

**b. From the Vein F x Vein A join (23 DEVILCASE partners resolved, 0 accepted).**
All 23 are documented DEVILCASE collaborations with an exact asset-upload date; each is rejected on scale or on identity, none on class.

| Candidate | DEVILCASE id / date | Followers | Reason |
|---|---|---|---|
| 波波與小泡芙 (`@bo_puff_bo`) | 11 / 2026-01-05 | 8,991 | **FALSE MATCH, rejected.** DEVILCASE's partner is 泡芙, a hedgehog whose sibling is 芋泥; the CET exhibitor's pairing is 波波 and 小泡芙. Different IP. The only sub-10k hit the join produced, and it does not survive reading the partner page |
| 小怪家 (`@guaaii__`) | 271 / 2025-12-12 | **10K exactly** | **Boundary-ambiguous, rejected.** Instagram rounds at and above 10,000, so the true value lies somewhere around 9,950-10,499 and the task's "at or under 10,000" cannot be decided. Recorded rather than banded |
| 安怎？Ann-Nua, 牙技師的牙齒們, 其實他是鵝, 青青小樹, 醜白兔, 小水豚豆仔, 小心臟, 伸縮自如的雞與鴨, 加零在電線桿下, 桃源深處有人家, 阿翰, 瘋狂眼珠, 屎蛋唐尼, 消極男子, 87小兔, 空罐王, 軟Q兔兔, 阿啾小劇場, 高雄捷運蜜柑站長, 小學課本的逆襲 (20) | various | 20K - 271K | Too large. Median ~36K |
| 茶包先生 (`@mr.teabag_`) | 308 / 2026-04-29 | 8,288 | Not a rejection - this is **row 1**, and the join independently reproduces build 1's hand-found handle from a second source |

**c. Handle-guessing attempts that failed the name-match rule (build 3 count: 30 candidate handles across 8 IPs).**
Every one resolved to a real account with a follower count and every one was discarded on display name.
Worked examples worth keeping: `@nipangnipang` (0 followers, display name "Nipang" - a squat that *passes* a naive name check and would have produced a 0-follower row), `@marshmallowshiba` (608, "Kira & Levi" - real people's pet account), `@nagi_nagi_` (63, "seyid"), `@chaigo` (4, "kyouhei shimamura"), `@chilittleworld` (2, "YuChi" - one underscore away from the real account at 3,267).

**d. Third-brand probes (2 rejected).**

| Candidate | Reason |
|---|---|
| UNIU (`uniu.com.tw`) | A Shopify storefront, so `collections.json` enumerates the whole catalogue in one request - but its 19 collections are all device/format collections (iPhone 17, MagSafe, AirPods). No artist or 聯名 programme exists |
| Amuse (`creator.amuse.com.tw`) | RHINOSHIELD's creator platform; every Design Studio asset is served from `assets.creator.amuse.com.tw`. `amuse.com.tw` and `www.amuse.com.tw` do not resolve and `creator.amuse.com.tw` serves a JS shell, so whether the platform serves brands other than RHINOSHIELD could not be established |

**Population-level rejection.** Of the 236 partner pages:
**41** are licensed properties or otherwise out of scope (Sanrio's eight characters, Moomin, Garfield, Rilakkuma, Gundam, Monster Hunter, HUNTERxHUNTER, 神魔之塔, 傳說對決, Hatsune Miku, 貓福珊迪, 吉伊卡哇, 卡娜赫拉, 白爛貓, ㄇㄚˊ幾兔, 好想兔, a government mascot, a temple, a car-review channel and similar) and were excluded before any follower work; and **70** sit at ids 1-135, dated only as "on or before 2023-12-04", so they fall outside the task's 2023-2026 window.
That leaves **142 in-scope, in-window partner pages** as the working population.

*(Build 1's arithmetic, kept as written. It is superseded by build 2's category sweep, which found 238 partners rather than 236 and puts the in-scope population at **143** - see `devilcase-categories-and-dates.md`. 143 is the denominator every completeness claim in this file is against.)*

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

### Build 3 additions (all curl-verified 2026-08-07)

| URL | Status | Role |
|---|---|---|
| https://rhinoshield.tw/design-studio/collections/%40chilittleworld | 200 | Row 11 `source_ref` (6 designs) |
| https://rhinoshield.tw/design-studio/collections/%40nagiart | 200 | Row 12 `source_ref` (7 designs) |
| https://www.instagram.com/chi_littleworld/ | 200 | Row 11 follower count (3,267) |
| https://www.instagram.com/oooo_nagixnagi/ | 200 | Row 12 follower count (8,105) |
| https://creativexpo.tw/robots.txt | 200 | Vein F access basis - only four SEO crawlers disallowed |
| https://creativexpo.tw/zh-TW/exhibitor_list | 200 | Vein F index (shows 15 featured only; the directory is reached by id sweep) |
| https://creativexpo.tw/zh-TW/exhibitor_list/1..749 | 200 on 629 | Vein F sweep - 405 publish an Instagram handle |
| https://creativexpo.tw/zh-TW/exhibitor_list/122 | 200 | Row 12 handle source (吶吉與他的搗蛋怪朋友) |
| https://creativexpo.tw/zh-TW/exhibitor_list/20 | 200 | Row 1 handle corroboration from a second source (茶包先生) |
| https://creativexpo.tw/zh-TW/exhibitor_list/129 | 200 | The rejected false match (波波與小泡芙) |
| https://devilcase.com.tw/crossover/11 | 200 | The partner page that refutes it (泡芙 is a hedgehog, sibling 芋泥) |
| https://devilcase.com.tw/crossover/276 | 200 | 尼胖 - the two-directory IP that stays unresolved |
| `store.line.me/api/search/sticker?query=...&country=TW&lang=zh-Hant` | 200, JSON | Vein G - the only CJK-queryable index found |
| https://store.line.me/stickershop/product/33409405/zh-Hant | 200 | LINE product pages are server-rendered (the search page is not) |
| https://store.line.me/stickershop/author/124941/zh-Hant | 200 | LINE author page - carries no social links |
| https://uniu.com.tw/robots.txt, /collections.json | 200 | Third-brand probe - Shopify, but no artist programme |
| https://creator.amuse.com.tw/ | 200 | JS shell; `amuse.com.tw` does not resolve |
| html.duckduckgo.com, lite.duckduckgo.com, tw.search.yahoo.com | **curl exit 000** | Search battery - no HTTP response at all |
| https://www.google.com/search?q=... | 200 but **JS redirect stub** | Search battery - answers, returns no results |
| https://www.mojeek.com/search?q=... | 200 but **zero results** | Search battery |

---

## What build 3 leaves owed

**12 of 25 rows.** The stop condition is not met, but the shape of what remains has changed: the two brand directories are now worked out, and the residue is concentrated in one place.

1. **Vein A's 120 unresolved partners are still the largest single pool, and the handle problem there is now *partly* solved.** The CET map resolves 23 of 143. The remaining 120 are DEVILCASE partners who did not exhibit at 文博會 2026 - and since exhibiting correlates with scale, that residue is *more* likely to be sub-10k than the 23 that resolved, not less. Other CJK name-to-handle directories of the same shape are the way in: earlier 文博會 editions (`2025.creativexpo.tw` exists and is linked from the current site), 原創基地節, 台灣文博會授權專區 exhibitor lists, and Pinkoi's designer directory.
2. **A third brand is still owed, and is now the single highest-value missing thing.** Two licensees, both phone accessories, is a category rather than a market. UNIU and Amuse were probed and closed. The technique that worked twice - find a brand that publishes one page per IP partner, then check *before committing* whether it also publishes the creator's handle - has not yet been run against non-accessory categories (drinkware, stationery, apparel, transit cards, convenience-store campaigns).
3. **The 39 VTubers still need a YouTube/Twitch read.** Unchanged across all three builds. `cate=5` gives the exact list.
4. **尼胖 specifically.** Two documented collaborations, both in window, both dated, blocked only on a handle. Worth a targeted attempt with any new index.
5. **Representability is still asserted, not tested.** Unchanged from build 2, and it now covers ten Vein E rows rather than eight. Every one is marked `representable: yes` on an absence-of-evidence basis - no agent, label or parent is named anywhere in the licensee's own roster record. `creator.amuse.com.tw` remains a JS shell. This must be said out loud on any prospect page that uses these rows.
6. **The 文博會 46.8% figure has 227 unbanded exhibitors behind it.** They publish no Instagram handle on their directory page. If handle-publishing correlates with scale the share moves, and nothing in this run establishes which way.

---

## What build 2 left owed

*(All six items below are discharged or superseded, except where noted.)*

| # | Build 2's owed item | Status after build 3 |
|---|---|---|
| 1 | Vein A handle problem - try a cross-join | **Partly discharged.** Cross-joining the two brand rosters directly was tried and yields almost nothing: they overlap in **3 of 143** partners (好想兔, weiweiboy, 尼胖), of which two publish no handle. The rosters are near-disjoint, which is itself worth knowing - directory *count* matters more than directory size. The CET map (Vein F) is what actually moved it, 23 of 143 |
| 2 | Vein E's 21 handle-less creators and 2 unresolved reads | **Discharged.** All 23 worked through: 2 became rows, 5 rejected, 1 resolved (18K), 6 are not creators, 9 remain unresolved |
| 3 | The 39 VTubers need a YouTube/Twitch read | **Not attempted.** Carried forward |
| 4 | A third brand | **Attempted and failed.** UNIU and Amuse probed and closed; carried forward as the highest-value remaining item |
| 5 | Representability is asserted, not tested | **Not attempted.** Carried forward |
| - | (new) The RHINOSHIELD dating basis | **Corrected.** See the correction notice at the top of this file |

---

## What build 1 left owed

1. **The resolution sweep reached 42 of the 142 in-scope, in-window partner pages, and only 7 of those 42 returned any candidate handle from the automated search** (four more - 茶包先生, 蝦米浣糕, 安怎？, 好吧星期一 - were resolved by hand). So roughly **107 of 142 partner pages are still unbanded**, and each one is a live `lt_10k` candidate. The blocker is search access, not the vein: DuckDuckGo's HTML endpoint answers about ten queries then serves empty result sets permanently, and Brave Search answers reliably at one worker but drops to roughly a 20% hit rate at three concurrent workers. The next build should run **one** worker with a longer delay, and must re-attempt the ids that logged an empty candidate list rather than treating them as resolved.
2. **The 29 VTuber partners need a YouTube/Twitch read**, not an Instagram one, before they can be accepted or rejected. `https://www.youtube.com/@<handle>` yields a subscriber count from the channel-header accessibility label, per the method already used for Fumeancats in `findings/census/taiwan-v2/ip_scale_bands.md`.
3. **Brand diversity.** Both build-1 rows carry the same brand. The rows are real, but a cell that rests on one licensee is thin for a prospect page. Vein D (文創股長 STARup hub) is the best untried source of a *second* brand-side directory, and 蝦米浣糕 x ViewFinder is a live lead into apparel.
4. **Ids 1-135 are undated.** If the 2023 slice matters, they need a second dating source - DEVILCASE's own Facebook/Instagram launch posts are the obvious candidate.
