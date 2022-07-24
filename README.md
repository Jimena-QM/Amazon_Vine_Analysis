# Amazon_Vine_Analysis

## Overview of the analysis

Understand if their is a bias between paid and non paid reviews of pet products using Amazon Vine. 
The first step of this analysis was to perform an ETL connecting to AWS RDS, extract and transform data using Google Colab and load data to pgAdmin.

Below are the images of the loaded tables in pgAdmin. 
![customer](https://github.com/Jimena-QM/Amazon_Vine_Analysis/blob/main/images/customers_table_postgres.jpg)
![products](https://github.com/Jimena-QM/Amazon_Vine_Analysis/blob/main/images/products_table_postgres.jpg)
![review_id](https://github.com/Jimena-QM/Amazon_Vine_Analysis/blob/main/images/review_id_table_postgres.jpg)
![vine](https://github.com/Jimena-QM/Amazon_Vine_Analysis/blob/main/images/vine_table_postgres.jpg)

The second step, analyzing for positive bias, was performed using Pandas and Jupyter Lab. The objective was to determine if having a paid Vine review makes a difference in the precentage of 5-star reviews using the vine table loaded to pgAdmin.

## Results

![Results](https://github.com/Jimena-QM/Amazon_Vine_Analysis/blob/main/images/Pet_products_vine_analysis.jpg)

- How many Vine reviews and non-Vine reviews were there?
    - 170 reviews were from Vine memebers, that is only 0.45% of the total reviews that are equal or greater than 50% of helpful votes. 
    - 37,840 reviews were non-Vine reviews, that is 99.55% of the total reviews that are equal or greater than 50% of helpful votes. 
- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
    - 65 Vine reviews were 5 stars
    - 20,612 non-Vine reviews were 5 stars
- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
    - 38.24% of Vine reviews were 5 stars
    - 54.47% of non-Vine reviews were 5 stars

## Summary
    Based on the above analysis there seems to be no bias for reviews of Vine members. The percentage of 5 star reviews by Vine members is 38.24% vs 54.47% of non-members. It seems that Vine members that evaluated pet products have no bias when rating a product. 
    Since the percentage of Vine reviews for pet products is only 0.45%, an additional analysis I would perform is to use all the data sets from Amazon vine and validate if the same tendency for pet products is present in all of them. Also, analyzing the distribution of all star-levels across Vine and non-Vine reviews will give us a better understanding if there may be negative bias of Vine members. 



