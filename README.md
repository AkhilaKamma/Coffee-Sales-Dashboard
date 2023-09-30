# Coffee sales Dashboard in Excel
Data:
Orders table - OrderId(Primary Key)
customers Table - CustomerId(Primary Key) 
Products Table - ProductId(Primary Key)
Concepts that I Learnt inorder to create the Dashboard in Excel
1. The customer data(customer name,email,country) in the orders table is empty. So inorder to gather the data I used XLOOKUP Formula
   =XLOOKUP(...)
   Lookup_value = CustomerId
   Lookup_array = In customers sheet, Seletect the entire customerId column and press F4 for the '$' to appear
   return_array = Select the entore chstomer name column and press F4
   if_not_found = ""
   Match_mode = 0(Exact math)
   search_mode (Optional)
   Repeat the above process 3 times to get all the values  
2. INDEX MATCH to gather the product data(coffee type, Roast type, size, sales). It is dynamic
   =INDEX(...)
   array = select entire products table
   row_num = MATCH(lookup_value,lookup_array,match_type)
             lookup_value = First value of the productId column in orders
             lookup_array = Select Entire ProductId column in products table
             match_type = 0 (Exact match)
   col_num = MATCH(lookup_value,lookup_array,match_type)
             lookup_value = Select Coffee type cell in orders , double press F4
             lookup_array = Select Entire first row(header row) in products table
             match_type = 0 (Exact match)
   The main adavantage of this is at a single time you can auto populate the values of all the rows(Coffee type,Roast type, size, sales)
Total sales Pivot table:
1. short cut : Alt+N+V+T press enter --> to create a pivot table on orders page

  
   
   

   
