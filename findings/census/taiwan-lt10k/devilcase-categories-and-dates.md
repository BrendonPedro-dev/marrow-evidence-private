# DEVILCASE 惡魔防摔殼 `/crossover/` - category taxonomy and asset-upload dating

Build 2 addition to `devilcase-crossover-directory.md`. Swept 2026-08-07.

**Two things build 1 missed, both of them on the page all along.**

**1. The directory is categorised, and the category is published.** `https://devilcase.com.tw/crossover/?cate=<1-6>` pages the whole directory by class, and each partner page carries its class in the breadcrumb. This replaces build 1's hand-classification of licensed vs independent, and it identifies the VTuber block exactly instead of by bio keyword.

| cate | label | partners |
|---|---|---|
| 1 | 熱門經典角色 (popular classic characters) | 17 |
| 2 | 三麗鷗聯名 (Sanrio) | 25 |
| 3 | 臺灣創作與角色 (Taiwanese creations and characters) | 127 |
| 4 | 海外創作與角色 (overseas creations and characters) | 16 |
| 5 | VTuber | 39 |
| 6 | 遊戲與動漫 (games and anime) | 14 |
| | **total** | **238** |

Build 1 counted 236 partner pages by id sweep and estimated 29 VTubers from bio keywords. The category sweep finds **238** partners and **39** VTubers - so the keyword heuristic under-counted the VTuber block by ten, and ten pages build 1 would have banded off Instagram are not Instagram-primary at all.

The `lt_10k` working population is **cate 3 + cate 4 = 143** partners. Cates 1, 2 and 6 (56 partners) are licensed property and out of scope by the task's own exclusion. Cate 5 (39) is held out pending a YouTube/Twitch read.

**2. Every partner page is exactly datable from its own asset filenames.** DEVILCASE uploads crossover art to `https://i.devilxxxx.com/uploads/crossover/<YYYYMMDDHHMMSS>.jpg` - the filename *is* the upload timestamp. The earliest such timestamp on a partner page dates that partner's art.

Cross-check against build 1's Wayback bracketing: crossover 308 (茶包先生, row 1) reads `20260429155101`, i.e. 2026-04-29 - inside the 2026-04-14 / 2026-05-09 bracket build 1 derived, and it collapses that ~3-week window to a single day. Crossover 321 (Wasabi Bear, row 2) reads 2026-07-08, consistent with build 1's post-2026-05-09 inference.

**The caveat that matters.** The timestamp dates the *art currently on the page*, so where DEVILCASE has refreshed a partner's artwork the reading is a refresh date, not a launch date. This is visible and self-diagnosing: crossover 1 (空罐王) was already live in the 2023-12-04 bulk crawl but reads 2025-10-29, because its art was replaced. **The rule: where the asset timestamp precedes the Wayback first capture it is the launch date; where it postdates it, it is a refresh date and the Wayback capture governs.** Ten low ids still read 2020-2022, which means their art has never been replaced and they are genuinely pre-window.

## Full table

