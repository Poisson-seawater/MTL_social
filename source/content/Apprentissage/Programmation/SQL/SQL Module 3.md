#coding/SQL 

###### Learning Objectives
-   Demonstrate how to use string patterns and ranges in SQL queries
-   Demonstrate the use of grouping data in result sets
-   Demonstrate how to sort and order result sets
-   Demonstrate how to write sub-queries and nested selects
-   Build queries to access multiple tables

#### Using String Patterns, Ranges

##### Using String Patterns
what if we don't know exactly what value to specify in the WHERE clause?

We can use string patterns to search data rows that match a condition.
> WHERE *columne_name* LIKE *patern*

Patern can be a letter, -> WHERE *firstname* LIKE R%
and "%" is a **wildcard charactere**.

A wildcard character is used to substitute other characters.
% is use to subtite to letter 
- The percent sign is used to define missing letters.
- The percent sign can be placed before the pattern,
- after the pattern, or both before and after the pattern

##### Using RANGE
Select *title, page* from *book*
Where *pages* >= 250 and *page* <= 300;

can be write as: 
> Select *title, page* from *book*
> WHERE *pages* between 290 and 300;


###### IN operator
The IN operator allows us to specify a set of values in a WHERE clause.

Select *firstname, lastname, country* from *author*
WHERE *country* ='AU' OR *country* ='BR'

can be write as:
> Select *firstname, lastname, country* from *author*
> WHERE *country* IN ('AU', 'BR')


#### Sorting Result Sets

Sort data by **ascending** order.
Here, *title* are string, so it is alphabetic ascending order, with the **columne name**: 
> Select *title* from *book*
> ORDER BY *title*

To have **descending** order:
> Select *title* from *book*
> ORDER BY *title* DESC


Another way of specifying the sort column is to **indicate the column sequence number**.
> Select *title, pages* from *book*
> ORDER BY 2

*title* is columne number 1
*page* is columne number 2.

So the results is show from the book with the least pages to the one having the most page.


#### Grouping Result Sets
At the end of this lesson, you will be able to explain how to eliminate duplicates from a result set and describe how to further restrict a result set.

When using ORDER BY, we can have duplicate.
> Select DISTINC(*columne_name*) from *table_name*;

Si on veux savoir la récurrance, on utilise "GROUP BY" et "DISTINCY"
> Select DISTINC(*columne_name*) from *table_name*
> GROUP BY *columne_name*;

Le résultat sera 2 colonne: columne_name et nombre d'occurance.
Comme la 2e colonne sera appelé "2".

On peut choisir son nom en écrivant: 
> Select *columne_name*, count(*colomne_name*) 
> as *2e_columne_name* from *table_name*
> GROUP BY *columne_name*;


###### HAVING
Work only with GROUP BY. C'est un peu comme le WHERE. C'est pour plus de restriction sur ce qu'on sort.

> Select *columne_name*, count(*colomne_name*) 
> as *2e_columne_name* from *table_name*
> GROUP BY *columne_name*
> HAVING *2e_columne_name*(*columne_name*) > n;


### Built-in Database Functions
When working with large data sets, it may be faster to use built in functions, rather than first retrieving the data into your application and then executing functions on the retrieved data.

Fonction comme min(), avr(), max(), sum() ... qui sont des valeurs résultant de calcule entre 2 colonne ou au sein de la colonne. 

To explicitly name the columne gatterng the information: 
> select SUM(*COST*) as SUM_OF_COST from *PETRESCUE*.

example of min:
> select MIN(*ID*) from *PETRESCUE* where *animal* = 'dog';

Pour avoir une division en résultat.
> select AVG(*COST* /  *QUANTITY*) from *PETRESCUE* where *ANIMAL* = 'Dog';

###### Scalar and String functions.
Scalar functions perform operations on individual values.
Can be used with WHERE. 

For example, to round up or down every value in the cost column
to the nearest integer
> select ROUND (*COST*) from *PETRESCUE*;

For char and varchar values: 
to retrieve the length of each value in animal column,
> select LENGTH (*ANIMAL*) from *PETRESCUE*;

to retrieve animal values in uppercase (or lowercase):
> select UPPERCASE (*ANIMAL*) from *PETRESCUE*.

If you're not sure whether the values are stored in upper, lower or mixed case in the table.
For example, to get unique cases for the animal column in uppercase: 
> select DISTINCT (UPPERCASE(*ANIMAL*)) from *PETRESCUE*;


### Date and Time Built-in Functions
Functions exist to extract the day, month, day of month, day of week, day of year, week, hour, minute, and second.

to get the day portion for each rescue date involving cat,
> select DAY (*RESCUEDATE*) from *PETRESCUE* where *ANIMAL*='cat';

Math:
> select (*RESCUEDATE* +  3 *DAYS*) from *PETRESCUE*.

to find how many days have passed since each rescue date till now:
> Select (*CURRENT_DATE* - *RESCUEDATE*) from *PETRESCUE*.


#### Sub-Queries and Nested Selects
You'll learn how to write sub-queries or nested selects statements.

Sub-queries or sub selects are like regular queries but placed within parentheses and nested inside another query. This allows you to form more powerful queries than would have been otherwise possible.

> Select *emp_id, F_Name, L_Name, Salary*
> from *employee*
> where *Salary* < 
> (Select AVG(*salary*) from *employee*)

**Explication:** aggregate functions, like the average function, cannot always be evaluated in the WHERE clause.
Car la, le WHERE peut se déplacer dans dans tout le tableau puis comparer au colonne restreinte. 

Sub-queries like these are sometimes called derived tables or table expressions.

To create a table expression that contains information from one table.
> Select * from 
> (select EMP_ID, F_NAME, L_NAME, DEP_ID from employees) AS EMP4AL;

#### Working with Multiple Tables
how to write queries that access more than one table.

Example: 
The employees table contains several columns for categories, such as employee ID, first name, last name, and salary to name a few. The Departments table contains a department ID, department name, Manager ID, and location ID.

If we want to retrieve only the employee records from the employees table for which a department ID exists in the departments table, we can use a sub-query as follows.
> Select * from *employees* 
> where *department_ID* IN 
> (Select *department_ID_department* from *departments*);

Without using the primary key
> Select * from *employees*
>  where *department_ID* IN,
>  (select *department_ID_department* from *departments* 
>  where *location_ID* = 'L0002');


Cartesian join or full join
> Select * from *employees*, *departements*;


Define the alias E for employees table and D for departments table:
>Select * from *employees* E, *departments* D, 
>where *E.department_ID* = D.department_ID_department;

