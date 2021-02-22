# SQL

According to [SQLBolt](https://sqlbolt.com/) SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.

### SQL Databases
1. SQL Lite
2. MySQL
3. MSSQL

### SQL Command and Syntax

to create a table, use **create** and **table** keywords with the table name as desired.
then add the columns of the table and the type of each.

```SQL
  create table student(
    id varchar(10) primary key,
    st_name varchar(20),
    grade number,
    course varchar(20)
);
```

to get data from a table in an SQL database, use the **select** keyword.

followed by the column/s name/s (use * to select all the columns).

then specify the table name using **from** keyword and the name of the table.

```SQL
  -- get all the columns data
  select * from student;

  -- get the student name and the course only
  select st_name, course from student;

```

to add a condition for data to meet, use **where** keyword.

```SQL
  -- to show only passed student names
  select st_name from student
  where grade > 50;
```

### Some SQL useful Keywords

1. **distinct** to remove duplication. Usage =>  `select distinct st_name from student`.
2. **order by** to order the data selected from the table ascending or descending. Usage =>  `select st_name from student order by asc`.
3. **like** to get data similarly to a pattern Usage =>  `select distinct st_name from student where name 'abd*`. 
this will select all students their names start with abd. 

### Notes
1. SQL is an insensitive case, keywords, table names or columns can be spelled capital or small, it will not raise any error, but people used to write SQL keywords in capital to distinguish between SQL and the programming language uses it.
2. each SQL statement must end with a **semicolon**.
