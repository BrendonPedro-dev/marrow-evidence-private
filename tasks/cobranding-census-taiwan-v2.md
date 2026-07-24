# Taiwan co-branding census - portfolio vs independent IP

RECURRING TASK - TAIWAN RE-RUN (v2). The original Taiwan census (129 rows,
findings/census/campaigns.md) predates the pinned edge cases and the
REPRESENTABLE sub-tag. This run brings Taiwan onto the IDENTICAL definition
as Japan and Korea so all three compare cleanly.

METHOD FOR THIS RE-RUN - re-classify + enrich, don't re-find:
1. START from the existing findings/census/campaigns.md (the 129 rows).
   Copy them into findings/census/taiwan-v2/campaigns.md.
2. RE-CLASSIFY every existing row against the updated ownership test +
   pinned edge cases below. Flag any row whose bucket CHANGES under the
   new rules (that delta is a finding - report it).
3. ADD the REPRESENTABLE column to every INDEPENDENT row.
4. Only THEN top up with any new campaigns toward 120+ if rows were
   reclassified out or the coverage thinned.
The question this answers: does the indie share hold at ~27% under the
stricter definition, or do the edge cases move it? Report the before/after
explicitly.

MISSION: count and classify identifiable brand-x-IP CO-BRANDING campaigns
in TAIWAN from 2024-01-01 to present (full-year 2024, full-year 2025, and
2026 year-to-date - kept separable so complete years can be cited alone),
answering: what share used corporate-portfolio IPs vs independent-creator
IPs, and - the number PBC actually needs - what share are CREATOR-OWNED
AND POTENTIALLY REPRESENTABLE. Attack any thesis as hard as the data
allows; if indies are more or less present than expected, that finding
matters more, not less.

SCOPE: co-branding/collab campaigns only - a brand pairing with a
character/illustration IP for products, drinks, events, or campaigns
(聯名). EXCLUDE plain licensed merchandise at retail (a Disney
mug is licensing, not co-branding) and celebrity/talent endorsements.
Taiwan-market campaigns only (Taiwanese brands or Taiwan editions of chains).

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
  PORTFOLIO if the platform owns it.
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
exists in Taiwan, not just how much indie IP exists.

## METHOD - dig for ownership, don't stop at the surface
When the owner isn't clear from the campaign article, do a SECOND search
before classifying: "who owns [character] / [character] 版權 / 授權", the licensor's company
page, the IP's official site. An AGENCY name in the deal is NOT the owner - dig past it to who OWNS the IP. If
ownership genuinely can't be established after the second search, mark
UNCLEAR and state what you searched - never guess an owner to force a
bucket.

Sweep zh-TW sources: brand news and lifestyle press (ETtoday/聯合/自由
lifestyle, mook, ctwant, dailyview, niusnews), convenience-store and
hand-shake-drink collab trackers (7-11/全家/全聯 campaign pages, the
drink-chain collab roundups), brand official FB/IG announcements,
character-goods and pop-up coverage, licensing trade press. Every row curl-verified; phantom entries are the known
failure class. On a refresh run, check the existing table first and only
append campaigns not already logged.

Log to findings/census/taiwan-v2/campaigns.md as one growing table: date,
YEAR tag (2024 / 2025 / 2026YTD), brand, IP, IP class (+ownership
evidence), REPRESENTABLE (indie rows only), format
(drink/merch/event/store), source URL.

## ANALYSIS OUTPUT findings/census/taiwan-v2/_VERDICT.md (opens "As of
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
4. The thesis read: does Taiwan support / refine / weaken "indies are a
   minor share"? Honest verdict, strongest counter-examples quoted.
5. Method limits, stated plainly: recall bias toward covered campaigns,
   the window (2024-01-01 to run date), format skew, and where ownership
   was hard to establish (the unclear rate is itself a finding).

RULES: never fabricate; "not found under [queries]" stays as stated; ja
sources primary; single-source rows flagged; per iteration aim for 15-25
verified rows or one analysis section - depth over speed.

COMPLETION: findings/census/taiwan-v2/campaigns.md holds at least 120
curl-verified year-tagged rows spanning 2024, 2025 and 2026 (with
ownership evidence per row and REPRESENTABLE on indie rows), and
findings/census/taiwan-v2/_VERDICT.md exists with all five sections including
the per-year splits and the addressable-indie number.