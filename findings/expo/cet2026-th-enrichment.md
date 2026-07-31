# CET2026 Phase 1 - Thailand enrichment

Input: the 7 IP-type Thailand attendee rows in `findings/expo/cet2026-match.md` (per-row disposition, rows 513, 514, 515, 516, 517, 518, 520).
The 4 Thai brand rows (508, 510, 511, 519) and the 3 Thai org rows (507, 509, 512) are out of scope and are not touched; REP does not apply to them.
Phase 0 is not re-run here and nothing in it is revised.
No other market is touched in this run, and no census market file was opened.

Run opened 2026-07-31.
All retrieval dates below are 2026-07-31 unless stated otherwise.

## The question this run answers

Whether Thai character IP is corporate-shaped where Hong Kong was solo-creator-shaped.
The hypothesis was tested per row rather than assumed, and it is answered in the "What the shape test found" section after every row carries a call.
The two readings the test has to separate are stated up front: a creator-owned company is still INDEPENDENT under the pinned 咖波 precedent, while a corporate-held property is PORTFOLIO.
The pinned Toyzeroplus call is applied as a test with a possible negative answer: creator-owned but exclusively label-channelled is REP=no.

All 7 rows carry a class, a REP call and a reason.
Row 516 (Shewsheep) carries its census adjudication unchanged and was checked for one thing only, per the task: whether a management or agency layer is evidenced.

## Method

**Both passes, artist-side mandatory.**
Every row gets a Thai-language pass (character name in Thai script, creator name, นักวาด / ผู้สร้าง / เจ้าของคาแรคเตอร์ / ลิขสิทธิ์ / ตัวแทนลิขสิทธิ์) and an EN pass (brand name, artist name, illustrator, character IP, licensing, studio).
The artist-side pass is mandatory and was run first on every row.
The Thai pass was not optional: the Thailand census established that Thai brand press names the licensee and omits the creator, so a brand-side-only sweep would systematically miss the artist.
That prediction held on this sample: on four of the seven rows the creator's name surfaced only in the Thai pass, and on two of those the English-language material named the licensee brand and no person at all.
The brand-side pass was used only to test for label, agency or management attachment.

**Evidence rules.**
Publisher pages only: Thai press titles, Thai business and market press, the creator's or brand's own site, the creator's own platform profile, a venue's or organiser's own programme page.
Aggregators, wikis, marketplaces-as-evidence and link-farm listings are not evidence; where a fact reached this file through a search summary alone and the publisher page could not be opened, it is labelled search-surfaced and treated as weaker.
Several Thai publishers returned HTTP 403 to direct retrieval (Bangkok Post, Prachachat, Urban Creature, Sarakadee Lite, The Bangkok Insight, Lomography); those attempts are recorded rather than silently dropped.
The exhibitor sheet's Notes column was not read in this run at all, since the scope permitted only the Phase 0 file; nothing from it is carried, and the company entities reported below were surfaced from evidence, not from the sheet.

**Band vocabulary, exactly the /start `follower_band` codes:** `lt_10k` / `10k_50k` / `50k_200k` / `200k_1m` / `gt_1m` / `unknown`.
Band = the IP's primary channel following, single channel, not a cross-platform total.
Basis codes are the census's: `at-campaign` / `current-proxy` / `unknown`.
Every band here that rests on a count retrieved in July 2026 is `current-proxy` and says so.
Thailand-specific caveat, stated once: on several of these rows the primary channel is Facebook, where the retrievable figure is a page like-count and not a follower count, so the like-count is used as a scale proxy and labelled as one.
A second Thailand-specific caveat: LINE sticker reach, which Thai press treats as the making of at least one of these characters, carries no retrievable count and is therefore invisible to this band vocabulary.

**Confirmed vs assumed.**
Every claim below is tagged.
`CONFIRMED` = a publisher page or first-party page states it.
`ASSUMED` = the evidence is consistent with it and nothing contradicts it, but no page states it.
Control signals (solo creator, label or agency attached, already under management, prior assignment visible in press) are ASSUMED by construction and are never concluded, however strong they look.
Where a Thai publisher states that a company is the character's copyright holder, that is recorded as what the publisher states and is not adopted as a rights_owner conclusion by this file.

