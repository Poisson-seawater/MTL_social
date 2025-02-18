#coding/SQL 

###### Learning Objectives
-   Describe basic relational database concepts including tables, primary keys, and foreign keys.
-   Create a database instance on the Cloud
-   Distinguish between Data Definition Language and Data Manipulation Language.
-   Explain the syntax of the CREATE TABLE statement.
-   Explain the syntax of the ALTER, DROP, and TRUNCATE statements.
-   Compose and execute CREATE TABLE, ALTER, DROP, and TRUNCATE statements hands-on on a live database.

#### Relational Database Concepts
The relational model is the most used data model for databases because this model allows
for data independence. Data is stored in a simple data structure.
Tables: this provides logical data independence, physical data independence, and physical storage
independence.

*technique vue en cours de TI*.

#### Types of SQL statements (DDL vs. DML)
Learn distinction between data definition language statements and data manipulation language statements.

**Data Definition Language** (or DDL) statements are used to define, change, or drop database
objects such as tables. Common DDL statement types include CREATE, ALTER, TRUNCATE, and DROP.
CREATE: which is used for creating tables and defining its columns;
ALTER: is used for altering tables including adding and dropping columns and modifying
their datatypes;
TRUNCATE: is used for deleting data in a table but not the table itself;
DROP: is used for deleting tables.


**Data Manipulation Language** (or DML) statements are used to read and modify data in tables.
These are also sometimes referred to as CRUD operations, that is, Create, Read, Update and Delete rows in a table.
Common DML statement types include INSERT, SELECT, UPDATE, and DELETE.
INSERT: is used for inserting a row or several rows of data into a table;
SELECT: reads or selects row or rows from a table;
UPDATE: edits row or rows in a table;
And DELETE: removes a row or rows of data from a table.

#### CREATE TABLE Statement
Goal: be able to distinguish between data definition language statements and data manipulation language statements, and explain how the entity name and attributes are used to create a relational database table.

Syntax:
CREATE TABLE *table_name*
(
column_name_1 datatype optional_parameters,
column_name_2 datatype,
...
column_name_n datatype
)

###### Datatype optional_parameters

CREATE TABLE author
(
autor_id **char**(2) Primary key not null,
lastname **varchar**(24) not null,
email varchar(40)
)

In this example, the data types used are: CHAR which is a character string of a fixed length, in this case 2.
And VARCHAR, which is a character string of a variable length. In this case, this variable character field can be up to 24 characters long.

Author_ID is the Primary Key.

Not null mean it must have a value


####  ALTER, DROP, and Truncate Tables

You use the ALTER TABLE statement to add or remove columns from a table, to modify the data type of columns, to add or remove keys, and to add or remove constraints:

> ALTER TABLE *table_name*
> ADD COLUMNE *columne_name1* datatype
> ...
> ADD COLUMNE columne_namen datatype;

Can use the ALTER COLUMN to modify or specifying the new data type for the column.
> ALTER TABLE *table_name*
> ADD COLUMNE *columne_name1* SET DATA TYPE CHAR(20)

*char(20) étant la modification*

**exemple de ALTER**
ALTER TABLE table_name
ADD COLUMN column_name data_type column_constraint;

ALTER TABLE table_name
DROP COLUMN column_name;

ALTER TABLE table_name
ALTER COLUMN column_name SET DATA TYPE data_type;

ALTER TABLE table_name
RENAME COLUMN current_column_name TO new_column_name;


###### DROP COLUMN clause to remove the column:

> ALTER TABLE author 
> DROP COLUMN telephone_number;


###### to delete a table
> DROP TABLE table_name ;

If you delete a table that contains data, by default the data will be deleted alongside the table
Can add the WHERE at to specify.


To delete juste the data
> TRUNCATE TABLE table_name IMMEDIATE;

The IMMEDIATE specifies to process the statement immediately and that it cannot be undone.