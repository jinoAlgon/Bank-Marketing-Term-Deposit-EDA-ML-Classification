# Bank Marketing Campaign Predictive Analytics

## Problem Statement

The Portuguese bank has been experiencing a revenue decline due to clients not depositing as frequently as before. Term deposits are critical as they:
- Allow the bank to retain funds for longer periods, enabling investments in higher-yield financial products.
- Provide opportunities to cross-sell other financial products like funds or insurance to increase revenue.

The objective of this project is to identify existing clients who are most likely to subscribe to a term deposit and optimize marketing efforts towards these clients.

---

## About the Dataset

- **Source**: [Kaggle Bank Marketing Campaigns Dataset](https://www.kaggle.com/datasets/volodymyrgavrysh/bank-marketing-campaigns-dataset)
- **Description**: The dataset consists of results from direct phone call campaigns, with the target variable indicating whether a client subscribed to a term deposit (`yes`/`no`).


## About the Project

This project involves analyzing the dataset, performing exploratory data analysis (EDA), and building a classification algorithm. The goal is to help the bank identify high-potential clients for term deposits.

### Objectives:
1. **Data Preparation**: Cleaning and preprocessing the dataset.
2. **Exploratory Data Analysis (EDA)**: Identifying key patterns and insights.
3. **Feature Engineering**: Transforming features for better predictive performance.
4. **Modeling**: Building and evaluating machine learning models.
5. **Recommendations**: Providing actionable insights for marketing optimization.

---

## Data Preparation and Cleaning

- **Initial Dataset**: 41,188 instances and 21 features.
- **Cleaning Steps**:
  - Addressed outliers in key numerical features using the IQR method.
  - Encoded categorical variables with techniques like ordinal, one-hot, and frequency encoding.
  - Standardized numerical features for uniformity.
  - Selected the top 15 features based on importance using `ExtraTreesClassifier`.

---

## Exploratory Data Analysis (EDA)

### Key Insights:
1. **Call Duration**: Clients with longer call durations were more likely to subscribe to term deposits.
2. **Job Roles**: Administrative, technician, and blue-collar jobs had the highest subscription rates.
3. **Education**: University graduates showed the highest subscription rates.
4. **Seasonality**: Campaigns were most successful during May, June, and July.
5. **Economic Context**: Employment variation and consumer price index positively influenced subscriptions.

---

## Feature Engineering

### Techniques:
1. **Outlier Handling**: Used IQR to manage anomalies in `age`, `campaign`, and `duration`.
2. **Categorical Encoding**:
   - Mapped `yes/no/unknown` fields to `1/0/-1`.
   - Applied one-hot encoding for `contact` and `poutcome`.
3. **Feature Scaling**: Standardized numerical features.
4. **Feature Selection**: Selected the top 15 impactful features using importance scores.

---

## Modeling

### Model Selection
Multiple classification models were evaluated using cross-validation:
- Logistic Regression: **92.4% accuracy**
- Support Vector Classifier (SVC): **91.9% accuracy**
- Decision Tree: **63.6% accuracy**
- K-Nearest Neighbors (KNN): **87.4% accuracy**
- Naive Bayes: **81.9% accuracy**

### Best Model: Logistic Regression
- Tuned hyperparameters (`C`, `penalty`) using GridSearchCV.
- Achieved **92% test accuracy** with excellent precision and recall.

### Evaluation Metrics:
- **Confusion Matrix**: High true positive rate.
- **ROC Curve**: Strong predictive capability.

---

## Conclusion and Recommendations

### Key Findings:
1. **Call Duration**: The most significant predictor of deposit likelihood.
2. **Job Roles & Education**: Strongly influence deposit outcomes.
3. **Seasonality**: Campaign success peaks during May, June, and July.

### Recommendations:
1. **Segment Job Roles**: Focus on tier-1 employees for early outreach.
2. **Enhance Call Quality**: Increase call duration by understanding client needs.
3. **Optimize Campaign Timing**: Target campaigns during favorable months (May–July).
4. **Economic Adaptation**: Align campaigns with positive economic indicators.

---

## Technologies Used

- **Programming Language**: Python
- **Libraries**:
  - Data Manipulation: `Pandas`, `NumPy`
  - Visualization: `Matplotlib`, `Seaborn`, `Plotly`
  - Machine Learning: `Scikit-learn`
  - Feature Selection: `ExtraTreesClassifier`

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/jinoAlgon/Bank-Marketing-Term-Deposit-EDA-ML-Classification.git

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt

3. Run the notebook:
   ```bash
   jupyter notebook bank-marketing-campaign-predictive-analytics.ipynb

4. Execute the cells in the notebook to reproduce the analysis.

## Acknowledgments

  - Dataset Source: Kaggle Bank Marketing Campaigns Dataset
  - Special thanks to the UCI Machine Learning Repository.