**Class.** INDEPENDENT / PORTFOLIO / MIXED on the census's ownership-shape test: portfolio = corporation, estate, platform or franchise-owned; independent = creator-owned (agency-managed but creator-owned is still independent, the 咖波 precedent); MIXED = an attendee carrying both.
`unresolved` where the entity or its IP could not be identified to that standard.

**REP decision rule, stated once and applied uniformly.**

- `no` - exclusive label or agency channelling is evidenced (the pinned Toyzeroplus call), or the attendee is itself a company, label or agency holding a character portfolio rather than an individual creator available to be represented.
- `yes` - creator-owned IP, at least one confirmed self-run commercial or publishing channel, and no label, agency or management attachment surfaced in either pass.
- `unclear` - an attachment signal exists whose scope is unresolved, or the entity or its IP could not be resolved well enough to call.

Unresolved is a valid answer.
Where a row is unresolved it stays unresolved and the reason names what was checked.

## Register

One line per row. `#` is the attendee number from the Phase 0 disposition table.

| # | Attendee | Class | REP | Reason (short) | Band | Basis |
|---|---|---|---|---|---|---|
| 513 | Bloody Bunny | PORTFOLIO | no | corporate character studio: a staff designer made the character inside the company, the founder-MD is not its creator, and the company runs its own licensing operation | `50k_200k` | current-proxy |
| 514 | Baan Maew Maew | INDEPENDENT | yes | founder-run design and publishing studio, one founder named in press as the brand's principal; licensing collaborations done in the brand's own name; no agency surfaced | `lt_10k` | current-proxy |
| 515 | Sweet Summer | PORTFOLIO | no | company-held character portfolio: the company is the only party named on any of its own character pages, no creator is credited anywhere, and design roles are staffed | `lt_10k` | current-proxy |
| 516 | Shewsheep | INDEPENDENT (carried) | yes (carried) | census adjudication carried unchanged; this run checked only for a management or agency layer and found none, and the company layer that exists is the creator's own studio | `50k_200k` (carried) | carried from census, basis not restated |
| 517 | Warbie Yama | INDEPENDENT | unclear | creator-owned and the 咖波 precedent holds through the agency layer, but a listed company is evidenced as the character's licensing agent and the scope of that channelling is unresolved | `lt_10k` | current-proxy |
| 518 | FLUFFY OMELET STUDIO | INDEPENDENT | yes | named solo artist trading as her own studio; retail and brand collaborations run in her own name; no agent named in any of them | `10k_50k` | current-proxy |
| 520 | Plaplatootoo | INDEPENDENT | yes | two-creator studio; the province adopted a character the creators had already made rather than commissioning it; no agency, label or management surfaced | `lt_10k` | current-proxy |

## Per-row detail

### 513. Bloody Bunny

**Identity (CONFIRMED).** The character sits inside บริษัท ทูสปอตคอมมิวนิเคชั่น จำกัด (2Spot Communications, trading as 2Spot Studio), a Bangkok character design and licensing studio that its own site dates to 2004.
The same site presents 2Spot as "Creator of Bloody Bunny" and carries a blanket copyright line over the characters and content on the site.

**Who made it (CONFIRMED).** Post Today, a Thai publisher, profiled อัครัชญ์ จารุศิลาวงศ์ (nickname Huff) as the character designer who designed Bloody Bunny early in his career at 2Spot, describing him as the company's first design employee and, at the time of the piece, its creative manager.
The same profile names กฤษณ์ ณ ลำเลียง (Kris Na Lamlieng) as the company's founder, and he appears in Thai business press as its managing director rather than as the character's author.
So the founder is not the creator, and the creator is a member of staff.
This is the authorship-is-not-ownership pin working in the direction opposite to its usual one: naming the designer does not make him the party a licensing counterparty would deal with, and nothing evidences him holding the property.

**Class: PORTFOLIO.** Corporate-held on the ownership-shape test: a company with a multi-character line-up, staff design roles, and no individual proprietor evidenced behind the character.
Bangkok Biz News describes the company in Thai as เจ้าของลิขสิทธิ์คาแรคเตอร์ across several of its characters; that is recorded as the publisher's statement, and no rights_owner or chain-of-title conclusion is drawn from it here.
The 咖波 carve-out was tested and does not apply: it needs the company to be the creator's own vehicle, and here the creator and the company's principal are different people.

