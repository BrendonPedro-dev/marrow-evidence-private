# Creative Expo Taiwan **2025** exhibitor directory - name-to-Instagram-handle map, with follower bands

Build 4 artefact, and the companion to `cet2026-exhibitor-handle-map.md`.
Swept 2026-08-07 from the previous edition of the same public directory.

**The path shape is different and that is the whole reason builds 1-3 missed it.**
The current edition serves exhibitors at `creativexpo.tw/zh-TW/exhibitor_list/<id>`; the 2025 edition serves them at `2025.creativexpo.tw/zh-TW/**brands**/<id>`, with a second block at `/zh-TW/kuroshio_ips/<id>` for the 黑潮星樂園 original-IP zone.
An id that exists in one namespace 302s into the other, so the two are one id space viewed through two paths.
`2025.creativexpo.tw/robots.txt` disallows only SemrushBot, MJ12bot, AhrefsBot and DotBot, and carries `User-agent: * / Allow: /`.

**The redirect trap, which silently inflates the sweep by 2.4x.** ids 1-759 all return HTTP 200 under a redirect-following client. Only **449** are real brand pages: **310** ids 302 to a single curation page (`嗨，水域場！`) and **41** to the site index. A sweep that counts 200s finds 759 exhibitors and a name-join against that set matches one curation page against everything.
**Rule: keep a page only if the final URL's trailing id equals the requested id.** The same trap is live on the 2026 host and on `collaboration_responses`.

Three Instagram handles (`creativexpo.tw`, `everydayobject.hof`, `no.2.good`) appear on all 759 responses and are site furniture; they were removed by a >50%-of-pages frequency rule before anything below was computed.

## Sweep result

| measure | count |
|---|---|
| ids swept | 1-759 |
| ids resolving to a real brand page | **449** |
| ids redirecting to a curation page or the index | 351 |
| pages publishing at least one Instagram handle | **378** |
| exhibitors with a live follower count resolved | **258** |
| handles probed that returned no `og:description` | 120 |

**Caveat that must travel with the band table below.** Only 258 of the 378 published handles resolved to a count (68%), against near-total resolution on the 2026 edition. The unresolved ones returned no `og:description` at all - private, renamed, deleted, or rate-limited during the sweep. The 2025 share below is therefore **not** directly comparable to the 2026 edition's 46.8% and should not be put beside it without this line.

## Band distribution of the resolved cohort

| band | exhibitors | share |
|---|---|---|
| `lt_10k` | 94 | 36.4% |
| `10k_50k` | 111 | 43.0% |
| `50k_200k` | 38 | 14.7% |
| `200k_1m` | 13 | 5.0% |
| `gt_1m` | 2 | 0.8% |
| **total** | **258** | 100% |

**94 of 258 resolved 2025 exhibitors - 36.4% - are sub-10k.**

## What this dictionary was used for

It is a name-to-handle index, not a row source; exhibiting is not a collaboration.
Against Vein A (DEVILCASE) it resolved **23 partners the 2026 edition does not carry** - 16 by exact name and 7 by an adjudicated partial match. Exactly one, 風速新營 XYWS at 6,011, is sub-10k, and it fails the character test. The other 22 run 16K-271K.
It also supplied the handle for **BIBI波波** (`@bb_hlw`, 12,000), the 大苑子 partner named in the 2025 異業合作 list, and confirmed **臺灣印事** (`@taiwan_impress`, 5,785) against census row 76.

Editions 2022, 2023 and 2024 do not resolve by DNS from here, so the dictionary stops at two editions.

## The sub-10k exhibitors

