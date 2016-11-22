# OdbcSelectWithRowColumArrayBind
Copyright (c) 2016 Sathyanesh Krishnan. All rights reserved.

Licensed under the Apache License, Version 2.0;

## ODBC Select With Row and Column bind

This is an ODBC SELECT sample with Row and Column wise Bind. 
Then each case retrieving values by using SQLFetchScroll and SQLExtendedFetch. 
Thou the code is mostly generic; the VS 2015 Project given with the demo is created by linking with Informix ODBC driver library.


## Key properties application need to set

### RowWiseBinding: The application set Attributes of   
* SQL_ATTR_ROW_BIND_TYPE  
    The application declares the size of the structure to the driver with the SQL_ATTR_ROW_BIND_TYPE statement attribute and binds the address of each member in the first element of the array. 
    Thus, the driver can calculate the address of the data for a particular row and column as.
     
* SQL_ATTR_ROW_ARRAY_SIZE  
    The application sets SQL_ATTR_ROW_ARRAY_SIZE on all statements to declare the number of rows returned on a SQLFetch or SQLFetchScroll function call.

* SQL_ATTR_ROW_STATUS_PTR  
    To Sets the address of the row status array filled so that SQLFetch and SQLFetchScroll can set the status value.

* SQL_ATTR_ROWS_FETCHED_PTR  
    Sets the address of the buffer in which SQLFetch and SQLFetchScroll return the number of rows fetched

* SQL_ROWSET_SIZE  
 FYI: If you are using SQLExtendedFetch rather than SQLFetchScroll to fetch the data`


### ColumnWiseBinding: The application set Attributes of   
* SQL_ATTR_ROW_BIND_TYPE
* SQL_ATTR_ROW_ARRAY_SIZE
* SQL_ATTR_ROW_STATUS_PTR
* SQL_ATTR_ROWS_FETCHED_PTR
