# K-Means Clustering on Credit Card Dataset

This project demonstrates the application of **K-Means Clustering** on a credit card dataset to group customers based on their financial behavior. The dataset includes features such as credit limit, age, bill amounts, and payment amounts. The goal is to identify meaningful clusters that can help in understanding customer segments.



## 📁 Dataset

The dataset used in this project contains the following columns:

- **ID**: Unique identifier for each customer.
- **LIMIT_BAL**: Credit limit of the customer.
- **SEX**: Gender of the customer (1 = male, 2 = female).
- **EDUCATION**: Education level of the customer.
- **MARRIAGE**: Marital status of the customer.
- **AGE**: Age of the customer.
- **PAY_0 to PAY_6**: History of past payments (e.g., PAY_0 = repayment status in September).
- **BILL_AMT1 to BILL_AMT6**: Amount of bill statement (e.g., BILL_AMT1 = bill amount in September).
- **PAY_AMT1 to PAY_AMT6**: Amount of previous payment (e.g., PAY_AMT1 = payment amount in September).
- **default.payment.next.month**: Target variable (1 = default, 0 = no default).

For this clustering task, we focus on the following features:
- `LIMIT_BAL`: Credit limit.
- `AGE`: Customer age.
- `BILL_AMT1`: Bill amount in September.
- `PAY_AMT1`: Payment amount in September.



## 🛠️ Code Overview

The code performs the following steps:

1. **Data Loading**:
   - The dataset is loaded from a CSV file (`TP3_dataset.csv`).

2. **Data Preprocessing**:
   - Relevant features (`LIMIT_BAL`, `AGE`, `BILL_AMT1`, `PAY_AMT1`) are selected.
   - The data is normalized using `StandardScaler` to ensure all features are on the same scale.

3. **K-Means Clustering**:
   - The K-Means algorithm is applied to the normalized data.
   - The number of clusters is set to 4 (`n_clusters=4`).

4. **Visualization**:
   - The clusters are visualized using a scatter plot matrix with `plotly.express`.

5. **Evaluation**:
   - The quality of clustering is evaluated using the **Elbow Method** to determine the optimal number of clusters.

