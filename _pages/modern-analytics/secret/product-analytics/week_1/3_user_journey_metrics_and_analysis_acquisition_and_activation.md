# User Journey Metrics and Common Analytics Patterns: Acquisition & Activation

## User Journey Metrics and Common Analytics Patterns: Acquisition & Activation

Acquisition and Activation
Top of the Funnel: Product Discovery
Onboarding Rate
Activation, or the 'A-Ha' Moment
Measuring Activation
As we learned in the previous section, using revenue as part of the business-outcome metrics usually breaks down into two major inputs: new user/customer acquisition and retention. 

Each input on its own contributes to revenue growth. For example, for a subscription product, if we acquire and activate more users each month without improving retention, we will get more revenue at least from the first month of these incremental users' subscriptions. And if we keep the activation constant but improve retention, then maybe now we get one or two incremental monthly subscription payments for each existing customer. And this applies to most monetization models! 

>KNOWLEDGE CHECK!
>Think about how this breakdown applies to e-commerce, marketplace, and ad-based products. Can you explain the revenue growth split into product improvements around acquisition and activation vs. retention?

In this section, we will discuss the most common metrics used to describe the first branch of growth — acquisition and activation — as well as analytics approaches traditionally applied to understand your product's baseline in this area. In the next chapter, we will transition to retention.

USER? CUSTOMER?


You may have noticed so far that we have used the words 'users' and 'customers' somewhat interchangeably. However, as we're diving into the metrics, it is helpful to align on the definitions. Generally, the most common definitions of a 'person using a product' you will find are:

Visitor: Someone who views a webpage. This person may or may not be 'signed up' for your product, and may or may not have generated revenue in the past (e.g., made a purchase). Visitors may be anonymous, meaning you might not always be able to track their lifetime engagement with the website and product unless they create an account or make a transaction, sharing their contact or personal information along the way.

User: Someone who is registered with your product, and has an account and a unique identifier (e.g., username or an internal user_id) in your system. Usually a user = a person. But note that in products with both supply and demand side (e.g., ride sharing, creator platforms, marketplace) a user may refer to someone on either side (e.g., Instacart shoppers and delivery people are both Instacart users, and so is the Instacart buyer).

Customer: Someone who pays for your product. In B2C or e-commerce products, customers are usually users who have made purchases or are on paid subscription plans. But in B2B products, a customer may refer to the business/company, while their employees are users.

Depending on the industry and the product, there may be other denominations. At Peloton, we called our customers 'members'. In healthcare products, the users may be referred to as 'patients'.

For simplicity, we will use 'customer' and 'user' interchangeably in this course, unless specified otherwise.

## Acquisition and Activation
To evaluate how well your product brings in new users and sets them up for eventual repeat usage, you will need to understand three main concepts and their respective metrics. We'll cover them below. 

Top of the Funnel: Product Discovery
First things first: How many new users discover and explore your product each time period? In other words, how many new site visitors do you have, or how many new store visitors are there? This aspect is often largely driven by marketing campaigns and their ability to communicate product-value proposition and to target the right audience. But product can also contribute.

Is there a product-market fit, and does it come through in the marketing materials? 

Is there a viral, sharing/referral, or word-of-mouth component that can bring in new users without paid marketing? We will revisit this some more in Week 2!



One thing to keep in mind when measuring the number of prospective users discovering your product is that it can actually be very tricky to count them. 

For example, if the entry point to your product is on a webpage, then chances are lots of your new visitors will be anonymous initially. Web-tracking tools really just count unique web cookies, as laptops don't generate unique device identifiers like mobile devices do. And cookies can reset: If someone uses different browsers over time, then they will have multiple cookies associated with them. Some users might not get tracked at all, because they have an ad blocker. So you are likely getting some level of approximation for the count of those users who never set up an account.

>TAM, SAM, AND OTHER ABBREVIATIONS
>What is the upper bound for how many users your product can have in the future? There are research/survey methodologies to find that out! 

