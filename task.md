# TASK: Thailand co-branding census (brand x character collaborations, 2024-2026YTD)

Extend the co-branding census to Thailand. Same job as taiwan-v2 / japan / korea / malaysia: the verified campaign table and the verdict, on the IDENTICAL definition, so all markets compare row-for-row.

## The definition (identical to the prior runs - do not drift)

A row is a brand x character IP collaboration campaign running in Thailand with any activity in 2024, 2025, or 2026 year-to-date. F&B-led but not F&B-only: retail, convenience, telco, banking, and mall campaigns count when a character IP fronts a consumer campaign.

**Ownership test per IP (the bucket call):**
- portfolio = owned by a corporation, estate, platform, or media franchise (or majority stake)
- independent = creator-owned. Agency-managed but creator-owned = independent (the 咖波 precedent)
- unclear = genuinely unresolvable after digging - use sparingly, record what was checked

**Pinned edge cases (carried forward):**
- Miffy = portfolio (estate + other IP)
- Snoopy = portfolio (Sony stake)
- Government-owned mascots = EXCLUDED (the Kumamon rule)
- Platform-owned characters (LINE Friends class) = portfolio

**REPRESENTABLE sub-tag** on independent rows only: yes / no / unclear - could an agency plausibly represent this IP (creator-owned, not captive, commercially active)? Non-indie rows carry '-'.

## The Thailand-specific key calls

1. **Thai-native sources are the market.** Thailand's character-collab coverage lives on Thai-language media, brand Facebook pages (FB dominates Thai brand comms), and LINE - an EN-only sweep will miss most of the market. Dig Thai-native: brand FB/IG posts, Thai marketing press (Marketeer, Brand Buffet, Marketing Oops), mall socials. Flag every row where Thai-source translation confidence is low rather than guessing - the translation-confidence flag is first-class in this market, expect to use it.
2. **The sticker-native creator scene is the indie bucket's heart.** Thailand's indie character economy grew out of LINE stickers - creators whose characters are sticker-first (the Cheesy Duck class) and license into merch/F&B from there. The ownership call: the creator owns the character even when LINE hosts the stickers - hosting is not owning (same line as the Korea webtoon-platform rule). LINE Friends' own characters remain portfolio. This distinction is where Thailand's indie count is won or lost.
3. **CP/conglomerate retail concentration:** 7-Eleven Thailand (CP ALL), Lotus's, Big C run character campaigns at national scale - each campaign is one row per the standard rule, and the brand is the Thai operator. Regional deals count only with evidenced TH activation (TH stores, TH-market announcement, Thai-social promotion) - same rule as Malaysia's franchise-local call.

**Known-entity rule:** Cheesy Duck (X10 Studio) may surface in Thai rows. Record from PUBLIC sources only, exactly like any other row - no internal knowledge enters the census. Where a public source and internal knowledge disagree, the census records the public source.

## Evidence standard (unchanged)

Every row curl-verified against a live source URL. Year tag from evidenced campaign dates - never inferred. Single-source rows flagged in notes. No invented dates, no invented outcomes, no outcome claims of any kind.

## Deliverables

`findings/census/thailand/campaigns.md` - the table:
| # | Date / window | Year | Brand | IP | IP class + ownership evidence | REPRESENTABLE | Format | Source | Notes |

`findings/census/thailand/_VERDICT.md` - all five sections:
1. The ratio - overall and per year (portfolio / independent / unclear counts and shares)
2. The addressable-indie read - REPRESENTABLE yes/no/unclear split within indie rows
3. Format mix and year trend
4. Methodology + edge cases encountered and how the pinned rules resolved them (the sticker-creator ownership calls especially)
5. Coverage-confidence statement: single-source count, translation-flagged count, and an honest depth read - a true smaller number beats a padded one

## Target

Comparable depth to the prior markets (~120-140 rows) IF the market supports it. Floor for a credible verdict: ~80 verified rows or an explicit documented coverage ceiling.

Out of scope: no Cortex import, no consolidation doc (that comes as its own task after this run), no outcome claims.