# Physical-Product Performance Data: What Exists, Who Can See It, Whether It Reaches the Pre-Deal Decision

*Research file — factual findings only, no pitch interpretation. Interpretation lives in `/pitch/`.*

**Question addressed (research question 4):** What performance data actually exists for
**physical licensed products** (POS/sell-through providers, retailer supplier portals, royalty
reports), **who can access it**, and — most importantly — **whether anyone wires it into the
*pre-deal* IP × licensee selection decision.** This file also gives an honest treatment of the
NielsenIQ / Circana counter to any claim that "the data doesn't exist."

**One-line answer:** The performance data for physical licensed products **does exist** and is
mature — but it is **fragmented across three disconnected layers** (syndicated market panels,
per-retailer supplier portals, self-reported royalty statements), each **retrospective**,
**aggregated or siloed**, and **access-gated**. **No product was found that ingests any of it to
score a specific IP × licensee *pairing before the deal is signed.*** So the correct framing is
**not** "the data doesn't exist" — it does — but **"the data exists and isn't wired into the
pre-deal fit decision."** This is the direct bridge from `consumer-product-gap.md`: the gap is
not a data-impossibility, it is a **wiring** gap.

---

## 1. The three layers of physical-product performance data

Performance data for a physical licensed product (a Sanrio plush, a character-branded snack, a
licensed T-shirt) lives in three places that do not talk to each other:

| Layer | Source | What it measures | Granularity | Temporality |
|---|---|---|---|---|
| **A. Syndicated market panels** | Circana, NielsenIQ | Category & brand/property sales across *many* retailers | Aggregated (property, category, channel) | Retrospective (weekly/monthly) |
| **B. Retailer supplier portals** | Walmart Luminate, Target Partners Online, Amazon Vendor Central | One retailer's own POS/sell-through for *your* SKUs | SKU × store × day (deep) | Retrospective (near-real-time) |
| **C. Royalty reports** | Licensee → licensor, via SaaS (Flowhaven et al.) | Units/net sales the *licensee self-declares* | SKU/territory (as reported) | Retrospective + lagged (monthly/quarterly) |

Each layer answers "how did products that *already exist* perform?" None answers "which IP ×
licensee pairing should we *sign*?"

---

## 2. Layer A — syndicated retail-tracking panels (Circana, NielsenIQ)

### Circana (the entertainment/toy-relevant one)
- **Formed** by the merger of **IRI** (Information Resources, Inc.) and **The NPD Group**,
  which **completed in 2022** (H&F acquired NPD 2021, merged with IRI Aug 2022); the combined
  company's **Circana rebrand was announced March 7, 2023** and rolled out through 2023. IRI's
  heritage is **POS/scan tracking in grocery, drug, mass,
  club, convenience**; NPD's is **discretionary general merchandise — toys, video games,
  apparel, beauty, footwear** — which is why the merged firm now spans both CPG and the
  **toy/entertainment** categories most relevant to character licensing. *(Multi-sourced:
  Wikipedia, Grocery Dive, Forbes, Mojo Nation.)*
- **Circana Retail Tracking Service** explicitly measures **licensed-property performance**: its
  April 2025 licensing commentary reports that newer properties such as **CoComelon, LankyBox,
  and Gabby's Dollhouse** sit in the **$50M–$100M U.S. brand-footprint** growth band while the
  largest properties (**>$250M**) are **plateauing**, and that Circana tracks the influence of
  **parental affinity** on licensed sales. *(Two sources: circana.com "Making sense of the
  licensing market"; kidscreen.com 2025-04-09 coverage of the same.)*
- **Crucial for this file:** every documented use is **post-hoc measurement** — sizing
  properties, ranking growth, tracking whether a *launched* license is growing or plateauing.
  Circana's own framing is to **"make sense of the licensing market,"** i.e. read it, not to
  **predict which pairing to sign**. *(circana.com.)*

### NielsenIQ (NIQ)
- **Retail Measurement Services (RMS)** captures standardized **in-store sales, price,
  distribution, promotion** for ~**50 million products** from ~**900,000 stores** globally,
  monthly, across grocery/mass/club/drug/convenience/e-commerce/specialty. A **separate NIQ
  product, Key Account Data (KAD)** (its own product page, not part of RMS), gives manufacturers
  **sell-out data shared by retail partners**, including on competitors' products. *(Sources:
  nielseniq.com RMS page + distinct KAD product page; SoftwareOne marketplace listing.)*
