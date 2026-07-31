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

No count was stated until every row was adjudicated.
The register below is the record; the counts section was held empty by design until the last row carried a call, and is now written.
All 32 rows carry a class, a REP call and a reason.

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
| 5 | Pure Studio | INDEPENDENT | yes | founder-owned studio, CONFIRMED on its own site and an incubator page; carries its own named brand properties; no label, agency or management surfaced | `10k_50k` | current-proxy |
| 6 | Nine Four Sixty X Dino Valley | unresolved | unclear | neither co-listed party resolved to a publisher page; every candidate handle is a false friend | `unknown` | unknown |
| 7 | Nalok.Lok | INDEPENDENT | yes | named illustrator working under her own name; no label or agency surfaced | `10k_50k` | current-proxy |
| 8 | 大爪作 BIGCLAWX | INDEPENDENT | yes | founder-owned art-toy brand, CONFIRMED in a bylined interview; no label or agency surfaced | `lt_10k` | current-proxy |
| 9 | YoYo! Yogurt!! Studio | INDEPENDENT | yes | creator-run studio brand (ASSUMED); no label or agency surfaced | `lt_10k` | current-proxy |
| 10 | EMO NEKO W.O.O.F. CLUB | INDEPENDENT | yes | creator-run character set under one studio identity (ASSUMED); no label or agency surfaced | `10k_50k` | current-proxy |
| 11 | Ouch!! Don't Cry!! | unresolved | unclear | strongest candidate identity is not confirmed; the candidate's own line-up does not carry this name | `unknown` | unknown |
| 12 | 021 Consultancy x SHIBAINC | INDEPENDENT | unclear | creator-owned and self-licensing, CONFIRMED; but a consultancy is co-listed on the exhibitor row itself and its scope is not resolvable | `10k_50k` | current-proxy |
| 13 | 無盡創意設計工作室 | unresolved | unclear | the sheet's own link resolves to a toy-design studio, but nothing independently ties that studio to this exhibitor name | `unknown` | unknown |
| 14 | FIGTION | unresolved | unclear | no channel or press resolved; the artist-side pass on the named collaborators did not corroborate the sheet's note | `unknown` | unknown |
| 16 | CHEAP CENTURY | INDEPENDENT | yes | named illustrator, own characters, own storefront, brand campaigns run in his own name; no agent named in press | `50k_200k` | current-proxy |
| 17 | Shadoowww | INDEPENDENT | unclear | one channel resolved and nothing else; too thin to call either way | `unknown` | unknown |
| 18 | club babo | INDEPENDENT | yes | creator team with its own character and self-run channels, CONFIRMED in a bylined profile; no agency surfaced | `10k_50k` | current-proxy |
| 19 | Genie Li | INDEPENDENT | yes | illustrator working under her own name with her own character; no label or agency surfaced | `10k_50k` | current-proxy |
| 20 | Venus Philosophy | INDEPENDENT | yes | creator-run brand under one artist identity; no label or agency surfaced | `10k_50k` | current-proxy |
| 21 | TOBALLKIDRAWING | INDEPENDENT | yes | named illustrator with her own character, CONFIRMED in a bylined interview; no label or agency surfaced | `10k_50k` | current-proxy |
| 22 | ARDUREY LIMITED | PORTFOLIO | no | the attendee is itself an artist licensing agency, CONFIRMED on its own site; it is the representation layer, not a creator | `unknown` | unknown |
| 23 | cheeky cheeky | INDEPENDENT | yes | named designer's own character (厚面子) running mall and pop-up campaigns in its own name; no agent named in the coverage | `lt_10k` | current-proxy |
| 24 | HEREAFTER STUDIO | INDEPENDENT | unclear | design-goods brand; no character IP evidenced, so nothing identified to represent | `10k_50k` | current-proxy |
| 25 | HANDMADESHIP | INDEPENDENT | unclear | design-goods brand; no character IP evidenced, so nothing identified to represent | `10k_50k` | current-proxy |
| 26 | Scentory | INDEPENDENT | unclear | fragrance brand; no character IP evidenced, so nothing identified to represent | `lt_10k` | current-proxy |
| 27 | Bethel | INDEPENDENT | unclear | handbag brand, own-design origin CONFIRMED first-party; no character IP evidenced | `10k_50k` | current-proxy |
| 28 | paper diamond® | INDEPENDENT | unclear | founder-run paper-art and jewellery brand, CONFIRMED; no character IP evidenced | `lt_10k` | current-proxy |
| 29 | DDED | INDEPENDENT | yes | creator-run character and art-toy brand with its own channels; no label, agency or management surfaced in either pass | `10k_50k` | current-proxy |
| 30 | Tse Sai Pei | INDEPENDENT | yes | illustrator working under their own name with their own storefront; no label or agency surfaced | `50k_200k` | current-proxy |
| 31 | Overloaddance | INDEPENDENT | yes | creator-run toy, comic and illustration studio; no label or agency surfaced | `lt_10k` | current-proxy |
| 32 | Mr n Mrs Moon | INDEPENDENT | yes | creator-pair character brand with its own store and brand tie-ins run in its own name; no agent named | `200k_1m` | current-proxy |
| 33 | Lewa Lee | INDEPENDENT | yes | named creator (阿華), called an independent studio in HK press, with a direct brand collaboration and no agent named | `50k_200k` | current-proxy |

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

### 5. Pure Studio

**The only row in the final batch that resolved, and the best-documented row in the register on ownership.**

**Identity (CONFIRMED).** Pure Studio, a Hong Kong studio founded in 2018, own site at `purestudio.hk`.
The Hong Kong Design Centre's Design Incubation Programme carries its own page for the company naming two founders, Au-Yeung Chun Hay and Tse Ka Yee, and the same 2018 founding date.
The studio's own site links out to `instagram.com/purehay/` and `facebook.com/AuYeungChunHay/` as its channels, and the Facebook page's own title is `Purehay - 禧之插畫世界`, which ties the studio, the founder and the channel together first-party.

**A generic name that was checked before it was accepted.** `@purestudio` (4 followers, no display name), `@pure_studio` (2 followers, no display name) and `@purestudio.hk` (empty display name, no count served) are all dead or unrelated; the accepted channel came from the studio's own site rather than from a handle guess.

**Class: INDEPENDENT.** Founder-owned: two named individual founders on the incubator page and no corporate, platform, estate or franchise owner anywhere in either pass.

Recorded rather than concluded: this is substantially a service studio.
Its own site describes "Illustration Art, movie picture, advertisement, pre-production for animation and games and brand development", which means a large part of its output is client work made to order.
That raises MIXED as an alternative reading, and it is rejected here for a stated reason: the attendee's own properties are the ones it carries, and its site lists two under Brand Development - `Eternal Palace` and `Big Bun Spiritual Card`.
Client pre-production work is not IP this attendee carries, so it does not make the row MIXED.
Whether any client work was assigned away is exactly the chain-of-title question this run refuses, and it is not answered.

**REP: yes.** Creator-owned, at least one confirmed self-run channel, own named brand properties, and no label, agency or management attachment surfaced in either pass.

One adjacent signal was found and checked rather than ignored: the studio sits on the Hong Kong Design Centre's Design Incubation Programme roster.
An incubation programme is a public support scheme, not a label, an agency or a management company, and it is treated exactly as row 7's book-fair promotion programme was - checked, named, and not treated as an attachment.
This is stated so that the `yes` is not read as "nothing was found", when in fact something was found and assessed.

