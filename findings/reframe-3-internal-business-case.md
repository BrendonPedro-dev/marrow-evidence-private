# Reframe sub-question 3: THE INTERNAL BUSINESS CASE - do marketing teams struggle to justify collab spend upward?

**Hypothesis under attack (H1, brand side):** the real buyer is the marketing manager who must build the internal business case ("spend this, make that") to convince their boss.
This file hunts evidence of that upward-justification pain: CMO pressure to prove ROI, budget-approval friction, and 效果不好交代 / 向老板证明 type language, plus the "brownie points" buyer persona in first person.

**Compiled:** 2026-07-18 (stress-test run, iteration 6).
Every quote below was verified verbatim against the raw page source (curl grep) unless flagged otherwise; AI page summaries alone were not trusted.

**Verdict: SUPPORTS the internal-business-case half of H1 (medium-high for marketing spend generally, medium for collabs specifically).**
The upward-justification pain is loudly documented in both zh-CN and zh-TW practitioner voices, including the exact 交代 language the hypothesis predicts (a relayed FMCG CMO: 「年底复盘根本交代不过去」).
The structural context is strong: 2024-2025 China saw brand departments cut, merged, or re-KPI'd onto conversion metrics precisely because they could not prove sales contribution, and Xiaohongshu built an entire ad campaign around this boss-pain, which is market-level evidence that the pain is common enough to sell against.
Two honest gaps keep this at medium for collabs specifically: most justification-pain voices are about marketing/brand budgets in general rather than 联名 line items, and the "brownie points" persona (doing a collab to look good upward) was not found in first person anywhere.
What was found instead is the defensive version of that persona: marketers pick big-fanbase IPs because facing a marketing KPI, a famous IP is the choice you cannot be blamed for.

---

## Practitioner and relayed brand-side instances (new)

### 1. Relayed FMCG CMO via 姜茶茶: boss watches ROI, every yuan must make a sound, and the year-end review is impossible to account for

- **URL:** https://www.digitaling.com/articles/1442566.html (数英, 2025-12-19, 《年底了，老板们的"痛"被小红书看透了？》)
- **Who:** 姜茶茶 (advertising-industry KOL, ex-agency) relaying conversations with anonymous brand-side CMOs - RELAYED first-person, anonymous.
  **Flag: the article is an advertorial for Xiaohongshu's C种草O campaign**, so the pain framing serves a platform pitch.
- **Quote 1 (relayed 快消品 CMO):** 「手下团队总说他抠，预算批得慢、卡得严。可老板盯着roi，每一分钱花出去都得听个响。账上也不是没钱，但得花在刀刃上，花得不高效，年底复盘根本交代不过去。」
  (Gloss: his team calls him stingy, approvals slow and tight - but the boss watches ROI, every yuan spent must make a sound, and if spend is inefficient the year-end review simply cannot be accounted for upward.)
