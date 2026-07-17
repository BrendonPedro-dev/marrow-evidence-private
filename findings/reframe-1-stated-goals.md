# Reframe sub-question 1: DO brands state revenue as the collab goal?

**Hypothesis under attack (H1, brand side):** brands judge IP collaborations on ONE question - "will this make us money?" - and awareness is secondary or unmeasurable.

**Compiled:** 2026-07-17 (stress-test run, iteration 2; salvages and completes the interrupted iteration 1 hunt).
Every quote below was verified verbatim against the raw page source (curl grep) unless flagged otherwise; AI page summaries alone were not trusted.

**Verdict: WEAKENS H1 as a universal claim; supports a segment split.**
Of the six brand-side first-person voices found, three state awareness/image/audience-rejuvenation as the PRIMARY goal (one of them explicitly ranks it above sales with the words 第一目标), one states revenue targets, and two state mixed goals with sales treated as an assumed baseline rather than the question.
Sales lift dominates only in the industry association's licensee survey (a perceived-benefit question, not a stated-goal question).
The split lines up with brand fame: the famous brands (名创优品, 清心福全, 合作金庫) talk image and rejuvenation; the merch-revenue operator (台灣高鐵) talks revenue targets.
Honest caveat: these are PUBLIC statements by CMO-level people, and PR framing plausibly under-reports the internal money question; H1 came from a little-known brand's internal calculus, which stated-goal evidence can weaken but not directly refute.
The internal business case is sub-question 3's hunt.

---

## Brand-side first-person instances

### 1. 名创优品 CMO 刘晓彬: the FIRST goal is image refresh, not sales

- **URL:** https://www.foodaily.com/articles/36804 (Foodaily interview, 2024-06-13)
- **Who:** 刘晓彬, 名创优品集团首席营销官 - BRAND-side first-person, top-tier famous brand (the most collab-intensive retailer in China).
- **Quote:** 「第一目标是想借此刷新品牌形象和消费者认知，吸引更多垂类圈层以及大众人群的关注。」
  (Gloss: "The first goal is to use it to refresh our brand image and consumer perception, and attract attention from more niche circles and the mass public.")
- **Verification:** curl grep on raw HTML returned the exact string.
- **Category: AWARENESS/IMAGE primary, explicitly ranked first.** Directly contradicts H1's "one question" for this brand.

### 2. 清心福全 執行長 趙啟宏: licensing is a publicity channel, evaluated on buzz and mindshare

- **URL:** https://www.bnext.com.tw/article/65151/chingshin-successor-story (數位時代, Taiwan)
- **Who:** 趙啟宏, 清心福全執行長 - BRAND-side first-person, Taiwan's largest hand-shake tea chain (adjacent industry to our KFT interview brand).
- **Quote 1:** 「授權是很好的宣傳管道，可以激發不同的消費族群，當消費者家裡一角放著清心的東西，『只要他看到，就會想起我們的品牌。』」
  (Gloss: "Licensing is a great publicity channel that can activate different consumer groups - when a Chingshin item sits in a corner of the consumer's home, whenever they see it, they think of our brand.")
- **Quote 2 (partially verified):** evaluation is 「主要評估網路聲量反應，以及增加消費者的『心佔率』」.
  (Gloss: mainly evaluated on online buzz and gains in consumer "mindshare".)
  curl grep confirmed the 「心佔率」 fragment and Quote 1 in full; Quote 2's full sentence rests on the fetched-page extraction. Flag: partial raw verification.
- **Category: AWARENESS/MINDSHARE primary.** A tea chain in KFT's own category publicly judges collabs on buzz and mindshare, not revenue - the sharpest single counter-instance to generalizing our n=1 interview.

### 3. 合作金庫銀行 董事長 雷仲達: "we are not just chasing card volume" - the goal is pulling the customer base younger

- **URL:** https://ec.ltn.com.tw/article/breakingnews/2505044 (自由時報, 2018-07-31)
- **Who:** 雷仲達 (合庫金控暨合庫銀董事長) and 陳玉明 (合庫銀信用卡部協理) - BRAND-side first-person, incumbent bank licensing 卡娜赫拉 for a co-branded card.
- **Quote 1 (雷仲達):** 「我們不會只是拚卡量！」...「像這張『卡娜赫拉的小動物icash聯名卡』就是要吸引年輕族群，訴求年輕人的市場。」
  (Gloss: "We are not just chasing card volume!" - the card exists to attract the young segment.)
