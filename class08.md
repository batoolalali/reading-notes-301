# SQL
**Structured Query Language**
a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.

There are many popular SQL databases including:
1. SQLite
2. MySQL
3. Postgres
4. Oracle 
5. Microsoft SQL Server.

## Relational databases
A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.

- *SELECT*  :   To retrieve data from a SQL database 
    - FROM
    - WHERE

SELECT column, another_column, …
FROM mytable
WHERE condition

- Filtering and sorting Query results
    - DISTINCT


ORDER BY clause are the LIMIT and OFFSET clauses, which are a useful optimization to indicate to the database the subset of the results you care about.
The LIMIT will reduce the number of rows to return, and the optional OFFSET will specify where to begin counting the number rows from.