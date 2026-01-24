# From Business Metrics to Product Metrics
## From Business Metrics to Product Metrics
Common Revenue Models
Many Monetization Models ➡️ Similar Metrics Approach
When starting at a new company or on a new product, one of the first things to understand is: How does this product drive financial outcomes? Or how is it monetized? The nitty-gritty of monetization — such as pricing, discounts, and incentives — can be an entire course on its own, but understanding it really well on a higher level (Do users or customers pay per interaction? Do they a pay monthly fee? Are users and paying customers the same?) is crucial for defining product metrics that will set the foundation for the rest of your work as a product analyst.

## Common Revenue Models
When discussing business or financial outcomes, most companies focus either on profit (revenue minus cost) or on revenue. (In early-stage or growth companies, there can be less focus on profitability while the company is aggressively investing revenue into new product development or customer acquisition.) 

In our course, we will focus on revenue as something that is usually more directly attributable to product, while such functions as marketing and operations may focus more on costs/spend. Of course, your mileage may vary: For hardware products, the material/component and production costs can be a large focus for the product. On the other hand, in marketplace products that 'own' the supply side (like Uber and Lyft for ride sharing, or teletherapy offerings like Lyra and BetterHelp), cost and efficiency are also likely to be important focuses for the product team. 

There are several common revenue models that translate to specific sets of metrics that connect product and business outcomes:

Revenue/Monetization Model

Product Examples

Metric Questions

Important Metrics

Per transaction

E-commerce (e.g., Amazon); direct-to-consumer (e.g., Warby Parker, Everlane); marketplace (e.g., Uber, Etsy)

Can users find the product or service they are looking for? Do they purchase regularly? How much do they spend?

Conversion to purchase, average purchase revenue; for item categories with a regular/repeat re-purchase cycle: repeat purchase rate, lifetime value

Leading metrics for conversion (usually capturing supply/demand balance and product/service discovery)

Monthly/annual subscription

B2B or B2B2C SaaS (e.g., Superhuman, Deepnote); consumer subscription products (e.g., Netflix, Spotify, Peloton)

Are users compelled to pay for the service? Does the product give them enough value/solve their problem to use it regularly?

Conversion from free trial or freemium to paid subscription, pay-period-to-pay-period retention

Leading metrics for retention; for entertainment products like Netflix or Spotify: amount of content consumed; for efficiency products like Superhuman: tasks completed

Usage-based

B2B SaaS (e.g., Amplitude charging by # of events tracked, or Snowflake [warehouse compute, dbt] by # of models)

Does the product solve the customer problem well enough to be used regularly? Will it help the customer if used more extensively?

Adoption within the customer, pay-period-to-pay-period retention and usage increase rate

Leading metrics for retention and upsell: regularity of usage, completed tasks, breadth of the feature-set adopted

Ad-based

Media sites (e.g., CNN, BuzzFeed); search engines (e.g., Google); social networks (e.g., Twitter, Facebook)

Do we have a large enough audience to provide our customers the return on advertising investment they are looking for?

Audience size (e.g., Daily Active Users), ad engagement (click-through rates)

Leading metrics for audience size and click-through rates (repeat visits and depth of engagement); for social networks: content generation, sharing, and engagement

>IS THIS ONE OF YOUR... FRAMEWORKS?
>You may say, "Hey, so many products don't fit into these neat categories!" And you're right! Products like Amplitude combine usage-based pricing with a flat platform fee that acts more like a subscription fee. Many subscription-based consumer entertainment products — like YouTube, Spotify, and Hulu — also have a free tier with ads. 

>Remember, frameworks get us 80% there! For these products, we will probably have to consider a combination of metrics from different rows of this table, and will prioritize based on the company's strategic goals and revenue impact.

## Many Monetization Models ➡️ Similar Metrics Approach
While we have at least four distinct monetization models, there are two common themes among them:

In each case, revenue growth splits into two branches: 

New user/customer acquisition + conversion: At what rate does a new audience discover your product, do they see its value and its ability to solve their problem, and is the cost reasonable enough for them to start engaging?

Long-term repeat behavior or retention: Do the customers become regulars, would they use the product regularly enough, and can they do more with the product over time?

When we think about metrics, we can think about them in levels: From outputs (revenue) to inputs (conversion, retention) to second-level inputs (early engagement or onboarding-flow performance as an input to conversion, 'stickiness' as input to retention), or from lagging metrics to leading metrics. Next week, we will discuss metric levels/hierarchies in more depth, as well as how to land those second+ level input metrics. As we go further down the hierarchy, the more unique the metric set will be to your specific product.

In the next chapter, we will discuss the most common metrics to describe these facets of the user journey and the most common type of analysis related to these metrics.