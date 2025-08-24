# 📊 Superstore Sales Dashboard

## 📥 Data Source
- Directly imported from **Excel sheets** into Power BI  
- Data modeling and visualization performed inside **Power BI**  

---

## ⚙️ DAX Measures & Calculations

```dax
-- 📌 Average Delivery Time (calculated column)
AvgDelivery = 
DATEDIFF(
    'SuperStore_Sales_Dataset'[Order Date],
    'SuperStore_Sales_Dataset'[Ship Date],
    DAY
)

-- 📌 Sales Forecasting Table
Salesforecast = 
SUMMARIZE(
    'SuperStore_Sales_Dataset',
    'SuperStore_Sales_Dataset'[Order Date],
    "Total Sales", SUM('SuperStore_Sales_Dataset'[Sales])
)
```
## 📊 Dashboard Metrics

| **Metric**           | **Value** |
|-----------------------|-----------|
| Total Sales           | $22M      |
| Total Orders          | 22K       |
| Profit                | $175K     |
| Avg Delivery Time     | 4 Days    |

---

## 🔍 Key Insights

### 🏆 Sales Performance
- Total sales reached **$22M** with **22K orders**  
- Profit margin maintained at **$175K**  
- Average delivery time recorded at **4 days**  

### 🌍 Regional Analysis
- **California** leads with **$0.34M** sales  
- Followed by **New York** with **$0.19M**  

### 📈 Forecasting
- Implemented **Power BI Forecasting** feature  
- Forecasted **sales for the next 15 days**  
- Trend indicates **steady growth in sales**  
