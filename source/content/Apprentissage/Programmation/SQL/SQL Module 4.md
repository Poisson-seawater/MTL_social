#coding/SQL 

#### Working with Real World Data Sets 
Introduced to some of the tips and techniques for working with real-world datasets.

To be able to:
- Work with and load CSV files in a database.
- Describe how attribute names in headers of CSV files map to column names in DB2.
- And restrict rows in a query to sample data in a table

Toujours MAJUSCULE_UNDERSCORE pour nommer.

#### Getting Table and Column Details
be able to: 
- identify where metadata for database objects is stored.
- Retrieve the list of tables in a database and their properties.
- And access information about each column in a table.

Sometimes your database may contain several tables and you may not remember the correct names. -> you want to read the META data. 
- In Db2 this catalog is called “SYSCAT.TABLES.”
- In SQL Server it is “INFORMATION_SCHEMA.TABLES” 
- And in Oracle it is “ALL_TABLES” or “USER_TABLES.”

In MySQL you can even enter a shortcut command like "SHOW
TABLES” on the MySQL Command Line Prompt to get the list of tables.

Db2 database you can run the following query: 
> select * from syscat.tables

This select statement will return too many tables, including system tables,
so it is better to filter the result set by specifying a user schema name as shown here:
> select TABSCHEMA, TABNAME, CREATE_TIME from syscat.tables where tabschema=‘ABC12345’

Ensure you replace ‘ABC12345’ with your own Db2 username or the schema you want to get details for.
When you do a select * from syscat.tables you get all the properties of the tables.