- NIQ is **CPG/grocery-weighted**; it is not the natural home of character-merchandise
  categories the way NPD/Circana is. Its **Brandbank / Content Licensing** business is
  **product-content syndication** (images, attributes, nutritional data across 39 markets,
  52,000+ brands) — *note the name collision:* this "content licensing" is **not IP brand
  licensing**, it is licensing *product-catalog content*. *(nielseniq.com Content Licensing.)*

**Access & cost (Layer A):** syndicated panels are **subscription products sold to brands and
retailers**; access is **expensive and enterprise-gated**, and the data is delivered
**aggregated** (property/category/channel), not as an open pairing-prediction feed. Exact pricing
is not publicly disclosed and is **not asserted here**.

---

## 3. Layer B — retailer supplier portals (siloed to one retailer's own suppliers)

Each large retailer runs its own portal exposing **its own POS/sell-through** to **its own
suppliers only**:

- **Walmart — Retail Link → Luminate.** Walmart **launched Luminate in 2021**, added the **free
  Luminate Basic package in Oct 2022**, and from **Oct 2023** moved suppliers off legacy Retail
  Link / DSS onto Luminate (DSS phased out early 2024), effectively **requiring suppliers to
  subscribe**. **Luminate Basic is free** (manual reports, no data feeds/API); **Luminate Charter
  is paid** (a % of sales; separates physical-store POS from dotcom, adds API feeds). *(Two+
  sources: Walmart corporate 2022-10-12; Talk Business & Politics 2023/2024; e2open; SPS
  Commerce.)* A ~90% "largest suppliers on Charter" figure circulates in trade press but traces
  to a single Walmart self-report (echoed by outlets, not independently confirmed) — **flagged
  UNVERIFIED.**
- **Target — Partners Online (partnersonline.com).** All Target vendors get logins to pull
  **retail sales data** — 40+ applications, ability to query **100+ metrics by SKU, location,
  and day**, plus raw **Business Partner Data (BPD)** feeds of sales and inventory. *(Two
  sources: Alloy.ai; inymbus / Cahoot supplier guides.)*
- **Amazon — Vendor Central (1P) Retail/Brand Analytics.** First-party vendors see **sales,
  traffic, conversion, sell-in vs sell-out**, plus Brand Analytics (repeat purchase, search
  terms, market basket) via portal and SP-API. Brand Analytics is **brand-owner-gated** (open to
  sellers and vendors who own the enrolled brand, not vendors exclusively).
  *(Two sources: Improvado; Be Bold Digital vendor guides.)*

**The structural fact:** Layer B is **deep** (SKU × store × day) but **siloed** — Walmart data
covers only Walmart, Target only Target, Amazon only Amazon — and is **scoped to a supplier's
own products**. There is **no cross-retailer, cross-licensee view**, and **no pre-deal
counterfactual** (you can't see how a product you *didn't* make would have sold). It answers
"how are *my* SKUs doing at *this* retailer," not "which IP × licensee should sign."

---

## 4. Layer C — royalty reports and royalty-rate benchmarks

Two distinct things live here; keep them separate.

### 4a. Royalty reports (the licensor's own performance data — self-reported, lagged)
The performance data a **licensor** actually holds on its own licensed products is the **royalty
statement the *licensee* self-declares** — units/net sales reported into the licensor, typically
monthly/quarterly. Modern licensing-ops SaaS (**Flowhaven**, and the type-B stack catalogued in
`quantified-licensing-landscape.md`) collects these through **self-service partner portals with
structured templates** and **flags discrepancies** (SKU mismatches, wrong rates, missing
territories, MG shortfalls) at submission — this portal/template/discrepancy-flag language is
**verified verbatim** on flowhaven.com's royalty-management page. A widely-circulated "found
millions in misfiled royalty statements" line is often attributed to Flowhaven but does **not**
appear verbatim on that page (it surfaces only as a paraphrased search snippet) — **flagged
UNVERIFIED and not load-bearing**. The *value proposition itself is evidence* that royalty data is
**self-reported, error-prone, and needs validation**. *(Sources: flowhaven.com royalty-management
page — verified; Software Advice profile.)*
- **Implication:** even the licensor's *own* first-party performance signal is **licensee-
  reported, lagged, and audit-prone** — the weakest possible substrate for a real-time pairing
  model, and post-deal by definition.