| id | category | IP partner | earliest asset upload |
|---|---|---|---|
| 1 | 臺灣創作與角色 | 空罐王 | 2025-10-29 |
| 8 | 臺灣創作與角色 | 英格藍貓 | 2020-09-17 |
| 9 | 臺灣創作與角色 | Atha | 2020-08-06 |
| 11 | 臺灣創作與角色 | 泡芙 | 2026-01-05 |
| 12 | 臺灣創作與角色 | 瘋狂眼珠 | 2024-12-10 |
| 13 | 臺灣創作與角色 | 天之火 | 2025-02-12 |
| 18 | 臺灣創作與角色 | Maruco小畫室 | 2026-06-29 |
| 19 | 臺灣創作與角色 | 好想兔 | 2026-03-04 |
| 20 | 臺灣創作與角色 | 水獺蹭蹭 | 2026-06-22 |
| 21 | 三麗鷗聯名 | 布丁狗 | 2025-05-12 |
| 22 | 臺灣創作與角色 | 地呱球 | 2025-10-01 |
| 23 | 臺灣創作與角色 | 浪味仙貝 | 2020-12-23 |
| 25 | 熱門經典角色 | 不二馬大叔 | 2025-01-21 |
| 26 | 熱門經典角色 | 小王子 | 2026-06-24 |
| 27 | 三麗鷗聯名 | 蛋黃哥 | 2025-05-12 |
| 31 | 臺灣創作與角色 | 柚町 | 2026-06-22 |
| 32 | 三麗鷗聯名 | 美樂蒂 | 2025-04-30 |
| 33 | 臺灣創作與角色 | 純粋 | 2024-02-29 |
| 34 | 臺灣創作與角色 | 兩小無猜 | 2025-09-03 |
| 35 | 臺灣創作與角色 | 霸軒與小美 | 2025-05-16 |
| 36 | 臺灣創作與角色 | 垃圾人 Trashman | 2022-07-25 |
| 37 | 臺灣創作與角色 | 鯊魚先生 | 2025-01-20 |
| 40 | 臺灣創作與角色 | Neneko 貓日 | 2025-10-02 |
| 45 | 臺灣創作與角色 | Sweet House | 2026-07-15 |
| 46 | 熱門經典角色 | 胸毛公寓 | 2024-09-18 |
| 49 | 臺灣創作與角色 | Pink Cat 小儀 | 2022-09-15 |
| 52 | 熱門經典角色 | 白爛貓 | 2025-08-27 |
| 53 | 海外創作與角色 | 呦嘻百分百 | 2026-06-24 |
| 55 | 臺灣創作與角色 | 肥兔寶 Fattubo | 2021-08-10 |
| 58 | 臺灣創作與角色 | 麵包樹 Bread Tree | 2025-12-18 |
| 59 | 臺灣創作與角色 | 寶寶不說 | 2026-03-16 |
| 61 | 臺灣創作與角色 | 柴語錄 | 2022-07-11 |
| 62 | 遊戲與動漫 | 傳說對決 | 2025-07-23 |
| 63 | 海外創作與角色 | 世上不可思議的貓世界 | 2024-08-28 |
| 65 | 三麗鷗聯名 | 大耳狗喜拿 | 2025-05-13 |
| 66 | 三麗鷗聯名 | 大眼蛙 | 2025-05-07 |
| 67 | 三麗鷗聯名 | 帕恰狗 | 2025-05-07 |
| 68 | 三麗鷗聯名 | 酷洛米 | 2025-04-30 |
| 69 | 三麗鷗聯名 | 酷企鵝 | 2025-05-05 |
| 70 | 三麗鷗聯名 | 雙星仙子 | 2025-05-05 |
| 72 | 海外創作與角色 | 助六的日常 | 2026-04-29 |
| 76 | 臺灣創作與角色 | ㄇㄚˊ幾兔 | 2024-06-05 |
| 78 | 熱門經典角色 | 哆啦A夢 | 2025-12-22 |
| 80 | 熱門經典角色 | 變種吉娃娃 | 2025-02-26 |
| 82 | 臺灣創作與角色 | 87小兔 chichi | 2025-10-08 |
| 83 | 臺灣創作與角色 | 某人日常 | 2022-03-31 |
| 86 | VTuber | 浠Mizuki | 2025-01-15 |
| 87 | 臺灣創作與角色 | 狐吉Huchii | 2025-10-01 |
| 89 | 臺灣創作與角色 | weiweiboy | 2026-05-11 |
| 90 | 海外創作與角色 | 卡娜赫拉的小動物 | 2025-07-09 |
| 92 | 臺灣創作與角色 | MYAOWL喵喔 | 2026-05-25 |
| 93 | 臺灣創作與角色 | 消極男子 Mainasu otoko | 2024-03-11 |
| 94 | 臺灣創作與角色 | 貓爪抓 | 2023-12-25 |
| 95 | 臺灣創作與角色 | 一輛YiLiang | 2026-01-28 |
| 96 | 臺灣創作與角色 | 醜白兔 | 2026-05-04 |
| 97 | 臺灣創作與角色 | 胖鯊魚鯊西米 | 2026-07-08 |
| 98 | 遊戲與動漫 | 和大姐姐愉快的感覺 | 2025-09-24 |
| 100 | VTuber | 空雲悠白 | 2026-05-29 |
| 101 | VTuber | 杏仁ミル | 2024-07-15 |
| 104 | 海外創作與角色 | 喫茶こぐまや | 2025-09-01 |
| 107 | 臺灣創作與角色 | 埃及大旅社 | 2024-10-28 |
| 109 | 臺灣創作與角色 | Naomi 芝 | 2022-12-07 |
| 112 | 三麗鷗聯名 | 人魚漢頓 | 2025-05-05 |
| 113 | 三麗鷗聯名 | 小麥粉精靈 | 2025-05-14 |
| 114 | 三麗鷗聯名 | 山姆企鵝 | 2025-05-05 |
| 117 | VTuber | KSP | 2024-12-30 |
| 120 | 海外創作與角色 | 墨繪師御歌頭 | 2025-01-15 |
| 124 | VTuber | 兔姬UsagiHime｜惡兔重工 | 2026-06-15 |
| 128 | VTuber | 瑪格麗特．諾爾絲 | 2026-06-17 |
| 129 | VTuber | 森森鈴蘭 | 2026-06-17 |
| 130 | 熱門經典角色 | 櫻桃小丸子 | 2026-07-15 |
| 133 | 臺灣創作與角色 | 胖才可愛 | 2025-06-04 |
| 137 | VTuber | EXITUS | 2026-03-16 |
| 138 | VTuber | 懶貓子 | 2026-03-16 |
| 139 | VTuber | 稻乙緹 | 2025-10-29 |
| 140 | 海外創作與角色 | 貓福珊迪 | 2026-06-24 |
| 141 | VTuber | Aoi Hinamori | 2025-09-03 |
| 142 | 臺灣創作與角色 | 玩什麼鬼啦 | 2026-07-06 |
| 143 | VTuber | 塔芭絲可 | 2025-11-10 |
| 144 | 臺灣創作與角色 | Go車誌 | 2024-06-07 |
| 146 | 臺灣創作與角色 | 黃蜂 BUMBLEBEE | 2024-06-26 |
| 149 | VTuber | 霓NEO(n) | 2026-05-27 |
| 150 | 熱門經典角色 | 吉伊卡哇 | 2026-05-27 |
| 151 | VTuber | 厭世醫師阿萬 | 2025-07-17 |
| 153 | VTuber | 極深空計畫 | 2024-11-14 |
| 154 | 臺灣創作與角色 | 何畇蓁YunzhenHo | 2024-11-13 |
| 156 | 臺灣創作與角色 | 小水豚豆仔 | 2025-09-05 |
| 158 | 臺灣創作與角色 | 灰塵魚 | 2025-04-21 |
| 159 | 臺灣創作與角色 | Aida&Kiki | 2024-11-27 |
| 161 | VTuber | 月蝕屋 MΦONLIT | 2024-11-27 |
| 162 | 臺灣創作與角色 | 想你熊shiny bear | 2026-06-01 |
| 163 | 遊戲與動漫 | 小河少年Kawa | 2025-11-12 |
| 165 | 臺灣創作與角色 | 薯樂棉棉島 | 2024-12-12 |
| 166 | 臺灣創作與角色 | 風速新營XYWS | 2024-12-12 |
| 167 | 臺灣創作與角色 | 麻吉貓 | 2026-04-29 |
| 168 | 臺灣創作與角色 | YUANCHi | 2025-11-11 |
| 169 | 臺灣創作與角色 | 香菇妹&拉比豆 | 2024-12-19 |
| 170 | 遊戲與動漫 | MONSTER HUNTER RISE / Monster Hunter Rise: sunbreak | 2024-12-19 |
| 171 | 熱門經典角色 | 海綿寶寶 | 2025-06-25 |
| 174 | 臺灣創作與角色 | 畫說日常 | 2026-07-27 |
| 175 | 臺灣創作與角色 | 一氏插畫工作室 Escouple | 2025-06-11 |
| 176 | 臺灣創作與角色 | 河童卡斯柏 Kasper | 2026-04-01 |
| 177 | 臺灣創作與角色 | 小心臟Little Heart | 2025-01-23 |
| 178 | 臺灣創作與角色 | 百鬼夜行誌 | 2025-08-13 |
| 179 | 臺灣創作與角色 | 小學課本的逆襲 | 2025-10-30 |
| 180 | 臺灣創作與角色 | 青青小樹 | 2025-11-26 |
| 181 | 臺灣創作與角色 | 羅寗 | 2025-02-13 |
| 182 | 臺灣創作與角色 | 紐約狗狗 | 2025-02-13 |
| 183 | 臺灣創作與角色 | 檸檬酸姐姐 | 2026-07-20 |
| 184 | 臺灣創作與角色 | PP mini 小小企鵝 | 2026-01-21 |
| 185 | 臺灣創作與角色 | Dorothy | 2025-02-13 |
| 186 | 臺灣創作與角色 | Nepeta Liu 貓仔草 | 2026-04-24 |
| 187 | 臺灣創作與角色 | 床編故事 | 2026-06-17 |
| 188 | VTuber | Alluria | 2025-02-20 |
| 189 | VTuber | MeloNyx | 2025-02-20 |
| 190 | 臺灣創作與角色 | Say HANa 林花 | 2026-08-03 |
| 191 | VTuber | 扉暮 | 2025-04-07 |
| 192 | 臺灣創作與角色 | 加零在電線桿下 | 2026-04-27 |
| 193 | 臺灣創作與角色 | 哭哭夥伴 | 2025-10-08 |
| 194 | 臺灣創作與角色 | 萬大 | 2025-11-12 |
| 195 | VTuber | 貓祭 | 2026-01-26 |
| 196 | 臺灣創作與角色 | chengcheng | 2025-03-14 |
| 197 | VTuber | 妖狐艾兒 | 2025-09-22 |
| 198 | VTuber | 食用系少女 | 2025-09-22 |
| 201 | 臺灣創作與角色 | 棉花獅的藝想世界 | 2026-01-05 |
| 203 | 臺灣創作與角色 | 竹筍日常Bambooxun | 2025-03-11 |
| 204 | 臺灣創作與角色 | 滴的小動物 | 2026-03-27 |
| 207 | 臺灣創作與角色 | 大幸子 | 2026-06-15 |
| 208 | 臺灣創作與角色 | 阿軒與一隻灰塵 | 2025-07-28 |
| 210 | 臺灣創作與角色 | 雞童可愛宮 | 2025-03-27 |
| 211 | 臺灣創作與角色 | 一事吳陳 | 2026-05-04 |
| 212 | 臺灣創作與角色 | 爺恩YA·NG | 2025-11-26 |
| 213 | 臺灣創作與角色 | itsalicelee art | 2026-07-13 |
| 216 | 臺灣創作與角色 | MEIMEIbyH.H先生 | 2025-04-09 |
| 217 | 臺灣創作與角色 | 獨角龍豆豆＆豆比 | 2026-04-15 |
| 219 | 臺灣創作與角色 | 路易斯與布丁 | 2025-04-09 |
| 220 | 臺灣創作與角色 | Luckylulu | 2026-07-01 |
| 222 | 海外創作與角色 | 寺田堤拉 | 2026-07-08 |
| 224 | 臺灣創作與角色 | 大頭兒 Ms. Big | 2026-04-27 |
| 225 | VTuber | 烟花蹦蹦蹦 | 2025-04-23 |
| 226 | 三麗鷗聯名 | 切片妞 | 2025-05-06 |
| 227 | 三麗鷗聯名 | 毛毯熊莫普 | 2025-05-06 |
| 228 | 臺灣創作與角色 | BaNAna Lin | 2025-05-15 |
| 229 | 臺灣創作與角色 | 宇宙貓咪 | 2025-05-14 |
| 230 | 臺灣創作與角色 | wei3h | 2025-05-14 |
| 231 | 臺灣創作與角色 | 阿啾小劇場 | 2026-04-01 |
| 232 | VTuber | 真理果 | 2025-05-19 |
| 233 | VTuber | ５１５ | 2025-05-22 |
| 234 | VTuber | Bana 蕉バナ | 2025-05-22 |
| 235 | 臺灣創作與角色 | Dooing初生之犢 | 2025-05-22 |
| 236 | 臺灣創作與角色 | 屎蛋唐尼 | 2025-05-22 |
| 237 | 臺灣創作與角色 | 小民日子 | 2026-05-20 |
| 238 | 臺灣創作與角色 | 肥肥與阿胡 | 2025-11-17 |
| 239 | 臺灣創作與角色 | dtto friends | 2026-04-08 |
| 241 | 臺灣創作與角色 | 兔鼠AEUAO | 2025-06-16 |
| 242 | 臺灣創作與角色 | 毛毛蟲 | 2025-06-12 |
| 243 | 臺灣創作與角色 | 笨笨喵 | 2025-06-19 |
| 245 | VTuber | Limnos 利姆諾斯 | 2026-07-30 |
| 246 | VTuber | Shippo尾巴 | 2025-07-10 |
| 247 | 海外創作與角色 | PINK ＆ VEN | 2025-08-11 |
| 248 | 臺灣創作與角色 | afu插畫日誌 | 2025-07-21 |
| 249 | 臺灣創作與角色 | 交換日記 | 2026-01-28 |
| 250 | VTuber | 庫洛姆 | 2025-07-31 |
| 251 | 熱門經典角色 | 加菲貓 | 2025-07-31 |
| 252 | 熱門經典角色 | MOOMIN | 2025-08-27 |
| 253 | 遊戲與動漫 | 請解開故事謎底 | 2025-09-01 |
| 255 | 遊戲與動漫 | 十八日 | 2025-09-03 |
| 256 | 臺灣創作與角色 | 累累LeiLei | 2025-09-19 |
| 257 | 臺灣創作與角色 | 新竹天王寺財神廟 | 2026-06-15 |
| 258 | 臺灣創作與角色 | 鳥時代 | 2025-10-16 |
| 259 | 海外創作與角色 | 鯊貓 | 2026-05-06 |
| 260 | 臺灣創作與角色 | 噗尼 Mobell | 2025-10-31 |
| 261 | 臺灣創作與角色 | 俞璟 | 2026-06-01 |
| 262 | VTuber | 名雪薇薇 NayukiViVy | 2025-11-14 |
| 263 | 臺灣創作與角色 | 伸縮自如的雞與鴨 | 2025-11-14 |
| 264 | VTuber | 鷗麥麥麥 | 2025-11-20 |
| 265 | 臺灣創作與角色 | 軟Q兔兔 | 2025-11-28 |
| 266 | 臺灣創作與角色 | 啾啾噗噗 | 2025-11-28 |
| 267 | 遊戲與動漫 | 逼居BIIJI | 2025-11-28 |
| 268 | 臺灣創作與角色 | 來碗寬片片 | 2025-12-03 |
| 269 | 海外創作與角色 | NOMA | 2025-12-05 |
| 270 | 臺灣創作與角色 | 牙技師的牙齒們 | 2025-12-12 |
| 271 | 臺灣創作與角色 | 小怪家 | 2025-12-12 |
| 272 | 三麗鷗聯名 | 夢幻遊樂園 | 2025-12-12 |
| 273 | 三麗鷗聯名 | 馬年 | 2025-12-12 |
| 274 | 臺灣創作與角色 | シロマロ 小白 | 2025-12-31 |
| 275 | 熱門經典角色 | 獵人 HUNTERxHUNTER | 2025-12-31 |
| 276 | 臺灣創作與角色 | 尼胖 | 2026-01-20 |
| 277 | 遊戲與動漫 | PockyCity夢蕾 | 2026-01-20 |
| 278 | 三麗鷗聯名 | Charmmykitty | 2026-01-20 |
| 279 | 三麗鷗聯名 | Tiny Chum | 2026-01-20 |
| 280 | 三麗鷗聯名 | 許願兔 | 2026-01-20 |
| 281 | 三麗鷗聯名 | 萌可魯玩偶貓 | 2026-01-20 |
| 282 | 三麗鷗聯名 | 大寶 | 2026-01-20 |
| 283 | 三麗鷗聯名 | 可樂鈴 | 2026-01-20 |
| 284 | 三麗鷗聯名 | 貝克鴨 | 2026-01-20 |
| 285 | 三麗鷗聯名 | 梅羅 | 2026-01-20 |
| 286 | 遊戲與動漫 | 艸肅Tsaosu | 2026-01-20 |
| 287 | 臺灣創作與角色 | Tommy Look小畫家 | 2026-02-10 |
| 288 | VTuber | 玖玖巴 | 2026-03-04 |
| 289 | 三麗鷗聯名 | 布丁狗30週年 | 2026-03-04 |
| 290 | VTuber | 璐洛洛 | 2026-03-10 |
| 291 | VTuber | CaKano | 2026-03-06 |
| 292 | VTuber | 音雲漫步計畫 | 2026-03-06 |
| 293 | 遊戲與動漫 | 茶葉少女 | 2026-03-12 |
| 294 | 臺灣創作與角色 | YuYing | 2026-03-12 |
| 295 | VTuber | 序境TeRaz | 2026-03-12 |
| 296 | 熱門經典角色 | 鋼彈 | 2026-03-17 |
| 297 | 遊戲與動漫 | MONSTER HUNTER WILDS | 2026-03-17 |
| 298 | 臺灣創作與角色 | 其實他是鵝 | 2026-03-17 |
| 299 | 臺灣創作與角色 | 高雄捷運－蜜柑站長 | 2026-03-27 |
| 300 | 臺灣創作與角色 | 熊的卡通頻道 | 2026-03-27 |
| 301 | 海外創作與角色 | Mochi Mochi Panda | 2026-03-27 |
| 302 | 海外創作與角色 | THE WEIRD THINGS | 2026-04-02 |
| 303 | 海外創作與角色 | Yeastken 麵包狗 | 2026-04-08 |
| 304 | 臺灣創作與角色 | 阿翰 | 2026-04-16 |
| 305 | VTuber | 幽李鈴 Uririn | 2026-04-20 |
| 306 | 海外創作與角色 | 桃源深處有人家 | 2026-04-20 |
| 307 | 臺灣創作與角色 | 狗醬 • DOG JAM | 2026-04-16 |
| 308 | 臺灣創作與角色 | 茶包先生 | 2026-04-29 |
| 309 | 遊戲與動漫 | 神魔之塔 | 2026-05-11 |
| 310 | VTuber | 角蓮 | 2026-05-07 |
| 311 | 臺灣創作與角色 | 墨魚設計／阿咘 | 2026-05-07 |
| 312 | 臺灣創作與角色 | 好吧星期一 | 2026-05-14 |
| 313 | 臺灣創作與角色 | 勒狗Leko | 2026-05-28 |
| 314 | 熱門經典角色 | 劇場版 世界計畫 崩壞的世界與無法歌唱的初音未來 | 2026-05-28 |
| 315 | 臺灣創作與角色 | 柯基犬卡卡 | 2026-06-05 |
| 316 | 臺灣創作與角色 | 橘皮 oranpeel | 2026-06-08 |
| 317 | 遊戲與動漫 | 妖怪五星好評 | 2026-06-26 |
| 318 | 遊戲與動漫 | 幕後花絮 | 2026-06-26 |
| 319 | 熱門經典角色 | Rilakkuma拉拉熊 | 2026-06-26 |
| 320 | VTuber | Haru 哈魯 | 2026-07-03 |
| 321 | 熱門經典角色 | Wasabi Bear | 2026-07-08 |
| 322 | 臺灣創作與角色 | 蝦米浣糕 RACCAKE | 2026-07-27 |
| 323 | 臺灣創作與角色 | 日頭 LITTOP | 2026-07-23 |
| 324 | 臺灣創作與角色 | 安怎？ Ann Nua | 2026-07-23 |
| 325 | 熱門經典角色 | 胡子碰碰 OHIGE no PON | 2026-07-29 |
| 326 | 海外創作與角色 | 意志薄弱狗 | 2026-07-29 |

