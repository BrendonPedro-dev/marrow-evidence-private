# Counterparty diligence: vostok inc (株式会社vostok), vostok.co.jp

Desk research pass, compiled 2026-08-01.
Sources are publisher pages, the company's own site, and public registry/WHOIS records.
No non-public information was used and none is contained here.

**Status of this pass:** Questions 1 and 2 are answered.
Questions 3, 4 and 5 are answered to the limit of what the public record currently supports, with the specific open items listed at the end.

## Confidence key

- **Confirmed** - stated on a primary source I retrieved directly, and named below.
- **Assumed** - consistent with the evidence but resting on inference, not on a document.
- **Unresolved** - looked for, not found. Recorded as such rather than guessed.

Nothing below asserts ownership, rights, or intent.
Where something looks like a pattern, it is written as a signal.

---

## Summary

The company is real, very new, and very small.
The founder is a genuinely documented figure with a verifiable track record, and the headline claim made in the approach checks out against contemporaneous press.
The gap is not credibility of the person.
The gap is that nothing in the public record connects this company, or this founder, to character IP licensing in any capacity, and the company publishes no service offering at all against which a proposal could be checked.

| # | Question | Short answer |
|---|---|---|
| 1 | Corporate reality | Real registered Japanese corporation, incorporated 2025-01-14, ~18 months old, ~11-16 staff, ¥113m stated capital, Shibuya address. Registry entry not independently retrieved. Okamoto unresolved. |
| 2 | The 17kg claim | **Confirmed.** He founded and ran it. The specific "400k in ~18 months" figure traces to a March 2019 interview. It is a 2017-2019 achievement in apparel D2C. |
| 3 | Character IP licensing work | **None found, by the company or by its people, ever.** Absence is consistent across their own site, their own selected press, and independent search. |
| 4 | What vostok sells | **Unresolved by their own choice.** The site states a one-line business description and publishes no services, no case studies, no clients, no products. Nothing public to match a proposal against. |
| 5 | Conflict surface | No evidence found of licensing or IP-matching tooling of their own. Also no evidence against it. The founder's documented pattern is building and operating his own consumer brands. |

---

## 1. Corporate reality

### Confirmed

**The company exists as a registered Japanese corporation.**
The domain vostok.co.jp is held by "vostok, Inc.", organization type recorded as `corporation`, in the JPRS registry.
Registered date and connected date are both 2025-01-28.
A `.co.jp` domain can only be held by a company registered in Japan and JPRS verifies this at registration, so the record is corroboration that a registration exists, independent of the company's own claims.
Source: JPRS WHOIS, `https://whois.jprs.jp/en/?type=DOM&key=vostok.co.jp`.

**Self-reported company facts, from their own site** (`https://vostok.co.jp/`, retrieved 2026-08-01):

| Field | Stated value |
|---|---|
| Company name | 株式会社vostok / vostok inc |
| Founded | 2025.01.14 |
| Employees | 約16名 ("approximately 16") |
| Capital | 1億1,300万円 (¥113,000,000) |
| Business | "ENTERTAINMENT領域のプロダクトやサービス制作" ("product and service production in the entertainment domain") |
| Address | 4F, MAGNET by SHIBUYA109, 1-23-10 Jinnan, Shibuya-ku, Tokyo 150-0041 |
| Named officer | Kenji Tsukahara (塚原健司), Founder & CEO |

**The two dates agree.**
Claimed incorporation 2025-01-14, domain registered 2025-01-28, fourteen days later.
That is the normal sequence for a genuinely new company and there is no inconsistency there.

**Company age: about 18 and a half months** as of 2026-08-01.

**The site contradicts itself on headcount.**
The visible page says 約16名.
The JSON-LD structured data embedded in the same page's `<head>` says `"numberOfEmployees": { "value": 11 }`.
Both were served on the same retrieval.
Signal only: most likely a stale structured-data block that was not updated alongside the visible copy, which would put the company somewhere in the 11-16 range and growing.
It is not evidence of misrepresentation, but the true headcount is not established by their own site.

**Domain control sits with Tsukahara personally.**
Both the administrative and the technical contact for vostok.co.jp resolve to `Tsukahara, Kenji`, organization `vostok, Inc.`, JPNIC handles KT80515JP and KT80516JP, last updated 2025-01-28.
Both records list a free webmail address rather than a company address, and one lists a personal mobile.
The contact details are not reproduced here; the handles above allow anyone to reproduce the lookup.
Signal: normal for a founder-run company of this age, and it corroborates that Tsukahara is the operating principal rather than a figurehead.

