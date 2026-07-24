# Korea co-branding census - portfolio vs independent IP

RECURRING TASK. Region-by-region series (Taiwan done: 129 rows). This is
the KOREA run - identical definition and rules to Taiwan so the three
markets are directly comparable; only the market, sources, and output
path change. First run builds; later runs EXTEND (append new campaigns,
never re-verify existing rows, rewrite _VERDICT with a fresh date).

MISSION: count and classify identifiable brand-x-IP CO-BRANDING campaigns
in KOREA from 2024-01-01 to present (full-year 2024, full-year 2025, and
2026 year-to-date - kept separable so complete years can be cited alone),
answering: what share used corporate-portfolio IPs vs independent-creator
IPs, and - the number PBC actually needs - what share are CREATOR-OWNED
AND POTENTIALLY REPRESENTABLE. Attack any thesis as hard as the data
allows; if indies are more or less present than expected, that finding
matters more, not less.

SCOPE: co-branding/collab campaigns only - a brand pairing with a
character/illustration IP for products, drinks, events, or campaigns
(コラボ / 콜라보). EXCLUDE plain licensed merchandise at retail (a Disney
mug is licensing, not co-branding) and celebrity/talent endorsements.
Korea-market campaigns only (Koreaese brands or Korea editions of chains).

## CLASSIFICATION - the ownership test (identical across all markets)

The test is ALWAYS: who OWNS and CONTROLS the IP now? Not fame, not size,
not who runs the campaign. Record the call + ownership evidence + source
per campaign.

- CORPORATE-PORTFOLIO: owned/controlled by a major licensor, studio,
  media/platform conglomerate, licensing company, or estate that manages
  OTHER IP (Sanrio, San-X, Bandai/Sunstar, Pokemon/Nintendo, major anime
  committees, LINE Friends/platform-owned characters, publisher-managed
  properties).
- INDEPENDENT: owned by a living creator or a small studio with no
  portfolio parent. Being managed/represented by an agency does NOT make
  it corporate - represented ≠ owned. Fame and size do NOT move an
  indie to portfolio.
- UNCLEAR: ownership genuinely cannot be established after a second
  search, OR a true borderline (co-owned 50/50, brand-mascot-vs-character
  ambiguity). Count separately, never force a bucket.

### Pinned edge cases (apply identically in every market)
- Creator SOLD control to a conglomerate -> PORTFOLIO (e.g. Snoopy /
  Peanuts: Sony holds a controlling stake - portfolio despite origin).
- Estate-owned, creator deceased, entity holds other IP -> PORTFOLIO
  (e.g. Miffy / Mercis BV - portfolio even as a single iconic character).
- Agency-MANAGED but creator-OWNED -> INDEPENDENT (dig past the agency to
  the owner; this is PBC's client profile).
- A brand's OWN mascot collaborating -> NOT COUNTED (own asset, not a
  license).
- Government / public-body owned (e.g. Kumamon / Kumamoto Prefecture) ->
  EXCLUDE from the indie/portfolio split (public asset, not a market
  participant); note separately.
- Webtoon/platform characters -> INDEPENDENT if the artist owns it,
  PORTFOLIO if the platform owns it. THIS IS THE KEY KOREA DISTINCTION:
  many Korean character IPs originate as webtoons/LINE/Kakao stickers.
  Kakao Friends and LINE Friends characters are PLATFORM-OWNED = portfolio.
  But an independent webtoon artist who retains ownership and licenses
  through an agency = INDEPENDENT (and likely REPRESENTABLE). Dig into
  whether the platform owns the character or merely hosted the artist's
  work - that ownership line decides the bucket and is often the hardest
  call in this market.
- Co-owned / JV -> whoever holds control; genuine 50/50 -> UNCLEAR.

### The PBC sub-tag (Gary-approved) - on INDEPENDENT rows only
For each INDEPENDENT row, add REPRESENTABLE = yes / no / unclear:
- yes = creator-owned, no conglomerate stake, not already locked to an
  exclusive agency in a way that would preclude representation - i.e. a
  plausible PBC client.
- no = indie by ownership but already exclusively tied up (own agency,
  captive studio) such that representation is closed.
- unclear = can't tell from public sources.
This column is the market-entry signal: how much addressable indie IP
exists in Korea, not just how much indie IP exists.

## METHOD - dig for ownership, don't stop at the surface
When the owner isn't clear from the campaign article, do a SECOND search
before classifying: "[character] 저작권 / 판권 / 라이선스 소유", the licensor's company page,
the IP's official site. An AGENCY / 에이전시 name in the deal is NOT the owner - dig past it to who OWNS the IP. If
ownership genuinely can't be established after the second search, mark
UNCLEAR and state what you searched - never guess an owner to force a
bucket.

Sweep ko sources: brand news and lifestyle press (Naver news, 매일경제/
한국경제 lifestyle, 데일리, 인사이트, 위키트리), convenience-store and cafe
collab trackers (CU/GS25/세븐일레븐/이마트24 campaign pages, 메가커피/
컴포즈커피/투썸 collab coverage), brand official Instagram/naver-blog
announcements, character-goods and pop-up (더현대/성수 popup) coverage,
licensing trade press. Every row curl-verified; phantom entries are the known
failure class. On a refresh run, check the existing table first and only
append campaigns not already logged.

Log to findings/census/korea/campaigns.md as one growing table: date,
YEAR tag (2024 / 2025 / 2026YTD), brand, IP, IP class (+ownership
evidence), REPRESENTABLE (indie rows only), format
(drink/merch/event/store), source URL.

## ANALYSIS OUTPUT findings/census/korea/_VERDICT.md (opens "As of
YYYY-MM-DD"; rewritten each refresh):
1. The ratio - overall AND per year: N campaigns; % portfolio / indie /
   unclear overall, then the same split for 2024, 2025, 2026YTD. Is the
   indie share growing, flat, or shrinking?
2. The addressable number: of the indie rows, how many are REPRESENTABLE
   (yes) - the count and share that could plausibly be PBC clients. This
   is the market-entry read.
3. Indie prominence: which indie IPs appear, how often, formats, brand
   sizes - a few recycling names or real breadth? Do indies land
   big-brand collabs?
4. The thesis read: does Korea support / refine / weaken "indies are a
   minor share"? Honest verdict, strongest counter-examples quoted.
5. Method limits, stated plainly: recall bias toward covered campaigns,
   the window (2024-01-01 to run date), format skew, and where ownership
   was hard to establish (the unclear rate is itself a finding).

RULES: never fabricate; "not found under [queries]" stays as stated; ja
sources primary; single-source rows flagged; per iteration aim for 15-25
verified rows or one analysis section - depth over speed.

COMPLETION: findings/census/korea/campaigns.md holds at least 120
curl-verified year-tagged rows spanning 2024, 2025 and 2026 (with
ownership evidence per row and REPRESENTABLE on indie rows), and
findings/census/korea/_VERDICT.md exists with all five sections including
the per-year splits and the addressable-indie number.