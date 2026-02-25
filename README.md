CREATE TABLE Sailors (
    sid NUMBER PRIMARY KEY,
    sname VARCHAR2(20),
    rating NUMBER,
    age NUMBER(5,2)
);

CREATE TABLE Boat (
    bid NUMBER PRIMARY KEY,
    bname VARCHAR2(20),
    color VARCHAR2(20)
);

CREATE TABLE Reserves (
    sid NUMBER,
    bid NUMBER,
    day DATE,
    FOREIGN KEY (sid) REFERENCES Sailors(sid),
    FOREIGN KEY (bid) REFERENCES Boat(bid)
);# Dbms



25 feb 2026



CREATE TABLE Employee (
    emp_id NUMBER PRIMARY KEY,
    emp_name VARCHAR2(50),
    salary NUMBER(10,2)
);





CREATE SEQUENCE emp_seq
START WITH 1
INCREMENT BY 1
NOCACHE
NOCYCLE;



INSERT INTO Employee (emp_id, emp_name, salary)
VALUES (emp_seq.NEXTVAL, 'Sahil', 50000);

INSERT INTO Employee (emp_id, emp_name, salary)
VALUES (emp_seq.NEXTVAL, 'Rahul', 60000);



CREATE INDEX emp_salary_index
ON Employee(salary);


SELECT * FROM Employee
WHERE salary > 50000;


SELECT * FROM Employee
WHERE salary = 60000;


CREATE VIEW High_Salary_View AS
SELECT emp_id, emp_name, salary
FROM Employee
WHERE salary > 50000;

SELECT * FROM High_Salary_View;
