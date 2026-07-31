# CET2026 Phase 1 - Hong Kong enrichment

Input: the 32 Hong Kong attendee rows that Phase 0 left unmatched (`findings/expo/cet2026-match.md`, per-row disposition, HK rows 1-33 minus #15 BigBoysToys, which Phase 0 matched brand-side).
Phase 0 is not re-run here and nothing in it is revised.
No other market is touched in this run.

Run opened 2026-07-31.
All retrieval dates below are 2026-07-31 unless stated otherwise.

## The question this run answers

How many of the 32 are representable, and how many are label-captive.
Hong Kong is the art-toy label capital and the census's own HK task pinned captive-by-channel as the expected default for this market.
This run tests that default per row rather than assuming it: the Toyzeroplus logic is applied as a test with a possible negative answer, not as a prior.

No count is stated until every row is adjudicated.
The register below is the working record; the counts section stays empty by design while rows remain open.

## Method

**Both passes, artist-side mandatory.**
Every row gets a zh-HK pass (traditional, Cantonese-register: artist name, character name, 插畫家 / 本地插畫家 / 創作人 / 原創品牌 / 授權) and an EN pass (brand name, artist name, illustrator, artist brand, art toy, licensing).
The artist-side pass is mandatory and is run first; the brand-side pass is used only to test for label, agency or management attachment.
Google News RSS (`hl=zh-HK&gl=HK&ceid=HK:zh-Hant`) is the working index for HK press, as established in the HK census sweep; where it returns a headline, the publisher page is opened directly rather than through the aggregator redirect.

**Evidence rules.**
Publisher pages only: HK press titles, the creator's or brand's own site, the creator's own platform profile, a mall or retailer's own directory page, a publisher's book page.
Aggregators, marketplaces-as-evidence and link-farm listings are not evidence.
The exhibitor sheet's Notes column is unverified prior research: it is used only as a query seed and never carried as a finding, and where the evidence contradicts it that is recorded.

**Band vocabulary, exactly the /start `follower_band` codes:** `lt_10k` / `10k_50k` / `50k_200k` / `200k_1m` / `gt_1m` / `unknown`.
Band = the IP's primary channel following, single channel, not a cross-platform total.
Basis codes are the census's: `at-campaign` / `current-proxy` / `unknown`.
Every band here that rests on a count retrieved in July 2026 is `current-proxy` and says so.
Anti-drift is carried from the HK bands pass: where a character channel and a creator channel are both evidenced and distinguishable, the character's channel governs and the alternative is recorded.

**Confirmed vs assumed.**
Every claim below is tagged.
`CONFIRMED` = a publisher page states it.
`ASSUMED` = the evidence is consistent with it and nothing contradicts it, but no page states it.
Control signals (solo creator, label or agency attached, already under management, prior assignment visible in press) are ASSUMED by construction and are never concluded, however strong they look.

**Class.** INDEPENDENT / PORTFOLIO / MIXED on the census's ownership test: portfolio = corporation, estate, platform or franchise-owned; independent = creator-owned (agency-managed but creator-owned is still independent, the 咖波 precedent); MIXED = an attendee carrying both.
`unresolved` where the entity or its IP could not be identified to the standard above.

**REP decision rule, stated once and applied uniformly.**

- `no` - exclusive label or agency channelling is evidenced (the pinned Toyzeroplus call: creator-owned but exclusively label-channelled is REP=no), or the attendee is itself a label, agency or retailer rather than a creator.
- `yes` - creator-owned IP, at least one confirmed self-run commercial or publishing channel, and no label, agency or management attachment surfaced in either pass.
- `unclear` - an attachment signal exists whose scope is unresolved, or the entity's identity or IP could not be resolved well enough to call.

Unresolved is a valid answer.
Where a row is unresolved it stays unresolved and the reason names what was checked.

## Register

One line per row. `#` is the attendee number from the Phase 0 disposition table.
Rows marked `open` have not been adjudicated yet and carry no call; they are not implied to be anything.

| # | Attendee | Class | REP | Reason (short) | Band | Basis |
|---|---|---|---|---|---|---|
| 1 | 0.9144m Studio | INDEPENDENT | unclear | owner-run craft studio; no character IP evidenced to represent | `lt_10k` | current-proxy |
| 2 | Din Dong & Uncle Fish | INDEPENDENT | yes | solo-illustrator brand (ASSUMED); self-run channels; no label or agency surfaced in either pass | `10k_50k` | current-proxy |
| 3 | Creature Collectors Club | INDEPENDENT | yes | creator-run character brand (ASSUMED); no label or agency surfaced in either pass | `10k_50k` | current-proxy |
| 4 | hohohola x magickira | unresolved | unclear | neither party resolved to a publisher page; candidate handles are false friends | `unknown` | unknown |
| 5 | Pure Studio | open | open | not yet adjudicated | open | open |
| 6 | Nine Four Sixty X Dino Valley | open | open | not yet adjudicated | open | open |
| 7 | Nalok.Lok | INDEPENDENT | yes | named illustrator working under her own name; no label or agency surfaced | `10k_50k` | current-proxy |
| 8 | 大爪作 BIGCLAWX | INDEPENDENT | yes | founder-owned art-toy brand, CONFIRMED in a bylined interview; no label or agency surfaced | `lt_10k` | current-proxy |
| 9 | YoYo! Yogurt!! Studio | INDEPENDENT | yes | creator-run studio brand (ASSUMED); no label or agency surfaced | `lt_10k` | current-proxy |
| 10 | EMO NEKO W.O.O.F. CLUB | INDEPENDENT | yes | creator-run character set under one studio identity (ASSUMED); no label or agency surfaced | `10k_50k` | current-proxy |
| 11 | Ouch!! Don't Cry!! | unresolved | unclear | strongest candidate identity is not confirmed; the candidate's own line-up does not carry this name | `unknown` | unknown |
| 12 | 021 Consultancy x SHIBAINC | INDEPENDENT | unclear | creator-owned and self-licensing, CONFIRMED; but a consultancy is co-listed on the exhibitor row itself and its scope is not resolvable | `10k_50k` | current-proxy |
| 13 | 無盡創意設計工作室 | open | open | not yet adjudicated | open | open |
| 14 | FIGTION | open | open | not yet adjudicated | open | open |
| 16 | CHEAP CENTURY | INDEPENDENT | yes | named illustrator, own characters, own storefront, brand campaigns run in his own name; no agent named in press | `50k_200k` | current-proxy |
| 17 | Shadoowww | INDEPENDENT | unclear | one channel resolved and nothing else; too thin to call either way | `unknown` | unknown |
| 18 | club babo | INDEPENDENT | yes | creator team with its own character and self-run channels, CONFIRMED in a bylined profile; no agency surfaced | `10k_50k` | current-proxy |
| 19 | Genie Li | INDEPENDENT | yes | illustrator working under her own name with her own character; no label or agency surfaced | `10k_50k` | current-proxy |
| 20 | Venus Philosophy | INDEPENDENT | yes | creator-run brand under one artist identity; no label or agency surfaced | `10k_50k` | current-proxy |
| 21 | TOBALLKIDRAWING | INDEPENDENT | yes | named illustrator with her own character, CONFIRMED in a bylined interview; no label or agency surfaced | `10k_50k` | current-proxy |
| 22 | ARDUREY LIMITED | open | open | not yet adjudicated | open | open |
| 23 | cheeky cheeky | open | open | not yet adjudicated | open | open |
| 24 | HEREAFTER STUDIO | open | open | not yet adjudicated | open | open |
| 25 | HANDMADESHIP | open | open | not yet adjudicated | open | open |
| 26 | Scentory | open | open | not yet adjudicated | open | open |
| 27 | Bethel | open | open | not yet adjudicated | open | open |
| 28 | paper diamond® | open | open | not yet adjudicated | open | open |
| 29 | DDED | open | open | not yet adjudicated | open | open |
| 30 | Tse Sai Pei | open | open | not yet adjudicated | open | open |
| 31 | Overloaddance | open | open | not yet adjudicated | open | open |
| 32 | Mr n Mrs Moon | open | open | not yet adjudicated | open | open |
| 33 | Lewa Lee | open | open | not yet adjudicated | open | open |

## Per-row detail

### 1. 0.9144m Studio

**Identity (ASSUMED).** The evidenced entity is a Hong Kong textile and tufting studio trading as `0.9144m - Textile Studio`, with a shop unit listed in the New Town Plaza (Sha Tin) shop directory and a tufting workshop offering covered in HK lifestyle press.
0.9144 m is one yard, which is consistent with a textile identity.
The identity link between that studio and the exhibitor row rests on the name and the HK market alone, so it is ASSUMED, not confirmed.

**Contradicts the sheet.** The Notes column called this an "international artist collective portfolio space".
Nothing found supports that reading; the evidenced entity is a single craft studio.
The note is not carried.

**Class: INDEPENDENT (ASSUMED).** Owner-operated craft studio with no corporate, platform or franchise parent surfaced.

**REP: unclear.** Not because an attachment was found, but because no character IP was evidenced at all: a tufting and textile workshop business is not shown to hold a character IP, and there is nothing identified to represent.
Resolving this needs the exhibitor's own CET2026 listing or a first-party statement of what IP it is exhibiting.

**Band: `lt_10k`, current-proxy.** Instagram @0.9144m, 5,187 followers, `og:description` retrieved 2026-07-31 (display name "0.9144m - 𝕋𝕖𝕩𝕥𝕚𝕝𝕖 𝕊𝕥𝕦𝕕𝕚𝕠").
Primary channel: Instagram; the Threads account of the same handle returned no count on two attempts.

**Control signals.** Solo or small owner-operated studio: ASSUMED. Label or agency attached: none surfaced (ASSUMED absent). Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://www.instagram.com/0.9144m/ - retrieved 2026-07-31, follower count from `og:description`.
- New Town Plaza shop directory entry for 0.9144m (mall operator's own directory), https://www.newtownplaza.com.hk/zh-hant/購物/0-9144m/ - the directory index resolved the tenant, the fetched page rendered the operator's shop index rather than the entry body, so this is recorded as a weaker citation than a read article.
- SundayMore, "Tufting香港Workshop手作毛氈9大推薦", 2024-04-15 - HK lifestyle publisher listing the studio's workshop offering.

### 2. Din Dong & Uncle Fish

**Identity (CONFIRMED at channel level).** The exhibitor's two characters are carried on the Instagram and Threads accounts of `Sleeping Pen` (睡睡筆), whose Threads bio is a Cantonese statement of the creative premise ("睡睡筆-意思係提醒自己，如果唔創作的話，所有筆都係曬喺度唔郁，要努力喚醒佢哋畫出令人快樂的創作！").
The account is the brand's own publisher page.

**Class: INDEPENDENT.** Creator-owned illustration brand; no corporate, platform or franchise owner surfaced.
Solo authorship is ASSUMED from the first-person Cantonese bio, not concluded.

**REP: yes.** Creator-owned, self-run channels, and neither pass surfaced a label, agency, management company or prior assignment.
The absence is a finding about what the sweep saw, not proof of no attachment.

**Band: `10k_50k`, current-proxy.** Instagram @sleepingpen, 12K followers, retrieved 2026-07-31.
Anti-drift: Threads @sleepingpen reads 3.1K (`lt_10k`) on the same identity; Instagram is the larger evidenced channel and governs, and the alternative is recorded here.
No separate per-character channel for Din Dong or Uncle Fish was found, so the brand account is correctly the read.

**Control signals.** Solo creator: ASSUMED. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced; Google News zh-HK returned nothing for this name.

**Evidence.**
- https://www.instagram.com/sleepingpen/ - retrieved 2026-07-31.
- https://www.threads.com/@sleepingpen - retrieved 2026-07-31, bio and follower count from `og:description`.

### 3. Creature Collectors Club

**Identity (CONFIRMED at channel level).** Instagram @creaturecollectorsclub, display name 不明生物俱樂部 ("Unidentified Creature Club"), a character brand account.

**Rejected candidate.** Instagram @butterpillar is an unrelated personal account (6 followers, display name "Raisin") and is not the exhibitor's character channel.
The sheet's "Butterpillar" note is therefore unverified and is not carried.

**Class: INDEPENDENT (ASSUMED).** Creator-run character brand; no corporate, platform or franchise owner surfaced.

**REP: yes.** No label, agency or management attachment surfaced in either pass; the brand runs its own channels.
Weaker than row 8: this call rests on channel evidence only, with no press to corroborate.

**Band: `10k_50k`, current-proxy.** Instagram @creaturecollectorsclub, 12K followers, retrieved 2026-07-31.
Anti-drift: Threads @creaturecollectorsclub reads 657 (`lt_10k`); Instagram is the larger evidenced channel and governs.

**Control signals.** Solo creator: ASSUMED, and weakly, since the name is a collective. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced; Google News zh-HK returned nothing for 不明生物俱樂部.

**Evidence.**
- https://www.instagram.com/creaturecollectorsclub/ - retrieved 2026-07-31.
- https://www.threads.com/@creaturecollectorsclub - retrieved 2026-07-31.

### 4. hohohola x magickira

**Unresolved, and left unresolved.**
Neither party resolved to a publisher page in either pass.
Handle probes returned false friends in every case: Instagram @hohohola (2 followers, unrelated), @hohohola_ (empty), @ho_ho_hola (0 followers, unrelated personal account), @magickira (16 followers, no posts, unrelated), @magickira_ (does not exist).
Google News zh-HK returned nothing for either name.

**Class: unresolved. REP: unclear. Band: `unknown`.**
The reason is identity, not attachment: there is nothing evidenced to classify.

**Control signals.** None assessable.

**What would resolve it.** The exhibitor's own CET2026 directory entry, or an HK press or market listing naming either party with a live channel.

### 5-6, 13-14, 22-33

Open. Not yet adjudicated in this run, and deliberately carrying no call.

### 7. Nalok.Lok

**Identity (CONFIRMED at channel level).** Instagram @naloklok, display name 奈樂樂 Nalok.Lok, an illustrator working under her own name.

**Class: INDEPENDENT.** Creator working under her own name; no corporate, platform or franchise owner surfaced, and no label imprint appears on the channel.

**REP: yes.** No label, agency or management attachment surfaced in either pass.
One adjacent press signal was found and checked: Google News zh-HK surfaced 新頭條 coverage of 《飛躍繪本》, a Hong Kong picture-book illustrator promotion programme for an international book fair.
A promotion programme is not a label, an agency or a management company, and participation in one would not change the REP call; the article was not confirmed to name this illustrator, so it is recorded as checked-and-not-relied-on rather than as evidence.

**Band: `10k_50k`, current-proxy, boundary flagged.** Instagram @naloklok, "10K" followers, retrieved 2026-07-31.
"10K" rounds from 9,500-10,499, so the true count straddles the `lt_10k` / `10k_50k` edge.
Recorded at `10k_50k` on the rounded figure with the boundary flagged, not resolved; the unrounded count was not obtainable from the crawler-served profile.

**Control signals.** Solo creator: ASSUMED. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://www.instagram.com/naloklok/ - retrieved 2026-07-31.
- 新頭條, "《飛躍繪本》- 香港繪本插畫師國際書展推廣計劃正式啟動" - surfaced via Google News zh-HK, checked as a possible attachment signal, not relied on.

### 8. 大爪作 BIGCLAWX

**The best-evidenced row in this batch.**

**Identity (CONFIRMED).** 橙新聞 (Orange News) ran a bylined exclusive interview on 2024-11-08, "搵錢呢啲嘢丨港產Figure有得炒？螯蝦達人殺入玩具界「自肥」", with Jeffery Yau, formerly in advertising and graphic design, who founded the art-toy brand 大爪作 BIGCLAWX.
Instagram @bigclawx carries his own name as the display name, which ties channel to person.

**Class: INDEPENDENT (CONFIRMED).** Founder-established, founder-owned art-toy brand.
The interview frames the brand as his own venture, made to produce the toys he wanted to make.

**REP: yes.** Creator-owned, self-run brand and channels; neither pass surfaced a label, an agency, a management company or a prior assignment.
He appears in third-party contexts as an exhibiting artist (TTF 2024 Taipei show coverage by 玩具人 TOY PEOPLE), which is exhibition, not representation.

**Band: `lt_10k`, current-proxy.** Instagram @bigclawx, 6,771 followers, retrieved 2026-07-31.
Anti-drift: this account is both the creator's and the brand's; no separate character channel exists, so no split arises.
Threads @bigclawx reads 1.5K and is the smaller channel.

**Control signals.** Solo creator: ASSUMED, strongly (the interview is with him alone about his own brand). Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- 橙新聞, 2024-11-08, https://www.orangenews.hk/exclusiveinterview/1244899/搵錢呢啲嘢丨港產Figure有得炒-螯蝦達人殺入玩具界-自肥.shtml
- 玩具人 TOY PEOPLE, 2024-10-10, TTF 2024 show report naming BIGCLAWX among exhibiting creators.
- https://www.instagram.com/bigclawx/ and https://www.threads.com/@bigclawx - retrieved 2026-07-31.

### 9. YoYo! Yogurt!! Studio

**Identity (CONFIRMED at channel level).** Instagram @yogustudi, display name "Kingyoneko yogurtstudio Kiyo", matching the exhibitor's studio name and naming an individual (Kiyo).

**Class: INDEPENDENT (ASSUMED).** Creator-run studio brand; no corporate, platform or franchise owner surfaced.

**REP: yes.** No label, agency or management attachment surfaced in either pass.
Rests on channel evidence only; no HK press was found for this studio.

**Band: `lt_10k`, current-proxy.** Instagram @yogustudi, 7,254 followers, retrieved 2026-07-31.
Threads @yogustudi exists under the same display name but returned no count on two attempts, so Instagram is the read.

**Control signals.** Solo creator: ASSUMED (one personal name on the studio account). Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://www.instagram.com/yogustudi/ - retrieved 2026-07-31.
- https://www.threads.com/@yogustudi - retrieved 2026-07-31, identity only.

### 10. EMO NEKO W.O.O.F. CLUB

**Identity (CONFIRMED at channel level).** Instagram and Threads @fingers.work, display name "Fingers Work", the studio identity behind the exhibitor's cat characters.
The sheet's note naming the characters (MIU MIU / GULU / LUBBY) is unverified prior research and is used only as a query seed; no publisher page confirming those names was reached, so they are not carried as a finding.

**Class: INDEPENDENT (ASSUMED).** Creator-run studio holding its own character set; no corporate, platform or franchise owner surfaced.

**REP: yes.** No label, agency or management attachment surfaced in either pass.

**Band: `10k_50k`, current-proxy.** Instagram @fingers.work, 22K followers, retrieved 2026-07-31.
Anti-drift note: the evidenced channel is the studio's, not a per-character channel; no separate character account was found, so no split arises.

**Control signals.** Solo creator: ASSUMED, weakly (a studio name, not a personal one). Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://www.instagram.com/fingers.work/ - retrieved 2026-07-31.
- https://www.threads.com/@fingers.work - retrieved 2026-07-31, identity only, no count served.

### 11. Ouch!! Don't Cry!!

**Unresolved on identity, and that is the finding.**

**Candidate.** `Don't Cry In The Morning`, a Hong Kong art-toy brand founded in 2013 by two Hong Kong artists, ASA & Poppy, making handmade resin and soft-vinyl toys with original characters from 2015.
That much is CONFIRMED on the brand's own site and restated on a retailer's artist page.

**Why the identity is not confirmed.** The brand's own site lists its lines as Soda Bear BoBo, Chill Fortune Cat, Ramenkun JSM, Hugger Fuku Bear and Be a good CAT!
No line called "Ouch" or "Ouch!! Don't Cry!!" appears.
The only thing linking the exhibitor row to this brand is the unverified Notes column (two-person team ASA & Poppy, resin/sofubi, est. 2014), which the method forbids carrying as a finding, and which also disagrees with the founding year the brand itself states.
So the match is a name-and-profile resemblance, not an identity.

**The Toyzeroplus test was run on the candidate, and it came back negative.**
TOYZEROPLUS carries Don't Cry In The Morning, and its own site files the brand under ARTISTS as an external artist brand rather than an in-house line, quoting the founding story verbatim.
At the same time the brand runs its own direct storefront with live HKD pricing and stock states, alongside its own Instagram.
Creator-owned with a label retail channel running concurrently with a self-run direct channel is the "label-distributed non-exclusively" branch of the pinned edge case, not the captive branch.
Had the identity been confirmed, this row would have read INDEPENDENT / REP=yes on that evidence.
It is not confirmed, so the call is not made.

**Class: unresolved. REP: unclear. Band: `unknown`.**
The candidate's channel would read `10k_50k` (Instagram @dontcryinthemorning, 21K, retrieved 2026-07-31); that figure is recorded against the candidate, not against this row.

**Control signals (against the candidate only, all ASSUMED).** Two-person team: CONFIRMED for the candidate. Label attached: a label retail channel is CONFIRMED for the candidate; exclusivity is not concluded and the direct storefront is evidence against it. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**What would resolve it.** The exhibitor's own CET2026 directory entry, or any page tying the string "Ouch!! Don't Cry!!" to a named HK creator or to the candidate brand.

**Evidence.**
- https://www.dontcryinthemorning.com/ - retrieved 2026-07-31, founding story, artist names, line-up, direct storefront.
- https://toyzeroplus.com/collections/dont-cry-in-the-morning - retrieved 2026-07-31, filed under ARTISTS as an external artist brand.
- https://www.instagram.com/dontcryinthemorning/ - retrieved 2026-07-31.

### 12. 021 Consultancy x SHIBAINC

**Identity (CONFIRMED).** SHIBAINC 柴犬工房, a Hong Kong original character brand founded in 2013 by 李頴欣 (Wing) and 鄭銘光 (DC) after they made a cartoon cup for their Shiba Inu's birthday and the response turned it into a business.
They left their jobs to run it full-time and opened their first pop-up store in 2016.
Instagram @shibainc carries the bilingual brand name.

**Class: INDEPENDENT (CONFIRMED).** The founders designed the characters, hold them, and registered trade marks in Hong Kong and the mainland after finding counterfeits abroad.
No corporate, platform or franchise owner appears anywhere in the coverage.

**Self-licensing is CONFIRMED and it is direct.**
am730's founder profile states they went to the 2017 Hong Kong International Licensing Expo, built a network of brands there, and began expanding by licensing (「2017年，他們參加了香港國際授權展，認識到不少國際品牌的網絡，並開始以授權方式拓展業務，製作更多不同的產品」), and separately that they license malls to use the characters for promotions (「柴犬工房亦與本地商場合作，授權商場使用他們的角色和精品進行推廣活動」).
The article names no licensing agent and no management company.
Campaign activity corroborates the pattern: OK便利店 (Circle K HK) ran a SHIBAINC tie-in covered by 新假期 and U Food in 2023, and 星島頭條 covered the brand's picture books in 2021.

**REP: unclear, and the reason is the exhibitor row itself.**
The attendee is listed as "021 Consultancy x SHIBAINC", which puts a consultancy on the row alongside the creator brand.
That co-listing is CONFIRMED (it is the directory string Phase 0 carried), and it is a live attachment signal.
What it means is not resolvable from any publisher page reached: whether 021 Consultancy represents SHIBAINC, co-exhibits with it, or is a separate exhibitor sharing a booth is unknown, and its scope, exclusivity and terms are refused ground.
Because a real attachment signal exists whose scope is unresolved, the rule returns `unclear` rather than `yes`.
Note what this row is not: nothing here matches the Toyzeroplus captive pattern, since the brand licenses directly and its press trail shows it dealing with brands itself.

**Band: `10k_50k`, current-proxy.** Instagram @shibainc, 15K followers, retrieved 2026-07-31.
Anti-drift: the account is the character brand's own, not a personal creator account, so the character channel is already the read.

**Control signals.** Solo creator: no, a founding pair, CONFIRMED. Label attached: none. Agency attached: ASSUMED from the exhibitor co-listing, never concluded. Already under management: not surfaced, and the am730 profile's silence on any agent is a point against it. Prior assignment visible in press: none surfaced; the press shows the founders licensing in their own name.

**Evidence.**
- am730, "創業故事｜從開心SHARE到成功創業 原創品牌「柴犬工房」的故事", https://www.am730.com.hk/article/296190
- 星島頭條, 2021-04-02, "【#慢讀樂趣】SHIBAinc原創品牌旗下柴犬繪本 搞笑內容陪過抗疫難關", https://www.stheadline.com/hot-place/1707453/
- 新假期, 2023-08-07, OK便利店 x 柴犬工房 十週年產品 (campaign coverage, HK publisher).
- U Food, 2023-12-29, OK便利店 x 柴犬工房 精品 (campaign coverage, HK publisher).
- https://www.instagram.com/shibainc/ - retrieved 2026-07-31.

### 16. CHEAP CENTURY

**Identity (CONFIRMED).** CHEAP CENTURY is the brand of Hong Kong illustrator 蘇泳康 / SOWINGHONG, whose characters are 大麻成 and 阿婆走得快.
The brand runs its own storefront at cheapcentury.com, which carries both characters as product collections, and the Facebook page is titled "Cheap Century (大麻成)".
明報 profiled him under its 大人ing column on 2024-06-05, covering how free WhatsApp stickers turned 大麻成 and 阿婆 into widely-shared characters and describing the "冤枉路" that got him there.

**Class: INDEPENDENT (CONFIRMED).** Named individual illustrator, own characters, own brand and own store.
No corporate, platform or franchise owner appears in any source reached.

**REP: yes.** Both passes were run and neither surfaced a label, an agency, a management company or a prior assignment.
The brand-side pass instead found him running brand work in his own name: 香港01 covered a 大麻成 colouring-wall weekend at 南豐紗廠 (The Mills) on 2024-09-19, and ezone covered 護瞳行動 (Orbis) partnering with 大麻成 on eye-health promotion on 2024-09-29.
Doing campaign work under his own brand name, with no intermediary named in the coverage, is the opposite of the captive pattern.

**Band: `50k_200k`, current-proxy.** Instagram @sowinghong, 141K followers, retrieved 2026-07-31.
Anti-drift: no separate 大麻成 character account was found, so the artist account is both the creator's and the characters' channel and no split arises.
Instagram @cheapcentury exists but is empty (0 followers, 0 posts) and is not the read; @cheapcentury.hk and @cheapcentury_hk do not exist.

**Control signals.** Solo creator: ASSUMED, strongly (a bylined single-artist profile). Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced; the campaign coverage names the artist and the character directly.

**Evidence.**
- 明報 (Ming Pao, Toronto edition of the same title), 2024-06-05, 大人ing："貼圖走紅背後︰一個插畫師的「冤枉路」", http://www.mingpaocanada.com/tor/htm/News/20240605/HK-gfh2_er_r.htm
- 香港01, 2024-09-19, "去南豐紗廠過一個油牆週末！為超人氣角色大麻成填上色彩！"
- ezone.hk, 2024-09-29, "大麻成現身荃灣南豐紗廠！護瞳行動攜手大麻成推廣護眼知識"
- https://www.cheapcentury.com/ - the brand's own storefront, both characters as collections.
- https://www.instagram.com/sowinghong/ - retrieved 2026-07-31.

### 17. Shadoowww

**Thin, and recorded as thin.**

**Identity (partial).** Threads @shadoowww__ resolves to a profile whose display name is "Shadow Chan", consistent with the exhibitor name.
That is the only channel that resolved.
Instagram @shadoowww (1 follower) and @shadoowww_ (47 followers, display name "USER") are unrelated accounts and are rejected.
Google News zh-HK returned nothing.

**Class: INDEPENDENT (ASSUMED).** A single-person illustration identity with no corporate, platform or franchise owner surfaced.
The assumption rests on the profile alone.

**REP: unclear.** Not an attachment finding: the row simply has too little evidence to call.
One channel with no follower count served, no storefront reached, no press, and no character identified.

**Band: `unknown`.** The Threads profile served an empty `og:description` on both attempts, so no count was obtained, and no Instagram account was confirmed.

**Control signals.** Solo creator: ASSUMED. Label or agency attached: not assessable. Already under management: not assessable. Prior assignment visible in press: no press found.

**What would resolve it.** The exhibitor's own CET2026 directory entry, or an Instagram or storefront link from the Threads profile body.

**Evidence.**
- https://www.threads.com/@shadoowww__ - retrieved 2026-07-31, identity only.

### 18. club babo

**Identity (CONFIRMED).** Capital 資本平台 ran a profile on 2025-03-24, "專訪本地文化創意團隊 Club Babo：Mr Flat Cat的白日夢與香港的日常哲學", identifying Club Babo as a Hong Kong creative team and Mr Flat Cat as its character.
Instagram and Threads @club_babo carry the same identity, with a Threads bio reading "illustration/ toy design/ apparel".

**Class: INDEPENDENT (CONFIRMED at team level).** A local creative team with its own character; no corporate, platform or franchise owner surfaced.

**REP: yes.** Neither pass surfaced a label, an agency, a management company or a prior assignment.
The brand-side pass found the team in market and fair listings (PMQ 玩嘢祭 2026 coverage by 港生活, 香港插畫及文創展 coverage by 香港01), which is exhibiting, not representation, and is treated as such.

**Band: `10k_50k`, current-proxy.** Instagram @club_babo, 27K followers, retrieved 2026-07-31.
Anti-drift: Threads @club_babo reads 8.9K (`lt_10k`) on the same identity; Instagram is the larger evidenced channel and governs, and the alternative is recorded.
No separate Mr Flat Cat channel was found, so the team account is the read.

**Control signals.** Solo creator: no, described as a team, CONFIRMED. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- Capital 資本平台, 2025-03-24, "專訪本地文化創意團隊 Club Babo：Mr Flat Cat的白日夢與香港的日常哲學"
- https://www.instagram.com/club_babo/ and https://www.threads.com/@club_babo - retrieved 2026-07-31.

### 19. Genie Li

**Identity (CONFIRMED at channel level).** Instagram @genieee.hk, display name 廢青豬妮Genie｜香港插畫, an illustrator working under her own name with a named character (廢青豬妮).

**Class: INDEPENDENT (ASSUMED).** Creator working under her own name; no corporate, platform or franchise owner surfaced.

**REP: yes.** Neither pass surfaced a label, an agency, a management company or a prior assignment.
Rests on channel evidence; no HK press was found for this name.

**Band: `10k_50k`, current-proxy.** Instagram @genieee.hk, 15K followers, retrieved 2026-07-31.
Anti-drift: the account carries the creator's name and the character's name together and there is no separate character channel, so no split arises.
Threads @genieee.hk exists under the same display name but served no count.

**Control signals.** Solo creator: ASSUMED. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://www.instagram.com/genieee.hk/ - retrieved 2026-07-31.
- https://www.threads.com/@genieee.hk - retrieved 2026-07-31, identity only.

### 20. Venus Philosophy

**Identity (CONFIRMED at channel level).** Instagram @venusphilosophy, display name LOSZEHAHA, matching the exhibitor's brand and artist identity.

**Rejected candidate.** Instagram @loszehaha is an unrelated near-empty account (35 followers, 4 posts) and is not the artist's channel; the artist identity sits on the brand handle instead.

**Class: INDEPENDENT (ASSUMED).** Creator-run brand under a single artist identity; no corporate, platform or franchise owner surfaced.

**REP: yes.** Neither pass surfaced a label, an agency, a management company or a prior assignment.
Rests on channel evidence; no HK press was found.

**Band: `10k_50k`, current-proxy.** Instagram @venusphilosophy, 17K followers, retrieved 2026-07-31.

**Control signals.** Solo creator: ASSUMED. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://www.instagram.com/venusphilosophy/ - retrieved 2026-07-31.

### 21. TOBALLKIDRAWING

**Identity (CONFIRMED).** 星島頭條 ran a bylined interview on 2023-08-15, "治癒系插畫師杜波淇 以「肥教主」溫暖人心 盼每個人用自己喜歡的方式生活｜專訪", identifying 杜波淇 (toballki) as the illustrator behind 肥教主.
Instagram and Threads @toballkidrawing carry the display name 杜波淇 | toballki.

**Class: INDEPENDENT (CONFIRMED).** Named individual illustrator with her own character.
No corporate, platform or franchise owner appears in the coverage.

**REP: yes.** Neither pass surfaced a label, an agency, a management company or a prior assignment.
The brand-side pass found her in a curated Taiwan pop-up: MOT TIMES and XINMEDIA covered 中島 GLAb's 《G Express》 in April 2023, which brought five Hong Kong creator brands to Taichung.
A curated retail pop-up that groups several independent brands for one event is a retail channel, not representation, and it does not move the call; it is recorded because it is the only third-party channel signal on this row.

**Band: `10k_50k`, current-proxy.** Instagram @toballkidrawing, 22K followers, retrieved 2026-07-31.
Anti-drift: Threads @toballkidrawing reads 8.3K (`lt_10k`) on the same identity; Instagram is the larger evidenced channel and governs.
No separate 肥教主 channel was found, so the artist account is the read.

**Control signals.** Solo creator: ASSUMED, strongly (a bylined single-artist interview). Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- 星島頭條, 2023-08-15, "治癒系插畫師杜波淇 以「肥教主」溫暖人心 盼每個人用自己喜歡的方式生活｜專訪"
- MOT TIMES 明日誌, 2023-04-27, "中島 GLAb 新企劃《G Express》快閃店！集結 5 組香港新生代創作快遞來台開展"
- XINMEDIA 欣傳媒, 2023-04-28, same pop-up, independent second publisher.
- https://www.instagram.com/toballkidrawing/ and https://www.threads.com/@toballkidrawing - retrieved 2026-07-31.

## Counts

Deliberately empty.
No representable-vs-captive number is stated while rows remain open, because a partial count of an unfinished adjudication would be read as an outcome.
The counts section is written once all 32 rows carry a call.

## Refusals applied

- No rights_owner, chain of title, territory, exclusivity or deal terms is concluded anywhere above.
  Where exclusivity was the natural next question (rows 11 and 12), the file says so and stops.
- No outcome numbers, and none implied.
  The counts section stays empty until the adjudication is complete.
- No HK indie share is stated, computed or hinted at.
  This file is internal only and the HK share is not quotable on its own in any case.
- No brand images fetched.
- No levels or ladder vocabulary.
- Pinned edge cases applied: the Toyzeroplus test was run explicitly on row 11's candidate and returned non-exclusive, which is recorded as a negative result rather than suppressed; the 咖波 precedent (agency-managed but creator-owned is still independent) is what keeps row 12 INDEPENDENT despite the consultancy co-listing; self-presentation is not ownership, which is why rows 3, 9 and 10 carry ASSUMED class calls rather than confirmed ones.
- Unresolved rows (4, 11) are left unresolved with the reason and the resolving evidence named.
- The exhibitor sheet's Notes column was used only as a query seed; where it was contradicted (rows 1, 3) or unconfirmed (rows 10, 11) that is recorded and the note is not carried.

## Method notes for the remaining rows

Recorded so the rest of the pass runs the same way.

1. **Handle probing beats search for this population.** These are small HK creator brands with thin press. Fetching `instagram.com/<handle>` and `threads.com/@<handle>` with a Googlebot user agent returns the follower count and often the bio in `og:description`, which resolves both identity and band in one call. Threads is a newly useful channel here: its profile `og:description` carries "N Followers - M Threads - <bio>", though it serves an empty description on a substantial share of attempts and needs a retry.
2. **False friends are the main hazard.** Eight of the sixteen rows adjudicated so far had at least one plausible handle that turned out to be an unrelated or empty account, several with single-digit follower counts. A handle is only accepted when the display name or bio independently matches the exhibitor.
3. **Google News RSS with `hl=zh-HK&gl=HK` is the press index**, as in the HK census. It found usable press for five of the sixteen and nothing for the rest, which is itself informative about this population's press depth: most of these creators are channel-visible and press-invisible.
5. **The character-vs-creator anti-drift split is rare in this population and the platform split is common.** Almost none of these creators run a separate character account, so the HK bands pass's hardest case barely arises here. What does arise on nearly every row is Instagram-versus-Threads: the same identity typically reads two to three times larger on Instagram, so the larger evidenced channel governs and the alternative is recorded, exactly as the census rule requires.
4. **Web search resolves the article better than the aggregator redirect.** Searching the exact headline returns the publisher URL directly, which sidesteps the blocked Google News resolver.
