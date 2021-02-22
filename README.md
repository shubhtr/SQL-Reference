# SQL Reference
## by Shubhrendu Tripathi

<br><br>

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

<br><br><br><br>

# References
* https://stackoverflow.com/questions/50056837/mysql-query-to-order-by-second-column-if-first-column-value-is-same
* https://dev.mysql.com/doc/refman/8.0/en/sorting-rows.html

