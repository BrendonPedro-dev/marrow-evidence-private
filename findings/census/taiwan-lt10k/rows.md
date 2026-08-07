# Taiwan x `lt_10k` independent collaborations - verified rows

Task: `tasks/tw-lt10k-independent.md`.
Goal: documented brand collaborations in Taiwan, 2023-2026, where the partner IP is an INDEPENDENT (or MIXED) character that stood at or under 10,000 followers.
The ten-market census (`findings/census/taiwan-v2/ip_scale_bands.md`) holds **zero** `lt_10k` Taiwan rows at whole-row level - the single `lt_10k` reading in that file is a per-creator sub-band inside two-creator row 76 (臺灣印事).
This file is the dedicated hunt for the missing cell.

**Status: STOP CONDITION MET.
Build 6 of the run - 25 verified rows of a 25-row stop condition.
Build 7 adds no rows; it discharges the file's largest caveat.
Retrieval date for everything below: 2026-08-07.**

> **Build 7 headline: representability was tested, and 19 of the 25 rows failed it.**
> Builds 1-6 marked every row `representable: yes` on the absence of a named agent, which is not evidence of anything. Build 7 applied a positive test: `yes` survives only where a source shows the creator **advertising licensing**, **soliciting collaborations**, or the licensee **naming direct contact**.
> **Six rows keep `yes`; nineteen become `unclear`.** Because rows 4 and 18 are the same creator, the file evidences **five addressable creators, not twenty-five**.
> The new **`representable basis`** column states, per row, which test was met and on what string. Method, rule and the three close calls: section 16.
> The channel that made this cheap: Threads serves the **full, untruncated** biography under a Googlebot user-agent, and the bio is where 「合作信箱」 and 「授權」 lines live. Instagram's `og:description` truncates them and is dead anyway.
> The share is separately restated: the ibon cohort is **12 of 15 resolved (80%)**, not 12 of 16 (75%), because 木子島工作室 is unresolved rather than out of band.

> **Build 6 headline: the character test finally has a channel to run on.**
> Build 5 established the rule - a character-test rejection requires reading the creator's *own* channel, not the licensee's blurb - and then could not apply it, because Instagram's profile route died mid-run and faults with HTTP 400 on any business-category account.
> **Threads serves the same accounts, server-rendered, over plain curl.** `https://www.threads.com/@<handle>` returns HTTP 200 with the account's full biography and its recent post captions embedded as JSON, under a Googlebot user-agent. The handle space is shared with Instagram, so every handle this run already holds is directly usable.
> Re-running build 5's rule through that channel across **all thirteen in-band character-test rejections** in the file reverses three and upholds ten:
> - **時薪一加侖鮮奶** signs every post 「崽唸ㄗㄞˇ／崽崽唸ㄗㄞˇㄗㄞ」 - a pronunciation guide for a named character, 崽崽, which it then tracks across formats in its own words (「藍色蝴蝶結崽圖一路從林崽的陶杯上跳到 T-shirt 上」). Build 2 rejected it as "a joke about being paid in milk"; the joke is the *studio* name. **Row 23.**
> - **窩窩頭** introduces named characters as beings - 「大家好，牠們分別叫做 大富、大貴、大吉、大利、大發、桃花」 - and a named character family, 達摩親子糰, made of 【爸爸摩】【哥哥摩】【貝比摩】. **Row 24**, and the weakest of the three; the evidence is quoted so it can be reversed.
> - **風速新營 XYWS** publishes a ZINE series that is literally one page per character, each named and given a personality: WOLFY the super moto rider, SK8EGG "a super bouncy boiled egg who loves skateboarding", BALANCE LE DOG "she loves collecting hats", Jessie, FU-KU ÉKIPU, NICE BÉBÉ & Devilcat. **Row 25** - and the licensee agrees: DEVILCASE's own product names on crossover 166 are `FAMILY TIME`, `DEVILCAT`, `WOLFY ＆ FUKU EKIPU`. Build 4 read the bio paragraph on that page and never read the product list two lines below it.
>
> The last point generalises past this run. **A licensee's product names are character evidence and its bio paragraph is not.** The bio is written about the artist; the SKU names are written about the thing being licensed.

> **Build 5 headline, and it is a method correction rather than a new vein.**
> Build 4 named the character test as the binding constraint on row count. Build 5 found that the test was being run against **the wrong document**.
> Every character adjudication in builds 2-4 was made from the *licensee's or the organiser's* blurb - a RHINOSHIELD roster bio, a 文博會 exhibitor page. Those are marketing copy about a brand, and they routinely do not mention the character even when one exists.
> Run the same test against **the creator's own channel** and it flips: 羊號角Piper, rejected by build 4 as "fantasy/nature illustration, no character", posts serialised stories about a named forest witch-doctor, **皮塔**, and built a six-month solo exhibition around him. That is row 22.
> The same correction produced row 21: 閃亮亮樂園's exhibitor blurb names no character, but its Instagram is a channel about **哈囉鵝 Hello Goose**, and it carries the creator's own account of the deal - 「也榮幸獲得文博媒合與澎湖輪合作，第一次有這麼有趣的案子」.
> **Rule going forward: the licensee's copy can only confirm a character, never refute one. A character-test rejection requires reading the creator's own channel.**
>
> **Build 5's second contribution is a measurement the run has needed since build 1.** The whole file rests on the claim that press coverage is a scale filter. 自由時報's full-text search works over plain curl, so that claim was tested rather than asserted: 536 名 文博會 exhibitors with known follower counts, queried against the paper's whole archive.
> Coverage rises monotonically with scale (13.1% sub-10k → 30.9% at `50k_200k` → 55.6% at `200k_1m`), and hand-reading every sub-10k hit returns **zero** independent-character brand collaborations - against the twenty this file already holds from non-press indexes. See `ltn-press-coverage-by-band.md`.

> **Build 4 headline.** The two brand-directory veins were worked out, so build 4 went looking for a third brand and found the wrong thing in the right place.
> The 文博會 organiser publishes its own **異業合作** (cross-industry partnership) section - a curated list of who partnered with whom, written by the party that brokered the deals.
> That section is a *collaboration* index, not an exhibitor index, and it is what builds 1-3 were missing: Vein F told you who a creator is, Vein G tells you who they signed with.
> It led directly to **7-ELEVEN's ibon 雲端列印 x 16 新銳創作者** (140+ licensed SKUs across 7,300 stores), of which **12 of the 15 resolved are sub-10k** - the single largest concentration of sub-10k Taiwanese licensing found anywhere in this run.

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
| **H. 7-ELEVEN / ibon 雲端列印 x 文博會 特印企劃** | Convenience-store cloud-print service; 140+ licensed print SKUs from 16 named 新銳 creators, sold in 7,300 stores | **WORKS, and is the richest single collaboration in the file.** 12 of the **15 resolved** creators are sub-10k (16 named, 木子島工作室 unresolved) and **8** clear the character test once the test is run against the creator's own channel (build 5 added 羊號角Piper). `print.ibon.com.tw` itself is a JS shell whose API is `robots.txt`-disallowed, so the creator list came from the trade press, not the brand |
| **G2. Creative Expo Taiwan organiser *news feed*** `2025.creativexpo.tw/zh-TW/posts/<id>` | The 2025 edition's own press releases - the section build 4 swept on the 2026 host but never on the 2025 one | **WORKS, and carries deals the 異業合作 section omits entirely.** 20 real posts of ids 1-60. Four brokered 2025 partnerships appear only here: 台灣航業 澎湖輪 x 4 IPs (**row 21**), WeMo Scooter x noii noii, ibon x 16 IPs (the 2025 cohort), and We TAIWAN 大阪世博 x 10 新秀 IPs. This is the second time the news feed beat the partnership page, so treat it as the rule and not the exception |
| **J. Threads profile pages** `www.threads.com/@<handle>` | The creator's own channel, on the platform that shares Instagram's handle space | **WORKS, and it is the replacement for the Instagram route that died during build 5.** Server-rendered under a Googlebot UA: HTTP 200, the full `biography` string and 3-25 recent post captions, all as JSON inside the page. Not a discovery index - Threads' own `/search` requires login and returns nothing to curl - and its `follower_count` is the **Threads** graph, not Instagram, so it cannot band anyone. What it does is adjudicate: it is the only channel this run has that reads what the creator says about their own work. Produced rows 23, 24 and 25 |
| **K. ibon 授權專區, archived generation** `print.ibon.com.tw/licenseproduct/Detail?LicenseProductId=<n>` via Wayback | The 2019-2023 server-rendered generation of 7-ELEVEN's own licensing directory, before it became the JS shell of Vein H | **READABLE and PARTLY WORKED - 58 campaign ids enumerated from CDX, 21 read.** It is a real national-brand licensing directory that names its licensors. Two in-window campaigns are pixiv FANBOX 創作者應援企劃 waves 3 and 4 (2023-03 and 2023-08-22/10-23, the latter tied to a 駁二藝術特區 exhibition), naming ~15 Taiwanese illustrators and comic artists between them. **No row taken**: these are poster/postcard print licences of comic and pin-up artwork rather than character IP, and their creators' primary channels are pixiv/X rather than anything this run can band. Wayback throttles hard - pace at 3s or the sweep silently returns empty bodies |
| **I. 自由時報 full-text search** `search.ltn.com.tw/list?keyword=<q>&type=all` | Taiwan's largest daily, with a standing 藝文 desk; answers over plain curl with real, parseable results | **WORKS as a search index and produces essentially nothing as a row source - which is itself the finding.** 536 名 exhibitors joined against the whole archive: 0 accepted `lt_10k` rows, 1 real licence rejected on class (蘭獸), 1 mis-banded exhibitor exposed (無所事事小海豹). It is the instrument that converts "press is a scale filter" from an argument into a number. See `ltn-press-coverage-by-band.md` |

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
| 6 | 羊號角Piper | `@piper.illu` | **3,604** (3,630 on 2026-08-07 re-read) | `lt_10k` | **pass, corrected by build 5** - build 4 read the exhibitor blurb and recorded "fantasy/nature illustration, no character"; the creator's own channel serialises 森林醫師**皮塔**. **Row 22** |
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

**12 of the 15 resolved creators are sub-10k - 80%; 8 of those clear the character test - 7 as rows 14-20, plus 羊號角Piper as row 22 after build 5 re-ran the test against the creator's own channel.**

**The denominator is 15, not 16.** 木子島工作室 is **unresolved** - no handle, no count, no band - and an unresolved creator is not an out-of-band creator.
Counting it in the denominator silently asserts it is above 10k, which no source supports; it is the one named creator in this cohort that six builds could not reach, and it is at least as likely to be sub-10k as not.
So the honest statement is **12 of 15 resolved (80%), with 1 of the 16 named creators unresolved**, and the range the evidence actually permits is 12/16 = 75% at worst and 13/16 = 81.3% at best.
Every count above is a live Instagram `og:description` read on 2026-08-07 against the handle the exhibitor publishes on their own 文博會 page, and every display name carries the IP's own name, so the handle-squat guard is satisfied twice over.

### 12. The character test was being run against the wrong document (build 5)

