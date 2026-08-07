# Does the Taiwanese press cover sub-10k creators? A measurement, not an argument

Build 5 artefact. Retrieval date 2026-08-07.

Every build in this run has rested on one claim, stated in `rows.md` since build 1 and never tested:

> Press coverage is itself a scale filter: a Taiwanese outlet writes up a 聯名 when the IP is already recognisable, so the press-indexed population starts at roughly `10k_50k` and runs up.

That was an inference from an absence - the ten-market census, built from press, has zero `lt_10k` Taiwan rows.
An absence is compatible with two very different explanations: the press does not cover small IP, or the census's particular sources missed it.
This file separates them by running a full-text newspaper archive against a cohort whose follower band is already known.

## The instrument

`https://search.ltn.com.tw/list?keyword=<q>&type=all` answers over plain curl with HTTP 200 and real, parseable results.
自由時報 (Liberty Times) is Taiwan's largest-circulation daily, runs a standing 藝文 (arts and culture) desk, and is one of the five outlet families the census itself was built from.
Its search returns a result count, and each result carries a title, a URL, a publication date and a snippet, all server-rendered.

Two properties of the endpoint have to be handled or the numbers are wrong:

1. **The count is fuzzy.** 「約有 N 項結果」 is an OR-ish relevance count, not an exact-phrase count. Querying 點睛設計 returns 4 results, none of which contains the string 點睛設計. **The count must be discarded and the exact name re-checked inside each returned title and snippet.**
2. **Short names collide with ordinary Chinese.** 祝好運, 銅樂, 甜酸, 咖咖 and 山霧 are all real exhibitor brand names and all also ordinary word runs, so they match articles about lottery wins, bronze medals and passion fruit. A minimum-length filter is reported alongside the raw figure rather than instead of it.

The article body on `news.ltn.com.tw` is **not** in the desktop HTML - only the `og:description` lede is. Requesting the same URL with an iPhone user-agent returns the full body. Worth remembering.

## The cohort

Both editions of the 文博會 exhibitor dictionary (`cet2026-exhibitor-handle-map.md`, `cet2025-exhibitor-handle-map.md`), deduplicated by name:

| cohort | distinct names queried |
|---|---|
| sub-10k exhibitors | 235 |
| 10k-and-above exhibitors | 301 |
| **total queries** | **536** |

This is the right cohort for the question because every one of these names is a *real, self-declared, exhibiting Taiwanese creative brand* with a resolved follower count.
They are not a sample of who got press; they are a sample of who exists.

## The result

"Covered" = the exhibitor's own name appears literally in the title or snippet of at least one 自由時報 article, over the paper's whole archive, on any subject.

| band | n | covered | rate | n (name ≥4 CJK chars) | covered | rate |
|---|---|---|---|---|---|---|
| `lt_10k` | 235 | 49 | 20.9% | 183 | 24 | **13.1%** |
| `10k_50k` | 205 | 50 | 24.4% | 150 | 19 | **12.7%** |
| `50k_200k` | 71 | 28 | 39.4% | 55 | 17 | **30.9%** |
| `200k_1m` | 21 | 13 | 61.9% | 18 | 10 | **55.6%** |
| `gt_1m` | 4 | 3 | 75.0% | 3 | 2 | **66.7%** |

The right-hand block is the one to quote: it drops names short enough to collide with ordinary Chinese, which is where nearly all the false positives sit.

**Coverage rises monotonically with scale and the step is sharp.** A `50k_200k` creative brand is about 2.4 times as likely to have been named in 自由時報 as a sub-10k one, and a `200k_1m` one about 4.2 times.
The two bottom bands are **indistinguishable from each other** (13.1% vs 12.7%), which says the filter does not operate at 10,000 - it operates somewhere around 50,000.

## The part that actually settles it

A raw name mention is a weak proxy. What the census needs is not "was this creator ever named in the paper" but "was this creator's brand collaboration ever written up".
So all 24 sub-10k long-name hits were read by hand. None of them is that.

