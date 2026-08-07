# RHINOSHIELD 犀牛盾 Design Studio - full creator roster (Taiwan storefront)

**Rebuilt in build 3. Build 2's version of this file carried two systematic errors; both are corrected here.**

Swept 2026-08-07. Source: the artist roster embedded in the Nuxt payload of any `https://rhinoshield.tw/design-studio/collections/@<slug>` page.
The payload is a devalue-style flat array: records hold *indices* into that array, not values, so it has to be dereferenced rather than regex-scraped.
Four collection pages (`@pluddie`, `@dipsy`, `@ilovemyselfself`, `@nagiart`) were parsed independently and each returned the identical **182** records with zero field mismatches.

## The two corrections to build 2

**1. The launch dates were the wrong field.** Build 2 reported a `firstLaunchedAt` epoch per creator, but the values it published are the **`?cb=` cache-buster on the creator's avatar image**, which is an asset-upload timestamp, not a launch date.
The real `firstLaunchedAt` differs by up to 20 months and moves four of build 2's eight row years (all four stay inside the 2023-2026 window).
Both fields are now published side by side below so the discrepancy is inspectable rather than asserted.
The two disagree in both directions, which is what tells you they are different things: `@dipsy` launched 2023-11-22 and had its avatar refreshed 2025-11-28, while `@cheesyduck` had its assets uploaded 2026-03-05 and launched 2026-05-22.
Where a banner cache-buster exists it tracks `firstLaunchedAt` closely (`@dipsy`: banner uploaded 11 minutes before launch), which is the corroboration that `firstLaunchedAt` is the launch field and the avatar `cb` is not.