**REP: no.** The exhibitor is the corporate studio itself, which runs its own licensing operation in-house across its own character line-up.
There is no individual creator identified as holding the property who could be represented.
The call is stable under the alternative reading as well: were the company shown to be a creator's own captive vehicle, the pinned 咖波 outcome would still be REP=no.

**Band: `50k_200k`, current-proxy.** Facebook page @BloodyBunny.2Spot, 141,788 likes, `og:description` retrieved 2026-07-31.
Facebook is the primary evidenced channel by a wide margin.
The figure is a page like-count used as a scale proxy, not a follower count, and is labelled as one.
Anti-drift: Instagram @bloodybunny reads 7,714 followers and X @bloodybunny reads 5,349 followers on the same identity, both `lt_10k`; the character channel governs and the alternatives are recorded here.
No separate company channel was used for the band, since the character channel is the larger and the correct read.

**Control signals.** Solo creator: contradicted; a staff designer and a team are evidenced. Label or agency attached: none external surfaced, because the licensing layer is the company itself (ASSUMED). Already under management: not applicable in the individual-creator sense. Prior assignment visible in press: none surfaced; Thai press treats the company as the character's home throughout.

**Evidence.**
- https://www.2spotstudio.com/about-us - first-party, retrieved 2026-07-31; founding year, self-description as a full-service character design and licensing studio.
- https://www.2spotstudio.com/bloodybunny - first-party, retrieved 2026-07-31; "Creator of Bloody Bunny" and the site copyright line.
- https://www.posttoday.com/lifestyle/373791 - Post Today profile of อัครัชญ์ จารุศิลาวงศ์, naming him as the designer of Bloody Bunny, an employee, and naming the company founder.
- https://www.bangkokbiznews.com/pr-news/biz2u/213680 - Bangkok Biz News; the company described in Thai as the character copyright business operator and the party doing brand collaborations.
- https://www.facebook.com/BloodyBunny.2Spot/ - like-count retrieved 2026-07-31 from `og:description`.

### 514. Baan Maew Maew

**Identity (CONFIRMED).** BAAN MAEW MAEW (บ้านแมวเหมียว), a Bangkok design and publishing studio founded in November 2022, building an original character set from Thai lucky cats (the Siamese cat, the Konja black cat, the Khaomanee white cat).
Bangkok Design Week's own programme page for the studio carries the founding date, the studio description and the licensing statement.
The brand's own site presents it as the "Official Home of Original Cat Character IP".

**Who runs it.** Onedeedee, a Thai lifestyle publisher, names คุณวิชชุกร โชคดีทวีอนันต์ as the person representing BAAN MAEW MAEW at the ICONCRAFT collaboration and its opening seminar: CONFIRMED that a named principal fronts the brand publicly.
A wider founding team, including a second Chokdeetaweeanan and two graphic designers, is search-surfaced from marketplace brand-story pages only; the publisher pages do not carry it, so the composition of the founding team is ASSUMED and the marketplace text is not treated as evidence.

**Class: INDEPENDENT.** Founder-run studio with a named principal and no corporate, platform, estate or franchise parent surfaced.
Under the 咖波 precedent, the studio wrapper does not move this to PORTFOLIO.
The contrast with row 513 is the whole point of the shape test: here the company is the founders' own vehicle, there it is not.

**REP: yes.** Creator-owned, self-run retail and publishing channels, and its licensing collaborations run in the brand's own name.
Bangkok Design Week records the studio opening an IP licensing line of business in late 2024 with a stationery collection for a large Thai paper manufacturer, and the ICONCRAFT exhibition is presented as a direct brand-to-venue collaboration.
Neither pass surfaced a licensing agent, label or management company.
The absence is a finding about what the sweep saw, not proof of no attachment.

**Band: `lt_10k`, current-proxy.** Instagram @baanmaewmaew, 4,177 followers, `og:description` retrieved 2026-07-31.
Instagram is the larger evidenced channel.
Anti-drift: the Facebook page @baanmaewmaew.shop reads 1,255 likes on the same identity, also `lt_10k`, and is recorded here.
This is a small-channel brand doing visible licensing work, which is the reverse of the pattern the census's campaign-press sweeps select for.

