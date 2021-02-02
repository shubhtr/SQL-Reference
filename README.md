# SQL Reference

## mysql - whoami type command

    SELECT CURRENT_USER();

    SELECT USER();

`CURRENT_USER` shows who you are authenticated as, while `USER` shows who you tried to authenticate as.


## MySQL - Query to order by second column if first column value is same

    SELECT * 
    FROM `user_job_application` 
    ORDER BY `user_job_application`.`user_id` DESC, user_job_application_date desc

# References
* https://stackoverflow.com/questions/50056837/mysql-query-to-order-by-second-column-if-first-column-value-is-same
* https://dev.mysql.com/doc/refman/8.0/en/sorting-rows.html