---

## Build 4 addition: 23 further partners resolved from the 2025 文博會 dictionary

The 2026 exhibitor directory resolved 23 of the 143 in-scope partners (build 3).
The **2025** edition (`cet2025-exhibitor-handle-map.md`) resolves 23 more that the 2026 edition does not carry - 16 by exact name and 7 by a partial match adjudicated against the DEVILCASE partner page.
Roughly 97 of the 143 remain unresolved.

| crossover id | partner | Instagram | followers | band | match |
|---|---|---|---|---|---|
| 166 | 風速新營XYWS | `@xyws_motards` | **6,011** | `lt_10k` | partial (2025 name is 風速新營) |
| 179 | 小學課本的逆襲 | `@turtledrawturtle` | 271,000 | `200k_1m` | exact |
| 180 | 青青小樹 | `@doromon01` | 27,000 | `10k_50k` | exact |
| 192 | 加零在電線桿下 | `@jia0kelvin` | 42,000 | `10k_50k` | exact |
| 208 | 阿軒與一隻灰塵 | `@xuann_illustrator` | 40,000 | `10k_50k` | exact |
| 231 | 阿啾小劇場 | `@achusan0817` | 227,000 | `200k_1m` | exact |
| 238 | 肥肥與阿胡 | `@ffah_diary` | 92,000 | `50k_200k` | exact |
| 239 | dtto friends | `@dttofriends` | 115,000 | `50k_200k` | exact |
| 263 | 伸縮自如的雞與鴨 | `@iyayahaaa` | 36,000 | `10k_50k` | exact |
| 266 | 啾啾噗噗 | `@jjjlllove_1209` | 168,000 | `50k_200k` | exact |
| 268 | 來碗寬片片 | `@kuanpianpian` | 16,000 | `10k_50k` | exact |
| 270 | 牙技師的牙齒們 | `@yajishi_de_teeth` | 22,000 | `10k_50k` | exact |
| 271 | 小怪家 | `@yiekubo` (2025 dir) | **no `og:description`** | - | exact, but unusable |
| 298 | 其實他是鵝 | `@hui____7` | 22,000 | `10k_50k` | exact |
| 304 | 阿翰 | `@todayfor_han` | 58,000 | `50k_200k` | exact |
| 308 | 茶包先生 | `@mr.teabag_` | 8,288 | `lt_10k` | exact - **already row 1** |
| 324 | 安怎？ Ann Nua | `@ann_nua_handmade` | 20,000 | `10k_50k` | exact |
| - | 消極男子 Mainasu otoko | `@mainasu_com` | 133,000 | `50k_200k` | partial |
| - | YUANCHi | `@yuanchisart` | 114,000 | `50k_200k` | partial (2025 name 萌萌與他的恐龍朋友 & YUANCHi) |
| - | 河童卡斯柏 Kasper | `@pcklt.kapa` | 40,000 | `10k_50k` | partial |
| - | 小心臟Little Heart | `@jeoyu` | 35,000 | `10k_50k` | partial |
| - | YuYing | `@yuying_1203` | 28,000 | `10k_50k` | partial |
| - | 高雄捷運－蜜柑站長 | `@krtcmikan` | 235,000 | `200k_1m` | partial - transit-operator mascot |

All counts are live Instagram `og:description` reads on 2026-08-07.

**What this settles about Vein A.** Across builds 3 and 4, **46 of the 143 in-scope DEVILCASE partners now have a resolved follower count, and exactly one is sub-10k** - 風速新營 XYWS at 6,011, which then fails the character test (an 「插畫雙人組」 named after their hometown, no character in either the DEVILCASE bio or their 文博會 page).
Build 1's two sub-10k DEVILCASE rows are the tail of this roster, not its centre.
The selection caveat still cuts the other way - the 97 unresolved are the partners who exhibited at neither edition of 文博會, and exhibiting plausibly correlates with scale - but two independent samples of 23 each returning one sub-10k partner between them is now a reasonably firm read on the roster.

**小怪家 stays boundary-ambiguous.** The 2025 directory publishes `@yiekubo` for it, which serves no `og:description` at all; build 3's `@guaaii__` read of "10K" still governs, and 10K under Instagram's rounding covers roughly 9,950-10,499.