**Band: `10k_50k`, current-proxy.** Instagram `@purehay`, display name `PureHay Art 🇭🇰`, 11K followers, retrieved 2026-07-31.
Anti-drift: no separate studio-branded channel exists, so the founder's artist channel is the studio's evidenced channel and there is no character-versus-creator split to resolve.
Cross-check: the linked Facebook page carries 6,235 likes, which is a smaller number on a different metric and does not move the band; the Instagram count governs and the Facebook figure is recorded, not averaged.
The two named brand properties have no separate channel evidenced.

**Control signals.** Solo creator: no - two named co-founders, CONFIRMED on the incubator page, so this row is a founder pair rather than a solo creator. Label or agency attached: none surfaced; an incubation programme was found and is not one. Already under management: none surfaced. Prior assignment visible in press: none surfaced, and the studio's client-service line is recorded above as a reason to expect the question rather than as an answer to it. All four remain ASSUMED and none is concluded.

**Evidence.**
- https://www.purestudio.hk/ - the studio's own site: founding year, service description, and the Brand Development entries. Retrieved 2026-07-31.
- https://hkdesignincubation.org/?category=2&company=376&route=incubation_inner - Hong Kong Design Centre incubation page: company name, both founders, 2018. Retrieved 2026-07-31.
- https://www.instagram.com/purehay/ - retrieved 2026-07-31.
- https://www.facebook.com/AuYeungChunHay/ - page title `Purehay - 禧之插畫世界`, like count. Retrieved 2026-07-31.

### 6. Nine Four Sixty X Dino Valley

**Unresolved, and left unresolved.**
Neither co-listed party resolved to a publisher page in either pass.

**What was checked.**
EN and zh-HK web search on both names, together and separately, returned nothing for either: the `Nine Four Sixty` queries surfaced only unrelated Hong Kong leather workshops, and the `Dino Valley` queries surfaced only unrelated dinosaur-themed products.
Google News zh-HK (percent-encoded) returned no matching headline for either name.
Handle probes were run across both spellings and returned false friends or nothing: Instagram `@ninefoursixty`, `@nine_four_sixty`, `@ninefoursixty.hk`, `@ninefoursixty_`, `@ninefoursixtyhk`, `@nine460`, `@9460leather`, `@leather946`, `@nfsxdinovalley` (none exist), `@946_0` (10 followers, no posts, unrelated), `@nfs946` (1 follower, no posts, no display name), `@n946` (John Grijalva, unrelated), `@dinovalley` (Deena Gregory, 36 followers, unrelated), `@dino_valley` ("The Land of spam", 2 followers, unrelated), `@dinovalley.hk` and `@dinovalley.tw` (do not exist); Facebook `/ninefoursixty` and `/NineFourSixty` served nothing.

**Class: unresolved. REP: unclear. Band: `unknown`.**
The reason is identity, not attachment: there is nothing evidenced to classify.

**One hypothesis was tested and is recorded because it would matter, not because it holds.**
The exhibitor string is a co-listing (`X`), the same shape as row 12, so the second party is the natural place to look for an attachment signal.
The Phase 0 sheet's Taiwan section carries #277 `恐龍山丘文化創意有限公司 (Dino Valley Creative)`, typed Agency, and a Taiwan entity of that name does exist: `dinovalley.com.tw`, a Facebook page `恐龍山丘 | Taichung`, and Instagram `@dinovalley2021` (0 followers, 54 posts).
If the `Dino Valley` on this Hong Kong row were that entity, the row would be a creator co-listed with an agency and would sit in the same unresolved-scope position as row 12.
It is not carried, for three reasons: the sheet describes this row as a leather craft brand and nothing connects a leather craft brand to the Taiwan entity; the Taiwan entity's own site could not be read (its TLS certificate has expired) so its business was never confirmed first-party; and the first party, `Nine Four Sixty`, never resolved at all, so there is no creator side to attach anything to.
Recorded as a checked-and-rejected hypothesis so that it is not silently lost, and so that no later reader re-derives it as a finding.

**Control signals.** None assessable.

**What would resolve it.** The exhibitor's own CET2026 directory entry once the organiser publishes the exhibitor list, or a Hong Kong press or market listing naming either party with a live channel.

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

### 13. 無盡創意設計工作室

**Unresolved, and left unresolved - the row where the sheet's own link resolved and still did not settle the identity.**

**What was checked.**
This is the one open row whose Notes column carried a live link rather than a handle: `facebook.com/share/18yLz9fE91`.
Followed with a crawler user agent, it redirects to a real Hong Kong Facebook page - `N9thstudio | Hong Kong`, 6 likes, self-description `N°9THSTUDIO`.
That page's brand resolves further: Instagram `@n9thstudio`, display name `N°9TH STUDIO`, 3,833 followers, 243 posts, bio `Toy Design | 3D Artist`, and a matching Threads profile under the same handle.
The sheet's other seeds were probed too: Instagram `@kailamchan` is a 2-follower personal account with no connection to a studio, and Google News zh-HK returned nothing for either `無盡創意設計工作室` or `N9THSTUDIO`.
Web search on the exhibitor name and on the studio name each returned nothing on-target.

**Why the candidate is not accepted.**
The method's rule is that a channel is accepted only when the display name or bio independently matches the exhibitor, and nothing here does.
Neither the Facebook page name, the Instagram display name nor the bio carries `無盡創意設計工作室`, and none names Kailam Chan.
The candidate's own two channels also disagree about where it is: the Facebook page is titled Hong Kong, while the Instagram bio lists Tokyo, Taipei and Kaohsiung and states an affiliation with a differently-named studio.

Two readings survive and neither can be discharged from the evidence available.
Either `無盡創意設計工作室` is the registered Chinese company name behind the `N°9TH STUDIO` trading name, which is an ordinary Hong Kong arrangement and would make the link correct; or the sheet's link is simply attached to the wrong row, which has already happened twice in this run on other fields.
The run's own rule about the Notes column - query seed only, never carried as a finding - decides it: the link points somewhere, but nothing independent confirms it points here.

**Class: unresolved. REP: unclear. Band: `unknown`.**
The reason is identity, not attachment.
The candidate's follower count is deliberately not carried into the band; adopting it would import the whole unverified identification through the back door.

**A conditional signal, recorded and not carried.** If the candidate ever is confirmed as this exhibitor, its own Instagram bio states an affiliation with another named studio, and that affiliation's scope would then have to be resolved before any REP call - which would put the row in row 12's position rather than in a clean `yes`. This is conditional on an identification that has not been made, and it is not counted as an attachment signal anywhere in this file.

**Control signals.** None assessable.

**What would resolve it.** A first-party page carrying both names together - the studio's own site or shop, a Hong Kong Companies Registry entry, or the exhibitor's own CET2026 directory entry.

### 14. FIGTION

**Unresolved, and left unresolved.**

