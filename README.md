# Berkeley-Machine-Learning-and-Artificial-Intelligence Course Assignment
Practical Application Assignment 5.1: Will the Customer Accept the Coupon?

Link to code: https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/blob/main/assignment_5_1_starter/prompt.ipynb


The goal of this project is to use visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not. 

I began by reading in the coupons.csv file and investigating the dataset for missing or problematic data. There are very many missing values in the 'car' column (only 108 entries out of 12684)
The 'Bar', 'CoffeeHouse', 'CarryAway', 'RestaurantLessThan20', and 'Restaurant20To50' columns also have missing values, but not so many to exclude them from the analysis. The 'toCoupon_GEQ5min' column is all "1" values. Becasue of the high percentage of missing data in the car column, I chose to remove this column from the dataset and not use this in the analysis.

Through the initial look at the data, I observed the overall about 56.8% of the coupons were accepted. I then created a bar graph to lok at the Frequency of Each Coupon Type. Coffe House coupons were the most prevelant.

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/6ae827a3-c20d-4fda-bd8f-6221bb324b0c)

I created a histogram for the temperature column. Interestingly, there were only 3 options for temperature, 30, 55, and 80. *0 degrees was by far the most frequent temperature reported.

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/4702c677-1f3a-4d39-90b7-ba2f643032d7)

Next, I was guided through analysis of segmenting the data to only look at bar coupons. I began by creating a new DataFrame that contains just the bar coupons. I observed that approximately 41% of the bar coupons were accepted. This suggests a lower acceptance rate compared to the 56.8% overall coupon acceptance rate. 

I then compared the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more.Frequent Bar Visitors (those who visit a bar 4 to 8 times or more than 8 times a month) have a high acceptance rate of approximately 76.88%. Infrequent Bar Visitors (those who visit a bar 3 times or fewer a month) have a much lower acceptance rate of approximately 37.06%.

Next, I compared the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others to see if there was a difference. there is a difference in the acceptance rates between the two groups: Target Group (drivers who go to a bar more than once a month and are over the age of 25) have an acceptance rate of approximately 69.52%. All Others have a much lower acceptance rate of approximately 33.50%.

I then used the same process to compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry. The comparison of acceptance rates between the two groups shows a huge difference: Filtered Group (drivers who go to bars more than once a month, had passengers that were not kids, and had occupations other than farming, fishing, or forestry) have an acceptance rate of approximately 71.32%. All Others have a much lower acceptance rate of approximately 29.60%.

I compared the acceptance rates between those drivers who:
- go to bars more than once a month, had passengers that were not a kid, and were not widowed OR
- go to bars more than once a month and are under the age of 30 OR
- go to cheap restaurants more than 4 times a month and income is less than 50K.

Drivers who go to bars more than once a month, had passengers that were not kids, and were not widowed: Acceptance rate is approximately 71.32%. Drivers who go to bars more than once a month and are under the age of 30: Acceptance rate is comparable but a little higher - approximately 72.17%. Drivers who go to cheap restaurants more than 4 times a month and have an income less than $50K: Acceptance rate is far lower than the other 2 conditions - approximately 45.35%. The overall acceptance rate for any of these conditions combined is about 58.89%.

Based on these observations, Drivers more likely to accept bar coupons are typically younger, less likely to be widowed, often do not have kids as passengers, and are regular bar goers. This would be a good target market for offering bar coupons.

I was then asked to conduct Independent Investigation to explore one of the other coupon groups and try to determine the characteristics of passengers who accept the coupons. I chose to look at the coffe house coupon segment. Approximately 49.92% of the Coffee House coupons were accepted. In an effort to understand traits of who might accept these coupons, I  created a bar graph of Coffee House Coupon Acceptance Rate by Age. The below 21 crowd has the highest coffee coupon acceptance rate.

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/9e527bd3-5f5c-4c7f-85cf-5eb0cafcb863)

I also looked at Acceptance Rate of Coffee House Coupons by Income. There is a varying responsiveness to coupon offers across income brackets, the  75𝑘−
 87499 group is significantly less likely to accept the coffe house coupon (only 29.7%).

 ![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/a7fc144e-33cb-4125-a6f8-5c0be35f0213)

I looked at Acceptance Rate by Gender for Coffee House Coupons. The acceptance rates between genders is very simailar. Although males have a slightly higher rate of coupon acceptance than females, there are similar enough that it probably isnt a significant factor to consider.

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/f06bcbc9-76f4-4ddc-9fc3-7ae4a41d349c)

Then I looked at Coffee House Coupon Acceptance Rate by Destination. Not surprisingly, those with No Urgent Destination had the highest coupon acceptance rate of approximately 58.1% while the lowest rate were those headed home with only a approximately 36.21% acceptance rate.Those headed to work had an acceptance rate of approximatley 44.58% which was a lower than the overall coffee house coupon acceptance rate of approximately 49.92%.

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/b5c71474-2332-45fa-830e-72e398aba521)

The acceptance rate of Coffee House coupons shows a noticeable difference based on whether or not someone is employeed. Those whose occupation is listed as "Unemployed" are more likely to accept Coffee House coupons compared to those who are employed. Unemployed: 54.21%  versus Employed (all other occupations): 49.21%

I also looked at Coffee House Coupon Acceptance Rate by Passenger. Those who were trqaveling alone or with kids were less likely to accept the coupon than thse traveling with a partner or friends.

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/b4d28b98-e86c-4c15-af29-d1a84e8e123b)

Then I looked at Acceptance Rates by Coffee House Visit Frequency. There is a clear trend where individuals who visit coffee houses more frequently are significantly more likely to accept coupons.

- Never: 18.88% acceptance rate
- Less than once a month (less1): 48.19% acceptance rate
- 1 to 3 times a month (1~3): 64.78% acceptance rate
- 4 to 8 times a month (4~8): 68.59% acceptance rate
- More than 8 times a month (gt8): 65.79% acceptance rate

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/98517172-9ef3-490b-9db4-997374511ce9)

Lastly, I created a Heatmap of Coupon Acceptance Rate by Age and Coffee House Visit Frequency. The acceptance rates generally increases as the frequency of visits increases across all age groups. This indicates that more frequent visitors, regardless of age, are more likely to accept coupons. The highest acceptance rates are generally observed in the younger age groups (below21, 21) for higher frequencies of visits (4-8 times a month, more than 8 times a month). This suggests that younger customers who frequently visit coffee houses are particularly receptive to promotions.

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/52135ce7-7299-4c4c-9131-a778d030169d)


Based on these observations, I hypothesize individuals more likely to accept coffee shop coupons frequent coffeehouses, are typically younger, riding with friend(s) or partner rather than with kids or alone, and have no urgent destination. These would be a good target market for offering coffee shop coupons.
