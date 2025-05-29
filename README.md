# Northwind Traders Sales & Operational Performance Analysis

# 𝗣𝗿𝗼𝗷𝗲𝗰𝘁 𝗢𝘃𝗲𝗿𝘃𝗶𝗲𝘄:
Northwind Traders, a global gourmet food distributor, sought to leverage data for improved sales, product management, and operational efficiency. As part of the Maven Analytics Power BI Challenge, I developed an interactive Power BI dashboard solution to provide actionable insights from their transactional data.


# Problem Statement/Objective:
The primary objective was to transform Northwind Traders' raw transactional data which consists of multiple tables viz Category, Customer, Date, Employees, Managers, Order_details, Orders, Products, Shippers into a comprehensive business intelligence tool. This involved analyzing sales performance, identifying key product and customer trends, and assessing operational metrics (e.g., order fulfillment, shipping costs) to enable data-driven strategic planning and decision-making for sustainable growth.


# What I did:

Data Acquisition & Transformation: Loaded and transformed raw data using Power Query, ensuring data quality and readiness for analysis.

Data Modeling: Established relationships between various tables (e.g., Orders to Order Details, Products to Categories) to create a robust analytical model. Image of the Data modelling is attached.

DAX Measures Development: Created multiple DAX measures for key performance indicators (KPIs) such as Sales in CY, YoY Sales Growth, Freight Cost, Avg Order Value, CPO (Cost Per Order), On-Time Delivery Rate, Repeat Purchase Rate, and Product Profitability.

Dashboard Design & Visualization: Designed two interconnected, user-friendly, and visually appealing dashboards (Sales Performance Dashboard & Operational Performance Dashboard), incorporating various Power BI visuals to convey insights effectively.

Insights Generation: Analyzed sales trends, product and customer performance, and operational metrics to derive actionable business insights and recommendations.

# Key Visualizations & Insights:

Dashboard 1:Sales Performance Overview

1. Year Slicers (2013, 2014, 2015):

Purpose: To enable quick year-over-year comparison and focus on specific periods.

Key Insight(s): These slicers provide immediate control over the data's timeframe, essential for historical analysis and tracking annual performance metrics. Beneficial for interactivity and flexible data exploration.

2.Key Performance Indicators (KPIs) :

Sales in CY ($440,624), Sales PYTD ($453,187) & YoY% (53%):

Description: Card visuals showing current year's sales, Previous year to date Sales and its year-over-year growth.

Purpose: To provide a quick pulse check on overall revenue performance and growth trajectory.

Insight: Current sales figures are robust, with a significant 53% YoY growth, indicating strong business expansion.

Freight Cost in CY ($64,943), Freight PYTD ($22,410) & YoY% (52%):

Description: Card visuals for current and previous year's freight costs and its year-over-year change.

Purpose: To track logistical expenses.

Insight: Freight costs are tracking closely with sales growth (52% YoY), suggesting efficient scaling of logistics with sales volume. It's important to monitor this to ensure it doesn't outpace revenue growth.

Orders in CY (830), YOY Revenue($453,187) & YoY% (2%):

Description: Card visuals for current year's total orders, its year-over-year revenue and  growth.

Purpose: To understand customer order volume.

Insight: While sales revenue shows strong growth, the relatively lower 2% YoY growth in order count suggests an increase in average order value or price per item, rather than just more individual orders. This implies successful upselling or higher-value product purchases.

Technical Details for all KPIs:  DAX measures were created for current year values, PYTD and YoY %.

3.Column Charts: MOM Sales across Year, MOM Freight Cost across Year & MOM Orders count across Year:

Description: Column charts showing month-over-month trends for sales, freight cost, and order count.

Purpose: To visualize monthly fluctuations, seasonality, and consistency in key financial and operational metrics.

Insight: These charts allow for detailed monthly trend analysis. For instance, peaks and troughs in sales can highlight seasonality, guiding inventory and marketing planning. Similar trends in freight cost indicate efficient logistics tied to sales volume.

Technical Details: These charts utilize Sales, Freight Cost , and Orders measures against a month-year hierarchy in axis and in legend.

4.Bar Charts: Top Product by Sales, Most Costly Products, Most Ordered Products:

Description: Horizontal bar charts identifying top performers based on different metrics.

Purpose: To pinpoint high-value products from sales, cost, and popularity perspectives.

Insight:
"Top Product by Sales: 'Côte de Blaye' ($141.40K) is a dominant revenue generator, indicating strong market demand or a high-price point. This product should be a focus for inventory and marketing."

"Most Costly Products: 'Côte de Blaye' ($203.50) is the highest in terms of cost. This indicates the total value of this product in inventory, not necessarily its profitability without further analysis."

Most Ordered Products: 'Camembert Pierrot' (1577 orders) is also the most ordered product. Its high order volume suggests it's a staple for customers. This demand is vital for inventory management.

Technical Details: These charts use appropriate measures (Sales, Freight, Orders) with Top 10 filters applied to product names.


5.Bar Charts: Top Customers by Sales value, Highest Cost Customers, Top Customers by Sales quantity:

Description: Horizontal bar charts for customer analysis.

Purpose: To identify key customer accounts based on their revenue contribution, associated freight costs, and order quantity.

