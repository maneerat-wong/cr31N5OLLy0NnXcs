# Customer Satisfication Prediction using Machine Learning

The company is one of the fastest growing startups in the logistics and delivery domain and works with several partners and make on-demand delivery to our customers. The company wants to to measure how happy each customer is in order to grow with the right global expansion strategy.

The company provides me a dataset of several customer feedback and a label whether the customer is happy.

## Goal

- Predict if a customer is happy or not based on the answers they give to questions asked. The company is aiming for 73% accuracy score or above
- Find which questions/features are more important when predicting a customer’s happiness

### Data Description

* Y = target attribute (Y) with values indicating 0 (unhappy) and 1 (happy) customers 
* X1 = my order was delivered on time
* X2 = contents of my order was as I expected
* X3 = I ordered everything I wanted to order
* X4 = I paid a good price for my order
* X5 = I am satisfied with my courier
* X6 = the app makes ordering easy for me

Attributes X1 to X6 indicate the responses for each question and have values from 1 to 5 where the smaller number indicates less and the higher number indicates more towards the answer.

# Conclusion

### <u> Model performance </u>

| Model | Test Score (Accuracy) | Test Score (F-1 Score) | Train Score (Accuracy) |
|-------|-------------|----------| ----- |
| Logistic Regression | 0.61 | 0.66 | 0.56 |
| KNN | 0.69| 0.73 | 0.76 |
| Random Forest| 0.61 | 0.66 | 0.69 |
| Decision Tree | 0.50 | 0.55 | 0.71 |
| SVC | 0.73 | 0.74 | 0.63 |
| XGBoost | 0.57 | 0.62 | 0.89 |



The SVC model performed the best with a test accuracy of 73% and an F1 score of 74%, which is slightly higher due to the class imbalance in the dataset. SVC tends to handle small datasets better than more complex models like XGBoost, which typically performs well on larger datasets. Given the small size of the dataset, SVC's simpler model structure allows it to generalize better and avoid overfitting compared to more complex models that might require more data to fully capture patterns.

### <u> Feature Selection </u>

In terms of features, X5 ("I am satisfied with my courier") has the highest correlation with customer satisfaction, followed by X1 ("My order was delivered on time"), which both related to the shipment. X2 ("Contents of my order was as I expected") shows the lowest correlation.

I would suggest the company to gather more feedbacks related to the shipment process and potentially remove X2 feature from the future surveys to enhance the company's predictive capabilities and growth potential.
