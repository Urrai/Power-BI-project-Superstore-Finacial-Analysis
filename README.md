# Power-BI-project-Superstore-Finacial-Analysis
# 💸 DIY Financial Analysis Dashboard in Power BI
 this project helps you visualize, analyze, and optimize your finances using powerful KPIs and interactive visuals.

---

## 📊 Dashboard Features

- **Sales Tracker**: Monthly breakdowns, category-wise spending, and trends
- **Identifying the low and high performing product Goals**: Track progress toward short- and long-term Sales targets
- **KPI Cards**: Real-time financial health indicators
- **Smart Filters**: Time periods, categories, accounts, and custom tags etc

---

## 📈 Key Performance Indicators (KPIs)

These KPIs are calculated using DAX and visualized with Power BI cards, gauges, and trend lines:

| KPI Name              | Description                                      | Target Example     |
|-----------------------|--------------------------------------------------|--------------------|
| 💰 Sales Current Year vs Last Year | % Increase or decrease every Year                    | ≥ 20%              |
| 📉 Orders Current Year vs Last Year  | % Increase or decrease every Year                      | ≤ 70%              |
| 📈 Profit Current Year vs Last Year      | % Increase or decrease every Year       | ≥ 8% annually      |
| 🧾 Profit Margin Current Year vs Last Year    | % Increase or decrease every Year | ± 5%               |
| 🏦 Discount Current Year vs Last Year    | % Increase or decrease every Year            | Positive trend     |

You can customize these KPIs based on your financial goals and lifestyle.

---

## 🧠 DAX Measures (Examples)


```DAX

Top 3 Product By sales = CALCULATE([Sales Amount],TOPN(3,ALLSELECTED(financials[Product]),[Sales Amount],DESC),VALUES(financials[Product]))
Discount Offered LY = CALCULATE([Discount Offered],DATEADD('Date Table'[Date],-1,YEAR))


## 🧠 Screenshot

