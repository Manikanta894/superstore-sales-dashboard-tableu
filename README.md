<div align="center">

# 📊 Superstore Sales & Profitability Intelligence

### Two Tableau dashboards. One retail dataset. Zero guesswork.

[![Tableau](https://img.shields.io/badge/Built%20with-Tableau%20Public-E97627?logo=tableau&logoColor=white)](https://public.tableau.com)
[![Dataset](https://img.shields.io/badge/Dataset-Sample%20Superstore-2ea44f)](data/superstore.csv)
[![Orders](https://img.shields.io/badge/Orders-5%2C111-blue)](#-overview)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**[🖥️ Sales Performance Terminal](https://public.tableau.com/app/profile/manikanta.r3244/viz/SALESPERFORMANCETERMINAL/Dashboard1)** · **[💰 Profitability Dashboard](https://public.tableau.com/app/profile/manikanta.r3244/viz/PROFITABILITY_17856991490550/PROFITABILITY)**

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Dashboard 1 — Sales Performance Terminal](#️-dashboard-1--sales-performance-terminal)
- [Dashboard 2 — Profitability](#-dashboard-2--profitability)
- [Key Findings](#-key-findings)
- [Data Dictionary](#-data-dictionary)
- [Repo Structure](#️-repo-structure)
- [Tech Stack](#-tech-stack)
- [How to Explore](#-how-to-explore)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📌 Overview

A two-dashboard Tableau project analyzing a full year of retail superstore transactions — built to answer one question executives always ask: **"We have sales. Are we actually making money?"**

| Metric | Value |
|---|---|
| 💵 Total Sales | ₹23,26,534.35 |
| 📈 Total Profit | ₹2,92,296.81 |
| 📊 Profit Margin | 12.56% |
| 🧾 Orders | 5,111 |
| 👥 Customers | 804 |
| 🗺️ States Covered | 59 |
| 🏙️ Cities Covered | 542 |
| 📦 Sub-Categories | 17 |

---

## 🖥️ Dashboard 1 — Sales Performance Terminal

A terminal-style command center — dark theme, green-on-black readouts — for tracking sales KPIs across category, region, segment, state, and city.

![Sales Performance Terminal](images/sales-performance-terminal.png)

**What it shows:**
- Headline KPIs: **Sales**, **Profit**, **Profit Margin %**
- Category × Region heatmap grid
- Monthly sales trend line
- Sales by Category, and Category × Segment breakdown
- Geographic drill-down — Sales by State and Sales by City

---

## 💰 Dashboard 2 — Profitability

The follow-up question dashboard: sales tell you *what* sold, this tells you *whether it was worth selling*.

![Profitability Dashboard](images/profitability-dashboard.png)

**What it shows:**
- Total profit by category — Technology, Furniture, Office Supplies
- Combined Profit & Sales trend over the year
- Profit-vs-Sales scatter (spotting outliers by category)
- Profit distribution / count histogram
- Category profit ranking (Gantt-style bars)

---

## 🧠 Key Findings

> The headline numbers hide a much messier story underneath. Here's what actually stood out digging into the data:

- 🥇 **Technology wins on every axis** — highest sales (₹8,39,893.28) *and* highest profit (₹1,46,543.38). It's the category to double down on.
- 🪑 **Furniture is a trap** — solid sales (₹7,54,747.76) but the *weakest* profit of the three categories by far (₹19,730 total). Worse: **Central region Furniture is outright unprofitable** (–₹2,802.21).
- 🪑📉 **Tables and Bookcases are bleeding money** — Tables lost **–₹17,753.21** and Bookcases lost **–₹3,632.07**, despite ₹2L+ and ₹1.1L in sales respectively. This is almost certainly a discounting problem, not a demand problem.
- 🖨️ **Copiers are the hidden gem** — only ₹1.5L in sales but ₹56,093.94 in profit, the best profit-per-sale ratio of any sub-category.
- 🌎 **West leads, Central lags** — West posts the best sales-to-profit ratio; Central is the weakest region across the board.
- 🏷️ **Discounting is aggressive** — average discount is ~15.5%, with a quarter of all orders discounted at 20%+ and some as high as 80%. This lines up almost exactly with which sub-categories are losing money.
- 🛒 **Consumer segment dominates** — ₹11.7L in sales and ₹1.36L in profit, more than Corporate and Home Office combined.
- 🌴 **California and New York are the sales engines** — ₹4.58L and ₹3.11L respectively, nearly 2× the next closest state (Texas).

**Bottom line:** growth isn't the problem — *discipline on discounting in Furniture (especially Tables and Bookcases)* is where the next margin points are hiding.

---

## 📖 Data Dictionary

The dataset (`data/superstore.csv`) contains 10,194 line items with the following fields:

| Column | Description |
|---|---|
| `Row ID` | Unique row identifier |
| `Order ID` | Order identifier (one order can span multiple rows) |
| `Order Date` / `Ship Date` | Order and fulfillment dates |
| `Ship Mode` | Standard / Second / First Class / Same Day |
| `Customer ID` / `Customer Name` | Customer identifiers |
| `Segment` | Consumer / Corporate / Home Office |
| `Country/Region`, `City`, `State/Province`, `Postal Code`, `Region` | Geography |
| `Product ID`, `Category`, `Sub-Category`, `Product Name` | Product hierarchy |
| `Sales` | Line-item revenue |
| `Quantity` | Units sold |
| `Discount` | Discount rate applied (0–0.8) |
| `Profit` | Line-item profit (can be negative) |

---

## 🗂️ Repo Structure

```
.
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── .gitignore
├── .github/
│   └── ISSUE_TEMPLATE.md
├── data/
│   └── superstore.csv          # Full source dataset
└── images/
    ├── sales-performance-terminal.png
    └── profitability-dashboard.png
```

---

## 🛠️ Tech Stack

- **Tableau Public** — dashboard design, calculated fields, and publishing
- **Sample Superstore dataset** — orders, sales, profit, and discount data
- **Markdown** — this very README 🙂

---

## 🚀 How to Explore

1. Click the live Tableau Public links at the top to interact with both dashboards — filter by region, category, or segment, and drill into individual states and cities.
2. Or clone this repo and open `data/superstore.csv` directly in Tableau, Excel, or Python/pandas to explore the raw numbers yourself.

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

---

## 🤝 Contributing

Suggestions and improvements are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md) for how to open an issue or PR.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE). The underlying dataset is the publicly available Sample Superstore dataset, used here for educational/portfolio purposes.

---

<div align="center">
Built by <a href="https://public.tableau.com/app/profile/manikanta.r3244">Manikanta R</a> on Tableau Public
</div>
