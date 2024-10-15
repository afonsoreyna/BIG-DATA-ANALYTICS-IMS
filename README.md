# Customer Targeting with Machine Learning

## Project Context

The objective of this project was to identify a group of customers who would be most receptive to receiving a voucher. We employed a supervised uplift machine learning approach to analyse customer behaviour and predict their likelihood of making a purchase. However, there were some nuances to be considered. The objective was to drive revenue, so it was crucial to avoid targeting customers who were likely to purchase without the incentive of a voucher. This was to minimise cannibalisation. In essence, the target audience were persuadable customers who were not prone to making a purchase, but who would respond positively when incentivised with a voucher.

## Methodology

The process involved several key steps:

1.	Feature Creation:
- We constructed a set of features using customer data from January to June. These features were designed to capture various aspects of customer behavior and engagement, providing a comprehensive view of each customer’s interaction with the brand.
2.	Label Assignment:
- We analyzed an AB test conducted in June, assigning labels to each customer based on their purchase behavior:
- Label 1: Assigned if a customer made an order in June, regardless of their group (control or test).
- Label 0: Assigned if a customer did not make an order.
3.	Dataset Preparation:
- We compiled the final dataset, which contained customer IDs and reference dates, labeling customers based on their purchase activity in each group. The dataset was then split into two separate DataFrames: df_control for the control group and df_test for the test group.
4.	Preprocessing and Modeling:
- Necessary preprocessing techniques were applied to both datasets. We trained separate machine learning models for each group, focusing on predicting whether a customer would make a purchase based on their historical data.
5.	Filtering and Evaluation:
- After obtaining predictions for both groups, we merged the results into a single dataset. We filtered customers who were predicted as unlikely to purchase in the control group (label 0) but likely to purchase in the test group (label 1). This filtering helped identify customers with a higher probability of responding positively to the voucher offer.
6.	Campaign Performance Evaluation:
- The filtered customers were utilized to evaluate the overall performance of our voucher campaign, allowing us to optimize future marketing efforts based on predictive insights.

## Results

The notebook provides a detailed overview of the entire process, including visualizations of the model’s performance and the effectiveness of the targeted voucher campaign.

## Features

- Customer Segmentation: Identify customer groups based on behavior and purchase history.
- Supervised Learning Models: Implemented models for predicting purchase likelihood.
- Data Preprocessing Pipelines: Utilized PySpark for efficient data handling and transformations.
- Evaluation Metrics: Included metrics to assess the performance of the predictive models.
