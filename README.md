# 🛒 Retail Store Sales Analysis

**An interactive 4-page Power BI dashboard that turns a year of retail transactions into store, product, customer and management insights.**

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Excel](https://img.shields.io/badge/Excel-Data%20Prep-217346?logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success)

**Author:** Rajeshwari M J | **Domain:** Retail Analytics | **Period:** Jan 2025 – Dec 2025

---

## Contents

1. [Business Problem](#business-problem)
2. [Dataset](#dataset)
3. [Tools Used](#tools-used)
4. [Dashboard Pages](#dashboard-pages)
5. [Key Insights](#key-insights)
6. [Recommendations](#recommendations)
7. [DAX Measures](#dax-measures)
8. [Workflow](#workflow)
9. [How to Use](#how-to-use)
10. [Project Structure](#project-structure)
11. [Contact](#contact)

---

## Business Problem

A retail chain with 12 stores and 40 products needs one place to answer:

- How are sales and profit performing overall?
- Which stores, products and categories drive results, and which lag?
- Who are the customers and how do they pay?
- Where are returns hurting the business, and what should management do next?

## Dataset

| Item | Detail |
|---|---|
| Period | Jan 2025 – Dec 2025 |
| Stores | 12 (across multiple Indian states) |
| Products | 40, in 6 categories (Fashion, Electronics, Home, Beauty, Grocery, Stationery) |
| Customers | ~1,000 (Regular, New, Premium segments) |
| Orders | ~8,000 |
| Source | `[Add source, e.g. synthetic / Kaggle / company export]` |
| Size | `[Add rows × columns]` |

## Tools Used

| Tool | Purpose |
|---|---|
| Power Query | Data cleaning and transformation |
| Excel | Data preparation |
| DAX | KPIs and business measures |
| Power BI | Data model, visuals and navigation |

---

## Dashboard Pages

### 1. Executive Overview
High-level health of the business: monthly sales trend, sales by category, customer segments, store performance, top products, payment methods, profit vs sales and sales by state.

![Executive Overview](https://github.com/user-attachments/assets/b2ca33a2-a78e-429a-8cb0-6c23b983d11f)

### 2. Store & Product Analysis
Store-wise sales and profit, top 5 stores, top and bottom products, category performance and share, state-wise sales, payment methods and return rate by category.

![Store & Product Analysis](https://github.com/user-attachments/assets/ec569c92-c539-4444-9ed1-52b382da726c)

### 3. Customer Analysis
Segment sales and distribution, gender and age-group analysis, payment behaviour, orders by rating and a customer-level table.

![Customer Analysis](https://github.com/user-attachments/assets/c3c0c712-f099-42a5-8e4c-0be4549bca4e)

### 4. Management Action Center
Store ranking, performance matrix, category contribution, profit efficiency, sales drivers and a ranking measure that labels each store with a recommended action.

![Management Action Center](https://github.com/user-attachments/assets/89411300-f802-42ed-a5ea-b40539140c42)

---

## Key Metrics

| Metric | Value | Metric | Value |
|---|---:|---|---:|
| Total Sales | ₹17.00M | Total Stores | 12 |
| Total Profit | ₹7.15M | Total Products | 40 |
| Profit Margin | 42.08% | Total Returns | 460 |
| Total Orders | ~8K | Return Rate | 5.75% |
| Units Sold | ~15K | Average Order Value | ₹2.12K |
| Total Customers | ~1K | Premium Customers | 315 |

## Key Insights

- **Fashion leads categories** with ₹5.91M (34.8% of sales), followed by Electronics (28.7%) and Home (21.7%).
- **Running Shoes is the #1 product** (₹13.5L), followed by Casual Shoes and Wireless Earbuds.
- **Chennai Central is the top store** at ₹20.2L, about 19% ahead of #2 Mumbai Store.
- **Store margins are very close** (roughly 41.4% to 42.6%), so sales volume and returns separate stores more than profitability does.
- **UPI is the dominant payment method** at 42.2% of sales.
- **Regular customers are the largest segment** (about 57% of customers and the highest segment sales).
- **Home has the highest return rate** among categories; Stationery has the lowest.
- **Lowest-selling products** include Notebook, Biscuits Pack and Packaged Juice, all in Grocery/Stationery.

## Recommendations

1. **Scale what works in Chennai Central.** It leads on sales and has the lowest return rate among the top 4 stores (5.45%); document its practices and replicate them.
2. **Reduce Home returns.** Home has the highest return rate; review product descriptions, quality checks and packaging.
3. **Double down on Fashion and Electronics.** Together they generate over 63% of sales; protect stock of top products such as Running Shoes.
4. **Review low sellers.** Test bundles or promotions for Notebook and Biscuits Pack, or reduce their stock.
5. **Push UPI offers.** With 42% of sales on UPI, cashback tie-ups can lift conversion.
6. **Grow the Premium segment.** 315 premium customers are a base for loyalty and upsell campaigns.

---

## DAX Measures

Example measures used in the model (adjust table and column names to your model):

```DAX
Total Sales = SUM ( Sales[Total_Amount] )

Total Profit = SUM ( Sales[Profit] )

Profit Margin % = DIVIDE ( [Total Profit], [Total Sales] )

Return Rate % = DIVIDE ( [Total Returns], [Total Orders] )

Average Order Value = DIVIDE ( [Total Sales], [Total Orders] )

Store Sales Rank = RANKX ( ALL ( Stores[Store_Name] ), [Total Sales], , DESC )
```

## Workflow

```text
Raw Retail Data → Cleaning (Power Query) → Data Modeling → DAX Measures
                → Visualizations → Insights → Management Actions
```

## How to Use

1. Download or clone this repository.
2. Open `Retail Store Sales Analysis.pbix` in **Power BI Desktop**.
3. Use the left navigation panel to move between the 4 pages and click visuals to cross-filter.

`[Optional: add a link to the PDF export or the Power BI Service report]`

## Project Structure

```text
Retail-Store-Sales-Analysis/
├── Retail Store Sales Analysis.pbix
├── Dataset/
├── Screenshots/
└── README.md
```

## Contact

**Rajeshwari M J**
LinkedIn: `[your link]` | Email: `[your email]`

⭐ If you found this project useful, consider giving it a star.