**Control signals.** Solo or small founder team: ASSUMED. Label or agency attached: none surfaced (ASSUMED absent). Already under management: none surfaced. Prior assignment visible in press: none surfaced; the counterparties named in press are licensee brands and a retail venue.

**Evidence.**
- https://www.bangkokdesignweek.com/en/bkkdw2026/program/138930 - organiser's own programme page; founding date, studio description, characters, and the late-2024 licensing line of business with its first partner.
- https://www.onedeedee.com/lifestyle/lifestyle-news/167169 - Thai lifestyle publisher; names the brand's representative and describes the ICONCRAFT x BAAN MAEW MAEW exhibition (20 June to 20 July 2026).
- https://www.baanmaewmaew.com/ - first-party, retrieved 2026-07-31; the brand's own positioning as an original character IP home. The `/en/brand` sub-page returned HTTP 404 on retrieval.
- https://www.instagram.com/baanmaewmaew/ and https://www.facebook.com/baanmaewmaew.shop/ - counts retrieved 2026-07-31.

### 515. Sweet Summer

**Identity (CONFIRMED).** Sweet Summer Co., Ltd., a Bangkok company running a cute-character stationery and gift business, with its registered address published on its own contact page.
Its own site carries a line-up of roughly ten character properties, including Cat Company, Little Amiko, Majory, Munchii & Marsh, Jessie Frog, Kuro & Friends, Unishiba, Hoshio & Kamomo, The Long Neck Gang and Mina & Koko.
Its own posts record repeated appearances at the Hong Kong licensing show and at Thai character showcases in Tokyo, so this is a company that presents itself to the licensing trade directly.

**Who made the characters: unresolved, and deliberately left so.**
The artist-side pass was run in both languages against the company name, each major character name and the contact name published on the site, and it surfaced no named creator on any publisher page.
The company's own character pages carry no artist credit at all: the only party named on them is the company, under a company copyright line.
A graphic-designer job posting under the Sweet Summer name is search-surfaced and is consistent with staffed design, but a job board is not a publisher page and it is not carried as evidence.

**Class: PORTFOLIO (ASSUMED).** Company-held on the ownership-shape test: a registered company holding a multi-character portfolio, presenting only the company on its own character pages, with no individual proprietor evidenced behind any character.
The creator-owned reading cannot be excluded, and it is named here as the open alternative: a founder-designer's own company would be INDEPENDENT under the 咖波 precedent.
What would settle it is a bylined interview or a first-party page naming a founder-creator, and neither pass produced one.

**REP: no.** Under either reading of the class the answer is the same, which is why the call is made despite the open class question.
As a corporate holder, there is no individual creator identified to represent.
As a founder's own vehicle, licensing runs entirely through that company, and the pinned 咖波 outcome is REP=no.
This is recorded as a call whose reason is structural, not as a resolution of the ownership question.

**Band: `lt_10k`, current-proxy.** Instagram @sweetsummer.shop, 9,463 followers, `og:description` retrieved 2026-07-31.
Instagram is the only substantial channel evidenced for the brand identity.
Rejected candidate: the Facebook page "Sweet Summer" in Ubon Ratchathani (1,061 likes) is an unrelated local business and is a false friend on this name; "Sweetsummer Smile" is a personal profile and is likewise not the exhibitor.
No per-character channel of larger size was found, so the brand account is the correct read.
The band sits just under a band boundary and is flagged as near-boundary.

**Control signals.** Solo creator: not evidenced either way. Label or agency attached: none surfaced; the company appears at licensing shows on its own behalf (ASSUMED). Already under management: none surfaced. Prior assignment visible in press: none surfaced.

**Evidence.**
- https://sweet-summer.com/ - first-party, retrieved 2026-07-31; character line-up, company copyright line, retail and collaboration channels.
- https://sweet-summer.com/gang/cat-company/ - first-party character page, retrieved 2026-07-31; no artist credit, company copyright line only.
- https://sweet-summer.com/contact-us-2/ - first-party, retrieved 2026-07-31; company entity name and registered address.
- https://www.instagram.com/sweetsummer.shop/ - count retrieved 2026-07-31.

