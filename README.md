# 🛍️ Customer Shopping Behavior Analysis

## 📌 Overview
This project analyzes customer shopping behavior using transactional retail data to uncover insights into **spending patterns, customer segmentation, and subscription trends**. The goal was to guide strategic business decisions around retention, discounting, and targeted marketing through a complete end-to-end data analytics workflow — from raw data to an executive-ready dashboard.

---

## 📊 Dataset
- **Size:** 3,900 rows × 18 columns
- **Features:**
  - **Demographics:** Age, Gender, Location, Subscription Status
  - **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color
  - **Shopping Behavior:** Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type
- **Data Quality:** 37 missing values identified in the `Review Rating` column

---

## 🛠️ Tools & Technologies
| Category | Tools Used |
|---|---|
| **Programming** | Python (Pandas, NumPy) |
| **Database** | MySQL / PostgreSQL |
| **Visualization** | Power BI |
| **Presentation** | Gamma |
| **Environment** | Jupyter Notebook |

---

## 🔄 Steps

### 1️⃣ Data Loading & Exploration (Python)
- Loaded dataset using Pandas
- Explored structure with `df.info()` and summary statistics with `.describe()`

### 2️⃣ Data Cleaning & Feature Engineering
- Imputed missing `Review Rating` values using category-level medians
- Standardized column names to snake_case
- Engineered new features: `age_group`, `purchase_frequency_days`
- Checked redundancy between `discount_applied` and `promo_code_used`; dropped the redundant column
- Loaded cleaned dataset into MySQL for further analysis

### 3️⃣ SQL Analysis
Answered 10 key business questions using SQL, including:
- Revenue comparison by gender
- High-spending customers who used discounts
- Top 5 products by average review rating
- Purchase amount comparison across shipping types
- Subscriber vs. non-subscriber spend and revenue
- Most discount-dependent products
- Customer segmentation (New, Returning, Loyal)
- Top 3 products per category
- Relationship between repeat purchases and subscription status
- Revenue contribution by age group

### 4️⃣ Dashboard (Power BI)
Built an interactive dashboard featuring:
- KPI cards: Number of Customers, Average Purchase Amount, Average Review Rating
- Subscription status breakdown (%)
- Revenue and sales by category
- Revenue and sales by age group
- Slicers for gender, category, and shipping type

### 5️⃣ Reporting & Presentation
- Compiled findings into a written analytical report
- Built a stakeholder-ready presentation deck using **Gamma**

---

## 📈 Key Results
- 💰 Male customers generated **~2x the revenue** of female customers ($157,890 vs. $75,191)
- 🔁 Non-subscribers accounted for **73% of total revenue**
- ⭐ **80% of customers** fall into the "Loyal" segment
- 🏷️ Top discount-dependent products (Hat, Sneakers, Coat) had discount rates near **48–50%**
- 📊 Young Adults were the highest-revenue age group

---

## 💡 Business Recommendations
- **Boost Subscriptions** — promote exclusive subscriber benefits
- **Customer Loyalty Programs** — reward repeat buyers to convert them into Loyal segment
- **Review Discount Policy** — balance sales growth with margin control
- **Product Positioning** — highlight top-rated and best-selling products in campaigns
- **Targeted Marketing** — focus on high-revenue age groups and express-shipping users

---

## ▶️ How to Run
1. Clone this repository
2. Install required Python packages:
```bash
   pip install pandas numpy sqlalchemy mysql-connector-python
```
3. Run the data cleaning and EDA notebook:
```bash
   jupyter notebook customer_shopping_behavior_analysis.ipynb
```
4. Set up a local MySQL database and update connection credentials
5. Run SQL scripts in `/sql` to reproduce business analysis queries
6. Open `customer_behavior_dashboard.pbix` in Power BI Desktop to explore the dashboard
7. See `/report` for the written analysis and `/presentation` for the Gamma deck

---

## 📁 Project Structure

├── data/
│ └── customer_shopping_behavior.csv
├── notebooks/
│ └── customer_shopping_behavior_analysis.ipynb
├── sql/
│ └── customer_behaviour_project.sql
├── dashboard/
│ └── customer_behavior_dashboard.pbix
├── report/
│ └── Customer Shopping Behavior Analysis.pdf
├── presentation/
│ └── Customer-Shopping-Behavior-Analysis.pdf
└── README.md

**MANASWINI.D** — Data Analyst 
