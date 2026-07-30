# TASK: ip_scale_band enrichment pass - all ten markets, independent rows

The comparable-bands teaser feature died on one fact: only ~5 of ~190 independent census rows record the IP's audience scale. This pass fixes exactly that - a per-row research enrichment adding each independent IP's follower-scale band AT CAMPAIGN TIME, from public evidence, across all ten market censuses. The output is what makes "which brand scales actually ran IPs at each band" an answerable question.

## Scope

Every INDEPENDENT row in all ten findings/census/<market>/campaigns.md tables (taiwan-v2, japan, korea, malaysia, thailand, singapore, hongkong, philippines, vietnam, indonesia). Include Indonesia's MIXED row 2 on its Si Juki side. PORTFOLIO and UNCLEAR rows are out of scope.

**Priority order:** REPRESENTABLE=yes rows first (all markets), then REP=unclear, then REP=no. If iteration budget runs short, complete priority tiers, don't spread - a fully-banded REP=yes set is the usable core.

## The band vocabulary - EXACTLY these codes, no others

lt_10k / 10k_50k / 50k_200k / 200k_1m / gt_1m / unknown

These match the /start intake's follower_band codes character-for-character (the Cortex alignment point - a lossy mapping here costs forever). Band = the IP's PRIMARY channel following (the creator's main platform for that character) at the time of the campaign.

## Evidence rules

1. **At-campaign-time is the target.** Acceptable evidence: press coverage stating a following at/near the campaign date, archived profile snapshots (Wayback and equivalents), the campaign's own materials citing reach, platform milestones dated near the window. Record the evidence source URL and its date per row.
2. **Today-only evidence is second-class but recordable:** if only a CURRENT follower count is findable, record the band it implies with the flag `current-proxy` and the retrieval date - never presented as at-campaign truth. A campaign from 2024 banded off a 2026 count is a proxy, and the flag says so.
3. **Unknowable stays unknown.** No triangulation-by-vibes, no inferring scale from "popular," no using brand prestige as a scale proxy. If no countable public evidence exists, the band is `unknown` with a one-line note of what was checked. An honest unknown beats a guessed band - the downstream feature renders nothing for unknowns by design.
4. **Primary-channel judgment recorded:** where a creator runs multiple platforms, name which platform the band reads from and why (largest evidenced following wins; ties note both).
5. No outcomes, no revenue, no sell-through - scale only.

## Deliverables

Do NOT modify any campaigns.md - the census tables are accepted artifacts. Instead, per market:

`findings/census/<market>/ip_scale_bands.md` - a table:
| Row # | IP | Creator | REP | Band | Evidence basis (at-campaign / current-proxy / unknown) | Primary channel | Source URL + date | Notes |

One row per independent census row, every row present even when band = unknown.

Then one summary: `findings/census/IP_SCALE_BANDS_SUMMARY.md` -
1. Coverage table per market: independent rows, banded-at-campaign count, current-proxy count, unknown count
2. The band distribution across all banded rows (how many campaigns at each band, per market and pooled-with-the-usual-refusal-note if depths differ materially)
3. A first cross-tab PREVIEW: band x brand identity for the banded rows (which brands ran IPs at which bands) - clearly marked preview, the real derivation happens at import
4. Honesty section: the current-proxy share, markets where banding was hardest and why, and a plain statement of whether the banded coverage is sufficient to support the comparable-bands feature honestly (a judgment with reasons, not a yes by default)

## Rules

Curl-verified evidence URLs. The existing census row data (IP names, creators, dates) is the index - read it, never edit it. Anti-drift: the band reflects the IP/character's channel, not the creator's personal account where they're distinguishable and both evidenced (note the choice when it matters). Commit per market or per few markets; push at end.

Out of scope: portfolio rows, any census table edits, the consolidation doc, any Cortex import, the bands render itself.