| followers | 2025 id | exhibitor | Instagram |
|---|---|---|---|
| 435 | 303 | FFFILO | `@fffilo_official` |
| 472 | 217 | ANEM 意識保養 | `@anem.official` |
| 586 | 168 | 超強萌友 | `@supertoughfriends` |
| 593 | 305 | 葫巧工坊手工葫蘆燈工作室 | `@gourds_ace_workshop_` |
| 594 | 186 | 乾唐軒ACERA | `@acera_tw` |
| 697 | 240 | 點睛設計有限公司 | `@taiwan_dotdesign` |
| 799 | 167 | 獨木設計 | `@uni_woodesign` |
| 858 | 165 | 吟遊文創．陳立凡 | `@cccdps` |
| 1,089 | 63 | 東京國際禮品展 | `@giftshowcojp` |
| 1,219 | 251 | 蘆葦女力 | `@swingreeds_official` |
| 1,242 | 207 | 海漂計畫有限公司 | `@entadarr` |
| 1,325 | 4 | KABA：三百多年日本青森傳統工藝「津輕漆器」之創新品牌 | `@kaba_japan` |
| 1,363 | 281 | 樂環實業股份有限公司 | `@ecojoy.tw` |
| 1,410 | 123 | 研石造物X金玉良研 | `@hualienstone` |
| 1,447 | 147 | 朱諾實業社 | `@lalala_home` |
| 1,494 | 214 | 誠十製物所 | `@sincerecraft_tw` |
| 1,555 | 77 | RAFAC / VA凹豆 / 戶外國度 | `@outdoornationtw` |
| 1,693 | 232 | 望秀好商號 | `@oneshoe2015` |
| 1,829 | 97 | 俍伴印所 | `@laidback_sealdesign` |
| 2,089 | 91 | 實驗室香氛 | `@laboratoryscent` |
| 2,117 | 75 | 奭表達有限公司 | `@isfor_art` |
| 2,153 | 198 | 來喲！帽子專門店 | `@layoodesign` |
| 2,280 | 142 | 曉創意股份有限公司 | `@dawn_creative` |
| 2,398 | 275 | 鉐葉 | `@shiye.craft.design` |
| 2,411 | 268 | Float Living | `@floatliving.tw` |
| 2,718 | 176 | 大振豐洋傘有限公司 | `@tcf.umbrella` |
| 2,734 | 121 | 蒙恬實業股份有限公司 | `@iwi_writing` |
| 2,838 | 170 | 木匠兄妹木工房 | `@carpenter_work_shop` |
| 2,907 | 283 | 美美實驗室 | `@suii_suii_lab` |
| 3,033 | 151 | 無所事事小海豹 | `@happacreative` |
| 3,199 | 116 | Unto | `@studiounto` |
| 3,299 | 246 | 臺灣文博會 | `@holenhello` |
| 3,512 | 247 | 百物語文庫 | `@hyakumono_tomei` |
| 3,688 | 103 | 慢火金工創作室 | `@unigaze_metalart` |
| 3,692 | 29 | 閃亮亮樂園 | `@kirakira_land` |
| 3,865 | 196 | 手手生活 | `@hands_life_style` |
| 4,130 | 238 | 玳作 | `@dazzleofficial.co` |
| 4,196 | 300 | BAAN MAEW MAEW | `@baanmaewmaew` |
| 4,207 | 181 | 六悅佳居創意國際有限公司 | `@craftopiataipei` |
| 4,467 | 99 | PÊIHU | `@peihumade` |
| 4,486 | 115 | RE:NEW研舊所 | `@renew_tw` |
| 4,603 | 163 | ei studio | `@eistudio.official` |
| 4,631 | 140 | 洋嘎-天然染織居家生活 | `@younga.tw` |
| 4,682 | 9 | 明順玻璃行 | `@mingshunglass` |
| 4,773 | 195 | 胡創有限公司 | `@hucreates` |
| 4,949 | 13 | 小田月所 | `@hihi.sep` |
| 4,951 | 80 | 針線球有限公司 | `@yarnball27` |
| 4,980 | 185 | A君B子 | `@akunbko` |
| 5,091 | 145 | 珄笙工作室 | `@v.j_studio` |
| 5,250 | 278 | 機腸路路本舖 | `@toriso_ontheway` |
| 5,572 | 244 | UGLYMEWS | `@uglymews.tw` |
| 5,686 | 76 | 香氛森林 | `@scentforest` |
| 5,721 | 258 | K-TOYZ Co.,Ltd. | `@ktoyz_official` |
| 5,828 | 280 | 雄獅鉛筆廠股份有限公司 | `@simbaliontw` |
| 5,930 | 166 | 台電文創 | `@tpcreative.taipower` |
| 5,939 | 291 | 檜山坊─台灣檜木香氛領導品牌 | `@kuai_shan_fang` |
| 6,000 | 252 | 臺灣文博會 | `@eatalldaysheep` |
| 6,011 | 48 | 風速新營 | `@xyws_motards` |
| 6,082 | 57 | 蔡郁珊 | `@shansarts` |
| 6,088 | 177 | 臺灣文博會 | `@cheesyduck_unstop` |
| 6,092 | 296 | eguchitoys | `@eguchitoys` |
| 6,128 | 307 | 甲黨甲替金工手作 | `@lai.lai.craft` |
| 6,173 | 205 | 好玻GOODGLAS | `@goodglastw` |
| 6,277 | 286 | ANTOU 岸頭設計 | `@antoudesign` |
| 6,296 | 42 | iii sum+ 實樂設計 | `@iii_sumplus` |
| 6,297 | 93 | umami | `@umami_tw` |
| 6,308 | 302 | Astrid阿脆 | `@astrid4art` |
| 6,389 | 191 | 山本口金店有限公司 | `@yamamoto_leather` |
| 6,745 | 110 | XAP | `@hello.xap` |
| 6,815 | 52 | 莫克 X 耶思波 | `@moektw` |
| 6,861 | 159 | 麥考艾裘 | `@mkacpen` |
| 7,065 | 24 | 小樹派派 | `@piepiepuu_official` |
| 7,242 | 84 | iNAKATA | `@inakata.tw` |
| 7,292 | 301 | TOAST LIVING | `@toastliving` |
| 7,564 | 96 | 蒔絮紙品 | `@shihsyu_paper` |
| 7,684 | 171 | 國立歷史博物館 | `@nmh_museum` |
| 7,762 | 189 | 臺灣文博會 | `@bloodybunny` |
| 7,813 | 190 | 藍子 | `@mygirlaiko` |
| 8,003 | 235 | THUMP! | `@thump.art` |
| 8,060 | 106 | 蛋定人生 | `@shock_mama` |
| 8,070 | 141 | 臺灣文博會 | `@warbieyama` |
| 8,288 | 119 | 茶包先生 | `@mr.teabag_` |
| 8,338 | 256 | yamama vibe | `@yamama_vibe` |
| 8,440 | 272 | 夏仙 | `@sammi_00712` |
| 8,641 | 66 | WKY560 STUDIO | `@wky560_studio` |
| 8,666 | 293 | ERIC LIAO STUDIO | `@eeericliao` |
| 8,991 | 101 | 波波與小泡芙 | `@bo_puff_bo` |
| 9,072 | 105 | 林源美香店 | `@yuan_incense` |
| 9,276 | 206 | SYDNNI | `@sydnni.co` |
| 9,446 | 287 | 5AM Jewelry | `@5amjewelry` |
| 9,572 | 197 | BOPOMOO 波波畝 | `@bopomoo.tw` |
| 9,639 | 22 | 有樂作業/Splendid Toys | `@yolozuya_toy` |
| 9,745 | 114 | 町金企業有限公司 | `@woolfromsheepmountain` |
| 9,993 | 253 | 富川創造股份有限公司 | `@liferich.creative` |

