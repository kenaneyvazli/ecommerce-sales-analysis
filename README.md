# 📊 E-Commerce Sales Data Analysis & Cleaning

This project focuses on cleaning, processing, and analyzing raw e-commerce order data using Python. It demonstrates end-to-end Data Analyst workflows including data wrangling, handling anomalies/missing values, KPI calculation, exploratory data analysis (EDA), and business insights generation.

---

## 📌 Project Overview

The primary objective of this project is to transform uncleaned e-commerce transactional data (`ecommerce_practice_raw.csv`) into actionable business insights. The dataset includes order details, shipping costs, categories, regions, pricing, discounts, and payment methods.

### Key Highlights:
- **Data Wrangling:** Fixed mixed date formats, inconsistent text entries (`BAKU`, `baku`, trailing spaces), missing values, duplicates, and negative pricing anomalies.
- **Feature Engineering:** Calculated financial metrics like `gross_sales`, `discount_amount`, and `net_sales`.
- **KPI Analysis:** Evaluated total revenue, average order value (AOV), total units sold, and order status breakdown.
- **Data Visualization:** Built comparison bar charts, distributions, and monthly sales trends using `Matplotlib`.

---

## 🛠️ Tech Stack & Libraries

- **Language:** Python 3.x
- **Data Manipulation:** `pandas`, `numpy`
- **Data Visualization:** `matplotlib`
- **Environment:** Jupyter Notebook

---

## 🧹 Data Cleaning & Preprocessing Workflow

1. **Handling Missing Values:**
   - Filled missing `city` and `payment_method` with `"Unknown"`.
   - Replaced missing `discount` values with `0`.
2. **Text Standardization:**
   - Standardized region names using `.str.strip().str.title()` to clean entries like `BAKU` or `baku `.
3. **Data Anomaly Handling:**
   - Dropped duplicate order rows to prevent inflated metrics.
   - Filtered out unrealistic negative unit prices (`unit_price >= 0`).
4. **Date Parsing:**
   - Converted `order_date` to standard datetime format using `pd.to_datetime(..., format="mixed", dayfirst=True)` to preserve valid records.

---

## 📈 Key Metrics & Results

| Metric | Value |
| :--- | :--- |
| **Total Orders** | 23 |
| **Total Net Sales** | 2,127.90 AZN |
| **Average Order Value (AOV)** | 92.52 AZN |
| **Total Units Sold** | 93 |
| **Delivered Orders** | 20 |
| **Total Shipping Cost** | 115.00 AZN |

---

## 🔍 Key Business Insights

1. **Regional Performance:**  
   - **Baku** generates the highest net sales (**1,043.8 AZN**), followed by **Ganja** (**692.0 AZN**) and **Sumqayit** (**392.1 AZN**).
2. **Category Performance:**  
   - **Electronics** is the top-performing category (**1,148.0 AZN** net sales), while **Office** generates the lowest revenue (**224.4 AZN**).
3. **Monthly Trend:**  
   - Sales peaked in **February (1,235.3 AZN)** but dropped significantly in **March (146.0 AZN)**, indicating a potential seasonal slump or supply issues.

---

## 💡 Business Recommendations

* **Revamp Office Category:** Investigate product availability and promotional offers for Office supplies to improve its revenue contribution.
* **Investigate March Performance:** Conduct a deep dive into March order drop-offs across product availability, logistics, and marketing campaigns to prevent future seasonal declines.

---

## 📁 Repository Structure

```text
├── ecommerce_python_final_Kenan_eyvazli.ipynb    # Main Python analysis & visualizations
├── ecommerce_practice_raw.csv                     # Raw input dataset
└── README.md                                      # Project documentation
