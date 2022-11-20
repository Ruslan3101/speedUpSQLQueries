# speedUpSQLQueries
How To Speed Up SQL Queries?

It is important to speed up SQL queries to ensure that your websites and applications work fast and deliver a good customer experience. Here are some tips to speed up database queries and improve query performance.



How To Speed Up SQL Queries
Here are some key ways to improve SQL query speed and performance.



1. Use column names instead of SELECT *
While using SELECT statements use only the columns you need in your result, instead of using SELECT * from … This will reduce the result size considerably and speed your SQL query.

Bonus Read : How to Increase Max Connections in MySQL


2. Avoid Nested Queries & Views
When you nest a query/view inside another query/view it results in many data return for every single query and slows down your query considerably. Sometimes, the database server may even time out and return nothing.



3. Use IN predicate while querying Indexed columns
While querying an indexed column, use an IN-list predicate instead of using mathematical operators such as ‘=’ or logical operators such as AND/OR. The IN predicate can speed up your SQL queries as the query optimizer sorts the IN-list to match the sort sequence of INDEX, leading to faster results.

Bonus Read : How to Store UTF8 characters in MySQL


4. Do pre-staging
If you have queries and procedures that do joins with large tables, it is advisable to create a separate table with this its result. When you join tables ahead of time, the SQL queries that use their result work much faster.



5. Use temp tables
Similarly, if you are joining a large table to a small one, create a temp table that contains only data required for joining with the smaller table. You can do this be selecting data from large table, transferring it to a temp table and joining the small table with this temp table.

Bonus Read : PostgreSQL Materialized View


6. Use CASE instead of UPDATE
UPDATE statement takes longer than CASE statement due to logging. On the other hand, CASE statement determines what needs to be updated and makes your SQL queries faster.



7. Avoid using GUID
Avoid using globally unique identifiers as they can slow down your queries. Use DATE or IDENTITY instead.

Bonus Read : How to Change database to UTF8


8. Avoid using OR in JOINS
JOINS are time consuming as your database has to examine each row for a match. If you also use OR condition in a JOIN, your database will take double the time to match records. As mentioned earlier, use IN operator instead.


Hopefully, the above tips will help you speed up SQL queries.