- **Quote 2 (the author, herself a marketer):** 「毕竟作为花钱的部门，如果不能证明自己的价值，都快成销售的编外部门了。」
  (Gloss: as the spending department, if marketing cannot prove its value it is nearly demoted to sales' adjunct.)
- **Quote 3 (relayed anonymous 甲方):** 「之前有个甲方跟我说，不仅每年营销预算砍30%，甚至还被要求KPI。」
  (Gloss: a brand-side contact said the marketing budget is cut 30% every year while KPIs are still demanded.)
- **Quote 4 (author narration):** 「每一笔钱背后，都藏着老板的ROI预期、销售的转化焦虑、团队的执行惯性。」
  (Gloss: behind every sum hides the boss's ROI expectation, sales' conversion anxiety, the team's execution inertia.)
- **Verification:** all four strings curl-verified in raw HTML.
- **Reading:** this is the closest published artifact to H1's buyer persona: a marketing leader whose daily problem is making spend defensible to the person above.
  The meta-fact matters as much as the quotes: **Xiaohongshu spent a campaign marketing AT this pain**, which a platform only does when the pain is widespread among its paying customers.

### 2. 刀客Doc (钛媒体): brand budgets cannot even reconcile exposure numbers, and departments that cannot show sales have a hard life

- **URL:** https://www.tmtpost.com/7632802.html (钛媒体, 2025-07-21, 《2025，大厂品牌部大撤退》, author 刀客Doc, marketing-industry columnist)
- **Who:** author relaying aggregated complaints from 甲方朋友 (brand-side contacts) plus his own analysis of named companies (京东 etc.) - RELAYED brand-side + columnist analysis.
- **Quote 1 (relayed 甲方):** 「我跟不少甲方朋友聊过，他们常常吐槽：“我们希望品牌能‘带销量’，但现实是很多品牌预算最后连曝光数据都很难对账。很多营销campaign的效果归因，周期最多也就30天，而品牌的作用时间可能以季度甚至年度为单位。”」
  (Gloss: brand-side contacts complain that brand budgets often cannot even reconcile exposure data, and campaign attribution windows top out at 30 days while brand effects run in quarters or years.)
- **Quote 2 (author, on 京东):** 「无法直接带来销量增长的品牌部门自然日子难过。」
  (Gloss: under a cut-costs-at-all-costs regime, a brand department that cannot directly show sales growth naturally has a hard life.)
- **Quote 3 (author):** 「品牌部门在写OKR的时候，要服务于转化率、点击率、复购率等指标，成为增长漏斗中的一环。」
  (Gloss: brand teams now write OKRs against conversion, click-through, and repurchase metrics - reduced to one link in the growth funnel.)
- **Verification:** all three strings curl-verified in raw HTML.
- **Reading:** the organizational consequence of failing the internal business case is documented at scale: brand functions in 2025 China were dissolved into business lines or re-KPI'd onto conversion numbers.
  This is the environment H1's marketing-manager buyer lives in.

### 3. Anonymous in-house marketer (甲方市场狗, 2016): the marketing department is perpetually asked why its budget does not just buy sales

- **URL:** https://www.digitaling.com/articles/25509.html (数英, 2016-06-08, 《甲方市场狗告诉你，市场部老会被问到哪些二逼问题》)
- **Who:** anonymous in-house (brand-side) marketer writing in first person - FIRST-PERSON practitioner, anonymous.
- **Quote 1 (a question marketing keeps being asked internally):** 「市场部预算为什么不去做销量?」
  (Gloss: "why doesn't the marketing budget just go make sales volume?")
- **Quote 2 (the attribution absurdity they face):** 「预算投多了的地方销量砰砰下跌,预算投少了的地方销量蹭蹭上涨?」
  (Gloss: places with heavy budget see sales fall, places with light budget see sales surge - the correlation bosses demand does not exist.)
- **Verification:** both strings curl-verified in raw HTML.
- **Reading:** a decade-old first-person complaint showing the justify-upward dynamic long predates the 2025 budget squeeze; the pain is chronic, not cyclical.

### 4. Taiwan ad buyer (vocus): the boss's three questions, and data as the weapon to answer them

- **URL:** https://vocus.cc/article/6768ea90fd897800011daea8 (方格子 vocus, Taiwan, 《沒錢還想廣告有效？廣告投手的數據說服力全解析！》)
- **Who:** anonymous Taiwan 廣告投手 (ad buyer/media buyer) writing in first person - FIRST-PERSON practitioner (vendor-adjacent: the essay sells data literacy), zh-TW.
- **Quote 1 (the internal questions):** 「為什麼效果不好？」「錢都花去哪裡了？」「能不能不增加預算就提升成效？」
  (Gloss: why are results bad? where did the money go? can you improve results without more budget?)
- **Quote 2:** 「數據就成了你最有力的武器。本文將分享廣告投手如何用數據說服主管與品牌方，不僅拿到更多預算，還能提升廣告成效的真實案例與實用技巧！」
  (Gloss: data becomes your most powerful weapon - how an ad buyer persuades supervisors and brand clients with data to win more budget.)
- **Also on-page (section heading):** 「主管不想加預算：讓數據回應風險」 (when the supervisor will not add budget, let data answer the risk).
- **Verification:** all strings curl-verified in raw HTML.
- **Reading:** first zh-TW instance of the justification dynamic on file: the practitioner's core skill is framed as building the internal case with numbers.
  Context is ad spend, not licensing - flag accordingly.

### 5. Taiwan marketer 薇琪徐 (TheNewsLens): brand marketers are routinely challenged on ROI by the boss or the CFO

- **URL:** https://www.thenewslens.com/article/129149 (關鍵評論網, book-informed essay on 《量化行銷時代》, author 鋼鐵"V"走闖職場/薇琪徐)
- **Who:** Taiwan marketing practitioner/columnist - FIRST-PERSON practitioner commentary, zh-TW.
- **Quote:** 「做品牌行銷的應該常常被被老闆或者是財務長挑戰ROI，不像是一些「製造需求行銷」，因為顧客被促銷活動和舉辦活動所吸引而購買產品，所以這些花費都可以被量化。但打造品牌知名度的行銷廣告或者是宣傳行為，常常存在時間差的問題，到底要如何量化他的產值呢 ?」
  (Gloss: brand marketers are constantly challenged on ROI by the boss or CFO - demand-generation spend is quantifiable, but awareness-building suffers a time lag, so how do you quantify its output? Note: the doubled 被被 is in the original.)
- **Verification:** curl-verified in raw HTML.
- **Reading:** zh-TW confirmation of the asymmetry H1 rides on: promo spend can be defended with numbers, awareness spend cannot - which is exactly why a marketing manager prefers goals they can prove.

## Instances already on file (reused, not re-found)

- **茅台冰淇淋 strategic retreat (see `findings/reframe-2-nonrevenue-goals.md` instance 2):** the chairman-sponsored awareness collab was rolled back within a year of the sponsor's departure (「从曾经的高调创新到当下的战略收缩」, 21jingji, curl-verified).
  Reading for THIS sub-question: today the internal defense of a non-revenue collab is a PERSON, not a business case - when the person leaves, the program dies.
  That is the sharpest evidence that no durable justification system exists.
- **CLC 2024 roundtable agenda (see `findings/problem-attribution-failure.md` instance 1):** 「联名产品推出后，如何有效评估联名效果」 listed by the industry's own association as an unsolved licensee pain point (licensing.org.cn, curl-verified).
  If the effect cannot be evaluated, the upward case cannot be built from evidence.
- **CBNData x 应极数字 2023 report (verified verbatim during the attribution hunt, recorded in `findings/problem-attribution-failure.md`):** 「因此对于品牌来说，面对营销KPI，只能选择《魔道祖师》、《恋与制造人》等粉丝基本盘庞大的IP，寄希望上线后粉丝可以蜂拥而至。」 (https://www.thepaper.cn/newsDetail_forward_26098521)
  (Gloss: facing a marketing KPI, brands can only pick huge-fanbase IPs and hope the fans swarm in.)
  Reading: this is the DEFENSIVE form of the brownie-points persona - the safe-famous-IP choice is the one a marketing manager cannot be blamed for, which also explains the gut-feel-by-fame selection documented in `findings/problem-gut-feel-selection.md`.

---

## Tally

| Evidence type | Instances | Languages |
| --- | --- | --- |
| Boss/CFO ROI-challenge language from practitioners | 4 (姜茶茶 relays, 甲方市场狗, vocus 投手, 薇琪徐) | zh-CN + zh-TW |
| Organizational consequence (brand teams cut/re-KPI'd for unprovable value) | 1 new (刀客Doc) + context in reframe-2 (茅台) | zh-CN |
| Collab-SPECIFIC justification pain | 2 reused (CLC agenda, 应极数字 KPI-driven IP choice) + 茅台 sponsor story | zh-CN |
| First-person "brownie points" (credit-seeking) voice | 0 found | - |

## Not found under the queries tried

- No first-person marketer saying they run collabs to look good upward (the positive brownie-points persona); only the defensive variant (blame-proof IP choice) is documented.
  Queries tried: 做联名 市场部 "向上汇报" OR "汇报好看" OR "政绩" OR "自嗨" 声量 老板 满意; 联名 立项 内部 老板 问 "能带来多少" OR "凭什么" 市场部 汇报 复盘 销量.
- No collab-specific budget-approval friction story (a 联名 proposal rejected or squeezed by the boss) in either zh-CN or zh-TW.
  Queries tried: IP授权 授权费 贵 老板 不批 预算 内部 说服 决策 采购 品牌方; 奶茶 茶饮 联名 内部 提案 过会 老板拍板 市场部 负责人 讲述 决策; 台灣 行銷人 "說服老闆" 預算 成效 聯名 IP 授權 提案.
- The ZAKER piece 《字节前CMO接手3家创业公司：品牌预算砍47%后》 (search-result claim: under 4% of brand-event attendees entered the sales funnel) could not be fetched or re-found via search; recorded as an unverified lead only.
- The Medium essay (angrywriter, 品牌行銷系列) with the reported line 「所以你的成效到底是什麼？賺錢還要等多久？」 is paywalled/blocked to fetching; the quote is recorded as an unverified lead only.

## Implication for the problem statement

The internal-business-case half of H1 survives the attack and comes out stronger, but with a twist.
The documented pain is not "brands only want revenue" - it is that the marketing manager's spend must be DEFENSIBLE, and revenue is simply the only defense that reliably works in a 2024-2026 budget environment where 品效合一 has collapsed into 效 (as 刀客Doc's OKR line and the brand-department layoffs show).
The buyer persona should therefore be written as the marketing manager who needs a blame-proof case, not a profit-hungry one: today their two available defenses are picking an IP so famous nobody questions it (应极数字's KPI line, our gut-feel finding) or having a senior sponsor personally shield the bet (茅台) - and both defenses are substitutes for the measurement system that does not exist.
That framing unifies sub-questions 1-3: famous brands can afford perception goals, unknown brands must promise revenue, and BOTH lack an evidence-grade way to justify the specific collab they chose.
