# Amazon Vine Analysis

## Project Overview
The purpose of this analysis was to analyze Amazon reviews written by members and non-members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies can they pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. This analysis was performed on a dataset of [book reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz). Here is the full list of datasets: [Amazon Review Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)).
For part one of this analysis, data from this set of [book reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz) was extracted, transformed, and loaded into pgAdmin.
For part two of this analysis, PySpark was used to determine if there was any bias toward favorable reviews from Vine members in the selected dataset.

## Results

-This book review [dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz) contained almost all Non-Vine member reviews. Out of 3105520 reviews, only 2 were reviewed by Vine members. There were 3105513 Non-Vine member reviews in this dataset.

<img width="444" alt="Total Reviews" src="https://user-images.githubusercontent.com/88804543/144679034-77668d65-58dc-4f33-825a-24e9baf4f152.png">

<img width="1403" alt="Two Vine Reviews" src="https://user-images.githubusercontent.com/88804543/144679084-c2285907-4798-456d-8ef0-bdad9d334293.png">

<img width="516" alt="Number of NonVine Reviews" src="https://user-images.githubusercontent.com/88804543/144679138-0f06e42a-1093-4392-bb3c-6380198a33d0.png">




## Summary
