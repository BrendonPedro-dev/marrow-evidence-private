cd "/mnt/c/Users/user.DESKTOP-7QU46KG/Desktop/Dev/PBC/WSL/Research/VC Pitch (0713)/licensing-research-output"
cat > tasks/BACKLOG.md << 'EOF'
# Queued research tasks (not yet built)
# Order below is the intended run order.

## 1. NEXT UP: Artist-side keyword re-sweep, four markets (TW/JP/KR/MY)
The Thailand run proved brand-side keywords structurally erase creators
(indie share 9.3% -> 20.5% purely by adding artist-side keywords:
ศิลปินไทย/นักวาด/ครีเอเตอร์). The four prior markets were swept brand-side
only, so their indie shares are likely UNDERSTATED and the cross-market
table is not comparable until re-swept. Per market, add the local
artist-side keyword class (TW: 繪師/插畫家/創作者; JP: イラストレーター/
クリエイター/絵師; KR: 일러스트레이터/작가/크리에이터; MY: EN + BM artist
terms) plus spelling variants (the TH คาแรกเตอร์/คาแรคเตอร์ lesson),
append new rows to the EXISTING tables under the EXISTING definition,
and add a post-re-sweep section to each _VERDICT (old share, new share,
what the keywords found). Do NOT rebuild tables from scratch.
GATE: the five-market consolidation and any published cross-market
comparison wait for this.

## 2. Five-market consolidation (GATED on the re-sweep)
Rebuild the comparison doc across TW/JP/KR/MY/TH - .md + .html, same
structure as the three-market version. Headline threads: does
~a-quarter-indie hold beyond East Asia; the TH closed-formats finding
(high-distribution formats 100% portfolio); the machinery hypothesis
(sticker/集點 economies vs MY's absence); the Butterbear concentration
caveat; format-mix divergence (TH licensed-goods/mall-led, not F&B-led).

## 3. Singapore census (market six)
Same identical definition. Key calls to write into the task when built:
English-dominant sources (for once), mall/loyalty-programme concentration,
the small-but-dense local creator scene, and the regional-HQ trap (SEA
campaigns announced from SG that never activated there - activation
evidence required, per the MY franchise-local rule). Runs with the full
keyword net (artist-side included) from birth.

## 4. MY census: dateless-indie backlog + expo conversion check
Tighten Malaysia's 12.6% toward its 16.7% ceiling: the TNG artist-card
line (5 dateless collabs: nothingwejun, DMEOW, HeyHey Brody, dao,
Home Too Much/Buku 555), SODA x Bichi Mao + x Yuurei Neko Sama apparel,
Walls x Yuurei Neko Sama, The Good Boisss x Lazada/Converse, Loklok &
Friends x Popular Bookstore + x Mitsui, Pee Yong Diary x McDonald's -
all real, excluded for want of dateable evidence. Plus: check which of
the 2026 Taiwan IP Expo's 12 TW-MY creator pairings (Sunway Pyramid,
2026-05-20, incl. Bichi Mao) converted to brand deals. (Partly absorbed
by item 1's MY leg - reconcile before running standalone.)

## 5. TH census: known holes follow-up
Brand Facebook pages (the largest known gap - likely suppresses indie),
LINE Creators Market rosters (the sticker-economy question is UNANSWERED,
not answered - trade press sees illustrators/art-toy, FB+LINE may see
stickers), the two unswept trade titles (Positioning Mag JS-search,
Marketing Oops 403), the Lotus's undercount, and the two known dateless
campaigns (AIS x Timo & Tintin, UNBOXING PRIDE s1).

## 6. Taiwan representable-sub-tag retrofit
Add the REPRESENTABLE column to Taiwan v2's indie rows so all markets
carry it; re-import under a new census_version when done. (Natural to
fold into item 1's TW leg - reconcile before running standalone.)

## 7. IP growth timelines - additional IPs
Bichi Mao timeline (pairs with the Wee interview data); more per Gary's
picks. Same spec as the Capoo/LAIMO/Monday Bruce/LuLu run: OBSERVABLE
public sequence only.
EOF
git add tasks/BACKLOG.md && git commit -m "backlog: reordered - artist-side re-sweep is next and gates the consolidation; SG queued as market six; TH holes + reconcile notes added"
git push