- **Quote 2 (陳玉明):** 「目前合庫銀信用卡客戶平均年齡約45歲，希望藉由此張卡，能夠把年齡拉低到35歲。」
  (Gloss: current average cardholder age is about 45; the hope is this card pulls it down to 35.)
- **Verification:** curl grep on raw HTML returned both strings.
- **Category: AUDIENCE REJUVENATION primary, volume explicitly disclaimed.** Note the nuance: the awareness-type goal is made MEASURABLE via a customer-age KPI, which cuts against H1's companion claim that non-revenue goals are unmeasurable.

### 4. 台灣高鐵: collab merch is a revenue business with a NT$100M target

- **URL 1:** https://www.nownews.com/news/5126251 (NOWnews, 2020-12-01)
- **URL 2:** https://www.chinatimes.com/realtimenews/20221201001990-260410 (中時, 2022-12-01)
- **Who:** 台灣高鐵公司 (corporate statements) - BRAND-side (licensee) voice on its 卡娜赫拉 program.
- **Quote (URL 1):** 「高鐵表示，與卡娜赫拉的小動物聯名獲得不少好評，周邊商品也因品牌力加乘效果，銷售成績不俗，因此加碼推出聯名食品」
  (Gloss: HSR said the collab drew praise and the merch sold well thanks to brand synergy, so they doubled down with co-branded food.)
- **Supporting figures (URL 2, fetched-page extraction, not raw-verified):** three years of the collab generated 50M+ NTD in revenue and the company is 「傾全力朝進帳1億元的目標挺進」 (pushing toward a 100M NTD revenue target - article paraphrase).
- **Verification:** URL 1 quote curl-verified; URL 2 figures rest on the fetched-page extraction. Flag accordingly.
- **Category: REVENUE primary.** The clearest H1-supporting brand voice found: a transport operator running licensing as a P&L line with revenue targets.

### 5. 兔头妈妈品牌方: sales and exposure are the assumed baseline, plus a category-education mission

