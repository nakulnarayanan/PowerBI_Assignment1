# PowerBI_Assignment1
PowerBI_Assignment1
Downloaded and Loaded the 3 CSV files to the power BI.
Opened the sheets in power query by using Transform Data option.
Data Transformation: 
● Restrict the "List of Orders" table to only the first 500 rows.  - Home->Keep Rows->Keep Top Rows -> enter 500 in list of orders table.
● Ensure the “Order Date” column in the “List of Orders” table is set to data type 'Date'. - Corrected
● Change the data type of “Amount” and “Target” columns to ‘Fixed Decimal Number’. - Updated by selecting at the top left of each columns mentioned.
● Format the "CustomerName" column into proper case, ensuring consistent capitalization for each word.  - Format-> Capitalize Each Word, Clean, Trim
● Merge the "State" and "City" columns to create a new column named "Location" in the format ‘City, State’.  - Add Column -> Custom column ->[City] & "," &" " &[State]
● Create a new custom column named "Profit Margin" as the percentage of "Profit" divided by "Amount". - Add Column -> custom column -> =([Profit]/[Amount])
● Add a new conditional column named "Profit Status" based on the values in the 
"Profit" column. The conditions are as follows: if the profit is less than 0, the label 
should be "Loss"; if the profit equals 0, the label should be "Break-Even"; and if the 
profit is greater than 0, the label should be "Profit". --> Used If else formula to give condition

Merging Data (Joins): 
● Merge the "List of Orders" and "Order Details" tables into a new single table named "Orders Data" based on the "Order ID" relationship.->Home->merge queris as new->Used left outer join by selecting the order id column in both tables.
Handling Missing Data & Duplicate Data: 
● Identify missing values in the data and determine a strategy to address them. -> No missing values found
● Check for duplicate rows and define a strategy to handle duplicates. -> Selected the entire columns and Remove Rows->Remove Duplicates

Sorting and Filtering Data: 
● In the ‘Orders Data’ table, utilize sorting and filtering techniques on columns like 
Order Date, State or Category to analyze data based on specific criteria: -done
◆ Sort the orders by Order Date in descending order to analyze recent trends. -Checked, found recently Profits were high.
◆ Filter the orders to focus only on a specific state (e.g., Tamil Nadu) for regional analysis. - Checked for TN, and found Loss is more compared to north indian states like Bihar.


Grouping and Aggregating Data: 
● Duplicate the “Order Details” table and calculate the count of each Order ID, average 
profit by Category or total amount by Sub-Category.  - done, using Home-> GroupBy option
● Duplicate the “Sales Target” table and aggregate the total target amount by Month of 
Order Date. - done, using Home-> GroupBy option. Also created a stacked column chart for this.


Data Modeling: 
● Establish a relationship between the “List of Orders” and “Order Details” tables using 
the ‘Order ID’ column. - Created the relationship, many to one
● Build a relationship between the “Order Details” and “Sales Target” tables based on 
the ‘Category’ column. Click "Manage relationships" and ensure this relationship is 
active. - Created many to many.
Checked and found both relationship is active.

