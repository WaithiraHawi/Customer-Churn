# Customer Churn Analysis

This project performs exploratory data analysis and predictive modeling on a bank's customer dataset to identify patterns related to customer churn. It explores key factors that influence customer retention and builds models to predict whether a customer is likely to leave the bank.


## Dataset
* Size: 10,000 rows × 18 columns
* Features:
  * Customer demographics (e.g., Age, Gender, Geography)
  * Account details (e.g., Balance, Tenure, NumOfProducts)
  * Engagement metrics (e.g., CreditScore, Complain, Satisfaction Score)
  * Churn status (`Exited`: 1 = Yes, 0 = No)

## Project Workflow

### **Data Loading and Inspection**

* Loaded data using `pandas`
* Checked data structure using `.info()` and `.head()`

### **Exploratory Data Analysis (EDA)**

Key visualizations:

* Customer Churn Distribution
* Churn by Gender
* Churn by Geography
* Age Distribution by Churn
* Feature Correlation Heatmap

## KPIs & Insights

| KPI / Feature          | Insight                                                |
| ---------------------- | ------------------------------------------------------ |
| **Exited**             | Binary churn indicator (0 = stayed, 1 = left)          |
| **Gender**             | Compared churn patterns across genders                 |
| **Geography**          | Evaluated churn rates by country                       |
| **Age**                | Older customers showed a higher likelihood of churning |
| **Credit Score**       | Weak correlation with churn                            |
| **Satisfaction Score** | Lower scores were associated with higher churn         |

## Data Preprocessing

* Dropped unnecessary identifier: `customerID` (if present)
* No missing values were detected
* Labelled encoded categorical features (`Gender`, `Geography`, `Card Type`, `Surname`)
* Feature scaling and correlation analysis

## Technologies Used

| Tool                     | Purpose                            |
| ------------------------ | ---------------------------------- |
| `Pandas`                 | Data loading and manipulation      |
| `Matplotlib` & `Seaborn` | Visualizations                     |
| `Scikit-learn`           | Encoding, modeling, and evaluation |
| `Jupyter Notebook`       | Interactive development            |

## Recommendations

* Focus retention efforts on:
  * Older customers with lower satisfaction
  * Customers in specific geographies (e.g., countries with high churn)
* Integrate churn prediction into CRM for real-time alerts
* Offer loyalty incentives to high-risk segments
