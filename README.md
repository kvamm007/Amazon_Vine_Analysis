# Amazon Vine Program Analysis

## Overview
The purpose of this analysis was to determine whether there is a bias towards favorable reviews from Vine members (customers who receive free products and are required to publish a review of the product in return) in the dataset of jewelry reviews on Amazon. 

## Results
For Jewelry reviews with at least 20 votes, here is what we observed for Vine (paid) versus non-Vine (unpaid, regular customers) reviews: 
![Review Summary](https://user-images.githubusercontent.com/85597801/138619229-29d97b0a-1d82-4a39-b1d1-09c7db66915e.png)

-	There were 21 total reviews marked as Vine reviews, and 7,689 reviews marked as non-Vine. At this point we are unsure how that compares to other data sets- but at least within jewelry, the Vine reviews (at least with 20 votes minimum) are very small compared to the ‘free’ reviews.
-	Of the Vine reviews, 11 reviews gave 5 stars. Of the non-Vine reviews, 4,444 gave 5 stars. It is difficult to compare these numbers without reviewing percentages (see next bullet for comparison) as the review count is so drastically different
-	52.4% of the Vine reviews in our jewelry review set received 5 stars; 57.8% of the non-Vine reviews received 5 stars. 

## Summary
Based on our results above, we would actually conclude it is possible that there is a slight negative bias by the Vine participants compared to regular non-Vine (paying) customers, which is the opposite of what we would expected to see. 

Since we came out with such a small number of Vine reviews, we may want to re-evaluate our filter. Based on the view of the top 20 rows in our original data set, most of the reviews have very few, if any, “total votes”. Assuming that this is the place where people vote whether the review is helpful or not, this may not necessarily be a good measure to use to exclude reviews. The positive reviews do seem to be slightly higher for Vine customers than non-Vine, however, the Vine sample set is so small that with the numbers being as close as they are (within about 5%) we would really need a larger sample of Vine reviews to be able to draw a conclusion about bias that may be seen with the Vine reviews. 

![Vine Table](https://user-images.githubusercontent.com/85597801/138619254-a7e18bf4-4fb9-4d48-a976-a3b1d232ba83.png)


### Additional Future Analysis
There is an additional analysis that could be performed which I believe would provide interesting or more robust data: remove the filters for at least 20 votes and at least 50% of votes being helpful. 

**Reasons to remove:**
 -	Whether a review receives votes as “Helpful” or “Unhelpful” we are reviewing the star rankings for this situation, and the stars still count towards the total item score whether it is helpful or not, or viewed or not. 
 -	We believe many customers look only at the aggregate score (especially as this is an easy to use filter) and this is impacted regardless of how many votes a comment has received. Also based on the first 20 rows of our original dataset, it appears we may be filtering out a lot of feedback by removing those with votes. 

**Benefits:**
 -	Removing these filters, we can compare a larger set of data for star ratings and whether the user is Vine or not. 
 -	We can perform an additional calculation to view whether Vine or non-Vine user reviews are viewed as more helpful. Based on our original calculations, it’s possible that standard users give reviews that are viewed as more helpful than Vine reviewers, as they may be more ‘invested’ in the product, since they spent money on it. 

