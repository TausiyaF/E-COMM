# E-COMM
E-Commerce Sales Dashboard
Dashboard Pages

Sales Overview – KPIs: Sales, Profit, Orders, Customers

Sales by Category/Sub-Category – Tree map / bar chart

Monthly Sales & Profit Trend – Line chart

Top 10 Products by Sales – Bar chart

Customer Analysis – New vs Returning customers

SQL
SELECT Category, SUM(Sales) AS Total_Sales, SUM(Profit) AS Total_Profit
FROM Orders
GROUP BY Category;

-- Top 10 Products
SELECT TOP 10 ProductName, SUM(Sales) AS Total_Sales
FROM Orders
GROUP BY ProductName
ORDER BY Total_Sales DESC;

DAX
Total Sales = SUM(Orders[Sales])
Total Profit = SUM(Orders[Profit])
Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)
Total Orders = COUNTROWS(Orders)
Customer Count = DISTINCTCOUNT(Orders[CustomerID])
