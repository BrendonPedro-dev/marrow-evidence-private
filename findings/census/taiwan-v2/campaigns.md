# Taiwan co-branding census (v2 re-run) - campaign log

This is the **v2 re-run** of the Taiwan co-branding census (聯名), rebuilt on the IDENTICAL definition, pinned edge cases, and REPRESENTABLE sub-tag now used for the Japan (131 rows, `findings/census/japan/campaigns.md`) and Korea (135 rows, `findings/census/korea/campaigns.md`) runs, so all three markets compare cleanly.
Window: 2024-01-01 to run date (full-year 2024, full-year 2025, 2026 year-to-date, kept separable).

**Method for this re-run - re-classify + enrich, not re-find.** The 129 rows below are carried over verbatim (data, sources, dates) from the v1 census at `findings/census/campaigns.md` - every one was already confirmed against at least one fetched source URL there.
This run (a) re-classifies every row against the updated ownership test + pinned edge cases, flagging any row whose bucket CHANGES (see "Reclassification delta" below), and (b) adds the REPRESENTABLE column to every INDEPENDENT row.
No new fetching was required because the underlying rows were already curl-verified in v1; rows resting on a single roundup source stay flagged in Notes.

**YEAR tag** is by campaign start/run date: `2024` = 2024-01-01..2024-12-31, `2025` = 2025-01-01..2025-12-31, `2026YTD` = 2026-01-01..run date.

**The ownership test (identical across all markets):** who OWNS and CONTROLS the IP now? Not fame, not size, not who runs the campaign.
- **PORTFOLIO** = owned/controlled by a major licensor, studio, media/platform conglomerate, licensing company, or estate that manages OTHER IP.
- **INDEPENDENT** = owned by a living creator or a small studio with no portfolio parent; agency-MANAGED but creator-OWNED still counts as independent (represented ≠ owned).
- **UNCLEAR** = ownership genuinely cannot be established after a second search, or a true borderline.

**Pinned edge cases (identical to Japan/Korea runs):** Chiikawa 吉伊卡哇 (nagano) = PORTFOLIO (publisher/committee-managed); Snoopy/Peanuts = PORTFOLIO (Sony controlling stake); Miffy 米飛/Mercis BV = PORTFOLIO (estate, creator deceased - portfolio even as a single iconic character); Sanrio / San-X / Pokemon-Nintendo / Disney / KAKAO FRIENDS / BT21-LINE FRIENDS = PORTFOLIO; a brand's OWN mascot = NOT COUNTED; government/public-body-OWNED IP = EXCLUDED from the split (none found in Taiwan - all IPs here are privately owned even where the brand is public); webtoon/platform characters = INDEPENDENT if the artist owns it, PORTFOLIO if the platform owns it; co-owned/JV = whoever holds control, genuine 50/50 = UNCLEAR.

**REPRESENTABLE** (INDEPENDENT rows only) = yes / no / unclear: yes = creator-owned, no conglomerate stake, not locked to an exclusive agency/captive studio in a way that precludes representation (a plausible PBC client); no = indie by ownership but already exclusively tied up (own captive licensing studio, third-party exclusive master licensor); unclear = can't tell from public sources. This is the market-entry signal - how much *addressable* indie IP exists, not just how much indie IP exists.