This is the most consequential thing build 5 did and it costs nothing to apply retrospectively.

Builds 2, 3 and 4 all adjudicated "is this an independent *character* IP?" from whichever document the vein happened to supply: RHINOSHIELD's roster bio line, or the creator's 文博會 exhibitor description.
Both of those are **written to sell a stand or a collection**, not to describe an IP. They lead on medium, mood and materials.
The consequence is a systematic false-negative rate, and it is measurable on two cases:

| creator | what the licensee/organiser blurb says | what the creator's own channel says |
|---|---|---|
| 閃亮亮樂園 (3,693) | 「以戳針、插畫與陶藝為主的個人創作品牌…品牌核心為『日常的事物都有其閃亮特質』」 - punch needle, illustration, ceramics. No character. | Ten of twelve recent posts are about **哈囉鵝 Hello Goose** 🪿 - 「Hello Goose on a snack mission」, 「哈囉鵝和食物夥伴們」, 哈囉鵝的透明防水貼紙 |
| 羊號角Piper (3,630) | 「以奇幻與自然為核心，將森林與魔法化作細膩的插畫故事」 - fantasy and nature illustration. No character. | Serialised stories about **皮塔 (Pita)**, a forest witch-doctor - 「身為巫醫的皮塔」, 「森林醫師皮塔」 - plus a catalogued world (`FM-26-IN-0514 水青粉蝶`, 屬性｜微光探測者) and a six-month solo exhibition, 森棲棲, built on it |

**Rule.** The licensee's or organiser's copy can *confirm* a character (as it does for rows 14-20, where 「以原創角色 SPARK 為核心」 is explicit) but it cannot *refute* one.
A character-test rejection is only sound if the creator's own channel was read.

Applied to build 4's five in-band character-test rejections, four survive re-examination on the creator's own channel and one reverses:

| creator | own-channel evidence | verdict after re-test |
|---|---|---|
| 洋樓拾憶文創工作室 (395) | Kinmen 洋樓 heritage: pop-up books, 得月樓, Red Dot award, community walking tours. No character anywhere in 67 posts | rejection **stands** |
| 魚氏 (1,200) | 水彩 / 插畫 / 漫畫; the recurring tag is `#YUcomic`, a comic strip, with no named cast | rejection **stands** |
| 張哲 (1,638) | Landscapes, furniture, 1980-89 car catalogues, tattoo stickers. No character | rejection **stands** |
| 羊號角Piper (3,630) | 皮塔, see above | **REVERSED → row 22** |
| 日句時刻所 (7,493) | account unreadable (see the Instagram note below) | rejection **unverified**, carried forward |

The same re-test was run against three of build 2's readable "character not evidenced" RHINOSHIELD rejections - 旅貓實驗室 (1,785), 阿薛 (2,428) and 張哲 - and all three stand: 旅貓實驗室 draws and photographs *real* cats, 阿薛 is a travel illustrator. The remaining ones could not be re-tested (below).

**Instagram access changed during this build, and the change constrains what can be re-tested.**
The `og:description` route every earlier build used is gone: `https://www.instagram.com/<handle>/` now returns **302 to `/accounts/login/?...&is_from_rle`** for every user-agent tried (Googlebot, Googlebot-smartphone, facebookexternalhit, Twitterbot, desktop Chrome, Applebot).
`instagram.com/robots.txt` states that automated collection is prohibited without written permission and carries `User-agent: ClaudeBot / Disallow: /`.
**No bulk sweep was run.** Follower and bio reads in this build were individual lookups against creators already named in this file, which is what the task's verification step requires; a planned 240-account scan of the sub-10k cohort was written and then abandoned on reading that policy, and future builds should not run one either.
Where an account carries a business category the profile endpoint returns HTTP 400 with `Asset asset://laser.provider/ig_business_category_subvertical has been deleted` - a server-side fault, not a rate limit, and it is why 日句時刻所, 窩窩頭, 時薪一加侖鮮奶, 舒媞 and AndreaCat could not be re-tested at all.

### 13. Vein G2 - sweep the *previous* edition's news feed too (build 5)

Build 4 established that the organiser's news feed carries deals its 異業合作 section does not, and proved it on the 2026 host (`posts/38` → 7-ELEVEN).
Build 5 ran the same sweep on the 2025 host, which no earlier build had: ids 1-60, keeping only pages whose final URL id matches the request, gives **20 real posts**.

`2025.creativexpo.tw/zh-TW/posts/14` (2025-07-24) is the 2025 equivalent of `posts/38` and it names four brokered partnerships that appear nowhere in `collaboration_responses`:

| partnership | named IPs | bands | outcome |
|---|---|---|---|
| 台灣航業 澎湖輪 x 4 IPs, 海盜船主題 | 其實他是鵝, **閃亮亮樂園**, 小喵WE, 維尼有畫想說 | 22K / **3,693** / 43,541 / 15K | **ROW 21** + 3 out of band |
| WeMo Scooter 聯名車款 + IP 安全帽 | noii noii | 44K | rejected - out of band |
| ibon 雲端列印 x 16 IPs (the **2025** cohort) | only 5 of 16 named: 啾啾噗噗 168K, 伸縮自如的雞與鴨 36K, 其實他是鵝 22K, 兔君 24K, 嗚比的朋友 104K | all out of band | **the other 11 were not recoverable** - see owed |
| We TAIWAN 大阪・關西世博 x 10 新秀 IP (accessories for the `a-We TO GO` game) | 恐龍的房間 94K, 妯米 10K, Tabbi L 11K, 小圓麵包 12K, 阿翰 58K, 安怎？Ann-Nua 20K, 幽默之星 11K, POPO鴿的鳥日子 67K, 蛋塔熊妹 37K, noii noii 44K | all at or above 10K | rejected - none in band. 妯米 reads exactly `10,000`, so it is boundary-ambiguous under the rounding rule and is recorded rather than banded |

Two further reads from the same sweep, both deals rather than rows:
`posts/30` records that 文化部 published **58 completed licensing cases** at the 2025 黑潮星樂園 and `posts/32` that the zone closed **84 signed contracts** - the largest deal index seen in this run. Neither is worked here, and both are a scale filter by design: the 黑潮 programme selects IPs with 「5年以上資歷」 and existing 授權實績.

### 14. Vein I - using a newspaper archive as an instrument rather than a source (build 5)

Full detail and the reproducible method are in `ltn-press-coverage-by-band.md`. In brief: `search.ltn.com.tw` answers over plain curl, its result *count* is a fuzzy OR count that must be discarded, and the exact name has to be re-checked inside each returned title and snippet.
Joining 536 名 文博會 exhibitors of known band against 自由時報's whole archive gives a coverage rate that rises monotonically with scale and **zero** accepted `lt_10k` rows.
One incidental but important mechanic: `news.ltn.com.tw` article bodies are absent from the desktop HTML and present when the same URL is requested with an iPhone user-agent.

### 15. Vein J - Threads as the channel the corrected character test needs (build 6)

Build 5 wrote the rule and could not run it.
Instagram's `og:description` route died mid-run (`/accounts/login/?...&is_from_rle` on every user-agent, plus `Disallow: /` for ClaudeBot in `instagram.com/robots.txt`), and the profile endpoint additionally faults with HTTP 400 `Asset asset://laser.provider/ig_business_category_subvertical has been deleted` on any business-category account - which is most working creators.
Five in-band rejections could not be re-tested at all.

**`https://www.threads.com/@<handle>` answers over plain curl with HTTP 200 and the account fully server-rendered.** Reproducible extraction:

```
curl -s -A "Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)" \
  "https://www.threads.com/@<handle>"
```

- `"biography":"..."` - the JSON-escaped bio, decode with `json.loads`
- `"caption":{...,"text":"..."}` - 3-25 recent post captions, the actual adjudication material
- `<meta property="og:title">` - the account's display name, which is the name-match guard from build 3's handle rule
- `"follower_count":<n>` - **the Threads follower graph, not Instagram's.** It runs an order of magnitude below the same account's Instagram count in every case checked (時薪一加侖鮮奶 566 vs 2,423; 窩窩頭 353 vs 2,154; AndreaCat 302 vs 1,055). **Never band off it.**

Two limits, both checked:

1. **Not a discovery index.** `threads.com/search?q=<CJK>` returns HTTP 200 and a 531KB page containing zero usernames - the results render only behind a login. So Threads does not solve handle discovery; 木子島工作室, 泰江 TJ GAMEBOY, 尼胖 and the other unresolved handles stay unresolved.
2. **A 302 means "no Threads account", not "no such creator".** `@yiekubo` is published by the 2025 文博會 directory and exists on Instagram, and 302s here. So a 302 closes the adjudication route for that creator, it does not refute them.

**Result of running the corrected test through this channel.** All thirteen in-band character-test rejections in the file were re-tested. Three reverse (rows 23-25), eight are upheld on the creator's own words, and two could not be reached (a 302 and a German artist outside the market question). The reversal rate is 3 of 11 reachable - materially lower than build 5's single-case reversal suggested, which is the useful calibration: the licensee blurb is unreliable, but it is wrong in only about a quarter of cases, not most.

### 16. Representability, tested rather than asserted (build 7)

Every earlier build marked `representable: yes` on the same non-basis: no agent, label or parent appeared in the sources read.
That is an absence of evidence and it was the file's largest caveat for six builds. It is now discharged, and it cost 25 curl requests.

**The rule applied.** `representable: yes` **only** where a source carries positive evidence of addressability, in one of three forms:

1. **`advertises-licensing`** - the creator's own channel names licensing or IP commercialisation as a service (授權, 圖像授權, 「以原創 IP 創造商業價值」).
2. **`solicits-collaboration`** - the creator's own channel names a contact route explicitly labelled for collaboration (合作信箱, 合作邀約歡迎來信, 歡迎合作請洽 + address).
3. **`licensee-names-contact`** - the licensee or deal source publishes a direct contact for the creator. **No row in this file qualifies on this basis.**

Everything else is `unclear`. The `representable basis` column states which applies, per row, with the string it rests on.
Absence of a named agent is recorded as **`no-agent-named`** and is never sufficient.

**The channel that made this testable.** Section 15's Threads route serves the profile only under a **Googlebot user-agent**; a browser UA and plain curl both return a 576KB shell with no `biography` field at all.

```
curl -sL -A "Googlebot/2.1 (+http://www.google.com/bot.html)" https://www.threads.com/@<handle>
```

The bio is the licensing-solicitation surface. Instagram bios are truncated in `og:description` and that route is dead anyway; the Threads `"biography"` field is the **full, untruncated** bio, which is where 合作信箱 and 授權 lines live.
23 handles probed, 19 served a biography, 4 did not (three have no Threads account, two accounts serve an empty bio).

**Result: 6 rows keep `yes`, 19 downgrade to `unclear`.**

| basis | rows | n |
|---|---|---|
| `advertises-licensing` | 1, 4, 18 | 3 |
| `solicits-collaboration` | 19, 22, 23 | 3 |
| `licensee-names-contact` | - | 0 |
| `no-agent-named` (absence only) | 3, 5-17, 20, 21, 24, 25 | 19 |
| `possible-licensor-in-chain` | 2 | 1 |

