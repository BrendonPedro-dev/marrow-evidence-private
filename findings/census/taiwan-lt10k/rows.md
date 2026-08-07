# Taiwan x `lt_10k` independent collaborations - verified rows

Task: `tasks/tw-lt10k-independent.md`.
Goal: documented brand collaborations in Taiwan, 2023-2026, where the partner IP is an INDEPENDENT (or MIXED) character that stood at or under 10,000 followers.
The ten-market census (`findings/census/taiwan-v2/ip_scale_bands.md`) holds **zero** `lt_10k` Taiwan rows at whole-row level - the single `lt_10k` reading in that file is a per-creator sub-band inside two-creator row 76 (臺灣印事).
This file is the dedicated hunt for the missing cell.

**Status: in progress.
Build 4 of the run - 20 verified rows of a 25-row stop condition.
Retrieval date for everything below: 2026-08-07.**

> **Build 4 headline.** The two brand-directory veins were worked out, so build 4 went looking for a third brand and found the wrong thing in the right place.
> The 文博會 organiser publishes its own **異業合作** (cross-industry partnership) section - a curated list of who partnered with whom, written by the party that brokered the deals.
> That section is a *collaboration* index, not an exhibitor index, and it is what builds 1-3 were missing: Vein F told you who a creator is, Vein G tells you who they signed with.
> It led directly to **7-ELEVEN's ibon 雲端列印 x 16 新銳創作者** (140+ licensed SKUs across 7,300 stores), of which **12 are sub-10k** - the single largest concentration of sub-10k Taiwanese licensing found anywhere in this run.

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
| **F2. Creative Expo Taiwan 2025 exhibitor directory** `2025.creativexpo.tw/zh-TW/brands/<id>` | The previous edition of the same directory, on a **different path shape** (`brands`, not `exhibitor_list`) | **WORKS, and extends the dictionary.** ids 1-759 → **449 real brand pages, 378 publishing an Instagram handle**. Adds 23 new handle resolutions to Vein A that the 2026 edition did not carry. Full map: `cet2025-exhibitor-handle-map.md`. Editions 2022-2024 do not resolve by DNS |
| **G. Creative Expo Taiwan 異業合作 sections** `creativexpo.tw` and `2025.creativexpo.tw` `/zh-TW/collaboration_responses/<id>` | The organiser's own writeup of every cross-industry partnership it brokered for that edition - hotel, transit, mall, beverage, print, scooter-share | **WORKS, and is a genuine row source - the first non-brand-directory one in this run.** 18 entries on the 2026 site, 12 on the 2025 site. Unlike Veins A/E/F this is an index of *collaborations*, so a hit is a row candidate rather than a name lookup. Produced rows 13-20 directly or by pointing at them. Full corpus: `cet-cross-industry-collaborations.md` |
| **H. 7-ELEVEN / ibon 雲端列印 x 文博會 特印企劃** | Convenience-store cloud-print service; 140+ licensed print SKUs from 16 named 新銳 creators, sold in 7,300 stores | **WORKS, and is the richest single collaboration in the file.** 12 of the 16 named creators are sub-10k and 7 clear the character test. `print.ibon.com.tw` itself is a JS shell whose API is `robots.txt`-disallowed, so the creator list came from the trade press, not the brand |

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

### 10. Vein G - the organiser's own 異業合作 list, which is a collaboration index rather than a name index (build 4)

