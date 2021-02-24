# SQL Reference
## by Shubhrendu Tripathi

<br><br>

## TOP, LIMIT or ROWNUM Clause

    SELECT column_name(s)
    FROM table_name
    WHERE condition
    LIMIT number;

    SELECT * FROM Customers
    LIMIT 3;

    SELECT * FROM Customers
    WHERE ROWNUM <= 3;

    SELECT * FROM Customers
    WHERE Country='Germany'
    LIMIT 3;

## get data from multiple tables

    SELECT      t1.*, t2.pathimg 
    FROM        tblOne t1, tblTwo t2 
    WHERE       t1.productid = 1 AND t1.imgseq = 1 AND t1.desc = 'a' 
    ORDER       BY t1.seq;

## mysql - whoami type command

    SELECT CURRENT_USER();

    SELECT USER();

`CURRENT_USER` shows who you are authenticated as, while `USER` shows who you tried to authenticate as.


## MySQL - Query to order by second column if first column value is same

    SELECT * 
    FROM `user_job_application` 
    ORDER BY `user_job_application`.`user_id` DESC, user_job_application_date desc

## Overview

### (1) Querying Data

    SELECT

### (2) Sorting Data

    ORDER BY

### (3) Filtering Data

    WHERE
    SELECT DISTINCT
    AND
    OR
    IN
    BETWEEN
    LIKE LIMIT
    IS NULL

### (4) Joining tables

    Table & Column Aliases
    Joins
    INNER JOIN
    LEFT JOIN
    RIGHT JOIN
    CROSS JOIN
    Self-join


### (5) Grouping Data

    GROUP BY
    HAVING
    ROLLUP

### (6) Subqueries

    Subquery
    Derived table
    EXISTS

### (7) Common Table Expressions

    Common Tables Expressions (CTE)
    Recursive CTE

### (8) Set Operators

    UNION and UNION ALL
    INTERSECT
    MINUS

### (9) Modifying data in MySQL

    INSERT
    INSERT multiple rows
    INSERT INTO SELECT
    INSERT IGNORE
    UPDATE
    UPDATE JOIN
    DELETE
    ON DELETE CASCADE
    DELETE JOIN
    REPLACE
    Prepared Statement

### (10) MySQL transaction

    Transaction
    Table locking

# MySQL Data Types

## Integer Types (Exact Value) - INTEGER, INT, SMALLINT, TINYINT, MEDIUMINT, BIGINT

SQL standard integer types - `INTEGER` (or `INT`) and `SMALLINT`

Extension to the standard - `TINYINT`, `MEDIUMINT`, and `BIGINT` 

Required Storage and Range for Integer Types Supported by MySQL
Type    |   Storage (Bytes) | Minimum Value Signed  |   Minimum Value Unsigned  | Maximum Value Signed  |	Maximum Value Unsigned  |
---         | --- | --- | --- | --- | --- |
TINYINT	    |   1   |	-128        |	0   |   127                     |	255                     |
SMALLINT	|   2   |   -32768      |	0   |	32767                   |	65535                   |
MEDIUMINT	|   3   |   -8388608    |	0   |   8388607                 |	16777215                |
INT	        |   4   |   -2147483648 |   0   |   2147483647              |   4294967295              |      
BIGINT	    |   8   |   -2<sup>63</sup>        |	0   |	2<sup>63</sup>-1	    |   2<sup>64</sup>-1        |

### select all columns EXCEPT one column

No native way of doing this in SQL.

## Mnemonic 

## SELECT

<ul>
<li>Sweaty</li>
<li>Feet</li>
<li>Will</li>
<li>Give</li>
<li>Horrible</li>
<li>Odours</li>
</ul>

corresponding to:

<ul>
<li>SELECT</li>
<li>FROM</li>
<li>WHERE</li>
<li>GROUP BY</li>
<li>HAVING</li>
<li>ORDER BY</li>
</ul>

