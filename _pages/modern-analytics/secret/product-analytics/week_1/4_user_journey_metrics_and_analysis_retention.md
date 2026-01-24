# User Journey Metrics and Analysis Techniques: Retention

## User Journey Metrics and Analysis Techniques: Retention


We are almost there! In the previous section we have mastered the early parts of the user journey: onboarding and activation. In this section we will dive into arguably one of the most important product analytics metrics — retention — and get familiar with an analysis technique that is a must-have for exploring retention: the cohort analysis.

Our user has successfully experienced the value proposition of our product and has agreed that the product solves their problem. Now we want this user to form a habit around our the product and engage with it repeatedly.

>ONCE IN A LIFETIME
>Note that there are products that don't assume repeat engagement, or repeat engagement may be happening on a long-term horizon only. A wedding registry product is a good example: People don't get repeatedly married all that often. A product facilitating home buying or home loans may experience repeat engagement once every several years. 

In this case you may want to pay more attention on acquisition and activation, as well as unit economics (Are we getting enough revenue from one-off engagement?), and ensuring that if repeat engagement happens down the line, then the existing users can recall your product.

## Retention as a Growth Lever
Interestingly, when the notion of 'product growth' is discussed, it is not uncommon to focus on acquiring and onboarding users, but retention is what really can make or break product growth long-term. 

Let's take a look at some scenarios!

### Scenario 1: Baseline

Our subscription product acquires 1,000 new subscribers per month. And we are subsequently losing 10% of subscribers of the previous month's count thereafter. In other words, if 1,000 users joined in January, then in February we will only have 900 remaining subscribers from this group (+ 1,000 new subscribers). In March, we will have 810 (900 - 90*0.1) from the January group, 900 from the February group, and 1,000 new subscribers, and so on. In this scenario, in December, we will have a total of 7,176 subscribers.



### Scenario 2: Acquisition Improvement

Let's assume that we got 100% better at acquiring new users, and now we have 1,100 new subscribers joining each month. With retention still at 90%, we will have a total of 7,893 users in December, and more than 800 incremental users!



### Scenario 3: Retention Improvement

Assume that we're back at the baseline of 1,000 new subscribers per month, but we got just a little better at retention. Instead of a 90% month-to-month retention rate, for each cohort we are now at 92% (2.2% relative improvement). In December we will have 7,903 users! That is more than in Scenario 2, although the relative improvement is comparatively more minor.



Retention compounds over time. Even on such a short-term scenario we were able to intuit that small retention improvements can compound over time. Imagine a longer horizon and a larger user base, with each user contributing $10+ of subscription revenue!

>YOUR TURN!
>You can find the scenarios above in this spreadsheet. Make a copy, and play around with the acquisition and retention numbers in the third scenario! 

If our month-to-month retention across cohorts is at 92%, how much can we compromise by in Month 0 acquisition to be at a breakeven with Scenario 1? Maybe we can spend a little less on acquisition marketing, and invest these extra funds in product development to find ways to increase retention?

## Defining Retention
Now that we've understood why retention is an important growth lever, let's try to define the metric we can use in our product analytics world.

From the scenarios above you likely already built an intuition that we were looking at % of users from those who were active subscribers the month before that are still subscribed to our product on a given month. And we were looking at it in a cohorted fashion, meaning that we broke our subscriber base into groups — cohorts — based on the month they started using the product, and we measured retention for each cohort separately. This is actually one of the most common product analytics approaches, and this is what we will stick with for the rest of the lesson and Week 1 project.

Note that this is not the only approach. Financial reporting would usually measure retention (or the inverse of it, churn) in a non-cohorted way by dividing the number of all active subscribers at the end of this month by the number of all active subscribers at the beginning of the month. For a transactional business where the repeat payments are not on a predictable cadence, you may want to measure average time since last purchase.

We are almost there, but we need to revisit two important considerations.

## Subscription Retention Is a Lagging Indicator

When we think about product metrics, we aim for them to be leading indicators of business outcomes. For example, when it comes to subscription apps, have you ever stopped using an app for a month, realized that you got charged your monthly payment, thought "I will probably use it next month", kept your subscription for another month or two, and then only canceled if you still weren't using it? 

Subscription retention — our business outcome — is unfortunately lagging. Once it goes down, we already missed a chance to reengage a customer. So for subscription products we often want to look at a different version of subscription metric based on the repeat occurrence of the product's main value exchange. 

In our workout app example, that could be... working out. So we would define Month 1 retention metric as: 'of users who joined the previous month, what % did at least one workout this month?'. For Netflix, it could be 'watching a movie'.

>CHAIN REACTION
>In one of their blog posts from their Data-Informed Product Building series, VC firm Sequoia Capital notes: "Engagement drives Stickiness drives Retention drives Growth." What a great way to remember this!

## What Is the Right Time Grain?

For subscription and non-subscription products alike, whether we look at retention metrics on a daily, weekly, monthly, or quarterly grain once again depends on our qualitative assumptions. How often should our value exchange happen in the optimal scenario? How often does the user encounter the problem we are solving? Your time grain should align with the natural frequency of using the product. Note that this consideration would apply to other metrics, too, such as engagement metrics, 'active users' metric, and so on.

For social networks or news websites/apps, this frequency may be daily. For any work-related applications, weekly work (because we try not to work on weekends! 😉). This could also be true for entertainment, workout/fitness apps, meal prep kits, grocery delivery. For a product like Credit Karma, it is likely monthly, coinciding with the frequency of credit score changes. And for a product like Turbo Tax, one or twice a year is sufficient for a tax filing and maybe for a tax projection.

KNOWLEDGE CHECK
What is the key value exchange and the natural frequency for a product you are working on or for your personal favorite product/app?

Visualizing Retention
One of the best ways to gauge how well the product is performing retention-wise is to draw the retention curve with time periods on the X axis and retention % (calculated as '% of users performing key value exchange in Month A of those who joined in Month 0') on the Y axis.

In our previous example with 90% month-to-month retention, the curve values will be 100% → 90% → 81% (90% * 0.9), and so on. And if we extend the curve all the way to the 2-3 year mark, it is going to be very close to 0. This is usually not the desired shape of the retention curve — it is another manifestation of a 'leaky bucket' problem.



A healthier retention curve looks something like below. In the first few time periods you are likely to lose some share of users with lower intent, or those for whom the occurrence of the problem your product solves happens less often than you hypothesized, so they aren't willing to pay for it. But after a few time periods you would want your retention curve to flatten or almost flatten — here you find your audience that retains long-term! 





FORCE OF HABIT
The point in time where this curve flattening happens is frequently referred to as the habit moment. It means that the users who 'survived' to that point are likely to stick around for good, because they formed a habit around the product usage.

We are almost at the end of this week's lesson! In the last section we will describe a technique frequently used in product analytics for retention diagnostics: cohort analysis.