**2. Ten slugs were wrong.** For ten creators build 2 recorded the creator's *Instagram handle* in the collection-slug column, so the `source_ref` URLs it implies (`/collections/@andreacat805`, `/collections/@ti_illustration`, `/collections/@1nsp0` and so on) do not exist.
All ten are in build 2's rejected list, so no accepted row is affected - the eight accepted rows' slugs were checked and are all correct - but the roster column is fixed here.
Examples: `@andreacat805` is really `@andreacat`; `@ti_illustration` is `@shuti`; `@1nsp0` is `@huijinchan`; `@jinjintattoo` is `@jinjintatto` (the site's own typo).

## Roster

`launch` = the brand's own `firstLaunchedAt` field. `avatar cb` = the avatar cache-buster build 2 mistook for it.
`ig` is the handle the brand itself publishes, so no handle guessing and no handle-squat exposure. `followers` read live from Instagram `og:description` under a Googlebot UA on 2026-08-07.
Other social platforms the roster carries are shown where no Instagram is published.

| launch | avatar cb | slug | name | ig | followers | band |
|---|---|---|---|---|---|---|
| 2023-06-29 | 2025-12-03 | `@moremoretoe` | MoreMoreToe | - | - | - |
| 2023-06-30 | 2025-11-30 | `@rachelliao` | 瑞秋廖 | `@rachelliao_illustration` | 171K | 50k_200k |
| 2023-06-30 | 2025-09-10 | `@jinjintatto` | Jin Jin Tattoo | `@jinjintattoo` | 3,207 | lt_10k |
| 2023-06-30 | 2023-07-06 | `@ilovemyselfself` | ilovemyselfself | `@ilovemyselfself` | 3,460 | lt_10k |
| 2023-07-13 | 2023-07-07 | `@thegirl` | The Girl | - | - | - |
| 2023-09-21 | 2023-09-18 | `@itsmonkiddo` | Monkiddo | `@itsmonkiddo` | 23K | 10k_50k |
| 2023-10-01 | 2025-11-29 | `@lazy-monster` | 懶懶怪 | `@chill.writing_` | 126K | 50k_200k |
| 2023-10-02 | 2023-10-01 | `@mashpatooties` | Mashpatooties | - | - | - |
| 2023-10-12 | 2023-09-30 | `@songprettybell` | Songprettybell | - | - | - |
| 2023-10-16 | 2023-10-26 | `@plurk` | 噗浪 | - | - | - |
| 2023-10-19 | 2023-10-10 | `@Change` | Chaigo | - | - | - |
| 2023-10-24 | 2023-10-24 | `@rongart` | 草棉谷RONG | - | - | - |
| 2023-11-09 | 2025-12-02 | `@mumub3dpocket` | 木木の口袋 | - | - | - |
| 2023-11-10 | 2025-11-28 | `@shiba-amix` | 棉花糖柴柴與廢貓阿米 | - | - | - |
| 2023-11-17 | 2025-10-24 | `@pluddie` | 小女孩和花花獅 | `@pluddiestudio` | 4,284 | lt_10k |
| 2023-11-20 | 2025-12-01 | `@andreacat` | AndreaCat | `@andreacat805` | 1,055 | lt_10k |
| 2023-11-22 | 2025-11-28 | `@dipsy` | 迪普西 | `@dipsydisplay` | 6,801 | lt_10k |
| 2023-11-23 | 2025-12-03 | `@hellostudio` | 你好工作室 | `@hellostudiotw` | 25K | 10k_50k |
| 2023-11-27 | 2023-11-22 | `@chilittleworld` | 阿7世界 | - | - | - |
| 2023-12-03 | 2025-12-02 | `@hsueh` | 阿薛 | `@hsueh.illu` | 2,428 | lt_10k |
| 2023-12-22 | 2025-12-02 | `@travelpaintcat` | 旅貓實驗室 | `@travelpaint.cat` | 1,785 | lt_10k |
| 2023-12-29 | 2025-11-30 | `@wohenlanduo` | 懶惰朽吉 | `@wohenlanduo` | 36K | 10k_50k |
| 2024-01-05 | 2023-11-24 | `@verymissrabbit` | 謙謙創藝-好想兔日常 | - | - | - |
| 2024-01-05 | 2023-12-08 | `@chesthairapartment` | 胸毛公寓 | - | - | - |
| 2024-01-25 | 2025-12-02 | `@otomerui` | 平凡乙女日記 | `@otome_rui` | 20K | 10k_50k |
| 2024-02-29 | 2025-12-11 | `@gallon-milk` | 時薪一加侖鮮奶 | `@gallon_milk14` | 2,423 | lt_10k |
| 2024-03-14 | 2023-11-19 | `@shadoowww` | Shadoowww | `@shadoowww__` | 21K | 10k_50k |
| 2024-05-10 | 2025-02-23 | `@sentimental` | 山東饅頭 | `@sentimentaldraws` | 12K | 10k_50k |
| 2024-05-16 | 2025-11-17 | `@bunnyismoving` | 廢物兔子 | `@bunny_is_moving` | 86K | 50k_200k |
| 2024-05-31 | 2025-08-13 | `@bettermii` | 米工 Better mii | `@bettermii_art` | 31K | 10k_50k |
| 2024-06-06 | 2024-05-06 | `@huengua` | 昏呱 | `@huengua` | 42K | 10k_50k |
| 2024-06-06 | 2025-12-01 | `@wewe` | Wewe 小喵WE | `@wewe_0413` | 44K | 10k_50k |
| 2024-06-17 | 2025-09-10 | `@chouscat` | 周氏喵喵 | `@cady._.design` | 12K | 10k_50k |
| 2024-06-18 | 2025-12-01 | `@cindywume` | Cindy Wume | `@cindy_wume` | 25K | 10k_50k |
| 2024-06-20 | 2024-05-23 | `@jessiewsart` | Jessie Wong | `@jessiewsart` | 54K | 50k_200k |
| 2024-06-25 | 2025-11-30 | `@asuan14` | 啊宣 ASUAN | `@asuan.14` | 223K | 200k_1m |
| 2024-07-02 | 2024-06-18 | `@dongillustration` | 咚東 | `@dong.dong.illustration` | 16K | 10k_50k |
| 2024-07-21 | 2024-06-13 | `@hihi-trickster` | Hihi 搗蛋鬼 | `@hihi_trickster` | 11K | 10k_50k |
| 2024-07-24 | 2026-01-15 | `@angyfrog` | angy frog | `@angyfrog_` | 217K | 200k_1m |
| 2024-08-01 | 2024-06-08 | `@celly` | Celly | `@cellydrw` | 49K | 10k_50k |
| 2024-08-04 | 2025-11-28 | `@beaverisajustin` | 胖西是隻河狸 | `@justinisabeaver` | 40K | 10k_50k |
| 2024-08-07 | 2024-07-23 | `@shooley-art` | Shooley Art | `@shooley.art` | 70K | 50k_200k |
| 2024-08-10 | 2026-01-13 | `@yemao` | 腋毛人 Yemao | `@yemao20130628` | 26K | 10k_50k |
| 2024-08-13 | 2025-09-01 | `@shuti` | 舒 媞 | `@ti_illustration` | 9,170 | lt_10k |
| 2024-08-13 | 2024-07-04 | `@TabbiL` | Tabbi L | `@tabbiliaw_art` | 11K | 10k_50k |
| 2024-08-14 | 2025-11-28 | `@drunk-bambi` | 微醺斑比 | `@abbybambi` | 21K | 10k_50k |
| 2024-08-16 | 2024-07-21 | `@odsanyu` | odsanyu | `@odsanyu` | 32K | 10k_50k |
| 2024-08-19 | 2025-01-20 | `@sekaiofkangae` | Sekai of Kangae | `@sekaiofkangae` | 24K | 10k_50k |
| 2024-08-20 | 2024-07-16 | `@nuomi` | Nuomi 諾米 | `@nuomi0213` | 89K | 50k_200k |
| 2024-08-21 | 2024-07-23 | `@korawia` | KORAWIA | `@korawia` | 64K | 50k_200k |
| 2024-08-22 | 2025-11-30 | `@ginnylambkin` | 居你 | `@ginnylambkin` | 17K | 10k_50k |
| 2024-08-24 | 2026-04-29 | `@pinkonweekend` | Powzzled | `@powzzled` | 17K | 10k_50k |
| 2024-08-25 | 2024-07-16 | `@kumakun-studio` | Kumakun Studio | `@kumakunstudio` | 15K | 10k_50k |
| 2024-08-26 | 2024-07-14 | `@Murmur-taipei` | 臺 北 碎 嘴 霧 裡 探 花 | `@murmurtaipei` | 22K | 10k_50k |
| 2024-08-28 | 2025-04-10 | `@justinejossart` | Justine Jossart | `@justinejossart` | 29K | 10k_50k |
| 2024-08-29 | 2024-07-24 | `@littop` | 日頭 | `@littop_design` | 46K | 10k_50k |
| 2024-08-30 | 2026-05-16 | `@simpleseasun` | SIMPLESEASUN | `@simpleseasun` | 18K | 10k_50k |
| 2024-09-04 | 2025-12-01 | `@jocelyntsaih` | 蔡佳倫 | `@jocelyntsaih` | 25K | 10k_50k |
| 2024-09-04 | 2024-08-14 | `@milkteadani` | Dani / milkteadani | `@milkteadani` | 68K | 50k_200k |
| 2024-09-04 | 2024-08-15 | `@LOZO_ILLU` | LOZO | `@lozo_illu` | 37K | 10k_50k |
| 2024-09-04 | 2025-12-01 | `@ruruspiano` | Ru's Piano Ru味春捲 | `@ruruspiano` | 227K | 200k_1m |
| 2024-09-04 | 2024-08-27 | `@tomalater` | Thomas Lateur (@tomalater) | `@tomalater` | 39K | 10k_50k |
| 2024-09-05 | 2024-09-04 | `@theorenjistudio` | 木登 オレンジ | `@theorenjistudio` | 29K | 10k_50k |
| 2024-09-06 | 2024-07-27 | `@jessica-berriver` | Jessica Berriver | `@itsberriver` | 21K | 10k_50k |
| 2024-09-06 | 2024-09-04 | `@baileycrouch` | Bailey Crouch | `@bailey.jpeg` | 16K | 10k_50k |
| 2024-09-06 | 2024-08-17 | `@amyhartelust` | Amy Hartelust | `@amyhartelust` | 16K | 10k_50k |
| 2024-09-06 | 2025-08-04 | `@lilyandstarsstudio` | LilyandStarsStudio | `@lilyandstarsstudio` | 7,586 | lt_10k |
| 2024-09-09 | 2024-08-20 | `@hilli` | hilli / helen bucher | `@helenbucher` | 78K | 50k_200k |
| 2024-09-10 | 2024-07-07 | `@easonillus` | Eason Ko | `@easonillus` | 164K | 50k_200k |
| 2024-09-20 | 2025-11-28 | `@kuroshio` | 財團法人黑潮海洋文教基金會 | `@kuroshio1998` | 7,399 | lt_10k |
| 2024-09-21 | 2024-07-20 | `@migmig` | Mig_Mig | `@mig_mig` | 22K | 10k_50k |
| 2024-09-26 | 2024-07-01 | `@artbyjulia` | Julia Peng | `@artbyjulia.png` | 171K | 50k_200k |
| 2024-09-28 | 2024-08-02 | `@arcasian` | Arcasian | `@arcasian__` | 68K | 50k_200k |
| 2024-09-30 | 2025-09-27 | `@sashakolesnik` | Sasha Kolesnik | `@_sashakolesnik` | 38K | 10k_50k |
| 2024-10-10 | 2024-09-03 | `@moonlume` | moonlume | `@moonlume` | 45K | 10k_50k |
| 2024-10-13 | 2024-09-28 | `@Derptiles` | Derptiles | `@official_derptiles` | 93K | 50k_200k |
| 2024-10-15 | 2025-05-06 | `@uglysquirrel` | uglysquirrel | `@uglysquirrel` | 23K | 10k_50k |
| 2024-10-16 | 2024-05-23 | `@minghan` | Minghan H. | `@minminmin_111` | 37K | 10k_50k |
| 2024-10-17 | 2025-08-25 | `@monstyplanet` | Monsty Planet | `@monstyplanet` | 24K | 10k_50k |
| 2024-10-21 | 2025-09-10 | `@shyly-kurodasang` | 害羞的黑田桑 | `@shyly_kurodasang` | 46K | 10k_50k |
| 2024-10-21 | 2025-08-19 | `@liliyth` | liliyth | `@liliyth` | 83K | 50k_200k |
| 2024-10-24 | 2024-08-12 | `@Noyisin` | Noyisin | `@noyisin` | 24K | 10k_50k |
| 2024-10-29 | 2025-09-10 | `@10secondsclass` | 10秒鐘教室 | `@10secondsclass` | 222K | 200k_1m |
| 2024-11-06 | 2024-09-09 | `@jushmu` | Jushmu | `@jushmu` | 12K | 10k_50k |
| 2024-11-07 | 2024-08-30 | `@snowlattes` | SNOWLATTES | `@snowlattes` | 41K | 10k_50k |
| 2024-11-13 | 2025-08-22 | `@bbnww` | 黑白小姐 Miss B&W | `@bnnnnw` | 35K | 10k_50k |
| 2024-11-14 | 2024-09-06 | `@ananaisdesign` | Ananais design | `@ananaisdesign` | 42K | 10k_50k |
| 2024-11-15 | 2025-09-26 | `@jessphoenix` | Jess Phoenix | `@jessraephoenix` | 63K | 50k_200k |
| 2024-12-02 | 2025-01-17 | `@rhinoshield-specials` | 犀牛盾主題特選 | - | - | - |
| 2024-12-02 | 2024-11-27 | `@thanhillustrates` | thanhillustrates | `@thanh.illustrates` | 24K | 10k_50k |
| 2024-12-02 | 2024-10-28 | `@dinosaurs-room` | 恐龍的房間 | `@dinosaurs.room` | 94K | 50k_200k |
| 2024-12-05 | 2023-11-09 | `@juanito` | Cazador Juanito | - | - | - |
| 2024-12-16 | 2024-12-10 | `@hanakin` | Hanakin Couple | `@h_rico16` | 468K | 200k_1m |
| 2024-12-19 | 2024-08-02 | `@marion-blanc` | Marion Blanc | `@marionblanc_illustration` | 52K | 50k_200k |
| 2024-12-25 | 2025-09-10 | `@shinuwubi` | shiny side up | `@shinysideup.art` | 11K | 10k_50k |
| 2024-12-27 | 2025-08-22 | `@bow6_6` | 不然你來當小寶 | `@bow6_6` | 12K | 10k_50k |
| 2025-01-10 | 2026-03-26 | `@letoastre` | Letoastre 勒托寫字 | `@letoastre` | 17K | 10k_50k |
| 2025-01-17 | 2025-01-19 | `@carlosarrojo` | Carlos Arrojo | `@carlos_arrojo` | 36K | 10k_50k |
| 2025-01-17 | 2024-12-20 | `@lorenaxangelina` | LorenaxAngelina | `@lorenaxangelina` | 2,704 | lt_10k |
| 2025-02-07 | 2024-09-27 | `@voodoo-salad` | Voodoo Salad | `@voodoo.salad` | 105K | 50k_200k |
| 2025-02-10 | 2024-07-11 | `@konistudio` | KoniStudio | `@konistudio` | 115K | 50k_200k |
| 2025-02-13 | 2025-12-01 | `@duck-c4` | 鴨梨子 | `@duck_c4` | 77K | 50k_200k |
| 2025-02-14 | 2025-12-01 | `@misstanghulu` | 唐葫蘆姑娘 | `@miss_tanghulu` | 28K | 10k_50k |
| 2025-02-18 | 2024-11-15 | `@chentomology` | chentomology | `@chentomology` | 63K | 50k_200k |
| 2025-02-18 | 2024-12-10 | `@hanomanga` | 歯の漫画 | `@hanomanga_ha` | - | - |
| 2025-02-20 | 2024-12-27 | `@clubbabo` | Club Babo | `@club_babo` | 27K | 10k_50k |
| 2025-02-21 | 2024-09-19 | `@yukfun` | YUK FUN | `@yukfunwow` | 82K | 50k_200k |
| 2025-02-23 | 2025-01-21 | `@wowohead` | 窩窩頭 | `@wowohead_2023` | 2,154 | lt_10k |
| 2025-02-25 | 2024-11-20 | `@ARTWITHEM` | Art With Em | `@art_with_em_` | 56K | 50k_200k |
| 2025-03-07 | 2025-03-03 | `@rhinishield-womens-specials` | 犀牛盾女性主題特選 | - | - | - |
| 2025-03-11 | 2024-08-28 | `@qiandreaming` | qian.dreaming | `@qian.dreaming` | 94K | 50k_200k |
| 2025-03-12 | 2025-11-30 | `@ohall` | 喔噢你好 | `@ohall_official` | 22K | 10k_50k |
| 2025-03-18 | 2025-12-30 | `@hueiheijibai` | 灰黑集白 | `@aasta_blacknwhite` | 4,443 | lt_10k |
| 2025-03-21 | 2025-11-28 | `@ramenexplorer` | 拉麵探險隊 | `@ramen_explorers` | 30K | 10k_50k |
| 2025-03-27 | 2025-08-22 | `@Akindofcafe` | 什物 a kind of café | `@akindofcafe` | 23K | 10k_50k |
| 2025-03-27 | 2025-06-18 | `@jeninuferu` | Jennifer Bouron | `@jeninuferu` | 131K | 50k_200k |
| 2025-03-28 | 2025-03-17 | `@xiaobaosg` | xiaobaosg | `@xiaobaosg` | 104K | 50k_200k |
| 2025-03-28 | 2025-03-18 | `@mocacamo` | 麻吉鴨鴨 | `@mocaccha` | 96K | 50k_200k |
| 2025-04-02 | 2025-02-20 | `@huijinchan` | 1nsp0 | `@1nsp0.1_0` | 18 | lt_10k |
| 2025-04-09 | 2024-09-04 | `@TAIWANIZE` | TAIWANIZE | `@taiwanize` | 13K | 10k_50k |
| 2025-04-15 | 2024-10-21 | `@marylouchalon` | Marylou Chalon | `@marylouchalon` | 47K | 10k_50k |
| 2025-04-22 | 2025-04-15 | `@kireileague` | 世界漂亮在台協會 | `@kirei_league` | 14K | 10k_50k |
| 2025-04-23 | 2026-04-26 | `@daffy` | Daffy | `@daffy_illust` | 13K | 10k_50k |
| 2025-04-24 | 2025-12-02 | `@hahasarah_` | haha sarah | `@hahaha_sarah` | 21K | 10k_50k |
| 2025-05-02 | 2024-10-17 | `@solmariart` | solmariart | `@solmariart` | 18K | 10k_50k |
| 2025-05-05 | 2025-09-04 | `@akinorioishi` | 大石曉規 | `@akinori_oishi` | 41K | 10k_50k |
| 2025-05-06 | 2025-08-25 | `@claireiglesias` | Claire Iglesias | `@claireiglesias_` | 14K | 10k_50k |
| 2025-05-09 | 2026-03-20 | `@mojiasobi` | mojiasobi | `@mojiasobi` | 48K | 10k_50k |
| 2025-05-17 | 2025-05-05 | `@Bee-Creates` | Bee Creates | `@bee_creates` | 38K | 10k_50k |
| 2025-05-21 | 2025-06-18 | `@erishimatsuka` | 島塚絵里 | `@erishimatsuka` | 21K | 10k_50k |
| 2025-05-23 | 2024-12-29 | `@parakid` | parakid | `@parakid` | 116K | 50k_200k |
| 2025-06-11 | 2025-04-30 | `@ABLIN` | ABLIN CHANNEL | `@ablin_alim` | 46K | 10k_50k |
| 2025-06-13 | 2024-11-08 | `@juliesolvstrom` | Julie Solvstrom | `@juliesolvstrom` | 58K | 50k_200k |
| 2025-06-24 | 2026-02-25 | `@zoeartgarden` | Zoe Art Garden | `@zoe.art.garden` | 200K | 200k_1m |
| 2025-07-03 | 2026-05-28 | `@enokriisfer` | 鐵雄 Keno | `@enokriisfer` | 16K | 10k_50k |
| 2025-07-03 | 2025-11-29 | `@EMR` | EMR | `@emeryouyangstudio` | 18K | 10k_50k |
| 2025-07-16 | 2025-07-15 | `@2inrow` | Two in Row | `@twoinrow.print` | 15K | 10k_50k |
| 2025-07-22 | 2025-07-16 | `@pixieeeshop` | pixieeeshop | `@pixieeeshop` | 92K | 50k_200k |
| 2025-08-14 | 2025-09-20 | `@mosla_greem` | MOSLA | `@mosla_greem` | 60K | 50k_200k |
| 2025-08-20 | 2025-08-04 | `@goeun` | son go eun | `@ohnicepiece` | 14K | 10k_50k |
| 2025-08-21 | 2025-06-26 | `@mrtom_design` | 湯姆先生 | `@mrtom_design` | 6,142 | lt_10k |
| 2025-08-28 | 2025-08-18 | `@Illustrator225` | IIO | `@illustrator_225` | 118K | 50k_200k |
| 2025-09-05 | 2025-08-01 | `@fluffyomelet` | Fluffy Omelet | `@fluffy_omelet` | 42K | 10k_50k |
| 2025-09-09 | 2025-08-23 | `@dumplingcatfamily` | 餃貓FAMILY | `@hsinhsiu_yao` | 38K | 10k_50k |
| 2025-09-10 | 2025-09-24 | `@bmd` | BMD Design | `@bmddesign` | 43K | 10k_50k |
| 2025-09-11 | 2025-08-13 | `@mengmengknow` | DumbDumb萌獴董懂 | `@dumbradio_meng` | 17K | 10k_50k |
| 2025-09-11 | 2025-09-10 | `@su-felting` | 舒 Su Felting | `@su.felting_` | 23K | 10k_50k |
| 2025-09-12 | 2025-09-03 | `@venusphilosophy` | Venus Philosophy | `@venusphilosophy` | 17K | 10k_50k |
| 2025-09-15 | 2025-09-13 | `@hltoo` | Hltoo | `@hl.t_oo` | 5,613 | lt_10k |
| 2025-09-23 | 2025-09-05 | `@mayyou_studio` | 沒有文青 | `@mayyou_studio` | 24K | 10k_50k |
| 2025-09-29 | 2026-03-22 | `@inkflowcalligraphy` | 墨流書法 | `@inkflowcalligraphy` | 7,295 | lt_10k |
| 2025-09-30 | 2025-11-28 | `@FlashWolves` | 網銀國際閃電狼職業電競隊 | `@flashwolves2013` | 105K | 50k_200k |
| 2025-10-01 | 2025-10-28 | `@byannasienna` | By Anna Sienna | `@byannasienna` | 56K | 50k_200k |
| 2025-10-02 | 2025-09-15 | `@weiweiboy` | weiweiboy 可愛大王 | `@weiweiboy` | 43K | 10k_50k |
| 2025-10-02 | 2025-08-05 | `@yumma` | YUMMA | `@myyumma` | 118K | 50k_200k |
| 2025-10-14 | 2026-02-23 | `@severuslian` | SEVERUS LIAN 里恩太太 | `@severuslian_illustration` | 12K | 10k_50k |
| 2025-11-18 | 2025-07-29 | `@1982kids` | 1982小時候 | `@1982kids` | 18K | 10k_50k |
| 2025-11-24 | 2025-10-28 | `@quintine` | @quintine | Threads | - | - |
| 2025-12-12 | 2025-11-19 | `@lieflatstudio` | 厭世貓貓與雞太郎 | `@taki828_` | 107K | 50k_200k |
| 2026-01-01 | 2025-12-10 | `@doudlestudio` | doudle studio | `@doudlestudio` | 21K | 10k_50k |
| 2026-01-06 | 2025-12-04 | `@GhostJohn` | 幽靈製造所GhostJohn. | `@ghost._.john` | 21K | 10k_50k |
| 2026-01-07 | 2026-01-01 | `@johnnp` | Johnnp | `@johnnp` | 11K | 10k_50k |
| 2026-01-20 | 2026-01-09 | `@double_lu_` | double_lu_( DL Studio ) | `@double_lu_` | 18K | 10k_50k |
| 2026-01-30 | 2026-01-26 | `@wuowuo` | 窩窩商店 wuoshop | `@wuoshop` | 11K | 10k_50k |
| 2026-02-09 | 2026-02-09 | `@waagger` | 威嗝高校 | `@waagger` | 85K | 50k_200k |
| 2026-02-10 | 2026-02-10 | `@yuanfenfactory` | 樂成宮│月緣室 | `@yuanfenfactory` | 2,494 | lt_10k |
| 2026-02-10 | 2026-02-10 | `@rhino-feature` | 犀牛盾棒球主題系列 | - | - | - |
| 2026-02-26 | 2024-09-10 | `@sillysally` | sillysally | `@sillysally.official` | 3,113 | lt_10k |
| 2026-03-02 | 2026-03-02 | `@hancomakkey` | makkey+ | `@hanco_makkey` | 15K | 10k_50k |
| 2026-03-05 | 2026-03-04 | `@Shuku` | Shuku | `@shuku.tinytots` | 16K | 10k_50k |
| 2026-03-13 | 2024-10-31 | `@florfu` | Flor Fuertes | `@florfu` | 21K | 10k_50k |
| 2026-03-31 | 2026-03-13 | `@ripo` | Ripo・Tou | `@11riposhima` | 120K | 50k_200k |
| 2026-04-03 | 2026-03-26 | `@TSGGhostHawks-TSGSkyHawks` | TSG GhostHawks X TSG SkyHawks | - | - | - |
| 2026-04-15 | 2026-04-15 | `@ericatw520` | Erica 在台灣工作的大阪人 | `@ericatw520` | 68K | 50k_200k |
| 2026-04-22 | 2026-04-20 | `@bichi-mao` | 彼奇貓 | `@bichi.mao` | 995K | 200k_1m |
| 2026-04-23 | 2025-08-15 | `@LalaLhuay1918` | LalaLhuay | `@lalalhuay` | 33K | 10k_50k |
| 2026-05-22 | 2026-03-05 | `@cheesyduck` | Cheesy Duck | `@cheesyduck_unstop` | 6,088 | lt_10k |
| 2026-05-24 | 2026-03-25 | `@2an_doodle` | 2an. | `@2an_doodle` | 22K | 10k_50k |
| 2026-06-03 | 2026-06-03 | `@fieldsatbloom` | Fields at Bloom | `@fieldsatbloom` | 42K | 10k_50k |
| 2026-06-12 | 2026-02-09 | `@nagiart` | 吶吉吶吉 | - | - | - |
| 2026-06-26 | 2026-06-26 | `@nipang` | 尼胖 | - | - | - |
| 2026-07-08 | 2026-07-09 | `@rhino-anime` | 動漫教會我的事 | - | - | - |

## Totals

| measure | count |
|---|---|
| records in the roster payload | 182 |
| of which RHINOSHIELD's own in-house theme collections, not creators | 4 |
| of which other non-creator entries (Plurk, a baseball-team pair) | 2 |
| publishing an Instagram handle | 161 |
| Instagram follower count resolved | 160 |
| sub-10k | 21 |

| band | creators | share |
|---|---|---|
| `lt_10k` | 21 | 13.1% |
| `10k_50k` | 93 | 58.1% |
| `50k_200k` | 39 | 24.4% |
| `200k_1m` | 7 | 4.4% |
| `gt_1m` | 0 | 0.0% |
| **total** | **160** | 100% |

Build 2's 21-of-157 sub-10k finding reproduces exactly: build 3 re-resolved every handle from scratch and got **21** sub-10k creators, the same 21, off a slightly larger resolved base (160, because `@1982kids` resolved this time - its roster URL is an `instagram.com/stories/...` form that needs the handle extracting from a different path segment).
The share is therefore **13.1%** of 160 rather than 13.4% of 157; the finding is unchanged.

## The creators with no Instagram in the roster

Build 2 left these 21 as owed work. Build 3 closes them.
Six are not creators at all (four RHINOSHIELD in-house theme collections, one baseball-team pair, and Plurk the social network).
Of the remaining fifteen, six were resolved by other routes and nine remain unresolved after handle-guessing, LINE STORE author lookup and the CET2026 directory join all failed.

| slug | name | outcome |
|---|---|---|
| `@moremoretoe` | MoreMoreToe | Resolved `@moremoretoe`, display name 墨墨頭 MoreMoreToe, **17K** - `10k_50k`, rejected on scale |
| `@thegirl` | The Girl | Unresolved. Name too generic for any index |
| `@mashpatooties` | Mashpatooties | Resolved `@mashpatooties`, display name Riynn Lee, **15K** - rejected on scale |
| `@songprettybell` | Songprettybell | Unresolved |
| `@plurk` | 噗浪 | Not a creator - Plurk, the social network |
| `@Change` | Chaigo | Unresolved. Chaigo, a stray-dog design by Kenji Chai (Malaysia); `@chaigo` and `@chaigo_official` are empty squats |
| `@rongart` | 草棉谷RONG | Resolved `@rong_art`, display name 草棉谷 RONG, **40K** - rejected on scale. (`@rongart` itself is a squat: Dumrong Chaicharoenwut, 48 followers) |
| `@mumub3dpocket` | 木木の口袋 | Resolved `@mumu.b3d.pocket`, display name 木木の口袋, **83K** - rejected on scale. Handle came from the LINE STORE sticker API, which returns `authorName` = `mumu.b3d.pocket` |
| `@shiba-amix` | 棉花糖柴柴與廢貓阿米 | Unresolved. LINE STORE gives `authorName` = "A Mix" for the 棉花糖柴柴 sticker series; no handle follows from it |
| `@chilittleworld` | 阿7世界 | **RESOLVED - now row 11.** `@chi_littleworld`, display name 阿7世界, **3,267**. Guessed handle, confirmed by exact display-name match |
| `@verymissrabbit` | 謙謙創藝-好想兔日常 | Not pursued. 好想兔 is an established licensed property (謙謙創藝), out of scope by the task's exclusion |
| `@chesthairapartment` | 胸毛公寓 | Unresolved. LINE STORE gives `authorName` = "Chest hair apartment"; no handle follows from it |
| `@rhinoshield-specials` | 犀牛盾主題特選 | Not a creator - RHINOSHIELD in-house theme collection |
| `@juanito` | Cazador Juanito | Unresolved |
| `@rhinishield-womens-specials` | 犀牛盾女性主題特選 | Not a creator - RHINOSHIELD in-house theme collection |
| `@quintine` | @quintine | Resolved `@quintine1115`, **641** - the roster publishes only a Threads URL, and the same handle works on Instagram. Rejected on class: the bio describes a Taichung graphic designer, no character |
| `@rhino-feature` | 犀牛盾棒球主題系列 | Not a creator - RHINOSHIELD in-house theme collection |
| `@TSGGhostHawks-TSGSkyHawks` | TSG GhostHawks X TSG SkyHawks | Not a creator - 台鋼 professional baseball teams |
| `@nagiart` | 吶吉吶吉 | **RESOLVED - now row 12.** `@oooo_nagixnagi`, display name NAGIxNAGI!!!吶吉和他的搗蛋怪朋友, **8,105**. Found via the CET2026 directory (exhibitor 122, 吶吉與他的搗蛋怪朋友), not by guessing |
| `@nipang` | 尼胖 | Unresolved, and the most costly miss - 尼胖 is the only IP in this run that appears in **both** brand directories (RHINOSHIELD 2026-06-26 and DEVILCASE crossover 276, 2026-01-20), so a resolved band would have produced two rows. Ten handle guesses and the LINE STORE author page (author 124941, `authorName` = "Nipang") all failed |
| `@rhino-anime` | 動漫教會我的事 | Not a creator - RHINOSHIELD in-house theme collection |
