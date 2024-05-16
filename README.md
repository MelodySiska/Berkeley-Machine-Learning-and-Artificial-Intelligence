# Berkeley-Machine-Learning-and-Artificial-Intelligence Course Assignment
Practical Application Assignment 5.1: Will the Customer Accept the Coupon?

The goal of this project is to use visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not. 

I began by reading in the coupons.csv file and investigating the dataset for missing or problematic data. There are very many missing values in the 'car' column (only 108 entries out of 12684)
The 'Bar', 'CoffeeHouse', 'CarryAway', 'RestaurantLessThan20', and 'Restaurant20To50' columns also have missing values, but not so many to exclude them from the analysis. The 'toCoupon_GEQ5min' column is all "1" values. Becasue of the high percentage of missing data in the car column, I chose to remove this column from the dataset and not use this in the analysis.

Through the initial look at the data, I observed the overall about 56.8% of the coupons were accepted. I then created a bar graph to lok at the Frequency of Each Coupon Type. Coffe House coupons were the most prevelant.

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/6ae827a3-c20d-4fda-bd8f-6221bb324b0c)

I created a histogram for the temperature column. Interestingly, there were only 3 options for temperature, 30, 55, and 80. *0 degrees was by far the most frequent temperature reported.

![image](https://github.com/MelodySiska/Berkeley-Machine-Learning-and-Artificial-Intelligence/assets/168995724/4702c677-1f3a-4d39-90b7-ba2f643032d7)

Next, I was guided through analysis of segmenting the data to only look at bar coupons. I began by creating a new DataFrame that contains just the bar coupons. I observed that approximately 41% of the bar coupons were accepted. This suggests a lower acceptance rate compared to the 56.8% overall coupon acceptance rate.

