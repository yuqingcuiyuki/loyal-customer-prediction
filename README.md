# Loyal Customer Prediction
### Goal: Predict if a new customer will become loyal customers in the future,i.e. predict the probability of new customer buying again within 6 months.
### 1. EDA
- check data type and shape
- check missing value: use -1 or 2(gender) to fill
- check data distribution, outlier?
- check label balance: imblanced
- explore current features and engineered relevant features 
    - aggregate sales
    - user and merchant features
- merge all data, fill na (0)
- dimension reduction: check correlation, remove some? pca?
### 2. Modeling
- Logistics regression
- KNN
- Decision tree
- Random forest
- SVM (very slow as expected)
### Summary
- With an **imblanced dataset**, all models have similar accuracy (around 93%), but other than logistic regression, other models have bad precision, recall and f1. After bootstrapping data to make it balanced, KNN performs the best with accuracy: 0.868, precision: 0.793, recall: 0.996, f1: 0.883
- **limitation of current features**: 
<br>Customer journey: register as a customer (demographics) -> browse (click, add to cart, favorate) -> purchase -> leave comment (or automatic 5 stars). For feature engineer, we only have data until purchase, but comment and score are also very important. They reflect if a customer is satisfied with the product. Some customer will leave comments like "very good, will buy again", so sentiment and text analysis of comment data is crucial.
