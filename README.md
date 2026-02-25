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
