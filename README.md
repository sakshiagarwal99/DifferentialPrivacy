## Introduction to the problem and its significance

The project aims to implement differential privacy in machine learning models, specifically focusing on 
1. Logistic Regression
2. Decision Trees, and 
3. Random Forests

- Differential privacy is crucial in preserving the privacy of individuals while extracting valuable insights from sensitive data, making it relevant in various domains, including finance, healthcare, and more.
* The main idea behind differential privacy is to add a controlled amount of noise or randomness to the data before it is released or analyzed, to prevent the identification of individuals within the dataset.
- While differential privacy provides strong privacy guarantees, it often comes at the cost of decreased model accuracy.

- ## Data collection and preprocessing methods.

#### 1. Utilized the 'bank-additional-full.csv' dataset from the UCI Machine Learning Repository, which focuses on direct marketing campaigns conducted by a Portuguese banking institution, focusing on phone calls to clients. 
#### 2. The dataset consists of 17 attributes, including both demographic information about bank clients and details related to the marketing campaign. The target variable 'y' indicates whether the client subscribed to a term deposit ('yes') or not ('no').
#### 3. Link for the data set: https://archive.ics.uci.edu/dataset/222/bank+marketing

- Key Attributes:
1. age: Numeric - Age of the client.
2. job: Categorical - Type of job.
3. marital: Categorical - Marital status.
4. education: Categorical - Level of education.
5. default: Binary - Has credit in default?
6. balance: Numeric - Average yearly balance in euros.
7. housing: Binary - Has a housing loan?
8. loan: Binary - Has a personal loan?

- Attributes Related to the Last Contact of the Current Campaign:
9. contact: Categorical - Contact communication type.
10. day: Numeric - Last contact day of the month.
11. month: Categorical - Last contact month of the year.
12. duration: Numeric - Last contact duration in seconds.

* Other Attributes:
13. campaign: Numeric - Number of contacts performed during this campaign.
14. pdays: Numeric - Number of days passed since the client was last contacted.
15. previous: Numeric - Number of contacts performed before this campaign.
16. poutcome: Categorical - Outcome of the previous marketing campaign.

* Output Variable:
17. y: Binary - Has the client subscribed to a term deposit?

- Missing Attribute Values: None

#### 4. Data preprocessing involved 
* Label encoding categorical variables,
* Scaling numerical features, and 
* Splitting the dataset into training and testing sets.

## Model selection and implementation.

- Implemented three machine learning models: logistic regression, decision trees, and random forests. Differential privacy was integrated using the diffprivlib library for each model. The epsilon parameter was chosen to control the privacy level, and models were trained on both the original and differentially private datasets.

* Logistic Regression - 
1. Chose Logistic Regression due to its interpretability and effectiveness in binary classification problems.
2. Well-suited for scenarios where understanding the impact of individual features on the outcome is important.
3. Logistic Regression serves as a baseline model for privacy comparisons.

* Decision Tree - 
1. Chose Decision Tree for their ability to capture non-linear relationships in the data.
2. Effective in handling both numerical and categorical data, making them suitable for a diverse dataset.
3. Decision Trees provide transparency into the decision-making process, aiding in model interpretation.

* Random Forest - 
1. Chose Random Forests as an ensemble method to improve predictive accuracy and robustness.
2. Mitigates overfitting often associated with individual Decision Trees.
3. Random Forests are known for their versatility and high performance across various types of datasets.

