# Reframe sub-question 4: SEGMENT SPLIT - does revenue-vs-awareness weighting differ by brand size or fame?

**Hypothesis under test:** our interview brand (KFT) was little-known and wanted revenue; reframe-1/2 predicted that fame decides whether a brand buys conversion or perception.
Any structure here changes who our first customer should be.

**Compiled:** 2026-07-18 (stress-test run, iteration 7).
Every quote below was verified verbatim against the raw page source (curl grep) unless flagged otherwise; AI page summaries alone were not trusted.

**Verdict: SUPPORTS a segment split at medium-high confidence, with a refinement - the boundary is not fame alone but TWO overlapping variables: brand fame AND the seat that owns the collab P&L.**
Every non-revenue goal voice on file (six brands) is a household-name or heritage brand, and every small-operator voice found frames the collab as an investment that must pay back: direct sales lift (茶饮加盟商), guaranteed sales (茶饮市场人员), break-even math on the licensing fee (王永昌), gross-margin recovery via repeat purchase (吳宗倫), renewal decided on last collab's sales (沐月).
The seat variable explains the residue fame cannot: within the same hand-shake-tea industry, the chain CEO talks mindshare while a franchisee talks direct sales lift, and famous 台灣高鐵 still runs collab merch on a NT$100M revenue target because merch is its own P&L line.
Closer to the P&L, the more the collab is judged on money; higher up the brand ladder (and the org chart), the more it is judged on perception.

---

## New instances (this iteration)

### 1. 某茶饮加盟商: collabs are our favorite activity because the sales lift is direct

- **URL:** https://www.21jingji.com/article/20241025/herald/539168d45cf2ff0a8b06bf1302073d49.html (21经济网, 2024-10-25, 《品牌"IP"授权生意，机会大于挑战？》)
- **Who:** unnamed tea-chain franchisee - OPERATOR-side first-person (the smallest P&L unit in the industry), anonymous, relayed by the reporter.
- **Quote:** 「IP联名是我们最欢迎的活动，对销量的带动很直接。」...「但我们每次也需要去做新的培训，学习一些联名IP的知识，负责点单的店员要背新的话术等。」
  (Gloss: "IP collabs are the activity we welcome most - the sales lift is direct," though each one costs the store new training and new counter scripts.)
- **Verification:** curl grep on raw HTML returned the exact strings.
- **Reading:** the purest small-operator revenue voice on file, and the sharpest within-industry contrast: 清心福全's CEO (see `reframe-1-stated-goals.md` instance 2) judges collabs on buzz and mindshare, while the franchise floor judges them on same-store sales.
  Same industry, different seat, different answer.

### 2. 现制茶饮企业市场工作人员: we pick IPs with loyal fanbases because sales are guaranteed