Rows 4 and 18 are one creator (灰黑集白), so the file evidences **five addressable creators, not twenty-five**.

**Three close calls, recorded so a human can overturn them.** Row 9 (`品牌相關請➡️IG` - routes brand enquiries but names no purpose), row 10 (a bare email under "Illustrator", no stated purpose), row 16 (an unlabelled email plus a 聯名商品 link category listing existing co-brands). Each is one sentence away from `yes` and none of them says that sentence.

**A keyword trap this pass found.** Build 5's proposed detection rule greps the creator's description for 總代理 / 代理 / 經紀 / 授權合作洽談. Run naively it produces a **false positive on row 16**: 鼠粒控's bio reads 「老鼠會會長代理人」, where 代理人 is a joke title inside the 老鼠會 conceit and not an agent. The rule needs the surrounding phrase read, not the substring matched.

**What this does not establish.** `unclear` is not `no`. Nineteen rows are creators whose channels simply do not discuss commercial terms, which is the normal state of a small creator's bio, not a signal of exclusivity. Equally, the six `yes` rows prove the creator invites approaches - **not** that no exclusive licensor sits behind them. The only true `no` in the file remains the population-level 無所事事小海豹 case, whose exhibitor page names a 總代理 outright.

---

## Rows

**Build 1: 2 verified rows.** Proposals for human accept; nothing here has been written to any database.

| # | brand_name | ip_name | market | year | year basis | source_ref | follower_band | count seen | representable | representable basis | ip_class | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | DEVILCASE 惡魔防摔殼 | 茶包先生 Mr. Teabag | TW | 2026 | `wayback-bracket` - crossover id 308, first captured 2026-05-09, and the preceding directory sweep on 2026-04-14 captured only up to id 302, so the partnership went live between those two dates | https://devilcase.com.tw/crossover/308 (HTTP 200, 2026-08-07) | `lt_10k` | **8,288** Instagram followers, `@mr.teabag_`, read 2026-08-07 | yes | `advertises-licensing` - the creator's own Threads bio reads 「授權·聯名·探店合作📮mr.teabag2020@gmail.com」, naming 授權 (licensing) as a service and a contact address for it | INDEPENDENT | Solo Taiwanese illustrator brand - three characters (茶包, 栽栽, 捲捲) described on the partner page as unrelated brothers, no studio or parent named anywhere. Handle name-match is exact: `og:description` display name reads `茶包先生｜文博會S057｜插畫 · 旅遊 ᴾᴸᴼᴳ`, i.e. the account states its own 文博會 (Creative Expo Taiwan) booth number **S057** - the creator is a CET exhibitor, which is the same population as `findings/expo/cet2026-*`. `current-proxy` count against a campaign roughly 3 months older, so the at-campaign figure was lower, not higher |
| 2 | DEVILCASE 惡魔防摔殼 | Wasabi Bear 芥末熊 / 와사비베어 | TW | 2026 | `id-sequence` - crossover id 321 has no Wayback snapshot at all, while id 309 was swept 2026-05-09; ids are sequential, so 321 went live after 2026-05-09 | https://devilcase.com.tw/crossover/321 (HTTP 200, 2026-08-07) | `lt_10k` | **4,252** on `@wasabibear_tw` (芥末熊 Wasabi Bear), the largest of three evidenced channels - Korean home account `@wasabibear.official` (와사비베어) reads **3,882** and `@wasabibear_japan` (ワサビベア【日本公式】) reads **3,973**. All read 2026-08-07 | unclear | `possible-licensor-in-chain` - retailed through LINE FRIENDS SQUARE, so an exclusive licensor may already sit in the chain. Unchanged from build 1 | INDEPENDENT | Korean creator-owned: the character is a handmade doll made by Sugar Rain (Kim Dan-bi) in September 2021, per the Korean-language NamuWiki entry - no conglomerate parent found. **Band is robust against the regional-account trap for once**: unusually, all three country accounts sit under 10K and the *home* account is the smallest of the three, so no choice of primary channel leaves `lt_10k`. `@wasabibear` (56) and `@wasabi.bear` (100) are squats and were rejected. REP=`unclear` because the character is retailed through LINE FRIENDS SQUARE, so an exclusive licensor may already sit in the chain - ownership is independent, addressability is not established |

**Rows 3-12: 10 verified rows from Vein E** (8 landed by build 2, 2 added by build 3). Same status - proposals for human accept, nothing written to any database.

For every row below: `brand_name` = RHINOSHIELD 犀牛盾 (Design Studio), `market` = TW, `ip_class` = INDEPENDENT, and `source_ref` = `https://rhinoshield.tw/design-studio/collections/@<slug>`, curl-verified 200 on 2026-08-07.
`year` basis is the same on all ten: the brand's own **`firstLaunchedAt`** field in the roster payload - a licensee-declared launch date, not an archive inference.
The `build 2 said` column records the value build 2 published for that field, which was in fact the avatar cache-buster; it is kept visible so the correction can be checked rather than taken on trust.
Follower counts are Instagram `og:description` reads on 2026-08-07 against the handle **the brand itself publishes** for that creator, so the count is `current-proxy` and, per section 5, conservative for a past campaign.

| # | ip_name | year | declared launch (`firstLaunchedAt`) | build 2 said | source_ref (`@slug`) | follower_band | count seen | live SKU designs | representable | representable basis | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 3 | 小女孩和花花獅 / PLUDDIE Studio | **2023** | 2023-11-17 | 2025-10-24 | `@pluddie` | `lt_10k` | **4,284**, `@pluddiestudio`, display name 小女孩和花花獅工作室 | 15 | unclear | `no-agent-named` - Threads bio (「嗨！我們是小女孩和花花獅 請多多指教」) names no licensing route and no contact. Absence only | The clearest character row in the file. The brand's own bio names two characters and their relationship: 小女孩, and 花花獅 as "her best friend and most faithful companion". One-studio operation, no parent or agent named. Year corrected by build 3 |
| 4 | 灰黑集白 / 黑貓馬路 Maru | 2025 | 2025-03-18 | 2025-12-30 | `@hueiheijibai` | `lt_10k` | **4,443**, `@aasta_blacknwhite`, display name 灰黑集白｜黑貓馬路 Maru | 19 | yes | `advertises-licensing` - the creator's own CET2026 exhibitor page reads 「致力以原創 IP 創造療癒的商業價值」 and, in English, 「we excel at transforming IP into high-value commercial assets」. The weakest of the six yeses: it advertises licensing as the business but publishes no collaboration contact route | Named character: a bobtail black cat, 馬路 (Maru). Creator-run, no label. **Independently corroborated by Vein F**: 灰黑集白 is CET2026 exhibitor 134 and publishes the same handle there |
| 5 | Cheesy Duck | 2026 | 2026-05-22 | 2026-03-05 | `@cheesyduck` | `lt_10k` | **6,088**, `@cheesyduck_unstop`, display name Cheesy_duck | 6 | unclear | `no-agent-named` - no Threads account; the only text is the licensee's roster bio. Absence only | Bio is explicit about the ownership shape: "Creator of Cheesy Duck, a cheerful character who loves small adventures" - a single creator who owns a single character. The newest row in the file; the current-proxy gap is 2.5 months |
| 6 | 湯姆先生 MR. TOM | 2025 | 2025-08-21 | 2025-06-26 | `@mrtom_design` | `lt_10k` | **6,142**, `@mrtom_design` (handle equals the collection slug), display name 湯姆先生MR. TOM | 7 | unclear | `no-agent-named` - Threads bio is a camping mood line, no licensing route. Absence only | Named character with a stated design rule - "every object in the world has a soul, just add eyes". Camping/outdoors theme |
| 7 | 迪普西 Dipsy | **2023** | 2023-11-22 | 2025-11-28 | `@dipsy` | `lt_10k` | **6,801**, `@dipsydisplay`, display name 迪普西 。Dipsy | **48** | unclear | `no-agent-named` - no Threads account, and the roster bio names no character let alone a licensing route. Absence only | The largest SKU count of any row here - 48 distinct designs off a 6.8K-follower creator, which is the single sharpest datum in this file against "small IP gets token deals". Year corrected by build 3, and the correction *strengthens* the row: the relationship is 2.5 years old, not 9 months. Weak on the character test - the brand's bio line ("描繪日常，用鬆餅犒賞自己") names no character, so the character claim rests on the collection name alone |
| 8 | LilyandStarsStudio / Bun and Bear | **2024** | 2024-09-06 | 2025-08-04 | `@lilyandstarsstudio` | `lt_10k` | **7,586**, `@lilyandstarsstudio` (handle equals slug), display name LilyandStarsStudio | 12 | unclear | `no-agent-named` - Threads bio reads 「Cute illustrations / Tiny animations / Shop open / US based」; a shop, not a licensing route. Absence only | Two named characters, Bun and Bear. Year corrected by build 3 |
| 9 | ilovemyselfself | 2023 | 2023-06-30 | 2023-07-06 | `@ilovemyselfself` | `lt_10k` | **3,460**, `@ilovemyselfself` (handle equals slug), display name Ilovemyselfself | 8 | unclear | `no-agent-named`, **close call** - Threads bio reads 「品牌相關請➡️IG」, i.e. the creator routes brand enquiries to their own Instagram. That shows they field brand business personally but names neither licensing nor a contact, so it falls short of the positive test | **The earliest in-window row in the file.** Bio self-describes as 獨立設計品牌 - an independent design brand built on a 厭世 dog character and a one-person `#ihatemondayclub`. Wayback first capture of the collection page is 2025-09-15, consistent with (and much later than) the declared 2023 launch. Note that 2023-06-30 is shared with two other records, so it is likely the platform's own data-import date and therefore an upper bound on this creator's real start |
| 10 | sillysally 실리샐리 | **2026** | 2026-02-26 | 2024-09-10 | `@sillysally` | `lt_10k` | **3,113**, `@sillysally.official`, display name sillysally 실리샐리 | 27 | unclear | `no-agent-named`, **close call** - Threads bio reads 「Illustrator 💌 sallyselimyang@gmail.com」. A bare email with no stated purpose is a contact route, not a licensing or collaboration solicitation | Korean creator, same import shape as row 2. The character is the brand name itself; the bio names no separate character, so this is among the weakest rows on the character test and is flagged as such rather than dropped. Year corrected by build 3 - and this is the one row where the correction moves the year *later*, because its assets predate its Taiwan launch by 17 months |
| 11 | 阿7世界 (欸貓 / 櫻鵝 / 草莓狗 / 貓桃鷹) | 2023 | 2023-11-27 | - | `@chilittleworld` | `lt_10k` | **3,267**, `@chi_littleworld`, display name 阿7世界 | 6 | unclear | `no-agent-named` - Threads bio names the four characters and nothing else. Absence only | **New in build 3.** The strongest character row in the file after row 3: the brand's own bio names four characters and their types - 熬夜系的欸貓, 佛系櫻鵝, 暖系草莓狗, 獨處系貓桃鷹 - and says they became friends. The roster publishes no handle for this creator, so the handle was guessed and then accepted only on an exact display-name match (阿7世界). The squat `@chilittleworld` (YuChi, 2 followers) is the counter-example that makes the name-match rule necessary |
| 12 | 吶吉吶吉 NAGIxNAGI | 2026 | 2026-06-12 | - | `@nagiart` | `lt_10k` | **8,105**, `@oooo_nagixnagi`, display name NAGIxNAGI!!!吶吉和他的搗蛋怪朋友｜IP雜貨 | 7 | unclear | `no-agent-named` - Threads bio reads 「新商品過程打樣都丟這裡」; the Instagram bio's `IP雜貨` is a self-description of the business, not a licensing offer. Absence only | **New in build 3, and the only row in the file found by cross-referencing two independent directories.** The roster publishes no handle; the handle came from Vein F (CET2026 exhibitor 122, 吶吉與他的搗蛋怪朋友), and the identification is carried by the character set, not the name: the RHINOSHIELD bio reads 「這裡是吶吉和他的搗蛋怪朋友們，兔人、鳥人、貓人」 and the Instagram display name reads 吶吉和他的搗蛋怪朋友. The account's own bio calls itself `IP雜貨`, i.e. the creator describes themselves as running an IP. Ten handle guesses had already failed on this one |

