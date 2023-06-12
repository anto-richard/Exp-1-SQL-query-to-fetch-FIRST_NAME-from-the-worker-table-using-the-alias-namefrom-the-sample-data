# Exp-1-SQL-query-to-fetch-FIRST_NAME-from-the-worker-table-using-the-alias-namefrom-the-sample-data...

## AIM:

To write a sql query to fetch "FIRST_NAME" from the worker table using the alias name from the sample data.

## ALGORITHM:

### Step 1:

Create database ORG.

### Step 2:

Create table Worker,Bonus,Title.

### Step 3:

Insert Value to the tables.

### Step 4:

Select firstname from the table worker as name.

### Step 5:

End the program.

## PROGRAM:

```sql

CREATE DATABASE ORG;
SHOW DATABASES;
USE ORG;
CREATE TABLE Worker 
(
WORKER_ID INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
FIRST_NAME CHAR(25),
LAST_NAME CHAR(25),
SALARY INT(15),
JOINING_DATE DATETIME,
DEPARTMENT CHAR(25)
);

INSERT INTO Worker
(WORKER_ID, FIRST_NAME, LAST_NAME, SALARY, JOINING_DATE,
DEPARTMENT) VALUES

(001, 'Audra', 'Arora', 80000, '14-02-20
09.00.00', 'HR'),
(002, 'Niharika', 'Verma', 80000, '14-06-11
09.00.00', 'Admin'),
(003, 'Vishal', 'Singhal', 300000, '14-02-20
09.00.00', 'HR'),
(004, 'Amitabh', 'Singh', 500000, '14-02-20
09.00.00', 'Admin'),
(005, 'Vivek', 'Bhati', 500000, '14-06-11 09.00.00',
'Admin'),
(006, 'Vipul', 'Diwan', 200000, '14-06-11 09.00.00',
'Account'),
(007, 'Satish', 'Kumar', 75000, '14-01-20 09.00.00',
'Account'),
(008, 'Geetika', 'Chauhan', 90000, '14-04-11
09.00.00', 'Admin');

CREATE TABLE Bonus 
(
WORKER_REF_ID INT,
BONUS_AMOUNT INT(10),
BONUS_DATE DATETIME,
FOREIGN KEY (WORKER_REF_ID)
REFERENCES Worker(WORKER_ID)
ON DELETE CASCADE
);

INSERT INTO Bonus
(WORKER_REF_ID, BONUS_AMOUNT, BONUS_DATE) VALUES
(001, 5000, '16-02-20'),
(002, 3000, '16-06-11'),
(003, 4000, '16-02-20'),
(001, 4500, '16-02-20'),
(002, 3500, '16-06-11');

CREATE TABLE Title (
WORKER_REF_ID INT,
WORKER_TITLE CHAR(25),
AFFECTED_FROM DATETIME,
FOREIGN KEY (WORKER_REF_ID)
REFERENCES Worker(WORKER_ID)
ON DELETE CASCADE
);

INSERT INTO Title
(WORKER_REF_ID, WORKER_TITLE, AFFECTED_FROM) VALUES
(001, 'Manager', '2016-02-20 00:00:00'),
(002, 'Executive', '2016-06-11 00:00:00'),
(008, 'Executive', '2016-06-11 00:00:00'),
(005, 'Manager', '2016-06-11 00:00:00'),
(004, 'Asst. Manager', '2016-06-11 00:00:00'),
(007, 'Executive', '2016-06-11 00:00:00'),
(006, 'Lead', '2016-06-11 00:00:00'),
(003, 'Lead', '2016-06-11 00:00:00');
SELECT FIRST_NAME AS name
FROM Worker;

```

## OUTPUT:

![sql1](https://github.com/anto-richard/Exp-1-SQL-query-to-fetch-FIRST_NAME-from-the-worker-table-using-the-alias-namefrom-the-sample-data/assets/93427534/7dc56e1b-aab6-45ff-b0b9-162a4f4fd095)

## RESULT:

Thus, the sql query to fetch "FIRST_NAME" from the worker table using the alias name from the sample data has been successfully executed.

