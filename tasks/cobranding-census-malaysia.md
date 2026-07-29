# TASK: Malaysia co-branding census (brand x character collaborations, 2024-2026YTD)

Extend the co-branding census to Malaysia. Same job as the Taiwan v2, Japan, and Korea runs: build the verified campaign table and the verdict, on the IDENTICAL definition, so all markets compare row-for-row.

## The definition (identical to taiwan-v2 / japan / korea - do not drift)

A row is a brand x character IP collaboration campaign running in Malaysia with any activity in 2024, 2025, or 2026 year-to-date. F&B-led but not F&B-only: retail, convenience, telco, banking, and mall campaigns count when a character IP fronts a consumer campaign.

**Ownership test per IP (the bucket call):**
- portfolio = the character is owned by a corporation, estate, platform, or media franchise (or majority stake thereof)
- independent = creator-owned. Agency-managed but creator-owned = independent (the 咖波 precedent)
- unclear = genuinely unresolvable after digging - use sparingly, record what was checked

**Pinned edge cases (carried from the prior runs):**
- Miffy = portfolio (estate + other IP)
- Snoopy = portfolio (Sony stake)
- Government-owned mascots = EXCLUDED entirely (the Kumamon rule)
- Platform-owned characters (LINE Friends class) = portfolio

**REPRESENTABLE sub-tag** on independent rows only: yes / no / unclear - could an agency like PBC plausibly represent this IP (creator-owned, not already locked into a captive arrangement, commercially active)? Non-indie rows carry '-'.

## The Malaysia-specific key call

Malaysia's collab landscape is mall- and franchise-heavy, and the market runs trilingual (EN / BM / zh). Two things decide where this census is won or lost:

1. **Franchise-local vs principal-run campaigns**: a global chain's MY arm (Pizza Hut Malaysia, Tealive, ZUS, Secret Recipe, MyNews, FamilyMart MY) running a character campaign counts as a Malaysia row even when the IP deal was struck regionally - the campaign ran in MY. Record the brand as the MY operator and note "regional deal, MY activation" where the evidence shows it. Do not double-count a regional campaign into MY unless MY activation is evidenced (MY store presence, MY-market announcement, BM/MY-social promotion).
2. **Source-language honesty**: sources will span EN, BM, and zh. Where a row rests on a BM or zh source and translation confidence is low, flag it in notes rather than guessing. Local media (SAYS, WauPost, Vulcan Post MY, mall and brand socials) will carry campaigns the EN trade press never covers - dig there; an EN-only sweep will systematically undercount local indie campaigns.

**Known-entity rule:** Bichi Mao's own MY collabs (Pizza Hut MY, SODA, Secret Recipe) will surface. Record them from PUBLIC sources only, exactly like any other row - no internal knowledge (deck figures, sell-through, royalties) enters the census. Where a public source and internal knowledge disagree, the census records the public source.

## Evidence standard (unchanged)

Every row curl-verified against a live source URL. Year tag from evidenced campaign dates - never inferred from "probably." Single-source rows flagged in notes. No invented dates, no invented outcomes, no outcome claims of any kind.

## Deliverables

`findings/census/malaysia/campaigns.md` - the table:
| # | Date / window | Year | Brand | IP | IP class + ownership evidence | REPRESENTABLE | Format | Source | Notes |

`findings/census/malaysia/_VERDICT.md` - all five sections:
1. The ratio - overall and per year (portfolio / independent / unclear counts and shares)
2. The addressable-indie read - REPRESENTABLE yes/no/unclear split within indie rows
3. Format mix and year trend
4. Methodology + edge cases encountered and how the pinned rules resolved them (the franchise-local calls especially)
5. Coverage-confidence statement: single-source count, language-flagged count, and an honest read on depth - if Malaysian collab volume is structurally thinner than TW/JP/KR, say so with the true number; an honest 80 beats a padded 130

## Target

Comparable depth to the prior markets (~120-140 rows) IF the market supports it. Floor for a credible verdict: ~80 verified rows or an explicit documented coverage ceiling explaining why fewer is the true number.

Out of scope: no Cortex import, no consolidation doc (that comes after Thailand), no outcome claims.