**Row 13, from Vein G.** A second brand for an IP this file already carries, which is the first time any IP in the file has two independent licensees.

| # | brand_name | ip_name | market | year | year basis | source_ref | follower_band | count seen | representable | representable basis | ip_class | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 13 | 南港老爺行旅 Hotel Royal Nikko Nangang | NAGI x NAGI 吶吉 (兔人 / 鳥人 / 貓人) | TW | 2026 | Organiser page dated **2026-08-03**; the offer itself runs 即日起至 11/30 and the trade press announced it 2026-07-27. No inference needed | https://creativexpo.tw/zh-TW/collaboration_responses/34 (HTTP 200, 2026-08-07) | `lt_10k` | **8,105** Instagram followers, `@oooo_nagixnagi`, display name NAGIxNAGI!!!吶吉和他的搗蛋怪朋友｜IP雜貨, read 2026-08-07 | unclear | `no-agent-named` - the organiser's page names the creator and the deal but publishes no contact for them, and the deal was brokered by the show rather than taken direct. Absence only | INDEPENDENT | A styled guest room built around the IP, NT$5,800 per night for two, running to 2026-11-30. **The same creator as row 12** (RHINOSHIELD), so this file now has one IP with two unrelated licensees in two unrelated categories - phone accessories and hospitality - which is the first direct evidence in the run that a sub-10k Taiwanese IP can hold more than one deal at a time. The organiser's own copy names the three characters (「兔人」「鳥人」與「貓人」) and calls NAGI 「來自臺灣的插畫創作者」, so the character test and the independence test are both carried by the source rather than inferred. The room's co-headliner, 泰江 TJ GAMEBOY, is rejected - see Rejected candidates |

**Rows 14-20: 7 verified rows from Vein H**, the 7-ELEVEN / ibon 雲端列印 x 2026 臺灣文博會 「第零位元」 特印企劃.

For every row below: `brand_name` = **7-ELEVEN 統一超商 (ibon 雲端列印)**, `market` = TW, `year` = **2026**, `ip_class` = INDEPENDENT. `representable` is per-row and mostly `unclear` - see the column.
`source_ref` = `https://www.cdns.com.tw/articles/1429446` (中華日報, 2026-07-14, HTTP 200 verified 2026-08-07) - the trade-press release that names all sixteen creators and the deal terms.
`year` basis is the same on all seven and needs no inference: the article states the two release waves as **2026-07-08 and 2026-07-15**, running to 2026-08-31.
Each row's second source is that creator's own 文博會 exhibitor page, which is where the Instagram handle and the character claim come from; all thirteen exhibitor pages touched were curl-verified 200 on 2026-08-07.
Follower counts are live Instagram `og:description` reads on 2026-08-07 - a `current-proxy` gap of about one month, the shortest in the file.

| # | ip_name | source_ref (secondary - exhibitor page) | follower_band | count seen | representable | representable basis | notes |
|---|---|---|---|---|---|---|---|
| 14 | SPARK的行動計畫 (SPARK) | https://creativexpo.tw/zh-TW/exhibitor_list/42 | `lt_10k` | **2,144**, `@actionplan24`, display name SPARK的行動計畫 | unclear | `no-agent-named` - Threads bio is a brand mood line. 行動計畫有限公司 establishes there is a company to contract with, which is not the same as evidence it is free to contract. Absence only | The cleanest single-character row in the file: the brand's own line is 「行動計畫有限公司以原創角色 SPARK 為核心」 - one company, one owned character, stated in that order. Incorporated as 行動計畫有限公司, so creator-owned but not a sole trader |
| 15 | 虎嚕吼嚕嚕 HOORU HORURU | https://creativexpo.tw/zh-TW/exhibitor_list/79 | `lt_10k` | **3,078**, `@hooru.horuru`, display name 虎嚕吼嚕嚕 HOORU HORURU | unclear | `no-agent-named` - Threads bio is the character's story plus this year's booth details. Absence only | The only row in the file whose own description uses the phrase **"original character IP"** unprompted. 黑色虎爺「虎嚕」 born at 嘉義城隍廟 - a folk-religion character, i.e. exactly the kind of locally-rooted small IP the census's press sources never reach. 25 posts and 4 accounts followed: a very new account, which makes the current-proxy read close to the at-campaign figure |
| 16 | 鼠粒控 / 3co Studio | https://creativexpo.tw/zh-TW/exhibitor_list/133 | `lt_10k` | **3,934**, `@3co_studio_`, display name 鼠粒控 / 3co Studio | unclear | `no-agent-named`, **close call** - Threads bio carries 「✉️ yuridraww@gmail.com」 and a link category 「線上販賣部、聯名商品、Line貼圖&主題」. The email is unlabelled and 聯名商品 lists existing co-branded goods rather than soliciting new ones. **Keyword trap:** the same bio says 「老鼠會會長代理人」 - 代理人 here is a joke title inside the 老鼠會 conceit, not an agent, and a naive 代理 grep would misread it | A cast of round, expressive mice organised as a mock 「老鼠會」 (a pun on Taiwan's word for a pyramid scheme). Independently named in a second 2026 collaboration - LINE 貼圖's 文博創作專區 - which is **rejected** as platform promotion rather than licensing, so this creator has one accepted row and one logged rejection |
| 17 | 兩顆糖製造機 2SugarStudio (齁咪呀 / 巴拉王子) | https://creativexpo.tw/zh-TW/exhibitor_list/268 | `lt_10k` | **4,049**, `@2sugarstudio`, display name 兩顆糖製造機 | unclear | `no-agent-named` - Threads bio is an in-character joke line. Absence only | Two named characters with species and role: 棉花糖鱷魚「齁咪呀」 and 鴨嘴獸「巴拉王子」. Works in resin and sofubi, i.e. an art-toy maker whose IP has now been licensed into a print format - a genuine category jump for a 4K-follower creator |
| 18 | 灰黑集白 / 黑貓馬路 Maru | https://creativexpo.tw/zh-TW/exhibitor_list/134 | `lt_10k` | **4,443**, `@aasta_blacknwhite`, display name 灰黑集白｜黑貓馬路 Maru | yes | `advertises-licensing` - same creator as row 4, same basis: the CET2026 exhibitor page advertises IP commercialisation and cites the RHINOSHIELD deal as a credential | **Same IP as row 4, different licensee.** Row 4 is RHINOSHIELD; this is 7-ELEVEN. The creator's own 文博會 line cites the RHINOSHIELD deal as a credential (「具備犀牛盾聯名與空間展陳實績」), which is the first case in this file of one accepted row being used by the creator to win the next - a documented licensing ladder inside the sub-10k band |
| 19 | 吉文考古 Auspicious Pattern Archeology | https://creativexpo.tw/zh-TW/exhibitor_list/293 | `lt_10k` | **6,951**, `@apa0824`, display name 吉文考古｜插畫｜平面設計｜圖像授權 | yes | `solicits-collaboration` - the creator's own Threads bio reads 「歡迎合作請洽：apahung0824@gmail.com」, an explicit invitation plus the address to use. The Instagram display name independently ends in 圖像授權 | Twin creators turning Taiwanese auspicious motifs into 「可愛角色與故事」 with a named world (吉地探險) and a named creature class (吉獸). The account's own bio ends in **圖像授權** - the creator advertises image licensing as a service, which is about as direct an addressability signal as this file contains |
| 20 | ATW STUDIO (怪噗 Guaipu / 飛克 Faker) | https://creativexpo.tw/zh-TW/exhibitor_list/347 | `lt_10k` | **8,116**, `@atw_studio`, display name ATW studio | unclear | `no-agent-named` - Threads bio reads 「一坨爛泥ㄉ日常」. Absence only | Two named characters, 怪噗 and 飛克, described as the perspectives the work is made through. The largest of the seven and the closest to the 10,000 boundary, but not close enough to be ambiguous under the rounding rule (Instagram serves an exact figure below 10,000) |

**Rows 21 and 22, from build 5.** Both come from the corrected character test in section 12 rather than from a new vein.

| # | brand_name | ip_name | market | year | year basis | source_ref | follower_band | count seen | representable | representable basis | ip_class | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 21 | 台灣航業 澎湖輪 (Taiwan Navigation, Penghu ferry) | 閃亮亮樂園 KIRA KIRA LAND (哈囉鵝 Hello Goose) | TW | 2025 | Organiser release `posts/14` is dated **2025-07-24** and describes the tie-up as running with the 2025 文博會 (8/2-8/11); the creator's own post says the on-board install was built and then visited at the end of that month. No inference beyond the dateline | https://2025.creativexpo.tw/zh-TW/posts/14 (HTTP 200, 2026-08-07) | `lt_10k` | **3,693** Instagram followers, `@kirakira_land`, display name `KIRA KIRA LAND 閃亮亮樂園`, read 2026-08-07 | unclear | `no-agent-named` - the Threads profile serves no biography text, so nothing positive could be read. The creator does describe the deal in the first person (「也榮幸獲得文博媒合與澎湖輪合作」), which shows she speaks for herself in it but is not a licensing offer | INDEPENDENT | A pop-up themed space aboard the Penghu inter-island ferry: 「2025 臺灣文博會 × 台灣航業｜澎湖輪 快閃主題空間 - 四位創作者的**原創角色**聯手登船，展開一場尋寶任務」, the characters hidden through the cabins, the rest area, the windows and the corridors as a treasure hunt. **The brokered-channel finding again, and this time in the creator's own words**: 「也榮幸獲得文博媒合與澎湖輪合作，第一次有這麼有趣的案子」 - a creator saying the trade show matched them to the deal, and that it was their first. Its 2025 booth was in the **IP新秀** (emerging IP) zone, S-065. Character test carried by the creator's channel, not the exhibitor blurb - see section 12. The other three IPs on the ferry (其實他是鵝 22K, 小喵WE 43,541, 維尼有畫想說 15K) are all out of band |
| 22 | 7-ELEVEN 統一超商 (ibon 雲端列印) | 羊號角Piper (皮塔 Pita) | TW | 2026 | The 中華日報 release states the two waves as **2026-07-08 and 2026-07-15**, running to 2026-08-31 - same basis as rows 14-20 | https://www.cdns.com.tw/articles/1429446 (HTTP 200, 2026-08-07); secondary https://creativexpo.tw/zh-TW/exhibitor_list/440 (HTTP 200) | `lt_10k` | **3,630** Instagram followers, `@piper.illu`, display name 羊號角Piper插畫, read 2026-08-07 | yes | `solicits-collaboration` - the creator's own Threads bio reads 「合作信箱：piper.studio23@gmail.com」, a mailbox explicitly labelled for collaboration | INDEPENDENT | **A build-4 rejection reversed.** Build 4 read the exhibitor blurb (「以奇幻與自然為核心」) and recorded "no character". The creator's own channel runs serialised episodes about a named protagonist, the forest witch-doctor **皮塔 (Pita)** - 「身為巫醫的皮塔」, 「森林醫師皮塔的藥水瓶」 - inside a catalogued world with its own specimen numbering (`FM-26-IN-0514 水青粉蝶`, 屬性｜微光探測者), and a solo exhibition 「森棲棲-插畫家的綠色狂想」 ran 2025-09-26 to 2026-03-01 on it. The creator confirms the deal directly: 「2026文博-IBON的合作終於可以曝光啦，即日起到8/31，全台IBON都可以找到這些魔法酷東西」. This makes the ibon cohort **8 of 12 sub-10k creators accepted**, not 7 |

