---
name: business-diagnosis
description: Use when a business has thin profit despite revenue, the owner wants to cut ad spend, leads seem low quality, close rate is low, customers churn, a product needs a price, prices are capped, some months lose money, revenue has plateaued at some number, the founder is the bottleneck, or the owner is hiring or scaling a sales team or other people-based business.
---

# Business Diagnosis

## Overview

Find the one number with the most room to move, quantify what moving it is worth, and fix only that. CAC can only fall to zero, but LTV has no ceiling, so look at price, upgrades and retention before ad cost.

Terms (CAC, LTV, AOV, ROAS, ascension, BNPL) are defined in [glossary.md](glossary.md).

Siblings: designing the offer itself is `offer-crafting`. Building the funnel is `lead-gen-funnels`. Discounts, pricing tiers and negotiation are `closing-deals`. This skill decides which number to work on.

## Diagnosis procedure

1. **Get the numbers.** Front-end price and AOV, CAC, every upsell price and its take rate, any monthly product with its join rate and monthly churn, gross margin, and what changed recently (traffic source, price, team).
2. **Compute LTV and LTV:CAC.** Use gross profit if you have margin. 3 to 1 is the usual healthy target. Also check payback: Money Models wants each customer to cover their CAC within 30 days.
3. **Find the lever with the most room to move.** For each number, write its floor or ceiling, then dollars per customer if it moved to a realistic target from the calls. Always include price. A number with a floor (CAC) usually loses to one without (price, upgrade rate, retention).
4. **Check the change beats the 20% dip.** Any change to a script, page or process drops performance about 20% at first. Only make it if the expected gain is clearly bigger. 30 to 50% is worth the bet. 5% is not.
5. **Pick ONE.** Name the single number, its target, and the dollars per customer. Not a ranked list of five. A focused fool beats a distracted genius.

## Formulas

All per customer unless noted.

- `upgrade value = upgrade rate x upgrade price`
- `continuity value = join rate x (monthly price / monthly churn)`
- `LTV = front-end price + every upgrade value + continuity value` (subtract delivery cost to get lifetime gross profit, which is what the playbooks mean by LTV)
- `LTV to CAC = LTV / CAC`
- `gain from a lever = (target rate minus current rate) x price`
- `profit per customer = yearly revenue per customer x margin`
- `new clients = confirms x show rate x book rate x close rate`
- `worth changing = expected gain > 20%`

Worked example from the $30M call: front end $2,000 (AOV about $900 from payment plans), CAC $1,500, $10K back end at 7%, LTV about $2,400, so 1.6 to 1. On CAC Hormozi said "You're not going to get below a thousand", so cutting it saves at most about $500. Moving the upgrade rate from 7% to 25% adds `0.18 x $10,000 = $1,800`. That is roughly 6 times the gain, so the back end is the one fix.

Price check from the playbooks call: 10 customers at $100 is $1,000. Doubling customers to 20 doubles delivery work. Doubling price to $200 gets the same $2,000 from the same 10 customers.

## Quick reference

