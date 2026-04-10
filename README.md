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

### Using variables
- Since they started trading, Adventure Works has never increased prices even when inflation has risen.
- The leadership team would like to understand what total sales would look like had they taken into consideration inflation when they first started trading.
- Create a new measure called "TotalSales_w_increase".
- For the measure, define a variable called "Increase" and set it to 5% (0.05).
- In the return statement of the variable, calculate the total sales, and add the 5% increase of the total sales, like this: 'Calculations'[TotalSales] + ('Calculations'[____] * increase)
- In the Report view, create two Card visuals that show TotalSales and TotalSales_w_increase.
- What is the new total sales with the 5% increase applied?
<div>
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/8.PNG" width="500">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/9.PNG" width="500">
<\div>  


### Iterator functions
- Iterator functions are very useful for running calculations without the need to create calculated columns. 
- I will be comparing the output of a AVERAGE() vs. AVERAGEX().
- Create a new measure AvgProfit which calculates the average of all the profit.
- Create a new measure called AvgProfit_x that uses the AVERAGEX() function to subtract line cost from line price.
- Create a Clustered column chart that shows AvgProfit and AvgProfit_x.
<div>
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/10.PNG" width="300">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/11.PNG" width="300">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/12.PNG" width="300">
<\div>  


### Sales by category and year
- In previous, I've calculated revenue by using a SUM() function to total the LinePrice column.
- Now I'll need to calculate the total sales and filter by category Bikes and order year 2018.
- I will be utilizing the CALCULATE() function.
- Create a measure called 2018 Bikes Revenue which calculates the sum of line price and filters on the product category "Bikes" and YEAR(Sales[OrderDate]) year being 2018.
- Create a Card visual that shows your new measure 2018 Bikes Revenue.
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/13.PNG" width="1000">


### Expanding the Date table
- A Date table has already been created using the CALENDAR() function that takes in two arguments.
- For our Date table, we have generated dates from the first order date to the latest order date.
- Some columns have already been created, but we are going to expand on this by creating new columns using date and text functions to work out which day of the week a particular day is.
- Create a new column in the Dates table called DayNo that uses the DAY() function to calculate the day number in the month.
- Use Dates[Date] for this new column.
- Create a new column in Dates called DayShortName that uses FORMAT() with Dates[Date] to return the 3 letter short name for days ("ddd").
- In the Report view, create a Table that shows Date (without hierarchy) and DayShortName.
<div>
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/14.PNG" width="300">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/15.PNG" width="300">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/16.PNG" width="300">
<\div>


### DATEDIFF
- Adventure Works would like to understand the timeline from customers making an order to the delivery being due. 
- We'll be utilizing the DATEDIFF() function to calculate the difference.
- Create a new column in the Sales table called Order2Delivery that calculates the number of days between Order Date and Delivery Due Date.
- Create a Card visual that shows the average of Order2Delivery.
<div>
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/17.PNG" width="500">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/18.PNG" width="500">
<\div>


###  Quick measure
- Create a new quick measure that calculates quarter-over-quarter change for TotalSales over one period.
- Select Quick Measure from the Home Ribbon which will return a number of calculations to choose from. Navigate to Time Intelligence and select Quarter-over-quarter change.
- The base value should contain the TotalSales measure and Date should be Date from the Dates table.
- Create a Line chart and clustered column chart to show the Total Sales QoQ% and TotalSales by Year and Quarter using the Date Hierarchy in Dates table.
- What was the `Total Sales QoQ%` for Q4 in 2018?
<div>
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/19.PNG" width="500">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Adventure-Works/blob/main/20.PNG" width="500">
<\div> 
