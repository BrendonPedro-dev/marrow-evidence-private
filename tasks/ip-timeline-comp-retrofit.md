# TASK: IP growth timelines - Bichi Mao build + comp-pool retrofit (scale anchors + engine determination)

The growth timelines have a new job: they are the PRO-COMP POOL for the comparable-bands feature. A comp reads "an early-stage LAIMO type" - which requires each timeline to answer "at what scale was this IP when it did X" (scale anchors) and "which growth engine does this arc represent" (engine determination). The existing four timelines (Capoo, LAIMO, Monday Bruce, LuLu the Piggy) are event sequences without scale anchors; Bichi Mao's timeline doesn't exist yet. This run does both.

## Part 1 - Bichi Mao timeline (new, built comp-ready from birth)

Same spec as the existing four: the OBSERVABLE public sequence only - product launches, brand collabs, platform milestones, market entries, exhibition/event appearances - each event dated and curl-verified against a live public source. Malaysian IP (creator: Wee / Niko Studio); the known public record includes Pizza Hut Malaysia, SODA apparel, Secret Recipe, the 2026 Taiwan IP Expo appearance (Sunway Pyramid), and the MY census rows 9/10 (the ~995K count near the gt_1m edge is already recorded in malaysia/ip_scale_bands.md - reuse it). PBC-INTERNAL wall applies absolutely: public record ONLY - nothing from the Wee interview, the deck, SODA figures, or any PBC-held material enters this artifact. If the public record is thin, the timeline is honestly thin.

Scale anchors from birth: per timeline event, band the IP's primary channel at that event's date where evidence allows (see Part 2 rules).

## Part 2 - Scale-anchor retrofit of the existing four timelines

APPEND, never rewrite: each existing timeline file gains a scale-anchor section/column - the event records themselves are untouched (the re-sweep discipline). Per major event in each timeline, attempt a band at that date:

1. **Bracketing first** (the enrichment pass's strongest construction): a dated figure before the event + a dated/live figure after, both in the same band = that band, drift-proof. Sources: archived profile snapshots (Wayback), dated press floors, platform milestone announcements.
2. **Dated press floors** ("突破10萬", "over 500k") usable when both drift directions stay in-band.
3. The enrichment pass's proven methods apply: crawler user-agent for Instagram, fxtwitter API for X counts, facebookexternalhit UA for TikTok.
4. **Honest unknowns stand:** Capoo and LAIMO are Facebook-primary and 白爛貓-class pages were named CLOSED platforms in the enrichment pass - anchors there may be unresolvable or rest solely on press floors. Record `unknown` with what was checked; never infer a band from prominence. Not every event needs an anchor - anchor the events that matter for comps (early collabs, first brand deals, scale-milestone moments) and say which were not attempted.

Band vocabulary EXACTLY: lt_10k / 10k_50k / 50k_200k / 200k_1m / gt_1m / unknown, primary single channel, never cross-platform totals - identical to the enrichment pass.

## Part 3 - Engine determination, all five IPs

Per IP, one stated determination against the two-engines framework from the original timeline research (fame-first vs designer-toy/goods-first - use the framework as the existing timeline findings define it, do not invent new engine names): which engine this arc represents, the observable evidence for the call, and a confidence note. If an arc genuinely doesn't fit either engine or shows a hybrid, say so plainly - a third pattern honestly observed beats a forced classification. This determination is what the comp feature's engine-matching consumes ("a goods-first prospect comps to goods-first arcs only").

## Deliverables

1. `findings/timelines/bichi-mao.md` (or the established timelines path - match the existing four's location and format exactly; check where they live first)
2. The four existing timeline files, each appended with: `## Scale anchors (2026-07 retrofit)` section + `## Engine determination` section
3. `findings/timelines/COMP_POOL_STATUS.md` - the pool summary: per IP - engine determination, anchor coverage (how many events banded, by evidence class), the plain-language era labels the comp feature would surface ("goods-led early chapters" etc., proposed from the arc's observable phases), and an honesty line on comp-readiness per IP (ready / partially ready / thin-with-reasons)

## Rules

Curl-verified sources per new claim. Append-only on existing files. No PBC-internal material anywhere. No outcome claims, no revenue, no trajectory language ("went on to become" describes the record; "will become" never appears). The COMP_POOL_STATUS honesty lines follow the enrichment summary's example: a qualified judgment with reasons, not a yes by default.

Out of scope: any Cortex import, any render/build work, the ~15-row bracketing cleanup from the enrichment watch-lists (separate task), additional timeline IPs beyond these five.