| Symptom | Check first | Rule from the calls | Source note |
|---|---|---|---|
| Big revenue, thin profit | Back-end upgrade rate | Upgrade target at least 25%, aim for 50%. Build it into onboarding: the onboarding call ends only when the buyer books a "goal setting" call | I Do $30M a Year |
| Owner wants to cut ad spend, cash is tight | ROAS and payback, then LTV | Spending less usually raises ROAS. A cash problem is "self-inflicted". Mature-market CAC has a floor | I Do $30M a Year |
| "Paid leads are bad" | Sales steps and price between click and sale | PPC is second best after referrals. Cost per lead may rise 2 to 3x, but doubling price could raise gross margin about 5x | My Paid Leads Are Low Quality |
| Low close rate, buyers agree but cannot pay | Qualifying questions | Ask facts (owns a business, revenue), not "willing to invest?". Expect cost per call up, CAC down, LTV up | Should I Add Qualifiers |
| High churn | The activation point | Call 20 who stayed and 20 who left. Ask stayers for the "this is great" moment. Point all onboarding at one action. Skool: 3 members means about 11x LTV | My Newsletter Loses 11% |
| Churn rose recently | What changed in traffic | Churn rose when the newsletter moved from a warm audience to paid ads. Monthly stayers show the real reason | My Newsletter Loses 11% |
| Pricing a new product | Where the value is | Drop throwaway fees. One-time onboarding fee plus per-seat price. Sell savings and an easy switch. Have 10 real conversations first | My Niche Software Has Zero Revenue |
| Price is capped | Margin | 15% to 30% margin doubles profit on a $50K customer from $7,500 to $15,000. Use a paid waitlist | Government Caps My Prices |
| Some months lose money | Sales motion, then price, in the losing season | If workers are scarce, not customers, raise price 20 to 30% | My Landscaping Loses Money |
| Plateau with one offer | A second, bigger sale | 20% of $3K buyers taking a $30K year makes the average buyer worth $9K | I Do $400K a Year Coaching |
| Growth depends on reps | Cost of acquiring talent vs lifetime gross profit per rep | Reps drop at week 1 or 2, day 30, day 90. Onboard 25 a week, not 5 | I Have 80 Reps |
| Founder is the only seller | Recruiting and training skill | Expect a 20 to 30% dip while learning to hire. Offer your too-small deals 50/50 as bait | I'm a Solo Broker |
| Fixes undo when founder leaves | Who reinforces the standard | Define, demonstrate, watch, feedback, repeat until peers praise each other | Everything I Fix Unravels |
| Founder hates calls, wants to go low ticket to scale | Delivery format, not price | Drop the one-on-ones and keep the price with group calls. One coach to six or seven people is about 6x capacity, but buys only about a year. A year of one-on-ones shows the five main problems to productize | My Founder Hates Calls |
| Referrals running out, clicks but no sales | A concrete offer | A mission is not an offer. 100 confirms, about 25 show, about 12 book, about 6 close | We're Running Out of Referrals |

Billing cadence also moves churn. Money Models cites Profitwell data: monthly plans churn 10.7% a month, quarterly 5%, annual 2%.

## Common mistakes

1. **Giving a ranked list instead of one number.** Name one number, its target and its dollars per customer. Others are "not now".
2. **Never testing price.** Always model a price raise. CAC can only fall to zero. LTV has no ceiling. The landscaping call used 20 to 30%. The leads call suggested about 2x for the best customers.
3. **Timid upgrade targets.** Moving an upsell from 5% to 7% is not the case in the calls. The $30M call moves 7% to at least 25%, and the coaching call expects 20 to 30%. Model the target the calls use, then say how to get there (built-in onboarding call, quick win, booked next call).
4. **A grab bag of churn tactics.** Find the one early action loyal customers took and make every new customer take it. Then test which candidate moves churn.
5. **Ignoring the change cost.** Every change drops results about 20% first, and changes to how people work hurt most. Show the expected gain beats that dip.
6. **Blaming leads or ads first.** Check qualifiers, sales steps and price before cutting spend or changing channels.
7. **Cutting price to fix delivery.** If the limit is how you deliver, change the delivery first. Going low ticket throws away the price point to solve a calls problem.

## Source notes

From the author's video study notes (Lessons):

- I Do $30M a Year. Why Does It Feel Unprofitable?
- Is This Change Worth the 20% Drop?
- My Newsletter Loses 11% of Subscribers a Month. How Do I Fix Onboarding?
- Government Caps My Prices. How Do I Grow Margin?
- My Landscaping Loses Money Until It Snows. What Do I Fix?
- My Niche Software Has Zero Revenue. How Should I Price It?
- My Paid Leads Are Low Quality. What Do I Do?
- Should I Add Qualifiers If My Close Rate Is Low?
- I Do $400K a Year Coaching. How Do I Get to $2M?
- I Have 80 Reps. How Do I Get to 200?
- I'm a Solo Broker Doing $2M. How Do I Get to $8M?
- Everything I Fix Unravels When I Leave. Why?
- We're Running Out of Referrals. Where Do Our Next Clients Come From?
- What Do All 12 of Hormozi's $100M Playbooks Actually Teach?
- A Focused Fool Beats a Distracted Genius (pick one constraint)
- keywords (glossary)

From the author's video study notes (Sales):

- My Founder Hates Calls. Should We Go Low Ticket?

Supporting math: `Books/Offers and Leads/$100M Money Models - Alex Hormozi.md`.
