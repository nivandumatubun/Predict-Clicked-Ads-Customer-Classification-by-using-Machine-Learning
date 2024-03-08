# **Predict Clicked Ads Customer Classification by using Machine Learning**

## Overview
A company in Indonesia wants to know the effectiveness of an advertisement they broadcast, this is important for the company to know how much the advertisement being marketed is so that it can attract customers to see the advertisement.
By processing historical advertising data and finding insights and patterns that occur, it can help companies determine marketing targets. The focus of this case is to create a machine learning classification model that functions to determine the right target customers.

## Goals
Generate a machine learning model that can detect potential users to convert or be interested in an advertisement. So we can optimize costs in advertising on digital platforms.

## Dataset Overview
| Column                   | Description                                    |
|--------------------------|------------------------------------------------|
| Daily Time Spent on Site | Amount of time spent by the user on the site   |
| Age                      | Age of the user                                |
| Area Income              | Income level of the area where the user lives  |
| Daily Internet Usage     | Amount of time the user spends on the internet |
| Gender                   | Gender of the user                             |
| Timestamp                | Timestamp when the data was recorded           |
| Clicked on Ad            | Whether the user clicked on the ad or not      |
| city                     | City where the user is located                 |
| province                 | Province where the user is located             |
| category                 | Category of the ad                             |

[Documentation Detail](https://github.com/nivandumatubun/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/master/pdf%20Predict%20Clicked%20Ads%20Customer%20Classification.pdf)

## Data Preparation
- Fill Data Null
- Handle Duplicated Rows
- Feature Extraction
- Feature Encoding
- Feature Selection

## Exploratory Data Analysis
- **Clicked on Ad Based** on `Age`, `Daily Time Spent on Site`, and `Daily Internet Usage`
![kde.png](https://github.com/nivandumatubun/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/master/kde.png)

- **User Segmentation**
![scatter.png](https://github.com/nivandumatubun/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/master/scatter.png)

- **Correlation**
![heatmap.png](https://github.com/nivandumatubun/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/master/heatmap.png)

## Modelling (Classification)
- K-Nearest Neighbot
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting<br>
There are 2 experiments on each model, the first **with normalization** and the second **without normalization**.

## Model Evaluation
Evaluation on model is done with *Confusion Matrix*
![conmat.png](https://github.com/nivandumatubun/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/master/conmat.png)

## Feature Importance
![featimportance.png](https://github.com/nivandumatubun/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/master/featimportance.png)

## Summary
Based on the EDA and feature importance that has been made, recommendations can be given, namely that there are 4 important features in predicting whether a customer will click on an ad or not. The 4 important features include:
1. **Daily Internet Usage**<br>
Based on high feature importance, focus your marketing strategy on users who have a high level of daily internet usage. This can be done by providing interesting and relevant advertising content for users who actively use the internet every day.

2. **Daily Time Spent on Site**<br>
This feature shows how long users spend on a website. You can leverage this information by serving more engaging ads to users who spend longer on your website. For example, by displaying more interactive ads or offering special discounts for users who are active on your site.

3. **Area Income**<br>
This feature shows the income level of the area where the user is located. You can adapt your marketing strategy based on this income level. For example, by offering products or services that suit their income level, or by adjusting prices or special offers according to regional income levels.
4. **Age**<br>
A customer's age can also be an important factor in determining their propensity to click on a particular ad. In this case, the adults or elders are a potential market for the digital market.

`Business takeaway :`
1. We can use a more unique method (soft selling) so that advertising is less visible to users.
2. Use mainstream content (simple but a topic of conversation) so you can attract users from the lower class segment.

## Business Simulation
By using the ML model that has been created we can create a simulation as follows, with assumption :
- to advertise to a user you can use a budget of **Rp.10.000,00**
- Using test data as a simulation tool for around 300 users with a total of 164 and 136 users in each class.
- Every user who converts will get a profit of **Rp.12.000,00**

1. **Without Machine Learning Model**
- We will use a budget of around 300 * Rp.10.000,00 = Rp.3.000.000,00 to carry out the advertisement.
- **Cost = Rp.3.000.000,00**
- Meanwhile the conversion rate we will get is 50%.
- Because there are only 136 converts, we will get 136 * Rp.12.000,00 = Rp.1.630.000,00
- **Revenue = Rp.1.630.000,00**
- **Profit = Rp.1.630.000,00 - Rp.3.000.000,00 = - Rp.1.370.000,00**
- Based on the simulation above, if we do not use a machine learning model, we will get **potential loss of Rp.1.370.000,00**


2. **With Machine Learning Model**
- We will advertise only on users who have the potential to be clicked (which we predict 1).
- We will use a budget of around 139 * Rp.10.000,00 = Rp.1.390.000,00 to do the advertisement.
- **Cost = Rp.1.390.000,00**
- Meanwhile the conversion rate we will get is 132/139 = 94.96%
- Of the 139 that we predict there will be 132 users who convert.
- Then we will get 132 * Rp.12.000,00 = Rp.1.580.000,00
- **Revenue = Rp.1.580.000,00**
- **Profit = Rp.1.580.000,00 - Rp.1.390.000,00 = Rp.190.000,00**
- Based on the simulation above, if we use a machine learning model, we will get **potential revenue of Rp.190.000,00**

In conclusion, Machine Learning can work well and can even anticipate potential loss into potential revenue.