**Who Tsukahara is.**
Born 1992-03-02.
Documented career, from the sources in section 2 and a Japanese Wikipedia entry: self-taught programmer at Hosei University, founded WhiteLabel Co., Ltd. and sold the company/business after about 18 months, founded Bordi Co., Ltd. in June 2017 which was later renamed 株式会社イチナナキログラム (17kg Inc.), and more recently produces the brand goodnight5tore.
He is a real, independently documented operator with named companies and dated press going back to at least 2019.
This is the strongest thing in the file.

### Assumed

- The ¥113m stated capital is a **funding-shaped number**, not a bootstrapping-shaped one. Round bootstrapped incorporations in Japan cluster at ¥1m, ¥5m, ¥10m. ¥113,000,000 is the shape left behind by one or more priced rounds. Assumed, because no funding announcement was found to confirm it (see below).
- The Shibuya address is a real commercial building (MAGNET by SHIBUYA109, at the Shibuya scramble crossing). Whether the 4th floor tenancy is a private office, a serviced office, or a shared/coworking floor is **not established**.

### Unresolved

- **The corporate registry entry itself was not retrieved.** The Japanese National Tax Agency corporate number site (houjin-bangou.nta.go.jp) is JavaScript-driven with no reachable GET search endpoint, its Web-API requires an issued application ID, and the third-party mirrors that normally index it were unavailable on this pass: gBizINFO keyword search returned HTTP 500, houjin.info returned 403, SalesNow DB returned 403 at the CDN, and Money Forward 法人ナビ has been discontinued since 2022-08-01. Searches surfaced only unrelated same-name entities (株式会社VOSTOK NINE, an advertising planning firm in Shinagawa; 株式会社ヴォストーク, a video production firm in Shinagawa; VOSTOK EUROPE, a watch brand distributed by 株式会社ANDOROS). **Corporate number, registered officers beyond Tsukahara, and registered capital are therefore unconfirmed from the register.**
- **Daisuke Okamoto is unresolved.** No public record was found linking anyone of that name to vostok inc, to Tsukahara, or to 17kg. Searches returned only unrelated individuals. Note that the name appears on a shared mailbox (`v-system@`) rather than a personal one, which is itself a signal worth registering: at a company of 11-16 people, outbound business development conducted from a shared system account under one name and signed by another is a shape, not a norm.
- **No funding announcement was found.** A PR TIMES search for 株式会社vostok returned 33 results, **none of which are this company** (all are VOSTOK NINE, VOSTOK EUROPE / ANDOROS, or unrelated). For a Shibuya entertainment-sector startup with ¥113m of capital, zero PR TIMES presence in 18 months is unusual. It is not evidence of a problem, but it does mean the capital figure, the investor set, and the board are all unverified.

---

## 2. The 17kg claim

**Claim as presented: built Instagram-led D2C brand 17kg to 400k+ followers in about 18 months.**

### Confirmed

**The claim checks out, and his role was founder and CEO, not vendor or consultant.**

The specific figure traces to a CareerHack (en-japan) interview published **2019-03-27**, which states the Instagram account reached **400,000 followers within one year and a half** of launch, and identifies Tsukahara, then 27, as 代表取締役 (representative director) of 17kg.
Source: `https://careerhack.en-japan.com/report/detail/1087`.

A WWD JAPAN feature published **2019-06-07** corroborates and extends it.
Source: `https://www.wwdjapan.com/articles/872421`.

| Fact | Value, as published 2019-06-07 |
|---|---|
| 17kg launched | June 2017 |
| Tsukahara's role | Founder, President/CEO |
| 17kg Instagram followers | 480,000 |
| Across all six brands | over 1,000,000 |
| Brands operated | 17kg, U_DRESSER, BEEP, RURU, LILY BOUTIQUE, BELLED |
| Headcount | approx. 80 including part-time, average age 23 |
| Revenue | "two-digit hundred millions" of yen annually |
| Growth | 110-120% month on month; 5-10x year on year |
| Capital raised | ¥4.5m from an angel, self-funded from revenue thereafter |
| First physical store | Laforet Harajuku, opened 2019-04-26, ¥10m in month one |

June 2017 launch plus eighteen months lands in December 2018, and the March 2019 article reports 400k at "a year and a half."
The arithmetic is internally consistent.
This is a claim that survives checking, which is not the usual outcome.

