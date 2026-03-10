# Customer Behavior Analysis with RFM Segmentation

## Project Overview
This project analyzes customer purchasing behavior using **RFM (Recency, Frequency, Monetary) analysis** to identify valuable customer segments. The goal is to transform transactional data into actionable insights that businesses can use for **customer retention, targeted marketing, and revenue optimization**.

Using Python-based data analysis tools, the project performs data cleaning, feature engineering, customer segmentation, and visualization.

This project demonstrates practical **data science workflow skills**, including exploratory data analysis, feature engineering, customer segmentation, and data visualization.

---

## Business Problem
Businesses often struggle to identify which customers bring the most value and which customers are at risk of churn.

This project answers key business questions:

- Which customers are the most valuable?
- Which customers purchase frequently?
- Which customers have not purchased recently?
- How can customers be segmented for targeted marketing strategies?

RFM analysis provides a data-driven approach to answering these questions.

---

## Dataset
The dataset contains **retail transaction data** including customer purchase history.

Key features used in this project include:

| Feature | Description |
|------|-------------|
| InvoiceNo | Unique transaction identifier |
| StockCode | Product code |
| Description | Product description |
| Quantity | Number of items purchased |
| InvoiceDate | Date and time of purchase |
| UnitPrice | Price per item |
| CustomerID | Unique identifier for customers |
| Country | Country of the customer |

From these features, we derive the **RFM metrics**.

---

## RFM Metrics Explained

### Recency (R)
Measures how recently a customer made a purchase.

Customers who purchased recently are more likely to engage again.

### Frequency (F)
Measures how often a customer makes purchases.

Frequent buyers indicate higher loyalty and engagement.

### Monetary (M)
Measures how much money a customer spends.

Customers with higher total spending contribute more revenue.

---

## Project Workflow

### 1. Data Cleaning
- Removed missing or invalid values
- Converted date fields to datetime format
- Filtered negative or invalid transactions

### 2. Feature Engineering
Calculated the RFM metrics:

- **Recency** = Days since last purchase
- **Frequency** = Number of purchases
- **Monetary** = Total spending per customer

### 3. RFM Scoring
Customers are ranked using quantile-based scoring for each metric.

Example scoring scale:

| Score | Meaning |
|-----|-------|
| 1 | Low value |
| 5 | High value |

Each customer receives an **RFM score combination**.

Example: R = 5, F = 4, M = 5


### 4. Customer Segmentation
Customers are grouped into segments such as:

- Champions
- Loyal Customers
- Potential Loyalists
- At Risk Customers
- Lost Customers

These segments help businesses create targeted marketing strategies.

### 5. Data Visualization
Visualizations are used to understand customer distribution and segment behavior.

Examples include:

- Customer segment distribution
- Frequency by segment
- Spending behavior

Tools used include:

- **Plotly**
- **Seaborn**
- **Matplotlib**

---

## Technologies Used

| Tool | Purpose |
|----|----|
| Python | Data analysis |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Seaborn | Statistical visualization |
| Plotly | Interactive visualization |
| Matplotlib | Plotting |
| Jupyter Notebook | Development environment |

---

## Key Insights
Some important insights from the analysis include:

- A small percentage of customers generate the majority of revenue.
- Some high-frequency customers have not purchased recently and may require re-engagement campaigns.
- Certain segments show strong loyalty and high spending behavior.

These insights can guide **targeted marketing strategies and customer retention efforts**.

---

## Repository Structure

online-retail-analysis
│
├── Customer_Behavior_Analysis.ipynb # Main analysis notebook
├── README.md # Project documentation
└── online_retail.csv