**What was checked.**
Instagram `@figtion` resolves but to `maria | fig🎵`, an unrelated individual; `@figtion_` is a private LEGO-collector account whose bio reads `#afol #legominifigurecollector #toystoryfan`, with no Hong Kong or brand connection; `@figtion.official` (9 followers, 0 posts) and `@figtion.studio` (6 followers, 12 posts) are both too empty to identify and neither carries anything tying it to this exhibitor; `@figtionhk`, `@figtion.hk`, `@figtion.hk_`, `@thefigtion`, `@figtionstudio`, `@figtion.toy` and `@figtiontoys` do not exist.
Facebook `/figtion`, `/figtionhk` and `/figtion.hk` served nothing.
Google News zh-HK on `FIGTION 香港` (percent-encoded) returned only unrelated noise on similarly-spelled titles.
EN and zh-HK web search on the brand plus NFC, Web3, collectibles and 潮玩 returned general market coverage and nothing on this name.

**The artist-side pass is what makes this a real negative rather than a thin one.**
The sheet's note claims collaborations with two named parties, so those were run artist-side, which this run treats as the mandatory pass.
`Deepsico Club` resolved to a genuine creator account - Instagram `@deepsicoclub`, 388 followers, a bio describing six aquatic characters, posts running October to November 2022 - and that account's own profile names no producer, no platform and no collaborator, FIGTION included.
`Blossom Man` did not resolve: `@blossomman` is an unrelated personal account.
So the one route that could have identified this exhibitor from the creator side was open, was taken, and returned nothing.

**Class: unresolved. REP: unclear. Band: `unknown`.**
The reason is identity, not attachment.
Nothing here is evidence that the sheet's note is wrong; it is evidence that the note is unverified, and an unverified note is not carried.

**Control signals.** None assessable.

**What would resolve it.** The exhibitor's own site or storefront, its own CET2026 directory entry, or either named collaborator's own channel naming it.

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

### 22. ARDUREY LIMITED

**The one row on this list that is the representation layer rather than a creator.**

**Identity (CONFIRMED).** ARDUREY's own site describes the company verbatim as "a one-stop shop global artist licensing agency that represents emerging artists and illustrators. We connect brands with talents, curating and managing some of the most recognizable creative crossover projects."
The HKTDC supplier directory carries an Ardurey Limited entry, and the company's own site gives a San Po Kong, Kowloon address.
The exhibitor sheet's own annotation on this row ("agency") is consistent with what the site says, which is the one place in this run where the sheet and the evidence agree; the finding still rests on the site, not the sheet.

**Class: PORTFOLIO.** The entity is a corporate agency presenting a roster of third-party artists.
This is a call about ARDUREY, not about its roster: the roster artists are separately creator-owned and nothing here says ARDUREY owns their IP.
No rights_owner or chain-of-title conclusion is drawn, and none is available from what was read.

**REP: no.** This is the second branch of the stated rule, applied for the first time in this run: the attendee is itself a licensing agency rather than a creator, so there is no creator-side IP on this row to represent.
That is a structural `no`, not a captivity finding, and it must not be counted as one.

**Roster checked against the other 31 rows, and it does not intersect.**
The artists named on ARDUREY's own site are MATSUI, INAPSQUARE, SHINICHIRO INUI, YEYE and Tomason.
None of them is any of the other 31 Hong Kong attendees.
This was the most direct attachment test available in this run - an actual HK representation agency exhibiting in the same hall as 31 creators - and it returned no overlap on the artists the agency itself lists.
The absence is only as complete as the roster page, which may not be exhaustive; that limit is stated rather than assumed away.

**Band: `unknown`.** An agency's own following is not an IP's channel following, and no IP channel belongs to this row.
Recording an agency's follower count as a band would be a category error, so it is left `unknown` rather than filled in.

**Control signals.** Solo creator: no, a company. Label or agency attached: the row *is* the agency. Already under management: not applicable. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://www.ardurey.com/ - retrieved 2026-07-31, self-description and roster.
- https://sourcing.hktdc.com/en/Supplier-Store-Directory/Ardurey-Limited/1S00O1D72 - HKTDC's own supplier directory entry.

### 23. cheeky cheeky

**The best-evidenced self-licensing row in this batch.**

**Identity (CONFIRMED).** The Facebook page cheekycheeky.hk is titled "Cheeky cheeky 厚面子" and its own description reads 設計師 (designer), tying the exhibitor to the character 厚面子.
No Instagram account resolved: @cheekycheeky is an empty account under an unrelated display name (0 followers, 0 posts), and @cheekycheeky.hk, @cheekycheekyhk, @cheeky_cheeky_hk and @cheekycheekyhongkong do not exist.
Threads has no account on either handle.
This row is Facebook-primary, which is unusual in this population.

**Class: INDEPENDENT (ASSUMED).** A designer's own character brand; no corporate, platform or franchise owner surfaced.
The sheet names the designer as Pok Li; that is a query seed only and no publisher page reached confirmed the name, so it is not carried.

**REP: yes, and the campaign trail is the reason.**
The brand-side pass found 厚面子 running named campaigns as itself: MOKO 新世紀廣場 x Cheeky Cheeky 「厚面的愛抱抱節」 (Yahoo 活動街), a 星島頭條 reader giveaway of MOKO x Cheeky Cheeky red packets and calendar cards, a Marketoo x Cheeky Cheeky Easter pop-up at 中環街市 (Time Out Hong Kong), a 白紙市集 x Cheeky Cheeky x The GenZ Fest Christmas market (nmplus.hk), and a 明報 家家有禮 item on 厚面子 appearing as 財神 at Chinese New Year.
Five publishers, four separate commercial deployments, and no intermediary named in any of them.
A mall, a market operator and a retail pop-up organiser are counterparties, not representatives.

**Band: `lt_10k`, current-proxy, weaker basis than the rest of this batch.**
Facebook page likes, 1,381, retrieved 2026-07-31.
Page likes are not follower counts and Facebook is the only channel that resolved, so this band rests on a proxy of a proxy; it is recorded at `lt_10k` because the figure is an order of magnitude clear of the boundary, not because the measure is good.
Note the mismatch this row carries: the campaign trail is the strongest in the batch while the channel is the smallest, which is a reminder that band and licensing activity are separate readings.

**Control signals.** Solo creator: ASSUMED (the page describes a designer, singular). Label or agency attached: none surfaced across five publishers. Already under management: none surfaced. Prior assignment visible in press: none surfaced; the campaigns name the character and the brand directly.

**Evidence.**
- https://www.facebook.com/cheekycheeky.hk - retrieved 2026-07-31, page title, self-description and like count.
- Yahoo 活動街, "新年好去處｜旺角MOKO新世紀廣場x Cheeky Cheeky「厚面的愛抱抱節」5大打卡位陪你迎新年".
- 星島頭條, "會員獎賞｜《星島頭條》APP送MOKO x Cheeky Cheeky利是封及火柴盒造型年曆卡30套".
- Time Out Hong Kong, "香港的Marketoo x Cheeky Cheeky 中環街市復活節 Pop-up Store".
- 明報 Our Lifestyle, 2023-01-10, 家家有禮："喜迎新春 厚面子化身財神".
- nmplus.hk, "白紙市集x Cheeky Cheeky厚面子x The GenZ Fest - 聖誕厚MK總動員".

### 24. HEREAFTER STUDIO