### 4b. Royalty-rate benchmark data (rates, not sell-through)
Separately, **benchmark databases** sell *comparable royalty rates* — **The Licensing Letter
"Royalty Trends Report,"** and IP-royalty databases like **RoyaltyRange, RoyaltySource,
ktMINE**. These tell you **what rate a category commands**, not how a specific pairing will
*sell*. They belong to the **valuation/benchmarking** bucket already ring-fenced in
`consumer-product-gap.md §2e` and **must not** be mistaken for fit or sell-through data. *(The
Licensing Letter cited via IMC Licensing; RoyaltyRange / RoyaltySource vendor pages —
rate-benchmark claim is **single-source-per-vendor**, treated as descriptive not load-bearing.)*
- **License Global's "Top Global Licensing Agents" whitepaper** *gathers retail sales data of
  licensed consumer products from the agents who represent the IP direct* — an **industry-
  aggregation** of self-reported agent figures (2026 edition: 60 agents, ~$117.7B licensed retail
  for 2025), retrospective and directional, **not** a pairing predictor. *(Now multi-sourced:
  License Global rankings + market-overview resource copy + GlobeNewswire 2026-04-02 release —
  upgraded from UNVERIFIED to confirmed for the "retail sales data" methodology.)*

---

## 5. Who can access what (summary)

| Data | Who can access | Cost posture | Cross-licensee / pre-deal use? |
|---|---|---|---|
| Circana / NIQ syndicated panels | Brands & retailers who subscribe | Enterprise subscription (undisclosed) | Cross-property **market sizing**, retrospective — **not** pairing prediction |
| Walmart Luminate | Walmart's own suppliers | Free (Basic) / paid (Charter) | Own-SKU, one retailer — **no** cross-licensee view |
| Target Partners Online | Target's own vendors | Included with vendor status | Own-SKU, one retailer |
| Amazon Vendor Central Analytics | Amazon 1P vendors / brand owner | Included with 1P status | Own-SKU, one channel |
| Royalty statements | The specific licensor (via SaaS) | SaaS subscription | Own-portfolio, self-reported, **post-deal** |
| Royalty-rate benchmarks | Anyone who buys the report | Report/subscription | Rate reference, **not** sell-through or fit |

**No row is a pre-deal, cross-licensee, pairing-level performance dataset.** Each is either
retrospective, siloed to one party's own products, aggregated to the category/property level, or
a rate reference.

---

## 6. Is any of it wired into the pre-deal decision? (the core finding)

**No product was found that ingests physical-product performance data to score an IP × licensee
pairing before signing.** What the evidence shows instead:
- **Circana/NIQ** are used to **read the market** and **track launched properties** — Circana's
  own licensing content is explicitly about **making sense of** the market and **measuring**
  property footprints, all retrospective. *(circana.com; kidscreen.com.)*
- **Retailer portals** are **operational/BI tools** for a supplier's **existing** business at
  **one** retailer — order management, chargebacks, replenishment, own-SKU performance. They are
  structurally incapable of a cross-licensee pre-deal comparison.
- **Royalty SaaS** is **post-deal administration** (`quantified-licensing-landscape.md` type B);
  the data it holds only exists *after* a deal is live.
- The **due-diligence** literature that *does* touch pre-deal is dominated by **IP-ownership/
  rights verification** (does the licensor validly own the IP), **not** performance-fit
  prediction. *(License Global / Vistex licensing-integration commentary; Lumenci, Mayer Brown,
  UpCounsel DD guides.)* Some brand-licensing guidance **does** discuss pre-deal **"partner
  fit"** — assessing whether a partner's products, market presence, and brand values align, plus
  a product-quality/reputation review — but this is **qualitative alignment vetting, not a
  data-driven performance/sell-through prediction**, and no productized quantitative version for
  physical consumer-product licensing was found.