A later WWD JAPAN piece, published **2021-02-12**, covers goodnight5tore, run by Tsukahara as CEO of Ichinanakilogram, and reports the 17kg account at 557,000 followers.
It describes goodnight5tore as operated by Tsukahara and one other person, with monthly drops selling out in minutes, and one January 2021 drop of ¥600m of inventory drawing ¥1.3bn in lottery applications from 7,000 people.
Source: `https://www.wwdjapan.com/articles/1176315`.

### What the claim does not establish

Stated as scope, not as criticism.

- **It is an apparel D2C track record, not a licensing one.** Six own-brand fashion labels, own inventory, own store, own audience.
- **It is 2017-2019 work**, roughly seven to nine years old, on an Instagram whose organic reach mechanics have changed substantially since.
- **It was his own company.** The demonstrated skill is building an owned brand and its audience. It is not evidence of executing on behalf of a third-party principal, to a brief, against someone else's assets.
- **It is not vostok's track record.** 17kg is 株式会社イチナナキログラム, founded June 2017. vostok inc was founded 2025-01-14. Presenting 17kg in a vostok approach is presenting the founder's history, which is legitimate and normal, but the operating entity being proposed has no track record of its own in the public record.

### Unresolved

- Whether Tsukahara still holds or operates 17kg / 株式会社イチナナキログラム, and what the current state of that company is. Not established on this pass.
- Current follower counts for any of the brands. The most recent figure retrieved is 557,000 from February 2021.

---

## 3. Character IP licensing work, ever

### Confirmed: none found

This was searched from several directions and the result was consistently nil.

**Their own site.**
The entirety of vostok.co.jp is a single page.
It contains: the company name, the founder's name and two social links, three press links, the six-line company table, and an address.
There is no work section, no case study, no client list, no product, no licensing reference of any kind.

**Their own selected press.**
The three articles vostok chose to link are the two WWD JAPAN pieces and the CareerHack interview, all covering 17kg and goodnight5tore.
All three are about building and selling **own-brand apparel**.
None mentions character IP, licensing, rights holders, or acting as an intermediary.
The company is displaying its best credentials on its front page, and character IP licensing is not among them.

**Independent search.**
No press, case study, announcement or credit was found associating vostok inc, Kenji Tsukahara, 17kg, or goodnight5tore with any character IP licensing campaign, in Japanese or English.

**Campaign-record cross-check.**
No trace of vostok inc, Tsukahara, 17kg, or goodnight5tore appears in any Japan character-licensing campaign record reviewed for this diligence, public or otherwise.

**This absence is a finding and should be weighted as one.**
It is not that the evidence is thin.
It is that across four independent angles, including the company's own chosen self-presentation, there is nothing.
The proposal describes work in a category in which neither the company nor its principal has any traceable prior involvement.

Note the boundary honestly: absence of public evidence is not evidence of absence.
Private, unannounced, or subcontracted licensing work would not necessarily surface.
But a firm proposing licensing work that had done licensing work would ordinarily say so on its front page, and this one does not.

---

## 4. What vostok sells

### Confirmed

**They publish no service offering.**
The only statement of what the business does is one line: "ENTERTAINMENT領域のプロダクトやサービス制作" - production of products and services in the entertainment domain.
That phrasing is deliberately broad and does not distinguish between an agency, a development shop, a growth consultancy, and an own-product studio.

There is no services page, no capabilities statement, no pricing, no engagement model, no client logos, no portfolio, and no named product.
There is no contact form and no email address published anywhere on the site.
The site does not have a `/company` or `/about` route; both return 404.
The structured data lists `"sameAs": []`, an empty set, meaning no corporate social or directory profiles are declared.

### Assumed

**The shape most consistent with the evidence is an own-product entertainment studio, not a services agency.**
The reasoning: the founder's entire documented history is building and operating brands he owns, the capital figure is investment-shaped rather than fee-revenue-shaped, and a services business 18 months in would normally publish an offer and references in order to sell.
This is an inference from shape, not a documented fact, and it could be wrong.

### Does the public offer match what was proposed?

**No, because there is no public offer to match it against.**
This is the honest answer and it is worth stating plainly rather than dressing up.

The proposal describes a 4-6 week market pilot producing a partner list and a "licensing and partner CRM prototype."
That is a defined consulting-and-build engagement.
Nothing on vostok's public surface indicates they sell consulting engagements, that they build CRM or tooling for clients, or that they work in licensing.
There is no published evidence they have ever delivered a client engagement of any kind.