A market research team might ask a representative sample of people, "Would you be interested in engaging with this product?" The number of respondents extrapolated to the general population is your Total Addressable Market (TAM). 

Then they might ask, "Would you engage with this product given that it costs $XXX?" Those who say yes (also extrapolated) are your Serviceable Addressable Market (SAM). You can measure your % SAM penetration at any given point in time. And it can be important, given that at a low-penetration point you probably are dealing with very engaged early adopters, and once you cross the chasm into mass market, engagement patterns may look less favorable. 

Note that SAM/TAM studies should be repeated over time. Peloton's SAM in 2015 looked very different from that in 2020 in the midst of the pandemic! 🚴‍♀️

## Onboarding Rate
Now that we counted the top of funnel, we want to know: What % of these users complete actions that set them up for meaningfully engaging with the product? This can mean entering your email, creating your account, starting a free trial (if there is nothing meaningful to do without a subscription on the app), or performing more specific actions (e.g., for an analytics notebook SaaS product, that might mean uploading a CSV file or connecting to a database). 

This is usually referred to as the setup moment. Metrics-wise, the setup (or onboarding, enrollment) rate is straightforward to compute: 


setup rate = (# of users who completed onboarding) / (# of new users discovering the product)
But there are a couple of things to keep in mind:

It can be very compelling to look at an onboarding rate that is in the 40-50% range and suggest to a product manager that we should decrease friction in the onboarding flow as much as possible. This comes with a trade-off: It means that the users who proceed to the next stage of the funnel will include a higher share of low-intent users (i.e., those who were just curious and wouldn't have contended with a heavier process), which means that the retention might suffer and the overall impact will be net negative. 

>SUPER-FRICTION?
>There are examples of companies that have done really well with a very high-friction onboarding. Until recently, the email productivity app Superhuman would only 'let in' users who went through an in-person onboarding call, where new users get a guided tour of the functionality and receive a customized setup. 

That said, making friction too high or having it be an undesirable type of friction (a broken or confusing experience) is risky! It is not easy to convince someone who had a negative first impression of the product to ever try it again once it improves. 

Activation, or the 'A-Ha' Moment
Once your new user is set up for meaningful engagement with your product, now it is time for them to experience your product's main value proposition for the first time. When this happens, you can almost imagine a light bulb go off above the user's head, like in a cartoon: 💡Ooooh this is what this product does! This is awesome!💡

For a product like Peloton, this could be completing your first workout and feeling that fun and endorphin rush (maybe even better if someone high-fived you during it!). For the Superhuman email app, this could mean achieving your first 'Inbox Zero'. For Amazon Prime, this may mean getting your first next-day delivery. (And it is probably fair to say that it is not really a single moment, but a set of user actions that culminate in that 'a-ha' reaction.)

This is truly a pivotal moment in a user's journey. Unless the product is something that absolutely has to be used (for example, you may be forced to use a specific video-conferencing app for your work meetings if that's something your company mandates), this is the crucial stepping stone towards any future engagement.

## Measuring Activation
The most famous activation metric out there is probably Facebook's metric for the number (or percent) of users who added 7 friends in their first 10 days. The company's former executive Chamath Palihapitiya famously recounted how this metric was a singular focus for the company for a long time, and how consistently driving it up put the company on a path for multi-million growth.

It is indeed very common for an activation metric to be formulated as the % of users who do X in the product at least Y times in the first Z days. 

How did the magic metric come about at Facebook? They probably saw in the data that a high share of users who added 7 friends in the first 10 days retained in the product long-term, and also that a high share of users who added less than 7 friends in that period did NOT retain. Sounds simple, right? And indeed it can be!

Here is how you can land on your activation metric:

Define the desirable short-term outcome that you will mark as the 'success' for your activated users. Maybe it is using the product past the first 30 days, if that means that the 30-day free trialers convert to subscription or that monthly subscribers make at least one more payment. This outcome should not be too far in the future, as too many external factors can get in the way of the user behavior.

Brainstorm — for now — qualitatively, what could be some meaningful user actions that could lead to the user realizing the value of the product? (We mentioned workouts for Peloton.) Some nature of 'establishing connections or following' makes sense for social networks, since otherwise there won't be curated content to engage with. For productivity/efficiency products, it can be completing specific tasks. 

PERFECT IDEAS IMPERFECTLY MEASURED ➡️ PERFECT MEASURES FOR IMPERFECT IDEAS
Here and elsewhere in this course, we will really flex our ability to start generating hypotheses before looking at the data. It is extremely important in product analytics to root yourself in your product strategy and your understanding of the user problem and value exchange. 

It can be very appealing as a first step to throw 50 features into a regression model and see what sticks, but this approach can lead to meaningless results obtained by chance in the specific sample, multicollinearity, and other oddities than can really lead you astray!

Now that you have your set of hypotheses, you can look at the correlations! Let's use a workout app example (e.g., Peloton, Tonal, or any similar product). Let's say the outcome we want is a user doing at least one workout in their Month 2 with the product, and we think that workouts — or a combination of workouts — and social features engagement are what would qualitatively manifest activation. 



We can also look at the data to see the distribution of workout activity in Month 1 for each user. We may see that the first two weeks are where the most activity happens. Now we are ready to map out some permutations of workout quantities and social features engagement in the first two weeks for each new user, and look at their respective rate of success (Month 2 retention) for each permutation, like so:



Here you can see that there is a steep change in successful outcomes at the '4 workouts in 14 days' threshold. (Makes sense — a twice-a-week workout routine!) You can also note that there is only an incremental bump to the success rate from the 5th workout. And while gaining followers does increase propensity to retain, it seems that a very low share of users gains followers in the first 14 days, so including this additional qualifier may not be necessary.

This simple analysis can be a great way to get you started. Of course, if you are comfortable with more sophisticated statistical techniques like logistic regression or parametric and non-parametric testing, you may consider applying a more rigorous approach with the same general framework.

"But this is correlation, not causation," you say. And you would be correct! The users who worked out 4+ times are probably higher intent, or maybe they have a personal trainer who wrote them a two-workout-a-week program. But even the correlation approach here provides a great starting point. To ensure you aren't leading your team astray, consider the following points and actions:

Does your threshold make sense conceptually? It does in this case, as twice a week is a common exercise frequency for someone who is not a serious athlete. But if it feels completely arbitrary, try to revisit your qualitative hypotheses and see if there are other permutations/thresholds to explore.

It is a good reminder here to try and use the product you are working on in order to develop a better feel for possible usage patterns, and look into any archive of market research or user research findings. Take some time to read through it!

Can you run a test against your new metric? For example, if we can encourage a randomly selected part of our user base to participate in a two-workout-a-week challenge with an incentive/prize, can we get more users to reach this threshold, and do they indeed retain better than those in the part of the user population that didn't get offered this challenge? If so, our metric may be pretty good! (No worries if a concept of an experiment is unfamiliar — we will get there in Week 4!)

WATCH FOR MOVING TARGETS
Be mindful if you are experimenting aggressively against an activation metric, as it may become a moving target. For example, if we made all workout classes twice as short at Peloton, then we would probably increase the number of users doing four workouts. This is because to achieve the same workout time, you now need to do four workouts instead of two. However, this might not meaningfully boost Month 2 retention, and you might have to switch your metric to '8 workouts in 14 days'. 

Similarly, if Facebook just automatically added seven random accounts in your Following list, it wouldn't have meaningfully improved your experience, but it could have changed the target metric!

If you are a skilled statistician and there is not a way to run a test, you may want to try a causal inference approach to see if you can find ways to eliminate omitted variable bias. Check out the optional Further Reading section if you want to learn more about causal inference!