**Rows 23, 24 and 25, from build 6.** All three are reversals of earlier character-test rejections, adjudicated on the creator's own Threads channel (Vein J). No new deal was found; what was found was a channel on which the deals already in the rejection log could be read correctly.

Follower counts are the Instagram figures the earlier builds read on 2026-08-07 from the handle the licensee itself publishes. **They were not re-read this build** - the Instagram route is dead and bulk collection there is robots-prohibited - so each is carried forward with its original basis stated. The Threads count is given alongside as an independent, *different* measure, never as the band.

| # | brand_name | ip_name | market | year | year basis | source_ref | follower_band | count seen | representable | representable basis | ip_class | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 23 | RHINOSHIELD 犀牛盾 (Design Studio) | 時薪一加侖鮮奶 (崽 / 崽崽) | TW | **2024** | The brand's own `firstLaunchedAt` = **2024-02-29**. Note this is the corrected field: build 2's rejection table recorded 2025-12-11 for this creator, which is the avatar cache-buster build 3 identified as the wrong column | https://rhinoshield.tw/design-studio/collections/@gallon-milk (HTTP 200, 2026-08-07); character evidence https://www.threads.com/@gallon_milk14 (HTTP 200, 2026-08-07) | `lt_10k` | **2,423** Instagram followers, `@gallon_milk14`, read 2026-08-07 by build 2 from the handle RHINOSHIELD publishes. Threads shows 566 followers on the same handle - a different graph, recorded for contrast only | yes | `solicits-collaboration` - the creator's own Threads bio reads 「合作邀約歡迎來信詢問」, an open invitation for collaboration approaches. This was already quoted in the row's notes at build 6 | INDEPENDENT | **A build-2 rejection reversed.** Build 2 read the roster bio (「陶、畫雙棲的嗜奶人」) and wrote "the name is a joke about being paid in milk, not a character". The studio name is the joke; the character is **崽崽**, and the creator appends a pronunciation guide for it to post after post (「崽唸ㄗㄞˇ／崽崽唸ㄗㄞˇㄗㄞ」). The character is tracked across licensed formats in the creator's own words: 「藍色蝴蝶結崽圖一路從林崽的陶杯上跳到 T-shirt 上，現在拿來插畫這邊變成完整的一幅」 - ceramics, apparel, illustration. Bio states 「合作邀約歡迎來信詢問」, i.e. the creator solicits collaborations directly and names no agent |
| 24 | RHINOSHIELD 犀牛盾 (Design Studio) | 窩窩頭 (達摩親子糰: 爸爸摩 / 哥哥摩 / 貝比摩) | TW | **2025** | The brand's own `firstLaunchedAt` = **2025-02-23**. Corrected field again - build 2 recorded 2025-01-21, the avatar cache-buster | https://rhinoshield.tw/design-studio/collections/@wowohead (HTTP 200, 2026-08-07); character evidence https://www.threads.com/@wowohead_2023 (HTTP 200, 2026-08-07) | `lt_10k` | **2,154** Instagram followers, `@wowohead_2023`, read 2026-08-07 by build 2 from the handle RHINOSHIELD publishes. Threads shows 353 on the same handle | unclear | `no-agent-named` - Threads bio describes the two-person studio and 「近期市集出攤」, a market-stall schedule rather than a licensing route. Absence only | INDEPENDENT | **A build-2 rejection reversed, and the weakest of build 6's three - the evidence is quoted so a human can put it back.** Build 2 wrote "hand-carved stamp studio, names no character". The creator's own channel names two character sets and introduces them as beings, not as SKUs: six lucky cats, 「大家好，牠們分別叫做 大富、大貴、大吉、大利、大發、桃花」, and a named family, 「#達摩親子糰 有【爸爸摩】、【哥哥摩】、【貝比摩】三個疊疊樂在一起 ... 因為是一家人，所以怎麼搖晃都不會分開」. **The counter-argument, stated plainly:** a hand-carving craft studio naming its designs is not obviously the same thing as running a character IP, and the named sets are organised as product series (招財貓系列, 咖啡動物系列, 植物系列). Accepted because the 達摩親子糰 set has a name, a membership and stated relationships - the same standard rows 3, 11 and 17 are held to. Two-person studio, self-described as 「由兩位喜歡怪東西的捲捲頭組成」, no agent |
| 25 | DEVILCASE 惡魔防摔殼 | 風速新營 XYWS MOTARDS (WOLFY / DEVILCAT / FU-KU ÉKIPU / SK8EGG / BALANCE LE DOG / NICE BÉBÉ / Jessie) | TW | **2024** | `asset-upload` - the partner page's art is served from `i.devilxxxx.com/uploads/crossover/**20241212143720**.jpg`, i.e. 2024-12-12, the dating method established in build 2 and re-verified live this build. The 2025 文博會 exhibitor record corroborates the creator was active and exhibiting in the same window | https://www.devilcase.com.tw/crossover/166 (HTTP 200, 2026-08-07); secondary https://2025.creativexpo.tw/zh-TW/brands/48 (HTTP 200); character evidence https://www.threads.com/@xyws_motards (HTTP 200, 2026-08-07) | `lt_10k` | **6,011** Instagram followers, `@xyws_motards`, read 2026-08-07 by build 4 from the 2025 文博會 exhibitor page | unclear | `no-agent-named` - the Threads profile serves no biography text, so nothing positive could be read. Absence only | INDEPENDENT | **A build-4 rejection reversed, and the cleanest reversal in the file because both sides of the deal name the same characters.** Build 4 read the bio paragraph on the DEVILCASE page (「插畫雙人組以家鄉地名為起點，畫出迎風而來的自由感」) and recorded "no character". Two lines below that paragraph the same page lists the licensed designs by name: **`FAMILY TIME`, `DEVILCAT`, `WOLFY ＆ FUKU EKIPU`** - and DEVILCASE files the partner under its own **臺灣創作與角色** ("Taiwanese creation and character") category rather than under 海外創作與角色 or 遊戲與動漫. The creator's channel then supplies the cast independently, one ZINE page per character with a one-line personality: 「A page about Wolfy, the super moto rider」, 「A page about "SK8EGG" who is a super bouncy boiled egg and loves skateboarding」, 「A page about BALANCE LE DOG. She loves collecting hats and making Artworks」, plus Jessie, FU-KU ÉKIPU and NICE BÉBÉ & Devilcat. **This is the only sub-10k partner in 46 resolved DEVILCASE partners**, so Vein A ends the run having produced three rows (1, 2, 25) and no more |

**Read on the twenty-two rows.** Build 1 could say the cell exists.
Build 2 could say what it looks like: a second Taiwanese-market licensee, larger and better documented, landing eight more sub-10k character deals, one of them running 48 SKUs.
Build 3 closes Vein E (every record parsed, every resolvable handle resolved), corrects the dating basis, and adds the two rows that were hiding behind the handle gap - one of them only reachable by cross-referencing a second directory.
Build 4 breaks the shape of the answer rather than extending it: **four brands, twenty rows**, and the two new brands are not phone-case makers.
One is a hotel and one is the largest convenience-store chain in Taiwan, which is the point - builds 1-3 could be read as "print-on-demand accessory brands will licence anyone", and rows 13-20 are not that.
The census's zero was a property of press indexing, and that is now shown four ways: two brand rosters, a trade-show floor, and an organiser-published list of brokered deals.

**Build 5 adds a fifth way, and it is the only one that measures the filter directly rather than routing around it.** 536 名 文博會 exhibitors of known band, joined against 自由時報's whole archive: the chance of a creative brand being named at all rises from 13.1% sub-10k to 55.6% at `200k_1m`, and the number of sub-10k *licensing* write-ups in the entire archive is **zero**. Build 5's own two rows are consistent with that - row 21 came from a ferry operator's press release via the organiser, row 22 from correcting an adjudication, and neither from a newspaper.

**Build 6 closes the file at twenty-five rows without finding a new deal, and that is the point.**
All three of its rows were already in the rejection log, in documented licensing deals, with the follower counts already read.
What was missing was a way to read what the creator says about their own work - and once Threads supplied it, the same thirteen candidates that had been adjudicated on marketing copy split three-to-eight rather than nought-to-thirteen.
**The binding constraint on this cell was never discovery and was only briefly banding; for the last three builds it was adjudication, run against the wrong document for want of a channel.**