Signal, stated as a signal: the proposal's ask (catalogue, priority assets, structure, materials, budget) is broad discovery input.
A firm with a standing practice in a category normally arrives with a narrower, more opinionated ask because its prior work has already told it what matters.
A broad discovery ask is the shape of a first engagement in a new category.
That is a legitimate thing to be, but it is a different thing from an established licensing practice, and the public record does not distinguish which is on offer here.

---

## 5. Conflict surface

### Confirmed

**No evidence found that vostok operates or sells IP-matching or licensing tooling of its own.**
No such product is named on their site, in their press, or in search.
No PR TIMES releases exist for this company at all.
No client list is published, so no client-side conflict can be assessed either way.

### The honest read

There is no evidence of a conflict, and there is also no evidence ruling one out.
An 18-month-old company with an empty public surface produces almost no conflict signal in either direction, and that neutrality should not be read as clearance.

Two things are worth registering as signals rather than conclusions:

- **The proposal's deliverable is a prototype of a tool.** A "licensing and partner CRM prototype" is a build, and the partner list that accompanies it is the dataset that would populate it. An engagement structured that way produces, as its output, a working component of exactly the kind of product a company in the "entertainment domain products and services" business might want to own. This is an observation about the shape of the deliverable. It carries no claim about anyone's intent, and it is equally consistent with a straightforward, good-faith scoping engagement.
- **The founder's documented method is explicitly pattern-extraction.** In the 2019 CareerHack interview he describes his approach as systematically observing services and content with abnormal growth, analysing 10-20 similar accounts in parallel to identify 歪み ("distortions", meaning platform hacks and information asymmetries), and then applying the findings operationally. That is a stated methodology, from his own mouth, in a published interview. It is a legitimate and effective operator's method and it is why 17kg worked. It is also directly relevant context for what a discovery engagement with this counterparty is likely to be used for.

### Unresolved

- Vostok's client base, entirely. None is published.
- Whether any product is in development. Nothing is announced.
- Cap table and investors, which would show whether any backer sits adjacent to licensing, IP, or rights management. Not retrievable without the registry entry or a funding announcement, neither of which was found.

---

## Sources

Primary, all retrieved 2026-08-01.

| Source | URL |
|---|---|
| vostok inc corporate site (single page) | `https://vostok.co.jp/` |
| JPRS WHOIS, domain record | `https://whois.jprs.jp/en/?type=DOM&key=vostok.co.jp` |
| JPRS WHOIS, contact records KT80515JP / KT80516JP | `https://whois.jprs.jp/en/?type=CONTACT&key=KT80515JP` |
| CareerHack (en-japan), Tsukahara interview, 2019-03-27 | `https://careerhack.en-japan.com/report/detail/1087` |
| WWD JAPAN, 17kg feature, 2019-06-07 | `https://www.wwdjapan.com/articles/872421` |
| WWD JAPAN, goodnight5tore interview, 2021-02-12 | `https://www.wwdjapan.com/articles/1176315` |
| Japanese Wikipedia, 塚原健司 | `https://ja.wikipedia.org/wiki/塚原健司` |
| PR TIMES search, 株式会社vostok | `https://prtimes.jp/main/action.php?run=html&page=searchkey&search_word=株式会社vostok` |

Note on the Wikipedia entry: it carries maintenance tags for weak sourcing and contested notability, so it is used here only for items that the dated press independently corroborates.

Note on "Featured In": the site displays a Forbes JAPAN logo alongside the WWD JAPAN logo, but links only the WWD and CareerHack articles.
The Forbes item is not linked and has not been retrieved.
The Wikipedia reference list points to a Forbes JAPAN piece on entrepreneurs' book recommendations, which if it is the same item would be a contributed listicle appearance rather than a company feature.
**Unverified**, and flagged because a masthead shown without a link is a soft signal.

---

## Open items for the next pass

1. Retrieve the actual corporate register entry: corporate number, registered address, registered capital, and the full officer list. Requires either an NTA Web-API application ID, the NTA bulk 基本3情報 download for Tokyo (prefecture 13), or a paid registry pull (登記情報提供サービス / Teikoku Databank / Tokyo Shoko Research).
2. Resolve Daisuke Okamoto, or establish positively that he has no public footprint.
3. Establish the current status of 株式会社イチナナキログラム and whether Tsukahara still holds it.
4. Confirm or drop the ¥113m capital figure and identify any investors.
5. Determine whether MAGNET by SHIBUYA109 4F is a private tenancy or a shared/serviced floor.
6. Retrieve the Forbes JAPAN item and confirm what kind of appearance it is.
7. Check archived snapshots of vostok.co.jp for any earlier version that stated a service offering, since the current page may be a recent simplification.
