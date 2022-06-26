# Background

Since your work with Jennifer on the SellBy project was so successful, you’ve been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, you’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. You’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, you’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. Then, you’ll write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.

# Objective
- Deliverable 1: Perform ETL on Amazon Product Reviews
- Deliverable 2: Determine Bias of Vine Reviews
- Deliverable 3: A Written Report on the Analysis (README.md)

# Results
Results are included in [Amazon_Vine_Analysis.ipynb](./Amazon_Vine_Analysis.ipynb) and [Vine_Review_Analysis](./Vine_Review_Analysis.ipynb) 

Based on the results for [Home Reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Home_v1_00.tsv.gz) dataset, there is a slight negative bias with vine reviews. However, we should look at other statistical metrics to evaluate further.

``` sql
VINE REVIEW METRICS
---------------------------------------------------------
Total Vine reviews          : 1448
Total Vine 5 star reviews   : 647
Percent Vine 5 star reviews   : 0.45
---------------------------------------------------------
NON VINE REVIEW METRICS
---------------------------------------------------------
Total Non Vine reviews          : 90768
Total Non Vine 5 star reviews   : 44104
Percent Non Vine 5 star reviews   : 0.49
---------------------------------------------------------
```