**Identity (CONFIRMED at channel level).** Instagram and Threads @hereafter.studioo both carry the display name ✥ 後來的 ✥ 𝐇𝐞𝐫𝐞𝐚𝐟𝐭𝐞𝐫 𝐒𝐭𝐮𝐝𝐢𝐨, and the Facebook page is titled 後來的 Hereafter Studio.
誠品 (eslite) carries a 後來的 / Hereafter Studio cooperation-brand page on its own 迷誠品 site, in both its HK and TW editions, and the brand runs its own storefront at hereafter-studio.com.
The sheet's Threads handle was correct and is the one confirmed lead in this batch that came from the Notes column.

**Rejected candidate.** Instagram @hereafter.studio (one `o`) is a different, near-empty account (390 followers, 3 posts) under a different display name and is not this brand.

**Class: INDEPENDENT (ASSUMED).** A Hong Kong design studio running its own retail and its own channels; no corporate, platform or franchise owner surfaced.
No founder name was confirmed from any publisher page.

**REP: unclear, and the reason is the same as row 1: there is no character IP evidenced to represent.**
What the evidence shows is a design-goods brand - phone cases and lifestyle goods carrying Hong Kong themes - sold through its own store, a workshop unit in Lai Chi Kok and a 誠品 counter in Tsim Sha Tsui.
Nothing found identifies a character or a licensable property.
This is not an attachment finding: no label, agency or management surfaced either.

**The 誠品 relationship was tested and it is retail, not representation.**
誠品's cooperation-brand page is a stocking listing on a bookstore chain's own site while the brand's direct storefront runs concurrently, which is the same non-exclusive shape the Toyzeroplus test returned on row 11's candidate.

**Band: `10k_50k`, current-proxy.** Instagram @hereafter.studioo, 26K followers, retrieved 2026-07-31.
Anti-drift: the account is the studio's own and no separate product-line channel exists, so no split arises.
Threads @hereafter.studioo served no count on three attempts.

**Control signals.** Solo creator: not assessable, the identity is a studio. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: no press found; Google News zh-HK returned only unrelated 誠品 store coverage.

**Evidence.**
- https://www.instagram.com/hereafter.studioo/ and https://www.threads.com/@hereafter.studioo - retrieved 2026-07-31.
- https://www.facebook.com/hereafter.studioo - retrieved 2026-07-31, page title.
- https://meet.eslite.com/hk/tc/cooperationbrand/202106170001 - 誠品's own cooperation-brand page.
- https://hereafter-studio.com/ - the brand's own storefront.

### 25. HANDMADESHIP

**Identity (CONFIRMED at channel level).** Instagram and Threads @handmadeship both carry the display name HANDMADESHIP®, and the Facebook page handmadeshipship is titled Handmadeship.
Both handles in the sheet's Notes column were correct.

**Class: INDEPENDENT (ASSUMED).** A Hong Kong handmade-goods brand; no corporate, platform or franchise owner surfaced and no founder name was confirmed from a publisher page.

**REP: unclear, on the row-1 ground.** The evidenced business is handmade goods built on Hong Kong nostalgia objects, sold through its own channels and a Central Market shop.
No character IP was evidenced, so nothing is identified to represent.
No label, agency or management surfaced either, so this is an absence-of-property finding, not an attachment finding.

**Press checked and not relied on.** Google News zh-HK returned an etnet 經濟通 piece on Hong Kong handmade brands drawing on local culture and a 明報 piece on training and licensing support for Hong Kong IP; neither was confirmed to name this brand, so both are recorded as checked rather than cited.

**Band: `10k_50k`, current-proxy.** Instagram @handmadeship, 14K followers, retrieved 2026-07-31.
Threads @handmadeship served no count on three attempts.

**Control signals.** Solo creator: not assessable. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: no confirmed press.

**Evidence.**
- https://www.instagram.com/handmadeship/ and https://www.threads.com/@handmadeship - retrieved 2026-07-31.
- https://www.facebook.com/handmadeshipship/ - retrieved 2026-07-31, page title.

### 26. Scentory

**Identity (CONFIRMED at channel level).** Instagram @scentoryhk and the Facebook page scentoryhk both carry the display name 香言 Scentory.

**Class: INDEPENDENT (ASSUMED).** A Hong Kong fragrance brand; no corporate, platform or franchise owner surfaced.
The sheet names a founder (Vanessa Choi); that is a query seed only, no publisher page reached confirmed it, and it is not carried.

**REP: unclear, on the row-1 ground.** A fragrance brand with no character IP evidenced has nothing identified to represent.
Google News zh-HK returned nothing for this brand on the queries run, so the row rests entirely on its own channels.
No label, agency or management surfaced.

**Band: `lt_10k`, current-proxy.** Instagram @scentoryhk, 3,034 followers, retrieved 2026-07-31.
Threads @scentoryhk served no count on three attempts.

**Control signals.** Solo creator: not assessable. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: no press found.

**Evidence.**
- https://www.instagram.com/scentoryhk/ - retrieved 2026-07-31.
- https://www.facebook.com/scentoryhk - retrieved 2026-07-31, page title.

### 27. Bethel

**Identity (CONFIRMED).** The Facebook page bethelofficial.hk is titled Bethel and its own description reads 香港品牌Bethel，原創設計始於2013年 ("Hong Kong brand Bethel, original design since 2013"), which is a first-party statement of origin rather than an inference.
Instagram @bethelofficial.hk carries the same display name.

**Class: INDEPENDENT (ASSUMED).** The own-design origin is confirmed first-party; the ownership structure behind it is not stated anywhere reached, so the class call stays ASSUMED.
No corporate, platform or franchise owner surfaced.

**REP: unclear, on the row-1 ground.** The evidenced business is handbags and accessories.
No character IP was evidenced, so nothing is identified to represent.
No label, agency or management surfaced.

**Band: `10k_50k`, current-proxy.** Instagram @bethelofficial.hk, 13K followers, retrieved 2026-07-31.
Cross-check: the Facebook page reads 12,358 likes, the same order, which is unusual in this population and is recorded because it makes the band unusually safe.

**Control signals.** Solo creator: not assessable, a brand identity. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced; Google News zh-HK returned only a 誠品 clearance-sale listing.

**Evidence.**
- https://www.instagram.com/bethelofficial.hk/ - retrieved 2026-07-31.
- https://www.facebook.com/bethelofficial.hk - retrieved 2026-07-31, page title, self-description and like count.

### 28. paper diamond®

**Identity (CONFIRMED).** paper diamond's own site states the brand was founded by Candice Hui, a Central Saint Martins graduate, and created during the L'Art de la Séduction exhibition in Paris in 2011, with the brand notion quoted verbatim as "'Redefine Ordinary' is our notion behind the brand - Even an ordinary material like paper can shine if value is added to it through good design and craftsmanship."
The Hong Kong tie is confirmed twice over: the site records the brand as a 2020 winner of the Hong Kong Smart Design Award (香港智營設計獎), and the brand's own Facebook page is titled "Paper Diamond | Hong Kong Hong Kong".
The site links its own Instagram as @paper_diamond.

**Rejected candidate, and it is a trap worth recording.** Instagram @paperdiamond (28K, display name "Paper Diamond") is not this brand: the same handle on Threads carries the bio "Musician / Artist / Developer / Friend", which is the American electronic musician of that name.
Reading the band off @paperdiamond would have put this row a full band too high on an unrelated person's audience.
@paper_diamond_ is a separate empty decoy (0 followers, 0 posts).

