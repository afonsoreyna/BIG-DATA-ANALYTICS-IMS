# Customer Targeting with Machine Learning

This project implements a machine learning model to identify customers likely to respond positively to a voucher campaign, based on their past behavior.

## Project Overview

We used a supervised learning approach to predict customer responses and optimize voucher distribution. The project involved:

- Feature Engineering: Created features based on customer behavior from January to June.
- Label Assignment: Labeled customers as 1 (purchase) or 0 (no purchase) based on a June AB test.
- Model Training: Separate models were trained for control and test groups to predict future purchases.
- Campaign Evaluation: We filtered customers predicted as unlikely to purchase in the control group but likely in the test group, indicating high response potential to the voucher.

## Features
- Customer segmentation based on AB testing.
- Supervised learning models for control and test groups.
- Preprocessing pipelines using PySpark.
- Feature and label generation for customer targeting.
