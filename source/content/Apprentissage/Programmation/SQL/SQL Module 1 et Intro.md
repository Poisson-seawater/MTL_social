#coding/SQL
The purpose of this course is to introduce relational database concepts and help you learn and apply foundational knowledge of the SQL language. It is also intended to get you started with performing SQL access in a data science environment.

The emphasis in this course is on hands-on and practical learning. As such, you will work with real databases, real data science tools, and real-world datasets. You will create a database instance in the cloud. Through a series of hands-on labs, you will practice building and running SQL queries.

###### Sommaire
**Module 1 - Getting Started with SQL**
-   Introduction to Databases
-   SELECT Statement
-   SELECT Statement Examples
-   Hands-on Lab: Basics of SELECT Statements
-   COUNT, DISTINCT, LIMIT
-   Hands-on Lab: COUNT, DISTINCT, LIMIT
-   INSERT Statement
-   UPDATE and DELETE Statements
-   Summary & Highlights
-   Practice Quiz
-   Module 1 Graded Quiz

**Module 2 - Introduction to Relational Databases and Tables**
-   Relational Database Concepts
-   How to Create a Database Instance on Cloud
-   Hands-on Lab: Sign up for IBM Cloud, Create Db2 Service Instance and Get started with the Db2 Console
-   Types of SQL Statements (DDL vs. DML)
-   CREATE TABLE Statement
-   ALTER, DROP and Truncate Tables
-   Examples to CREATE and DROP Tables
-   Hands-on Lab: CREATE, ALTER, TRUNCATE, DROP
-   Hands-on Lab: Create and Load Tables using SQL Scripts
-   Summary & Highlights
-   Practice Quiz
-   Module 2 Graded Quiz

**Module 3 -** **Intermediate SQL**
-   Using String Patterns and Ranges
-   Sorting Result Sets
-   Grouping Result Sets
-   Hands-on Lab: String Patterns, Sorting & Grouping
-   Summary & Highlights
-   Practice Quiz
-   Module 3 Graded Quiz 1
-   Built-in Database Functions
-   Date and Time Built-in Functions
-   Hands-on Lab: Built-in Functions
-   Sub-Queries and Nested Selects
-   Hands-on Lab: Sub-Queries and Nested SELECTs
-   Working with Multiple Tables
-   Hands-on Lab: Working with Multiple Tables
-   Summary & Highlights
-   Practice Quiz
-   Module 3 Graded Quiz 2

**Module 4 -** **Assignment Preparation: Working with real-world data sets and built-in SQL functions**
-   Working with Real World Datasets
-   Hands-on Lab: Working with a Real World Dataset using SQL and IBM Cloud DB2
-   Getting Table and Column Details
-   LOADing Data

## Module 1
-   Describe SQL and Databases
-   Explain the syntax of basic SQL statements - Select, Insert, Update, Delete
-   Compose and execute basic SQL statements hands-on on a live database
-   Demonstrate how to write basic SQL statements


### Introduction to Databases
SQL is a language used for relational databases to query or get data out of a database.
SQL = Structured English Query Language.

A database is a repository of data. It is a program that stores data. A database also provides the functionality for adding, modifying, and querying that data

There are five simple commands to create a table, 
- insert data to populate the table, 
- select data from the table, 
- update data in the table,
- delete data from the table.
So those are the building blocks for SQL for data science.

RDBMS stands for Relational Database Management System.

### Retrieving Data from a Table
The SELECT statement is called a query, and the output we get from executing this query is called a result set or a result table.

how yo use SELECT: 
Select * from table_name
Etoile : * , signifie ce que tu saisie, une colonne par exemple.

WHERE: 
est utiliser pour rajouter une condition au SELECT. WHERE évalue: true, false ou unknow.

*exemple:*
select book_id, title from Book
where book_id='B1'

To retrieve all columne, use the * : 
**select COLUMN* from TABLE1 ;**
instead of, select COLUMN1, COLUMN2, ... from TABLE1 ;

**select * from COUNTRY** => To retrieve data for all rows in the COUNTRY table

#### Comparaison Operator 
Équale : =
Greater than: > 
Lesser than: < 
Greater than or equal: >= 
Not equal to: <>


### COUNT, DISTINCT, LIMIT
>Select COUNT (DISTINCT Medals) where years = 2018 LIMIT 5.

COUNT is a built-in database function that retrieves the number of rows that match the query criteria.
Let's say you create a table called MEDALS which has a column called COUNTRY, and
you want to retrieve the number of rows where the medal recipient is from Canada.
You can issue a query like this:
- Select COUNT(COUNTRY) from MEDALS where COUNTRY='CANADA.'

DISTINCT is used to remove duplicate values from a result set.
retrieve the list of unique countries that received gold medals.
That is, removing all duplicate values of the same country.
- Select DISTINCT COUNTRY from MEDALS where MEDALTYPE = 'GOLD'.

*Like WHERE, LIMIT est une restriction a qu'est ce qu'on sort*
LIMIT is used for restricting the number of rows retrieved from the database.
Example retrieve just the first 10 rows in a table.
- Select * from tablename LIMIT 10.
Retrieve just a few rows in the MEDALS table for a particular year.
- Select * from MEDALS where YEAR = 2018 LIMIT 5.

Retrieve the first 15 rows from the “FilmLocations” table starting from row 11: 
SELECT * FROM FilmLocations LIMIT 15 OFFSET 10;

### INSERT Statement
After table is created, the table needs to be populated with data.
To insert data into a table, we use the INSERT statement. to add new ROW.

The INSERT statement is one of the data manipulation language statements.
Data manipulation language statements or DML statements are used to read and modify data.
> INSERT INTO [TableName] <([ColumnName],...)> VALUES ([Value],...)

It is important that the number of values provided in the values clause is equal to the number of column names specified in the column name list.

> Insert into Author 
> 	(AUTHOR_ID, LASTNAME, FIRSTNAME, EMAIL, CITY, COUNTRY)
> 	VALUES('A1', 'Chong', 'Raul', 'bb@mail.com', 'Toronto', 'CA')

Note, on peut rajouter autant de ligne VALUES avec les valeurs que l'on souhaite dans le Statement Insert. 


### UPDATE and DELETE Statements
Altering and deleting data in a relational database table.
The UPDATE statement is one of the data manipulation language or DML statements.
Pour les 2 statements, important de spécifier les **where** car sinon cela s'applique sur toute la base de donnée. 

> UPDATE [TableName] SET [ [ColumnName]=[Value] ] WHERE [Condition]

In this statement, table name identifies the column value to be changed as specified in the WHERE condition

Example: 
change A2 from Rav Ahuja to Lakshmi Katta.
> UPDATE AUTHOR SET LASTNAME='KATTA' FIRSTNAME='LAKSHMI' WHERE AUTHOR_ID='A2'


The syntax of the DELETE statement looks like this: 
> DELETE FROM [TableName] WHERE [Condition]

Example: we want to delete the rows for author ID A2 and A3.
> DELETE FROM AUTHOR WHERE AUTHOR_ID ID IN ('A2', 'A3') 