- **URL:** same 21jingji article as instance 1.
- **Who:** unnamed marketing staffer at a made-to-order tea company - BRAND-side first-person, anonymous.
- **Quote:** 「好的IP合作，应该是四两拨千斤的。我们倾向于一些有忠实粉丝基础的IP，销量有保障，最好粉丝还是年轻人，可以更好转化为我们品牌的受众。」
  (Gloss: a good IP collab should move a lot with a little; we lean toward IPs with loyal fanbases because sales are guaranteed, ideally young fans who convert into our brand's audience.)
- **Verification:** curl grep on raw HTML returned the exact string.
- **Reading:** sales named FIRST and audience conversion second, from a mid-level marketer at a (likely mid-tier) tea brand.
  Also restates the blame-proof selection logic from `reframe-3-internal-business-case.md`: the loyal-fanbase IP is the choice whose sales you do not have to defend.

### 3. 吳宗倫 Louis Wu (FMCG brand manager, zh-TW): for small brands the licensing decision is a gross-margin and repeat-purchase calculation

- **URL:** https://www.thenewslens.com/article/127274 (關鍵評論網, 2019-11-12, 《小品牌也能玩國際級IP授權》, credited repost of the author's Medium essay)
- **Who:** 吳宗倫 Louis Wu, Taiwan FMCG 品牌經理人 writing from first-hand licensing experience - PRACTITIONER first-person, zh-TW.
- **Quote 1:** 「對小品牌來說，如果產品單價高，品質好，回購率高，忠誠度高，而且做授權能吸引許多新客戶，雖然做授權短期會傷害毛利，但長期對生意很有幫助。」
  (Gloss: for a small brand, licensing hurts gross margin short-term and only pays if unit price, quality, repeat purchase, and loyalty are high enough that the new customers it attracts compound.)
- **Quote 2 (structural barrier):** 「你的生產數量一定要夠大，至少上萬，才比較有機會談、並且做大，而代理商通常會有最低門檻的限制，才能啟動專案」
  (Gloss: your production run must be at least ten thousand units to even get a conversation, and agencies impose minimum thresholds before a project starts.)
- **Verification:** both strings curl-verified in raw HTML.
- **Reading:** a small-brand practitioner walks through the collab decision entirely in P&L terms (margin damage, payback via repeat purchase, minimum volumes); brand image appears nowhere in the calculus.
  This is H1's "will this make us money" question stated as a working method, not a slogan.

### 4. 王永昌 (台灣希爾拓博, small importer, zh-TW): the Disney quote ended at a NT$15M break-even, so he walked away

- **URL:** https://www.ieatpe.org.tw/magazine/ebook347/storypage03.html (台北市進出口商業同業公會《貿易》雜誌 347期, 2020, 撰文 葉惟禎)
- **Who:** 王永昌, founder of 台灣希爾拓博 (party-goods importer) - SMALL-BRAND-side, reporter-relayed with one direct quote.
- **Relayed account:** 「王永昌試算後發現，若要把這些圖像使用所有派對商品上，光是前期營業額就須達1,500萬元才能持平，對甫創業的他而言，風險與負擔實在太大。」
  (Gloss: his math showed he would need NT$15M in up-front revenue just to break even on Disney's per-SKU licensing fees - too much risk for a young company, so he gave up and bought from licensed distributors instead.)
- **Direct quote:** 「畢竟即使有圖像IP，後續商品還要行銷推廣，更何況不是只給一次性授權金就好。」
  (Gloss: even with the IP secured, you still must fund the marketing behind the product, and the fee is not a one-time payment.)
- **Article's framing sentence (author voice):** 「圖像IP或許是門好生意，然而過高的授權金，往往是中小企業卻步的主因。」
  (Gloss: excessive licensing fees are the main reason SMEs back away.)
- **Verification:** all three strings curl-verified in raw HTML.
- **Reading:** the small-brand collab decision is literally a break-even spreadsheet.
  Bonus structural note from the same article: 「國際知名IP大廠如迪士尼已不需特別塑造品牌形象，而是著重於大而穩定的客戶，以授權金價格做出市場區隔」 - the fame logic runs on the IP side too; famous IPs no longer need exposure and price small buyers out.

### 5. 沐月 renewal decision (relayed by agency): the second collab happened because the first one sold

- **URL:** same 貿易雜誌 article as instance 4.
- **Who:** 顏銘錫, 聯合數位文創數位事業群IP授權暨商品發展部經紀中心經理, recounting his licensee 沐月 (Taiwan drinks maker) - AGENCY-side relay of brand behavior. Flag: vendor voice, ranked below first-person brand voices.
- **Quote:** 「第一次的合作也為沐月創造不錯的銷售成績，而決定進行第二波的授權......即使聯合後來開的授權金較高，沐月還是決定繼續合作。只要圖像與產品TA相符，對自家的產品推廣有幫助，即使必須支付較高的授權金，從投資報酬率來看仍存在商機。」
  (Gloss: the first collab produced good sales, so 沐月 committed to a second wave and accepted a higher fee, because on an ROI view the business case still held.)
- **Verification:** curl grep on raw HTML returned the string.
- **Reading:** a small brand's renew/no-renew decision hinged on observed sales and ROI - revenue is not just the stated goal but the operating decision rule.

### 6. 花仙子 x 馬來貘 (third-party narration): the Taiwan heritage brand in the story collabs for young-audience reach, on cue

- **URL:** same 貿易雜誌 article as instance 4.
- **Who:** article narration about 花仙子 (established Taiwan household-chemicals brand, second-generation succession) - THIRD-PARTY, no first-person brand quote.
- **Quote:** 「如家庭日用化學品老牌大廠花仙子在二代接班後，面對國內已趨飽和的打掃工具類市場......為拓展年輕客群，跨界與插畫家馬來貘合作推出聯名商品，果然大受歡迎。」
  (Gloss: facing a saturated cleaning-tools market, the heritage brand collabed with illustrator Cherng to expand into young customer segments.)
- **Verification:** curl grep on raw HTML returned the string.
- **Reading:** even inside a single article, the pattern holds: the established brand's goal is audience rejuvenation, the startups' goal is unit economics.

## Instances already on file (reused, not re-found)

The fame gradient assembled from prior findings:

- **Famous/heritage, perception goals:** 大白兔 (rejuvenation as SOLE goal), 茅台 (strategic above commercial), 名创优品 CMO (image refresh ranked 第一目标), 合作金庫 (「我們不會只是拚卡量！」), 清心福全 (buzz and 心佔率), 旺旺 (mixed, brand-equity frame). See `reframe-1-stated-goals.md` and `reframe-2-nonrevenue-goals.md`.
- **Mid-size, mixed:** 兔头妈妈 (销量和曝光 as assumed baseline plus mission goal). See `reframe-1-stated-goals.md` instance 5.
- **Famous but merch-P&L seat, revenue goal:** 台灣高鐵 (NT$100M revenue target). See `reframe-1-stated-goals.md` instance 4 - the case that breaks pure-fame segmentation and motivates the P&L-seat variable.
- **Mid-tier brands quitting when sales do not show:** 雷报/36kr documentation that mid-tier brands pause collabs when no visible sales return appears (喜茶 37 collabs to 0). See `problem-attribution-failure.md`.
  Reading for this sub-question: mid-tier brands behave like revenue buyers in exit decisions even when their entry rhetoric is mixed.
- **KFT interview (internal, n=1):** the little-known brand whose one question was revenue - the anchor observation this sub-question tests.

---

## Tally

| Segment | Stated collab frame | Instances |
| --- | --- | --- |
| Famous/heritage brand, brand-marketing seat | Perception (rejuvenation, image, mindshare) | 6 on file (all zh-CN/zh-TW famous names) + 花仙子 (third-party) |
| Famous brand, merchandising P&L seat | Revenue target | 1 (台灣高鐵) |
| Mid-size brand | Mixed, sales as baseline; revenue decides exit | 兔头妈妈, 现制茶饮市场人员, 雷报 mid-tier exits |
| Small brand / operator / franchisee | Revenue, break-even, margin payback | 4 new (加盟商, 吳宗倫, 王永昌, 沐月-relayed) + KFT |
| Small brand stating a perception goal | - | 0 found |

## Not found under the queries tried

- No survey or whitepaper cross-tabbing collab GOALS by brand size or fame; the segment claim rests on assembled instances, not a distribution.
  Queries tried: 大品牌 联名 品牌形象 小品牌 联名 销量 区别 "对于大品牌" OR "对于小品牌" OR "头部品牌" IP联名 目的不同; 中小品牌 IP联名 目的 销量 带货 "小品牌" 联名 为了; 新消费品牌 联名 目的 "拉动销量" OR "带动销售" 创始人 采访 IP授权.
- A Zhihu answer claiming SMEs should pick 腰部/垂直 IPs for 预算低、门槛低、转化高 could not be curl-verified (JS-rendered); recorded as an unverified lead only (https://www.zhihu.com/question/484280067/answer/2020911986762889070).
- Flag on source independence: 吳宗倫's 2019 essay and the 2020 貿易雜誌 passage share near-identical small-brand phrasing (回購率/短期傷害利潤), so the magazine likely drew on the same author or a common source; the 王永昌 and 沐月 cases in the magazine are independent of Wu.

## Implication for the problem statement and the first customer

The segment structure is real and two-dimensional: fame sets whether a brand CAN afford perception goals, and the seat owning the P&L sets whether anyone in the room is allowed to think that way.
Small brands, franchisees, and merch-line operators all speak in break-even math, and no small brand anywhere in the record states a perception goal, so H1 is approximately TRUE for the small/operator segment and approximately FALSE for the famous-brand marketing seat.
For the pitch, that means our KFT interview generalizes to a definable customer: brands and operators for whom the collab itself must pay - little-known brands, franchise systems, category traders, and merch P&L owners - and 王永昌's abandoned Disney deal shows this segment is today PRICED OUT or flying blind, deciding on a spreadsheet with no evidence base (which `problem-gut-feel-selection.md` and the class-pricing idea in the afternoon refinements speak to directly).
The famous-brand marketing seat is a different product conversation: they buy perception on purpose but need the blame-proof case documented in `reframe-3-internal-business-case.md`.
