#sql
## SQL
SQL might seem intimidating but it’s really fairly easy to understand. SQL stands for
Structured Query Language and simply put, it’s a search language for you to instruct a
database about what information you’d like retrieved from it.<br />
## SELECT queries:
Select query for a specific columns<br />
SELECT column, another_column, …<br />
FROM mytable;<br />
and 
Select query for all columns
SELECT * 
FROM mytable;
slect all table for movies
SELECT * FROM movies;
## Queries with constraints
Select query with constraints
SELECT column, another_column, …
FROM mytable<br />
WHERE condition<br />
    AND/OR another_condition<br />
    AND/OR …;<br />
## Queries with constraints
|Operator|	Condition|	Example|
|------------|:-------------------:|----------:|
| =    |   	Case sensitive exact string comparison (notice the single equals)   | 	col_name = "abc"   |
| != or <>    | Case sensitive exact string inequality comparison  | 	col_name != "abcd"   |
| LIKE    |Case insensitive exact string comparison| 	col_name LIKE "ABC"  |
|%    |   	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)  | 	col_name LIKE "%AT%"
(matches "AT", "ATTIC", "CAT" or even "BATS")   |
| _  | 	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE) | 	col_name LIKE "AN_"
(matches "AND", but not "AN")  |
| IN (…)   |String exists in a list| 		col_name IN ("A", "B", "C")  |
| NOT IN (…) |String does not exist in a list| 			col_name NOT IN ("D", "E", "F")  |

## Exercise

Select query with constraints
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
    
  ##  Multi-table queries with JOINs
  Select query with INNER JOIN on multiple tables
SELECT column, another_table_column, …
FROM mytable
INNER JOIN another_table 
    ON mytable.id = another_table.id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;
  
  ## OUTER JOINs
  Select query with LEFT/RIGHT/FULL JOINs on multiple tables
SELECT column, another_column, …
FROM mytable
INNER/LEFT/RIGHT/FULL JOIN another_table 
    ON mytable.id = another_table.matching_id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;
  
 ## Database Management
  Example: Correlated subquery
For example, in our Movies table, the values in the Year column must be an Integer, and the values in the Title column must be a String.
  
  Insert statement with values for all columns
INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;
       Insert statement with specific columns
INSERT INTO mytable
(column, another_column, …)
VALUES (value_or_expr, another_value_or_expr, …),
      (value_or_expr_2, another_value_or_expr_2, …),
      …;
      Example Insert statement with expressions
INSERT INTO boxoffice
(movie_id, rating, sales_in_millions)
VALUES (1, 9.9, 283742034 / 1000000);
## Updating rows
  Update statement with values
UPDATE mytable
SET column = value_or_expr, 
    other_column = another_value_or_expr, 
    …
WHERE condition;
## Deleting rows
  Delete statement with condition
DELETE FROM mytable
WHERE condition;
 ## Creating tables
  Create table statement w/ optional table constraint and default value
CREATE TABLE IF NOT EXISTS mytable (
    column DataType TableConstraint DEFAULT default_value,
    another_column DataType TableConstraint DEFAULT default_value,
    …
);
### An example
  Movies table schema
CREATE TABLE movies (
    id INTEGER PRIMARY KEY,
    title TEXT,
    director TEXT,
    year INTEGER, 
    length_minutes INTEGER
);
 ## Altering tables
  Altering table to add new column(s)
ALTER TABLE mytable
ADD column DataType OptionalTableConstraint 
    DEFAULT default_value;
    Altering table to remove column(s)
ALTER TABLE mytable
DROP column_to_be_deleted;
### Renaming the table
    Altering table name
ALTER TABLE mytable
RENAME TO new_table_name;
## Dropping tables
Drop table statement
DROP TABLE IF EXISTS mytable;
### imge for sql and databases managment
[image](./SQLBolt - Learn SQL - SQL Lesson X_ To infinity and beyond! - Google Chrome 2_26_2022 12_49_49 PM)
