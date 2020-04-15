# Database Normalization
Database normalization: is a process used to organize a database into tables and columns. 
- The main idea with this is that a table should be about a specific topic and only supporting topics included. 
- Take a spreadsheet containing the information as an example, where the data contains salespeople and customers serving several purposes:
- Identify salespeople in your organization
- List all customers your company calls upon to sell a product
- Identify which salespeople call on specific customers.


## Reasons for Database Normalization
There are three main reasons to normalize a database. 
1. to minimize duplicate data.
2. to minimize or avoid data modification issues.
3. to simplify queries.


## Data Duplication and Modification Anomalies
- Duplicated information presents two problems:
    1. It increases storage and decrease performance.
    2. It becomes more difficult to maintain data changes.

## There are three common forms of database normalization:
1. First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
2. Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
3. Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key.