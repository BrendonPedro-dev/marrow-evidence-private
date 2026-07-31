TASK: CET2026 attendee prioritisation - PHASE 0, census match only

INPUT: tasks/input/cet2026-orgs.md - 521 rows, Name / Country / Type / Notes.
This is the ONLY input file. Ignore anything else in tasks/input/.
Public exhibitor directory data from creativexpo.tw. Organisation and IP names only;
no contact data is present and none may be added.

SCOPE: matching only. No web queries in this run. Everything needed is already in
this repo.

DO
1. Match all 521 names against the ten-market census (1,054 rows, 234 INDEPENDENT)
   and the ip_scale_bands pass (235 rows). Match on name, with romanisation and
   alternate-script variants attempted; record the basis of every match.
2. Report per market: matched, unmatched, ambiguous. Ambiguous is a valid outcome
   and must not be forced either way.
3. For matched rows, carry through what the census already adjudicated - class
   (INDEPENDENT / PORTFOLIO / MIXED), REP call, ip_scale_band. Do not re-derive it.
4. Report Hong Kong separately and prominently. 33 HK attendees, all IP-side, against
   a census that found 6 distinct addressable creators in that market. State how many
   match, how many are new to the census, and how many show label attachment on the
   evidence already in the census tables.
5. Treat the sheet's Notes column as unverified prior research to be checked later,
   never as a finding.

THE COVERAGE FINDING - a stated output, not a side effect
Every addressable-creator count in the census is explicitly a floor (Hong Kong's
verdict says the ceiling is above 6 and names the reason; the Philippines and
Indonesia say floor outright). This attendee list is a sampling frame the census
never had. Report what the unmatched share implies about census coverage per market,
as a measurement observation with its own confidence, not as a corrected number.
Do not restate any market's indie share.

REFUSALS
- No new research in this run. If a name cannot be matched, it is unmatched.
- Never conclude rights_owner, chain of title, territory, exclusivity or deal terms.
- Never state or imply outcome numbers. Never fetch brand images.
- Hong Kong's indie share is NOT quotable on its own (2.6% to 14.0%, biased upward).
  Internal use only; never in any prospect-facing output.
- No levels or ladder vocabulary.
- Poland (2 rows) and Macao (1 row) have NO census coverage. Report them as
  out-of-coverage; do not substitute a neighbouring market.
- Pinned edge cases apply: Toyzeroplus, Molly Factory, Kumamon, 咖波, own-mascot
  exclusion, authorship is not ownership.

OUTPUT: findings/expo/cet2026-match.md
Per-market matched / unmatched / ambiguous counts, the Hong Kong section stated
separately, the coverage observation, and a per-row table carrying the census verdict
where one exists. Unresolved is a valid answer and must not be filled in.