Insight:
Top Customers by Sales value: 'QUICK-Stop' ($110,277) is the leading customer by revenue, highlighting the importance of key account management and customer retention strategies.

Highest Cost Customers: 'QUICK-Stop' also appears as the highest cost customer(110277.31), which is expected to given its high sales volume. This is a point to monitor for profitability if freight costs are disproportionately high for this customer.

Top Customers by Sales Quantity:  'Save-a-lot' Markets (4958) leads significantly in sales quantity, closely followed by 'Ernst Handel' (4543) and 'QUICK-Stop' (3961). This concentration of high-volume shows the importance for inventory planning and logistical efficiency.

Technical Details: Bar charts with 'Top 10' filters, utilizing measures for sales, order cost, and sales quantity, sliced by customer name.


Dashboard 2: Product & Operational Performance

1. Key Performance Indicators (KPIs) :

CPO (Cost Per Order): The average cost per order is $78, a key operational metric to monitor for efficiency.

Avg Order Value: The average order value is $587, reinforcing the idea that higher average transaction sizes contribute to revenue growth even with fewer orders.

Discontinued Products (8): Currently, 8 products are discontinued. This number is critical for inventory management and product lifecycle planning.

Total Product Count (77): Northwind Traders manages a total of 77 products, providing context for the product profitability analysis.

Technical Details: DAX measures calculated for CPO & Average order value.

2. Matrix Visual: Product Profitability:

Description: A matrix showing the profitability (or unprofitability) of specific products.

Purpose: To identify which products are generating profit and which are incurring losses.

Insight: This matrix is crucial for product portfolio management. Products like 'Sasquatch Ale' and 'Spegesild' show negative profitability, indicating potential issues possibly with pricing, cost of goods, or sales volume. This demands immediate attention for reconsiderations.

Technical Details: This involves a calculated measure for Product Profitability  and breaking it down by Product Name.

3. Line Chart: Average Order Fulfillment Time across Year:

Description: Line chart showing the average time taken to fulfill orders over time.

Purpose: To track operational efficiency and identify trends in order processing.

Insight: The fulfillment time appears to fluctuate, with some spikes (e.g., Mar 2015, Jan 2015) indicating potential high demand periods. A general slight increase over time might suggest a need for process optimization as the business scales.

Technical Details: DAX measure calculating the order fulfillment time using difference between OrderDate and ShippedDate.

4. Gauge Chart: On-Time Delivery Rate (95.54%)

Description: A visual indicating the percentage of orders delivered on time.

Purpose: A critical operational KPI for customer satisfaction and supply chain efficiency.

Insight: A high on-time delivery rate of 95.54% is excellent, indicating strong logistical performance and high customer satisfaction. This is a key strength for Northwind Traders.

Technical Details:  DAX measure calculating the percentage of orders delivered where ShippedDate is before or on RequiredDate and Gauge chart is used to visualize the same.

5. Map Visual: Sales by Country (Global Distribution)

Description: A world map displaying sales volume by country.

Purpose: To visualize geographical sales distribution and identify key markets.

Insight: The map clearly shows a strong presence in North America and Europe, with larger bubbles indicating higher sales volumes. This confirms the primary markets and suggests potential for expansion in untapped markets.

Technical Details:  Power BI map visual is used, using Sales measure against Country geographical data.

6. Line Chart: Shipping Cost Trend:

Description: A line chart showing the trend of shipping costs over time.

Purpose: To monitor the efficiency and cost-effectiveness of shipping operations.

Insight: The shipping cost trend generally aligns with sales trends, showing peaks and troughs. The significant rise towards Jan 2015 might indicate increased shipping volume or rising carrier costs, requiring further investigation to optimize logistics.

Technical Details: Plots Freight Cost measure against ShippedDate.

7. Gauge: Repeat Purchase Rate (98.88%)

Description: A visual showing the percentage of customers who made repeat purchases.

Purpose: A crucial customer loyalty metric.

Insight:  An exceptionally high repeat purchase rate of 98.88% indicates outstanding customer loyalty and satisfaction. This is a massive strength for Northwind Traders and a testament to their product quality or service.

Technical Details: DAX measure is calculated to analyse the percentage of unique customers who have placed more than one order.

8. Stacked Bar Chart: Employee Performance:

Description: A stacked bar chart showing sales, no. of successful orders completed, no. of products sold as %Gt(Percent of Grand Total) attributed to each employee as their performance .

Purpose: To assess individual employee performance and identify top performers or areas for training.

Insight:  This visual allows for evaluating individual employee contributions. For example, 'Margaret Peacock' and 'Janet Leverling' appear to be strong performers, while others might need coaching or have different performance metrics."

Technical Details:  %GT of OrderID, Sales, ProductID as measures is put in axis and broken down by Employee name. DAX used to calculate these measures.

9. Donut Chart: Sales by product category:

Description: A donut chart showing the percentage contribution of different product categories to total sales.

Purpose: To understand the distribution of sales across product categories.

Insight:  Beverages and Dairy Products dominate sales (27.79% and 24.33% respectively), while other categories like Confections (17.36% ) also contribute significantly. This informs inventory management and marketing focus for different categories.

Technical Details: Utilizes a Sales measure sliced by Category Name.