| what the 24 hits actually are | n |
|---|---|
| institutional or corporate exhibitor, not an independent creator (國泰世華銀行, 國立歷史博物館, 嘉義市政府文化局, 臺灣文博會, 露天市集, 東京國際禮品展, TCOD台中原創, 彩虹文創, picupi挑品, 三貝多股份有限公司, 雄獅文具, 台電文創) | 12 |
| false positive - the name matched a different subject entirely (謝工作室, 重要的小事, 往山裡走, 沙伯迪澳, 慶祝今天) | 5 |
| the creator appears, but for an exhibition, a market stall or a costumed appearance - not a licence (二允兄弟, 蘆葦女力, 比爾公主沒蓋子, 糙灰搭的獨角獸) | 4 |
| a real collaboration, but not IP licensing (木匠兄妹 x 后里動物之家 shelter charity; 大振豐洋傘 x 石虎 conservation umbrella) | 2 |
| **a mis-banded exhibitor the dictionary got wrong** (無所事事小海豹, see below) | 1 |
| **accepted `lt_10k` independent-character brand collaborations** | **0** |

Widening back out to the unfiltered 49 adds exactly one real IP licence - **蘭獸** (a two-character name, so the length filter drops it) - and that one is rejected on class, below.

**Zero.** Against twenty such rows already standing in `rows.md`, every one of them found through a brand-run directory, a licensee roster or an event organiser's partnership list - never through a newspaper.

That is the claim converted from an inference to a measurement. The census's zero is a property of its sources.

## Two things the sweep found that were not the question

**1. 蘭獸 ORCHIDSAUR - the one real licence in the sub-10k cohort, and it fails on class.**
`https://news.ltn.com.tw/news/life/breakingnews/5024990` (2025-04-27, HTTP 200): 世茂農業生技 x 「世茂×ORCHIDSAUR」聯名母親節限定花款, a pop-up at 台南遠東百貨成功店 running to 2025-05-11, orchids nano-dyed with the character's artwork.
蘭獸 (`@orchidsaur_official`, 3,485) is a properly-constructed character - CET2026 exhibitor 403 describes 「蘭花吉祥物-蘭獸」 born of a symbiosis legend between orchids and dinosaurs, with new-shoot horns and eight legs.
But the Facebook page the exhibitor register publishes for it (`facebook.com/tiostwn`, HTTP 200) resolves to **臺灣國際蘭展暨花卉科技展 Taiwan International Orchid Show**, a state-backed industry exposition at 農業部花卉創新園區.
So the rights holder is an event institution, not an independent creator. **Rejected on IP class** - a new rejection category, sibling to but distinct from the corporate-mascot rejection (捷米 JAMIE), because here the licensee genuinely is a third party.

**2. 無所事事小海豹 - the agent-account trap, and it is a caveat on the 46.8%.**
The CET2025 dictionary bands 無所事事小海豹 at **3,033** followers.
無所事事小海豹 is one of Taiwan's best-known sticker characters; 自由時報 alone carries eight articles naming it, including a 2023 SKM Park Outlets installation and the 2022 Kaohsiung 聊療漂漂河 balloon programme.
The exhibitor page (`2025.creativexpo.tw/zh-TW/brands/151`, HTTP 200) explains the discrepancy in its own words: 「樹葉文創有限公司為《無所事事小海豹》總代理同時也是小海豹的創作團隊」 - the handle the directory publishes, `@happacreative`, is **the licensing agent's corporate account**, not the IP's.

This is a third variant of the follower-count trap, after handle-squatting and the regional account, and it is the most dangerous of the three because nothing on the page looks wrong:

> **The agent-account trap.** A trade-show exhibitor page can publish the rights-holding *company's* account rather than the *IP's* account. The company account is small because companies do not have fans. Banding the IP from it understates by an order of magnitude - in exactly the direction that manufactures a false `lt_10k` row.

Detection rule that would have caught it: the exhibitor's own description contains 總代理 / 代理 / 經紀 / 授權合作洽談. That is also, separately, a `representable: no` signal - an IP with a named general agent is not addressable.

**The 46.8% sub-10k share of the 文博會 floor therefore has an unmeasured upward bias**, and this file cannot say how large it is. One case is confirmed; the sweep did not look for others, because the LTN join only surfaces the ones famous enough to have press - which is precisely the population where the trap is visible.

## Reproducing this

```bash
curl -s -A "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 Chrome/124.0" \
  "https://search.ltn.com.tw/list?keyword=$(python3 -c 'import urllib.parse;print(urllib.parse.quote("羊號角Piper"))')&type=all"
```

Parse `<li>` blocks; take `<a ... class="tit" title="...">` for the headline and URL, `class="time"` for the date, `<p>` for the snippet.
Keep a result only if the queried name occurs literally in the title or the snippet.
Pace at 0.7s between queries; 536 queries ran without a single rate-limit response.
