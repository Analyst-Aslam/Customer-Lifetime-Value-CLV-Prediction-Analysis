#  Customer Lifetime Value (CLV) Prediction & Analysis

This project focuses on **predicting Customer Lifetime Value (CLV)** using a real-world transactional dataset from a UK-based online retail store. The data spans from **December 2010 to December 2011** and includes purchases made by both **wholesalers and individual customers**.

---

##  What is CLV?

**Customer Lifetime Value (CLV)** is a prediction of the **net profit** or **revenue** attributed to the **entire future relationship** with a customer.

###  Why is CLV Important?

- **Retention Focus**: Helps prioritize long-term relationships over one-time purchases.
- **Marketing ROI**: Helps allocate marketing budgets based on customer value.
- **Customer Segmentation**: Enables segmentation into High/Medium/Low CLV groups.
- **Personalization**: Drives personalized offers and loyalty programs.
- **Business Valuation**: A core metric in estimating company worth and forecasting growth.

> In short, CLV tells you *how much a customer is worth* to your business over time.

---

##  Dataset Summary

- **Source**: [UCI Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)

---

##  Project Goals

- Clean and preprocess transactional data
- Calculate Recency, Frequency, and Monetary Value (RFM)
- Build a probabilistic CLV model using **BG/NBD + Gamma-Gamma**
- Evaluate model performance using MAE and RMSE

---

##  Data Cleaning Highlights

- Removed duplicates
- Filtered invalid/missing Customer IDs
- Detected and investigated **anomalies and extreme values**
  - e.g. `POSTAGE`, `PAPER CRAFT , LITTLE BIRDIE`, and bulk purchase outliers
- Verified that some high-value entries are likely valid due to wholesaler behavior

---

##  Feature Engineering

| Feature         | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `frequency`     | Number of time periods a customer made purchases (not total purchases)     |
| `recency`       | Time since first purchase to latest purchase                                |
| `T`             | Customer age — time from first purchase to end of observation window        |
| `monetary_value`| Average value of a customer's purchases (total spend ÷ number of purchases) |

---

##  Model Used

###  BG/NBD Model
Used to predict **expected number of future transactions**.

###  Gamma-Gamma Model
Used to predict **expected average transaction value**.

---

##  Model Performance

- **Mean Absolute Error (MAE)**: `~3.10`
- **Root Mean Squared Error (RMSE)**: `~10.53`

---

##  Key Insights

- High-CLV customers are mostly repeat buyers and often wholesalers.
- Certain products and customers heavily skew purchase amounts.
- Segmentation will help in tailoring marketing strategies to different customer groups.

---

##  Next Steps

- [ ] Segment customers using predicted CLV (e.g., high, medium, low)
- [ ] Visualize in Power BI / Matplotlib / Seaborn
- [ ] Export insights for marketing and sales strategy
- [ ] Deploy as a dashboard for business use

---

## ⚙ Tools & Libraries

- Python (pandas, NumPy, lifetimes)
- Jupyter Notebook



