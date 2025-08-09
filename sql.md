## **Beginner project on sql**
***This project is aimed at implemeting how to retrieve a data from a database.***

### **What is SQL?**
SQL means structured querry language. Its a language that you can use to interact with databases. You can retrieve data, add, delete, filter, sort, update and remove data from a database.

### **What is a database?**
A database is a collection of tables and those tables have relatonships.
In order to interface with a database, we are going to use something called ***RDBMS (Relational Database Management System)*** these includes:
- Oracle
- MySQL
- PostgreSQL
- Microsoft SQL Server

After setting up your database engine, we are going go need a graphical frontend that will allow us to write queries against our database. (A tool call SQL Server Management Studio) wwill be used. This will allow us connect to the database engiine.

## W3schools.com
Every table has: **fields, records (or rows), and columns**

- **Fields:** Fields are columns designed to maintain specific information about every record.
- **Recors or Rows:** is each individual entry in a table.
- **Columns:** are vertical entities in a table, containing all information associated with a specific field.


## SQL Syntax
- **SQL Statements**

Most of the actions you need to perform on a database are done with SQL statements.

SQL statements consist of keywords that are easy to understand.

ExampleGet your own SQL Server
Select all records from the Customers table:

```
SELECT * FROM Customers;
```

## Database Tables
A database most often contains one or more tables. 
Each table is identified by a name ***(e.g. "Customers" or "Orders")***, and contain records (rows) with data.

**POV:** SQL keywords are not case sensitive.

```
select is the same as SELECT
```

- **Semicolon after SQL Statements?**

Some database systems require a semicolon at the end of each SQL statement. Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same call to the server.

- **Some of The Most Important SQL Commands**

```
SELECT - extracts data from a database
UPDATE - updates data in a database
DELETE - deletes data from a database
INSERT INTO - inserts new data into a database
CREATE DATABASE - creates a new database
ALTER DATABASE - modifies a database
CREATE TABLE - creates a new table
ALTER TABLE - modifies a table
DROP TABLE - deletes a table
CREATE INDEX - creates an index (search key)
DROP INDEX - deletes an index
```

- ### The SQL SELECT Statement**

The SELECT statement is used to select or grab a specific data from a database.

- Example: 

Return data from the Customers table:

```
SELECT CustomerName, City FROM Customers;
```

### Syntax

```
SELECT column1, column2, ...
FROM table_name;
```

Here, column1, column2, ... are the field names of the table you want to select data from.

The table_name represents the name of the table you want to select data from.

- **Select ALL columns**

If you want to return all columns, without specifying every column name, you can use the 

```
SELECT * 
```
syntax.

- **Example**

Return all the columns from the Customers table:

```
SELECT * FROM Customers;
```


### SQL SELECT DISTINCT Statement
The SELECT "DISTINCT" statement is used to return only distinct (different) values. In otherwords, the `"distinct"` stamenet ***`is used 
to return unique values from a column that contains duplicates`***

- Example: 

Select all the different countries from the "Customers" table:

```
SELECT DISTINCT Country FROM Customers;
```

Inside a table, a column often contains many duplicate values ***(for example in a column named countries, you may have Nigeria apearing more than 5 times in a row; the distinct statement will filter duplicate countres and give u each individual countries without its duplicate)***; and sometimes you only want to list the different (distinct) values.

### Count Distinct

By using the `'DISTINCT'` keyword in a function called `'COUNT'`, we can return the number of different countries.

- **Example**

```
SELECT COUNT (DISTINCT Country) FROM Customers;
```

### SQL WHERE Clause
The **`WHERE`** clause is used to filter records.

It is used to extract only those records that fulfill a specified condition.

- Example

Select all customers from Mexico:

```
SELECT * FROM Customers
WHERE Country='Mexico';
```

`Note:` The WHERE clause is not only used in SELECT statements, it is also used in UPDATE, DELETE, etc.!