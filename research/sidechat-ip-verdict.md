# Sidechat IP — identity verdict with documented trail

**Seed question 1:** does any company named "Sidechat" (or similar) do AI licensing
scoring? Verdict required: exists / does not exist / conflation with [what].

**Researched:** 2026-07-15. zh-TW/zh-CN queries primary, English secondary, per task rules.

---

## Verdict

**EXISTS — but scores the wrong object.** "Sidechat IP" is a real product page from a real,
identifiable, VC-backed company (Spaceport Technologies / spaceport.xyz), and it does market
**AI scoring in licensing** — but the scoring is (a) *applicant deal-quality* triage of
inbound licensee requests and (b) *infringement-alert confidence*, *not* IP × product
pairing-fit prediction. No company under this or a similar name was found doing quantified
brand-IP **fit** scoring. The name additionally collides with two unrelated entities
(documented in §4) that a VC could conflate.

**Confidence: HIGH** on corporate identity and lineage (multiply sourced: funding PR,
company site, PR Newswire, LinkedIn/Crunchbase listings). **LOW** on the Sidechat IP
*product's* claims and traction — every product claim is vendor-stated with no independent
coverage found (flagged single-source throughout §2).

---

## 1. Corporate identity — the entity chain (multiply sourced)

The previously "UNVERIFIED / vendor-described" attribution in `consumer-product-gap.md §2h`
is now **CONFIRMED**. The chain:

