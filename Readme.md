DBMS PRACTICAL ASSIGNMENT – 2

Title:
Implement SQL DDL statements demonstrating the use of SQL objects such as Table, View, Index, Sequence and Constraints.

---------------------------------------------------------
PART A
---------------------------------------------------------

1) Create Tables using ORACLE SQL DDL

CREATE TABLE employee (
    ID INTEGER PRIMARY KEY,
    person_name VARCHAR2(50),
    street VARCHAR2(100),
    city INTEGER
);

CREATE TABLE works (
    ID INTEGER PRIMARY KEY,
    company_name VARCHAR2(50)
);

CREATE TABLE company (
    company_name VARCHAR2(50) PRIMARY KEY,
    city VARCHAR2(50)
);

CREATE TABLE manages (
    ID INTEGER PRIMARY KEY,
    manager_id INTEGER
);

---------------------------------------------------------

2) Add column salary in works table

ALTER TABLE works
ADD salary INTEGER;

---------------------------------------------------------

3) Modify datatype of city column in employee to string

ALTER TABLE employee
MODIFY city VARCHAR2(50);

---------------------------------------------------------

4) Delete column street from employee table

ALTER TABLE employee
DROP COLUMN street;

---------------------------------------------------------

5) Rename column manager_id to manager in manages table

ALTER TABLE manages
RENAME COLUMN manager_id TO manager;

---------------------------------------------------------

6) Rename table company to CMP

ALTER TABLE company
RENAME TO CMP;

---------------------------------------------------------

7) Drop table manages

DROP TABLE manages;

---------------------------------------------------------
PART B
---------------------------------------------------------

Given Table:
employee(empno, empname, designation, city, salary, zipcode, county)

1) Create a Sequence for empno

CREATE SEQUENCE emp_seq
START WITH 1
INCREMENT BY 1
NOCACHE
NOCYCLE;

2) Create an Index on county

CREATE INDEX idx_county
ON employee(county);

3) Create a View for employees having salary < 50000 and city = 'Mumbai'

CREATE VIEW mumbai_low_salary AS
SELECT *
FROM employee
WHERE salary < 50000
AND city = 'Mumbai';

---------------------------------------------------------

SQL Objects Used:
TABLE, PRIMARY KEY, ALTER TABLE, DROP TABLE, RENAME, SEQUENCE, INDEX, VIEW.
