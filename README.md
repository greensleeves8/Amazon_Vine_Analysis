# Amazon Vine Analysis

Cloud ETL with PySpark, SQL, Pandas, and AWS

## Overview of the Analysis

For this project we were tasked with using the cloud ETL process to analye datasets of Amazon reviews, 
with the end goal of separating paid Amazon Vine reviews from non-Vine reviews. By separating the Vine and 
Non-Vine reviews, we're able to compare the two datasets and examine them for any bias toward favorable reviews
that the Vine members may have.

## Results

The analysis of the Vine and non-Vine reviews yielded the following results:

- After filtering our initial table of reviews to only include reviews with at least 20 total votes, and then 
further filtering to exclude reviews that were not considered 'helpful' by at least 50% of the votes, we were 
left with datasets of 60 Vine reviews, and 14,447 non-Vine reviews, respectively. 
![Size of Vine and non-Vine DataFrames](https://github.com/greensleeves8/Amazon_Vine_Analysis/blob/main/Resources/Vine_reviews.png "Vine and non-Vine Reviews")

- Of the Vine reviews, 34 were rated 5 stars. Of the non-Vine reviews, 8212 were rated 5 stars. 
![5 Star ratings](https://github.com/greensleeves8/Amazon_Vine_Analysis/blob/main/Resources/5_star_Reviews.png "5 Star Reviews")

- 56.67% of the Vine reviews were rated 5 stars, and 56.72% of the non-Vine reviews were rated 5 stars.
![% of Five Star Reviews](https://github.com/greensleeves8/Amazon_Vine_Analysis/blob/main/Resources/Vine_Summary_DF.png "% of 5 Star Reviews")

## Summary

In summary, there does not seem to be any positivity bias among the Vine reviews, as the Vine reviews and the non-Vine
reviews were essentially equal, with the non-Vine reviews actually having a slightly larger rate of positive reviews.
The biggest issue with the current data is the relatively small sample of Vine reviews compared to the non-Vine reviews. 
Personally, I would consider finding the rate of 5-star Vine reviews among the entire dataset as compared to the non-Vine
reviews before filtering the sample down further. 