## The 10k-and-above exhibitors

| followers | 2025 id | exhibitor | Instagram |
|---|---|---|---|
| 2,000,000 | 25 | 貓貓蟲咖波 | `@bugcat_capoo` |
| 1,000,000 | 61 | 黃阿瑪的後宮生活 | `@fumeancat` |
| 995,000 | 233 | 臺灣文博會 | `@bichi.mao` |
| 687,000 | 132 | 廢物女友 | `@lousygirlfriend` |
| 566,000 | 74 | 怪奇事物所 | `@incrediville_tw` |
| 544,000 | 67 | 啾樂創意有限公司 | `@chuchumei__` |
| 477,000 | 102 | 變種吉娃娃 | `@godgwawa` |
| 459,000 | 87 | 栗子頭創意有限公司 | `@onionman__` |
| 420,000 | 69 | 鹿迷動畫設計有限公司 | `@twodeerman` |
| 319,000 | 226 | 寂寞鱷魚有限公司 | `@lonely.crocodile` |
| 275,000 | 153 | 軟Q魚 | `@sqftfish` |
| 262,000 | 134 | 有隻兔子 | `@tooooozitw` |
| 235,000 | 263 | 蜜柑站長 | `@krtcmikan` |
| 230,000 | 188 | 油頭二世 | `@oilheadjunior` |
| 227,000 | 33 | 阿啾小劇場 | `@achusan0817` |
| 168,000 | 298 | 啾啾噗噗 | `@jjjlllove_1209` |
| 138,000 | 83 | 新夭插畫/小樂子創意工作室 | `@brainholesky` |
| 134,000 | 203 | 三個不結婚的女人 | `@yuyuhiei11` |
| 133,000 | 37 | 消極男子 | `@mainasu_com` |
| 127,000 | 292 | 野獸國股份有限公司 | `@beast_kingdom` |
| 123,000 | 43 | 松尼創意國際有限公司 | `@sweethouse.sl` |
| 115,000 | 34 | dtto friends | `@dttofriends` |
| 114,000 | 30 | 萌萌與他的恐龍朋友 &amp; YUANCHi | `@yuanchisart` |
| 114,000 | 169 | 小白的日常 | `@shiromaro_painting` |
| 113,000 | 239 | KINGJUN | `@kingjun` |
| 111,000 | 139 | 咻熊家 | `@xiuxiubear` |
| 107,000 | 184 | FILTER017® | `@filter017` |
| 106,000 | 21 | MooMoo姆姆 | `@moomoo_studio77` |
| 104,000 | 17 | 嗚比的朋友工作室 | `@woobi_dooggy` |
| 101,000 | 285 | Kurt Wu | `@kurrrtwu` |
| 98,000 | 306 | 馬卡龍腳趾 | `@macarontoe` |
| 95,000 | 148 | justfont | `@justfont` |
| 94,000 | 224 | 恐龍的房間工作室 | `@dinosaurs.room` |
| 92,000 | 73 | 三麗鷗 x 哈利波特 x 咻咻熊 x Oolab限量聯名款 | `@oolab.tw` |
| 90,000 | 19 | 吃貨雞仔 | `@foodie_g86821` |
| 89,000 | 267 | 諾米 | `@nuomi0213` |
| 87,000 | 45 | 屎蛋唐尼歡樂動物園 | `@tonystan8787` |
| 85,000 | 237 | 威嗝高校 | `@waagger` |
| 82,000 | 79 | 方坊 | `@squarestudiotw` |
| 77,000 | 297 | 鴨梨子 | `@duck_c4` |
| 73,000 | 143 | 低級失誤 | `@saitemiss` |
| 72,000 | 187 | 1G | `@___1chun` |
| 67,000 | 155 | POPO鴿的鳥日子 | `@popolifetw` |
| 65,000 | 7 | The Butters 奶油家族 | `@thebutters_official` |
| 64,000 | 259 | Crazyeyes瘋狂眼珠 | `@crazyeyes0128` |
| 63,000 | 157 | 梅康米 | `@mekameeee` |
| 60,000 | 59 | 右手超人工作室 | `@ej04zp` |
| 58,000 | 89 | 阿翰 | `@todayfor_han` |
| 56,000 | 193 | 懶散兔與啾先生 | `@lobsterflow` |
| 54,000 | 88 | 夥伴玩具有限公司 | `@partnertoys4` |
| 54,000 | 23 | 路遙圓創有限公司 | `@luyao.design2019` |
| 54,000 | 137 | 熊老闆BearBoss | `@bearboss__` |
| 51,000 | 92 | 布朗尼 | `@annnbrownie` |
| 49,000 | 28 | 波波冰狗室 | `@carol_meat` |
| 49,000 | 164 | 小黃間 | `@littleyellowstudio` |
| 49,000 | 111 | 屌面人 | `@lanpar_man` |
| 47,000 | 94 | 社畜請上車 | `@bowlcut_life` |
| 46,000 | 65 | 日頭 | `@littop_design` |
| 46,000 | 128 | 害羞的黑田桑 | `@shyly_kurodasang` |
| 44,000 | 86 | noii noii | `@noiinoii_official` |
| 44,000 | 173 | mikolu universe | `@mikolu.universe` |
| 44,000 | 122 | 小喵WE | `@wewe_0413` |
| 43,000 | 274 | 企鵝波波 | `@imaginstation` |
| 43,000 | 104 | JINART | `@jinart2018` |
| 42,000 | 231 | 加零在電線桿下 | `@jia0kelvin` |
| 42,000 | 130 | 昏呱 | `@huengua` |
| 40,000 | 36 | 台灣連友股份有限公司 | `@linefriends_square_tw` |
| 40,000 | 225 | 阿軒與一隻灰塵 | `@xuann_illustrator` |
| 40,000 | 209 | 河童卡斯柏 | `@pcklt.kapa` |
| 40,000 | 135 | 胖西是隻河狸 | `@justinisabeaver` |
| 38,000 | 78 | 餃貓FAMILY | `@hsinhsiu_yao` |
| 37,000 | 200 | 蛋塔熊妹 | `@eggybear._.poka` |
| 37,000 | 182 | Minghan H. | `@minminmin_111` |
| 36,000 | 212 | 伸縮自如的雞與鴨 | `@iyayahaaa` |
| 36,000 | 194 | 玩具加乘國際有限公司 | `@toyzeroplus_tw` |
| 35,000 | 273 | 小心臟 | `@jeoyu` |
| 35,000 | 144 | 黑白小姐插畫設計工作室 | `@bnnnnw` |
| 34,000 | 221 | 經典眼鏡 | `@classico2012` |
| 33,000 | 70 | 狗狗夾星 | `@dogdogbengpeng` |
| 33,000 | 131 | Raimochi | `@raimochi` |
| 31,000 | 10 | 小虎day | `@eeeericoco` |
| 30,000 | 179 | 拉麵探險隊 | `@ramen_explorers` |
| 30,000 | 120 | 聚塔創意股份有限公司 | `@towertorch` |
| 30,000 | 11 | 郁郁 | `@yuyuteadaily` |
| 29,000 | 55 | 歐亞迪國際企業有限公司 | `@paperself_tw` |
| 29,000 | 229 | LSY林三益專業彩妝刷具 | `@lsy_tw` |
| 29,000 | 220 | 東億兆實業有限公司 | `@nikkohelmets_tw` |
| 28,000 | 85 | 酪梨 | `@_avocado__` |
| 28,000 | 46 | 株式会社Craft Tokyo | `@toki.tokyo.accessories` |
| 28,000 | 242 | 唐葫蘆姑娘 | `@miss_tanghulu` |
| 28,000 | 107 | YuYing｜神秘狗是一隻兔子 | `@yuying_1203` |
| 27,000 | 276 | club babo design | `@club_babo` |
| 27,000 | 27 | 阿說不想說 | `@lishuo_bushuo` |
| 27,000 | 192 | 青青小樹 | `@doromon01` |
| 26,000 | 54 | 腋毛人 | `@yemao20130628` |
| 26,000 | 31 | 臺灣文博會 | `@cafeandhof` |
| 25,000 | 2 | Take a Snooze 瞇一下｜台灣質感香氛 | `@takeasnooze` |
| 25,000 | 138 | 點點陳插畫事務所 | `@pointdiary` |
| 25,000 | 113 | 你好藝思有限公司 | `@hellostudiotw` |
| 25,000 | 112 | 甜蜜生活 | `@ladolcevitastudio` |
| 24,000 | 90 | 一公分手作 | `@1cm_handmake` |
| 24,000 | 50 | 臺灣文博會 | `@unmelt` |
| 24,000 | 248 | 兔君 | `@lubonnie_art` |
| 23,000 | 53 | 獺咘獺咘 | `@149.bonny.lin` |
| 23,000 | 249 | SU.FELTING | `@su.felting_` |
| 23,000 | 109 | 大宇人的小雨宙超市 | `@dayuyoyo` |
| 22,000 | 56 | 小小PETIT 水性無毒可剝指甲油 | `@petit_girls` |
| 22,000 | 44 | 嗨小強 | `@hi_johnnn` |
| 22,000 | 208 | 杜波淇繪部 | `@toballkidrawing` |
| 22,000 | 199 | 山羊先生工作室 | `@mrgoat9` |
| 22,000 | 133 | 其實他是鵝 | `@hui____7` |
| 22,000 | 124 | 喔噢你好 | `@ohall_official` |
| 22,000 | 12 | 牙技師的牙齒們 | `@yajishi_de_teeth` |
| 21,000 | 60 | 微醺斑比 | `@abbybambi` |
| 21,000 | 49 | 幽靈製造所 | `@ghost._.john` |
| 21,000 | 234 | 臺灣文博會 | `@berry_winkle_` |
| 21,000 | 202 | 文化內容策進院 | `@taicca.tw` |
| 21,000 | 117 | Shadoowww | `@shadoowww__` |
| 21,000 | 1 | doudle studio | `@doudlestudio` |
| 20,000 | 290 | 安怎？Ann-Nua | `@ann_nua_handmade` |
| 20,000 | 129 | 紙間設計有限公司 | `@liyu.lin.tw` |
| 20,000 | 125 | 圓臉人 | `@circular5132` |
| 19,000 | 219 | 緩緩工作室 | `@whonwhon1126` |
| 18,000 | 81 | 花大鼻小文青工作室 | `@huadabii0610` |
| 18,000 | 38 | 露咖貓 | `@lookacat.studio` |
| 18,000 | 270 | 丸樂趣國際有限公司 | `@playtoysforever.co.ltd` |
| 18,000 | 26 | 奇意果國際有限公司 | `@hmmproject` |
| 17,000 | 204 | 沃廚 | `@wokywaterbottle` |
| 17,000 | 149 | 慢慢挑 | `@pianopiano.pick` |
| 16,000 | 98 | 咚東 | `@dong.dong.illustration` |
| 16,000 | 51 | 噗尼 | `@mobell_2020` |
| 16,000 | 41 | 虎爺實習中 | `@paparaya` |
| 16,000 | 236 | 來碗寬片片 | `@kuanpianpian` |
| 16,000 | 16 | 美可女子 | `@mayco.tw` |
| 16,000 | 100 | somesortof.fern | `@somesortof.fern` |
| 15,000 | 71 | FandoraShop | `@fandorashop` |
| 15,000 | 58 | 水紋汀 | `@wavecement` |
| 15,000 | 47 | 陌光 | `@st.light_studio` |
| 15,000 | 3 | 卡卡瑪蒂工作室 | `@corgikaka` |
| 15,000 | 211 | 茶浣熊 | `@tanukii_don` |
| 15,000 | 178 | 維尼有畫想說 | `@spx_wie` |
| 15,000 | 175 | Story Wear | `@storywear_continues` |
| 15,000 | 154 | 三貓俱樂部 | `@miimiicat` |
| 14,000 | 68 | 皮康 | `@pikangpikang` |
| 14,000 | 265 | 安喬欣業有限公司 | `@etseq.nailpolish` |
| 14,000 | 261 | 起司貝爾 | `@chiiz_bear` |
| 14,000 | 210 | 世界漂亮在台協會 | `@kirei_league` |
| 14,000 | 152 | 織療室 | `@ziliaoshi` |
| 14,000 | 126 | 肉球paw pad | `@paw_pad` |
| 14,000 | 118 | 地獄書道工作室 | `@kaishodo` |
| 13,000 | 216 | HEY SUN | `@heysun.tw` |
| 12,000 | 35 | 塗狗 | `@togo.clay` |
| 12,000 | 277 | 小圓麵包 | `@frodog_10` |
| 12,000 | 257 | 富比商貿有限公司 | `@fubees` |
| 12,000 | 255 | superB studio | `@superb_studio` |
| 12,000 | 254 | 宅男打籃球 | `@theunderdogs_tw` |
| 12,000 | 222 | 里恩太太 | `@severuslian_illustration` |
| 12,000 | 162 | BIBI波波 | `@bb_hlw` |
| 11,000 | 95 | 摩摩渣渣 | `@momoxzaza` |
| 11,000 | 294 | 幽默之星 | `@twinkle_twinkle_humor_star` |
| 11,000 | 201 | 源源鋼藝 | `@hello_uanuan` |
| 11,000 | 156 | HiHi 搗蛋鬼 | `@hihi_trickster` |
| 11,000 | 14 | Tabbi L | `@tabbiliaw_art` |
| 10,000 | 32 | 妯米 | `@nozomii.art` |