**Class: INDEPENDENT (CONFIRMED at founder level).** Founder-established, founder-made; the site states Candice Hui finishes each product by hand.
No corporate, platform or franchise owner appears on the site, and no agency, distributor or licensing partner is named on it.

**REP: unclear, on the row-1 ground.** The evidenced property is paper art and jewellery - a craft practice and a product line, not a character IP.
Nothing found identifies a licensable character, so there is nothing identified to represent.
No label, agency or management surfaced.

**Band: `lt_10k`, current-proxy.** Instagram @paper_diamond, 3,483 followers, retrieved 2026-07-31, display name "Paper Art & Jewellery".
Threads @paper_diamond reads 593 and is the smaller channel.

**Cross-market note, recorded and not acted on.** The Threads bio read 8月活動📌 臺灣文博會K2-019 on 2026-07-31, which is this brand exhibiting at the Taiwan Creative Expo.
That is consistent with the sheet listing the same brand name under both Hong Kong and Taiwan; see the observation at the end of this file.
It is not used to adjudicate this row.

**Control signals.** Solo creator: ASSUMED, strongly (the site describes the founder finishing each product herself). Label or agency attached: none surfaced, and the site's silence on any distributor is a point against it. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://paperdiamond.uk/pages/about and https://paperdiamond.uk/ - the brand's own site, founder, founding statement, award, linked Instagram.
- https://www.facebook.com/paperdiamonduk/ - retrieved 2026-07-31, page title carrying the Hong Kong location.
- https://www.instagram.com/paper_diamond/ and https://www.threads.com/@paper_diamond - retrieved 2026-07-31.

### 29. DDED

**Identity (CONFIRMED at channel level).** Instagram @ddedhk, display name DDED, and Threads @ddedhk with the Cantonese bio 愛角的創作人 ("a creator who loves characters"), plus a Facebook page at the same handle.
The self-description is a character creator's, in the brand's own words.

**Class: INDEPENDENT (ASSUMED).** Creator-run brand; no corporate, platform or franchise owner surfaced.
A widely repeated account attributes the brand's founding to an advertising creative and links it to a later "GodToys" line, matching the sheet's note, but the only sources carrying it are wikis and search snippets, which this method does not accept, so the founding story is not carried.

**REP: yes, with two weaknesses stated.**
Neither pass surfaced a label, an agency, a management company or a prior assignment on any publisher page.
The two things that could change this call, both recorded rather than resolved:
1. The brand's own Shopline storefront at ddedhk.shoplineapp.com resolves to a `/closed` page as of 2026-07-31, so the direct commercial channel is evidenced but not currently open.
2. Tiny 微影, the Hong Kong diecast and toy brand run by Orient Toy, appears to carry a DDED category on its own site; the category URL redirected to Tiny's corporate default page when fetched, so the relationship is checked and unresolved, not evidenced.
Neither weakness points at captivity: a creator licensing a line to a toy manufacturer is licensing out, which is the opposite direction from being represented, and it is treated the same way row 8's exhibition listings and row 21's curated pop-up were treated.

**Band: `10k_50k`, current-proxy.** Instagram @ddedhk, 39K followers, retrieved 2026-07-31.
Anti-drift: Threads @ddedhk reads 17.1K, also `10k_50k`, so the two channels agree on the band and Instagram governs as the larger.
No separate per-character channel was found.

**Control signals.** Solo creator: not assessable from a publisher page. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced; Google News zh-HK returned nothing on the queries run.

**Evidence.**
- https://www.instagram.com/ddedhk/ and https://www.threads.com/@ddedhk - retrieved 2026-07-31, display name, bio, counts.
- https://www.facebook.com/ddedhk/ - retrieved 2026-07-31.
- https://ddedhk.shoplineapp.com/products - retrieved 2026-07-31, resolves to `/closed`.

### 30. Tse Sai Pei

**Identity (CONFIRMED at channel level).** Instagram @tsesaipei, display name 謝曝皮, and the Facebook page tsesaipei, titled 謝曝皮 Tse Sai Pei, whose own description links the storefront www.tsesaipei.com/shop.
The store URL resolves.

**Class: INDEPENDENT (ASSUMED).** An illustrator working under their own name with their own shop; no corporate, platform or franchise owner surfaced.

