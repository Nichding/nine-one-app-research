# Nine One MVP Recommendation

## MVP thesis

Nine One should not launch as a generic booking app. The strongest wedge is:

**A padel-native venue and player platform that combines court booking, trusted match formation, and smart coaching feedback from real sessions.**

The core product should make players better and make clubs fuller. Booking is the transaction layer; coaching, match quality, and community are the retention layer.

## Recommended MVP scope

| Priority | Feature | User | Why it matters |
| --- | --- | --- | --- |
| P0 | Court booking and payment | Player, club | Required table-stakes workflow against Playtomic, MATCHi, CourtReserve, and Padel Mates. |
| P0 | Open match creation and joining | Player | Padel depends on finding four compatible players. |
| P0 | Player profile with skill level and reliability | Player, club | Solves trust, balanced matches, no-shows, and match acceptance. |
| P0 | Club dashboard | Club | Lets venues manage courts, bookings, payments, open matches, and basic utilization. |
| P0 | Match chat and structured invites | Player | Reduces WhatsApp dependency while keeping coordination simple. |
| P0 | Payment state controls | Player, club | Prevents unpaid users from blocking match slots; include holds, expiry, and owner controls. |
| P1 | Post-match recap | Player | Creates Strava-like retention loop: result, attendance, level confidence, and next recommendation. |
| P1 | Coach-assisted level validation | Player, coach | Differentiates from opaque/rage-inducing rating systems. |
| P1 | Smart coaching clips or notes | Player, coach | Start lightweight: manual/coach tags first, AI later if needed. |
| P1 | Club programs | Club, coach | Clinics, intro sessions, ladders, social nights, and recurring open play. |
| P2 | AI video analysis | Player, coach, club | Strong differentiator, but only after capture quality and session data are reliable. |
| P2 | Loyalty/membership automation | Club | Convert repeat players into memberships and lessons. |

## What to exclude from MVP

| Exclude | Reason |
| --- | --- |
| Full Hudl-style video analysis suite | Too complex before booking/session loops are validated. |
| Enterprise POS/pro-shop system | CourtReserve already owns deep club ops; not needed for first wedge. |
| Broad multi-sport support | Start padel-native; add tennis/pickleball only after workflows are solid. |
| Generic Strava-like feed | Social should begin with match recaps, club groups, and achievements, not an empty feed. |
| Fully automated skill algorithm | Risk of trust issues; begin with self-rating, match outcomes, reliability, and coach validation. |

## MVP user journeys

| Journey | Flow |
| --- | --- |
| New player books | Choose venue -> select court/open match -> see price/rules -> pay -> receive reminders -> play -> get recap. |
| Player finds match | Set availability and level -> browse compatible matches -> join/pay -> chat -> confirm attendance -> post-match feedback. |
| Club creates open play | Select template -> set courts/time/level/capacity/price -> publish -> monitor fill rate -> approve substitutions -> view utilization. |
| Coach validates level | Player books assessment/session -> coach records rating and notes -> Nine One updates level confidence -> recommends next matches/drills. |
| Player improves | Match recap -> top weakness -> suggested drill/clinic/coach -> book next action. |

## Key product principles

| Principle | Implementation |
| --- | --- |
| Trust beats growth hacks | Verified profiles, attendance reliability, transparent payment status, and clear cancellation rules. |
| Explain levels | Show why level changed: match result, opponent level, coach input, confidence, and recency. |
| Reduce coordination load | Availability, squads, substitutes, reminders, and payment expiry should replace messy chat threads. |
| Make clubs smarter | Show fill rate, revenue, cancellation/no-show, repeat players, lesson conversion, and underused slots. |
| Add AI only where it creates action | AI should recommend drills, coach sessions, or match levels, not just produce stats. |

## MVP success metrics

| Metric | Target signal |
| --- | --- |
| Booking conversion | Visitors who complete first booking. |
| Open match fill rate | Percentage of open matches filled before start time. |
| Repeat play | Players booking again within 14 and 30 days. |
| Match quality | Post-match rating of balance, reliability, and enjoyment. |
| No-show / late cancellation rate | Should decline as reliability scoring and reminders improve. |
| Coach conversion | Percentage of players booking a clinic/lesson after recap. |
| Club utilization | Off-peak and total court utilization improvement. |

## Source links

- Playtomic booking and open matches: https://playerhelp.playtomic.com/hc/en-gb/articles/19831715222929-How-to-book-a-court-or-a-spot-in-a-match-in-your-favourite-Club
- Playtomic pricing/features: https://playtomic.com/pricing
- MATCHi app flow: https://play.google.com/store/apps/details?hl=en-US&id=com.matchi
- CourtReserve features: https://help.courtreserve.com/en/articles/11795322-courtreserve-features-at-a-glance
- CourtReserve pricing: https://courtreserve.com/pricing/
- Padel Mates app features: https://play.google.com/store/apps/details?id=com.padelmates
- SwingVision AI coaching/video: https://swing.vision/home/
- Strava subscription and progress loops: https://support.strava.com/hc/en-us/articles/216917657-Strava-Subscription-Features
- Hudl video analysis/product ecosystem: https://www.hudl.com/products
