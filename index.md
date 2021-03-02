**Dev:** *ASavransky*  
**Date:** *3.1.2021*


# SQL Functions
## Introduction

In this document, I will discuss the use of SQL User Defined Functions (UDFs). I will also go over the differences between Scalar, Inline, and Multi-Statement functions. 

### Use of SQL UDF

User Defined Functions (UDFs) is SQL code that performs actions, such as a complex calculation, and returns the result of that action. The result either is a scalar (single) value or result set (table). UDFs are similar to SQL Views in that they limit the ability to make changes in the data. While Views are limited to a single SELECT statement, UDFs can have multiple SELECT statements and provide more powerful logic than is possible with Views. One of the main benefits and reasons to use UDFs is that it allows users to create the function once, store it in the database, and call it as needed. This is a benefit that UDFs also share with Views and Stored Procedures. Figure 1 below shows the syntax for a scalar UDF. Notice that the command used to create an UDF is CREATE FUNCTION, which is followed by the name of the function and a list of parameters. The data type is specified with the RETURNS command and a RETURN statement is used to return a value inside the body of the function. 

![alt text](https://github.com/andressav1/ITFnd100-Mod07/blob/main/Screen%20Shot%202021-03-01%20at%208.53.37%20PM.png "tooltip text")
**Figure 1: Scalar UDF Syntax**

Figure 2 below shows the syntax used to create a table UDF. Notice how the RETURNS TABLE command specifies that the function will return a table and there is no BEGIN or END statements. 

![alt text](https://github.com/andressav1/ITFnd100-Mod07/blob/main/Screen%20Shot%202021-03-01%20at%208.53.37%20PM.png "tooltip text")
**Figure 2: Table UDF Syntax**

### Scalar, Inline, and Multi-Statement Functions 

Scalar UDFs take one or more parameters and return a single data value. The main benefit of using a scalar function is that it simplifies the code. For example, if there is a complex calculation that appears in many queries, a scalar function can be created to replace the calculation in each query. An inline table-valued function is an UDF that returns data of a table type. A multi-statement table-valued function is a table-valued function that returns the result of multiple statements. The multi-statement-table-valued function is very useful because it allows execution of multiple queries within the function and to aggregate results into the returned table. Figure 3 below shows how a simple Scalar UDF can be created to add two numbers. 

![alt text](https://github.com/andressav1/ITFnd100-Mod07/blob/main/Screen%20Shot%202021-03-01%20at%208.53.37%20PM.png "tooltip text")
**Figure 3: Creating a Simple Scalar UDF**

## Conclusion

SQL UDFs can perform complex logic, calculations, have one or more parameters and return either a scalar value or a table. This article shows to create UDFs and execute them.