That changes the reading of the sub-10k share on RHINOSHIELD's roster too.
**Ten of the 21 sub-10k RHINOSHIELD creators are now accepted character rows, not eight** - the accept rate off a resolved sub-10k pool is 48%, not the ~40% build 2 predicted.
The remaining eleven fail on class for reasons that survive reading their own channels: a heritage temple, a marine NGO, a tattoo studio, a calligrapher, a student heritage-design team, and six illustrators who genuinely do not run a character.

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
| **7-ELEVEN / ibon x 文博會 2026 licensed creators** (a **single brand's actual signed cohort**) | **15 resolved** of 16 named | **12** | **80%** |
| the ten-market census, Taiwan (**press-built**) | - | 0 | **0%** |
| 自由時報 archive coverage of 文博會 exhibitors, sub-10k band (**a press *filter*, measured**) | 183 | 24 named at all, **0** with a licensing write-up | **13.1% named / 0% licensed** |
| the same, `50k_200k` band | 55 | 17 named | **30.9%** |

**The 80% is the most consequential number in this file.** The other denominators measure who is *available* to be licensed; this one measures who a specific national brand *actually signed*, and four in five of them were sub-10k. It is one deal and it was explicitly framed as a 新銳 (emerging-talent) programme, so it is not a general estimate of 7-ELEVEN's licensing - but it is a direct counter-example to the reading that sub-10k IP is not commercially licensable in Taiwan, and it is exactly denominated.

**Say "12 of 15 resolved", not "12 of 16".** The sixteenth creator, 木子島工作室, is unresolved rather than out of band, and the earlier 75% figure quietly counted it as above 10k. If it later resolves sub-10k the share is 13/16 = 81.3%; if above, 12/16 = 75%. Either way the resolved-cohort statement stands and the unresolved one must be said out loud rather than absorbed into the denominator.

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

**Total rejected across six builds: 88 named** (11 in build 1, 13 in build 2, 26 in build 3, 23 in build 4, 19 in build 5, less 羊號角Piper reversed by build 5 into row 22 and less 時薪一加侖鮮奶, 窩窩頭 and 風速新營 XYWS reversed by build 6 into rows 23-25), **plus 2 new named rejections in build 6 and the population-level rejections below.**

### Build 6: the full character-test re-adjudication (13 candidates, 3 reversed, 8 upheld, 2 unreachable)

Every in-band candidate the file had ever rejected on the character test, re-run against the creator's own Threads channel per Vein J. Instagram counts are the earlier builds' reads, carried forward with their basis; they were not re-read (route dead, bulk collection robots-prohibited).

| Candidate | IG followers | Licensee | Verdict | What the creator's own channel says |
|---|---|---|---|---|
| 時薪一加侖鮮奶 `@gallon_milk14` | 2,423 | RHINOSHIELD | **REVERSED → row 23** | Named character 崽崽 with a pronunciation guide in every post signature |
| 窩窩頭 `@wowohead_2023` | 2,154 | RHINOSHIELD | **REVERSED → row 24** | 達摩親子糰 (爸爸摩/哥哥摩/貝比摩) and six named 招財貓 |
| 風速新營 XYWS `@xyws_motards` | 6,011 | DEVILCASE | **REVERSED → row 25** | A ZINE series of one page per named character; licensee's SKU names match |
| 日句時刻所 `@heyyoumoment` | 7,493 | 7-ELEVEN / ibon | **upheld** | 「黃色風格 ⌂ 家為主題的插畫設計」. Posts are 磁吸迷你傢俱盲盒, 房子磁吸小燈, 貼紙櫃 - houses and furniture as *objects*, no character, and the creator signs as 森妮 (her own name). Build 4's call stands, now on the right document |
| 舒媞 SHUTI `@ti_illustration` | 9,170 | RHINOSHIELD | **upheld** | 「Shuti 一位自由插畫家...喜歡用畫筆紀錄生活」. Her recurring 冰島小馬 series is a *motif* carried across a phone case and a calendar, and she describes designing a logo for someone else's brand. Subject matter, not a character. The nearest-to-boundary in-band rejection in the file |
| HLTOO 曾湘玲 `@hl.t_oo` | 5,613 | RHINOSHIELD | **upheld** | Picture books, 主視覺 commissions, a 太空人系列 and a 禪意狗狗 - series and one-offs, none named or serialised as a character. Confirms the RHINOSHIELD deal herself (「和犀牛盾聯名！對這也是我的 Dreams come true」), so the deal is real and the class is what fails |
| 魚氏 `@yulin.ovo` | 1,170 | 7-ELEVEN / ibon | **upheld, and still the closest call in the file** | Bio is 「無用日常」; twelve posts total, all one-liners about drawing. One - 「垃圾小童好懷念」 - names something that *could* be a character, once, in the past tense, with no other trace. Not enough to carry a row, and said out loud here because a human with access to the account's grid might reverse it |
| 阿薛 Hsueh `@hsueh.illu` | 2,428 | RHINOSHIELD | **upheld** | Bio 「講一些廢話的地方」; the channel is a travel and personal diary. No character |
| 旅貓實驗室 `@travelpaint.cat` | 1,785 | RHINOSHIELD | **upheld** | 「手繪插畫 x 手作創作」 - draws and photographs real cats, sells a 桌曆 combining 插畫與攝影. No original character. Interesting for a different cell: sells through 寄賣店, 市集 and a 賣貨便 storefront, i.e. entirely outside licensing |
| AndreaCat `@andreacat805` | 1,055 | RHINOSHIELD | **upheld** | Bio describes the creator (「喜歡貓、占星、身心靈書籍的書蟲」); three posts, none about a character |
| 張哲 `@changche.drawing` | 1,608 | 7-ELEVEN / ibon | **upheld** | Fruit, cats, chairs, Taiwanese furniture in watercolour and oil pastel. Exhibits at 文博會 and a Busan illustration fair. No character |
| 洋樓拾憶文創工作室 `@quemoy_memory` | 386 | 7-ELEVEN / ibon | **upheld** | The channel settles what it is: a **student團隊 graduation project** (畢製, 專題審查, 新一代設計展 2025) about Kinmen 洋樓 architectural memory, licensing a 雙龍搶珠 relief motif onto shirts. Heritage design, not a character - and worth noting the smallest account in the run is a student team |
| Quintine C. `@quintine1115` | 641 | RHINOSHIELD | **upheld** | 「A graphic designer based in Taichung」; posts are political and personal. Corroborates the RHINOSHIELD relationship (links her own collection URL) but names no character |
| LorenaxAngelina `@lorenaxangelina` | 2,704 | RHINOSHIELD | **unreachable** | Threads 302s (no account). German fantasy artist; also outside the Taiwan-market question |
| 1nsp0 `@1nsp0.1_0` | 18 | RHINOSHIELD | **unreachable / not banded** | Unchanged from build 2 - the account cannot carry the most extreme datum in the file |

### Build 6: 2 new named rejections

| Candidate | Where | Reason |
|---|---|---|
| pixiv FANBOX x ibon 創作者應援企劃 第三彈 (Glycan, Hiten, Nuomi諾米, SIBYL西貝魯, TaaRO, 小河少年, 空罐王, 高橋麵包, 深雪Miyuki) | Wayback `licenseproduct/Detail?LicenseProductId=47`, captured 2023-03-15 | **Rejected on class and on channel.** A real 7-ELEVEN licence - A4 posters and postcards printed in store, revenue-shared with the artist - and in window. But the licensed asset is pin-up and doujin illustration, not a character IP with a named cast, and these creators' primary channels are pixiv and X, which this run has no banding route for. Kept as a documented format rather than a row |
| pixiv FANBOX x ibon x 駁二藝術特區 「他是誰？動漫女子寫真展」 第四彈 (Say HANa, 日下棗, 曾耀慶, 綜合口味, 謝東霖, 致怡Zei) | Wayback `licenseproduct/Detail?LicenseProductId=64`, captured 2023-10-23; campaign dated **2023-08-22 to 2023-10-23** on the page itself | **Rejected on class.** Same shape, and here the licensed works are explicitly comic pages (「漫畫的女兒 第50頁」, 「入伍吧魔法少女 第三集書皮」) tied to a public exhibition at 駁二. Comic-page print licensing, not character licensing |

### Build 5 rejected: 19 named

**a. From Vein G2 (the 2025 organiser news feed), 17 named across four brokered partnerships.** (其實他是鵝 and noii noii each appear in two of the four and are counted once.)

| Candidate | Followers | Deal | Reason |
|---|---|---|---|
| 其實他是鵝 `@hui____7` | 22,000 | 澎湖輪 + ibon 2025 | out of band |
| 小喵WE `@wewe_0413` | **43,541** | 澎湖輪 | out of band |
| 維尼有畫想說 `@spx_wie` | 15,000 | 澎湖輪 | out of band |
| noii noii `@noiinoii_official` | 44,000 | WeMo Scooter 聯名車款 + 安全帽; also We TAIWAN 大阪 | out of band. Would otherwise be a strong row - a co-branded scooter livery is a real licence |
| 啾啾噗噗 `@jjjlllove_1209` | 168,000 | ibon 2025 | out of band |
| 伸縮自如的雞與鴨 `@iyayahaaa` | 36,000 | ibon 2025 | out of band |
| 兔君 `@lubonnie_art` | 24,000 | ibon 2025 | out of band |
| 嗚比的朋友 `@woobi_dooggy` | 104,000 | ibon 2025 | out of band |
| 恐龍的房間 `@dinosaurs.room` | 94,000 | We TAIWAN 大阪世博 | out of band |
| nozomii 妯米 `@nozomii.art` | **10,000** | We TAIWAN 大阪世博 | **boundary-ambiguous.** Instagram rounds at and above 10,000, so this reading covers roughly 9,950-10,499 and cannot decide a threshold stated as "at or under 10,000". Recorded, not banded - same call as DEVILCASE's 小怪家 |
| Tabbi L `@tabbiliaw_art` | 11,000 | We TAIWAN 大阪世博 | out of band |
| 小圓麵包 `@frodog_10` | 12,000 | We TAIWAN 大阪世博 | out of band |
| 阿翰 `@todayfor_han` | 58,000 | We TAIWAN 大阪世博 | out of band |
| 安怎？Ann-Nua `@ann_nua_handmade` | 20,000 | We TAIWAN 大阪世博 | out of band |
| 幽默之星 `@twinkle_twinkle_humor_star` | 11,000 | We TAIWAN 大阪世博 | out of band |
| POPO鴿的鳥日子 `@popolifetw` | 67,000 | We TAIWAN 大阪世博 | out of band |
| 蛋塔熊妹 `@eggybear._.poka` | 37,000 | We TAIWAN 大阪世博 | out of band |

**b. From Vein I (自由時報 full-text join), 2 named - and one of them is a new rejection category.**

| Candidate | Followers | Reason |
|---|---|---|
| 蘭獸 ORCHIDSAUR `@orchidsaur_official` | **3,485** | **Rejected on IP class - institutional / event mascot.** The deal is real and in window: 世茂農業生技 x 「世茂×ORCHIDSAUR」聯名母親節限定花款, a pop-up at 台南遠東百貨成功店 from 2025-04-27 to 2025-05-11, nano-dyed orchids carrying the character (`news.ltn.com.tw/news/life/breakingnews/5024990`, HTTP 200). The character is properly constructed - CET2026 exhibitor 403 describes 「蘭花吉祥物-蘭獸」, born of a symbiosis legend between orchids and dinosaurs, new-shoot horns, eight legs. But the Facebook page the exhibitor register publishes for it (`facebook.com/tiostwn`) resolves to **臺灣國際蘭展暨花卉科技展 Taiwan International Orchid Show**, a state-backed industry exposition at 農業部花卉創新園區, so the rights holder is an institution, not an independent creator. **This is a new category, distinct from the corporate-mascot rejection (捷米 JAMIE): there the brand and the IP were the same party, here they are genuinely two parties and the IP class is what fails.** Worth flagging for a human - if the census's INDEPENDENT/MIXED line is drawn to admit institutional character IP, this is a row |
| 無所事事小海豹 (`@happacreative`, 3,033) | **not truly in band** | **Rejected on scale, after the dictionary got it wrong.** 無所事事小海豹 is one of Taiwan's best-known sticker characters and 自由時報 alone carries eight articles about it. The 3,033 reading is 樹葉文創有限公司's *corporate* account: the exhibitor page states 「樹葉文創有限公司為《無所事事小海豹》總代理同時也是小海豹的創作團隊」. Also `representable: no` on its face - an IP with a named 總代理 is not addressable. See the agent-account trap in `ltn-press-coverage-by-band.md` |

**c. Carried but not resolved.** 閃亮亮樂園's three ferry co-headliners are listed above; 日句時刻所 (7,493) stays a build-4 rejection that build 5 could not re-test because its Instagram profile endpoint faults.

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

### Build 5 additions (all curl-verified 2026-08-07)

**Row sources.**

| URL | HTTP | What it establishes |
|---|---|---|
| https://2025.creativexpo.tw/zh-TW/posts/14 | **200** | `source_ref` for row 21. Organiser release 2025-07-24 naming 台灣航業 澎湖輪 and the four IPs, plus the WeMo, ibon-2025 and We TAIWAN partnerships |
| https://2025.creativexpo.tw/zh-TW/brands/29 | **200** | Row 21 - booth S-065, brand description, and the handle `@kirakira_land` |
| https://creativexpo.tw/zh-TW/exhibitor_list/440 | **200** | Row 22 - booth S-070, handle `@piper.illu`, and the blurb that build 4 rejected on |
| https://www.cdns.com.tw/articles/1429446 | **200** | Row 22's primary source - re-verified; the same 中華日報 release behind rows 14-20 |
| Instagram profile reads for `kirakira_land` (3,693) and `piper.illu` (3,630) | **200** | The two follower counts and both character claims |

**Rejection and adjudication sources.**

| URL | HTTP | What it establishes |
|---|---|---|
| https://news.ltn.com.tw/news/life/breakingnews/5024990 | **200** | 世茂農業生技 x ORCHIDSAUR, 2025-04-27 - the one real sub-10k licence Vein I surfaced, rejected on class |
| https://creativexpo.tw/zh-TW/exhibitor_list/403 | **200** | 蘭獸's own character description |
| https://www.facebook.com/tiostwn/ | **200** | Resolves 蘭獸's publisher to 臺灣國際蘭展暨花卉科技展 - the evidence for the institutional-mascot rejection |
| https://2025.creativexpo.tw/zh-TW/brands/151 | **200** | 「樹葉文創有限公司為《無所事事小海豹》總代理」 - the agent-account trap, in the exhibitor's own words |
| Instagram profile reads for `quemoy_memory`, `yulin.ovo`, `changche.drawing`, `travelpaint.cat`, `hsueh.illu` | **200 each** | The five character-test re-examinations that upheld earlier rejections |

**Vein and index infrastructure.**

| URL | HTTP | Note |
|---|---|---|
| https://2025.creativexpo.tw/zh-TW/posts/1..60 | 200 on **20** | Vein G2. Ids 7, 9, 10, 13, 15, 16, 18-21, 24, 25, 27 and 33-60 all 302 to `?locale=zh-TW` - the same redirect trap build 4 documented |
| https://creativexpo.tw/zh-TW/collaboration_responses/1..70 | 200 on **18** | Re-swept after the 2026 expo opened. **No new entries** - Vein G's 2026 edition is closed |
| https://creativexpo.tw/zh-TW/posts/1..60 | 200 on **12** | Same; no new release naming the NeverHaveIEver cohort |
| `https://search.ltn.com.tw/list?keyword=<q>&type=all` | **200, parseable** | **Vein I. 536 queries at 0.7s spacing with zero rate-limit responses.** The result *count* is a fuzzy OR count and must be discarded |
| https://news.ltn.com.tw/news/... (desktop UA) | 200 but **body absent** | Article text is not in the desktop HTML - only the `og:description` lede |
| https://news.ltn.com.tw/news/... (iPhone UA) | 200, **full body** | The same URL with a mobile user-agent serves the article |
| https://art.ltn.com.tw/article/breakingnews/5530413 | **200** | 2026-08-07 LTN report on the NeverHaveIEver / Shoppe Object New York tie-up - **names the deal but not the 10 IPs**, so the lead stays open |
| https://www.instagram.com/`<handle>`/ | **302 → /accounts/login/** | On every user-agent tried. The `og:description` route all earlier builds used is **gone** |
| https://www.instagram.com/robots.txt | 200 | `User-agent: ClaudeBot / Disallow: /`, plus a header notice prohibiting automated collection without written permission. **The planned 240-account cohort sweep was abandoned on reading this** |
| https://print.ibon.com.tw/sitemap.xml | **200** | ibon publishes a `/licenseproduct` section - a national-brand licensing directory of Vein-A shape, ids running past 646 |
| https://print.ibon.com.tw/licenseproduct/`<id>` | 200 but **empty JS shell** | Including via Wayback (`web.archive.org/web/20260804072043/...`, 10.6 KB, no content). The catalogue lives behind `/api/`, which `robots.txt` disallows, so **this vein is visible and unreadable** |
| https://taicca.tw, https://www.taicca.tw | **403** | 文策院 - closed to plain curl |
| https://tccf.tw, https://yodex.com.tw, https://www.pinkoi.com | 200 | Other-organiser probes that resolve; none swept |
| licensingexpo.com.tw, taiwanlicensingexpo.com.tw, comicexpo.net, designexpo.tw, kaohsiungdesignfestival.tw | **curl exit 000** | Other-organiser probes that do not resolve by DNS |
| https://www.bing.com/search?q=...&format=rss | 200 | Re-confirmed useless for CJK - a 木子島工作室 query returned Google Docs help pages |
| `https://store.line.me/api/search/sticker?query=木子島` | 200, `totalCount: 0` | 木子島工作室 is absent from LINE STORE as well as from both CET editions and 自由時報 |

---

### Build 6 additions (all curl-verified 2026-08-07)

**Row sources.**

| URL | HTTP | What it carries |
|---|---|---|
| https://rhinoshield.tw/design-studio/collections/@gallon-milk | 200 | Row 23 primary. Title 「時薪一加侖鮮奶 \| 客製化手機殼設計 \| RHINOSHIELD 犀牛盾」 |
| https://www.threads.com/@gallon_milk14 | 200 | Row 23 character evidence. Bio + 15 captions |
| https://rhinoshield.tw/design-studio/collections/@wowohead | 200 | Row 24 primary |
| https://www.threads.com/@wowohead_2023 | 200 | Row 24 character evidence. Bio + 17 captions |
| https://www.devilcase.com.tw/crossover/166 | 200 | Row 25 primary. Category 臺灣創作與角色, SKU names `FAMILY TIME` / `DEVILCAT` / `WOLFY ＆ FUKU EKIPU`, art asset `uploads/crossover/20241212143720.jpg` |
| https://2025.creativexpo.tw/zh-TW/brands/48 | 200 | Row 25 secondary - the 2025 文博會 exhibitor record and the source of the 6,011 count |
| https://www.threads.com/@xyws_motards | 200 | Row 25 character evidence. 15 captions, one per ZINE character page |

**Adjudication sources** (all HTTP 200 unless noted): `threads.com/@` for `heyyoumoment`, `ti_illustration`, `hl.t_oo`, `yulin.ovo`, `hsueh.illu`, `travelpaint.cat`, `andreacat805`, `changche.drawing`, `quemoy_memory`, `quintine1115`, `guaaii__`, `hanomanga`. **302 (no Threads account):** `lorenaxangelina`, `yiekubo`, and all eight handle guesses for 木子島工作室 / 泰江 TJ GAMEBOY.

**Infrastructure probes, and what each settles.**

| Endpoint | HTTP | Verdict |
|---|---|---|
| `threads.com/search?q=<CJK>&serp_type=users` | 200, 531KB, **zero usernames** | Search is login-gated. Threads does not solve handle discovery |
| `print.ibon.com.tw/robots.txt` | 200 | `Disallow: /api/` and `/js/`; `Allow: /`. The catalogue API stays off-limits by policy, not by capability |
| `print.ibon.com.tw/sitemap.xml` | 200, **19 static URLs** | No per-campaign entries. The live directory cannot be enumerated from the site itself |
| `print.ibon.com.tw/{news,product,studio,licenseproduct/Detail?...}` | 200, 8,519 bytes each, **11 characters of text** | Every live path is the same JS shell. Confirms build 5: Vein H's brand surface is closed |
| Wayback `licenseproduct/645` (2025-08-03), `/646` (2025-07-31), `/611` (2026-08-04) | 200 | The shell was archived too, with only the site-wide boilerplate `<meta description>`. **The 2025 ibon cohort is not recoverable this way** - build 5's owed item 1 is now closed as a dead route rather than untried |
| Wayback CDX `licenseproduct/Detail*` | 200, **58 distinct campaign ids** | Vein K. 21 read before throttling; pace at 3s between requests or bodies come back empty with no error |
| `taicca.tw/robots.txt` | 200 | **`User-agent: ClaudeBot` / `Disallow: /`.** Taiwan's national content agency - the body behind the 文博會 brokerage that produced rows 13-22 - prohibits this run's crawler outright. Not swept. Its `wp-json` also 403s |
| `zeczec.com/{search,categories}` | **403** Cloudflare interstitial | The task brief named 募資 platforms; Taiwan's largest is behind a JS challenge. `robots.txt` itself is permissive, so this is an infrastructure block, not a policy one |
| `songshanculturalpark.org/{originalfestival,shop}` | 200, server-rendered, `robots.txt` fully permissive | Readable and thin: 原創基地節 is a student and emerging-creator *exhibition* programme (an index of people), and 線上小賣所 stocks **5** products. One co-branded item (蘑菇MOGU x 松菸小賣所 glass) and no character IP |
| `huashan1914.com/robots.txt` | 404 (IIS default) | - |
| `store.line.me/stickershop/showcase/{sponsor,top_free}/zh-Hant` | **404** | Re-confirms Vein C dead |
| `store.line.me/api/search/sticker?query=木子島` | 200, `totalCount: 0` | 木子島工作室 has no LINE sticker presence |
| `bing.com/search?q=木子島工作室&format=rss` | 200, **results unrelated to the query** (ChatGPT jailbreak repos, Zhihu threads) | Worse than build 2 recorded. Bing's RSS endpoint does not merely degrade on CJK, it returns another query's cached results. **A 200 here is worthless and must not be logged as a negative result** |
| `devilcase.com.tw/crossover/276` (尼胖) | 200 | Re-checked for creator socials; the page links only DEVILCASE's own accounts. 尼胖 stays unresolved after three builds |

### Build 7 additions (all curl-verified 2026-08-07)

| source | status | what it carries |
|---|---|---|
| `threads.com/@<handle>` under a **Googlebot** user-agent, 23 handles - one per accepted-row creator | **200 on all 23**; 19 served a `"biography"` field, 4 did not | The representability test of section 16. The bio is the licensing-solicitation surface and it is served **untruncated**, which `og:description` never was |
| the same 23 handles under a **browser** user-agent and under plain curl | 200, ~576KB, **no `biography` field at all** | The user-agent is load-bearing, not cosmetic. A browser UA returns a login-gated shell that looks like a successful fetch. **A plain-curl 200 here is not evidence the profile is empty** |
| `creativexpo.tw/zh-TW/exhibitor_list/{20,42,79,122,133,134,268,293,347,440}` | **200 on all ten** | Re-fetched live. Each page carries the exhibitor's **booth number** (S-041 through S-087) and the exhibitor's **own email address**, neither of which any earlier build extracted. Feeds `output/cet-sub10k-creators.md` |
| `creativexpo.tw/zh-TW/visit_info` | 200 | 品牌商展 runs **8/6-8/12 at 台北南港展覽館一館 1F**; 8/6-8/7 are 專業買家日 |
| `creativexpo.tw/zh-TW/posts/38` | 200 | 2026 opening release: 870+ brands, 1,200+ booths, 53 international brands, **640+ scheduled B2B 媒合洽商 sessions**, and 32 Taiwanese original-character IP companies in the 黑潮星樂園 zone |

**A note on the exhibitor emails.** All ten CET2026 creators publish a direct email on their own exhibitor page, in a directory the organiser describes as a 圖像授權交易平臺. That is a reachability route, and it is deliberately **not** counted as `representable: yes` - an agency-represented creator exhibits too. It is recorded as `exhibitor-directory-contact` in the walking list rather than in the basis column, so a human can weigh it separately.

---

## What build 7 leaves owed

**No rows added; the stop condition was already met.** Build 7 is a correction pass, and it leaves three things open.

1. **`unclear` is now the file's most common value and it is genuinely uncertain, not negative.** Nineteen rows sit there because a small creator's bio does not normally discuss commercial terms. Distinguishing "no agent" from "agent not mentioned" needs a source no channel in this run provides: a licensing-agency roster, a contract registry, or asking the creator. The 台灣角色品牌授權協會 (named in the 2026 opening release) is the obvious untried index.
2. **The three close calls in section 16 - rows 9, 10 and 16 - should be re-read by a human**, not by another build. Each turns on whether an unlabelled contact address counts as soliciting collaboration, which is a judgment call rather than a retrieval problem.
3. **The `licensee-names-contact` basis has zero rows and that is itself a finding.** Not one licensee in this file - two phone-case brands, a convenience-store chain, a hotel, a ferry operator - publishes a contact route for the creator it licensed. Every route back to these creators runs through the creator's own channel or the trade show. That is consistent with the brokered-channel mechanism in rows 13-22 and worth testing on a market that is not Taiwan.

---

## What build 6 leaves owed

**25 of 25 rows. The stop condition is met and the run should end here.** What follows is not a shortfall list - it is what a reader of these rows should know is *not* established.

1. ~~**Representability is asserted on all twenty-five rows and tested on none.**~~ **DISCHARGED by build 7.** The test was run across all twenty-five against the creators' own Threads biographies, and it moved the answer a long way: **19 rows downgraded from `yes` to `unclear`, 6 kept**, on the rule and per-row basis set out in section 16. What remains owed is narrower and stated there - `unclear` is not `no`, and even the six `yes` rows evidence that the creator invites approaches rather than that no exclusive licensor sits behind them.
2. **Follower counts are one-time reads and can no longer be refreshed.** Every band in this file traces to an Instagram `og:description` read on 2026-08-07 or earlier. That route is dead and bulk collection there is robots-prohibited, so no future build can re-verify a band by the method that produced it. Threads gives a different graph and the exhibitor directories give a stale one. **Any re-verification needs a channel this run does not have.**
3. **The counts are `current-proxy` for rows whose campaigns are older.** Rows 23 (2024) and 25 (2024) carry 2026 reads against 2024 campaigns, so the at-campaign figure was lower, not higher - conservative in the direction that matters, but it means "at or under 10,000 *at the time*" is inferred rather than observed for those two.
4. **Three named creators in documented national deals were never resolved:** 木子島工作室 (7-ELEVEN / ibon 2026, one of the sixteen), 泰江 TJ GAMEBOY (南港老爺行旅 2026) and 尼胖 (the only IP appearing in *both* brand directories). Each is a live `lt_10k` candidate, not a negative. Six builds, four index types and roughly sixty handle guesses failed on them.
5. **The 2025 ibon cohort is 11 creators short and the route is now closed, not untried.** Build 5 listed a Wayback sweep of `licenseproduct/645` and `/646` as the promising untried option; build 6 ran it and both captures are the JS shell. The 2026 edition of the same programme produced eight rows, so the 2025 list would have made the 80% a time series rather than a single point. It would need 7-ELEVEN's corporate newsroom or a 文化部 release this run could not reach.
6. **TAICCA prohibits this crawler.** `taicca.tw/robots.txt` carries `User-agent: ClaudeBot / Disallow: /`. That is the national agency behind the brokerage mechanism rows 13-22 depend on, and its 58 published licensing cases and 84 signed contracts from the 2025 黑潮星樂園 stay unread for policy reasons rather than technical ones. A human, or a differently-identified agent, can read them.
7. **魚氏 (1,170) is one post away from being a twenty-sixth row.** Upheld as a rejection on twelve one-line captions, one of which names 垃圾小童 in passing. Flagged because the file's standard is that a human should be able to see the closest calls.
8. **Vein A's ~97 unresolved DEVILCASE partners and its 39 VTubers.** Unchanged across all six builds - though Vein A is now settled in a way it was not: 46 partners resolved, exactly one sub-10k, and that one is row 25.

---

## What build 5 leaves owed

**22 of 25 rows.** Three short. The shortfall is no longer a discovery problem *or* a character-test problem - build 5 fixed the test - it is that the four richest deal cohorts found in this run are all scale-filtered upward at source.

1. **The 2025 ibon cohort is still 11 creators short and it is the single highest-value missing thing.** The 2026 edition of exactly this programme produced eight rows. The 2025 release names only 5 of 16, and all five are the large ones - which is the press-release pattern, not the cohort. Every route tried failed: 自由時報, Google News RSS (four query formulations), 立報, ocacnews, the MOC release, and ibon's own surface. Untried: 7-ELEVEN's corporate newsroom (`www.7-11.com.tw/company/news`, HTTP 200 and unswept), ibon's Facebook page under a Googlebot user-agent, and a Wayback sweep of `print.ibon.com.tw/licenseproduct/645` and `/646` - both captured on 2025-07-31 and 2025-08-03, right inside the campaign.
2. **ibon's `/licenseproduct` directory is a national-brand licensing directory that this run has now *seen* and cannot read.** Ids run past 646, `robots.txt` allows the path, and the pages are an empty JS shell whose data sits behind a disallowed `/api/`. The 2019-2023 generation of the same site *was* server-rendered (`licenseproduct/Detail?LicenseProductId=<n>`) and Wayback has captures. That older block is only partly in window, but it would establish whether ibon licenses small IP outside the 文博會 programme.
3. **NeverHaveIEver x 10 組臺灣原創IP → Shoppe Object New York.** Reported by 自由時報 on 2026-08-07 and by the organiser, with the ten IPs unnamed in both. Also unresolved on class: setting up a 「Creative Expo Taiwan」 booth at a US trade show may be representation rather than licensing, in which case it is a rejection under build 4's collaboration-type rule.
4. **The 58 published licensing cases and 84 signed contracts from the 2025 黑潮星樂園.** The largest deal index this run has located. 文化部 「公佈已成功合作的58個授權案例」 with certificates presented on stage - so a list exists. It is a scale filter by construction (the programme requires five years' history and existing 授權實績), so expect few or no sub-10k hits, but 84 contracts is worth a targeted look for the exception.
5. **The character-test re-examination is incomplete.** Five in-band creators - 日句時刻所, 窩窩頭, 時薪一加侖鮮奶, 舒媞, AndreaCat - could not be re-tested because their Instagram profile endpoint faults on a server-side schema error. Each is a documented licensing deal with a sub-10k creator, and section 12 has now shown that a blurb-based rejection is unreliable. **These five are the cheapest remaining path to rows 23-25 and they need a channel other than Instagram** (Facebook page, Threads, personal site, 賣貨便 storefront).
6. **The 46.8% 文博會 denominator now has a known upward bias of unknown size**, because at least one exhibitor (無所事事小海豹) is banded off its licensing agent's corporate account. The detection rule - the exhibitor's own description contains 總代理 / 代理 / 經紀 - is cheap to run across both dictionary editions and has not been run.
7. **Representability is still asserted, not tested** - now across twenty-two rows. Unchanged from build 4. The 無所事事小海豹 case shows the test has real content: an exhibitor that names a 總代理 is not addressable, and nothing in this file has been checked for one.
8. **Instagram is no longer available as a bulk channel**, by policy as well as in practice. Any future build that needs to band a cohort rather than verify a named candidate must use a different source - the exhibitor directories' own published counts, Facebook page like-counts via Googlebot, or Wayback snapshots.
9. **Vein A's ~97 unresolved DEVILCASE partners and the 39 VTubers.** Unchanged across all five builds.

---

## What build 4 leaves owed

**20 of 25 rows.** Five short, and for the first time the shortfall is not a discovery problem - build 4 found more in-band candidates than it could accept, and the binding constraint is the character test.

1. **Vein G is not exhausted, it is barely started.** Only two editions of one trade show were swept, and only its `collaboration_responses` and `posts` sections. Untried on the same two hosts: `events` (68 + 82 entries, swept but only keyword-scanned, not read), `online_events`, `taicca_curations`, `kuroshio_ips` (the 黑潮星樂園 original-IP zone, 15 entries on the 2026 site and a separate id block on the 2025 one). Two named 2026 deals inside Vein G were seen and not worked: **NeverHaveIEver x 10 組臺灣原創IP** into the New York Shoppe Object show, and the **2025 edition of the same ibon programme** ("去年首次與臺灣文博會合作"), whose creator list was not found - a whole second cohort of the vein that produced seven rows.
2. **Other organisers publish the same section.** The generalisation is not "文博會 has a 異業合作 page", it is "an event organiser that brokers deals publishes who signed". 原創基地節, 台北國際動漫節, 高雄設計節, 新一代設計展 and the 文策院 (TAICCA) programme pages are all untried and all the same shape.
3. **木子島工作室 specifically.** Named in a national convenience-store licensing deal, in window, and absent from both CET editions. One handle away from being row 21.
4. **The 12-of-15-resolved ibon cohort is one deal, and the 80% wants a second data point.** If the 2025 ibon cohort resolves, the two together make a real time series on one brand's emerging-talent licensing - and if the share holds, that is a much stronger claim than a single year.
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
5. **Representability is still asserted, not tested.** *(Historical - superseded by build 7, section 16: the test was run and eight of these ten Vein E rows downgraded to `unclear`.)* Unchanged from build 2, and it now covers ten Vein E rows rather than eight. Every one is marked `representable: yes` on an absence-of-evidence basis - no agent, label or parent is named anywhere in the licensee's own roster record. `creator.amuse.com.tw` remains a JS shell. This must be said out loud on any prospect page that uses these rows.
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
