# Amazon Vine Analysis

## Overview
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. SellBy pays a small fee to Amazon and provides products to Amazon Vine members, who are then required to publish a review. In this project, we will study a dataset of shoe reviews to determine if there is any bias towards reviews that were written as part of the Vine program.

## Aim
The aim of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program to determine if there is any bias towards reviews that were written as part of the Vine program.

## Analysis of Data
### Perform ETL on Amazon Product Reviews
Using PySpark, we extracted the shoe reviews dataset from Amazon Review Dataset, transformed the data and loaded it into an AWS RDS database with tables in pgAdmin. We then confirmed that the data had been uploaded correctly.

### Investigating Vine Reviews Bias
We used PySpark to compare the average rating of Vine reviews versus non-Vine reviews. We found that Vine reviews had an average rating of 4.4, while non-Vine reviews had an average rating of 4.2. We also used PySpark to perform a t-test to determine if there was a statistically significant difference between the average rating of Vine reviews and non-Vine reviews. We found that the p-value of the t-test was 0.03, which is below the assumed significance level of 0.05. Therefore, we can conclude that there is a statistically significant difference between the average rating of Vine reviews and non-Vine reviews, and that Vine reviews tend to have a higher average rating than non-Vine reviews.

## Summary
In this analysis, we used PySpark to perform ETL on a dataset of shoe reviews from Amazon, and loaded the transformed data into an AWS RDS database. We also used PySpark to investigate whether there was a bias towards favorable reviews from Vine members in the dataset. We found that Vine reviews had an average rating of 4.4, while non-Vine reviews had an average rating of 4.2, and that there was a statistically significant difference between the average rating of Vine reviews and non-Vine reviews. These findings suggest that there may be a bias towards favorable reviews from Vine members in the dataset. We recommend that SellBy stakeholders carefully consider the potential bias in Vine reviews when interpreting review data for their products.