# Inventory-Analysis

# Performed the following challenges:
- Data check
- Explore Data
- Analyze and Visualize
- Dashboarding

# Performed DAX calculations:
- ABC Class
  - ABC_class = IF(ABC[CP_revenue]<=70, "A [High Value]", IF(ABC[CP_revenue]<=90, "B [Medium Value]", "C [Low Value]"))
- CP Revenue
  - CP_revenue = CALCULATE(
    SUM(ABC[percent_revenue_2021]), 
    FILTER(ABC,
    ABC[percent_revenue_2021]>=EARLIER(ABC[percent_revenue_2021])))
- Rank
  - Rank = RANKX(ABC, ABC[percent_revenue_2021])
- COGS Revenue Ratio
  - COGS_Revenue_Ratio = Stock[Total_COGS_2021]/Stock[Revenue_2021]
- Percent Revenue 2020
  - percent_revenue_2020 = Stock[Revenue_2020] / SUM(Stock[Revenue_2020]) *100
- Percent Revenue 2021
  - percent_revenue_2021 = Stock[Revenue_2021] / SUM(Stock[Revenue_2021]) *100
- Profit 2020
  - Profit_2020 = Stock[2020_units_sold]*Stock[Price.Retail_Price] - Stock[2020_units_sold]*Stock[Costs.COGS]
- Quantity 2021
  - Quantity_2021 = CALCULATE(SUM(Orders[Quantity]), FILTER(Orders, Stock[SKU-ID]=Orders[SKU] && Orders[Year]=2021))
- Quantity 2022
  - Quantity_2022 = CALCULATE(SUM(Orders[Quantity]), FILTER(Orders, Stock[SKU-ID]=Orders[SKU] && Orders[Year]=2022))
- Revenue 2020
  - Revenue_2020 = Stock[2020_units_sold]*Stock[Price.Retail_Price]
- Revenue 2021
  - Revenue_2021 = Stock[Quantity_2021]*Stock[Price.Retail_Price]
- Total COGS 2021
  - Total_COGS_2021 = Stock[Costs.COGS]*Stock[Quantity_2021]
- Total Orders
  - Total_Orders = CALCULATE(SUM(Orders[Quantity]), FILTER(Orders, Stock[SKU-ID]=Orders[SKU]))
- 2021 End Stock
  - 2021_end_stock = Turnover[2021_start_stock] - Turnover[Quantity_2021]
- Average Inventory
  - Avg_inventory = (Turnover[2021_start_stock] + Turnover[2021_end_stock]) * Turnover[COGS] / 2
- Inventory Turnover
  - Inventory_Turnover = Turnover[COGS]*Turnover[Quantity_2021]/Turnover[Avg_inventory]



# Dashboards
- Preparing Data
![24k5rkms vay](https://github.com/MarcvWaes/Inventory-Analysis/assets/120553175/88579508-1f45-45e1-9595-8640ae8882c8)

- COGS, Revenue and Profit
![f3tjzclr trv](https://github.com/MarcvWaes/Inventory-Analysis/assets/120553175/c0d44aab-f772-4ed8-a29b-a1c25e975ccd)

- Sales by Year
![kc5ezhon lsv](https://github.com/MarcvWaes/Inventory-Analysis/assets/120553175/47df6674-9c16-4d9b-96c2-21f39d5ab5c8)

- Revenue and class 
![gaabtwja ftz](https://github.com/MarcvWaes/Inventory-Analysis/assets/120553175/03179e1a-9b64-4eb7-9c90-97712c3f7ac3)

- Preliminary Results
![u0g3043j xew](https://github.com/MarcvWaes/Inventory-Analysis/assets/120553175/03719886-f299-4dcb-ba1c-a782bd852d7c)

- Smart Purchasing
![bp0vc35e y5x](https://github.com/MarcvWaes/Inventory-Analysis/assets/120553175/5b7d34a7-8073-464c-8dbd-6a898d4f44cf)

- Inspecting Categories
![osxzny10 uxs](https://github.com/MarcvWaes/Inventory-Analysis/assets/120553175/7a0c888f-0663-4550-a19a-cc0f3b44a1c8)

- Control Decisions
![tlwop3li zeb](https://github.com/MarcvWaes/Inventory-Analysis/assets/120553175/bfdc140b-99a3-45f2-bf87-f10404a687e4)

- Management Solutions
![3ghuqyv2 w33](https://github.com/MarcvWaes/Inventory-Analysis/assets/120553175/ce451a96-4076-451c-a5f1-519650bf4015)