**REP: yes.** Neither pass surfaced a label, an agency, a management company or a prior assignment.
The self-run commercial channel is confirmed from the artist's own Facebook description and the store resolves, which is the strongest form of the `yes` leg available in this run.
Google News zh-HK returned one item on this name that is a different subject entirely (a 自由時報 report on an illustrator's June Fourth artwork) and it is not relied on; the sheet's note about a physical store opening in 2025 is a query seed only and is not carried.

**Band: `50k_200k`, current-proxy.** Instagram @tsesaipei, 118K followers, retrieved 2026-07-31.
Cross-check: the Facebook page reads 163,377 likes, which also sits in `50k_200k`, so the band holds on both channels; Instagram governs as the stated primary.

**Control signals.** Solo creator: ASSUMED (a personal name carried on both channels). Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://www.instagram.com/tsesaipei/ - retrieved 2026-07-31.
- https://www.facebook.com/tsesaipei - retrieved 2026-07-31, page title, own-store link and like count.
- https://www.tsesaipei.com/shop - retrieved 2026-07-31, resolves.

### 31. Overloaddance

**Identity (CONFIRMED at channel level).** Instagram and Threads @overloaddance_studio, display name Overloaddance, and the Facebook page overloaddance.studio, whose own description reads "Toy / Comic / Illustration".
That three-word self-description is the whole of what a publisher page says about this practice.

**Rejected candidate.** Instagram @overloaddance is an unrelated account (1 follower, 0 posts, display name "Alexandria,sahara") and is not this studio; @overloaddance.studio does not exist on Instagram even though it is the Facebook handle, which is a reminder that the handle does not carry across platforms.

**Class: INDEPENDENT (ASSUMED).** A creator-run studio; no corporate, platform or franchise owner surfaced.

**REP: yes, and it is the thinnest `yes` in this batch.**
Neither pass surfaced a label, an agency, a management company or a prior assignment, and the studio runs its own channels across three platforms.
But no press was confirmed - Google News zh-HK returned nothing on the queries run - and no storefront was reached, so this rests on channel evidence alone, at the same strength as rows 3, 9, 19 and 20 rather than rows 8, 16 or 23.
The sheet's note (sofubi toys, active since 2009) matches the Facebook self-description in kind but the date is not confirmed and is not carried.

**Band: `lt_10k`, current-proxy.** Instagram @overloaddance_studio, 5,486 followers, retrieved 2026-07-31.
Anti-drift: Threads @overloaddance_studio reads 1.1K and the Facebook page 4,722 likes; all three sit in `lt_10k`, so the band is safe on every channel.

**Control signals.** Solo creator: ASSUMED, weakly (a studio name). Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: no press found.

**Evidence.**
- https://www.instagram.com/overloaddance_studio/ and https://www.threads.com/@overloaddance_studio - retrieved 2026-07-31.
- https://www.facebook.com/overloaddance.studio - retrieved 2026-07-31, page title, self-description and like count.

### 32. Mr n Mrs Moon

**The largest channel in the run so far.**

**Identity (CONFIRMED).** Instagram and Threads @mr_n_mrs_moon and the Facebook page MrandMrsMoon all carry the display name Mr n Mrs Moon, and the brand runs its own storefront at mrnmrsmoon.com, which resolves and carries its own product collections, wallpapers and an animated sticker range for WhatsApp, Signal, Telegram and Line.
The brand's own site describes the work as the everyday life of a married couple.

**Rejected candidate.** Instagram @mrnmrsmoon (no underscores) is an unrelated personal account (255 followers, display name "Gemintang Bintang").

**Class: INDEPENDENT (ASSUMED).** A creator-pair character brand running its own store; no corporate, platform or franchise owner surfaced.
The creators' names were not confirmed from any publisher page and are not stated here.

**REP: yes, and the brand-side pass is what carries it.**
U Food covered a 天仁茗茶 x Mr n Mrs Moon Christmas theme, and the character appears in mall campaign coverage in HK press.
Both are the brand dealing with counterparties under its own name, with no agent, licensing agency or management company named in any of the coverage reached.
Neither pass surfaced a label or a management attachment.
A separate retailer listing of a Mr n Mrs Moon x MASKEEPER item was seen and is not cited: it sits on a marketplace-style storefront, which this method does not accept as evidence.

**Band: `200k_1m`, current-proxy.** Instagram @mr_n_mrs_moon, 230K followers, retrieved 2026-07-31.
Anti-drift: the account is the character brand's own, so the character channel is already the read and no creator-versus-character split arises.
The count sits just over the `50k_200k` boundary, so the band is recorded with the boundary noted; it is not near enough to the edge to be in doubt at the rounding this source serves.

**Control signals.** Solo creator: no, a pair, ASSUMED from the brand's own premise rather than concluded. Label or agency attached: none surfaced. Already under management: none surfaced. Prior assignment visible in press: none surfaced; the campaign coverage names the brand directly.

**Evidence.**
- https://www.instagram.com/mr_n_mrs_moon/ and https://www.threads.com/@mr_n_mrs_moon - retrieved 2026-07-31.
- https://www.facebook.com/MrandMrsMoon/ - retrieved 2026-07-31.
- https://www.mrnmrsmoon.com/en - the brand's own storefront, retrieved 2026-07-31.
- U Food, "天仁茗茶 x Mr n Mrs Moon 聖誕限定主題" - HK publisher, campaign coverage.

### 33. Lewa Lee

**The most press-visible row in the run.**

**Identity (CONFIRMED).** The exhibitor trades as LeeeeeeToy.
Instagram and Threads @leeeeeetoy both carry the display name LeeeeeeToy, and the creator is named 阿華 in a 橙新聞 interview filed from the Shenzhen Cultural Fair, "直擊深圳文博會｜LeeeeeeToy阿華：在複雜的成人世界裡，用一隻軟膠玩具留住純粹".
The sheet's Threads handle was correct.

**Class: INDEPENDENT (CONFIRMED).** 香港01 filed its coverage under the heading 獨立品牌LeeeeeeToy工作室 - an independent brand studio, in a publisher's own words rather than the brand's.
明報周刊 (Ming Pao Weekly) covered the studio in a piece on reviving Hong Kong's toy-making standing, framing it as an artist-run art-toy practice.
No corporate, platform or franchise owner appears in any of the coverage reached.

**REP: yes.** Neither pass surfaced a label, an agency, a management company or a prior assignment across five publishers.
The brand-side pass instead found the studio doing its own deals: MING'S covered a YMDH x LEEEEEETOY MADONNA EARTH BAG collaboration with the Hong Kong fashion label, with no intermediary named.
Third-party channels found are all of the exhibition or gallery kind and are treated as such, not as representation: a Taipei solo show at 伊日後樂園 BACK_Y covered by 玩具人 TOY PEOPLE and by 500times (udn), and the Shenzhen Cultural Fair Hong Kong pavilion, which is a trade-fair pavilion rather than a representative.

**Band: `50k_200k`, current-proxy.** Instagram @leeeeeetoy, 53K followers, retrieved 2026-07-31.
Anti-drift: Threads @leeeeeetoy reads 7.0K (`lt_10k`) on the same identity; Instagram is the larger evidenced channel and governs, and the alternative is recorded.
The count sits just above the `10k_50k` boundary, so the band is recorded with the boundary noted.
No separate per-character channel was found, so the studio account is the read.

**Control signals.** Solo creator: ASSUMED, strongly (a bylined interview with one named creator about his own studio). Label or agency attached: none surfaced across five publishers. Already under management: none surfaced. Prior assignment visible in press: none surfaced; the fashion collaboration names the studio directly.

**Evidence.**
- 橙新聞, "直擊深圳文博會｜LeeeeeeToy阿華：在複雜的成人世界裡，用一隻軟膠玩具留住純粹".
- 香港01, "【周日Cult遊】獨立品牌LeeeeeeToy工作室 跨界創作人改裝展暖場".
- 明報周刊 Ming Pao Weekly, "復興港產玩具地位 藝術玩具Leeeeee Toy：香港人可以想出許多古靈精怪的創新設計".
- MING'S, "本地時裝品牌 YMDH 聯同 LEEEEEETOY 攜手打造 MADONNA EARTH BAG 聯乘系列", https://www.mings.hk/ymdh-leeeeeetoy-本地品牌-382806/
- 玩具人 TOY PEOPLE, "LeeeeeeToy台北個展【The Game of Lifeeeeee 無呢頭多功能遊戲人生機】at伊日後樂園BACK_Y 現場報導".
- 500times (udn), "讓創作玩心大開，回歸赤子之心：香港藝術家LeeeeeeToy《地球國》伊日後樂園展出".
- https://www.instagram.com/leeeeeetoy/ and https://www.threads.com/@leeeeeetoy - retrieved 2026-07-31.

## Observations carried, not concluded

Recorded here because they change how the finished register should be read, and because leaving them implicit would make the eventual counts misleading.

**1. `unclear` is carrying two entirely different situations, and they must not be summed.**
At the close of the run the `unclear` calls split cleanly:
- *No property to represent.* Rows 1, 24, 25, 26, 27 and 28 are identified, creator-owned, self-channelled businesses that make craft or design goods rather than character IP. Nothing is unresolved about them; the finding is that there is no character IP evidenced on the row.
- *Identity or scope unresolved.* Rows 4, 6, 11, 13, 14 and 17 could not be identified well enough to call, and row 12 has a real attachment signal whose scope is not resolvable.
Both return `unclear` under the stated rule and the rule was not changed mid-run, but a count that adds them together would report a measurement failure and a substantive finding as the same thing.
The counts section separates them, and any later use of this file must keep them separate.

**2. Row 22's `no` is structural, not captive, and the two branches must be kept apart when the counts are written.**
ARDUREY returns REP=`no` because the attendee is itself a licensing agency, which is the rule's second branch.
That is a different fact from the rule's first branch - exclusive label or agency channelling - and the two must be tallied separately rather than added, or the count will say something the evidence does not.
No branch tally is stated here; the point is that the counts section cannot be written as a single `no` column.

**3. Every label-or-retailer channel tested in the whole run came back running alongside a self-run channel, not replacing it.**
Three tests in total: TOYZEROPLUS on row 11's candidate, 誠品 on row 24, and Tiny 微影 on row 29 (the last unresolved).
In each case the creator's own direct channel was live or evidenced at the same time.
That is the non-exclusive branch of the pinned edge case each time.
No conclusion about exclusivity is drawn from this - exclusivity is refused ground and a concurrent direct channel is not proof of a non-exclusive arrangement - but the pattern of what the sweep can see is worth recording as it accumulates.

**4. A sheet artefact, recorded for Phase 0 rather than acted on here.**
Eight of the names on this Hong Kong list also appear in the sheet's Taiwan section: ARDUREY LIMITED (#309, typed Agency), HEREAFTER STUDIO (#348), HANDMADESHIP (#349), Scentory (#350), paper diamond® (#388), DDED (#425), Tse Sai Pei (#436) and Overloaddance (#437), all typed Brand and all carrying "N/A detail" notes.
The Hong Kong rows carry Hong Kong-specific first-party handles and the evidence above confirms Hong Kong entities, so the Hong Kong rows are the substantive ones.
One independent corroboration that the duplication may be real exhibiting rather than a transcription error: paper diamond's own Threads bio on 2026-07-31 advertised a Taiwan Creative Expo booth.
Phase 0 is not re-run and its disposition is not revised; this is flagged so that any later cross-market count knows the eight names are the same organisations and must not be counted twice.

**5. The six unresolved rows are not a random sample of the list, and the counts must not be read as if they were.**
Every row that failed to resolve failed the same way: no channel, no press, and every plausible handle a false friend.
The four rows left to the final batch were exactly the four whose Notes column carried no handle, and three of them (6, 13, 14) stayed unresolved while the one that carried usable text (5) resolved completely and became the best-documented ownership row in the register.
That is a property of the seed data rather than of the exhibitors: presence of a handle in the sheet, not size or type of business, is what predicted whether a row could be adjudicated.
It matters for the counts because the sweep's blind spot is systematic - a creator whose public footprint is thin is both harder to identify and likelier to be channelled through someone else - so the unresolved rows lean, if anything, away from the run's headline result rather than neutrally.

**6. A second possible agency co-listing was found and could not be closed.**
Row 6 is a co-listed exhibitor string (`Nine Four Sixty X Dino Valley`) and the sheet's Taiwan section separately carries a `Dino Valley Creative` typed as an Agency.
If those are the same party, the register would hold two rows where an agency sits on the creator's own exhibitor line rather than one.
It is recorded in row 6 as a checked-and-rejected hypothesis: neither party resolved first-party, so the connection is unverified and is not carried into any count.
Noted here so that a later reader who spots the same coincidence finds it already examined rather than re-deriving it as new.

## Counts

All 32 rows now carry a class, a REP call and a reason, so the register is tallied here.

**What this section is, and what it is not.**
This is a tally of the 32 rows in this register and nothing else.
It is not a rate, not a share, not a proportion of the Hong Kong market, and not a base for extrapolation to anything - not to the rest of the CET2026 list, not to Hong Kong, not to the census.
No percentage is computed anywhere in this file, deliberately.
This file is internal only.

**REP, the run's question.**

| REP | Rows | Count |
|---|---|---|
| `yes` | 2, 3, 5, 7, 8, 9, 10, 16, 18, 19, 20, 21, 23, 29, 30, 31, 32, 33 | 18 |
| `no` | 22 | 1 |
| `unclear` | 1, 4, 6, 11, 12, 13, 14, 17, 24, 25, 26, 27, 28 | 13 |

**The single `no` must be read on the correct branch.**
Row 22 (ARDUREY LIMITED) is the rule's second branch - the attendee is itself an artist licensing agency, so it is the representation layer rather than something to represent.
On the rule's first branch, exclusive label or agency channelling, the count across all 32 rows is zero.

**`unclear` splits into two unrelated things and is never reported as one number.**

| Kind of `unclear` | Rows | Count |
|---|---|---|
| No character IP evidenced on the row - identified, creator-owned craft, design, fashion, fragrance or paper-art businesses with no property of the kind this run adjudicates | 1, 24, 25, 26, 27, 28 | 6 |
| Identity not resolvable to the evidence standard | 4, 6, 11, 13, 14, 17 | 6 |
| Identity resolved, but a real attachment signal whose scope could not be resolved | 12 | 1 |

The first kind is a finding about what this exhibitor list contains.
The second is a measurement failure of this sweep.
The third is the only row in the register where an attachment signal was found on an identified creator and could not be closed.
Adding them would report all three as the same thing.

**Class.**

| Class | Rows | Count |
|---|---|---|
| INDEPENDENT | all rows except those below | 26 |
| PORTFOLIO | 22 | 1 |
| MIXED | none | 0 |
| unresolved | 4, 6, 11, 13, 14 | 5 |

**Band**, `current-proxy` on every banded row, July 2026 counts.

| Band | Rows | Count |
|---|---|---|
| `lt_10k` | 1, 8, 9, 23, 26, 28, 31 | 7 |
| `10k_50k` | 2, 3, 5, 7, 10, 12, 18, 19, 20, 21, 24, 25, 27, 29 | 14 |
| `50k_200k` | 16, 30, 33 | 3 |
| `200k_1m` | 32 | 1 |
| `gt_1m` | none | 0 |
| `unknown` | 4, 6, 11, 13, 14, 17, 22 | 7 |

Row 7's band sits on a rounded "10K" and straddles the `lt_10k` / `10k_50k` edge; it is counted at `10k_50k` with the boundary flagged in the row and not resolved.

**The label-captive default did not reproduce, and that is the run's answer to its own question.**
Hong Kong is the art-toy label capital and captive-by-channel was the expected default for this market, pinned in advance so it would be tested rather than assumed.
Across all 32 rows, the number that returned exclusive label or agency channelling is zero.
Three label-or-retailer tests were run explicitly - TOYZEROPLUS, 誠品, Tiny 微影 - and each came back with the creator's own direct channel live at the same time.

That result is bounded, and the bounds are part of the finding rather than a caveat on it:

- Exclusivity is refused ground in this run. A concurrent direct channel is not proof of a non-exclusive arrangement, and none is claimed. What the zero states is that no exclusive channelling was *evidenced*, not that none exists.
- Six rows could not be identified at all. Captive arrangements are exactly the kind that leave a thin public trail, so the unresolved rows are not neutral with respect to this question and cannot be assumed to distribute like the resolved ones.
- The frame is an expo exhibitor list. Exhibiting under one's own name at a licensing expo is itself a selection: a creator whose IP is exclusively label-channelled has less reason to take a booth in their own name, and the label would take it instead. The population may therefore be pre-filtered toward the answer this run found. This is the strongest single reason not to read the zero as a statement about Hong Kong.
- Control signals are ASSUMED throughout by construction. On most `yes` rows the reason is "no attachment surfaced in either pass", and this population is channel-visible and press-invisible, so an attachment could exist without leaving a trace either pass could see.

Within those bounds the finding stands: on this list, in this frame, the expected captive default is not what the evidence shows.

## Refusals applied

- No rights_owner, chain of title, territory, exclusivity or deal terms is concluded anywhere above.
  Where exclusivity was the natural next question (rows 11 and 12), the file says so and stops.
- The counts section was held empty until every row carried a call, so no partial number could be read as an outcome.
  What it now contains is a tally of this 32-row register and is labelled as such: no rate, no share, no proportion, no extrapolation, and no percentage computed anywhere in this file.
  The bounds on the run's headline result are stated in the same section as the result, not below it.
- No HK indie share is stated, computed or hinted at.
  This file is internal only and the HK share is not quotable on its own in any case.
- No brand images fetched.
- No levels or ladder vocabulary.
- Pinned edge cases applied: the Toyzeroplus test was run explicitly on row 11's candidate and returned non-exclusive, which is recorded as a negative result rather than suppressed; the 咖波 precedent (agency-managed but creator-owned is still independent) is what keeps row 12 INDEPENDENT despite the consultancy co-listing; self-presentation is not ownership, which is why rows 3, 9 and 10 carry ASSUMED class calls rather than confirmed ones.
- Unresolved rows (4, 6, 11, 13, 14) are left unresolved with the reason and the resolving evidence named, and none is filled in.
  Row 13 is the sharpest case: the sheet's own link resolved to a real, named, 3,833-follower toy-design studio, and it is still recorded as unresolved because nothing independently ties that studio to the exhibitor name. The candidate's follower count is deliberately not carried into the band, since adopting it would import the unverified identification through the band column.
- Row 5's `yes` names what was found and assessed rather than resting on absence: an incubation-programme listing was surfaced, checked, and judged not to be a label, agency or management attachment, on the same reasoning as row 7's promotion programme.
  Its client-service business line is recorded as a reason to expect the assignment question, not as an answer to it; whether any client work was assigned away is chain-of-title and is refused.
- Row 6's agency hypothesis is written down as checked-and-rejected rather than dropped, so that a plausible-looking coincidence in the source sheet cannot later be re-derived as a finding.
- The exhibitor sheet's Notes column was used only as a query seed; where it was contradicted (rows 1, 3) or unconfirmed (rows 10, 11, 26, 29, 30, 31) that is recorded and the note is not carried.
  The Notes column's handles did verify on rows 24, 25, 29, 30, 31, 32 and 33, which is recorded as a property of the seeds, not as evidence: each was still confirmed against the display name on the platform's own page before being accepted.
- Row 22's REP=`no` is the rule's agency branch, not the captive branch, and the file says so in the row and again in the observations so that it cannot be read as a captivity finding.
- Where a row is a design-goods or craft business with no character IP evidenced (rows 1, 24, 25, 26, 27, 28), the file records exactly that and returns `unclear`; it does not invent a property, and it does not treat the absence as an attachment.
- Row 28's follower count was deliberately not taken from the larger same-name account, because that account is a different person; the higher number is rejected in the row rather than quietly dropped.

## Method notes

Recorded during the pass so that a repeat of it runs the same way.

1. **Handle probing beats search for this population.** These are small HK creator brands with thin press. Fetching `instagram.com/<handle>` and `threads.com/@<handle>` with a Googlebot user agent returns the follower count and often the bio in `og:description`, which resolves both identity and band in one call. Threads is a newly useful channel here: its profile `og:description` carries "N Followers - M Threads - <bio>", though it serves an empty description on a substantial share of attempts and needs a retry.
2. **False friends are the main hazard.** Eight of the sixteen rows adjudicated so far had at least one plausible handle that turned out to be an unrelated or empty account, several with single-digit follower counts. A handle is only accepted when the display name or bio independently matches the exhibitor.
3. **Google News RSS with `hl=zh-HK&gl=HK` is the press index**, as in the HK census. It found usable press for five of the sixteen and nothing for the rest, which is itself informative about this population's press depth: most of these creators are channel-visible and press-invisible.
4. **Web search resolves the article better than the aggregator redirect.** Searching the exact headline returns the publisher URL directly, which sidesteps the blocked Google News resolver.
5. **The character-vs-creator anti-drift split is rare in this population and the platform split is common.** Almost none of these creators run a separate character account, so the HK bands pass's hardest case barely arises here. What does arise on nearly every row is Instagram-versus-Threads: the same identity typically reads two to three times larger on Instagram, so the larger evidenced channel governs and the alternative is recorded, exactly as the census rule requires.
6. **Facebook is the third channel and it is the most informative one per call.** Fetching `facebook.com/<handle>` with a Googlebot user agent returns `og:title` (the page's own title, often bilingual, which resolves identity) and `og:description` carrying the like count, the page's self-description and sometimes its own storefront URL. That is how rows 27, 30 and 31 got a first-party self-description and row 30 got its store link. Page likes are not followers and are used as a band proxy only where nothing else resolved (row 23) and flagged as such; where both exist they agreed on the band on every row tested (27, 30, 31).
7. **Google News with a Chinese query string must be percent-encoded or it returns HTTP 400.** Passing traditional-Chinese characters raw in the `q` parameter produced `Error 400 (Bad Request)` on every attempt and looks exactly like an empty result set. Encode the query first; several rows initially read as press-invisible purely because of this.
8. **The highest-value false friend is a same-name account that is bigger, not smaller.** The decoys in the first batch were all tiny and obvious. Row 28's decoy had 28K followers under the exactly-correct display name and would have placed the row a band too high; what exposed it was the same handle on Threads carrying a different bio. Cross-platform bio comparison is the check that catches this class, and count size is not evidence of being the right account.
9. **A whole cluster of this list is design-goods businesses with no character IP.** Rows 1, 24, 25, 26, 27 and 28 are craft, fashion, fragrance or paper-art brands. They are not unresolved and they are not captive; they simply have no property of the kind this run is adjudicating. Recorded as what they are rather than forced into a call.
10. **On a generic brand name, work from the entity's own site outward instead of guessing handles.** Row 5 is the case: `@purestudio`, `@pure_studio` and `@purestudio.hk` are all dead or unrelated, and the real channel (`@purehay`) shares no string with the exhibitor name at all. It was reachable only because the studio's own site links to it. Handle probing is the cheap first move on a distinctive name and is close to worthless on a generic one - switch to a site-first route as soon as the name is a common word.
11. **The public-support register is a usable identity source and is not an attachment.** The Hong Kong Design Centre's incubation directory carried a company page for row 5 with both founders and the founding year - a publisher page, first-party to the programme, on a row where press returned nothing. Incubation and promotion programmes have now appeared twice (rows 5 and 7); both were checked as possible attachments and neither is a label, agency or management company. Check them, name them, and do not let them move the REP call.
12. **A link in the sheet's Notes column resolving is not the same as the row resolving.** Row 13's Facebook share link followed cleanly to a real, named, active studio, and the row is still unresolved because the destination's own name never matches the exhibitor's. A resolving link is the most convincing-looking kind of false friend in this dataset precisely because it came from the source sheet rather than from a guess, and the same acceptance rule has to be applied to it: the display name or bio must independently match.
13. **When a note claims a collaboration, run the named collaborator artist-side.** Row 14's note named two partners. One resolved to a genuine creator account whose own profile named no producer or collaborator; the other was a false friend. That converts the row from "nothing found" into "the one route that could have identified it was open, was taken, and returned nothing", which is a materially different record to leave behind.
14. **Expired TLS on a target's own site is a hard stop, not a soft one.** Row 6's hypothesis could not be tested because the candidate entity's own site could not be fetched at all. Worth recording as a distinct failure mode from "no site" and from "blocked", because it is the one that looks like a dead brand and is not.
