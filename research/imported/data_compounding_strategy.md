# Nine One Data Compounding Strategy

## Data compounding thesis

Nine One's data moat should come from **repeated, structured, real-world padel interactions**.

The valuable data is not just "a booking happened." The valuable data is:

**who played, whether they showed up, how balanced the match felt, how skill confidence changed, what the player wanted next, and which recommendation caused another real-world action.**

## Data assets that compound

| Data asset | Initial value | Compounding value |
| --- | --- | --- |
| Player skill confidence | Helps place new players into reasonable matches | Becomes more accurate with outcomes, feedback, and coach validation. |
| Reliability score | Reduces no-show risk | Becomes a trusted participation credential. |
| Partner/opponent graph | Shows who has played together | Reveals compatible groups, rivalry, repeat behavior, and squad formation. |
| Match quality score | Measures whether a match was balanced | Improves match construction and level-band design. |
| Venue demand map | Shows when players want to play | Helps venues create profitable open-play, clinic, and off-peak programming. |
| Improvement intent | Shows what players want to improve | Helps coaches and AI recommend useful next actions. |
| Recommendation conversion | Shows what players actually do next | Improves retention, coaching, and monetization. |

## Data loop mechanics

| Loop stage | Signal captured | System learns |
| --- | --- | --- |
| Discovery | Search, availability, abandoned joins, waitlists | Where demand exists even without a booking. |
| Commitment | Join, payment, cancellation, substitute usage | Who is reliable and what conditions drive conversion. |
| Completion | Attendance, result, match context | Which combinations of players produce completed matches. |
| Reflection | Balance rating, peer feedback, improvement tag | Whether the match was worth repeating. |
| Recommendation | Suggested match, clinic, coach, or drill | What next action is most likely to create retention. |
| Follow-through | Rebooking, clinic attendance, coach session | Which recommendations create real behavior. |

## AI training path

| Phase | Model/data focus | Why this sequence matters |
| --- | --- | --- |
| Phase 1 | Rules and transparent scoring | Small datasets require understandable logic. |
| Phase 2 | Skill confidence and reliability prediction | These directly improve match quality and trust. |
| Phase 3 | Next-best-action recommendation | Converts match data into retention and revenue. |
| Phase 4 | Coach-assisted labels | Human expertise improves quality before full AI automation. |
| Phase 5 | Padel-specific video/tactical AI | Only after enough labeled events and capture quality exist. |

## Why data gets stronger over time

| Mechanism | Explanation |
| --- | --- |
| Repeated observations | One match is noisy; repeated matches reveal stable behavior. |
| Cross-validation | Self-rating, peer feedback, outcomes, and coach validation correct each other. |
| Context awareness | Skill and reliability can vary by venue, partner, time, and match type. |
| Recommendation feedback | The system learns not only what it predicted, but whether users acted. |
| Local density | More matches in the same market create better calibration than scattered global data. |

## Data-to-product translation

| Data signal | Product behavior |
| --- | --- |
| High waitlist for intermediate evening matches | Recommend venue add recurring intermediate open play. |
| Strong player reliability and balanced-match feedback | Prioritize player in open-match recommendations. |
| Frequent match imbalance at a level band | Adjust level range or require coach validation. |
| Player repeatedly selects "weak at net" | Recommend relevant clinic, coach, or drill. |
| Off-peak slots fill with specific cohorts | Suggest targeted venue programs for those cohorts. |
| Player joins after seeing familiar reliable players | Prioritize squad and trusted-player recommendations. |

## Defensible dataset

| Dataset | Why it is defensible |
| --- | --- |
| Attendance reliability | Requires verified match participation over time. |
| Skill confidence | Requires player outcomes, feedback, and coach labels. |
| Match balance | Requires completed matches and subjective feedback. |
| Coaching conversion | Requires linking improvement intent to paid or attended coach activity. |
| Local demand elasticity | Requires venue-level supply, pricing, fill, and waitlist history. |

## Governance requirements

| Requirement | Reason |
| --- | --- |
| Explain score changes | Prevents rating distrust and user churn. |
| Separate confidence from level | A player can have a level estimate with low confidence. |
| Allow correction/dispute | Reliability and level scores affect access to matches. |
| Keep coach notes private by default | Coaching data is sensitive. |
| Give venues useful but privacy-safe analytics | Venue ROI should not require exposing unnecessary personal data. |

## Source links

- Playtomic open matches: https://playerhelp.playtomic.com/hc/en-gb/articles/19831715222929-How-to-book-a-court-or-a-spot-in-a-match-in-your-favourite-Club
- Padel Mates features and level feedback: https://play.google.com/store/apps/details?id=com.padelmates
- CourtReserve features/reporting: https://help.courtreserve.com/en/articles/11795322-courtreserve-features-at-a-glance
- SwingVision AI stats/coaching: https://swing.vision/home/
- Strava progress/segments: https://support.strava.com/hc/en-us/articles/216918167-What-are-Segments-
- Hudl products: https://www.hudl.com/products
