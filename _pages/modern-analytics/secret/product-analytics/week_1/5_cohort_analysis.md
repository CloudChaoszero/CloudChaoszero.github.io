Cohort Analysis
Cohort Analysis
From Engagement to Retention
Retention Diagnostics
Just like we did in our illustrative example in the previous section, retention is usually analyzed in a cohorted fashion. The reality is that the products don't usually acquire new users at a steady clip, and different time periods may bring you different type of audience, hence aggregating retention over time may hide important trends.

Let's walk through an example of calculating cohorted retention from engagement data and discovering important trends. 

From Engagement to Retention
On the left, we see a table with a distinct row for each monthly acquisition cohort (# new users). The following columns show us the # of users from that cohort that performed the value exchange (e.g., performing a workout on a workout app) in each month following their acquisition (portrayed as "M1" for the first month following their acquisition, and so forth). On the right, we transformed these totals into percentages by dividing each monthly cell by the cohort size in the same row.



You can already pick up on some interesting aspects here. Firstly, it seems that the majority of the user loss happens in months 1-3, and then our 'curve' flattens. Also, we can see that the cohort sizes are uneven: The January cohort is really big (New Year's Resolutions, am I right?), and so is the May cohort. Maybe we ran a big ad campaign in May and lots of new users discovered us?

Retention Diagnostics
To facilitate additional discovery, let's subtract the average retention across a cohort from the individual cohort's value in the corresponding map, and then use some conditional formatting to create a heatmap.



Huh, interesting! Looks like our January cohort ended up performing much better than the rest. The determined New Year's Resolutions folks had a great experience early on, and stuck with it! 

On the other hand, our May cohort acquired via an ad campaign is performing the worst. Looks like we might have targeted this campaign in a way that attracted lots of users that were low intent, or perhaps were not the right target audience. Perhaps we can look into this audience some more to learn from this campaign and make changes to our targeting.

If you look at it some more, you will notice another interesting thing: 



There is a clear diagonal line that shows a dip in retention compared to average. This is how seasonality manifests in cohort analysis! The diagonal line originates in M1 for the June cohort, which is July. For the May cohort, July is Month 2, and for April cohort, it's Month 3 — hence, the diagonal pattern. 

Looks like retention and engagement in our app dips across all cohorts in July. That makes sense if our audience is located in the U.S. or generally in the northern hemisphere. There's the July 4th holiday, there's great weather, school is out, and college is on break  — our users are traveling and spending time outside. Can we implement some new features in our workout app to retain them better in the summer? Travel yoga workouts? Hiking? Beach runs? 🌴

SLICE AND DICE
In the analysis above we've identified that users acquired via advertising behave differently. We also noted that the seasonality pattern may differ in other markets like Australia, where July is the middle of winter. 

At this point, if you feel like you have a lot of geographic variation or lots of variation by user acquisition source (or any other parameters like demographics, monthly vs. annual, subscription plan tier), then it might be helpful to run retention analysis isolating to specific target populations to see if you notice additional patterns. 

We made it to the end of this week's content! The analysis above, as well as simulations from the previous chapter, are available to you in this spreadsheet. Check them out, and you are ready for our project!

