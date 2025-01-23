# Customer Segmentation Using Credit Card Data 🏦💳
---
## Project Overview 🌟

Customer segmentation is essential for understanding different behaviors within a customer base and crafting marketing strategies accordingly. In this project, I am tasked with performing customer segmentation for Bank ABC using credit card transaction data over the last 6 months. By implementing clustering algorithms, we can group customers into distinct segments and provide recommendations based on their spending behavior.
---
## Objective 🎯
The goal of this project is to:
- Obtain data using Google BigQuery 📊
- Prepare the data for clustering 🔄
- Apply clustering techniques using Scikit-Learn 🤖
- Implement clustering to segment customers based on their credit card usage 💳
- Provide business recommendations for each customer segment 💡
---
## Dataset 📑
The dataset used in this project contains customer credit card information, such as:
- **TENURE** (length of time the customer has been with the bank)
- **PURCHASES** (total purchases made)
- **BALANCE** (credit card balance)
- **PAYMENTS** (amount paid)
- **CREDIT_LIMIT** (maximum credit limit)
- **PURCHASES_FREQUENCY** (how often purchases are made)
---
The data was obtained from Google BigQuery with the following parameters:
- **Project ID**: `ftds-hacktiv8-project`
- **Dataset Name**: `phase1_ftds_<batch-number>_hck`
- **Table Name**: `credit-card-information`
---
## Problem Statement 💬
Bank ABC’s marketing team requested a customer segmentation analysis based on credit card usage. The goal is to identify meaningful customer groups through clustering and provide targeted recommendations for each group.

Key questions to answer:
1. How does **TENURE** influence **PURCHASES**, **BALANCE**, and **PAYMENTS**? 
2. Does a higher **CREDIT_LIMIT** correlate with higher **PURCHASES_FREQUENCY**? 
---
## Methodology 🧑‍💻

### 1. Data Loading 📥
We load the data from Google BigQuery into the environment, ensuring we check for missing values and rename columns for clarity. 

### 2. Exploratory Data Analysis (EDA) 🔍
Exploration is done to examine the relationship between variables like **TENURE**, **PURCHASES**, **BALANCE**, **PAYMENTS**, and **CREDIT_LIMIT**. We also visualize how these features correlate and offer business insights.

### 3. Feature Engineering 🔧
We preprocess the data by normalizing numerical values and encoding categorical variables to make them suitable for clustering. We also perform feature selection based on correlation analysis.

### 4. Clustering Model 🤖
We use the **K-Means** clustering algorithm, applying the **Elbow Method** to determine the optimal number of clusters for the dataset.

### 5. Model Evaluation 📈
The model is evaluated using the **Silhouette Score**, and results are visualized to determine the quality of the clusters.

### 6. Business Insights & Recommendations 💡
Business recommendations are provided for each cluster to guide marketing strategies. Segments like **Cautious Spenders**, **Inactive Users**, and **Big Spenders** will benefit from tailored marketing approaches.
---
## Libraries Used 📚

- `google.cloud` (for BigQuery)
- `pandas`, `numpy` (for data manipulation)
- `seaborn`, `matplotlib` (for data visualization)
- `sklearn` (for clustering and preprocessing)
- `pickle` (for model saving)

```python
# Example of libraries used in the project
from google.colab import auth
from google.cloud import bigquery
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.cm as cm
import matplotlib.pyplot as plt
from sklearn.decomposition import PCA
import warnings
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import silhouette_score, silhouette_samples
from sklearn.cluster import KMeans
```
---
## Model Evaluation 🏅
### Clustering Results 🎯

The K-Means model was trained with 4 clusters as determined by the Elbow Method. The evaluation of clustering results using Silhouette Score indicates good separation of customer groups.

### Insights from the clusters:

Cautious Spenders: Customers with low spending behavior and low balance. 💰
Inactive Users: Customers with a long tenure but low purchasing activity. ⏳
Regular Users: Customers with moderate spending frequency and balance. 🛒
Big Spenders: Customers with high purchasing frequency and balance. 💸
---
## Business Recommendations 💡

Cautious Spenders: Offer loyalty rewards to encourage increased purchasing frequency. 🎁
Inactive Users: Re-engage with personalized promotions to encourage spending. 💌
Big Spenders: Provide exclusive offers to retain these high-value customers. 💎
---
## Conclusion 🎉
This project successfully segments customers into meaningful clusters, providing insights into customer behavior. The marketing team can now implement targeted strategies to improve customer engagement and maximize revenue.
---
## Contact
LinkedIn: www.linkedin.com/in/muhammadasharihsan
Email: ashar4iksan@gmail.com
