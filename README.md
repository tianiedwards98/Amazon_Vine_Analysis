# Amazon Vine Analysis

## Overview of Project
For this week's project, we will be looking at Big Data and Cloud Services. Big Data is data that has more variety and is generating at high volumes quickly. Spark has become the leading technology for handling big data. This will allow us to process and analyze data quickly and at a massive scale. We will also be using Google Colab since it is hosted in the cloud. This makes it easier to read datasets that are from the cloud as well. Our data will be pulled from Amazon's Simple Storage Service (S3).

## Results 
In order for us to determine if there was a bias of Vine Reviews, we created a dataframe from our Amazon review data that had 6 columns:

review_id: The unique ID of the review.
star_rating: The 1-5 star rating of the review.
helpful_votes: Number of helpful votes.
total_votes: Number of total votes the review received.
vine: Review was written as part of the Vine program.
verified_purchase: The review is on a verified purchase.
We filtered the dataframe to retrieve rows where the total_count was greater or equal to 20 and also filtered to show reviews that are more likely to be helpful. We created two more dataframes based on if the review was a Vine review (paid) or non-Vine review (unpaid).

Here are the results of total number of reviews, the number of 5-star reviews, and percentage of 5-star reviews for the two types of review (paid vs. unpaid)

Total Number of Reviews

Vine Reviews
![Screenshot](https://github.com/tianiedwards98/Amazon_Vine_Analysis/blob/main/Screenshots/paid-total-reviews.png?raw=true)


Non-Vine Reviews
![Screenshot](https://github.com/tianiedwards98/Amazon_Vine_Analysis/blob/main/Screenshots/unpaid-total-reviews.png?raw=true)

Number of 5 Star Reviews

Vine 5 Star Reviews
![Screenshot](https://github.com/tianiedwards98/Amazon_Vine_Analysis/blob/main/Screenshots/paid-5-star.png?raw=true)


Non-Vine 5 Star Reviews
![Screenshot](https://github.com/tianiedwards98/Amazon_Vine_Analysis/blob/main/Screenshots/unpaid-5-star.png?raw=true)

Percentage of 5 Star Reviews

Vine 5 Star Review Percentage
![Screenshot](https://github.com/tianiedwards98/Amazon_Vine_Analysis/blob/main/Screenshots/paid-percentage.png?raw=true)


Non-Vine 5 Star Review Percentage
![Screenshot](https://github.com/tianiedwards98/Amazon_Vine_Analysis/blob/main/Screenshots/unpaid-percentage.png?raw=true)


##Summary
After reviewing the results comparing the Vine vs. Non-Vine reviews, there is not a bias for reviews in the Vine program. As seen in the images above, 33% of Vine members reviews were 5-star and 55% of Non-Vine reviews were 5-star. The number of Vine reviews total in comparison to Non-Vine reviews is significantly less though.

In order to confirm the Non-Vine customers actually purchased the item from Amazon or that it wasn't gifted, we can also filter based on the verified_purchase column. After rerunning the calculations on this new dataframe, 57% of Non-Vine members reviews were 5-star and verified that they purchased the item.

![Screenshot](https://github.com/tianiedwards98/Amazon_Vine_Analysis/blob/main/Screenshots/Additional-analysis-1.png?raw=true)

![Screenshot](https://github.com/tianiedwards98/Amazon_Vine_Analysis/blob/main/Screenshots/Addititonal-analysis-2.png?raw=true)