### 516. Shewsheep

**Not re-adjudicated.** Phase 0 matched this attendee to the Thailand census (thailand row 74) and the census verdict is carried unchanged: INDEPENDENT, REP=yes, band `50k_200k`.
Per the task, this run checked one thing only: whether a management or agency layer is evidenced.

**Management or agency layer: none evidenced, and one company layer that is the creator's own.**
The creator is ป๊อป-สุมิตร สีมากุล (Sumitr Simargool), owner of the Eat All Day page from which the yellow sheep character came.
Marketeer Online's coverage of the 2025 FUTUREPARK x SHEWSHEEP campaign names him directly as the designer and owner of the character and names no intermediary: the mall's campaign is presented as a direct collaboration with him.
Animation Xpress, an industry publisher, describes the character as the flagship property of Liffolab, a Bangkok studio, and quotes Simargool as its managing director describing brands approaching them directly to use the character.
That is a company layer, but it is the creator's own studio, so under the pinned 咖波 precedent it does not touch the carried class, and it is not an external agency or management attachment.
The same piece notes he serves as president of the Digital Content Association of Thailand, which is an industry-body role and not a representation relationship over the character.

**Signal recorded, not a re-adjudication.** Management or agency attached: none surfaced (ASSUMED absent). Creator's own company layer: CONFIRMED at publisher level.
For completeness and without re-banding: the Eat All Day Facebook page reads 185,380 likes retrieved 2026-07-31, which is consistent with the carried band and is recorded as an observation only.

**Evidence.**
- https://marketeeronline.co/archives/437436 - Marketeer Online; names the creator as designer and owner of the character, with no agent or intermediary named in the mall campaign.
- https://www.animationxpress.com/latest-news/from-comics-to-commerce-thailands-playbook-for-building-character-ips/ - industry publisher; names Liffolab as the studio, the creator as its managing director, and describes brands approaching the studio directly.
- https://www.facebook.com/eatalldaysheep/ - like-count retrieved 2026-07-31, recorded as an observation.

### 517. Warbie Yama

**Identity (CONFIRMED).** Warbie and Yama are original characters by Arut Tantasirin, a Thai animator and animation director based between Los Angeles and Bangkok, developed out of his award-winning student short "Cheez...z" and popularised in Thailand through LINE stickers.
His own site carries the bio and the character's origin, and River City Bangkok's own page for the 2022 exhibition "It's me, Warbie! The Inside World of Warbie Yama" describes the show as a collaboration between the venue and "the creator of Warbie Yama".

**Agency attachment: evidenced.**
T.A.C. Consumer PCL (TACC), a listed Thai consumer-products company, publishes news items under its own newsroom describing itself as the Warbie character copyright agent and launching the character commercially.
Hoonsmart, a Thai market publisher, sets out TACC's character business: an agency line that carries San-X properties for a named group of Southeast Asian territories under a multi-year agreement, alongside home-grown Thai characters it represents, with Warbie Yama added in 2021.
Thai business press covering the launch is search-surfaced as naming Arut as the character's creator and copyright holder while TACC acts as the licensing representative; the Matichon page returned HTTP 403 to direct retrieval, so that particular attribution is labelled search-surfaced and weaker.

**Class: INDEPENDENT.** Creator-owned, with the agency layer sitting on top: this is the 咖波 precedent applied exactly as pinned, and agency management does not move the class.
No company was surfaced as the character's proprietor, and no creator-owned company vehicle was surfaced either; the creator appears in his own name throughout.

**REP: unclear.** An attachment signal exists and its scope is unresolved.
What is evidenced is that a listed company holds itself out as the character's licensing agent and runs its commercial programme.
What is not evidenced is whether that channelling is exclusive, and this run refuses to conclude exclusivity, territory or terms.
The rule is applied honestly in both directions: if the channelling proved exclusive the pinned Toyzeroplus call would give REP=no, and if the agent's mandate proved partial the row would read REP=yes on the creator's own continuing self-run exhibition and art activity.
Resolving it needs a first-party statement of the mandate, which no page carried.

