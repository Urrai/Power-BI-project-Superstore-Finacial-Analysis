# Power-BI-project-Superstore-Finacial-Analysis
# 💸 DIY Financial Analysis Dashboard in Power BI
 this project helps you visualize, analyze, and optimize your finances using powerful KPIs and interactive visuals.

---

## 📊 Dashboard Features

- **Income & Expense Tracker**: Monthly breakdowns, category-wise spending, and trends
- **Savings Goals**: Track progress toward short- and long-term savings targets
- **Investment Performance**: ROI, asset allocation, and growth trends
- **Net Worth Monitor**: Assets vs. liabilities over time
- **KPI Cards**: Real-time financial health indicators
- **Smart Filters**: Time periods, categories, accounts, and custom tags

---

## 📈 Key Performance Indicators (KPIs)

These KPIs are calculated using DAX and visualized with Power BI cards, gauges, and trend lines:

| KPI Name              | Description                                      | Target Example     |
|-----------------------|--------------------------------------------------|--------------------|
| 💰 Monthly Savings Rate | % of income saved each month                    | ≥ 20%              |
| 📉 Expense Ratio       | Expenses as % of income                         | ≤ 70%              |
| 📈 Investment ROI      | Return on investment over selected period       | ≥ 8% annually      |
| 🧾 Budget Variance     | Difference between planned vs. actual spending  | ± 5%               |
| 🏦 Net Worth Growth    | Change in net worth month-over-month            | Positive trend     |
| 🎯 Goal Completion     | % of savings goal achieved                      | ≥ 100%             |

You can customize these KPIs based on your financial goals and lifestyle.

---

## 🧠 DAX Measures (Examples)

```DAX
MonthlySavingsRate = 
DIVIDE(
    SUM(Finance[Amount]),
    CALCULATE(SUM(Finance[Amount]), Finance[Type] = "Income")
)

ExpenseRatio = 
DIVIDE(
    CALCULATE(SUM(Finance[Amount]), Finance[Type] = "Expense"),
    CALCULATE(SUM(Finance[Amount]), Finance[Type] = "Income")
)

NetWorth = 
SUM(Assets[Value]) - SUM(Liabilities[Value])
