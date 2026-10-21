# 🥐 Bakery Sales & Inventory Analytics

An end-to-end data analysis and inventory optimization project evaluating transactional bakery data, customer purchasing behaviors, waste costs, and promotion strategies.

---

## 📌 Project Overview

Bakery and perishable retail operations face a constant trade-off between product availability and spoilage costs. This project analyzes retail transaction logs across weather patterns, customer demographics, and production batches to:

- Quantify sales performance and net profit across product categories.
- Evaluate shelf-life constraints, spoilage risk, and waste cost impacts.
- Measure the effectiveness of promotional discounts and customer loyalty programs.
- Model recommendations for inventory stock planning and dynamic discounts.

---

## 📊 Dataset Schema

The dataset comprises granular transaction-level records enriched with operational, temporal, and inventory metrics:

| Category | Columns |
| :--- | :--- |
| **Transaction & Order** | `transaction_id`, `date`, `time`, `product`, `category`, `quantity`, `unit_price`, `selling_price`, `total_bill`, `payment_method` |
| **Customer Profile** | `customer_id`, `customer_age`, `customer_gender`, `customer_segment`, `loyalty_member`, `customer_rating` |
| **Discounts & Promotions** | `discount_percentage`, `discount_amount`, `promotion_applied`, `promotion_type`, `promotion_score`, `recommended_discount` |
| **Time & Environment** | `day_of_week`, `weekend`, `season`, `festival`, `weather`, `temperature` |
| **Store & Operations** | `store_id`, `employee_id` |
| **Inventory & Shelf-Life** | `manufacturing_date`, `expiry_date`, `shelf_life_days`, `stock_available`, `units_produced`, `units_sold`, `unsold_units`, `expiry_risk` |
| **Financials & Output** | `profit`, `waste_cost`, `recommended_product` |

---

## 🛠 Tech Stack

- **Language:** Python 3.11+
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Development Environment:** Jupyter Notebook / VS Code

---

## 🔍 Key Analysis & Focus Areas

### 1. Financial Performance & Profitability
- **Net Profit vs. Waste Cost:** Comparison of gross margin against losses incurred from unsold inventory and expired goods (`waste_cost`).
- **Revenue by Category:** Identification of top-performing bakery categories (e.g., Artisan Breads, Pastries, Savory Items).

### 2. Spoilage & Inventory Optimization
- **Expiry Risk Assessment:** Analysis of `shelf_life_days` against sales velocity (`units_sold` vs. `unsold_units`).
- **Production Efficiency:** Measuring variance between `units_produced` and consumer demand across individual `store_id` locations.

### 3. Customer Demographics & Behavior
- **Segmentation:** Spending behavior across `customer_segment` (e.g., Regular, Occasional, VIP) and `loyalty_member` status.
- **Rating Distributions:** Correlation between discount satisfaction, wait times/shelf-life freshness, and `customer_rating` (1–5).

### 4. Promotion & External Factor Impacts
- **Weather & Seasonality:** Impact of `weather`, `temperature`, `season`, and `festival` events on daily footfall and basket sizes.
- **Discount Elasticity:** Analyzing whether higher `discount_percentage` drives net positive `profit` or merely erodes margin.

---

## 📁 Repository Structure

```text
├── data/
│   └── bakery_sales_data.csv       # Raw or processed transaction dataset
├── notebooks/
│   └── bakery_analytics.ipynb      # Main EDA and analytics notebook
├── assets/
│   └── figures/                    # Exported plots and charts
├── requirements.txt                # Python environment dependencies
└── README.md                       # Project documentation