# Taiwan co-branding census - portfolio vs independent IP

RECURRING TASK (tasks/cobranding-census.md). First run builds the census;
later runs EXTEND it - append newly found campaigns to the existing
table, never re-verify existing rows, and rewrite _VERDICT.md with a
fresh "as of" date.

MISSION: count and classify identifiable brand-x-IP CO-BRANDING campaigns
in Taiwan from 2024-01-01 to present (full-year 2024, full-year 2025, and
2026 year-to-date - kept separable so complete years can be cited alone),
answering: what share used corporate-portfolio IPs vs independent-creator
IPs, and how prominent are indies really? ATTACK the founder thesis
("indies are shut out") as hard as the data allows - if indies are more
present than we believe, that finding matters MORE, not less.

SCOPE: co-branding/collab campaigns only - a brand pairing with a
character/illustration IP for products, drinks, events, or campaigns
(聯名). EXCLUDE plain licensed merchandise at retail (a Disney mug is
licensing, not co-branding) and KOL/celebrity endorsements. Taiwan-market
campaigns only (TW brands or TW editions of chains).

CLASSIFICATION RULES (record the call + evidence per campaign):
- CORPORATE-PORTFOLIO: IP owned/controlled by a major licensor, studio,
  or media/platform conglomerate (Disney/Pixar/Marvel, Sanrio, San-X,
  Nintendo/Pokemon, Warner, LINE FRIENDS/IPX, Kakao Friends, major anime
  committees, Chiikawa/major publisher-managed properties).
- INDEPENDENT: creator- or small-studio-owned, no conglomerate parent
  (Taiwan illustrator IPs like 咖波/Bugcat Capoo, 爽爽貓, 白爛貓-class,
  and foreign indie characters) - note: signed-to-an-agency does NOT make
  an IP corporate; ownership does.
- UNCLEAR: state why; count separately, never force a bucket.

METHOD (state it in the output - this is a sample census, not a claim of
exhaustiveness): sweep zh-TW sources - brand news (ETtoday/聯合/自由
lifestyle sections), campaign roundups, convenience-store and hand-shake
drink collab trackers, brand FB/IG announcements, 7-11/全家/全聯 campaign
pages, licensing trade coverage. Log every campaign found:
findings/census/campaigns.md as one growing table - date, YEAR tag
(2024 / 2025 / 2026YTD, so per-year splits compute directly), brand, IP,
IP class (+evidence), format (drink/merch/event/store), source URL.
Every row curl-verified; phantom entries are the known failure class.
On a refresh run: check the existing table first and only append
campaigns not already logged.

ANALYSIS OUTPUT findings/census/_VERDICT.md (opens with "As of
YYYY-MM-DD"; rewritten each refresh):
1. The ratio - overall AND per year: N campaigns found; X% portfolio /
   Y% indie / Z% unclear overall, then the same split for 2024, 2025,
   and 2026YTD separately - is the indie share growing, flat, or
   shrinking? The per-year trend is the deck's strongest possible form
   of this number.
2. Indie prominence: which indie IPs appear, how often, in what formats,
   with which brand sizes - are the same 3-4 Taiwan illustrator IPs
   recycling, or is there breadth? Do indies get big-brand collabs or
   only small-brand ones?
3. The thesis read: does the data support "indies are shut out", refine
   it (shut out of certain formats/brand tiers), or weaken it? Honest
   verdict with the strongest counter-examples quoted.
4. Method limits, stated plainly: recall bias toward covered campaigns,
   the window (2024-01-01 to run date), format skew.

RULES: never fabricate; "not found under [queries]" stays as stated;
zh-TW primary; single-source rows flagged; per iteration, aim for 15-25
verified campaign rows or one analysis section - depth over speed.

COMPLETION: campaigns.md holds the verified year-tagged table,
_VERDICT.md exists with all four sections including the per-year splits.