This is fully consistent with `consumer-product-gap.md`: the pre-deal fit-prediction slot for
character × physical product is **unoccupied**, and this file explains **why the raw material for
it is sitting unused** — it is spread across three non-interoperable, access-gated, retrospective
layers that nobody has assembled into a forward-looking pairing model.

---

## 7. The honest counter: NielsenIQ / Circana and "the data exists"

A VC or competitor can fairly object: *"Sell-through data clearly exists — brands can buy Circana
and NielsenIQ; Walmart hands suppliers Luminate. So the 'no data' premise is false."* **That
objection is correct, and this file concedes it plainly.** The physical-product performance data
**does exist** and is, in places, very deep (SKU × store × day at Walmart/Target/Amazon).

The accurate claim is therefore **not** "the data doesn't exist," but the narrower, defensible:

> The data exists, but it is **fragmented, retrospective, siloed by retailer, aggregated in the
> syndicated layer, self-reported in the royalty layer, and access-gated** — and **no player has
> wired any of it into the pre-deal IP × licensee selection decision.** Every existing use is
> *post-hoc measurement* or *single-retailer operations*, never *forward pairing prediction*.

Why the wiring hasn't happened (structural, evidence-based reasons — offered as explanation, not
as proven causation):
1. **No cross-licensee counterfactual.** Portals show only your own SKUs; syndicated panels
   aggregate to property/category — neither exposes "how would *this specific pairing* perform."
2. **Retrospective, not predictive.** All three layers describe the past of *launched* products.
3. **Siloing & access cost.** Walmart/Target/Amazon data are locked to that retailer's suppliers;
   syndicated data is expensive and enterprise-gated.
