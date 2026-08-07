# TW x lt_10k independent collaborations

## Goal
Find documented brand collaborations in Taiwan where the partner IP was an
independent character with under 10,000 followers at the time of the campaign.
The census currently holds zero such rows. Every teaser now renders a Taiwan
block first, so this cell is load-bearing on every prospect page.

## Scope
- Market: Taiwan only.
- Years: 2023-2026.
- IP class: INDEPENDENT or MIXED. Exclude licensed-property campaigns
  (Sanrio, Disney, POP MART, Minecraft and similar) entirely.
- Scale: partner IP at or under 10k followers at campaign time. Where the
  follower count at campaign time is not findable, record the current count
  and say so.

## Where to look
Small-format campaigns rarely get press. Prioritise: brand and creator
Instagram/Facebook/Threads posts, LINE sticker shop collaboration entries,
department store and mall event pages (新光三越, 遠百, 誠品, 華山, 駁二),
convenience store and drinks-chain campaign pages, pop-up and market listings,
募資 platforms, and 文博會 / 創意市集 exhibitor materials.

## Required fields per row
brand_name, ip_name, market (TW), year, source_ref (direct URL),
follower_band, representable (yes/no/unclear), ip_class, notes.

## Verification
Every row needs a source URL that resolves. Curl-verify each one and record
the status. A row without a working source does not go in the output.

## Output
Structured rows in the run-branch output file, proposed for human accept.
Do not write to any database. Do not claim a follower count you did not see -
state what was found and where.

## Stop condition
Stop at 25 verified rows or when the sources are exhausted, whichever comes
first. Report how many candidates were rejected and why.