- **Spaceport Technologies** (site: spaceport.xyz) — founded **Jan 2022** by **Le Zhang**
  (CEO) and Lida Tang. Raised a **$3.6M pre-seed, Dec 2022**, led by Arca, Decasonic, and
  CRIT Ventures (VC arm of Com2uS); participants incl. Cozomo De Medici, Diaspora Ventures,
  Infinity Ventures, FBG Capital, NextView Ventures, Republic Asia, Valhalla Ventures.
  (Some listings classify it as a ~$4M seed.)
  - Funding PR: https://www.spaceport.xyz/blog/web3-licensing-protocol-spaceport-closes-36m-pre-seed-round
  - Crunchbase org listing (profile fetch blocked 403; identity via search snippet):
    https://www.crunchbase.com/organization/spaceport-technologies
  - LinkedIn company: https://www.linkedin.com/company/spaceportxyz
  - Core business: IP licensing into **UGC gaming** (Roblox, Fortnite) — "Universal Catalog
    of IP," Smart Licenses. Real, independently reported partnerships: **Toei Animation**
    (https://licensinginternational.org/news/spaceport-announces-intellectual-property-licensing-partnership-with-toei-animation-to-license-content-into-roblox-and-fortnite/),
    **Com2uS Platform** (https://www.gamespress.com/Spaceport-and-Com2uS-Platform-Join-Forces-to-Unify-IP-Licensing-for-Ro),
    **Rainbow/Winx Club → Roblox** (https://toybook.com/winx-club-roblox-news/),
    **Intella X** (https://www.einpresswire.com/article/646271553/spaceport-partners-with-intella-x-to-offer-seamless-ip-licensing-for-gaming-and-metaverse-developers).
- **Sidechat** (site: side.chat) — Spaceport's pivot/second product: an "AI employee for
  your business" (CRM, research, scheduling, documents, reports; Slack/WhatsApp/email).
  About page names Spaceport Technologies as builder, Le Zhang as founder; investors listed:
  NextView Ventures, Coinbase Ventures, Gokul Rajaram, IDG Capital; Google Cloud partner.
  Contact: le@side.chat. Source: https://side.chat/about — note this investor list only
  partially overlaps the 2022 pre-seed list; whether it reflects a new round is
  **not determinable** from public sources (flagged).
  Le Zhang's own LinkedIn now titles him at Sidechat: https://www.linkedin.com/in/lezhang
- **Sidechat IP** (site: ip.side.host, "Sidechat for IP Licensing") — the Sidechat agent
  packaged for licensing operations, marketed for **Licensing Expo 2026 (Mandalay Bay,
  May 19–21)**. Five apps: Deal Intake Queue, Deal Monitor, Infringement Radar, Contract
  Drafting, Pipeline CRM. Source: https://ip.side.host/

**Resolved open item from `pitch/positioning-implications.md §2c` guardrails:** the
"Spaceport Technologies" name on ip.side.host and the "Spaceport (Cambridge, MA)" in the
Negosh Dec-2024 partnership (`negosh-apac.md`) are **the same company** — the PR Newswire
release gives the URL spaceport.xyz and quotes "Le Zhang, CEO of Spaceport":
https://www.prnewswire.com/news-releases/spaceport-and-negosh-forge-strategic-partnership-empowering-ip-holders-to-build-integrated-brand-licensing-strategies-that-bridge-the-physical-and-digital-worlds-302326318.html
So the newest pre-deal-AI-scoring entrant is corporately connected to Negosh's digital
partner. Implication for the pitch: this is one ecosystem player (Spaceport: Negosh partner
+ Sidechat IP vendor), not two independent proofs of category timing.

**Location discrepancy (flagged, unresolved):** Dec-2024 PR says Cambridge, MA (offices LA
and Berkeley); the 2026 ip.side.host page reads as Las Vegas-based per fetch — plausibly
conflated with the Licensing Expo venue (Mandalay Bay, Las Vegas). Single-source each way;
not load-bearing for the verdict.

## 2. What its "AI scoring" actually scores (vendor-stated only — UNVERIFIED)

Direct read of https://ip.side.host/ (2026-07-15):

- **Deal Intake Queue:** AI scores inbound licensing requests on **"revenue history, IP
  compliance, completeness"**, flags missing documentation; "intake to qualified lead" in
  under 60 seconds. → scores the *applicant/lead*, i.e. which inbound licensee is
  strongest/most legitimate.
- **Infringement Radar:** HIGH/MEDIUM/LOW **confidence scoring** on unauthorized-use alerts
  across Etsy, Amazon, eBay, TikTok Shop, Redbubble. → scores *detection confidence*.
- Nothing on the page scores whether a given IP × given product would *perform well
  together*. No pairing-fit, no outcome prediction, no market-fit quantification.
- Catalog shown (Bob Ross, National Lampoon, Doge, Lucha Libre AAA) is Spaceport-managed
  inventory. One testimonial (Kyle Brockett, Koo Capital: "handled 320 requests in one
  evening") — vendor-quoted, no independent confirmation found.
- **No independent press coverage, review, or named-customer reporting of Sidechat IP was
  found** under any query in §5. All product claims remain single-source (vendor).

## 3. Chinese-language coverage: none found

Per task rules, absence stated with trail: **no zh-TW or zh-CN source covering Sidechat IP
or Sidechat-as-licensing-AI was found under the queries tried** (§5). zh queries returned
only the English vendor pages, the unrelated campus app, and coincidental near-names (§4).
Spaceport's Toei partnership surfaces in Japanese media (MoguLive:
https://www.moguravr.com/roblox-hypergalactic/) but with no Sidechat mention. Chinese-market
invisibility cuts both ways: a Taipei VC is *unlikely* to raise Sidechat IP from zh sources,
but if they walked Licensing Expo 2026 they may have seen it first-hand.

## 4. Name-collision guard (what a VC might conflate it with)

1. **Sidechat, the anonymous campus app** (sidechat.lol; iOS App Store id1591988276) —
   anonymous college community app launched early 2022; widely covered (CBS News:
   https://www.cbsnews.com/news/sidechat-app-explained-student-protests/, Wikipedia:
   https://en.wikipedia.org/wiki/Sidechat, Harvard Magazine). **No relation** to Spaceport —
   different product, different domain, consumer social vertical. This is the entity that
   dominates general "Sidechat" search results.
2. **塞掐 Side Chat** — a Taiwanese tech podcast whose name surfaces in zh-TW searches
   (e.g. https://www.youtube.com/watch?v=BJ92fomIRJM). Coincidental homophone; no relation.
3. **Sider / Sider.ai** — AI browser-sidebar assistant (https://sider.ai/); near-name that
   appears in zh AI-tool searches; no relation.

## 5. Search trail (queries run 2026-07-15)

- zh: `"Sidechat" 授權 AI 評分 IP` (zh-TW); `Spaceport 授权 AI 评分 IP 许可 平台 智能`
  (zh-CN); `Spaceport 東映 IP授權 Roblox 平台` (zh-TW/ja mixed); `"Sidechat" app 匿名 校園`
  (collision check) → no zh coverage of Sidechat IP found.
- en: `"Sidechat" IP licensing AI scoring "Spaceport Technologies"`;
  `"Spaceport Technologies" OR "spaceport.xyz" funding seed Le Zhang founded`.
- Direct fetches: ip.side.host, side.chat/about, spaceport.xyz funding-PR, PR Newswire
  Negosh release. Crunchbase profile fetch returned 403 (identity taken from search-result
  listing only — flagged).
- Registry note: no state/company-registry filing was directly retrieved; legal-entity name
  and jurisdiction remain **unverified** (Crunchbase/LinkedIn/PR consistently say
  "Spaceport Technologies," which is sufficient for identity but not for registry-grade
  confirmation).

## 6. One-line answer for the pitch room

"Sidechat IP is real — it's the licensing-ops pivot of Spaceport (spaceport.xyz), the
$3.6M-funded Roblox-IP-licensing startup that partnered with Negosh in Dec 2024. Its AI
scores which inbound *applicant* to trust, in 60 seconds — it still doesn't score whether an
IP and a product will sell *together*. Even the newest AI entrant scores the wrong object;
the pairing decision is still open." (All Sidechat IP product claims are vendor-stated;
never cite its traction.)
