# Map-target brand briefs - approach-ready research

RECURRING TASK (tasks/brand-briefs.md). Runs once per strategic-map
version. INPUT: map-targets.md in this repo - refresh it from the latest
STRATEGIC_MAP_vN before each run.

MISSION: deep public-source research on the strategic map's top-ranked
brands so PBC's outreach opens informed. Work each IP's top 8 ranked
brands, deduplicating brands ranked under several IPs (one brief per
brand, noting all IPs it ranked for).

WHAT TO SKIP (check findings/brands/_INDEX.md FIRST):
- SKIP brands whose brief's Researched date is within the last 90 days,
  unless map-targets.md marks them CHANGED.
- Briefs older than 90 days whose brands remain in the top ranks get a
  REFRESH pass: update momentum/campaigns/decision-context, keep stable
  identity sections, bump the Researched date, append a "What changed
  since [old date]" line - never silently rewrite.
- Brands new to the top ranks get full briefs.

THE IPs (context for angle-fit):
- Bichi Mao 彼奇貓: Malaysian cat character, healing/warm style, Taiwan
  licensing via PBC; strongest with pet/animal-welfare/F&B audiences.
- Cheesy Duck 確幸鴨: Thai duck character; picture-book and F&B angles.
- Jolly Gee Studio: Korean retro-kitsch character family (JOLLY/LYGEE/
  LYLEE); stationery, lifestyle goods, cafe collabs.
- SHUYA 舒雅: illustration IP; lifestyle/pastry/bookstore angles.

PER BRAND, research and write findings/brands/<brand-slug>.md. Every
brief opens with a header line:
"Researched: YYYY-MM-DD | IPs ranked for: ... | Status: complete"
Then the seven sections:
1. IDENTITY: official name (en+zh), what they sell, ownership/parent,
   scale (stores/size if public), official site + socials with follower
   counts (dated, labelled estimates).
2. AUDIENCE: who buys/follows - demographics as publicly evidenced,
   always labelled estimate vs stated.
3. RECENT MOMENTUM: campaigns, launches, expansion, press from the last
   ~18 months, each dated with URL.
4. COLLAB/IP HISTORY: past character/IP collaborations - partner, year,
   format, any public read on results. "None found under [queries]" is a
   valid answer and must be stated as exactly that.
5. DECISION CONTEXT: how marketing decisions appear to run (marketing
   dept? owner-led? franchise HQ?), any named marketing contacts ONLY
   from official/public pages (title + where seen; no scraped personal
   emails/phones - note the official contact surface instead).
6. SUGGESTED ANGLE: 2-3 sentences - which of the ranked IPs fits this
   brand best and why, tied to evidence above; flag which campaign goal
   it maps to (foot traffic/seasonal, awareness, identity, audience).
   Label as suggestion, not finding.
7. SOURCES: every claim URL'd; single-source claims flagged; first-person
   brand statements ranked above third-party coverage.

RULES: zh-TW sources primary for Taiwan brands, zh-CN/ja/en as needed.
Never fabricate; curl-verify any quote used verbatim (phantom quotes from
search snippets are a known failure - verified twice). No rights/
territory/exclusivity guesses ever. Estimates labelled. Where the map's
one-line why cited a research note or reply-on-record, treat that as
PBC-internal context to build around, not to re-verify publicly.

PER ITERATION: complete 2-4 brand briefs fully rather than many
partially. Maintain findings/brands/_INDEX.md as you go: brand, IPs
ranked for, Researched date, brief status, one-line headline.

COMPLETION: all top-8-per-IP unique brands from map-targets.md have
current briefs (new or refreshed per the skip rules) + _INDEX.md complete
with Researched dates + findings/brands/_SUMMARY.md rewritten (opens
"As of YYYY-MM-DD"; cross-brand patterns: which angles repeat, which
brands look strongest per IP, contact-surface gaps).