- **URL:** https://www.digitaling.com/articles/1315572.html (数英/剁椒Spicy, 2025-02-10)
- **Who:** 兔头妈妈 (children's personal-care brand) representative - BRAND-side first-person, mid-size brand.
- **Quote:** 「除了销量和曝光，我们还希望能破圈传递儿童防蛀这件事，通过好玩、有趣的联名让更多人关注到防蛀这件事，也让更多孩子开始习惯性践行防蛀」
  (Gloss: "Beyond sales and exposure, we also hope to break circles and spread the children's cavity-prevention message...")
- **Verification:** curl grep on raw HTML returned the exact string.
- **Category: MIXED - 销量 named first but as an assumed baseline alongside exposure, with a mission goal stacked on top.** Neither pure-H1 nor pure-awareness.

### 6. 名创优品 品牌营销总监 龚莹: convert IP fans into consumers, build a rejuvenated brand image

- **URL:** https://www.adquan.com/article/349904 (广告门, 2025-02-13)
- **Who:** 龚莹, 名创优品品牌营销总监 - BRAND-side, though parts may be article narration rather than direct quotation. Flag: attribution boundary unclear.
- **Quote fragments (curl-verified strings):** 「将IP粉丝群体转化为品牌潜在的消费者。」 and 「频繁与潮流IP合作出新，为名创优品打造出了一个年轻化的品牌形象」.
  (Gloss: converting IP fan bases into potential consumers of the brand; frequent trend-IP collabs built MINISO a rejuvenated brand image.)
- **Same article's hard numbers:** IP products are 30%+ of sales, growing ~40% YoY, with 25%-200% price premiums.
- **Category: MIXED - conversion (revenue-flavored) and image-rejuvenation stated together.** For MINISO the "does it make money" question was answered long ago at the portfolio level, so per-collab goals shift to image.

---

## Non-brand voices (context, ranked below the above)

### 7. 小黄豚 IP方负责人 Chloe: brands collab either to push a young product line or because they are a young-audience brand

- **URL:** https://www.digitaling.com/articles/1315572.html (same article as #5)
- **Who:** Chloe, 小黄豚 IP方品牌负责人 - IP-side (licensor) voice describing brand motives, not a brand speaking about itself.
- **Quote:** 「一般品牌跟年轻人喜欢的IP做联名，要么是为了推年轻的产品线，要么它本身就是面向年轻消费群体的品牌。这次五菱宏光推的新品主要面向年轻的家庭场景，跟小黄豚的粉丝是高度一致的。」
  (Gloss: brands collab with youth-loved IPs either to push a young product line or because they already target young consumers - audience-fit framing, not revenue framing.)
- **Verification:** curl grep on raw HTML returned the exact string.

### 8. 《2025中国授权行业发展白皮书》survey: 91.4% of licensees say licensing lifted sales

- **URLs:** https://ip365x.com/news/info/17107 and https://ex.chinadaily.com.cn/exchange/partners/82/rss/channel/cn/columns/sz8srm/stories/WS67e638e2a31008317a2af1bf.html (also https://news.pedaily.cn/20250328/104473.shtml, JS-rendered)
- **Who:** 中国玩具和婴童用品协会 (China Toy & Juvenile Products Association) annual whitepaper survey of licensees - SURVEY of brand-side respondents, published by an industry association with a promotional interest. Flag: vendor-adjacent.
- **Quote:** 「91.4% 的受访被授权商认为 IP 授权带动销售提升，其中，22.7% 的受访被授权商认为 IP 授权带动销售提升一倍以上，比上年增长 5.0 个百分点。」
  (Gloss: 91.4% of surveyed licensees say IP licensing drove sales lift; 22.7% say it more than doubled sales.)
- **Verification:** exact string curl-verified on two independent outlets (ip365x, China Daily exchange).
- **Reading:** this measures perceived BENEFIT, not stated GOAL, and the near-unanimous "it lifted sales" claim sits awkwardly beside our attribution-failure finding (`problem-attribution-failure.md`) that nobody can actually measure collab effect - suggesting the 91.4% is belief, not measurement. It supports "sales is the dominant frame licensees reach for" more than it supports "sales is measurably delivered".

---

## Tally (the distribution IS the answer)

| Stated primary goal | Brand-side first-person instances |
| --- | --- |
| Awareness / image / rejuvenation | 3 (名创优品 CMO, 清心福全 CEO, 合作金庫 chairman) |
| Revenue / sales targets | 1 (台灣高鐵) |
| Mixed, sales as assumed baseline | 2 (兔头妈妈, 名创优品 龚莹) |

## Not found under the queries tried

- No brand-side voice saying the H1 sentence itself ("the only question is whether it makes us money").
  Queries tried: 喜茶 OR 奈雪 联名 负责人 专访 "我们希望" OR "联名的目的"; 瑞幸 联名 负责人 采访 目的 拉新 OR 破圈 OR 声量; 好利来 罗成 联名 采访 目的; 杨飞 瑞幸 联名 采访 目标; 名创优品 IP联名 负责人 专访 目的; "聯名" 行銷長 專訪 IP 授權 "業績" 台灣 品牌 目的 經理人; 統一超商 7-ELEVEN 表示 聯名 話題 帶動 買氣; 全家 聯名 卡娜赫拉 行銷 目的 業績; 手搖飲 聯名 角色 IP 業績成長 品牌 表示 年輕化; 銀行 聯名卡 發卡 目標 表示 年輕客群; 動腦 brain.com.tw IP聯名 品牌 行銷 經理 表示 目的.
- No survey giving a percentage BREAKDOWN of licensees' goals (sales vs awareness vs traffic vs image).
  Queries tried: 品牌 联名 目的 调研 报告 白皮书 "品牌年轻化" OR "拉新" 百分比; 中国品牌授权行业发展白皮书 被授权 企业 开展授权业务 目的 提升品牌 OR 销售 占比. The 2022 whitepaper page at clii.com.cn was unreachable (connection refused).

## Implication for the problem statement

H1's strong form ("brands judge on one question: will this make us money") is an over-generalization from n=1.
The defensible form is segmented: for brands where the collab itself is a P&L line (merch operators, little-known brands needing the collab to pay for itself), money is the stated question; for established brands, the stated question is image/rejuvenation/mindshare - and at least one (合作金庫) has made that goal measurable with a customer-demographics KPI.
What survives across ALL segments is that sales language is the default frame licensees reach for (the 91.4% survey), even though our prior attribution finding shows they cannot actually measure it - which is the real wedge for the product: not "brands only care about money" but "whatever goal brands state, the money question is the one they cannot answer with evidence".