**Band: `lt_10k`, current-proxy.** Instagram @warbieyama, 8,060 followers, `og:description` retrieved 2026-07-31.
Instagram is the largest evidenced channel.
Anti-drift: the Facebook page @warbieyama reads 5,850 likes and X @WarbieYama reads 382 followers on the same identity, both `lt_10k`, and both are recorded here.
This band is flagged as understating the character's evidenced reach: Thai press treats LINE stickers as the channel that made it, and LINE carries no retrievable count, so the band vocabulary cannot see the channel that matters most for this row.
An Instagram account under the creator's own name did not resolve, so no creator-channel alternative is recorded.

**Control signals.** Solo creator: ASSUMED, and consistent with every page found. Label or agency attached: CONFIRMED at first-party level (the agent says so on its own newsroom), scope ASSUMED unresolved. Already under management: the agency relationship is the only such signal, dated from 2021 in market press. Prior assignment visible in press: none surfaced; press names the creator as author throughout.

**Evidence.**
- https://www.aruttantasirin.com/bio - first-party, retrieved 2026-07-31; creator identity, character origin, no management or studio entity named for the character.
- https://rivercitybangkok.com/its-me-warbie-the-inside-world-of-warbie-yama/ - venue's own exhibition page; names Arut as the creator and the show as a direct collaboration with the venue.
- https://www.tacconsumer.com/cn/news_details.php?i=276 and https://tacconsumer.com/news_details.php?i=276 - the agent's own newsroom, retrieved 2026-07-31; TACC describes itself as the Warbie character copyright agent.
- https://hoonsmart.com/archives/195941 - Hoonsmart; TACC's character agency portfolio, the San-X mandate and its territories, and the 2021 addition of Warbie Yama.
- https://www.matichon.co.th/economy/news_2776930 - search-surfaced only, HTTP 403 on retrieval; reported as naming the creator as copyright holder with TACC as licensing representative. Weaker citation, flagged.
- https://www.instagram.com/warbieyama/, https://www.facebook.com/warbieyama/, https://x.com/WarbieYama - counts retrieved 2026-07-31.

### 518. FLUFFY OMELET STUDIO

**Identity (CONFIRMED).** Fluffy Omelet, also styled ไข่เจียวปุย (Kai Jiew Pui), a Bangkok illustration and character studio whose own site describes it as a small studio started from a passion for drawing and turning sketches into everyday products.
Its characters include Fluffy Omelet and Crispy Bacon, Daisy and Smokey Cat.

**Who made it (CONFIRMED).** Positioning, a Thai marketing publisher, names คุณณัชริญา เหล่าศรีสิน as the artist behind the brand in its coverage of the MOSHI collaboration.
The Instagram account describes the same identity as a Thai illustrator and character artist making original artwork and designing merchandise.
The studio's own about page does not name her, so the artist identity rests on the publisher page rather than on first-party text, and the one-person reading of "small studio" is ASSUMED.

**Class: INDEPENDENT.** Creator-owned studio under a single named artist, with no corporate, platform or franchise parent surfaced.
The studio wrapper is the artist's own trading name, which is the 咖波 precedent's easy case.

**REP: yes.** Creator-owned, self-run store and platform channels, and brand collaborations that run in her own name.
The brand-side pass found the counterparties to be licensee brands and retailers rather than representatives: a Thai variety retailer's designer collaboration collection across its store network, a convenience-store café cup design, and a camera special edition with an international film-photography brand.
The Positioning piece describes the retailer partnering with the artist directly, and names no agent or intermediary.
Neither pass surfaced a licensing agent, label or management company.
The absence is a finding about what the sweep saw, not proof of no attachment.

**Band: `10k_50k`, current-proxy.** Instagram @fluffy_omelet, 42K followers, `og:description` retrieved 2026-07-31.
Instagram is the primary channel by a wide margin.
Anti-drift: the Facebook store page @fluffyomeletstore reads 3,850 likes on the same identity, `lt_10k`, and is recorded here.
This is the largest artist-side channel in the Thai IP-type set after the two company-held rows and Shewsheep.

