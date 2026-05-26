# V1 Feature Stack

## Feature stack principle

V1 features should exist only if they strengthen the new sports behavior model:

**Find the right match -> commit -> show up -> reflect -> improve -> return.**

Everything else should wait.

## V1 layers

| Layer | Feature | Purpose |
| --- | --- | --- |
| Identity | Player profile | Makes players recognizable and accountable. |
| Identity | Home venue | Anchors belonging and local network effects. |
| Identity | Level confidence | Helps players find matches that fit. |
| Identity | Reliability score | Makes open matches safer to join. |
| Liquidity | Recommended open matches | Core entry point for play. |
| Liquidity | Match creation by venue/host | Creates structured supply. |
| Liquidity | Waitlist/substitute flow | Converts failed demand into future liquidity. |
| Commitment | Payment confirmation | Makes slots real. |
| Commitment | Cancellation rules | Protects fairness and trust. |
| Commitment | Reminders | Helps people show up. |
| Coordination | Match thread | Supports necessary coordination only. |
| Reflection | Result entry | Adds match memory. |
| Reflection | Balance rating | Measures quality. |
| Reflection | Peer reliability signal | Protects trust. |
| Reflection | Improvement tag | Feeds coaching and AI path. |
| Return | Post-match recap | Turns match into learning. |
| Return | Next action | Drives rebooking, clinic, coach, or validation. |
| Coach | Coach validation | Adds trusted skill signal. |
| Coach | Coach improvement note | Humanizes progression. |
| Venue | Open-play templates | Lets venues create repeatable community rhythm. |
| Venue | Fill-rate dashboard | Shows venue ROI. |
| Venue | Demand and waitlist view | Helps venues know what to run next. |

## V1 feature hierarchy

| Priority | Feature group | Why |
| --- | --- | --- |
| P0 | Open match recommendation and joining | Without this, there is no core behavior. |
| P0 | Player identity, level, reliability | Without trust, open matches do not scale. |
| P0 | Payment/commitment/cancellation | Without commitment, matches fail emotionally. |
| P0 | Post-match feedback and recap | Without reflection, there is no memory or improvement loop. |
| P1 | Coach validation and improvement tags | Creates differentiation and better data. |
| P1 | Venue templates and demand dashboard | Creates venue value and repeat supply. |
| P2 | Basic squad/repeat group support | Creates stronger retention once match volume exists. |

## Data captured by feature

| Feature | Data captured |
| --- | --- |
| Player profile | Name, photo, home venue, level, availability, preferences |
| Open match browsing | Match views, saves, abandoned joins, preferred times |
| Join/payment | Commitment, price tolerance, payment status |
| Cancellation | Timing, reason, substitute need |
| Attendance | Verified show/no-show |
| Match result | Score/result and player combination |
| Balance rating | Match quality by level, venue, time, players |
| Reliability feedback | Trust signals and social risk |
| Improvement tag | Player learning need |
| Recap action | Rebook, clinic click, coach request, ignored recommendation |
| Venue template | Supply design by time, level, price, format |

## V1 exclusions

| Excluded | Reason |
| --- | --- |
| Full court marketplace | Commodity, inventory-heavy, and not the behavior wedge. |
| Feed of posts/photos | Does not help first trusted match. |
| Advanced gamification | Can cheapen the emotional tone before trust exists. |
| Full video AI | Requires capture quality and labeled data first. |
| Complex tournament ladders | Too much structure before reliable weekly play is proven. |
| Multi-sport architecture in UI | Dilutes padel specificity. |
| Pro-shop/POS/accounting | Club software commodity. |
| Public global rankings | Encourages ego and mismatches before level confidence is mature. |
| Automated rating black box | Creates distrust. |

## V1 operating features

Some V1 "features" should be internal and manual.

| Internal feature | Why it matters |
| --- | --- |
| Manual venue setup | Faster than building full self-serve tooling. |
| Manual match seeding | Creates early liquidity. |
| Manual coach recruitment | Coaches anchor trust. |
| Manual data review | Prevents early scoring mistakes. |
| Human support | Protects the fragile trust layer. |

## Feature acceptance test

Before building a feature, ask:

| Test | Requirement |
| --- | --- |
| Match quality | Does it help create better matches? |
| Trust | Does it make commitment safer? |
| Return | Does it help the player come back? |
| Data | Does it create useful structured memory? |
| Venue | Does it help the club host a better community? |
| Coach | Does it help human guidance become more effective? |

## Sources

- Playtomic open matches: https://playerhelp.playtomic.com/hc/en-gb/articles/19831715222929-How-to-book-a-court-or-a-spot-in-a-match-in-your-favourite-Club
- CourtReserve features: https://help.courtreserve.com/en/articles/11795322-courtreserve-features-at-a-glance
- Padel Mates features: https://play.google.com/store/apps/details?id=com.padelmates
- SwingVision: https://swing.vision/home/
- Hudl products: https://www.hudl.com/products
