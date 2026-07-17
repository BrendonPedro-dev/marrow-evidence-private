# Reframe sub-question 5: MEASUREMENT ASYMMETRY - is short-term collab revenue measurable while long-term awareness is not?

**The question (from the stress-test brief):** is short-term collab revenue actually measurable today (limited editions, campaign SKUs) while long-term awareness is not?
If revenue is measurable and brands still cannot attribute (our prior finding `problem-attribution-failure.md`), reconcile: what exactly can they not measure - incrementality? repeat purchase? halo?

**Compiled:** 2026-07-18 (iteration 8 of the reframe run).
Every NEW quote below was verified verbatim against page source via curl grep on raw HTML; reused instances carry their original verification status.

**Verdict: SUPPORTS the asymmetry at medium-high confidence, with a specific reconciliation.**
GROSS campaign-SKU revenue is not just measurable - it is measured to the cup, on day one, and publicly bragged about (瑞幸's official 战报, 全家's per-SKU annual figures, 萊爾富's per-campaign figures).
What no source shows any brand measuring is four layers above gross revenue: INCREMENTALITY (would these customers have bought anyway; are they new), REPEAT PURCHASE (does anyone come back after the campaign), HALO (long-horizon brand effect, which outruns the ~30-day attribution windows marketing analytics actually support), and even the MEANING of the measured revenue (when consumers buy the collab for the merch and discard the product, the SKU number overstates product adoption).
The reconciliation with H1: the internal business case ("spend this, make that") is buildable ex post ONLY at the gross-revenue level - which is precisely why revenue is the one defensible frame (see `reframe-3-internal-business-case.md`) and why awareness goals need either a famous-brand budget or a converted proxy KPI (see the 合作金庫 counter-nuance below).

---

## The measurable side: campaign-SKU revenue exists at day-one, per-SKU precision

### 1. 瑞幸 official sales bulletin (酱香拿铁): single-SKU, first-day revenue published to the hundred-million yuan

- **URL:** https://m.21jingji.com/article/20230907/herald/d331c688c9c1ff32986249a3692b0a9f.html (21财经/21经济网, 2023-09-07, 《分析｜"酱香拿铁"单日破亿，现象级联名爆款能否复制？》)
- **Who:** 瑞幸咖啡 official Weibo bulletin, relayed by 21财经 - BRAND-side official publication.
- **Quote:** 「9月5日，瑞幸咖啡官方微博发布“酱香拿铁”销售数据，美酒加咖啡的搭配刷新了单品纪录，首日销量突破542万杯，单品首日销售额突破1亿元。」
  (Gloss: on Sep 5 Luckin's official Weibo published the sales data for the Moutai latte - a single-SKU record, first-day volume over 5.42M cups, first-day single-SKU revenue over 100M yuan.)
- **Verification:** curl grep on raw HTML returned the exact string.
- **Reading:** the strongest possible existence proof for the measurable half of the asymmetry.
  A collab campaign SKU is a discrete product with its own till code, so its gross revenue is known by the next morning - so precisely that publishing a same-week 战报 (victory bulletin) is standard practice.
  Note what the bulletin does NOT contain: nothing about new-vs-existing customers, repeat purchase, or effect on either brand.

### 2. 中央社 via 商周: Taiwan convenience chains track collab revenue per SKU, per campaign, per shelf (zh-TW)

- **URL:** https://www.businessweekly.com.tw/business/blog/3018265 (商業周刊 repost of 中央社, 《超商鮮食曾是配角、如今撐起3成營收！全家一款聯名炒飯賣破億元》)
- **Who:** spokesperson statements from 統一超 (7-11), 全家 (FamilyMart), and 萊爾富 (Hi-Life), relayed by 中央社 - BRAND-side relayed corporate voices, zh-TW.
- **Quote 1 (全家, per-SKU annual revenue):** 「比如全家與名店鼎泰豐合作，運用其醬料延伸開發出烤飯糰、炒麵等商品，其中「香辣醬蒜味香腸蛋炒飯」為年銷破億元明星品項。」
  (Gloss: FamilyMart's Din Tai Fung collab fried rice is a star item selling over NT$100M a year - revenue known at the single-SKU level.)
- **Quote 2 (全家, per-campaign revenue):** 「與王品集團旗下麻辣鍋品牌2023年首次合作，推出多款現烤美食及冷凍袋裝小吃，合作3個月即創下5000萬元業績」
  (Gloss: the first Wowprime spicy-hotpot collab hit NT$50M in its first three months.)
- **Quote 3 (萊爾富, per-campaign and per-shelf):** 「每檔銷售業績都挹注千萬元營收，帶動貨架業績成長2成以上。」
  (Gloss: every collab wave contributes NT$10M-level revenue and lifts shelf-section sales by over 20%.)
- **Verification:** all three strings curl-verified in the raw HTML articleBody.
- **Reading:** zh-TW retail measures collab revenue at three granularities (SKU-year, campaign, shelf).
  The asymmetry lives INSIDE this same article: 萊爾富 also claims the collabs 「網羅平常不會進便利商店購買鮮食的客群」 (net customers who normally never buy fresh food at a convenience store) - a new-customer claim stated with zero numbers, in the same paragraph where revenue is quantified to the campaign.
  Flag: these are success-PR statements to a wire service; failed campaigns get no bulletin, so the public record of "measurable revenue" is survivorship-filtered.

### 3. Store-level lift is visible to the operator's naked eye (reused)

- **From `reframe-4-segment-split.md` instance 1 (21jingji 2024-10-25, curl-verified):** a tea-chain franchisee: 「IP联名是我们最欢迎的活动，对销量的带动很直接。」
  (Gloss: collabs are the activity we welcome most - the sales lift is direct.)
- **Reading for THIS sub-question:** at the smallest P&L unit, short-term lift is not even a measurement problem - it is same-store sales during campaign week, visible without any analytics.

## The unmeasurable side: what no brand in the record can show

### 4. 刀客Doc via 钛媒体: attribution windows top out at ~30 days while brand effects run in quarters or years (reused)

- **From `reframe-3-internal-business-case.md` instance 2 (https://www.tmtpost.com/7632802.html, curl-verified):** relayed 甲方 complaint: 「很多营销campaign的效果归因，周期最多也就30天，而品牌的作用时间可能以季度甚至年度为单位。」 plus 「很多品牌预算最后连曝光数据都很难对账。」
- **Reading for THIS sub-question:** this is the mechanism of the asymmetry, stated with a number.
  The measurement toolkit brands actually run supports a ~30-day window; a campaign SKU's revenue completes inside that window, halo does not.
  Even the exposure side often cannot be reconciled, so awareness is doubly unprovable: wrong time-scale AND unauditable inputs.

### 5. 薇琪徐 (TheNewsLens, zh-TW): promo spend is quantifiable, awareness spend has a time-lag problem (reused)

- **From `reframe-3-internal-business-case.md` instance 5 (https://www.thenewslens.com/article/129149, curl-verified):** 「因為顧客被促銷活動和舉辦活動所吸引而購買產品，所以這些花費都可以被量化。但打造品牌知名度的行銷廣告或者是宣傳行為，常常存在時間差的問題，到底要如何量化他的產值呢 ?」
- **Reading:** the zh-TW practitioner statement of the same asymmetry in general marketing terms: demand-generation spend quantifies, awareness spend does not because the effect arrives after the measurement window closes.

### 6. 雷报Pro (2026): even the biggest IP cannot be shown to drive repeat purchase

- **URL:** https://news.qq.com/rain/a/20260702A09YZD00 (腾讯新闻 mirror of 公众号 雷报, 2026-07-02, 《半年103场IP联名，休闲餐饮品牌的联名战争越"卷"越焦虑？》, author 呋辛酯, editor 努尔哈哈赤)
- **Who:** 雷报, IP-industry trade media - MEDIA voice.
- **Quote:** 「品牌必须清醒认识到，IP联名不是流量叠加的捷径，而是基于情感认同的促销协同——其真正目标不是制造“不得不买”的短期冲动，而是让消费者在消费过程中获得实用、情感、社交等多重价值的叠加满足。做不到这一点，再大的IP也撑不起复购。」
  (Gloss: brands must recognize a collab is not a traffic shortcut but promo-synergy built on emotional identification; its real goal is not manufacturing a must-buy short-term impulse - and absent that, even the biggest IP cannot sustain repeat purchase.)
- **Verification:** curl grep on the raw page returned the full string.
- **Reading:** the trade press's own framing concedes the default collab outcome is a short-term impulse spike, with repeat purchase the thing that usually fails to materialize - and no source in this entire run publishes a collab repeat-purchase number, in either direction.

### 7. Exposure counts exist, value attribution does not; spend is measurable, brand effect can be measurably NEGATIVE (reused)

- **From `problem-attribution-failure.md` instance 2 (深响 via CBNData, 2025-02):** 「如何评估联名的价值，更有待给出“曝光量”之外的标准。」 (evaluating a collab's value still awaits any standard beyond exposure volume).
- **From `problem-attribution-failure.md` instance 3 (雷报 via 36kr, 2025-07):** mid-tier brands 「未必有头部品牌那样直观的销售额回报」, and the section heading 「上亿成本挡不住品牌指数骤降40%，联名是不是“赔钱赚吆喝”？」 (hundred-million-yuan costs could not stop a 40% brand-index plunge).
- **From `problem-attribution-failure.md` instance 5 (IMC Licensing, en, agency voice, weak):** "no one has yet come up with a way to isolate and measure the impact" of licensing's brand-building benefits.
- **Reading for THIS sub-question:** costs and exposure are countable, the value standard is missing, and where a brand-health metric does exist (品牌指数) it can move DOWN while collab spend goes up - the perception side of the ledger is not merely unmeasured but occasionally measured against you.

### 8. The measured revenue itself can be a lying number: merch contamination (reused)

- **From `problem-brand-erasure.md` instance 2 (刺猬公社 via 数英, 2023-07, curl-verified):** in 茶百道's hit collab, fans 「会要求店家分开打包」 (asked for the tea packed separately from the merch), resold complete merch sets at 「几乎和原套餐等价」 (nearly the full set price), and organized 代喝 proxy-drinking so the tea never reached the buyer.
- **Reading for THIS sub-question:** the campaign's gross revenue was real and countable, but part of it was merch demand wearing a beverage SKU as a wrapper.
  So even the ONE number brands can produce overstates product adoption and says nothing about whether the brand acquired a customer or merely operated a merch distribution point (the IP's fans bought the IP, not the tea).

## Counter-nuance: perception goals CAN be made measurable when a brand defines a proxy

- **From `reframe-1-stated-goals.md` instance 3 (合作金庫, 自由時報 2018, curl-verified):** the bank set a demographic KPI for its 卡娜赫拉 co-branded card: 「目前合庫銀信用卡客戶平均年齡約45歲，希望藉由此張卡，能夠把年齡拉低到35歲。」
  (Gloss: average cardholder age is ~45; the card should pull it to 35.)
- **Reading:** the asymmetry is not a law of nature - a rejuvenation goal became measurable the moment the brand converted it into a portfolio-demographics number.
  What is missing in the market is not the arithmetic but the CONVENTION: no shared, standard proxy metrics exist for collab perception goals (this is the "licensing lacks the ad industry's justification system" refinement, supported).
- **Related (from `reframe-4-segment-split.md` instance 3, 吳宗倫, zh-TW):** small-brand licensing decisions are modeled ex ante on gross margin and repeat purchase - but nothing in his essay or any other source shows the repeat-purchase half being VERIFIED ex post, consistent with the asymmetry.

---

## Tally

| Ledger side | What the record shows | Instances |
| --- | --- | --- |
| Gross campaign revenue | Measured to the cup/SKU/campaign/shelf, published same-week | 瑞幸战报, 全家 x2, 萊爾富, franchisee (5) |
| Incrementality (new vs existing) | Claimed without numbers, never measured | 萊爾富 claim, 深响 no-standard (0 measured) |
| Repeat purchase | Named as the thing collabs fail to sustain; no number published anywhere | 雷报 2026, 吳宗倫 ex-ante only (0 measured) |
| Halo / brand equity | Time-scale outruns ~30-day attribution; index can fall despite spend | 刀客Doc, 薇琪徐, 雷报 40% plunge, IMC (0 attributed) |
| Meaning of measured revenue | Merch demand contaminates the SKU number | 茶百道 separate-packaging (behavioral) |
| Perception made measurable (counter) | Possible via defined proxy KPI, but no market convention | 合作金庫 age KPI (1) |

## Not found under the queries tried

- No brand-side voice stating the reconciliation in one sentence ("we can read campaign revenue but not incrementality/repeat/halo") - the reconciliation above is assembled from separately verified pieces and flagged as our synthesis.
- No brand or platform publishing a collab NEW-CUSTOMER rate or REPEAT-PURCHASE rate, in any language searched.
  Queries tried: 联名 销量 "增量" 还是 "存量" 品牌 复盘 到底是不是新客 IP联名; 联名 爆款 短期 销量 "复购" 难 一次性 热度过后 IP联名 拉新 留存.
- A 「昙花一现...该降价的降价，该清库存的清库存」 sentence surfaced in a search-engine summary but could not be located in any fetchable source (searched the 雷报 qq mirror and the 知乎 reposts); recorded as untraceable and NOT used.
  Likewise the fragment 「导流效果下滑是必然事件」 could not be traced to a verifiable page ("导流效果下滑" 联名 品牌 IP 人群重合 增量 returned only unrelated academic and agency pages).
- The Zhihu essay 《IP 联名新观察：从"流量狂欢"到"价值深耕"》 (zhuanlan.zhihu.com/p/1969734500088017411) is JS-rendered and was left unverified; its themes duplicate instance 6, so nothing was lost.
- zh-TW yielded no practitioner voice on collab attribution specifically (consistent with two prior runs); the zh-TW contribution here is the measurable-side precision (instance 2) plus the reused 薇琪徐 general-marketing asymmetry.

## Queries tried this pass

- zh-CN: 瑞幸 茅台 酱香拿铁 单品 首日 销售额 突破 1亿 官方 战报; 联名 销量 "增量" 还是 "存量" 品牌 复盘 到底是不是新客 IP联名; 联名 爆款 短期 销量 "复购" 难 一次性 热度过后 IP联名 拉新 留存; "导流效果下滑" 联名 品牌 IP 人群重合 增量; "吊着存在感" 联名 腰尾部品牌
- zh-TW: 台灣 超商 聯名 限量 "完售" 業績成長 帶動買氣 數字 一成 兩成

## Confidence line

**The asymmetry is SUPPORTED at medium-high confidence.**
The measurable half rests on brand-published, curl-verified numbers at day-one/SKU precision in both zh-CN and zh-TW (five instances); the unmeasurable half rests on one relayed brand-side mechanism quote with a number (30-day windows), one zh-TW practitioner statement, and three media/agency voices, with zero counter-examples found (no brand anywhere publishing incrementality, repeat, or halo numbers for a collab).
What keeps it from HIGH: the unmeasurable half still has no first-person named brand voice, the measurable half is survivorship-filtered PR, and the four-layer reconciliation is our assembly rather than any source's own statement.
**Implication for H1 and the product:** revenue is not what brands uniquely CARE about - it is what they can uniquely PROVE inside a 30-day window, so the stated goal collapses toward the only number that exists; a product that makes incrementality, repeat purchase, or a perception proxy (合作金庫-style) auditable would widen what a marketing manager is ALLOWED to want.