**Control signals.** Solo creator: ASSUMED, consistent with the first-party "small studio" text and the single named artist. Label or agency attached: none surfaced (ASSUMED absent). Already under management: none surfaced. Prior assignment visible in press: none surfaced; the brand collaborations name the artist.

**Evidence.**
- https://positioningmag.com/pr-news/103019 - Positioning; names the artist, dates the MOSHI collaboration launch to 10 November 2024 across the retailer's store network, and names no intermediary.
- https://fluffyomeletstudio.com/our-story/ - first-party, retrieved 2026-07-31; self-description as a small studio, no parent or agent named.
- https://www.lomography.com/magazine/353150-enjoy-summer-on-film-with-the-lomoapparat-fluffy-omelet-special-edition - HTTP 403 on retrieval; the collaboration is search-surfaced and recorded as a brand-side data point only, not relied on.
- https://www.thebangkokinsight.com/news/pr-news/1510576/ - HTTP 403 on retrieval; the convenience-store café cup collaboration is search-surfaced and recorded the same way.
- https://www.instagram.com/fluffy_omelet/ and https://www.facebook.com/fluffyomeletstore/ - counts retrieved 2026-07-31.

### 520. Plaplatootoo

**Identity (CONFIRMED).** ปาป้า-ทูทู่ (Pla-pla Too-too), a character pair consisting of a small alien resembling a Mae Klong mackerel and a small robot that rides on its head, associated with Samut Songkhram province.
The Momentum, a Thai publisher, profiles the two people behind it: วิน (Bhattrapong Choosutti), art director and designer, and เต (Tatchasit Yoswipan), a freelance photographer and content creator.
The pair trade publicly as Plaplatootoo Studio on their own Facebook page.

**Own-mascot exclusion: tested and not triggered.**
This row is the one where the exclusion had to be checked seriously, because the character functions publicly as a provincial symbol.
The Momentum's account is that the designer first offered the character to the Samut Songkhram Chamber of Commerce for a festival and was turned down, then the two of them built the audience themselves on their own page, and the chamber adopted the character for the festival afterwards.
That sequence is adoption of an existing independent character, not a mascot commissioned by and made for the adopting body, so the own-mascot exclusion does not apply.
The same publisher describes them as independent creators rather than employed designers and names no corporate sponsor or management company; a national design-agency competition win is recorded as the character's origin story rather than as a holder relationship.
Ownership itself is not concluded here: what is recorded is that no page names any body other than the creators as the character's home.

**Class: INDEPENDENT.** Two named creators working under their own studio identity, with no corporate, platform or government parent surfaced.

**REP: yes.** Creator-owned, self-run channels, and public-facing work that runs in the creators' own studio name.
The brand-side pass surfaced provincial and tourism counterparties and local product collaborations, all of which read as users of the character rather than as representatives of it, and no licensing agent, label or management company surfaced in either pass.
The absence is a finding about what the sweep saw, not proof of no attachment.
Three Thai publisher interviews on this row returned HTTP 403 to direct retrieval, so the attachment test rests on the one long profile that did open plus the artist-side channel evidence, and that limit is stated rather than papered over.

**Band: `lt_10k`, current-proxy.** X @plaplatootoo, 3,330 followers, retrieved 2026-07-31 via the fxtwitter API.
Instagram @plaplatootoo reads 2,725 followers on the same identity, also `lt_10k`, retrieved 2026-07-31.
The primary channel is in fact the Facebook page @plaplatootoo.studio, whose count could not be retrieved: the page serves an `og:title` but no `og:description` to a crawler, on two user agents.
A Thai publisher article gives that page as being followed by 9,801 people, which is search-surfaced, undated in the summary, and below the band boundary; every evidenced channel therefore reads `lt_10k` and the band is called on that.
The row is flagged as near-boundary: the unretrievable Facebook count is the one that could move it.

**Control signals.** Two-person creator team: CONFIRMED at publisher level. Label or agency attached: none surfaced (ASSUMED absent). Already under management: none surfaced. Prior assignment visible in press: none surfaced; the provincial chamber's use is described as adoption, and no transfer is stated anywhere.

