# EX 3 SubQueries, Views and Joins 


### Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
### Insert the values
```sql
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

### Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
### Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:
![280709538-ffacbd63-d7ce-48b1-be46-a430bb96138c](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/51d2bf9e-761d-4d5a-9450-a27fe05be0c0)


### OUTPUT:
![280709424-1ca3a0ed-dee9-4aa2-843d-69efbcfa11c1](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/46410724-3c29-4f5a-8446-6d8306097a8f)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
![280709669-be046083-b7d9-4ada-9790-3fb99a5dd2f5](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/692717cf-e8f4-45ee-95af-31dd15825ee7)


### OUTPUT:
![280709957-17467088-0a96-45fc-9f2f-5a5527b740a2](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/6d30055d-bcbe-4ec8-8c27-a34b93930b79)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
![280709999-f2537a43-d410-48a8-b6e7-07ac2d1f6d44](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/19dc1dd7-d939-4ec3-826b-58e9b65af126)


### OUTPUT:
![280710051-2ea101e5-35a3-4da6-b58a-79bfbfdb47da](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/9646392a-0a01-41a1-92b1-afc26956c2e4)


### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![280710143-0c1b682f-05d0-4d6c-8cd8-c8f93099486d](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/7354d080-92de-4b1f-b9bf-de88064a5c4f)


### OUTPUT:
![280710262-3a35705f-d443-40d0-b58d-44fc85481d06](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/29bea315-e62d-4ee8-a76f-e7084fcd0641)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:
![280710322-62de8c01-8e89-44af-b0da-6cfd1835cc83](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/bc262724-2d62-4fa4-92e8-f9c4e968bf90)


### OUTPUT:
![280710861-5b83cebb-a748-43fe-9498-886b11e4c8b9](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/f58b5137-45a0-4753-90f0-7ee077565c8d)

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
![280710588-400707bb-0655-489f-9a86-5a8bfd8ddf50](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/9d67061f-b4e3-4bb2-8805-255662c02bfc)


### OUTPUT:
![280710745-196752b7-5f04-440c-912b-f28c8200ec83](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/b459db13-e82f-4761-ae47-98364833b89d)

### Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
### Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
### Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
### Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:
![280711086-88778d03-2834-4b39-be9f-12a068a03957](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/0f095d15-1746-4cd7-90d3-949ec20e5984)


### OUTPUT:
![280714057-61a5dd86-1dbd-499a-ad3a-e875fad7700c](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/f54e12a3-e8fe-4a19-8a67-aad023863cf0)

### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
![280714139-0a797b0c-6a71-411d-b8cc-1b75a5bcb5a1](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/0193f72f-a3a0-4233-abcd-582730e166ce)


### OUTPUT:
![280711401-cb1c45ac-f2f8-46f5-8da0-856e1a076c75](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/4bb512a9-3815-4c34-9577-b83c5653721a)

### Q9) Perform Natural join on both tables

### QUERY:
![280711400-0107b98f-9158-44c8-83c4-be82aab13c52](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/3d0409c7-3af9-4e05-aa4e-eb6d48bb564f)


### OUTPUT:
![280711399-ef2d21b0-d921-4faf-a8ce-0d0eddde5f7c](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/8bda9a17-ec4f-4b16-9609-0a2ffffb565d)

### Q10) Perform Left and right join on both tables

### QUERY:
## LEFT JOIN:
![280712373-674a9084-24cf-4eed-96e2-9a141ae4460a](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/0e15ddd6-dab4-4bb1-a152-1d13989dcd23)

## Right join:
![280712529-0684b670-3f58-440f-93a8-f35a674762d5](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/502ae8e9-3a54-41d2-b6f6-ff54cd09a868)



### OUTPUT:
## Left Join:
![280712810-b800743b-54a9-4ae0-b84d-ab7d5a462468](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/94cd6d95-ca62-4bac-9ff6-df66d615fb0c)

## Right join:
![280712919-30daf374-09e9-4e3c-9b0b-8ea87cfb4446](https://github.com/MaithreyanDinakaran/EX-3-SubQueries-Views-and-Joins/assets/119104032/531df71f-28f8-4fad-b484-13351a1d9a7c)

## RESULT:
Thusthe Subqueries,Views and Joins are created.
