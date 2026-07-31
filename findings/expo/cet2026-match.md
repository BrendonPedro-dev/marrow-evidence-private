# CET2026 attendee list x ten-market census - Phase 0 name match

Input: `tasks/input/cet2026-orgs.md` (521 rows, public exhibitor-directory names only).
Matched against: the ten-market census (`findings/census/<market>/campaigns.md`, 1,054 rows, 234 INDEPENDENT) and the ip_scale_bands pass (`findings/census/<market>/ip_scale_bands.md`).
Run date 2026-07-31. No web queries were made; every result below rests on name evidence already in this repo.
The sheet's Notes column was treated as unverified prior research throughout: it was never used as a match basis and nothing from it is carried as a finding.

**Match method.** Names were normalised (NFKC, case-folded) and compared on CJK runs (exact and substring, minimum 2 characters), Latin token sets, and romanisation / alternate-script variants.
Candidate pairs were generated mechanically against every IP cell, brand cell, and full row text in all ten markets (339 pairwise candidates plus two full-text sweeps at different token lengths), then each candidate was adjudicated by hand; the basis of every accepted match is recorded in the register below.
Rejected candidates were generic-token coincidences (e.g. 'friends', 'hello', 'thailand', 'sakura') and are not matches.

**Match categories.** `matched-ip` = the attendee's IP is a census-adjudicated IP row.
`matched-brandside` = the attendee appears in a census row as the brand-side / campaign party, not as an IP.
`matched-label` = the attendee appears in census evidence as the licensing label or agent attached to a census IP.
`ambiguous` = a name-basis hit whose entity identity cannot be resolved without new research; it is left unresolved on purpose.
`out-of-coverage` = the attendee's market has no census (Poland, Macao, UK); no neighbouring market was substituted.

## Per-market result

| Market | Rows | Matched | Ambiguous | Unmatched | Out-of-coverage |
|---|---|---|---|---|---|
| Taiwan | 382 | 10 | 1 | 371 | 0 |
| Japan | 59 | 0 | 0 | 59 | 0 |
| HK | 33 | 1 | 0 | 32 | 0 |
| Korea | 28 | 2 | 2 | 24 | 0 |
| Thailand | 14 | 1 | 0 | 13 | 0 |
| Taiwan/Korea (HQ unclear) | 1 | 0 | 0 | 1 | 0 |
| Poland | 2 | 0 | 0 | 0 | 2 |
| Macao | 1 | 0 | 0 | 0 | 1 |
| UK | 1 | 0 | 0 | 0 | 1 |
| **Total** | **521** | **14** | **3** | **500** | **4** |

Matched breaks down as 9 IP-entity matches, 3 brand-side matches, and 2 label/agent matches; the register below lists every one with its basis.

## Hong Kong, stated separately

33 Hong Kong attendees, all listed IP-side, against a census whose verdict found 6 distinct addressable (REP=yes) creators in that market: Yan Ip / Plastic Thing, 圓DUM DUR, Hello Wong, 豚豚, LeonLollipop, and 馮德倫 / BUCKET MAN (`findings/census/hongkong/_VERDICT.md` section 2).

- **Matches against the six addressable creators: 0 of 33.**
  No attendee name matches any of the six on any basis attempted (CJK, Latin, romanisation, substring).
