# Amazon Vine Analysis

## Project Overview
The purpose of this analysis was to analyze Amazon reviews written by members and non-members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies can they pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. This analysis was performed on a dataset of [book reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz). Here is the full list of datasets: [Amazon Review Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)).
For part one of this analysis, data from this set of [book reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz) was extracted, transformed, and loaded into pgAdmin.
For part two of this analysis, PySpark was used to determine if there was any bias toward favorable reviews from Vine members in the selected dataset.

## Results

### Results Based on Entire Dataset

The following results are based on the entire dataset:

- The [dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz) contained almost all non-Vine member reviews. Out of 3105520 reviews, only 2 were reviewed by Vine members. There were 3105513 Non-Vine member reviews in this dataset.

<img width="444" alt="Total Reviews" src="https://user-images.githubusercontent.com/88804543/144679034-77668d65-58dc-4f33-825a-24e9baf4f152.png">

<img width="1403" alt="Two Vine Reviews" src="https://user-images.githubusercontent.com/88804543/144679084-c2285907-4798-456d-8ef0-bdad9d334293.png">

<img width="516" alt="Number of NonVine Reviews" src="https://user-images.githubusercontent.com/88804543/144679138-0f06e42a-1093-4392-bb3c-6380198a33d0.png">

- Out of the 2 Vine member reviews, 1 of them was 5 stars. So 50% of the 2 Vine member reviews were 5 stars.
- In total, there were 1864804 5 star reviews. 1 out of the 1864804 (<0.0001%) was a Vine member. 
- 1864803 out of the 1864804 (99.99%) 5 star reviews were from non-Vine members.
- Of the non-Vine reviews, 60% were 5 stars.

<img width="843" alt="Total Number of 5 Star Reviews" src="https://user-images.githubusercontent.com/88804543/144681595-616082ff-62da-42d4-a0d0-8d1919e59faa.png">


### Results Based on Subset of Data

#### Subset Criteria
The following results are based on a subset of the dataset. This subset includes reviews that meet the following criteria:
1. Each review has 20 or more total votes
2. Each review has 50% or more helpful votes relative to total votes

#### Results:
- There were 0 Vine reviews and 403807 non-Vine reviews out of 403807 reviews.
- Number of 5 star Vine reviews: 0
- Number of 5 star non-Vine reviews: 242889
- Total number of 5 star reviews: 242889
- 0% of the Vine reviews were 5 stars
- 100% of the non-Vine reviews were 5 stars






## Summary
Within this dataset, there was no positivity bias for reviews in the Vine program. It is critical to highlight that less than 0.001% of the total reviews in this dataset were from Vine members. Only 2 of 3105520 reviews were from Vine members. This analysis should be repeated for other available datasets that contain a more equal distribution of Vine and non-Vine member reviews.




