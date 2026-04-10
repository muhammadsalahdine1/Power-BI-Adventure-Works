# Power-BI-Adventure-Works

### Profit column
- Adventure Works Cycles have just started their Power BI journey and would like to understand their yearly profitability.
- In the Sales table, we would like to create a column to see how much profit we gained from each order line.
- To calculate profit, we need to subtract the line cost from the line price.
- Create a new column in the Sales table called Profit that subtracts line cost from line price.
- In the Report view, create a Clustered column chart that shows the sum of Profit for each order year.
- Add OrderDate on the X-axis and Profit field as the Y-axis.
- Make sure the sum aggregation is selected in the dropdown menu after clicking the arrow next to Profit in the Visualizations pane.
- How much profit did Adventure Works Cycles generate in 2019?
<div>
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/1.PNG" width="500">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/2.PNG" width="500">
<\div>

### Sales count
- we created a calculated column to find the profit for each transaction.
- Now, we will be utilizing a count function to understand the general trend of orders since Adventure Works started operating.
- Create a new measure SalesCount inside the _Calculations table which uses the DISTINCTCOUNT() function on the column that contains order numbers(OrderNo).
- Create a Line chart to show the SalesCount by Order Date hierarchy.
- In which month year do we see our largest number of orders?
<div>
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/3.PNG" width="500">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/4.PNG" width="500">
<\div> 

### Profit margin ratio
- The profit margin ratio compares the total profit to the total sales.
- It's an important financial metric and it's always expressed as a percentage.
- I will create a measure to represent the profit margin ratio.
- TotalSales has already been calculated for , but we need Total Profit. Luckily, in an earlier , we created a Profit column that we can use to make our Total Profit measure.
- There are two ways to calculate this, one way is by using DIVIDE()
- Create a TotalProfit measure inside the _Calculations table, which takes the sum of all the profit.
- Create a measure called ProfitMarginRatio which divides TotalProfit by TotalSales inside the _Calculations table.
- Create a Line chart to visualize the ProfitMarginRatio by Order Year.
- In which year did Adventure Works achieve the highest profit margin ratio?
<div>
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/5.PNG" width="300">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/6.PNG" width="300">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/7.PNG" width="300">
<\div> 