Build 3 left "a third brand" as the highest-value owed item and build 4 opened by hunting one directly.
That failed, and it is worth recording how completely, because the failure is what forced the better move.
Fourteen candidate Taiwanese consumer brands were probed by domain for the DEVILCASE/RHINOSHIELD shape (a live page per IP partner): `telephant.tw`, `www.telephant.com.tw`, `shop.easycard.com.tw`, `www.kuaikuai.com.tw`, `www.csdmask.com.tw`, `www.stayreal.com.tw`, `www.apbs.com.tw`, `www.umade.com.tw`, `www.aholic.com.tw`, `www.iamzoe.com.tw`, `www.grandtechshop.com.tw`, `www.wemoji.com.tw` and `www.mageasy.com` all fail DNS or connection from here; `www.candies.tw` 404s; `www.jeantopia.com` resolves to a squatted domain serving Chinese SEO spam.
Of the ones that answered, `switcheasy.com` (MAGEASY's parent, Shopify) has **261 collections and not one artist collection**; `www.mageasy.com.tw` serves a one-URL sitemap pointing at `/lander`; `www.zeczec.com` and `www.feds.com.tw` and `meet.eslite.com` 403.
**Blind brand-domain guessing is not a method.** It cost a sixth of the build and returned nothing.

What worked instead was noticing that the directory build 3 had already opened publishes a **second, differently-shaped section**:

```
https://creativexpo.tw/zh-TW/collaboration_responses/<id>          (2026 edition, 18 entries)
https://2025.creativexpo.tw/zh-TW/collaboration_responses/<id>     (2025 edition, 12 entries)
```

This is the 文博會 organiser writing up, in its own words, every cross-industry partnership it brokered that year: a hotel, a metro operator, an airline, a mall, four beverage brands, a scooter-share operator, a bookstore chain, a printing service, a department store.
The distinction that matters: **Vein F is an index of people, Vein G is an index of deals.** An exhibitor page tells you who a creator is; a 異業合作 page tells you who they signed with, when, and for what product. That is a row, not a lookup.

Method, and it is short:

1. Sweep `collaboration_responses/1..70` on both hosts, keeping only pages whose final URL id matches the requested id (both apps 302 unknown ids to a curation page, so an unchecked sweep returns hundreds of duplicates - the 2025 `brands` sweep returned 759 "pages" of which **310 were one redirect target repeated**).
2. Strip the page chrome and read the body. Every entry names its counterparties in prose.
3. Cross-reference each named creator against the Vein F/F2 handle dictionaries to band them.
4. Adjudicate on class and on collaboration type before accepting.

Both editions' full text and the per-entry adjudication are in `cet-cross-industry-collaborations.md`.

**Two adjudications this vein forces that no earlier vein did.**

*Collaboration type.* Not everything in a 異業合作 list is an IP licence. The 2026 LINE 貼圖 entry (`collaboration_responses/36`) names 鼠粒控 (3,934) and 茶包先生 (8,288) in a 「文博創作專區」 - but LINE is hosting the creators' own self-published stickers in a promotional zone, not applying their IP to a LINE product. That is platform promotion, and it is **rejected** here even though both creators are in band and would each have made a row. Same call on the 2026 opening-ceremony line-up (`posts/38`), where 糙灰搭的獨角獸 (9,514) opened the doors as a costumed character: an appearance is not a collaboration.

*Already-censused rows.* The 2025 entry `collaboration_responses/18` is 南港老爺行旅 x 臺灣印事 + 腋毛人 - which is **already census row 76**, the very row this file's header cites as the census's only `lt_10k` reading. It is not added again. What it does do is discharge that row's `single source - flagged` caveat: the census had one ETtoday article, and this is the organiser's own primary account of the same deal, naming both IPs.

### 11. Vein H - 7-ELEVEN / ibon, reached through the trade press because the brand's own surface is closed (build 4)

The 2026 品牌商展 opening release (`https://creativexpo.tw/zh-TW/posts/38`) contains one clause that is worth more than the rest of the vein: 「ibon雲端列印再度攜手文博會，邀集16位新銳創作者推出超過140款原創授權商品」.

`print.ibon.com.tw` cannot be read: it serves an 8.5 KB JavaScript shell and its `robots.txt` disallows `/api/`, which is where the catalogue lives. That path was not taken.
The creator list came from the trade press instead, and the route to it is reusable:

1. `https://news.google.com/rss/search?q=<urlencoded>&hl=zh-TW&gl=TW&ceid=TW:zh-Hant` **answers over plain curl with HTTP 200 and 40-70 real results per query** - the first working general search index any build in this run has had. Ten discovery queries returned 475 distinct headlines.
2. Its article links are `news.google.com/rss/articles/...` and do **not** redirect (200, no `Location`), so the headline plus the `<source>` outlet is all you get.
3. Resolve the headline against the outlet directly. 中華日報 `www.cdns.com.tw` runs WordPress with an **open WP-REST endpoint**: `wp-json/wp/v2/posts?search=<q>` finds the article and `wp-json/wp/v2/posts/<id>` returns the clean body text, which the rendered page does not (the article HTML inlines the whole theme stylesheet into the content div).

The article - `https://www.cdns.com.tw/articles/1429446`, 2026-07-14, HTTP 200 - names all 16 creators and the deal terms: two waves from 2026-07-08 and 2026-07-15, running to 2026-08-31, 140+ SKUs across postcards, sticker sheets, name labels, card skins and timetables, printable in 7,300+ 7-ELEVEN stores, explicitly 「原創授權周邊商品」.

15 of the 16 resolve against the Vein F dictionary; only 木子島工作室 does not appear in either edition of the exhibitor directory and is unresolved.

| # | creator | Instagram | followers | band | character test |
|---|---|---|---|---|---|
| 1 | 洋樓拾憶文創工作室 | `@quemoy_memory` | **386** | `lt_10k` | fail - Kinmen heritage design collective, no character |
| 2 | 魚氏 | `@yulin.ovo` | **1,170** | `lt_10k` | fail - watercolour illustration brand, "original IP" claimed but no character named |
| 3 | 張哲 | `@changche.drawing` | **1,608** | `lt_10k` | fail - oil-pastel painter, image licensing, no character |
| 4 | SPARK的行動計畫 | `@actionplan24` | **2,144** | `lt_10k` | **pass** - 「以原創角色 SPARK 為核心」 |
| 5 | 虎嚕吼嚕嚕 | `@hooru.horuru` | **3,078** | `lt_10k` | **pass** - 黑色虎爺「虎嚕 HOORU」, self-described "original character IP" |
| 6 | 羊號角Piper | `@piper.illu` | **3,604** | `lt_10k` | fail - fantasy/nature illustration, no character |
| 7 | 鼠粒控 | `@3co_studio_` | **3,934** | `lt_10k` | **pass** - mouse cast, 「老鼠會」 |
| 8 | 兩顆糖製造機 | `@2sugarstudio` | **4,049** | `lt_10k` | **pass** - 棉花糖鱷魚「齁咪呀」, 鴨嘴獸「巴拉王子」 |
| 9 | 灰黑集白 | `@aasta_blacknwhite` | **4,443** | `lt_10k` | **pass** - 黑貓「馬路」Maru |
| 10 | 吉文考古 | `@apa0824` | **6,951** | `lt_10k` | **pass** - 「把傳統祝福變成可愛角色」, 神奇吉獸 |
| 11 | 日句時刻所 | `@heyyoumoment` | **7,493** | `lt_10k` | fail - yellow-themed lifestyle illustration, no character |
| 12 | ATW studio | `@atw_studio` | **8,116** | `lt_10k` | **pass** - 「以怪噗&飛克視角」, two named characters |
| 13 | 摘星小宇宙 | `@little.__.sparkles` | 14,000 | `10k_50k` | out of band |
| 14 | 簡莘蒂 | `@cindychien_studio` | 16,000 | `10k_50k` | out of band |
| 15 | 嘎嘎雞 | `@gaga_g_scream_chicken` | 19,000 | `10k_50k` | out of band |
| 16 | 木子島工作室 | - | - | - | unresolved - in neither CET edition |

**12 of 16 named creators are sub-10k; 7 of those clear the character test and become rows 14-20.**
Every count above is a live Instagram `og:description` read on 2026-08-07 against the handle the exhibitor publishes on their own 文博會 page, and every display name carries the IP's own name, so the handle-squat guard is satisfied twice over.

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

**Row 13, from Vein G.** A second brand for an IP this file already carries, which is the first time any IP in the file has two independent licensees.

| # | brand_name | ip_name | market | year | year basis | source_ref | follower_band | count seen | representable | ip_class | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 13 | 南港老爺行旅 Hotel Royal Nikko Nangang | NAGI x NAGI 吶吉 (兔人 / 鳥人 / 貓人) | TW | 2026 | Organiser page dated **2026-08-03**; the offer itself runs 即日起至 11/30 and the trade press announced it 2026-07-27. No inference needed | https://creativexpo.tw/zh-TW/collaboration_responses/34 (HTTP 200, 2026-08-07) | `lt_10k` | **8,105** Instagram followers, `@oooo_nagixnagi`, display name NAGIxNAGI!!!吶吉和他的搗蛋怪朋友｜IP雜貨, read 2026-08-07 | yes | INDEPENDENT | A styled guest room built around the IP, NT$5,800 per night for two, running to 2026-11-30. **The same creator as row 12** (RHINOSHIELD), so this file now has one IP with two unrelated licensees in two unrelated categories - phone accessories and hospitality - which is the first direct evidence in the run that a sub-10k Taiwanese IP can hold more than one deal at a time. The organiser's own copy names the three characters (「兔人」「鳥人」與「貓人」) and calls NAGI 「來自臺灣的插畫創作者」, so the character test and the independence test are both carried by the source rather than inferred. The room's co-headliner, 泰江 TJ GAMEBOY, is rejected - see Rejected candidates |

**Rows 14-20: 7 verified rows from Vein H**, the 7-ELEVEN / ibon 雲端列印 x 2026 臺灣文博會 「第零位元」 特印企劃.

For every row below: `brand_name` = **7-ELEVEN 統一超商 (ibon 雲端列印)**, `market` = TW, `year` = **2026**, `ip_class` = INDEPENDENT, `representable` = yes.
`source_ref` = `https://www.cdns.com.tw/articles/1429446` (中華日報, 2026-07-14, HTTP 200 verified 2026-08-07) - the trade-press release that names all sixteen creators and the deal terms.
`year` basis is the same on all seven and needs no inference: the article states the two release waves as **2026-07-08 and 2026-07-15**, running to 2026-08-31.
Each row's second source is that creator's own 文博會 exhibitor page, which is where the Instagram handle and the character claim come from; all thirteen exhibitor pages touched were curl-verified 200 on 2026-08-07.
Follower counts are live Instagram `og:description` reads on 2026-08-07 - a `current-proxy` gap of about one month, the shortest in the file.

| # | ip_name | source_ref (secondary - exhibitor page) | follower_band | count seen | representable | notes |
|---|---|---|---|---|---|---|
| 14 | SPARK的行動計畫 (SPARK) | https://creativexpo.tw/zh-TW/exhibitor_list/42 | `lt_10k` | **2,144**, `@actionplan24`, display name SPARK的行動計畫 | yes | The cleanest single-character row in the file: the brand's own line is 「行動計畫有限公司以原創角色 SPARK 為核心」 - one company, one owned character, stated in that order. Incorporated as 行動計畫有限公司, so creator-owned but not a sole trader |
| 15 | 虎嚕吼嚕嚕 HOORU HORURU | https://creativexpo.tw/zh-TW/exhibitor_list/79 | `lt_10k` | **3,078**, `@hooru.horuru`, display name 虎嚕吼嚕嚕 HOORU HORURU | yes | The only row in the file whose own description uses the phrase **"original character IP"** unprompted. 黑色虎爺「虎嚕」 born at 嘉義城隍廟 - a folk-religion character, i.e. exactly the kind of locally-rooted small IP the census's press sources never reach. 25 posts and 4 accounts followed: a very new account, which makes the current-proxy read close to the at-campaign figure |
| 16 | 鼠粒控 / 3co Studio | https://creativexpo.tw/zh-TW/exhibitor_list/133 | `lt_10k` | **3,934**, `@3co_studio_`, display name 鼠粒控 / 3co Studio | yes | A cast of round, expressive mice organised as a mock 「老鼠會」 (a pun on Taiwan's word for a pyramid scheme). Independently named in a second 2026 collaboration - LINE 貼圖's 文博創作專區 - which is **rejected** as platform promotion rather than licensing, so this creator has one accepted row and one logged rejection |
| 17 | 兩顆糖製造機 2SugarStudio (齁咪呀 / 巴拉王子) | https://creativexpo.tw/zh-TW/exhibitor_list/268 | `lt_10k` | **4,049**, `@2sugarstudio`, display name 兩顆糖製造機 | yes | Two named characters with species and role: 棉花糖鱷魚「齁咪呀」 and 鴨嘴獸「巴拉王子」. Works in resin and sofubi, i.e. an art-toy maker whose IP has now been licensed into a print format - a genuine category jump for a 4K-follower creator |
| 18 | 灰黑集白 / 黑貓馬路 Maru | https://creativexpo.tw/zh-TW/exhibitor_list/134 | `lt_10k` | **4,443**, `@aasta_blacknwhite`, display name 灰黑集白｜黑貓馬路 Maru | yes | **Same IP as row 4, different licensee.** Row 4 is RHINOSHIELD; this is 7-ELEVEN. The creator's own 文博會 line cites the RHINOSHIELD deal as a credential (「具備犀牛盾聯名與空間展陳實績」), which is the first case in this file of one accepted row being used by the creator to win the next - a documented licensing ladder inside the sub-10k band |
| 19 | 吉文考古 Auspicious Pattern Archeology | https://creativexpo.tw/zh-TW/exhibitor_list/293 | `lt_10k` | **6,951**, `@apa0824`, display name 吉文考古｜插畫｜平面設計｜圖像授權 | yes | Twin creators turning Taiwanese auspicious motifs into 「可愛角色與故事」 with a named world (吉地探險) and a named creature class (吉獸). The account's own bio ends in **圖像授權** - the creator advertises image licensing as a service, which is about as direct an addressability signal as this file contains |
| 20 | ATW STUDIO (怪噗 Guaipu / 飛克 Faker) | https://creativexpo.tw/zh-TW/exhibitor_list/347 | `lt_10k` | **8,116**, `@atw_studio`, display name ATW studio | yes | Two named characters, 怪噗 and 飛克, described as the perspectives the work is made through. The largest of the seven and the closest to the 10,000 boundary, but not close enough to be ambiguous under the rounding rule (Instagram serves an exact figure below 10,000) |

**Read on the twenty rows.** Build 1 could say the cell exists.
Build 2 could say what it looks like: a second Taiwanese-market licensee, larger and better documented, landing eight more sub-10k character deals, one of them running 48 SKUs.
Build 3 closes Vein E (every record parsed, every resolvable handle resolved), corrects the dating basis, and adds the two rows that were hiding behind the handle gap - one of them only reachable by cross-referencing a second directory.
Build 4 breaks the shape of the answer rather than extending it: **four brands, twenty rows**, and the two new brands are not phone-case makers.
One is a hotel and one is the largest convenience-store chain in Taiwan, which is the point - builds 1-3 could be read as "print-on-demand accessory brands will licence anyone", and rows 13-20 are not that.
The census's zero was a property of press indexing, and that is now shown four ways: two brand rosters, a trade-show floor, and an organiser-published list of brokered deals.

**Three things rows 13-20 establish that rows 1-12 could not.**

1. **A sub-10k IP can hold two licences at once.** 灰黑集白 (4,443) appears as row 4 with RHINOSHIELD and row 18 with 7-ELEVEN; 吶吉 (8,105) appears as row 12 with RHINOSHIELD and row 13 with a hotel. Two of the file's twenty rows are repeat business by the same creator with an unrelated licensee, and in 灰黑集白's case the creator's own 文博會 copy cites the first deal to sell the next.
2. **The formats are not token.** 140+ SKUs across 7,300 stores is national convenience-store distribution, and the hotel row is a room sold at NT$5,800 a night for four months. The census's Taiwan rows at this scale do not exist, but not because the deals are small.
3. **The channel is brokered.** Every one of rows 13-20 traces back to the same intermediary - the 文博會 organiser (台灣設計研究院 / 文化部) - which brokered the hotel deal, the mall deal, the scooter deal and the 7-ELEVEN deal. That is a *mechanism*, not just a source: for sub-10k Taiwanese IP, the route to a national brand runs through a state-backed trade show rather than through the brand's inbound channel.

**The population statistics, which may matter more than the rows.** There are now three exactly-known Taiwanese denominators, one of them a *deal* population rather than a roster.

| population | n | sub-10k | share |
|---|---|---|---|
| RHINOSHIELD Design Studio creators with a resolved follower count (a **licensing roster**) | 160 | 21 | **13.1%** |
| Creative Expo Taiwan 2026 exhibitors with a resolved follower count (a **trade-show floor**) | 402 | 188 | **46.8%** |
| DEVILCASE Taiwanese/overseas-character partners resolvable via the CET map (a **licensing roster**) | 23 | 0 | **0%** (one at exactly 10K) |
| **7-ELEVEN / ibon x 文博會 2026 licensed creators** (a **single brand's actual signed cohort**) | 16 | **12** | **75%** |
| the ten-market census, Taiwan (**press-built**) | - | 0 | **0%** |

**The 75% is the most consequential number in this file.** The other denominators measure who is *available* to be licensed; this one measures who a specific national brand *actually signed*, and three quarters of them were sub-10k. It is one deal and it was explicitly framed as a 新銳 (emerging-talent) programme, so it is not a general estimate of 7-ELEVEN's licensing - but it is a direct counter-example to the reading that sub-10k IP is not commercially licensable in Taiwan, and it is exactly denominated.

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

**Total rejected across four builds: 73 named (11 in build 1, 13 in build 2, 26 in build 3, 23 in build 4), plus the population-level rejections below.**

### Build 4 rejected: 23 named

**From Vein H (7-ELEVEN / ibon), all sixteen creators adjudicated, 9 rejected.** Five are in band and fail the character test - the same split build 2 found on RHINOSHIELD, and at almost the same rate.

| Candidate | Followers | Reason |
|---|---|---|
| 洋樓拾憶文創工作室 `@quemoy_memory` | **386** | In band, fails class. A Kinmen 洋樓 heritage-design collective - 「用設計，讓世界看見金門」. Same shape as build 2's heritage-temple rejection: a real independent licensor, not a character IP. The smallest follower count seen anywhere in this run |
| 魚氏 `@yulin.ovo` | **1,170** | In band, fails class - **the closest call in the file.** The English copy says "Our work spans illustrations, original IP, and product design", so the creator claims an IP, but no character is named anywhere on the page. Recorded as a rejection under the standing rule (the source must name the character), and flagged here because a looser rule would make it row 21 |
| 張哲 `@changche.drawing` | **1,608** | In band, fails class. Oil-pastel painter; the page describes image licensing and commissions, no character |
| 羊號角Piper `@piper.illu` | **3,604** | In band, fails class. Fantasy/nature illustration; forests and magic, no named character |
| 日句時刻所 `@heyyoumoment` | **7,493** | In band, fails class. A yellow-themed stationery and homeware illustration brand; the theme is a colour, not a character |
| 摘星小宇宙 `@little.__.sparkles` | 14,000 | Out of band |
| 簡莘蒂 `@cindychien_studio` | 16,000 | Out of band |
| 嘎嘎雞 `@gaga_g_scream_chicken` | 19,000 | Out of band |
| 木子島工作室 | unresolved | Named in the 7-ELEVEN release but present in neither the 2025 nor the 2026 文博會 exhibitor directory, and no other index reached it. Owed to a later build - it is a live `lt_10k` candidate, not a negative |

**From Vein G, rejected on collaboration type rather than on scale or class.** These are the ones that would have been rows under a looser definition, and each is named so the call can be reversed by a human.

| Candidate | Where | Followers | Reason |
|---|---|---|---|
| 鼠粒控 x LINE 貼圖 | `collaboration_responses/36` | 3,934 | **Platform promotion, not licensing.** LINE hosted the creators' own self-published stickers in a 「文博創作專區」; the IP was not applied to a LINE product. The same creator's 7-ELEVEN deal *is* a row (row 16), which is what makes the distinction concrete rather than pedantic |
| 茶包先生 x LINE 貼圖 | `collaboration_responses/36` | 8,288 | Same call. Already row 1 on a different brand |
| ㄅㄅㄐ x LINE 貼圖 | `collaboration_responses/36` | 18,000 | Out of band as well |
| 糙灰搭的獨角獸 | `posts/38` | 9,514 | **An appearance is not a collaboration.** Opened the 2026 品牌商展 doors as a costumed character alongside 變種吉娃娃 and 可愛大王. In band and would otherwise be a strong candidate |
| 泰江 TJ GAMEBOY x 南港老爺行旅 | `collaboration_responses/34` | unresolved | Co-headliner of the same hotel programme as row 13. Fails class on the organiser's own description - 「以『文字之美 × 當代語言文化』為創作核心」, typographic reinterpretation of memes and puns, no character. Handle also unresolved: not in either CET edition, and `@tjgameboy` / `@tj_gameboy` are both empty squats (0 followers), which is the handle-squat trap presenting itself again |
| 臺灣印事 x 南港老爺行旅 (2025) | `2025 collaboration_responses/18` | 5,785 | **In band, but already census row 76** - the single `lt_10k` reading this file's header cites. Not double-counted. Its value here is that it discharges that row's `single source - flagged` caveat with the organiser's own primary account |
| 腋毛人 Yemao x 南港老爺行旅 (2025) | `2025 collaboration_responses/18` | 26,000 | Out of band; the other half of census row 76 |
| BIBI波波 x 大苑子 | `2025 collaboration_responses/19` | **12,000** | Out of band by 2,000. A genuine national drinks-chain licence (limited cup design 〈夏日水果樂園〉, all TW stores from 2025-07-31) and the nearest miss in the file. Worth carrying forward as evidence of the format |
| 咚東 x 有記名茶 | `2025 collaboration_responses/19` | 16,000 | Out of band. 小恐龍茶盒 with a 百年茶行 - another format that would matter if the creator were smaller |
| 毛絨絨星人 x WeMo | `collaboration_responses/35` | 374,000 | Out of band, despite the organiser describing them as 「療癒系文創新秀」 - a reminder that "emerging" in Taiwanese trade copy is not a scale claim |
| 駝背人 x WeMo | `collaboration_responses/35` | 66,000 | Out of band |
| 貓貓蟲咖波 x WeMo | `collaboration_responses/35` | 2,000,000 | Out of band |
| 咕咕嘎嘎 x LaLaport 南港 | `collaboration_responses/32` | 25,000 | Out of band |
| 咻熊家 x LaLaport 南港 | `collaboration_responses/32` | 111,000 | Out of band |
| 美可女子 x LaLaport 南港 | `collaboration_responses/32` | 16,000 | Out of band |
| 凱西.陳 x LaLaport 南港 | `collaboration_responses/32` | unresolved | CET2026 exhibitor 1 publishes Facebook only (`Macaoillustrator`), no Instagram, so no band. Unresolved rather than rejected |
| 皮皮家族 x 文博會 (饅頭燒雞蛋糕) | `2025 collaboration_responses/20` | 9,000,000 | Out of band |
| 捷米 JAMIE x 台北捷運 | `collaboration_responses/31` | 1,769 | **In band and rejected on ownership.** JAMIE is Taipei Metro's own in-house mascot - the brand and the IP are the same party, so there is no licensing relationship to record. A corporate mascot is not independent IP however small its account |

**From Vein A (DEVILCASE) via the new 2025 dictionary, 23 partners newly resolved, 1 in band, 1 rejected.**

| Candidate | Followers | Reason |
|---|---|---|
| 風速新營 XYWS (crossover 166, 2024-12-12) | **6,011** | In band, fails class. Both the DEVILCASE partner page and the creator's own 文博會 page describe an 「插畫雙人組」 named after their hometown 新營 with no character: 「以寶山家鄉地名為起點，畫出迎風而來的自由感」. The only sub-10k hit in 23 newly resolved DEVILCASE partners |

The other 22 resolved between 16K and 271K and are simply out of band: 小學課本的逆襲 271K, 阿啾小劇場 227K, 蜜柑站長 235K, 啾啾噗噗 168K, 消極男子 133K, dtto friends 115K, YUANCHi 114K, 肥肥與阿胡 92K, 阿翰 58K, 加零在電線桿下 42K, 阿軒與一隻灰塵 40K, 河童卡斯柏 40K, 伸縮自如的雞與鴨 36K, 小心臟 35K, YuYing 28K, 青青小樹 27K, 其實他是鵝 22K, 牙技師的牙齒們 22K, 安怎？ 20K, 來碗寬片片 16K.
小怪家 stays boundary-ambiguous: the 2025 directory publishes `@yiekubo` for it, which serves no `og:description` at all, so build 3's 10K reading on `@guaaii__` still governs.

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
| `store.line.me/api/search/sticker?query=...&country=TW&lang=zh-Hant` | 200, JSON | Method section 9 - the only CJK-queryable index found by build 3 |
| https://store.line.me/stickershop/product/33409405/zh-Hant | 200 | LINE product pages are server-rendered (the search page is not) |
| https://store.line.me/stickershop/author/124941/zh-Hant | 200 | LINE author page - carries no social links |
| https://uniu.com.tw/robots.txt, /collections.json | 200 | Third-brand probe - Shopify, but no artist programme |
| https://creator.amuse.com.tw/ | 200 | JS shell; `amuse.com.tw` does not resolve |
| html.duckduckgo.com, lite.duckduckgo.com, tw.search.yahoo.com | **curl exit 000** | Search battery - no HTTP response at all |
| https://www.google.com/search?q=... | 200 but **JS redirect stub** | Search battery - answers, returns no results |
| https://www.mojeek.com/search?q=... | 200 but **zero results** | Search battery |

### Build 4 additions (all curl-verified 2026-08-07)

**Row sources.**

| URL | HTTP | What it establishes |
|---|---|---|
| https://www.cdns.com.tw/articles/1429446 | **200** | `source_ref` for rows 14-20. 中華日報 2026-07-14: names all 16 ibon creators, both release waves, 140+ SKUs, 7,300 stores, 「原創授權周邊商品」 |
| https://www.cdns.com.tw/wp-json/wp/v2/posts?search=... | 200, JSON | How that article was found and read - open WP-REST search plus clean body text |
| https://creativexpo.tw/zh-TW/collaboration_responses/34 | **200** | `source_ref` for row 13. Names NAGI×NAGI, the three characters, the room, the price and the run dates |
| https://creativexpo.tw/zh-TW/exhibitor_list/42 | **200** | Row 14 - handle `@actionplan24` and the SPARK character claim |
| https://creativexpo.tw/zh-TW/exhibitor_list/79 | **200** | Row 15 - handle `@hooru.horuru`, "original character IP" |
| https://creativexpo.tw/zh-TW/exhibitor_list/133 | **200** | Row 16 - handle `@3co_studio_` |
| https://creativexpo.tw/zh-TW/exhibitor_list/268 | **200** | Row 17 - handle `@2sugarstudio`, 齁咪呀 / 巴拉王子 |
| https://creativexpo.tw/zh-TW/exhibitor_list/134 | **200** | Row 18 - handle `@aasta_blacknwhite`; also the creator's own citation of the RHINOSHIELD deal |
| https://creativexpo.tw/zh-TW/exhibitor_list/293 | **200** | Row 19 - handle `@apa0824` |
| https://creativexpo.tw/zh-TW/exhibitor_list/347 | **200** | Row 20 - handle `@atw_studio`, 怪噗 / 飛克 |
| https://creativexpo.tw/zh-TW/exhibitor_list/122 | **200** | Row 13 - handle `@oooo_nagixnagi` (also row 12's) |
| https://www.instagram.com/{atw_studio, aasta_blacknwhite, actionplan24, 2sugarstudio, 3co_studio_, apa0824, hooru.horuru, oooo_nagixnagi}/ | **200 each** | The eight live follower reads behind rows 13-20 |

**Rejection sources.**

| URL | HTTP | What it establishes |
|---|---|---|
| https://creativexpo.tw/zh-TW/collaboration_responses/36 | 200 | The LINE 貼圖 entry rejected on collaboration type |
| https://creativexpo.tw/zh-TW/collaboration_responses/35 | 200 | WeMo x 咖波 / 毛絨絨星人 / 駝背人 - all out of band |
| https://creativexpo.tw/zh-TW/collaboration_responses/32 | 200 | LaLaport 南港 x 4 creators - all out of band or unresolved |
| https://creativexpo.tw/zh-TW/collaboration_responses/31 | 200 | 台北捷運 捷米 JAMIE - in band, rejected on ownership |
| https://2025.creativexpo.tw/zh-TW/collaboration_responses/18 | 200 | 南港老爺行旅 x 臺灣印事 + 腋毛人 - the primary source that discharges census row 76's single-source flag |
| https://2025.creativexpo.tw/zh-TW/collaboration_responses/19 | 200 | 大苑子 x BIBI波波 and 有記名茶 x 咚東 - the two nearest misses |
| https://creativexpo.tw/zh-TW/exhibitor_list/{86,238,440,313,418} | 200 each | The five in-band ibon creators rejected on the character test |
| https://2025.creativexpo.tw/zh-TW/brands/48 | 200 | 風速新營 XYWS - the sole sub-10k DEVILCASE hit, rejected on class |
| https://devilcase.com.tw/crossover/166 | 200 | Its DEVILCASE partner page, which corroborates the "illustrator duo, no character" reading |

**Vein and index infrastructure.**

| URL | HTTP | Note |
|---|---|---|
| https://2025.creativexpo.tw/robots.txt | 200 | Disallows only SemrushBot, MJ12bot, AhrefsBot, DotBot; `User-agent: * / Allow: /` |
| https://2025.creativexpo.tw/zh-TW/brands/1..759 | 200 on 449 real | Vein F2 sweep; **310 further ids 302 to one curation page and 41 to the index** - the redirect trap |
| https://{2024,2023,2022}.creativexpo.tw/ | **curl exit 000** | Earlier editions do not resolve by DNS. The dictionary stops at two editions |
| https://creativexpo.tw/zh-TW/collaboration_responses/1..70 | 200 on 18 | Vein G, 2026 edition |
| https://2025.creativexpo.tw/zh-TW/collaboration_responses/1..70 | 200 on 12 | Vein G, 2025 edition |
| https://creativexpo.tw/zh-TW/posts/38 | 200 | The 品牌商展 opening release that names the ibon deal, the NeverHaveIEver New York deal and the LaLaport deal |
| `https://news.google.com/rss/search?q=<q>&hl=zh-TW&gl=TW&ceid=TW:zh-Hant` | **200, 40-70 items** | **The first working general search index in this run.** 10 queries → 475 distinct headlines |
| `https://news.google.com/rss/articles/CBMi...` | 200, **no redirect** | Google News article links do not resolve to the publisher. Title-plus-outlet is all you get |
| https://print.ibon.com.tw/ | 200 but **8.5 KB JS shell** | Vein H's brand surface is unreadable; `robots.txt` disallows `/api/`, so it was not used |
| https://switcheasy.com/sitemap_collections_1.xml | 200 | Third-brand probe - **261 collections, zero artist collections** |
| https://www.mageasy.com.tw/sitemap.xml | 200 | Third-brand probe - one URL, `/lander` |
| https://www.jeantopia.com/ | 200 | Third-brand probe - **squatted domain serving Chinese SEO spam**, not the Wooderful life brand |
| telephant.tw, www.telephant.com.tw, shop.easycard.com.tw, www.kuaikuai.com.tw, www.csdmask.com.tw, www.stayreal.com.tw, www.apbs.com.tw, www.umade.com.tw, www.aholic.com.tw, www.iamzoe.com.tw, www.grandtechshop.com.tw, www.wemoji.com.tw, www.mageasy.com | **curl exit 000** | Third-brand probes - DNS or connection failure |
| www.candies.tw | 404 | Third-brand probe |
| www.zeczec.com, www.feds.com.tw, meet.eslite.com | 403 | 募資 platform and two department stores - closed to plain curl |
| searx.be/search?format=json | 200 but **anti-bot challenge** | Search battery re-test; `startpage`, `brave` (429), `mojeek` (0 results), `yandex` (302) all still closed |

---

## What build 4 leaves owed

**20 of 25 rows.** Five short, and for the first time the shortfall is not a discovery problem - build 4 found more in-band candidates than it could accept, and the binding constraint is the character test.

1. **Vein G is not exhausted, it is barely started.** Only two editions of one trade show were swept, and only its `collaboration_responses` and `posts` sections. Untried on the same two hosts: `events` (68 + 82 entries, swept but only keyword-scanned, not read), `online_events`, `taicca_curations`, `kuroshio_ips` (the 黑潮星樂園 original-IP zone, 15 entries on the 2026 site and a separate id block on the 2025 one). Two named 2026 deals inside Vein G were seen and not worked: **NeverHaveIEver x 10 組臺灣原創IP** into the New York Shoppe Object show, and the **2025 edition of the same ibon programme** ("去年首次與臺灣文博會合作"), whose creator list was not found - a whole second cohort of the vein that produced seven rows.
2. **Other organisers publish the same section.** The generalisation is not "文博會 has a 異業合作 page", it is "an event organiser that brokers deals publishes who signed". 原創基地節, 台北國際動漫節, 高雄設計節, 新一代設計展 and the 文策院 (TAICCA) programme pages are all untried and all the same shape.
3. **木子島工作室 specifically.** Named in a national convenience-store licensing deal, in window, and absent from both CET editions. One handle away from being row 21.
4. **The 12-of-16 ibon cohort is one deal, and the 75% wants a second data point.** If the 2025 ibon cohort resolves, the two together make a real time series on one brand's emerging-talent licensing - and if the share holds, that is a much stronger claim than a single year.
5. **Vein A's ~97 unresolved partners.** The 2025 dictionary took 23 more of the 143, leaving roughly 97. The evidence now says this pool is not worth much for `lt_10k` (46 DEVILCASE partners resolved across two builds, exactly one sub-10k, and that one failed the character test) - but the residue is still the non-exhibitors, so the selection argument cuts the other way.
6. **The 39 VTubers still need a YouTube/Twitch read.** Unchanged across all four builds.
7. **Representability is still asserted, not tested** - now across twenty rows. Rows 14-20 are marked `yes` because no agent, label or parent appears in the creator's own 文博會 record; 行動計畫有限公司 (row 14) is an incorporated company but a creator-owned one. This must be said out loud on any prospect page that uses these rows.
8. **The character test is now the binding constraint and it deserves a second opinion.** Build 4 rejected five in-band creators on it, one of them (魚氏, 1,170) narrowly enough that a human might reverse it. Build 2 rejected seven the same way. Every one of the twelve is a sub-10k independent creator who really did sign a brand deal; what they lack is a named character. The rule is defensible - the task asks for an independent *character* - but the file should surface the arithmetic rather than bury it: **adding back build 4's five character-test rejections alone would take this file to 25 rows and meet the stop condition.** That is a human's call to make, not this build's, and it is the single decision that most changes what the file says.

---

## What build 3 leaves owed

*(Status after build 4 in italics.)*

**12 of 25 rows.** The stop condition is not met, but the shape of what remains has changed: the two brand directories are now worked out, and the residue is concentrated in one place.

*Build 4 status per item: (1) partly discharged - the 2025 edition resolved 23 more, leaving ~97, and the pool now looks low-value; (2) **discharged twice over** - a hotel and 7-ELEVEN, neither of them accessories, but not by the technique the item proposed; (3) not attempted; (4) not attempted; (5) not attempted, now spanning twenty rows; (6) unchanged, and the 2025 edition adds its own unbanded residue.*

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