<ins>Source</ins>:
* https://picnicerror.net/development/sql-server-command-order-mnemonic-2011-06-28/

## DDL

<ul>
<li>Cat</li>
<li>Dropped</li>
<li>A</li>
<li>Tank</li>
<li>Machine</li>
</ul>

corresponding to (Data Definition Language commands):

<ul>
<li>Create</li>
<li>Drop</li>
<li>Alter</li>
<li>Truncate</li>
<li>Merge</li>
</ul>

# Types

There are five types of SQL commands:

Type | Description | Commands
--- | --- | ---
DDL | Data Definition Language | <ul><li>Create</li><li>Drop</li><li>Alter</li><li>Truncate</li></ul>
DML | Data Manipulation Language | <ul><li>Insert</li><li>Update</li><li>Delete</li></ul>
DCL | Data Control Language | <ul><li>Grant</li><li>Revoke</li></ul>
TCL | Transaction Control Language | <ul><li>Commit</li><li>Rollback</li><li>Savepoint</li></ul>
DQL | Data Query Language | <ul><li>Select</li><ul>

## CREATE
It is used to create a new table in the database.

Syntax:

    CREATE TABLE TABLE_NAME (COLUMN_NAME DATATYPES[,....]);  

Example:

    CREATE TABLE EMPLOYEE(Name VARCHAR2(20), Email VARCHAR2(100), DOB DATE);  

## DROP 
It is used to delete both the structure and record stored in the table.

Syntax

    DROP TABLE ;  

Example

    DROP TABLE EMPLOYEE;  

## ALTER
It is used to alter the structure of the database. This change could be either to modify the characteristics of an existing attribute or probably to add a new attribute.

Syntax

To add a new column in the table

    ALTER TABLE table_name ADD column_name COLUMN-definition;    

To modify existing column in the table:

    ALTER TABLE MODIFY(COLUMN DEFINITION....);  

EXAMPLE

    ALTER TABLE STU_DETAILS ADD(ADDRESS VARCHAR2(20));  
    ALTER TABLE STU_DETAILS MODIFY (NAME VARCHAR2(20));  

## TRUNCATE
It is used to delete all the rows from the table and free the space containing the table.

Syntax:

    TRUNCATE TABLE table_name;  

Example:

    TRUNCATE TABLE EMPLOYEE;  

## MERGE
UPSERT operation (insert or update)

## INSERT
It is used to insert data into the row of a table.

Syntax:

    INSERT INTO TABLE_NAME (col1, col2, col3,.... colN) VALUES (value1, value2, value3, .... valueN);  

Or

    INSERT INTO TABLE_NAME VALUES (value1, value2, value3, .... valueN);    

For example:

    INSERT INTO javatpoint (Author, Subject) VALUES ("Sonoo", "DBMS");  

## UPDATE
This command is used to update or modify the value of a column in the table.

Syntax:

    UPDATE table_name SET [column_name1= value1,...column_nameN = valueN] [WHERE CONDITION]   

For example:

    UPDATE students    
    SET User_Name = 'Sonoo'    
    WHERE Student_Id = '3'  

## DELETE
It is used to remove one or more row from a table.

Syntax:

    DELETE FROM table_name [WHERE condition];  

For example:

    DELETE FROM javatpoint  
    WHERE Author="Sonoo";  

     
## GRANT
It is used to give user access privileges to a database.

Example

    GRANT SELECT, UPDATE ON MY_TABLE TO SOME_USER, ANOTHER_USER;  

## REVOKE 
It is used to take back permissions from the user.

Example

    REVOKE SELECT, UPDATE ON MY_TABLE FROM USER1, USER2;  

<br><br><br><br>

# References
* https://stackoverflow.com/questions/50056837/mysql-query-to-order-by-second-column-if-first-column-value-is-same
* https://dev.mysql.com/doc/refman/8.0/en/sorting-rows.html
* https://www.javatpoint.com/dbms-sql-command
* https://www.w3schools.com/sql/