4. **Self-report weakness at the licensor.** The licensor's own performance signal is
   licensee-declared and audit-prone (Flowhaven's whole value prop).
5. **Digital-vs-physical latency.** As `quantified-licensing-landscape.md` documents, fit
   quantification appeared first where interaction data is **born digital** (in-game events,
   influencer posts) — physical sell-through is captured *after* the sale and stitched together
   from disconnected systems, so the modeling substrate arrived later and messier.

**Net:** the counter *strengthens* rather than weakens the underlying point — it moves the claim
from the fragile "there's no data" to the sturdy "**the data exists and no one has connected it
to the decision that matters.**"

---

## 8. Evidence quality: "no evidence found" vs "evidence of absence"

| Finding | Coverage depth | Claim strength |
|---|---|---|
| The three data layers exist and are retrospective/siloed | Vendor & trade pages read across all three layers | **Well-evidenced, multi-source** |
| Circana measures licensed properties **post-hoc** | Circana article + Kidscreen coverage, feature-level | **Evidence of absence** of a pre-deal/predictive use on the surface described |
| No product wires this data into pre-deal pairing selection | Search-level across syndicators, portals, licensing SaaS, DD literature | **No evidence found** (strong), consistent with the direct evidence-of-absence in `consumer-product-gap.md` |
| Exact subscription pricing of Circana/NIQ | Not publicly disclosed | **Unknown — not asserted** |
| "90% of top Walmart suppliers on Charter" (Walmart self-report); Flowhaven "millions misfiled" (paraphrased snippet, not on-page) | Single/company-origin source each | **UNVERIFIED — flagged inline** |
| License Global "gathers agent-reported retail sales data" | Rankings page + market-overview resource + GlobeNewswire 2026-04-02 | **Confirmed (upgraded from UNVERIFIED)** |

---

## Sources

All accessed **2026-07-13**. Royalty-rate-benchmark and type-B SaaS sources overlap with
`quantified-licensing-landscape.md §Sources` and `consumer-product-gap.md`; new/primary sources
for this file:

### Syndicated panels (Layer A)
- Circana formation (IRI + NPD merger 2022; Circana name announced 2023-03-07) —
  https://www.businesswire.com/news/home/20230307005358/en/ ; https://en.wikipedia.org/wiki/Circana ;
  https://www.grocerydive.com/news/circana-rebranded-name-for-iri-npd/644407/ ;
  https://www.forbes.com/sites/johnellett/2023/10/18/circanas-cmo-united-iri-and-npd-brands-to-fuel-growth/ ;
  https://www.mojo-nation.com/the-npd-group-rebrands-as-circana-following-iri-merger/
- Circana licensing / Retail Tracking Service (post-hoc property measurement, CoComelon/Gabby's
  $50–100M band, >$250M plateauing) — https://www.circana.com/post/making-sense-of-the-licensing-market ;
  https://kidscreen.com/2025/04/09/circana-makes-sense-of-the-licensing-market/
- NielsenIQ RMS (50M products / ~900k stores), Key Account Data sell-out, Content Licensing /
  Brandbank — https://nielseniq.com/global/en/products/retail-measurement-services-rms/ ;
  https://nielseniq.com/global/en/products/key-account-data/ ;
  https://nielseniq.com/global/en/products/maximize-sales-on-key-retail-accounts/ ;
  https://nielseniq.com/global/en/products/content-licensing/ ;
  https://platform.softwareone.com/product/retail-measurement-services-rms/PCP-2582-9792

### Retailer supplier portals (Layer B)
- Walmart Retail Link → Luminate (2021 launch; free Basic package Oct 12 2022; Oct 2023 supplier
  mandate off legacy DSS; Basic free / Charter paid; ~90% top-supplier Charter figure = Walmart
  self-report echoed by trade press, UNVERIFIED) —
  https://corporate.walmart.com/news/2022/10/12/walmart-luminate-introduces-basic-package-free-of-charge-to-suppliers ;
  https://talkbusiness.net/2023/10/walmart-requiring-all-suppliers-to-move-to-luminate-data-service/ ;
  https://www.e2open.com/blog/goodbye-retail-link-hello-walmart-luminate ;
  https://www.spscommerce.com/community/articles/what-is-walmarts-luminate ;
  https://talkbusiness.net/2024/06/the-supply-side-walmart-expands-luminate-sales-data-platform/
- Target Partners Online (partnersonline.com; 40+ apps, 100+ metrics by SKU/location/day, BPD raw
  feeds) — https://alloy.ai/target-partners-online-retail-data ;
  https://blog.inymbus.com/target-partners-online-a-complete-guide-for-suppliers ;
  https://www.cahoot.ai/target-vendor-portal/
- Amazon Vendor Central Retail/Brand Analytics (1P, sell-in vs sell-out, SP-API) —
  https://improvado.io/blog/amazon-vendor-central-analytics ;
  https://www.bebolddigital.com/blog/amazon-brand-analytics-explained

### Royalty reports & rate benchmarks (Layer C)
- Flowhaven royalty management (self-service partner portals, discrepancy flagging; "millions in
  misfiled" = vendor claim, UNVERIFIED) — https://flowhaven.com/platform/royalty-management/ ;
  https://flowhaven.com/resources/blog/royalty-management-brand-licensing/ ;
  https://www.softwareadvice.com/license-management/flowhaven-profile/
- Royalty-rate benchmarks (rates, not sell-through): The Licensing Letter "Royalty Trends
  Report" cited via https://imclicensing.com/what-should-my-licensing-royalty-rate-be/ ;
  RoyaltyRange https://www.royaltyrange.com/solutions/royalty-rates-database/ ; RoyaltySource
  https://selfserve.royaltysource.com/royalty-rate-ip-data-guide/
- License Global "Top Global Licensing Agents" (gathers agent-reported retail sales data; 2026 ed.
  = 60 agents, ~$117.7B licensed retail for 2025 — now multi-sourced/confirmed methodology) —
  https://www.licenseglobal.com/rankings-lists/top-brand-licensing-agents ;
  https://www.licenseglobal.com/licensing-resources/top-global-licensing-agents-market-overview ;
  https://www.globenewswire.com/news-release/2026/04/02/3267135
- Pre-deal due diligence = IP ownership/rights verification, not performance-fit —
  https://www.vistex.com/blog/licensing/licensing-integration/