- **Matches against the HK census on any basis: 1 of 33.**
  BigBoysToys (#15) appears in hongkong row 22 - and on the brand/retail side of that row (the kkplus x IIJAN x BIGBOYSTOYS art-toy retail collab hosting a Creamy Mami campaign, a PORTFOLIO IP), not as an IP.
- **New to the census: 32 of 33** as organisations, and all 33 as IP-side entities (BigBoysToys' census appearance is not an IP appearance).
- **Label attachment on census evidence: 0 creators shown attached.**
  The census tables name these HK label-side entities: TOYZEROPLUS (six LuLu the Piggy rows, the market's entire REP=no block), kkplus, IIJAN, BIGBOYSTOYS (row 22), and - with zero adjudicable rows - How2work, Kennyswork and ToyQube.
  None of the 33 attendee names appears attached to any of them in any census cell.
  The one attendee the census does contain, BigBoysToys, appears as a label/retail platform itself, not as a creator attached to one.
  This is a statement about what the census evidence shows, not about the attendees: the census simply carries no evidence either way for the other 32, so absence of attachment here is absence of evidence, not evidence of independence.

The HK census verdict states its addressable count is a floor with a ceiling above 6, and names the reason (two definition-level rejections alone hold six more named HK creators).
This attendee list is consistent with that: it supplies 32-33 HK creator organisations the census never saw, which is a sampling-frame observation, not a corrected count (see the coverage section).
Per the pinned refusal, no HK indie-share figure is restated here; the bounded range in the HK verdict is internal-only and not quotable on its own.

## Match register

Every accepted match, with the basis recorded.
Census verdicts are carried verbatim from the census tables and the ip_scale_bands pass; nothing was re-derived.

### IP-entity matches (9)

| # | Attendee | Market | Census entity | Census ref | Class | REP | Band | Basis |
|---|---|---|---|---|---|---|---|---|
| 140 | 貓貓蟲咖波 (Capoo Bugcat) | Taiwan | 貓貓蟲咖波 Bugcat Capoo | taiwan-v2 rows 1, 4, 32, 39, 51, 108, 112, 114 | INDEPENDENT | no | gt_1m | CJK exact 貓貓蟲咖波 + Latin Bugcat/Capoo |
| 187 | 露咖貓 (Looka Cat) | Taiwan | 露咖貓 LOOKA CAT | taiwan-v2 row 118 | INDEPENDENT | yes | 10k_50k | CJK exact + Latin |
| 217 | 黃阿瑪的後宮生活 / fumeancats | Taiwan | 黃阿瑪的後宮生活 Fumeancats | taiwan-v2 rows 21, 29 | INDEPENDENT | no | gt_1m | CJK exact + Latin |
| 218 | 諾米 / Nuomi | Taiwan | Nuomi 諾米 | taiwan-v2 row 130 | INDEPENDENT | yes | 50k_200k | CJK exact + Latin |
| 235 | 腋毛人 / Yemao | Taiwan | 臺灣印事 & 腋毛人 Yemao | taiwan-v2 row 76 | INDEPENDENT | yes | 10k_50k (腋毛人 side) | CJK exact + Latin |
| 245 | 台灣連友 / LINE FRIENDS | Taiwan | LINE FRIENDS (incl. BT21) | hongkong 9, 25; indonesia 86; korea 67; philippines 3, 10; singapore 13; thailand 49 | PORTFOLIO | - | - | exact name; attendee is the Taiwan arm; no taiwan-v2 row exists |
| 111 | MIND.A.DAY | Korea | MIND.A.DAY / CoverCat 跩跩貓 = 마인드어데이 커버캣 | korea row 154; taiwan-v2 row 101 | INDEPENDENT | yes | 10k_50k (both) | exact name (TW row); romanised variant (KR row) |
| 112 | Mr.Donothing | Korea | 미스터두낫띵 (Mr.DoNothing) | korea row 142 | INDEPENDENT | yes | 50k_200k | exact romanisation |
| 516 | Shewsheep | Thailand | SHEWSHEEP (ชูชีพ) | thailand row 74 | INDEPENDENT | yes | 50k_200k | exact name |

The REP=no calls carry their census reasons unchanged: Capoo through the creator's own captive studio (卡特島創意), Fumeancats per the taiwan-v2 adjudication, and neither is re-argued here.

### Brand-side matches (3)

| # | Attendee | Market | Census ref | What the census row shows | Basis |
|---|---|---|---|---|---|
| 15 | BigBoysToys | HK | hongkong row 22 | brand/retail side of kkplus x IIJAN x BIGBOYSTOYS; row IP Creamy Mami (PORTFOLIO) | exact name in brand cell |
| 459 | 國立故宮博物院 | Taiwan | taiwan-v2 row 51 | brand-side co-party (7-ELEVEN Taiwan x 國立故宮博物院); row IP Bugcat Capoo x 故宮100周年 (INDEPENDENT, REP=no) | CJK exact in brand cell |
| 504 | 五桐號 | Taiwan | taiwan-v2 rows 2, 13, 107 | licensee brand for Chiikawa (PORTFOLIO), Care Bears (PORTFOLIO), Dinotaeng (INDEPENDENT, REP=yes) | CJK exact in brand cell |

### Label / agent matches (2)

| # | Attendee | Market | Census ref | What the census shows | Basis |
|---|---|---|---|---|---|
| 301 | 玩具加乘 (TOYZEROPLUS) | Taiwan | hongkong rows 78, 79, 81, 89, 91, 92; taiwan-v2 row 5; thailand row 12 | the partner label for 罐頭豬 LuLu the Piggy - INDEPENDENT, REP=no under the pinned Toyzeroplus call (creator-owned, exclusively label-channelled), band 200k_1m | exact name in IP cells; attendee is the label's Taiwan arm, an agency, not an IP |
| 302 | 木棉花國際 (MUSE COMMUNICATION) | Taiwan | taiwan-v2 rows 104, 105 | named in class evidence as the TW licensing channel for 伊藤潤二 Junji Ito (PORTFOLIO) | CJK exact in evidence text |

### Ambiguous (3) - deliberately unresolved

| # | Attendee | Market | Census ref | Why it stays ambiguous |
|---|---|---|---|---|
| 93 | SLBS | Korea | philippines row 53 (evidence text) | census evidence names "Samsung SLBS studio" as the production channel on a PORTFOLIO row (SKZOO / Stray Kids); the exact acronym matches, but whether the exhibitor is that same studio cannot be resolved without new research, which this run refuses |
| 119 | SLBS | Korea | philippines row 53 (evidence text) | same name, same reasoning as #93 (the sheet lists SLBS twice) |
| 307 | 台灣角川 (KADOKAWA TAIWAN) | Taiwan | korea row 47 (evidence text) | evidence names Kadokawa/Trigger as the owner of Dungeon Meshi; the name matches the Japanese parent, the attendee is its Taiwan subsidiary - a lineage hit, not an entity match |

## The coverage finding

The census's addressable-creator counts are stated floors (Hong Kong's verdict says the ceiling is above 6 and names why; the Philippines and Indonesia verdicts say floor outright).
This attendee list is a sampling frame the census never had - organisations self-selected for actively seeking licensing and market exposure - and the unmatched share measures how much of that frame the census's campaign-based press sweeps never saw.

Per market, counting IP-type attendees against any census appearance:

| Market | IP-type attendees | Matched to that market's census as an IP | Observation |
|---|---|---|---|
| Taiwan | 147 | 5 | 142 IP-side organisations exhibiting at the market's flagship licensing expo are invisible to a census built from campaign press coverage |
| HK | 33 | 0 | see the Hong Kong section; 0 overlap with the six addressable creators |
| Japan | 23 | 0 | zero overlap in either direction with the japan census's own independent layer |
| Korea | 18 | 2 | the two matches are the two attendees with active cross-border campaign records |
| Thailand | 7 | 1 | includes census-absent IPs of visible scale (e.g. Bloody Bunny, unmatched) |

What this does and does not imply, stated with its own confidence:

1. **Direction (high confidence): every market's addressable-creator count is confirmed as a floor.**
   The expo frame contains dozens (Korea, Thailand) to hundreds (Taiwan) of creator organisations per market that campaign-press sweeps structurally cannot see, because those sweeps only observe creators who already have a brand campaign in the window.
   This is the same one-way direction the HK verdict argued from its query-class split, now shown from an independent frame.
2. **Magnitude (low confidence): the unmatched share is not a corrected addressable count.**
   Exhibiting is not campaign activity, and no unmatched attendee has been adjudicated for ownership class or REP; some would fail the census's own tests (own-mascot rows like #129 台北捷運捷米 JAMIE BY METRO TAIPEI and #223 樂天胖達 Okaimono Panda are excluded from the census by definition, so their absence is structural, not a coverage gap).
   No market's indie share is restated or adjusted here.
3. **Selection effects run in opposite directions (medium confidence).**
   The census over-samples campaign-proven IPs; the expo over-samples market-seeking ones.
   The matched set is consistent with that: the census-side matches concentrate in the largest bands (gt_1m Capoo and Fumeancats), while the expo-only tier sits below the campaign threshold the census can observe.
4. **The two frames measure different populations, and the gap between them is itself the measurement.**
   Where the census found single-digit addressable creators (HK: 6), this frame supplies 33 IP-side organisations from the same market in one venue; the true creator population is at least the union, and only the census side of it carries adjudicated verdicts.

## Refusals and edge cases applied

- No new research: 500 in-coverage names stay unmatched rather than guessed; 3 stay ambiguous rather than forced.
- Poland (2), Macao (1) and the UK (1) are out-of-coverage; no neighbouring market was substituted.
- No rights_owner, chain-of-title, territory, exclusivity or deal-term conclusions anywhere in this file; carried REP calls are census adjudications, not new ones.
- No outcome numbers; no brand images fetched.
- HK's indie-share range is not restated (internal-only per the pinned refusal); no market's indie share appears in this file.
- Pinned edge cases honoured: Toyzeroplus (#301 matched as label, not IP; LuLu's REP=no carried), 咖波 (Capoo REP=no via captive studio carried), own-mascot exclusion (noted in the coverage section, not used to adjudicate attendees), authorship-is-not-ownership (no attendee was matched to an IP on a creator-credit basis), Molly Factory and Kumamon (no attendee triggered either).
- The sheet's Notes column was never used as a match basis and none of its claims are carried as findings.

## Per-row disposition (all 521 rows)

Census verdicts are carried, not re-derived; the verdict column is filled only where the census adjudicated the matched entity.
Unmatched means exactly that: the name was not found in any census table on any basis attempted; it is not evidence about the organisation.

| # | Name | Country | Type | Disposition | Census ref | Carried census verdict / note |
|---|---|---|---|---|---|---|
| 1 | 0.9144m Studio | HK | IP | unmatched | - | |
| 2 | Din Dong & Uncle Fish | HK | IP | unmatched | - | |
| 3 | Creature Collectors Club | HK | IP | unmatched | - | |
| 4 | hohohola x magickira | HK | IP | unmatched | - | |
| 5 | Pure Studio | HK | IP | unmatched | - | |
| 6 | Nine Four Sixty X Dino Valley | HK | IP | unmatched | - | |
| 7 | Nalok.Lok | HK | IP | unmatched | - | |
| 8 | 大爪作 BIGCLAWX | HK | IP | unmatched | - | |
| 9 | YoYo! Yogurt!! Studio | HK | IP | unmatched | - | |
| 10 | EMO NEKO W.O.O.F. CLUB | HK | IP | unmatched | - | |
| 11 | Ouch!! Don't Cry!! | HK | IP | unmatched | - | |
| 12 | 021 Consultancy x SHIBAINC | HK | IP | unmatched | - | |
| 13 | 無盡創意設計工作室 | HK | IP | unmatched | - | |
| 14 | FIGTION | HK | IP | unmatched | - | |
| 15 | BigBoysToys | HK | IP | matched-brandside | hongkong row 22 | row entity is brand-side; row IP: 我係小忌廉 Creamy Mami, PORTFOLIO |
| 16 | CHEAP CENTURY | HK | IP | unmatched | - | |
| 17 | Shadoowww | HK | IP | unmatched | - | |
| 18 | club babo | HK | IP | unmatched | - | |
| 19 | Genie Li | HK | IP | unmatched | - | |
| 20 | Venus Philosophy | HK | IP | unmatched | - | |
| 21 | TOBALLKIDRAWING | HK | IP | unmatched | - | |
| 22 | ARDUREY LIMITED (agency) | HK | IP | unmatched | - | |
| 23 | cheeky cheeky | HK | IP | unmatched | - | |
| 24 | HEREAFTER STUDIO (brand) | HK | IP | unmatched | - | |
| 25 | HANDMADESHIP (brand) | HK | IP | unmatched | - | |
| 26 | Scentory (brand) | HK | IP | unmatched | - | |
| 27 | Bethel | HK | IP | unmatched | - | |
| 28 | paper diamond® (brand) | HK | IP | unmatched | - | |
| 29 | DDED (brand) | HK | IP | unmatched | - | |
| 30 | Tse Sai Pei (brand) | HK | IP | unmatched | - | |
| 31 | Overloaddance (brand) | HK | IP | unmatched | - | |
| 32 | Mr n Mrs Moon | HK | IP | unmatched | - | |
| 33 | Lewa Lee | HK | IP | unmatched | - | |
| 34 | Kitsutaka Co., Ltd. | Japan | Brand | unmatched | - | |
| 35 | BAN INOUE | Japan | Brand | unmatched | - | |
| 36 | SAKURA WAQS | Japan | Brand | unmatched | - | |
| 37 | Murakami Lighting Co., Ltd | Japan | Brand | unmatched | - | |
| 38 | ASAHIDO Kyoto Kiyomizu Ware | Japan | Brand | unmatched | - | |
| 39 | YAMAICHIYA | Japan | Brand | unmatched | - | |
| 40 | Junintowa | Japan | Brand | unmatched | - | |
| 41 | KYOTO KARASUMA ROKUHICHIDO | Japan | Brand | unmatched | - | |
| 42 | OKADAYA LACQUERWARE CO. | Japan | Brand | unmatched | - | |
| 43 | hiro | Japan | Brand | unmatched | - | |
| 44 | NIIDA BUSSAN | Japan | Brand | unmatched | - | |
| 45 | Business Guide-Sha, Inc. | Japan | Agency | unmatched | - | |
| 46 | TERAICHI | Japan | Brand | unmatched | - | |
| 47 | Fujiwara Dyeing Co., Ltd. | Japan | Brand | unmatched | - | |
| 48 | BLOOMING NAKANISHI & COMPANY | Japan | Brand | unmatched | - | |
| 49 | Craft Tokyo 東京選物 (Craft Tokyo Co.) | Japan | Retail | unmatched | - | |
| 50 | 沖繩在台辦事處 (Okinawa Taipei Office) | Japan | Org | unmatched | - | |
| 51 | 中川貴雄｜Takao Nakagawa | Japan | IP | unmatched | - | |
| 52 | Alicevigor | Japan | IP | unmatched | - | |
| 53 | TULIP PRINCE★BUNTAN | Japan | IP | unmatched | - | |
| 54 | HARIKEN 哈利剣 | Japan | IP | unmatched | - | |
| 55 | FREE BUT BUSY | Japan | IP | unmatched | - | |
| 56 | NekoLand | Japan | IP | unmatched | - | |
| 57 | 柴尾-shibao- | Japan | IP | unmatched | - | |
| 58 | Lemon & Sugar | Japan | IP | unmatched | - | |
| 59 | Mochi Mochi Ducks | Japan | IP | unmatched | - | |
| 60 | Tooth comics | Japan | IP | unmatched | - | |
| 61 | CHIKUWAS | Japan | IP | unmatched | - | |
| 62 | frankenji. | Japan | IP | unmatched | - | |
| 63 | KIWI kun | Japan | IP | unmatched | - | |
| 64 | LIL DUMPLING CHAO | Japan | IP | unmatched | - | |
| 65 | fancy ferret KORO&MARU | Japan | IP | unmatched | - | |
| 66 | tama | Japan | IP | unmatched | - | |
| 67 | Mediusa-chan | Japan | IP | unmatched | - | |
| 68 | MITSUME | Japan | IP | unmatched | - | |
| 69 | MOGU MOLE | Japan | IP | unmatched | - | |
| 70 | KENELEPHANT | Japan | IP | unmatched | - | |
| 71 | TiFiLid & Fulcro | Japan | Brand | unmatched | - | |
| 72 | chi-bee | Japan | IP | unmatched | - | |
| 73 | ICELOLLY | Japan | IP | unmatched | - | |
| 74 | SAUVENIR | Japan | Brand | unmatched | - | |
| 75 | CEMENT PRODUCE DESIGN | Japan | Brand | unmatched | - | |
| 76 | Kitsutaka Co.; Ltd. | Japan | Brand | unmatched | - | |
| 77 | KOBE | Japan | Brand | unmatched | - | |
| 78 | BAN INOUE | Japan | Brand | unmatched | - | |
| 79 | SAKURA WAQS | Japan | Brand | unmatched | - | |
| 80 | Murakami Lighting Co.; Ltd | Japan | Brand | unmatched | - | |
| 81 | WINTEN | Japan | Brand | unmatched | - | |
| 82 | ASAHIDO Kyoto Kiyomizu Ware | Japan | Brand | unmatched | - | |
| 83 | YAMAICHIYA | Japan | Brand | unmatched | - | |
| 84 | Junintowa | Japan | Brand | unmatched | - | |
| 85 | KYOTO KARASUMA ROKUHICHIDO | Japan | Brand | unmatched | - | |
| 86 | OKADAYA LACQUERWARE CO.; LTD | Japan | Brand | unmatched | - | |
| 87 | hiro | Japan | Brand | unmatched | - | |
| 88 | NIIDA BUSSAN | Japan | Brand | unmatched | - | |
| 89 | Business Guide-Sha, Inc. | Japan | Agency | unmatched | - | |
| 90 | TERAICHI | Japan | Brand | unmatched | - | |
| 91 | Fujiwara Dyeing Co., Ltd. | Japan | IP | unmatched | - | |
| 92 | BLOOMING NAKANISHI＆ COMPANY | Japan | Brand | unmatched | - | |
| 93 | SLBS | Korea | Brand | ambiguous | philippines row 53 (evidence text) | row IP: SKZOO / Stray Kids, PORTFOLIO; SLBS named as production studio, not IP |
| 94 | Busan Design Company Products | Korea | Org/Brand | unmatched | - | |
| 95 | HANABI | Korea | IP | unmatched | - | |
| 96 | Cafe and Hof | Korea | IP | unmatched | - | |
| 97 | hellogitii | Korea | IP | unmatched | - | |
| 98 | TOMARMON | Korea | IP | unmatched | - | |
| 99 | KITSCHS BEAR | Korea | IP | unmatched | - | |
| 100 | PETPETDOLL | Korea | IP | unmatched | - | |
| 101 | jop_dong_sa_ni | Korea | IP | unmatched | - | |
| 102 | MYOCAT&BOMNAENGE GOLGOLSONG | Korea | IP | unmatched | - | |
| 103 | SHINKIRU | Korea | IP | unmatched | - | |
| 104 | MILL HOUSE | Korea | IP | unmatched | - | |
| 105 | JOLLYGEE STUDIO (already known contact - Hyunji Song; ongoing relationship since 6/24) | Korea | IP | unmatched | - | |
| 106 | PETITBEAR friends & ee yeoreum | Korea | IP | unmatched | - | |
| 107 | ds_tape | Korea | IP | unmatched | - | |
| 108 | WEIRDOLLS | Korea | IP | unmatched | - | |
| 109 | Dokkaebi atelier | Korea | IP | unmatched | - | |
| 110 | Yangchee | Korea | IP | unmatched | - | |
| 111 | MIND.A.DAY | Korea | IP | matched-ip | korea row 154; taiwan-v2 row 101 | INDEPENDENT; REP=yes; band 10k_50k (both markets) |
| 112 | Mr.Donothing | Korea | IP | matched-ip | korea row 142 | INDEPENDENT; REP=yes; band 50k_200k |
| 113 | PAPER CONCRETE | Korea | Brand | unmatched | - | |
| 114 | s-lock vacuum container | Korea | Brand | unmatched | - | |
| 115 | LUMENA | Korea | Brand | unmatched | - | |
| 116 | MONSTARGEAR | Korea | Brand | unmatched | - | |
| 117 | duck_safe | Korea | Brand | unmatched | - | |
| 118 | CHICKEN IN THE LAB | Korea | Brand | unmatched | - | |
| 119 | SLBS | Korea | Brand | ambiguous | philippines row 53 (evidence text) | row IP: SKZOO / Stray Kids, PORTFOLIO; SLBS named as production studio, not IP |
| 120 | Busan Design Company Products | Korea | Org/Brand | unmatched | - | |
| 121 | MACAO ILLUSTRATORS ASSOCIATION | Macao | Org | out-of-coverage | - | no census exists for Macao; reported as out-of-coverage, not substituted |
| 122 | Polish Graphic Design Foundation | Poland | Org | out-of-coverage | - | no census exists for Poland; reported as out-of-coverage, not substituted |
| 123 | Polish Illustration | Poland | Org | out-of-coverage | - | no census exists for Poland; reported as out-of-coverage, not substituted |
| 124 | 腦袋星球 & 碰碰紅綠豆 | Taiwan | IP | unmatched | - | |
| 125 | 小水豚豆仔 (BabyCapybara) | Taiwan | IP | unmatched | - | |
| 126 | 咻熊家 (Xiubear Studio) | Taiwan | IP | unmatched | - | |
| 127 | 鹿人 (TWODEERMAN) | Taiwan | IP | unmatched | - | |
| 128 | 三貓俱樂部 (3 CATS CLUB) | Taiwan | IP | unmatched | - | |
| 129 | 台北捷運捷米 (JAMIE BY METRO TAIPEI) | Taiwan | IP | unmatched | - | |
| 130 | JINART | Taiwan | IP | unmatched | - | |
| 131 | 小呸角 (O!PLAY) | Taiwan | IP | unmatched | - | |
| 132 | 懶散兔&啾先生 (Lazy Rabbit & Mr.Chu) | Taiwan | IP | unmatched | - | |
| 133 | 章魚熊 (TAKOKUMA) | Taiwan | IP | unmatched | - | |
| 134 | A君B子 (akunbko) | Taiwan | IP | unmatched | - | |
| 135 | 胡創 (Hu Creates) | Taiwan | IP | unmatched | - | |
| 136 | 消極男子 (Mainasu otoko) | Taiwan | IP | unmatched | - | |
| 137 | Kurt | Taiwan | IP | unmatched | - | |
| 138 | 右手超人 (Yohand Studio) | Taiwan | IP | unmatched | - | |
| 139 | 奶油家族 (The Butters) | Taiwan | IP | unmatched | - | |
| 140 | 貓貓蟲咖波 (Capoo Bugcat) | Taiwan | IP | matched-ip | taiwan-v2 rows 1, 4, 32, 39, 51, 108, 112, 114 | INDEPENDENT; REP=no (pinned: creator-owned via captive studio 卡特島創意 Carter Island); band gt_1m |
| 141 | 虎豹屋敷 (Ultra Tiger Toys) | Taiwan | IP | unmatched | - | |
| 142 | 胖西是隻河狸 (Justin is a Beaver) | Taiwan | IP | unmatched | - | |
| 143 | 你好工作室 (Hello Studio) | Taiwan | IP | unmatched | - | |
| 144 | 變種吉娃娃 (GODGWAWA) | Taiwan | IP | unmatched | - | |
| 145 | 怪奇事物所 (Incrediville) | Taiwan | IP | unmatched | - | |
| 146 | 尋寶獅 (SHIBUDI) | Taiwan | IP | unmatched | - | |
| 147 | 雙夏 (PatonaNatsu) | Taiwan | IP | unmatched | - | |
| 148 | 小印紅鹿 (INDEER) | Taiwan | IP | unmatched | - | |
| 149 | 扭蛋雞 (Gacha Chicken) | Taiwan | IP | unmatched | - | |
| 150 | 二允兄弟 (WinBrothers) | Taiwan | IP | unmatched | - | |
| 151 | 小不點動畫 (Studio ilya) | Taiwan | IP | unmatched | - | |
| 152 | 小萌獸朵咪 (DouxAmi) | Taiwan | IP | unmatched | - | |
| 153 | 華研 (HIM) | Taiwan | IP | unmatched | - | |
| 154 | 夥伴玩具 (PartnerToys) | Taiwan | IP | unmatched | - | |
| 155 | 空罐王 (CankingSketch) | Taiwan | IP | unmatched | - | |
| 156 | 微疼 (WEITENG) | Taiwan | IP | unmatched | - | |
| 157 | 油頭二世 (OILHEADJUNIOR) | Taiwan | IP | unmatched | - | |
| 158 | 啾啾妹 (CHUCHUMEI) | Taiwan | IP | unmatched | - | |
| 159 | 阿啾小劇場 (Achu) | Taiwan | IP | unmatched | - | |
| 160 | KINGJUN | Taiwan | IP | unmatched | - | |
| 161 | 屎蛋唐尼 (Tony Stan) | Taiwan | IP | unmatched | - | |
| 162 | 蘭獸 (Orchidsaur) | Taiwan | IP | unmatched | - | |
| 163 | 喔噢你好 (OH! ALL) | Taiwan | IP | unmatched | - | |
| 164 | 洋蔥與阿文 (Onion Man) | Taiwan | IP | unmatched | - | |
| 165 | 蜜可魯 (mikolu) | Taiwan | IP | unmatched | - | |
| 166 | 無所事事小海豹 (The Nothing Seal) | Taiwan | IP | unmatched | - | |
| 167 | noii noii | Taiwan | IP | unmatched | - | |
| 168 | 獺咘獺咘 (TaBuTaBu) | Taiwan | IP | unmatched | - | |
| 169 | 豆苗先生 (Mr.Doumiao) | Taiwan | IP | unmatched | - | |
| 170 | 黑白小姐 (Miss B&W) | Taiwan | IP | unmatched | - | |
| 171 | 平凡乙女日記 (Otomerui) | Taiwan | IP | unmatched | - | |
| 172 | 當肯 (DUNCAN) | Taiwan | IP | unmatched | - | |
| 173 | 廢物女友 (lousy girlfriend) | Taiwan | IP | unmatched | - | |
| 174 | 蜜柑站長 (Mikan Station Master) | Taiwan | IP | unmatched | - | |
| 175 | 嗨小強 (HI JOHN) | Taiwan | IP | unmatched | - | |
| 176 | 害羞的黑田桑 (SHYLYKURODASANG) | Taiwan | IP | unmatched | - | |
| 177 | 波波冰狗室 (Kawaii Hyoka) | Taiwan | IP | unmatched | - | |
| 178 | 貓日 (Neneko) | Taiwan | IP | unmatched | - | |
| 179 | A ee mi | Taiwan | IP | unmatched | - | |
| 180 | 威嗝高校 (WAAGGER) | Taiwan | IP | unmatched | - | |
| 181 | 春天先生 (Mr. Spring) | Taiwan | IP | unmatched | - | |
| 182 | 醜白兔 (Ugly rabbit) | Taiwan | IP | unmatched | - | |
| 183 | 安怎？Ann-Nua (Ann-Nua Studio) | Taiwan | IP | unmatched | - | |
| 184 | 夢の犬與好友們 (Mr. Cloudy With Friends.) | Taiwan | IP | unmatched | - | |
| 185 | one little planet | Taiwan | IP | unmatched | - | |
| 186 | doudle studio | Taiwan | IP | unmatched | - | |
| 187 | 露咖貓 (Looka Cat) | Taiwan | IP | matched-ip | taiwan-v2 row 118 | INDEPENDENT; REP=yes; band 10k_50k |
| 188 | 凱西.陳 (cathie's goods) | Taiwan | IP | unmatched | - | |
| 189 | 狗狗夾星 (DOGDOGSANDWICH) | Taiwan | IP | unmatched | - | |
| 190 | WKY560 STUDIO | Taiwan | IP | unmatched | - | |
| 191 | 小心臟 (LittleHeart) | Taiwan | IP | unmatched | - | |
| 192 | 屌面人 (Lanparman) | Taiwan | IP | unmatched | - | |
| 193 | 恐龍的房間 (DINOSAUR'S ROOM) | Taiwan | IP | unmatched | - | |
| 194 | HOLY YA 虎力爺 | Taiwan | IP | unmatched | - | |
| 195 | Weeeee | Taiwan | IP | unmatched | - | |
| 196 | 1G | Taiwan | IP | unmatched | - | |
| 197 | 胖極 Pangiistudio | Taiwan | IP | unmatched | - | |
| 198 | 小虎day | Taiwan | IP | unmatched | - | |
| 199 | 小學課本的逆襲 | Taiwan | IP | unmatched | - | |
| 200 | 加零在電線桿下 (Jia0) | Taiwan | IP | unmatched | - | |
| 201 | 糙灰搭的獨角獸 (Burned Unicorn) | Taiwan | IP | unmatched | - | |
| 202 | 日頭 (Littop) | Taiwan | IP | unmatched | - | |
| 203 | 嗚比的朋友 (Woobi Dooggy) | Taiwan | IP | unmatched | - | |
| 204 | 麥考艾裘 (MaiKaoAiChiou) | Taiwan | IP | unmatched | - | |
| 205 | 愚室實驗所 (yushilab) | Taiwan | IP | unmatched | - | |
| 206 | nozomii 妯米 | Taiwan | IP | unmatched | - | |
| 207 | superB studio | Taiwan | IP | unmatched | - | |
| 208 | 小怪家 (guaaii) | Taiwan | IP | unmatched | - | |
| 209 | 微醺斑比 (Drunk Bambi) | Taiwan | IP | unmatched | - | |
| 210 | 金馬桶 (KINMATON) | Taiwan | IP | unmatched | - | |
| 211 | 萌萌與他的恐龍朋友 | Taiwan | IP | unmatched | - | |
| 212 | 伸縮自如的雞與鴨 (GUGU & GUAGUA) | Taiwan | IP | unmatched | - | |
| 213 | 花大鼻小文青 (Huadabii) | Taiwan | IP | unmatched | - | |
| 214 | 青青小樹 植生物 (Doromon Plantimals) | Taiwan | IP | unmatched | - | |
| 215 | 昏呱 / HuenGua | Taiwan | IP | unmatched | - | |
| 216 | 1982小時候 / 1982Kids | Taiwan | IP | unmatched | - | |
| 217 | 黃阿瑪的後宮生活 / fumeancats | Taiwan | IP | matched-ip | taiwan-v2 rows 21, 29 | INDEPENDENT; REP=no; band gt_1m |
| 218 | 諾米 / Nuomi | Taiwan | IP | matched-ip | taiwan-v2 row 130 | INDEPENDENT; REP=yes; band 50k_200k |
| 219 | 於是日常了RJ / PINGRAYK | Taiwan | IP | unmatched | - | |
| 220 | 瘋狂眼珠 / Crazyeyes | Taiwan | IP | unmatched | - | |
| 221 | 小黃間 / little yellow studio | Taiwan | IP | unmatched | - | |
| 222 | 松尼奇尼 / SweetHouse | Taiwan | IP | unmatched | - | |
| 223 | 樂天胖達 / Okaimono Panda | Taiwan | IP | unmatched | - | |
| 224 | 熊老闆BearBoss | Taiwan | IP | unmatched | - | |
| 225 | 牙技師的牙齒們 / Yajishi de Teeth | Taiwan | IP | unmatched | - | |
| 226 | 布朗尼 / annnbrownie | Taiwan | IP | unmatched | - | |
| 227 | 方坊 / Square Studio | Taiwan | IP | unmatched | - | |
| 228 | MooMoo姆姆 / moomoo studio | Taiwan | IP | unmatched | - | |
| 229 | 咚東 / Dong Dong | Taiwan | IP | unmatched | - | |
| 230 | 皮康 / Pikang | Taiwan | IP | unmatched | - | |
| 231 | 慢慢挑 / PianoPiano | Taiwan | IP | unmatched | - | |
| 232 | Minghan H. | Taiwan | IP | unmatched | - | |
| 233 | HiHi 搗蛋鬼 / Hihi trickster | Taiwan | IP | unmatched | - | |
| 234 | 三個不結婚的女人 / Three Unmarried Women | Taiwan | IP | unmatched | - | |
| 235 | 腋毛人 / Yemao | Taiwan | IP | matched-ip | taiwan-v2 row 76 | INDEPENDENT; REP=yes; band 10k_50k (腋毛人 side of a two-creator row; co-listed 臺灣印事 reads lt_10k) |
| 236 | bubukai | Taiwan | IP | unmatched | - | |
| 237 | 醉猫畫室 / Peno alcohol. | Taiwan | IP | unmatched | - | |
| 238 | Ginny Lambkin 居你 | Taiwan | IP | unmatched | - | |
| 239 | SAITEMISS 低級失誤 | Taiwan | IP | unmatched | - | |
| 240 | 搖星 / SHAKE STAR | Taiwan | IP | unmatched | - | |
| 241 | 美可女子 / Mayco illustration | Taiwan | IP | unmatched | - | |
| 242 | ポコ大王 / POKO | Taiwan | IP | unmatched | - | |
| 243 | 山羊先生工作室 / Mister Goat illustration | Taiwan | IP | unmatched | - | |
| 244 | BIRD ERA x Mio.Tsubasa | Taiwan | IP | unmatched | - | |
| 245 | 台灣連友 / LINE FRIENDS | Taiwan | IP | matched-ip | hongkong rows 9, 25; indonesia row 86 (BT21); korea row 67; philippines rows 3, 10 (BT21); singapore row 13; thailand row 49 | PORTFOLIO in every census appearance; no REP / band (portfolio rows carry neither) |
| 246 | 桃源深處有人家 / LuoLuo official | Taiwan | IP | unmatched | - | |
| 247 | 小雞汁 / Chickie Small | Taiwan | IP | unmatched | - | |
| 248 | 想你熊胖胖&狐獴杯杯 / SHINY BEAR & MEERKATBEIBEI | Taiwan | IP | unmatched | - | |
| 249 | 小田月所 | Taiwan | IP | unmatched | - | |
| 250 | 郁郁YùYù | Taiwan | IP | unmatched | - | |
| 251 | HALO | Taiwan | IP | unmatched | - | |
| 252 | 二位工作室 / AWAY studio | Taiwan | IP | unmatched | - | |
| 253 | Hank Max | Taiwan | IP | unmatched | - | |
| 254 | Color Wave | Taiwan | IP | unmatched | - | |
| 255 | satana | Taiwan | IP | unmatched | - | |
| 256 | Float Living | Taiwan | IP | unmatched | - | |
| 257 | 茉荷 / MIHER | Taiwan | IP | unmatched | - | |
| 258 | 眠腦 / minnao | Taiwan | IP | unmatched | - | |
| 259 | 邦妮插畫工作室 / Bon Bon Stickers | Taiwan | IP | unmatched | - | |
| 260 | NINA HO ILLUSTRATION | Taiwan | IP | unmatched | - | |
| 261 | 莫克 X 耶思波 (Moek X Jesper) | Taiwan | IP | unmatched | - | |
| 262 | 瀏海樹 (BANGSTREE) | Taiwan | IP | unmatched | - | |
| 263 | 塗狗 (togo) | Taiwan | IP | unmatched | - | |
| 264 | Miaoisland 喵島 | Taiwan | IP | unmatched | - | |
| 265 | TTC 火柴人 (TTC Goods) | Taiwan | IP | unmatched | - | |
| 266 | 咖咖 (KAKA_LAZY) | Taiwan | IP | unmatched | - | |
| 267 | 山頂洞人實驗室 (Homosapiens Lab) | Taiwan | IP | unmatched | - | |
| 268 | eguchitoys | Taiwan | IP | unmatched | - | |
| 269 | sanaxillu | Taiwan | IP | unmatched | - | |
| 270 | 早安妞妞 (MORNING NUNU) | Taiwan | IP | unmatched | - | |
| 271 | 小公視 (PTSXS) | Taiwan | Org | unmatched | - | |
| 272 | 銳耳創作股份有限公司 (STAYREAL) | Taiwan | Brand | unmatched | - | |
| 273 | 有樂作業 (Yolozuya) | Taiwan | Brand | unmatched | - | |
| 274 | 台灣角協 (TCBLA) | Taiwan | Org | unmatched | - | |
| 275 | 坤翔國際有限公司 (KHUN SIANG INT'L) | Taiwan | Agency | unmatched | - | |
| 276 | 好生藝品牌管理顧問有限公司 (Brand Beat) | Taiwan | Agency | unmatched | - | |
| 277 | 恐龍山丘文化創意有限公司 (Dino Valley Creative) | Taiwan | Agency | unmatched | - | |
| 278 | 赫思西亞品牌創意有限公司 (HESTIA) | Taiwan | Agency | unmatched | - | |
| 279 | 普威實業股份有限公司 (BLUE WAY JEAN) | Taiwan | Brand | unmatched | - | |
| 280 | 島友文創商社 (YAMAMAVIBE) | Taiwan | Brand/Retail | unmatched | - | |
| 281 | 路遙圓創 (Luyao Design) | Taiwan | Service | unmatched | - | |
| 282 | 伽特原創有限公司 (JTSTUDIO) | Taiwan | Agency | unmatched | - | |
| 283 | 勝明文具百貨有限公司 (SANMIN) | Taiwan | Brand | unmatched | - | |
| 284 | 給好 (Wonderful Giving) | Taiwan | Brand | unmatched | - | |
| 285 | iii sum+ 實樂設計 (iii sum+) | Taiwan | Service | unmatched | - | |
| 286 | 有亦文創股份有限公司 (Uiii Cultural and Creative) | Taiwan | Agency | unmatched | - | |
| 287 | 文化內容策進院 (Taiwan Creative Content Agency) | Taiwan | Org | unmatched | - | |
| 288 | 三貝多股份有限公司 (SAN-BYTE CREATIVE) | Taiwan | Agency | unmatched | - | |
| 289 | 印花樂 (inBlooom) | Taiwan | Brand | unmatched | - | |
| 290 | 小貓島Kittensisland (Kittensisland) | Taiwan | Brand | unmatched | - | |
| 291 | 梅康米 (MEKAMEE) | Taiwan | Brand | unmatched | - | |
| 292 | 東尼蛋創意股份有限公司 (TonyEgg Creative) | Taiwan | Agency | unmatched | - | |
| 293 | 甜蜜生活 (LDV) | Taiwan | Brand | unmatched | - | |
| 294 | HANABI | Taiwan | Brand | unmatched | - | |
| 295 | 包大山製作所 (Baozi studio) | Taiwan | Brand | unmatched | - | |
| 296 | 露天市集 (PChome eBay Co.) | Taiwan | Retail | unmatched | - | |
| 297 | Cafe and Hof | Taiwan | Retail | unmatched | - | |
| 298 | 什物 a kind of café | Taiwan | Retail | unmatched | - | |
| 299 | 婕米環球 (Jammy Global) | Taiwan | Agency | unmatched | - | |
| 300 | 聚塔創意 (TTCC) | Taiwan | Agency | unmatched | - | |
| 301 | 玩具加乘 (TOYZEROPLUS) | Taiwan | Agency | matched-label | hongkong rows 78, 79, 81, 89, 91, 92; taiwan-v2 row 5; thailand row 12 | attached IP 罐頭豬 LuLu the Piggy: INDEPENDENT; REP=no (pinned Toyzeroplus call: creator-owned, exclusively label-channelled); band 200k_1m |
| 302 | 木棉花國際 (MUSE COMMUNICATION) | Taiwan | Agency | matched-label | taiwan-v2 rows 104, 105 (evidence text) | attached IP 伊藤潤二 Junji Ito: PORTFOLIO; 木棉花國際 named as TW licensing channel |
| 303 | ds_tape | Taiwan | Brand | unmatched | - | |
| 304 | 野獸國 / BEAST KINGDOM | Taiwan | Agency | unmatched | - | |
| 305 | 好好盒作有限公司 / The Box | Taiwan | Brand | unmatched | - | |
| 306 | 國際影視有限公司 / Animation Entertainment Ltd. | Taiwan | Agency | unmatched | - | |
| 307 | 台灣角川 / KADOKAWA TAIWAN | Taiwan | Agency | ambiguous | korea row 47 (evidence text) | row IP: 던전밥 Dungeon Meshi, PORTFOLIO; evidence names Kadokawa/Trigger as owner |
| 308 | 世界漂亮在台協會 (The prettiest in the world) | Taiwan | Org | unmatched | - | |
| 309 | ARDUREY LIMITED | Taiwan | Agency | unmatched | - | |
| 310 | 沃廚 (WOKY) | Taiwan | Brand | unmatched | - | |
| 311 | 思謀研器有限公司 (Studio Smoll) | Taiwan | Brand | unmatched | - | |
| 312 | 乾唐軒 (ACERA) | Taiwan | Brand | unmatched | - | |
| 313 | FILTER017® | Taiwan | Brand | unmatched | - | |
| 314 | 安喬欣業 (25togo) | Taiwan | Brand | unmatched | - | |
| 315 | 民台科技 (FORMOSA LIGHT) | Taiwan | Brand | unmatched | - | |
| 316 | TiFiLid & Fulcro | Taiwan | Brand | unmatched | - | |
| 317 | 格洛維斯 (Glowis) | Taiwan | Brand | unmatched | - | |
| 318 | umami | Taiwan | Brand | unmatched | - | |
| 319 | IDDAT / IDDAT SelectiON | Taiwan | Retail | unmatched | - | |
| 320 | 居加良品 (Addable) | Taiwan | Brand | unmatched | - | |
| 321 | 滾雪球文具 (tsnowstationery) | Taiwan | Brand | unmatched | - | |
| 322 | VentureZac | Taiwan | Brand | unmatched | - | |
| 323 | Vinxper 電子醒酒器 | Taiwan | Brand | unmatched | - | |
| 324 | 山霧 (ZenU) | Taiwan | Brand | unmatched | - | |
| 325 | 女姝坊 (DAN DAN HANDMADE) | Taiwan | Brand | unmatched | - | |
| 326 | 台灣染 (TAIWAN DYE) | Taiwan | Brand | unmatched | - | |
| 327 | 沐籟 (Moonlight) | Taiwan | Brand | unmatched | - | |
| 328 | 溫紋陶 (WENWENWORKS) | Taiwan | Brand | unmatched | - | |
| 329 | 軟水泥生活實驗室 (CELEMENT LAB) | Taiwan | Brand | unmatched | - | |
| 330 | 林源美百年香店 (LIN,YUAN-MAI Incense) | Taiwan | Brand | unmatched | - | |
| 331 | 勇氣雜貨商行 (FUFU grocerystore) | Taiwan | Retail | unmatched | - | |
| 332 | 亭氏香氛 (TINGS AROMA) | Taiwan | Brand | unmatched | - | |
| 333 | 手提包公會 (TBA) | Taiwan | Org | unmatched | - | |
| 334 | 酷樂村 (SLEEPYVILLE CRITTERS) | Taiwan | Brand | unmatched | - | |
| 335 | 長隆實業IP授權 (EVER GREEN INTERNATIONAL) | Taiwan | Agency | unmatched | - | |
| 336 | 益裕塑膠工業 (YUE TRAVELER & BAGS) | Taiwan | Brand | unmatched | - | |
| 337 | 沙伯迪澳 (SOBDEALL) | Taiwan | Brand | unmatched | - | |
| 338 | 老師傅工作室 (Master Project Studio) | Taiwan | Brand | unmatched | - | |
| 339 | MAYBES AROMA | Taiwan | Brand | unmatched | - | |
| 340 | 天然客製皂專門 (LIKEDO) | Taiwan | Brand | unmatched | - | |
| 341 | 母栽 (moodplant) | Taiwan | Brand | unmatched | - | |
| 342 | 經典眼鏡 (CLASSICO) | Taiwan | Brand | unmatched | - | |
| 343 | 慶祝今天 (Celebrate Today) | Taiwan | Brand | unmatched | - | |
| 344 | 多淼設計 (a plant studio) | Taiwan | Brand | unmatched | - | |
| 345 | 曉創意-招財揪吉 (Dawn Creative - Lucky Toad) | Taiwan | Brand | unmatched | - | |
| 346 | 筧燭 (Reminis Candēre) | Taiwan | Brand | unmatched | - | |
| 347 | FERN ONLY 只有蕨 x mark taiwan | Taiwan | Brand | unmatched | - | |
| 348 | HEREAFTER STUDIO | Taiwan | Brand | unmatched | - | |
| 349 | HANDMADESHIP | Taiwan | Brand | unmatched | - | |
| 350 | Scentory | Taiwan | Brand | unmatched | - | |
| 351 | 插畫小農 (Hsiaoyu illustration) | Taiwan | Brand | unmatched | - | |
| 352 | 窩窩wuowuo (wuowuo) | Taiwan | Brand | unmatched | - | |
| 353 | 墨田時尚 (SUMIDA MODERN) | Taiwan | Brand | unmatched | - | |
| 354 | 香氛森林 (SCENT FOREST) | Taiwan | Brand | unmatched | - | |
| 355 | 實驗室香氛 (LABORATORYSCENT) | Taiwan | Brand | unmatched | - | |
| 356 | Hibāng | Taiwan | Brand | unmatched | - | |
| 357 | DR.WILDS 荒野醫生 | Taiwan | Brand | unmatched | - | |
| 358 | RAFAC / 戶外國度 / MOJO Camping | Taiwan | Brand | unmatched | - | |
| 359 | 鈦造 | Taiwan | Brand | unmatched | - | |
| 360 | 檜山坊 | Taiwan | Brand | unmatched | - | |
| 361 | 府城三郊營仔脚朝興宮温陵廟：温朝興商號 | Taiwan | Org/Brand | unmatched | - | |
| 362 | 瞇一下 | Taiwan | Brand | unmatched | - | |
| 363 | 三支筆工作室 | Taiwan | Brand | unmatched | - | |
| 364 | LSY 林三益 | Taiwan | Brand | unmatched | - | |
| 365 | 禪香不二 | Taiwan | Brand | unmatched | - | |
| 366 | no.30 | Taiwan | Brand | unmatched | - | |
| 367 | 無 | Taiwan | Brand | unmatched | - | |
| 368 | SAUVENIR | Taiwan | Brand | unmatched | - | |
| 369 | 小陽台 | Taiwan | Brand | unmatched | - | |
| 370 | 喜朋 | Taiwan | Brand | unmatched | - | |
| 371 | 緹家 | Taiwan | Brand | unmatched | - | |
| 372 | iNATA | Taiwan | Brand | unmatched | - | |
| 373 | 賽先生科學工廠 (Mr. Sci Science Factory) | Taiwan | Brand/Retail | unmatched | - | |
| 374 | 倆個Glass玻璃工作室 (Oursglass) | Taiwan | Brand | unmatched | - | |
| 375 | STUDIO BUBEE | Taiwan | Brand | unmatched | - | |
| 376 | dodu | Taiwan | Brand | unmatched | - | |
| 377 | 謝工作室 (TSHAPEOF) | Taiwan | Brand | unmatched | - | |
| 378 | 老3香室 (laoshan collector) | Taiwan | Brand | unmatched | - | |
| 379 | 祝好運 (BUENA SUERTE) | Taiwan | Brand | unmatched | - | |
| 380 | 這一窯 (Huiaio studio) | Taiwan | Brand | unmatched | - | |
| 381 | CEMENT PRODUCE DESIGN | Taiwan | Brand | unmatched | - | |
| 382 | 一帆布包 (Yi Fan Canvas Bags) | Taiwan | Brand | unmatched | - | |
| 383 | 獨木設計 (UniWoodesign) | Taiwan | Brand | unmatched | - | |
| 384 | 明順玻璃行 (Mingshun Glass) | Taiwan | Brand | unmatched | - | |
| 385 | 玖一藝術工作室 (91art.studio) | Taiwan | Brand | unmatched | - | |
| 386 | 手手生活 (Hands) | Taiwan | Brand | unmatched | - | |
| 387 | 小島匠所 (Evakaku) | Taiwan | Brand | unmatched | - | |
| 388 | paper diamond® | Taiwan | Brand | unmatched | - | |
| 389 | 以稀創造 (MUFUN design) | Taiwan | Brand | unmatched | - | |
| 390 | 禾日香氛 (HORI Aroma) | Taiwan | Brand | unmatched | - | |
| 391 | 鉐葉 (SHIYE) | Taiwan | Brand | unmatched | - | |
| 392 | 去哪裡都行 (goanywheredesign) | Taiwan | Brand | unmatched | - | |
| 393 | 美美實驗室 (Suii Suii Lab) | Taiwan | Brand | unmatched | - | |
| 394 | 不歸鹿 (BUGRELU) | Taiwan | Brand | unmatched | - | |
| 395 | 包手作羊毛氈 (BAO Needle Felt) | Taiwan | Brand | unmatched | - | |
| 396 | su3 | Taiwan | Brand | unmatched | - | |
| 397 | 鶯目瓷器 (YINGMULIFE) | Taiwan | Brand | unmatched | - | |
| 398 | 羊毛出在羊山上 (Sheep Mountain) | Taiwan | Brand | unmatched | - | |
| 399 | 山令頁 (ShanLingYe) | Taiwan | Brand | unmatched | - | |
| 400 | 東瑭國際有限公司 (DONG TANG) | Taiwan | Agency | unmatched | - | |
| 401 | 和漫聲音 (HOMM SOUND) | Taiwan | Brand | unmatched | - | |
| 402 | 白景 (HAKKEI) | Taiwan | Brand | unmatched | - | |
| 403 | 山本口金店 (Yamamoto Leather) | Taiwan | Brand | unmatched | - | |
| 404 | 珄笙工作室 (V&J studio) | Taiwan | Brand | unmatched | - | |
| 405 | Saw Framed | Taiwan | Brand | unmatched | - | |
| 406 | 一公分手作 (1cmhandmake) | Taiwan | Brand | unmatched | - | |
| 407 | 研石造物 X 金玉良研 X 永續材質圖書館 | Taiwan | Brand/Org | unmatched | - | |
| 408 | 紙間 (PAPIR LAB) | Taiwan | Brand | unmatched | - | |
| 409 | 02編織工作室 (02's crochet) | Taiwan | Brand | unmatched | - | |
| 410 | TOBE craft | Taiwan | Brand | unmatched | - | |
| 411 | picupi挑品 | Taiwan | Retail | unmatched | - | |
| 412 | 木合金 (WM Craft Studio) | Taiwan | Brand | unmatched | - | |
| 413 | 重要的小事 (LittleMatter) | Taiwan | Brand | unmatched | - | |
| 414 | 誠十製物所 (Sincerecraft-TW) | Taiwan | Brand | unmatched | - | |
| 415 | 本質創作室 (Essence Design & Craft) | Taiwan | Brand | unmatched | - | |
| 416 | 慢火金工創作室 (UNIGAZE Metal Art) | Taiwan | Brand | unmatched | - | |
| 417 | KOBE | Taiwan | Brand | unmatched | - | |
| 418 | 安達窯 (Anta Pottery) | Taiwan | Brand | unmatched | - | |
| 419 | 城市美文創刺繡 (DND city beauty) | Taiwan | Brand | unmatched | - | |
| 420 | 小小PETIT (PETIT) | Taiwan | Brand | unmatched | - | |
| 421 | PAPER CONCRETE | Taiwan | Brand | unmatched | - | |
| 422 | s-lock vacuum container | Taiwan | Brand | unmatched | - | |
| 423 | LUMENA | Taiwan | Brand | unmatched | - | |
| 424 | MONSTARGEAR | Taiwan | Brand | unmatched | - | |
| 425 | DDED | Taiwan | Brand | unmatched | - | |
| 426 | 簡單製造 (Simply Made) | Taiwan | Brand | unmatched | - | |
| 427 | duck_safe | Taiwan | Brand | unmatched | - | |
| 428 | CHICKEN IN THE LAB | Taiwan | Brand | unmatched | - | |
| 429 | 針線球 (Yarn Ball) | Taiwan | Brand | unmatched | - | |
| 430 | 地獄書道 kaishodo calligraphy | Taiwan | Brand | unmatched | - | |
| 431 | 蒙恬實業 (IWI) | Taiwan | Brand | unmatched | - | |
| 432 | 彩虹文創 (Rainbow Creative) | Taiwan | Agency | unmatched | - | |
| 433 | 茄子先生 (Mr. Eggplants) | Taiwan | Brand | unmatched | - | |
| 434 | 陳皮製茶 (CHEN PI TEA) | Taiwan | Brand | unmatched | - | |
| 435 | HMM | Taiwan | Brand | unmatched | - | |
| 436 | Tse Sai Pei | Taiwan | Brand | unmatched | - | |
| 437 | Overloaddance | Taiwan | Brand | unmatched | - | |
| 438 | Koazuma小木屋文創 (Koazuma) | Taiwan | Brand | unmatched | - | |
| 439 | 布嵐的販賣部 (BuLan's Studio) | Taiwan | Brand | unmatched | - | |
| 440 | 比爾公主沒蓋子 (Billnogates) | Taiwan | Brand | unmatched | - | |
| 441 | WINTEN | Taiwan | Brand | unmatched | - | |
| 442 | 汲溡宇 (Godsend medical) | Taiwan | Brand | unmatched | - | |
| 443 | 原木哲學/檜木居香氛生活 (feelosophy/Cypress House) | Taiwan | Brand | unmatched | - | |
| 444 | ANUNNAKI | Taiwan | Brand | unmatched | - | |
| 445 | 雄獅文具 (Lion Pencil) | Taiwan | Brand | unmatched | - | |
| 446 | 東億兆實業有限公司 (NIKKO HELMETS) | Taiwan | Brand | unmatched | - | |
| 447 | justfont | Taiwan | Brand/Service | unmatched | - | |
| 448 | 大象杯 (Elephant Cuppa) | Taiwan | Brand | unmatched | - | |
| 449 | 穩邁文創有限公司 (STEP Cultural and Creative) | Taiwan | Agency | unmatched | - | |
| 450 | 好玻 (GOODGLAS) | Taiwan | Brand | unmatched | - | |
| 451 | 點睛設計 (DOT design) | Taiwan | Service | unmatched | - | |
| 452 | 艸一田人 (HUANGS STUDIO) | Taiwan | Brand | unmatched | - | |
| 453 | 日日森活 (Mori Daily) | Taiwan | Brand | unmatched | - | |
| 454 | 大振豐洋傘 (Tcf.) | Taiwan | Brand | unmatched | - | |
| 455 | Threedotstype Type Foundry | Taiwan | Brand/Service | unmatched | - | |
| 456 | Blank Studio | Taiwan | Service | unmatched | - | |
| 457 | A | Taiwan | Brand | unmatched | - | |
| 458 | TCOD台中原創 | Taiwan | Org | unmatched | - | |
| 459 | 國立故宮博物院 | Taiwan | Org | matched-brandside | taiwan-v2 row 51 | brand-side co-party (7-ELEVEN Taiwan x 國立故宮博物院); row IP: Bugcat Capoo x 故宮100周年, INDEPENDENT REP=no |
| 460 | 嘉義縣文化觀光局 | Taiwan | Org | unmatched | - | |
| 461 | 宜蘭敬好生活 | Taiwan | Org | unmatched | - | |
| 462 | 山林製造 | Taiwan | Brand | unmatched | - | |
| 463 | 嘉義市政府文化局 | Taiwan | Org | unmatched | - | |
| 464 | 屏東縣政府 | Taiwan | Org | unmatched | - | |
| 465 | 台灣專利超級站 | Taiwan | Org/Service | unmatched | - | |
| 466 | 台糖公司 | Taiwan | Org | unmatched | - | |
| 467 | 臺北市政府青年局 | Taiwan | Org | unmatched | - | |
| 468 | 羊泥工坊 | Taiwan | Brand | unmatched | - | |
| 469 | 洋樓拾憶文創工作室 | Taiwan | Brand | unmatched | - | |
| 470 | 帕崎工作室 | Taiwan | Brand | unmatched | - | |
| 471 | 光沐之間 (WINTASY) | Taiwan | Brand | unmatched | - | |
| 472 | 銅樂 (TONGLE) | Taiwan | Brand | unmatched | - | |
| 473 | 雱 PĀNG | Taiwan | Brand | unmatched | - | |
| 474 | 吾手 (Wooso) | Taiwan | Brand | unmatched | - | |
| 475 | 波鳥 (bobird) | Taiwan | Brand | unmatched | - | |
| 476 | 璃河 (glassriver) | Taiwan | Brand | unmatched | - | |
| 477 | 清嶼 (tranquil island) | Taiwan | Brand | unmatched | - | |
| 478 | 5AM Jewelry | Taiwan | Brand | unmatched | - | |
| 479 | 山桔 (Sunjit) | Taiwan | Brand | unmatched | - | |
| 480 | WILD TYPE | Taiwan | Brand | unmatched | - | |
| 481 | 玳作 (Dazzle Jewelry) | Taiwan | Brand | unmatched | - | |
| 482 | 恬日 (tan.nichi) | Taiwan | Brand | unmatched | - | |
| 483 | 象往 (elephantsgogo) | Taiwan | Brand | unmatched | - | |
| 484 | 寓物設計 (Yuwu Design) | Taiwan | Service | unmatched | - | |
| 485 | 雜然設計 (zarandesign) | Taiwan | Brand | unmatched | - | |
| 486 | 一屋｜客製化寵物商品 (1Woof) | Taiwan | Brand | unmatched | - | |
| 487 | 織療室 (ziliaoshi) | Taiwan | Brand | unmatched | - | |
| 488 | 川衣 (WEAR BEING) | Taiwan | Brand | unmatched | - | |
| 489 | 好悠栽 (Decentplanting) | Taiwan | Service | unmatched | - | |
| 490 | 彭 · 璐 (PENG LU POTTERY) | Taiwan | Brand | unmatched | - | |
| 491 | 密密制作 (memedo) | Taiwan | Brand | unmatched | - | |
| 492 | 讚讚製造 (Good Good Goods) | Taiwan | Brand | unmatched | - | |
| 493 | 往山裡走 (in the mountains) | Taiwan | Brand | unmatched | - | |
| 494 | 山織 (Mount) | Taiwan | Brand | unmatched | - | |
| 495 | 一米作物 (Immyhandmake) | Taiwan | Brand | unmatched | - | |
| 496 | 款款飾物工作室 (KUÂN KUÂN) | Taiwan | Brand | unmatched | - | |
| 497 | 有點市 | Taiwan | Retail | unmatched | - | |
| 498 | 日耀堂 (BetterDays studio®) | Taiwan | Agency | unmatched | - | |
| 499 | 小怪選物 (THE WEIRD STUDIO) | Taiwan | Retail | unmatched | - | |
| 500 | MILL HOUSE | Taiwan | Brand | unmatched | - | |
| 501 | 零尚壹 | Taiwan | Brand | unmatched | - | |
| 502 | 愛爾蘭funs (Irelandfuns) | Taiwan | Brand | unmatched | - | |
| 503 | 國泰世華銀行 (Cathay United Bank) | Taiwan | Org | unmatched | - | |
| 504 | 五桐號 | Taiwan | Brand | matched-brandside | taiwan-v2 rows 2, 13, 107 | row entity is the licensee brand; row IPs: Chiikawa (PORTFOLIO), Care Bears (PORTFOLIO), Dinotaeng (INDEPENDENT REP=yes) |
| 505 | TALUMA 知返設計 | Taiwan | Brand | unmatched | - | |
| 506 | BOMBOM Co., | Taiwan / Korea (exchange agency, HQ unclear) | Agency | unmatched | - | |
| 507 | 泰國館 (Thai Pavilion) - Cheesy Duck/Stop | Thailand | Org | unmatched | - | |
| 508 | UNMELT | Thailand | Brand | unmatched | - | |
| 509 | Thailand Creative House | Thailand | Org | unmatched | - | |
| 510 | PAHKAHMAH THAILAND | Thailand | Brand | unmatched | - | |
| 511 | WISHULADA | Thailand | Brand | unmatched | - | |
| 512 | LGBTQq | Thailand | Org | unmatched | - | |
| 513 | Bloody Bunny | Thailand | IP | unmatched | - | |
| 514 | Baan Maew Maew | Thailand | IP | unmatched | - | |
| 515 | Sweet Summer | Thailand | IP | unmatched | - | |
| 516 | Shewsheep | Thailand | IP | matched-ip | thailand row 74 | INDEPENDENT; REP=yes; band 50k_200k |
| 517 | Warbie Yama | Thailand | IP | unmatched | - | |
| 518 | FLUFFY OMELET STUDIO | Thailand | IP | unmatched | - | |
| 519 | Humor Sapiens | Thailand | Brand | unmatched | - | |
| 520 | Plaplatootoo | Thailand | IP | unmatched | - | |
| 521 | 英國if文創 (if & Bookaroo) | UK | Agency | out-of-coverage | - | no census exists for UK; reported as out-of-coverage, not substituted |

