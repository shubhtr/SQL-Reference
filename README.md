# SQL Reference

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


# References
* https://stackoverflow.com/questions/50056837/mysql-query-to-order-by-second-column-if-first-column-value-is-same
* https://dev.mysql.com/doc/refman/8.0/en/sorting-rows.html