**Evidence.**
- https://themomentum.co/feature-plaplatootoo-samutsongkhram/ - The Momentum; names both creators and their roles, sets out the rejection-then-adoption sequence with the chamber of commerce, and names no management or sponsor entity.
- https://www.mangozero.com/plaplatootoo/ - search-surfaced; character description and the Facebook page follower figure. Weaker citation, flagged.
- https://urbancreature.co/plaplatootoo-interview/, https://www.sarakadeelite.com/faces/plapla-tootoo-thai-character/, https://www.prachachat.net/d-life/news-1459212 - all HTTP 403 on retrieval; attempts recorded, content not used.
- https://x.com/plaplatootoo and https://www.instagram.com/plaplatootoo/ - counts retrieved 2026-07-31.
- https://www.facebook.com/plaplatootoo.studio/ - page confirmed to exist under the studio name; no count served to a crawler on two attempts.

## What the shape test found

The hypothesis was that Thai character IP is corporate-shaped where Hong Kong was solo-creator-shaped.
As stated, it fails, and the way it fails is more useful than a confirmation would have been.

**A company or studio layer is nearly universal here, and that is not the same as corporate-held.**
Six of the seven rows carry some company or studio identity: 2Spot Communications, Sweet Summer Co., Ltd., Liffolab, Baan Maew Maew as a design and publishing studio, Fluffy Omelet Studio, and Plaplatootoo Studio.
But on four of those six the company is the creator's own vehicle, which under the pinned 咖波 precedent leaves the class INDEPENDENT.
Only two rows are corporate-held with no creator evidenced behind the property, and on one of those two the corporate reading is itself the assumed one.
So the entity count that would have looked like corporate shaping is mostly trading names, not holders.

**What is genuinely different from Hong Kong is the representation layer, not the ownership layer.**
Hong Kong's 32 rows produced no evidenced label or agency attachment at all.
Thailand's 7 produce one: a listed consumer-products company that publicly holds itself out as a character licensing agent, carrying both an imported Japanese portfolio and home-grown Thai characters, with one of these attendees among them.
That is a structurally different market feature from the art-toy label channelling that Hong Kong was tested for and did not evidence, and it is the single finding here most worth carrying into the remaining markets: the Thai attachment risk is a licensing-agency layer with listed-company economics, not a label.

**The creator-visibility asymmetry the census predicted held.**
On the rows where a creator exists, Thai-language artist-side queries were what surfaced them, and the brand-side material named the licensee and stopped there.
The one row where the artist-side pass produced nothing at all, in either language, is the row that is called PORTFOLIO on assumption rather than on a named holder, and that is recorded as an open question rather than resolved.

**Counts, stated only after every row carried a call.**
Seven rows adjudicated in total, one of them carried unchanged from the census rather than re-adjudicated.
Class: five INDEPENDENT (including the carried row), two PORTFOLIO.
REP: four yes (including the carried row), two no, one unclear.
Bands: four `lt_10k`, one `10k_50k`, two `50k_200k` (one of them carried).
Every band except the carried one is current-proxy.
Two rows are flagged as near-boundary and one is flagged as understating evidenced reach because its main channel is not countable.
No share, ratio or market-level figure is computed from these counts, here or anywhere in this file.

## Refusals and edge cases applied

- No rights_owner, chain-of-title, territory, exclusivity or deal-term conclusions anywhere in this file; where a publisher states a company holds a copyright, that is recorded as the publisher's statement and nothing is built on it.
- No outcome numbers; no percentages; no levels or ladder vocabulary; no brand images fetched.
- Pinned edge cases honoured: Toyzeroplus applied as a test on row 517 and left unresolved rather than forced; 咖波 applied on rows 514, 516, 518 and 520 to keep creator-owned companies INDEPENDENT, and tested and rejected on row 513 where the company principal is not the creator; own-mascot exclusion tested on row 520 and found not to apply; authorship-is-not-ownership applied on row 513, where the named designer is a member of staff and is not treated as a holder.
- Unresolved kept as an answer: row 515's creator question and row 517's agency scope are left open with the reason and with what would settle them.
- Row 516 was not re-adjudicated; its census class, REP and band are carried verbatim and this run added only the management-layer signal it was asked for.
- The exhibitor sheet's Notes column was not read in this run, per the scope; the company entities reported here were surfaced from evidence.
- Internal only. No figure in this file is quotable to a prospect.
