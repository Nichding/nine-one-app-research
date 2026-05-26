# Nine One Data Moat Strategy

## Data moat thesis

Nine One's defensible data should come from **structured padel participation and improvement data**, not generic booking records.

Booking data alone is not enough. Competitors can collect reservation time, venue, court, and payment data. Nine One should compound a richer dataset:

**player reliability + skill confidence + match balance + venue context + coach validation + improvement intent.**

## Proprietary data assets

| Data asset | How it is captured | Why it matters |
| --- | --- | --- |
| Skill confidence | Self-rating, match outcomes, peer balance feedback, coach validation | Enables better matching and reduces rating disputes. |
| Reliability graph | Attendance, late cancellations, payment completion, no-shows, peer feedback | Makes joining open matches safer. |
| Match quality score | Post-match balance rating, result, level spread, repeat behavior | Improves recommendations and venue programming. |
| Player availability | Preferred days/times, joined matches, waitlists, abandoned joins | Predicts demand and fills courts faster. |
| Venue demand map | Time slots, level bands, fill rates, waitlists, off-peak gaps | Helps clubs optimize pricing and programming. |
| Improvement intent | Recap engagement, coach notes, selected weaknesses, clinic clicks | Connects coaching supply to player need. |
| Coach validation history | Coach-assessed level and improvement tags | Adds trusted human signal before AI is mature. |

## Data flywheel

| Step | Data generated | Product improvement |
| --- | --- | --- |
| Player joins match | Intent, price, level, time, venue | Better match recommendations. |
| Match completes | Attendance, result, context | Better reliability and skill confidence. |
| Players rate balance | Match quality signal | Better level bands and matchmaking. |
| Coach validates | Trusted level and weakness signal | Better recommendations and clinic targeting. |
| Venue reviews fill data | Demand by segment | Better open-play templates and off-peak activation. |
| Player books next action | Conversion data | Better next-best-action model. |

## Moat principles

| Principle | Implementation |
| --- | --- |
| Capture data as a byproduct of value | Do not ask for long surveys; use match join, attendance, result, and 30-second feedback. |
| Prefer structured fields over free text | Level, reliability, balance, weakness, and next action should be analyzable. |
| Combine human and behavioral signals | Coach validation plus attendance and outcomes is stronger than self-rating alone. |
| Make data useful immediately | Players see better matches; venues see better fill; coaches see better prospects. |
| Be transparent | Explain why level or reliability changed to avoid trust loss. |

## Initial scoring models

| Model | MVP approach | Future upgrade |
| --- | --- | --- |
| Skill confidence | Weighted blend of self-rating, coach validation, match outcomes, and peer balance feedback | Bayesian rating with uncertainty and partner/opponent adjustment. |
| Reliability score | Payment completion, attendance, cancellation timing, no-show history | Predictive no-show risk by time, venue, event type, and user behavior. |
| Match quality score | Level spread, player reliability, post-match balance rating, repeat intent | Recommendation model for ideal player combinations. |
| Venue opportunity score | Fill rate, waitlists, off-peak availability, repeat users | Dynamic program/pricing recommendations. |
| Improvement recommendation | Coach tag plus player-selected weakness | Video/AI-derived skill and tactical model. |

## Data advantage over competitors

| Competitor pattern | Their likely data advantage | Nine One's target advantage |
| --- | --- | --- |
| Booking platforms | Court inventory, reservations, payments, club utilization | Trust, match quality, level confidence, player intent, coach conversion |
| Fitness social networks | Activity history, segments, social graph | Padel-specific partner/opponent history and match context |
| Video platforms | Shot/video/performance data | Session data connected to booking, opponent level, coach action, and venue economics |
| Club management tools | Membership and operational data | Community liquidity and player progression data |

## Privacy and trust requirements

| Requirement | MVP policy |
| --- | --- |
| Player control | Let players control profile visibility and contactability. |
| Venue data ownership | Clarify export rights and how venue customer data is used. |
| Reliability fairness | Show events that affected score and allow dispute/support path. |
| Coach notes | Private by default unless player shares. |
| Data minimization | Collect only data tied to matching, reliability, improvement, or venue ROI. |

## Source links

- Playtomic booking/open match flow: https://playerhelp.playtomic.com/hc/en-gb/articles/19831715222929-How-to-book-a-court-or-a-spot-in-a-match-in-your-favourite-Club
- CourtReserve features and reporting: https://help.courtreserve.com/en/articles/11795322-courtreserve-features-at-a-glance
- Padel Mates level feedback/features: https://play.google.com/store/apps/details?id=com.padelmates
- SwingVision stats/coaching: https://swing.vision/home/
- Strava segments/progress: https://support.strava.com/hc/en-us/articles/216918167-What-are-Segments-
- Hudl video analysis products: https://www.hudl.com/products
