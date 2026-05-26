# Nine One Version 1 Scope

## Version 1 objective

Build the smallest product that proves:

1. Players will use Nine One to join better padel matches.
2. Venues will use Nine One to fill courts and run open-play programs.
3. Match data can improve recommendations over time.
4. Post-match feedback can create a coaching and retention loop.

## V1 product scope

| Area | Build | Notes |
| --- | --- | --- |
| Player onboarding | Phone/email login, profile, photo, home venue, availability, self-rated level, preferred side | Keep onboarding under 2 minutes. |
| Venue setup | Venue profile, courts, time slots, prices, cancellation rules, open-match templates | Manual admin support is acceptable for V1. |
| Open matches | Create/join match, level range, slot state, payments, waitlist, cancellation, reminders | Core product surface. |
| Payments | Player payment confirmation, slot expiry, refund/cancellation state | Use a third-party payment provider; avoid custom payment complexity. |
| Match chat | Lightweight match thread with system messages | Enough to coordinate; avoid building a full messenger. |
| Reliability | Attendance confirmation, no-show flag, cancellation timing, payment status | Visible enough to influence trust. |
| Skill confidence | Self-rating plus post-match feedback plus optional coach validation | Avoid fully automated hidden algorithm. |
| Post-match recap | Result, balance rating, player feedback, level confidence, reliability impact, next action | The core retention loop. |
| Coach validation | Coach can validate level and tag one improvement area | Manual but high-signal. |
| Venue dashboard | Open-match fill rate, completed matches, no-shows, repeat players, off-peak utilization | Focus on actionable venue ROI. |

## V1 excludes

| Excluded feature | Reason |
| --- | --- |
| Full private court booking marketplace | Commodity and inventory-heavy; include only where required by partner venues. |
| Native branded venue apps | Too much overhead for V1. |
| POS/pro-shop/accounting | Not core differentiation. |
| Full tournament/league engine | Can be simulated with open-match templates and manual operations. |
| Full AI video analysis | Data foundation comes first. |
| Generic social feed | Network effect should center on matches and squads. |
| Broad multi-sport support | Padel-specific depth matters more than sport breadth. |
| Dynamic pricing engine | Start with venue-defined pricing and manual off-peak offers. |

## Suggested build sequence

| Sprint | Build focus | Outcome |
| --- | --- | --- |
| 1 | Player profile, venue profile, court/time-slot model | Basic supply and identity foundation. |
| 2 | Open match creation/joining, level range, slot states | First liquidity workflow. |
| 3 | Payment confirmation, cancellation rules, reminders | Reliable match commitment. |
| 4 | Match chat, waitlist, substitute flow | Coordination without WhatsApp dependency. |
| 5 | Attendance, result, balance feedback, reliability score | First data flywheel. |
| 6 | Post-match recap and next-match recommendation | Retention loop. |
| 7 | Coach validation and improvement tags | Differentiated trust/coaching layer. |
| 8 | Venue dashboard and open-play templates | Venue ROI proof. |

## V1 operating model

| Function | Startup-friendly approach |
| --- | --- |
| Venue onboarding | White-glove setup for first partners. |
| Customer support | Direct human support for first venues and high-value player issues. |
| Match seeding | Manually schedule recurring open-play events by level. |
| Coach supply | Recruit 3-10 trusted coaches per launch region. |
| Data QA | Review early match-quality and reliability scores manually before automation. |
| Growth | Venue communities, coach-hosted sessions, existing WhatsApp groups, referral squads. |

## V1 success thresholds

| Metric | Good early signal |
| --- | --- |
| Open match fill rate | Majority of published open matches fill before start time. |
| Repeat player rate | Players return within 30 days after first completed match. |
| Match quality rating | Players consistently rate matches as balanced/enjoyable. |
| No-show rate | Lower than partner venues' previous informal open-play process; exact baseline may be Unknown at launch. |
| Venue ROI | Partner venues report increased off-peak utilization or reduced coordination burden. |
| Coach conversion | Recaps lead to measurable clinic or lesson bookings. |

## V1 product principles

| Principle | Product decision |
| --- | --- |
| Fewer workflows, higher trust | Prioritize open matches over broad booking surfaces. |
| Manual before automated | Use manual coach validation and venue operations before AI automation. |
| Data before AI | Build structured match and coaching data first. |
| Local density before scale | One strong launch cluster beats broad availability. |
| Explain every score | Reliability and level changes must be understandable. |

## Source links

- Playtomic booking/open match help: https://playerhelp.playtomic.com/hc/en-gb/articles/19831715222929-How-to-book-a-court-or-a-spot-in-a-match-in-your-favourite-Club
- MATCHi Google Play listing: https://play.google.com/store/apps/details?hl=en-US&id=com.matchi
- CourtReserve features: https://help.courtreserve.com/en/articles/11795322-courtreserve-features-at-a-glance
- CourtReserve pricing: https://courtreserve.com/pricing/
- Padel Mates Google Play listing: https://play.google.com/store/apps/details?id=com.padelmates
- SwingVision: https://swing.vision/home/
- Strava subscription/features: https://support.strava.com/hc/en-us/articles/216917657-Strava-Subscription-Features
- Hudl products: https://www.hudl.com/products