| # | Date / window | Year | Brand | IP | IP class | Class evidence | REPRESENTABLE | Format | Source | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 2024 (paper-cup series) | 2024 | 清心福全 | 貓貓蟲咖波 Bugcat Capoo | INDEPENDENT | Creator 亞拉, owned via his own studio 卡特島創意 (Carter Island); no conglomerate parent | no | Drink (9 cup designs) + merch | https://udn.com/news/story/7186/8074761 | REP=no: Carter Island is the creator's own captive licensing studio running an active TW program |
| 2 | 2024-08-23..09-30 | 2024 | 五桐號 | 吉伊卡哇 Chiikawa | PORTFOLIO | Chiikawa (nagano) publisher/committee-managed; PORTFOLIO per pinned rule | - | Drink (4 cup designs) + 便利貼 | https://udn.com/news/story/7270/8171769 | |
| 3 | 2024-10-30..12-31 | 2024 | 7-ELEVEN Taiwan | 吉伊卡哇 Chiikawa | PORTFOLIO | Same as row 2 | - | 集點 add-on merch | https://news.para-daily.com/2024/10/25/chiikawa-7-11-cobrands-tw/ | Also 7-11 event page 24mickey/chiikawa.aspx |
| 4 | 2025-05-11..06-14 | 2025 | 壽司郎 Sushiro Taiwan | 貓貓蟲咖波 Bugcat Capoo | INDEPENDENT | Same as row 1 | no | Food + store (6 themed) + blind-bag merch | https://travel.udn.com/travel/story/7193/9487495 | REP=no (Carter Island) |
| 5 | 2025 (summer) | 2025 | 麥味登 | LuLu the Piggy 露露豬 | INDEPENDENT | Designer-toy IP by Cici (Cici's Story); creator-owned, no conglomerate stake | no | Food + store + merch | https://cava.tw/lifestyle/travel-food/265108 | REP=no: exclusively channelled through ToyzeroPlus label + 52TOYS distribution; single roundup source - flagged |
| 6 | 2025 (summer) | 2025 | Mister Donut Taiwan | 寶可夢 Pokemon | PORTFOLIO | The Pokemon Company / Nintendo | - | Food + merch | https://cava.tw/lifestyle/travel-food/265108 | Single roundup source - flagged |
| 7 | 2025 (summer) | 2025 | 弘爺漢堡 | Hello Kitty / Kuromi | PORTFOLIO | Sanrio | - | Add-on merch | https://cava.tw/lifestyle/travel-food/265108 | Single roundup source - flagged |
| 8 | 2025 (summer) | 2025 | 桂冠冰菓室 | 布丁狗 Pompompurin | PORTFOLIO | Sanrio | - | Food, limited packaging | https://cava.tw/lifestyle/travel-food/265108 | Single roundup source - flagged |
| 9 | 2025 (summer) | 2025 | 大武山牧場 | Peko ペコ (不二家 Fujiya) | PORTFOLIO | Fujiya, major Japanese confectioner | - | Food + merch | https://cava.tw/lifestyle/travel-food/265108 | Single roundup source - flagged |
| 10 | 2026-01-26.. | 2026YTD | CoCo都可 | 美樂蒂 My Melody | PORTFOLIO | Sanrio | - | Drink + merch | https://www.beauty321.com/post/71098 | Also playing.ltn 32370, WalkerLand 421569 |
| 11 | 2026-02-02..04-13 | 2026YTD | 龜記茗品 | Labubu | PORTFOLIO | Kasing Lung character owned by POP MART, a listed IP/licensing conglomerate | - | Drink + merch + lucky draw | https://woman.udn.com/woman/story/123162/9293523 | Also playing.ltn 32370, WalkerLand 421569 |
| 12 | 2026 (spring) | 2026YTD | TeaTop 第一味 | 戀與深空 Love and Deepspace | PORTFOLIO | Mobile-game IP by 疊紙 Papergames, a large game studio | - | Drink | https://www.walkerland.com.tw/subject/view/421569 | Single roundup source - flagged |
| 13 | 2026 (spring) | 2026YTD | 五桐號 | Care Bears | PORTFOLIO | Cloudco Entertainment, major US licensor | - | Drink + merch | https://cava.tw/lifestyle/travel-food/263159 | Single roundup source - flagged |
| 14 | 2026-02 (CNY) | 2026YTD | 得正 | OBJECT / SOSO FAMILY | UNCLEAR | Korean character brand; ownership/parent not established under queries run | - | Merch | https://cava.tw/lifestyle/travel-food/263159 | Single roundup source; class unresolved |
| 15 | 2026-02 | 2026YTD | 功夫茶 | 《功夫》 Kung Fu Hustle (film) | UNCLEAR | Film IP (Stephen Chow / Star Overseas); film licence, borderline vs character-IP co-branding | - | Drink | https://cava.tw/lifestyle/travel-food/263159 | Single roundup source; scope-borderline |
| 16 | 2026-02 | 2026YTD | 發發 | 乖乖 Kuai Kuai | UNCLEAR | 乖乖 is a corporate snack brand/mascot, not a character-illustration IP; brand-x-brand tie-in | - | Drink (yogurt) | https://cava.tw/lifestyle/travel-food/263159 | Single roundup source; scope-borderline |
| 17 | 2026-07-01..07-19 | 2026YTD | 金色雙島藝術祭 (馬公市公所 tourism festival) | 白爛貓 Lan Lan Cat | INDEPENDENT | Original Taiwan illustration IP (source: 超人氣原創IP), creator-owned, no conglomerate parent; brand is public but IP is private (counted) | unclear | Event (island art festival + commemorative fans) | https://truemii.chinatimes.com/content/20260627002337-265003 | REP=unclear: licensing entity/exclusivity for 白爛貓 not established; single-source |
| 18 | 2024-11-04..12-29 | 2024 | 7-ELEVEN Taiwan | 卡娜赫拉的小動物 Kanahei (Piske & Usagi) | INDEPENDENT | Kanahei is an individual JP illustrator who owns her characters; agency-managed but creator-owned | no | 集點 add-on merch | https://www.7-11.com.tw/event/24mickey/kanahei.aspx | REP=no: creator-owned but locked to an exclusive master licensor (per Japan run row 62) |
| 19 | 2024-11-04..12-31 | 2024 | 7-ELEVEN Taiwan | 貓福珊迪 mofusand x 三麗鷗 | PORTFOLIO | Joint campaign with Sanrio characters; Sanrio side makes it portfolio | - | 集點 add-on merch | https://www.7-11.com.tw/event/24mofusanrio/index.aspx | mofusand-solo rows (122,126) are INDEPENDENT; this Sanrio-paired wave is portfolio |
| 20 | 2024-10-17..11-10 | 2024 | 新光三越 A9 | 任天堂 Nintendo (Mario/Zelda/動森/Pikmin/Splatoon) | PORTFOLIO | Nintendo | - | Store/event (POP-UP + 周年慶集點) | https://udn.com/news/story/7270/8278936 | Department-store format |
| 21 | 2024 (股東會) | 2024 | 富采 Ennostar (listed) | 黃阿瑪的後宮生活 Fumeancats | INDEPENDENT | IP owned by creators 志銘與狸貓, no conglomerate parent | no | Corporate premium (shareholder 帆布袋) | https://finance.ettoday.net/news/2913939 | REP=no: run through the creators' own captive brand operation (self-managed licensing); single source |
| 22 | 2025-01-08..02-19 | 2025 | 7-ELEVEN Taiwan | 史努比 Snoopy (Peanuts 75周年) | PORTFOLIO | Peanuts controlled by WildBrain/Sony/Schulz consortium; Sony controlling stake per pinned rule | - | 集點 add-on merch | https://www.7-11.com.tw/event/25snoopy/index.aspx | Official event page |
| 23 | 2025-01-22..02-28 | 2025 | 長榮航空 EVA Air | Hello Kitty | PORTFOLIO | Sanrio | - | Event/transport (粉萌機 A321 livery) | https://www.cna.com.tw/news/ahel/202412230277.aspx | Livery run inside existing EVA-Sanrio partnership |
| 24 | 2025-02-19..04-30 | 2025 | 7-ELEVEN Taiwan | 湯姆貓與傑利鼠 Tom and Jerry (85週年) | PORTFOLIO | Warner Bros. Discovery | - | 集點 add-on merch | https://www.7-11.com.tw/event/25tomandjerry/index.aspx | Official event page |
| 25 | 2025-03-26..04-30 | 2025 | 7-ELEVEN Taiwan | 哆啦A夢 Doraemon | PORTFOLIO | Fujiko Pro / Shogakukan-Shueisha Productions | - | 快閃購 merch | https://www.7-11.com.tw/event/25tomandjerry/doraemon.aspx | Official event page |
| 26 | 2025-04-02..05-31 | 2025 | 7-ELEVEN Taiwan | 蠟筆小新 / 獵人 / 福音戰士 | PORTFOLIO | Publisher/committee-managed anime IPs (Futabasha; Shueisha; khara) | - | 集點 add-on merch (50+ items) | https://www.7-11.com.tw/event/25tomandjerry/shinchan.aspx | One wave bundling three anime IPs; counted once |
| 27 | 2025-04-16..05-18 | 2025 | 7-ELEVEN Taiwan | 三麗鷗 Sanrio x HUNTER | PORTFOLIO | Sanrio (paired with boot brand HUNTER) | - | 集點 add-on merch (incl. luggage) | https://www.7-11.com.tw/event/25tomandjerry/huntersanrio.aspx | Official event page |
| 28 | 2025-04 (春遊) | 2025 | 丸亀製麵 Marugame Taiwan | 爽爽貓 SongSongMeow | INDEPENDENT | Taiwan illustrator IP by SECOND, creator-owned | yes | Food-chain 集點 | https://www.marukametw.com/rewardpoint2504.php | REP=yes: individual creator (SECOND), open ad-hoc brand collabs; JS-shell page, title curl-verified |
| 29 | 2025 (股東會 05-23) | 2025 | 富采 Ennostar | 黃阿瑪的後宮生活 Fumeancats | INDEPENDENT | Same as row 21 | no | Corporate premium (不鏽鋼雙層碗) | https://finance.ettoday.net/news/2913939 | REP=no (own captive operation); single source; 2nd consecutive year |
| 30 | 2025-07-23..09-16 | 2025 | 7-ELEVEN Taiwan | 哆啦A夢 (電影) | PORTFOLIO | Fujiko Pro / ShoPro | - | 集點 add-on merch | https://chinesedora.com/news/94700.htm | Single fan-news source |
| 31 | 2025-09-10 (announced) | 2025 | 《超蝦大作戰》 (mobile game, TW) | 白爛貓 Lan Lan Cat | INDEPENDENT | Creator-owned Taiwan illustration IP | unclear | Gaming (in-game character + events) | https://gnn.gamer.com.tw/detail.php?sn=292015 | REP=unclear (see row 17) |
| 32 | 2025-09..10 | 2025 | 中華郵政 Chunghwa Post | 貓貓蟲咖波 Bugcat Capoo | INDEPENDENT | Same as row 1 | no | Stamps + merch + 限定咖波郵局 | https://applealmond.com/posts/293406 | REP=no (Carter Island); indie IP lands a national institution; single source |
| 33 | 2025-11 | 2025 | 家而適 | 爽爽貓 SongSongMeow | INDEPENDENT | Same as row 28 | yes | Lifestyle retail (storage/home goods) | https://www.yes566.com.tw/songsongmeow/ | REP=yes; date inferred from page asset timestamps; 3rd collab wave |
| 34 | 2026-03-04.. | 2026YTD | 7-ELEVEN Taiwan | 蠟筆小新 (睡衣派對) | PORTFOLIO | Futabasha-managed | - | 集點 add-on merch (81 items) | https://supertaste.tvbs.com.tw/accessories/358616 | Single roundup source - flagged |
| 35 | 2026 (spring wave) | 2026YTD | 7-ELEVEN Taiwan | OSAMU GOODS 原田治 (棒球系列) | PORTFOLIO | **RECLASSIFIED v2 (was UNCLEAR):** creator Osamu Harada deceased (d.2016); OSAMU GOODS is now an estate/heritage-brand goods property - PORTFOLIO per the deceased-creator/estate pinned rule (Miffy precedent) | - | 集點 add-on merch | https://supertaste.tvbs.com.tw/accessories/358616 | Single roundup source |
| 36 | 2026-03-11.. | 2026YTD | 7-ELEVEN Taiwan | ANNA SUI x 三麗鷗 | PORTFOLIO | Sanrio (paired with ANNA SUI) | - | 集點 add-on merch (第2波) | https://supertaste.tvbs.com.tw/accessories/358616 | Single roundup source - flagged |
| 37 | 2026 (spring wave) | 2026YTD | 7-ELEVEN Taiwan | 牛仔史努比 Cowboy Snoopy | PORTFOLIO | Peanuts consortium (Sony controlling stake) | - | 集點 add-on merch | https://supertaste.tvbs.com.tw/accessories/358616 | Single roundup source - flagged |
| 38 | 2026-04-29 (on sale) | 2026YTD | 悠遊卡公司 EasyCard | 吉伊卡哇 Chiikawa | PORTFOLIO | Publisher/committee-managed | - | Transit-card product (3款 SuperCard) | https://tech.udn.com/tech/story/124457/9469101 | Borderline co-brand vs licensed product; kept |
| 39 | 2026 (股東會 06-18) | 2026YTD | 華南金控 Hua Nan Financial (listed FHC) | 貓貓蟲咖波 Bugcat Capoo | INDEPENDENT | Same as row 1 | no | Corporate premium (雙盤組) | https://money.udn.com/money/story/5613/9412556 | REP=no (Carter Island); indie IP lands a major FHC |
| 40 | 2024-07-19..08-15 | 2024 | 藏壽司 Kura Sushi Taiwan | 名偵探柯南 Detective Conan | PORTFOLIO | Shogakukan/committee-managed anime IP | - | Food-chain gacha (30款扭蛋) | https://www.walkerland.com.tw/subject/view/393664 | Dates on page |
| 41 | 2024-08-23..09-02 | 2024 | 藏壽司 Kura Sushi Taiwan | 吉伊卡哇 Chiikawa | PORTFOLIO | Publisher/committee-managed | - | Food-chain gacha (18款扭蛋) | https://gnn.gamer.com.tw/detail.php?sn=272437 | The 藏壽司之亂; early end from demand |
| 42 | 2024-10-02..12-31 | 2024 | 7-ELEVEN Taiwan | 迪士尼米奇與好朋友 Disney Mickey & Friends | PORTFOLIO | Disney | - | 集點 add-on merch | https://www.7-11.com.tw/event/24mickey/index.aspx | Parent wave of rows 3/18 siblings |
| 43 | 2025-01-22..02-16 | 2025 | 7-ELEVEN Taiwan | 白爛貓 Lan Lan Cat + 我不是胖虎 (蛇來運轉) | INDEPENDENT | Both creator-owned Taiwan illustrator IPs | unclear | 集點/快閃購 (incl. 白爛貓 x SOL 安全帽) | https://www.7-11.com.tw/event/25snoopy/lancat.aspx | REP=unclear: two indie IPs, licensing entities/exclusivity not established; counted once |
| 44 | 2025-03-26..04-06 | 2025 | 7-ELEVEN Taiwan | 怪獸大學 Monsters University | PORTFOLIO | Disney/Pixar | - | 集點 add-on merch | https://www.7-11.com.tw/event/25tomandjerry/monsters.aspx | Official event page |
| 45 | 2025-03-26.. | 2025 | 麥當勞 McDonald's Taiwan | MINECRAFT 麥塊電影 | PORTFOLIO | Mojang/Microsoft (film: Warner Bros.) | - | Food + 盲盒公仔 + 兒童餐 | https://supertaste.tvbs.com.tw/food/354091 | Single roundup source - flagged |
| 46 | 2025-04-09..04-30 | 2025 | 7-ELEVEN Taiwan | 玩具總動員 Toy Story (30週年) | PORTFOLIO | Disney/Pixar | - | 集點 add-on merch | https://www.7-11.com.tw/event/25tomandjerry/toystory.aspx | Official event page |
| 47 | 2025-05-28.. | 2025 | 全家 FamilyMart Taiwan | 寶可夢 Pokemon (TCG 特典卡) | PORTFOLIO | The Pokemon Company / Nintendo | - | Convenience store (滿299送卡包) | https://pokemonhubs.com/ptcg/familymart-ptcg-taiwan-2025/ | Single fan-news source |
| 48 | 2025-09 | 2025 | 肯德基 KFC Taiwan | 航海王 One Piece | PORTFOLIO | Shueisha/Toei-managed anime IP | - | Food (惡魔果實咔啦海陸堡) | https://playing.ltn.com.tw/article/31947 | Single roundup source - flagged |
| 49 | 2025-10 | 2025 | 全家 FamilyMart Taiwan | 原神 Genshin Impact | PORTFOLIO | HoYoverse/miHoYo, major game conglomerate | - | Convenience store (聯名美食) | https://www.4gamers.com.tw/saged/detail/5q9w0xg1jxq7jl | TW-only stated on page |
| 50 | 2025-10-08.. | 2025 | 麥當勞 McDonald's Taiwan | TinyTAN (BTS) | PORTFOLIO | HYBE-owned character IP | - | Blind-box 公仔 (7款) | https://www.ettoday.net/news/20251002/3043663.htm | |
| 51 | 2025-10-29..12-31 | 2025 | 7-ELEVEN Taiwan x 國立故宮博物院 | 貓貓蟲咖波 Bugcat Capoo (x 故宮100周年) | INDEPENDENT | Same as row 1; museum is co-brand partner, Capoo is the IP | no | 全店精品集點 (7,100+ stores) | https://talkacemedia.com/article/42024 | REP=no (Carter Island); indie IP carries a flagship full-store 集點 wave |
| 52 | 2025-10/11 | 2025 | 7-ELEVEN Taiwan | noodoll | INDEPENDENT | Independent London designer plush brand, no conglomerate parent | yes | 集點 add-on merch | https://talkacemedia.com/article/42024 | REP=yes: small independent design brand, open collabs; single source - flagged |
| 53 | 2026-01-07..02-18 | 2026YTD | 悠遊卡公司 EasyCard | 卡娜赫拉的小動物 Kanahei | INDEPENDENT | Same as row 18 | no | Transit-card (Supercard 3款) | https://www.easycard.com.tw/museum?page=1&keywords=%E5%8D%A1%E5%A8%9C | REP=no (exclusive master licensor); borderline co-brand vs licensed product, kept per row 38 |
| 54 | 2026-04 | 2026YTD | 麥當勞 McDonald's Taiwan | 超級瑪利歐 Super Mario | PORTFOLIO | Nintendo | - | Blind-box 公仔 (12款) | https://www.cool-style.com.tw/wd2/archives/1285201 | Single roundup source - flagged |
| 55 | 2026-06-24..09-01 | 2026YTD | 全家 FamilyMart Taiwan | FINAL FANTASY XIV 繁中版 | PORTFOLIO | Square Enix | - | Convenience store (聯名漢堡 + 虛寶) | https://event.ffxiv.com.tw/2026/familymart/ | Official event microsite |
| 56 | 2026-07 (summer) | 2026YTD | 特‧好喝 | 蠟筆小新 Crayon Shin-chan | PORTFOLIO | Futabasha-managed | - | Drink (3款冰沙) + merch | https://supertaste.tvbs.com.tw/food/360433 | Single roundup source - flagged |
| 57 | 2026-07 (summer) | 2026YTD | 先喝道 | SPY×FAMILY 間諜家家酒 | PORTFOLIO | Shueisha-managed anime IP | - | Drink + campaign | https://supertaste.tvbs.com.tw/food/360433 | Single roundup source - flagged |
| 58 | 2026-07-17.. | 2026YTD | 藏壽司 Kura Sushi Taiwan | 名偵探柯南 Detective Conan | PORTFOLIO | Shogakukan/committee-managed | - | Food-chain gacha (24款扭蛋) | https://udn.com/news/story/7270/9624904 | Distinct from 2024 Conan campaign (row 40) |
| 59 | 2024-06-28..09-05 | 2024 | 全聯 PXmart | 蠟筆小新 Crayon Shin-chan | PORTFOLIO | Futabasha-managed | - | Supermarket loyalty | https://www.fincake.co/blog/pxmart-points | Single fincake source |
| 60 | 2024-06-28..09-05 | 2024 | 全聯 PXmart | KAKAO FRIENDS | PORTFOLIO | Kakao Corp, major Korean platform conglomerate; PORTFOLIO per pinned rule | - | Supermarket loyalty (換購廚具) | https://www.fincake.co/blog/pxmart-points | Single fincake source |
| 61 | 2024-12 | 2024 | 鶴茶樓 | Bunni Konbiny 兔子便利商店 | UNCLEAR | Designer character brand; ownership/parent not established under queries run | - | Drink + merch | https://www.ctwant.com/article/382389/ | |
| 62 | 2024-12-18..2025-02-26 | 2024 | 客美多咖啡 KOMEDA'S Coffee Taiwan | 布丁狗 Pompompurin | PORTFOLIO | Sanrio | - | Coffee chain (飲品/甜點 + 周邊) | https://gnn.gamer.com.tw/detail.php?sn=277798 | Also ctwant 382389, udn 8413010 |
| 63 | 2024-12-19.. | 2024 | 可不可熟成紅茶 KEBUKE | 玩具總動員 Toy Story | PORTFOLIO | Disney/Pixar | - | Drink + 10款杯身 + 周邊 | https://supertaste.tvbs.com.tw/food/352587 | Also ctwant 382389 |
| 64 | 2024-12 | 2024 | 萬波島嶼紅茶 Wanpo | 飛天小女警 The Powerpuff Girls | PORTFOLIO | Warner Bros. Discovery / Cartoon Network | - | Drink + merch | https://dailyview.tw/popular/detail/28438 | Single roundup source - flagged |
| 65 | 2024-12-24..2025-05-04 | 2024 | 路易莎咖啡 Louisa | 草間彌生 Yayoi Kusama | INDEPENDENT | **RECLASSIFIED v2 (was UNCLEAR):** living fine artist who owns her own artwork, no conglomerate parent - INDEPENDENT per the Japan run's fine-artist precedent (Higuchi/Nagaba/Murakami all INDEPENDENT); scope caveat (exhibition-tie-in cups) retained | no | Coffee chain (聯名紙杯/杯身) | https://udn.com/news/story/7186/8442048 | REP=no: among the most tied-up living artists (exclusive major-gallery representation / own studio) |
| 66 | 2024-12-27..2025-02-16 | 2024 | 新光三越 A11 | 進擊的巨人 Attack on Titan | PORTFOLIO | Kodansha/committee-managed anime IP | - | Dept-store pop-up | https://www.4gamers.com.tw/news/detail/69287/kimetsu-aot-kanahei-garfield-pop-up-store-taiepi-a11-2024-winter | Venue-hosted pop-up, kept per row-20 precedent |
| 67 | 2024-12-27..2025-02-16 | 2024 | 新光三越 A11 | 鬼滅之刃 Demon Slayer | PORTFOLIO | Shueisha/Aniplex committee-managed | - | Dept-store pop-up | https://www.4gamers.com.tw/news/detail/69287/kimetsu-aot-kanahei-garfield-pop-up-store-taiepi-a11-2024-winter | Same venue window as row 66 |
| 68 | 2024-12-27..2025-02-16 | 2024 | 新光三越 A11 | 卡娜赫拉的小動物 Kanahei (睡衣派對) | INDEPENDENT | Same as row 18 | no | Dept-store pop-up | https://gnn.gamer.com.tw/detail.php?sn=278818 | REP=no (exclusive master licensor); the one indie among four A11 pop-ups |
| 69 | 2024-12-27..2025-02-16 | 2024 | 新光三越 A11 | 加菲貓 Garfield | PORTFOLIO | Garfield owned by Paramount (acquired 2019) | - | Dept-store pop-up | https://www.4gamers.com.tw/news/detail/69287/kimetsu-aot-kanahei-garfield-pop-up-store-taiepi-a11-2024-winter | Same venue window as row 66 |
| 70 | 2025-03 / 05-28 | 2025 | 星巴克 Starbucks Taiwan | 史努比 Snoopy (PEANUTS) | PORTFOLIO | Peanuts consortium (Sony controlling stake) | - | Coffee chain merch (8款杯款) | https://www.skm.com.tw/skmmedia/lifestyleandfood/living/peanuts0318op | Two 2025 waves counted once |
| 71 | 2025-06-05.. | 2025 | 85度C | 蠟筆小新 Crayon Shin-chan | PORTFOLIO | Futabasha-managed | - | Food (4款蛋糕 + 公仔) | https://supertaste.tvbs.com.tw/food/355048 | Also nownews 6690638 |
| 72 | 2025-06-28..09-14 | 2025 | 華山1914文創園區 (x 楽玩多) | 三麗鷗男團 HAPIDANBUI | PORTFOLIO | Sanrio | - | Culture-park pop-up | https://www.huashan1914.com/w/huashan1914/exhibition_25062017525772023 | Official venue page; venue-hosted pop-up |
| 73 | 2025-08.. | 2025 | 東旅集團 Hotel East | 三麗鷗男團 HAPIDANBUI | PORTFOLIO | Sanrio | - | Hotel (5款主題房 + 備品) | https://www.mook.com.tw/article/38479 | |
| 74 | 2025-08-29..31 | 2025 | 味全龍 WeiChuan Dragons (CPBL) | hololive production (EN) | PORTFOLIO | Cover Corp, Tokyo-listed VTuber conglomerate | - | Sports event (主題日 + 周邊) | https://www.gvm.com.tw/article/131331 | First edition confirmed |
| 75 | 2025 | 2025 | 高雄漢來大飯店 Grand Hi-Lai | 三麗鷗8大角色 | PORTFOLIO | Sanrio | - | Hotel (10間主題房) | https://travel.ettoday.net/article/3042487.htm | Single source - flagged |
| 76 | 2025 (文博會 tie-in) | 2025 | 台北南港老爺行旅 Hotel Royal-Nangang | 臺灣印事 & 腋毛人 Yemao (台灣插畫家) | INDEPENDENT | Taiwan illustrator IPs, creator-owned, surfaced via 台灣文博會 | yes | Hotel (主題房 + 明信片/小物) | https://travel.ettoday.net/article/3042487.htm | REP=yes: individual TW illustrators, open collabs; single source - flagged; the only indie hotel row |
| 77 | 2025-10-16.. | 2025 | 85度C | 吉伊卡哇 Chiikawa | PORTFOLIO | Publisher/committee-managed | - | Food (3款蛋糕 + 樂扣杯) | https://www.85cafe.com/News_content.php?data=9223 | Official 85cafe news page |
| 78 | 2025-12 | 2025 | 屈臣氏 Watsons Taiwan | 吉伊卡哇 Chiikawa | PORTFOLIO | Publisher/committee-managed | - | Drugstore (加價購3款) | https://fashion.ettoday.net/news/3079308 | |
| 79 | 2025-12 | 2025 | 7-ELEVEN Taiwan | 米飛 Miffy (白色系, 86款) | PORTFOLIO | **RECLASSIFIED v2 (was INDEPENDENT):** owned by Mercis bv, the Bruna-family estate company, creator Dick Bruna deceased (d.2017) - PORTFOLIO per the estate pinned rule (portfolio even as a single iconic character) | - | 集點/周邊 program (86款) | https://woman.udn.com/woman/story/123164/9179195 | The headline v1->v2 bucket change; see Reclassification delta |
| 80 | 2026-03-23.. | 2026YTD | 星巴克 Starbucks Taiwan | 哈利波特 Harry Potter | PORTFOLIO | Warner Bros. | - | Coffee chain (限定飲品 + 杯款/徽章) | https://istyle.ltn.com.tw/article/39395 | First TW Starbucks co-branded drink |
| 81 | 2026-07-04..22 | 2026YTD | 味全龍 WeiChuan Dragons | hololive production (JP+EN) | PORTFOLIO | Cover Corp | - | Sports event (4場主題日) | https://www.gvm.com.tw/article/131331 | Also gnn 306603; 2nd consecutive year |
| 82 | 2026-07-13.. | 2026YTD | GU Taiwan | 三麗鷗 曬黑系列 (9款) | PORTFOLIO | Sanrio | - | Apparel (T恤/家居服) | https://fashion.ettoday.net/news/3197344 | |
| 83 | 2026-07..08 | 2026YTD | 台北遠東香格里拉 Shangri-La Far Eastern | 美樂蒂 & 雙星仙子 | PORTFOLIO | Sanrio | - | Hotel (主題房 + 5款周邊) | https://supertaste.tvbs.com.tw/travel/359718 | Also nextapple 2026-07-08 |
| 84 | 2024-12-13.. | 2024 | GU Taiwan | 葬送的芙莉蓮 Frieren | PORTFOLIO | Shogakukan/committee-managed anime IP | - | Apparel (台日同步) | https://www.4gamers.com.tw/news/detail/68866/gu-taiwan-frieren-collab-release-date | |
| 85 | 2024-11-27..2025-01-07 | 2024 | 全家 FamilyMart Let's Café | 原神 Genshin Impact | PORTFOLIO | HoYoverse/miHoYo, major game conglomerate | - | Convenience-store coffee (杯身 + 虛寶) | https://gnn.gamer.com.tw/detail.php?sn=277192 | Distinct from 2025 全家 x 原神 (row 49) |
| 86 | 2024-11-08..12-26 | 2024 | 康是美 Cosmed | 史努比 Snoopy (Peanuts) | PORTFOLIO | Peanuts consortium (Sony controlling stake) | - | Drugstore (19款集點/加購 + 收納包) | https://supertaste.tvbs.com.tw/accessories/352004 | |
| 87 | 2024 (Sanrio 彩妝波) | 2024 | Amuse (Korean beauty, TW retail) | Hello Kitty | PORTFOLIO | Sanrio | - | Cosmetics (氣墊/唇露/眼影盤) | https://fashion.ettoday.net/news/2815157 | Single roundup source - flagged |
| 88 | 2024 (Sanrio 彩妝波) | 2024 | neuve (蜜粉品牌) | 酷洛米 Kuromi | PORTFOLIO | Sanrio | - | Cosmetics (蜜粉限定包裝) | https://fashion.ettoday.net/news/2815157 | Single roundup source - flagged |
| 89 | 2025-02-01.. | 2025 | INNISFREE Taiwan | 美樂蒂 My Melody (25/50週年) | PORTFOLIO | Sanrio | - | Cosmetics (3款限定 + 收納包) | https://www.cosme.net.tw/beautynews/28099 | 全台限量 |
| 90 | 2025 (beauty roundup) | 2025 | INNISFREE Taiwan | Brunch Brother 早餐兄弟 | UNCLEAR | Korean character brand; ownership/parent not established under queries run | - | Cosmetics (滿額分級贈周邊) | https://cava.tw/beauty/skincare/260843 | Single roundup source; class unresolved |
| 91 | 2025 (spring) | 2025 | 專科 Senka (Shiseido) | BT21 | PORTFOLIO | BT21 owned/managed by IPX (LINE FRIENDS); platform-owned per pinned rule | - | Cosmetics (4款洗面乳角色包裝) | https://www.marieclaire.com.tw/beauty/news/84300 | Single roundup source - flagged |
| 92 | 2025-01 | 2025 | CeraVe 適樂膚 (L'Oréal) | 馬來貘 LAIMO | INDEPENDENT | Taiwan illustrator IP by Cherng (陳信宇), creator-owned, no conglomerate parent | yes | Skincare (保濕限定組 + 周邊; 多通路) | https://www.marieclaire.com.tw/beauty/news/84300 | REP=yes: individual illustrator, historically very open ad-hoc collabs; big-brand x TW indie |
| 93 | 2025 (spring) | 2025 | 屈臣氏 Watsons Taiwan | 小白 Shiro (蠟筆小新) | PORTFOLIO | Futabasha-managed | - | Drugstore-exclusive beauty (粉撲 + 狗碗) | https://www.marieclaire.com.tw/beauty/news/84300 | Watsons TW exclusive; single roundup - flagged |
| 94 | 2025 (..12-31) | 2025 | BOBBI BROWN Taiwan (Estée Lauder) | 愛麗絲夢遊仙境 Alice in Wonderland | PORTFOLIO | Disney | - | Cosmetics (8色眼影盤) | https://cava.tw/beauty/skincare/260843 | Single roundup source - flagged |
| 95 | 2025 (Oct..Mar) | 2025 | ampm | Care Bears 彩虹熊 | PORTFOLIO | Cloudco Entertainment, major US licensor | - | Cosmetics (5色原液) | https://cava.tw/beauty/skincare/260843 | Single roundup source - flagged |
| 96 | 2025 (beauty roundup) | 2025 | 雪花秀 Sulwhasoo (AmorePacific) | ZERO PER ZERO | INDEPENDENT | Korean independent design studio (creator-owned duo), no conglomerate parent | yes | Skincare (台灣獨家 illustrated 系列) | https://cava.tw/beauty/skincare/260843 | REP=yes: small indie design studio, open collabs; TW-exclusive; single roundup - flagged |
| 97 | 2025 (beauty roundup) | 2025 | CLIO Taiwan | 哈利波特 Harry Potter | PORTFOLIO | Warner Bros. | - | Cosmetics (眼影盤 + 氣墊) | https://cava.tw/beauty/skincare/260843 | Single roundup source - flagged |
| 98 | 2025 (beauty roundup) | 2025 | ORBIS Taiwan | 三麗鷗 (大耳狗/布丁狗/帕恰狗) | PORTFOLIO | Sanrio | - | Hair care (character bottles) | https://cava.tw/beauty/skincare/260843 | Single roundup source - flagged |
| 99 | 2025 (beauty roundup) | 2025 | uka Taiwan | 寶可夢 Pokemon | PORTFOLIO | The Pokemon Company / Nintendo | - | Beauty tool (頭皮按摩刷 角色款) | https://cava.tw/beauty/skincare/260843 | Single roundup source - flagged |
| 100 | 2025-02-21..06-08 | 2025 | 誠品 R79 中山地下書街 | 飛天小女警 The Powerpuff Girls | PORTFOLIO | Warner Bros. Discovery / Cartoon Network | - | Bookstore pop-up (百款周邊) | https://www.4gamers.com.tw/news/detail/70147/thepowerpuffgirls-pop-up-store-taipei-2025 | Also meet.eslite, gnn 280792; venue-hosted pop-up |
| 101 | 2026-05-06.. | 2026YTD | 迷客夏 Milksha | MIND.A.DAY / CoverCat 跩跩貓 | INDEPENDENT | Korean original creator-owned IP (designer's own cat), no conglomerate parent | yes | Drink (荔枝系列) + 5款周邊加購 | https://www.milksha.com/news_detail.php?Key=394&cID=2 | REP=yes: creator-owned Korean indie, open collabs; also travel.ettoday 3159824 |
| 102 | 2024-06-19.. | 2024 | 珍煮丹 Truedan | matsui (日本插畫家, 療癒狗狗) | INDEPENDENT | Self-represented Japanese indie illustrator; no studio/conglomerate parent | yes | Drink (西瓜飲系列 collab cups) | https://www.foodnext.net/life/recipes/dessert/paper/5234961509 | REP=yes: self-representing individual illustrator; single roundup - flagged; 2nd matsui wave |
| 103 | 2024-07-16..10-31 | 2024 | 鮮茶道 Presotea | 寶可夢 Pokemon | PORTFOLIO | The Pokemon Company / Nintendo | - | Drink (5款 + 杯身/周邊) + 主題店 | https://travel.udn.com/travel/story/7186/8098200 | Theme store at 台北站前 |
| 104 | 2024-08-04.. | 2024 | 鶴茶樓 Hechalou | 伊藤潤二 Junji Ito | PORTFOLIO | Publisher-managed horror-manga IP (Shogakukan/Asahi Sonorama; TW via 木棉花國際 Muse) | - | Drink (4款杯 + 8款周邊) | https://travel.udn.com/travel/story/7186/8135590 | First wave; distinct from row 105 |
| 105 | 2025-08-23..09-21 | 2025 | 鶴茶樓 Hechalou | 伊藤潤二-狂熱 Junji Ito (2nd wave) | PORTFOLIO | Same as row 104 (licensed via 木棉花國際) | - | Drink (變色杯 + 6款周邊) | https://travel.ettoday.net/article/3015994.htm | Sequel campaign |
| 106 | 2024-11-14..11-20 | 2024 | 康青龍 Kang Qing Long | 蛋仔派對 Eggy Party | PORTFOLIO | Mass-market mobile game published by NetEase, a major conglomerate | - | Drink (3款杯 + 虛寶卡) | https://travel.ettoday.net/article/2854652.htm | Also udn 8362065; GNN source 403 |
| 107 | 2024-01-17 (第二彈) | 2024 | 五桐號 WooTea | Dinotaeng (Quokka & BoBo) | INDEPENDENT | Korean creator-owned indie illustrator brand, no conglomerate parent | yes | Drink (聯名禮盒 + 周邊) | https://travel.udn.com/travel/story/7186/7715318 | REP=yes: creator-owned studio, open collabs; single strong source - flagged |
| 108 | 2024-01-24 (launch) | 2024 | 出發吧麥芬 Go Go Muffin (mobile RPG, TW) | 貓貓蟲咖波 Bugcat Capoo | INDEPENDENT | Same as row 1 | no | Gaming (launch collab event) | https://gnn.gamer.com.tw/detail.php?sn=261446 | REP=no (Carter Island); inside window |
| 109 | 2024-08-27..09-26 | 2024 | 寶可夢台灣官方 LINE 帳號 | 寶可夢 Pokemon (咖波-style 貼圖) | PORTFOLIO | The Pokemon Company is the co-branding brand; featured IP is Pokemon | - | Digital platform (LINE free sticker) | https://gnn.gamer.com.tw/detail.php?sn=272980 | Borderline scope (free-sticker promo) |
| 110 | 2025-07-02.. | 2025 | 風之國度 Wind Kingdom (傳奇網路, TW) | 三麗鷗 美樂蒂與酷洛米 | PORTFOLIO | Sanrio | - | Gaming (skins, bond quests) | https://gnn.gamer.com.tw/detail.php?sn=288179 | Melody 50th / Kuromi 20th |
| 111 | 2025-12-24.. | 2025 | Garena 傳說對決 AOV (TW) | 三麗鷗家族 | PORTFOLIO | Sanrio | - | Gaming (free skin via tasks) | https://www.4gamers.com.tw/news/detail/76052/aov-sanrio-characters-collab-in-game | AOV's first Sanrio crossover |
| 112 | 2026-03-10..04-07 | 2026YTD | 咻咻史萊姆 Pew Pew Slime (傳奇網路, TW) | 貓貓蟲咖波 Bugcat Capoo | INDEPENDENT | Same as row 1 | no | Gaming (launch collab: skins/partners) | https://gnn.gamer.com.tw/detail.php?sn=301523 | REP=no (Carter Island) |
| 113 | 2026-07-17.. | 2026YTD | 心動小鎮 Heartopia (life-sim, TW) | 三麗鷗家族 | PORTFOLIO | Sanrio | - | Gaming (outfits, furniture) | https://gnn.gamer.com.tw/detail.php?sn=308353 | Inside window edge |
| 114 | 2025-12-12..2026-02-22 | 2025 | 中國信託金融園區 CTBC (南港) | 貓貓蟲咖波 Bugcat Capoo | INDEPENDENT | Same as row 1 | no | Public event (免費戶外溜冰場「咖波冰原大冒險」+ 集章) | https://travel.udn.com/travel/story/7205/9198471 | REP=no (Carter Island); landmark corporate public-event co-brand |
| 115 | 2026-04-02..08-31 | 2026YTD | 台北101 89F 觀景台 | 星期一的布魯斯 Monday Bruce | INDEPENDENT | Taiwan 人氣原創插畫IP (source: 推廣台灣原創IP), creator-owned, no conglomerate parent | yes | Public event (雲端特展 + 快閃專櫃) | https://udn.com/news/story/7241/9419978 | REP=yes: creator-owned TW original IP, open collabs; also gnn 302899; indie IP wins a flagship landmark |
| 116 | 2025-12-15..2026-01-25 | 2025 | 統一時代百貨 Dream Plaza 台北 5F | 勾卡 KKOTKA (quokka) | INDEPENDENT | Korean studio YOUNG FOREST, small-studio-owned, no conglomerate parent | yes | Dept-store pop-up (first TW stop) | https://www.techbang.com/posts/126849-kkotka-pop-up-store-taiwan | REP=yes: small Korean studio, open collabs; KKOTKA's first TW stop |
| 117 | 2026-04-02..05-03 | 2026YTD | 新光三越 A11 B1F | 勾卡 KKOTKA | INDEPENDENT | Same as row 116 (YOUNG FOREST studio) | yes | Dept-store pop-up (~50 新品) | https://www.winnews.com.tw/263387 | REP=yes; also gnn 302448; KKOTKA's second TW stop |
| 118 | 2026-04-01..06-28 | 2026YTD | 駁二藝術特區 C5倉庫 (Kaohsiung Pier-2) | 露咖貓 LOOKA CAT | INDEPENDENT | Taiwan 原創品牌 (露咖貓工作室 lookacat.com), creator-owned | yes | Public arts-venue pop-up (免費入場) | https://pier2.org/exhibition/info/1857 | REP=yes: creator-owned TW studio, open collabs; official venue page |
| 119 | 2024-12-28..2025-04-06 | 2024 | 松山文創園區 5號倉庫 | 蠟筆小新 Crayon Shin-chan (電影大冒險) | PORTFOLIO | Committee-managed (Shin-Ei / Futabasha) | - | Culture-park pop-up (200+ 周邊) | https://www.songshanculturalpark.org/exhibition/activity/a8f6349b-93ce-480f-b26b-7671011d85e6 | Also walkerland 408934; venue-hosted pop-up |
| 120 | 2025-05-09 | 2025 | Decathlon 迪卡儂 Taiwan | 俵谷哲典 Tetsunori Tawaraya | INDEPENDENT | Independent Japanese singer/illustrator with a self-owned art universe (prior indie collabs: BEAMS, Volcom, Brain Dead); no conglomerate parent | yes | Apparel + hats/bags + 2款改造球鞋 | https://www.kiks.com.tw/post/首次發表全新運動生活風格系列！迪卡儂-decathlon-攜手日本藝術家俵谷哲典 | REP=yes: individual artist, open ad-hoc collabs; Decathlon TW's first-ever crossover |
| 121 | 2026-04-24 | 2026YTD | GU Taiwan | JOJO的奇妙冒險 JoJo's Bizarre Adventure | PORTFOLIO | Major manga franchise, Hirohiko Araki / Shueisha | - | Apparel (UT印花Tee + 襯衫) | https://www.cool-style.com.tw/wd2/archives/1291111 | Also gnn 303467; first GU x JOJO |
| 122 | 2025-03-31 / ~04-03 | 2025 | UNIQLO Taiwan | 貓福珊迪 mofusand (麵包貓 UT) | INDEPENDENT | Created by individual illustrator ぢゅの (Juno), creator-owned; distinct from row 19 (Sanrio-paired) | no | Apparel (UT graphic tees) | https://www.uniqlo.com/tw/news/topics/2025033101/ | REP=no: exclusively managed by Gray Parka Service (per Japan run rows 22/85); now large but creator-owned |
| 123 | 2024-01-19 / 01-22 | 2024 | PAZZO (apparel) | 史努比 SNOOPY / Peanuts | PORTFOLIO | Peanuts Worldwide (Sony controlling stake) | - | Apparel + accessories | https://today.line.me/tw/v3/article/wJG89wl | Discrete dated drop |
| 124 | 2025-01-13 | 2025 | PAZZO (apparel) | Care Bears 彩虹小熊 | PORTFOLIO | Cloudco Entertainment | - | Apparel + plush/socks/mug | https://www.marieclaire.com.tw/fashion/news/83987/pazzo | First PAZZO x Care Bears |
| 125 | 2024-01 | 2024 | CACO (apparel) | 三麗鷗 大耳狗 Cinnamoroll (+others) | PORTFOLIO | Sanrio | - | Apparel (造型外套) + hats/bags | https://today.line.me/tw/v3/article/wJG89wl | Store-opening-tied; single roundup - flagged |
| 126 | 2024-12-04..2025-02-06 | 2024 | 誠品 R79 中山地下書街 | 貓福珊迪 mofusand | INDEPENDENT | Created by solo illustrator ぢゅの (Juno), no conglomerate parent (mofusand solo; cf. row 19) | no | Bookstore pop-up (~30 新品) | https://universe.oneone.com.tw/posts/1621 | REP=no (Gray Parka Service exclusive, per Japan run); venue-hosted pop-up |
| 127 | 2025-07-10..07-28 | 2025 | 誠品書店 / 誠品生活新店 (文具展) | unpis | INDEPENDENT | unpis is an individual Japanese illustrator (studio Unpict), acted as visual director; no conglomerate owner | yes | Stationery-expo co-branding (20+ 獨家聯名) | https://www.wowlavie.com/article/250025915 | REP=yes: individual illustrator, open collabs |
| 128 | 2025-04-10 / 04-17 | 2025 | MINISO 名創優品 Taiwan | 吉伊卡哇 Chiikawa | PORTFOLIO | Publisher/committee-managed | - | Lifestyle retail (櫻花季系列) | https://universe.oneone.com.tw/posts/2683 | TW-market article (oneone/維肯娛樂) |
| 129 | 2026-07-09..08-05 | 2026YTD | HOLA 和樂家居 | 哆啦A夢 Doraemon / 哆啦美 | PORTFOLIO | Fujiko Pro / Shogakukan-Shueisha | - | Homeware (玩偶/抱枕/餐具) | https://chinesedora.com/news/107045.htm | HOLA's first Doraemon 聯名; within window |

## Reclassification delta (v1 -> v2)

Re-scoring all 129 rows against the updated ownership test + pinned edge cases moved exactly **three** rows.
No other row changed bucket - the v1 calls held up under the stricter definition.

| Row | IP | v1 class | v2 class | Reason |
|---|---|---|---|---|
| 79 | 米飛 Miffy | INDEPENDENT | **PORTFOLIO** | Estate pinned rule: Mercis bv is the Bruna-family estate company, creator Dick Bruna deceased (2017); portfolio even as a single iconic character (Miffy is the pinned example). |
| 35 | OSAMU GOODS 原田治 | UNCLEAR | **PORTFOLIO** | Deceased-creator/estate pinned rule: Osamu Harada died 2016; OSAMU GOODS is now an estate/heritage-brand goods property, resolved from UNCLEAR to portfolio under the Miffy-style rule. |
| 65 | 草間彌生 Yayoi Kusama | UNCLEAR | **INDEPENDENT** | Japan-run fine-artist precedent: living artists who own their own work (Higuchi, Nagaba, Murakami) classify INDEPENDENT; Kusama owns her artwork, no conglomerate parent. REP=no (locked to exclusive gallery/own-studio representation). Scope caveat (exhibition-tie-in cups) retained. |

**Net effect on the split:**

| Class | v1 count | v2 count | Delta |
|---|---|---|---|
| PORTFOLIO | 87 | 89 | +2 (Miffy in, OSAMU in) |
| INDEPENDENT | 35 | 35 | 0 (Miffy out, Kusama in - they cancel) |
| UNCLEAR | 7 | 5 | -2 (OSAMU out, Kusama out) |
| **Total** | **129** | **129** | 0 |

**Headline:** the indie share is **unchanged at 35/129 = 27.1%**.
The stricter definition and pinned edge cases move individual rows (one indie out, one indie in) but the indie count is identical - the ~27% Taiwan indie share is robust to the tighter rules, not an artifact of loose classification.
What the edge cases actually tightened was the UNCLEAR bucket (7 -> 5): two genuinely-borderline rows resolved into portfolio (OSAMU estate) and independent (Kusama fine-artist).

## Running counts (v2)

- Total rows: 129
- PORTFOLIO: 89  |  INDEPENDENT: 35  |  UNCLEAR: 5
- 2024: 37 rows (9 indie, 27 portfolio, 1 unclear) - indie 24.3% (v1: 8 indie / 21.6%; Kusama row 65 moved unclear->indie)
- 2025: 60 rows (18 indie, 41 portfolio, 1 unclear) - indie 30.0% (v1: 19 indie / 31.7%; Miffy row 79 moved indie->portfolio)
- 2026YTD: 32 rows (8 indie, 21 portfolio, 3 unclear) - indie 25.0% (v1: 8 indie / 25.0%; OSAMU row 35 moved unclear->portfolio)

(No government/public-body-OWNED IP appears in Taiwan - every IP here is privately owned, even where the *brand* is a public body (rows 17, 32, 39). Nothing is excluded from the split, unlike Korea's Seoul-Haechi/Daejeon rows.)

**REPRESENTABLE tally (INDEPENDENT rows only, n=35):**

- yes: 15 (28, 33, 52, 76, 92, 96, 101, 102, 107, 115, 116, 117, 118, 120, 127)
- no: 17 (1, 4, 5, 18, 21, 29, 32, 39, 51, 53, 65, 68, 108, 112, 114, 122, 126)
- unclear: 3 (17, 31, 43)

## Excluded (logged so we do not re-add - carried from v1)

- 得正 x fwee - Korean cosmetics brand, no character IP (brand-x-brand). Source: cava.tw/265108.
- Mr.WISH x SOU・SOU - Japanese textile label, no character IP (brand-x-brand). Source: cava.tw/263159.
- 全家 蛇年福袋 (Chiikawa/Sanrio/柯南 multi-IP 福袋, Dec 2024) - licensed-goods lucky bag, closer to retail licensing. Source: oneone 1737.
- COMEBUY x 可樂果 - snack-brand mascot, brand-x-brand. Source: playing.ltn/32370.
- LuLu the Piggy x 貓貓蟲咖波 (2026-06 joint line) - IP-x-IP (two indie TW IPs), not brand-x-IP; noted in _VERDICT §3 as indie-prominence evidence. Sources: cava.tw/265108, gnn 304779.
- 咖波小浪漫快閃店 (2026-06-05) - IP owner's own-brand pop-up, not an outside co-brand. Source: carterislandtw.com.
- 全聯 x 哆啦A夢 (from 2023-10-06) - outside window. Source: chinesedora.com/56336.
- 全家 x 吉伊卡哇公仔 (2025) - only source (beauty321/66468) returned 403; phantom-entry guard.
- BOUYIEE x 醜白兔 - category page carries no campaign date.
- 日本麥當勞 x 吉伊卡哇 / x 寶可夢 (2025) - Japan-market, out of scope.
- 味全龍 x 白爛貓, DEVILCASE x 白爛貓, HOYACASA x 黃阿瑪 - shop/listing pages only, no dates established.
- 大陸麥當勞 x 蠟筆小新 (2025-06) - China-market, out of scope.
- 咖波 x 屌面人 (2026-01) - IP-x-IP and cancelled after backlash.
- 麥當勞 x 可口可樂 撲克牌 (2025-10) - brand-x-brand premium, no character IP.
- 必勝客 x 屋馬 (2025-09) - restaurant-x-restaurant, no character IP.
- 台灣高鐵 x 卡娜赫拉 - official page is a JS shell, no dates via curl.
- 清心福全 x 咖波 書籤 2nd wave - source returns 406; row 1 covers the 2024 pairing.
- 摩斯漢堡 MOS Friends x 超級瑪利歐 - no MOS-specific dated source.
- 味全龍 x 白爛貓 主題日 - dates to 2023-06, outside window.
- 星巴克 x 史努比 2024-10 Asia wave - TW availability unconfirmed; TW-confirmed waves are 2025 (row 70).
- 合作金庫 x 卡娜赫拉 聯名卡 - card pages carry no launch date.
- 吉伊卡哇 x 三麗鷗 聯名系列 (2025-12) - IP-x-IP pairing.
- 誠品生活南西 x 塔麻可吉 Tamagotchi (2024-10) - only source Cloudflare-protected; phantom-entry guard.
- Crocs TW x 哆啦A夢, Onitsuka Tiger x 原子小金剛 - no clean TW-market launch date.
- HOLA x 三麗鷗 / x 迪士尼 奇奇蒂蒂 - resolved to 2023/2020, outside window.
- POYA 寶雅 x 三麗鷗 - 2021 story, outside window.
- 鶴茶樓 x SHOP1107 (2023), 茶湯會 x 馬來貘 (2022) - pre-2024, outside window.