## Exhibitors publishing a handle that returned no count

These are unbanded, not counted as anything.

| 2025 id | exhibitor | Instagram |
|---|---|---|
| 72 | 簡莘蒂 | `@chienpj` |
| 160 | 小怪家 | `@yiekubo` |
| 227 | 下班後的魔法王國 | `@willsann_` |
| 230 | an everything | `@n_senses_` |
| 264 | 麗嬰國際股份有限公司 | `@funmediatw` |
| 269 | CHICKENMAN大雞雞人 | `@kkoo1377` |
| 279 | CEMENT PRODUCE DESIGN | `@cementproducedesign_japan` |
| 299 | 日耀堂 | `@betterdays_studio` |
| 308 | 醜白兔 (海沐島設計有限公司) | `@uglyrabbit.07` |
| 309 | 陳彫刻處 | `@chenswood` |
| 310 | 三支筆工作室 | `@penpenpenstudio` |
| 311 | 一帆布包 | `@yi_fan_canvas_bags` |
| 312 | no.30 | `@no.30designs` |
| 313 | A ee mi | `@e.e___c` |
| 314 | 這一窯 Huiaio studio | `@huiaio_studio` |
| 316 | 臺灣文博會 | `@thepinkfongcompany` |
| 317 | 繩經 | `@nerve.jumprope` |
| 318 | 九天民俗技藝團 | `@chio_tian_drums` |
| 319 | 臺灣印事 | `@taiwan_impress` |
| 322 | 臺灣文博會 | `@muffin.corner` |
| 323 | 夢の犬與他的朋友們 | `@bananalin2006` |
| 324 | 好生藝品牌管理顧問有限公司 | `@brandbeat_group` |
| 325 | 茉荷 | `@mihercare` |
| 326 | 三日揖 | `@321_writing` |
| 327 | 辛卡米克創意有限公司 | `@sinkcomic` |
| 328 | 昀子YUNZI | `@yunzi_00` |
| 329 | 春天先生 | `@mr.spring_and_his_fish` |
| 330 | BOMBOM Co., | `@bombom_co` |
| 331 | 小怪選物有限公司 | `@the.weird.things` |
| 332 | 帕崎工作室 | `@_pachipachi` |
| 333 | 瀏海樹 | `@bangstree2012` |
| 335 | 豆苗先生 | `@mr.doumiao` |
| 336 | 陳皮製茶 | `@chenpi_tea` |
| 338 | 愛烙達股份有限公司 | `@ogrill_tw` |
| 339 | 人中人株式會社 | `@fat_bin_2007` |
| 340 | 連鎖 | `@momentscompany_japan` |
| 341 | 本質創作室 | `@essencedesigntw` |
| 342 | ZENLET | `@zenlet` |
| 343 | 兩顆糖製造機 | `@goodmiastyle` |
| 344 | 好說設計股份有限公司 | `@hibang_official` |
| 345 | 山霧設計股份有限公司 | `@zenu_design` |
| 346 | 維納絲畫著說 | `@venusphilosophy` |
| 351 | 棉花糖柴柴與廢貓阿米 | `@fuckcute.studio` |
| 352 | mind.a.day(cover cat) | `@mindaday_studio` |
| 353 | 上山上山，嘉南平原欸氣味 | `@homecomingfragrance` |
| 354 | 小學課本的逆襲 | `@turtledrawturtle` |
| 355 | 祖母綠 插畫設計 | `@emerald_illustration` |
| 356 | 臺灣文博會 | `@studio_pigeon` |
| 357 | 亭氏香氛 | `@tings_aroma` |
| 358 | 愚室實驗所 | `@yu_shi_lab` |
| 360 | 台北市工業設計發展協會 | 新燃點 | `@iddat.tp` |
| 362 | 艸一田人 | `@huangs.studio` |
| 363 | 岸下事物 | `@tydo_info` |
| 364 | 相信音樂國際股份有限公司 | `@binmusic.ig` |
| 366 | 肥肥與阿胡 | `@ffah_diary` |
| 367 | picupi挑品 | `@picupi.life` |
| 368 | 神戶皮革合作社 | `@kobe_leather_official` |
| 372 | 臺灣文博會 | `@sweetsummer.shop` |
| 374 | 豚友文創設計股份有限公司 | `@ct_pig` |
| 376 | 民傑資科股份有限公司 | `@maktar_tw` |
| 380 | 踊の心 | `@odo.ri` |
| 381 | 波實業有限公司 | `@n__afl` |
| 382 | 雲杉設計 Spruce Artistry | `@spruceartistry` |
| 383 | 母栽 | `@moodplant_official` |
| 385 | Pinkoi | `@ilovepinkoi` |
| 386 | 臺灣文博會 | `@ladne.co` |
| 389 | 大苑子 | `@dayungs_official` |
| 415 | 優諾創作室有限公司 | `@kingyonekosan` |
| 417 | 奴作工作室有限公司 | `@pawsomeisland` |
| 418 | 廢青豬妮 | `@genieee.hk` |
| 421 | 莫啃泥與賴讓插畫 | `@mokeni` |
| 424 | 里奧白工作室 | `@creamy_lili` |
| 440 | AMVEL UMBRELLA STORE | `@amvel_umbrella_store` |
| 442 | 檬檬糖糖 | `@lemonsugarjp` |
| 443 | 小餃子喬桑 | `@watanabeai` |
| 444 | 臺灣文博會 | `@icelolly.zakka` |
| 445 | 哈利剣 | `@harikenjp` |
| 446 | 郁金香王子★BUNTAN | `@zuco_tokyo` |
| 447 | 歯の漫画 | `@hanomanga_ha` |
| 448 | 竹輪串串 | `@chikuwas1` |
| 449 | 臺灣文博會 | `@himatan_desyu` |
| 451 | 麻吉鴨鴨 | `@mocaccha` |
| 452 | 臺灣文博會 | `@3eyestakahashi` |
| 453 | 臺灣文博會 | `@tama__m27` |
| 454 | 彩虹貓咪樂園・ねこらんど | `@rinrin.cioccomoca` |
| 456 | aimant,e.,inc. | `@cheek.official.am` |
| 457 | 臺灣文博會 | `@rokkaku_official` |
| 458 | 柴尾 | `@shibao_` |
| 459 | 黑貓設計 | `@kuroneko_design` |
| 460 | 臺灣文博會 | `@kucch_kiwi` |
| 461 | Show-Mon Art Co., Ltd | `@show_mon_art` |
| 463 | kapuwa | `@kapuwa_official` |
| 464 | 株式会社  寺一 | `@teraichi_knit` |
| 465 | 臺灣文博會 | `@hanabi_crayon` |
| 467 | 臺灣文博會 | `@jop_dong_sa_ni` |
| 468 | 臺灣文博會 | `@mill_artworks` |
| 469 | 臺灣文博會 | `@weirdolls_official` |
| 471 | 臺灣文博會 | `@hellogitii` |
| 472 | 臺灣文博會 | `@ds_tape` |
| 474 | 臺灣文博會 | `@yangchee_` |
| 475 | 京都烏丸六七堂 | `@kyoto_karasuma_67` |
| 477 | 巴吉波特 | `@baggyport` |
| 479 | 不明生物俱樂部 | `@creaturecollectorsclub` |
| 480 | 臺灣文博會 | `@hohoholahk` |
| 481 | 拉筋熊公司 | `@stretching_bear` |
| 482 | 派膠玩具有限公司 | `@tooplastic` |
| 483 | 妖怪畫坊 | `@daol_palette` |
| 484 | 臺灣文博會 | `@brunch_friends` |
| 486 | 口羊豆頁miemietou | `@miemie_tou` |
| 487 | 恐龍山丘 | `@dinovalleytw` |
| 489 | 沐籟工藝設計工作室 | `@m.oonl_ight` |
| 491 | 寶璽文創實業有限公司 | `@wenwenworks` |
| 492 | 左翌創意設計工作室有限公司 | `@zoels_wonderland` |
| 496 | 起風 | `@thewindrises2019` |
| 500 | 嘉義異鄉人 | `@outsiderinchiayi` |
| 502 | 精工刻印有限公司 | `@jing_gong_stamp` |
| 503 | 雙夏工作室 | `@PatonaNatsu` |
| 504 | 小呸角 | `@ooooo_play` |
| 508 | 波來多巴笛 | `@parade_party` |
| 512 | SUNMAI | `@sunmai.beer` |
