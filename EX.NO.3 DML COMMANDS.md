# EX 3 Data Manipulation Language (DML) Commands and built in functions in SQL

### DATE : 24-08-2023
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
update manager set salary=salary+(salary*0.10);
### OUTPUT:
![280975522-05a37c0e-a6da-43d2-91c8-88ceeee8448f](https://github.com/sujithrabkn/DBMS/assets/119477857/e6b5fc2f-08e2-4776-ad1c-27373a7538ee)

### Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:

delete from manager where salary<2750;

### OUTPUT:
![280975677-fc282edd-1c38-479d-a032-5179e38b686c](https://github.com/sujithrabkn/DBMS/assets/119477857/45431301-6a50-4380-83aa-f85aeaf0e553)

### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
select ename as "Name",salary*12 as "Annual salary" from manager;

### OUTPUT:
![280975783-b7fe2085-486e-430a-8061-6e7232c2143d](https://github.com/sujithrabkn/DBMS/assets/119477857/0ab6d1e1-a825-4e68-af15-3a0f9d62850e)

### Q4)	List the names of Clerks from emp table.


### QUERY:
select ename from manager where designation='clerk';

### OUTPUT:
![280975849-4ef98158-9ca7-4489-9191-b7ec33c40858](https://github.com/sujithrabkn/DBMS/assets/119477857/43780dcf-5da4-4276-ab7a-5e785c2c36ca)


### Q5)	List the names of employee who are not Managers.


### QUERY:
select ename from manager where designation <> 'manager';

### OUTPUT:

![280976025-0464eced-a962-4239-8a26-0955f7d621a8](https://github.com/sujithrabkn/DBMS/assets/119477857/e2ed2506-873c-4180-8dc8-ad860aa0587a)

### Q6)	List the names of employees not eligible for commission.


### QUERY:
select ename from manager where commission=0;

### OUTPUT:

![280976194-e75c20b1-18d3-42e8-bddb-bd284a5f7f77](https://github.com/sujithrabkn/DBMS/assets/119477857/70366c62-76b8-453a-b210-76355d1de005)

### Q7)	List employees whose name either start or end with ‘s’.


### QUERY:
select ename from manager where ename like '%s' or ename like 's%';

### OUTPUT:

![280976317-d1beae0d-6feb-4919-8c1d-2ded2bf20a5d](https://github.com/sujithrabkn/DBMS/assets/119477857/0e1b489c-2f68-46f8-8fe2-cfb2bf46a8f4)

### Q8) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
select ename,designation as "job",deptno,hiredate from manager order by hiredate asc;

### OUTPUT:

![280976429-22d643d9-88fb-4e71-93cf-31d5c963c9ee](https://github.com/sujithrabkn/DBMS/assets/119477857/3f8dfedb-9a9a-4db9-9c21-e37c452af571)

### Q9) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');

### OUTPUT:

![280976496-f4fa653f-2463-4180-a5be-2db3b02e0a50](https://github.com/sujithrabkn/DBMS/assets/119477857/0d7e32d7-1da8-4155-a209-49ab66136c1b)

### Q10)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
select ename,deptno,salary from manager order by deptno asc,salary desc;

### OUTPUT:

![280976556-d648feda-5f03-4bc4-9c27-e9fa17a1f84b](https://github.com/sujithrabkn/DBMS/assets/119477857/d40dcffe-81d4-442f-ba72-278a29cf0bdf)

### Q11) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
select ename from manager where deptno not in (30,40,10);

### OUTPUT:
![280976646-aeb20207-0520-40de-a2cd-21cdce341715](https://github.com/sujithrabkn/DBMS/assets/119477857/39608478-9b54-4f4c-847b-bfb5f83a35bb)

### Q12) Find number of rows in the table EMP

### QUERY:
select count(*) from manager;

### OUTPUT:

![280976782-aba95e8b-198b-4fc1-a563-59648d96f941](https://github.com/sujithrabkn/DBMS/assets/119477857/364142fe-22a6-4a59-a991-f9defd3fb993)

### Q13) Find maximum, minimum and average salary in EMP table.

### QUERY:

select max(salary) from manager;

select min(salary) from manager;

select avg(salary) from manager;

### OUTPUT:

![280976957-161961c6-9223-4d4e-8f94-cb1deaa69509](https://github.com/sujithrabkn/DBMS/assets/119477857/646e2f61-5a29-45c2-ba09-22bbc15af149)
![280995504-87197178-e5b6-4665-a065-0a3aa0f49626](https://github.com/sujithrabkn/DBMS/assets/119477857/ad9b2416-81c6-4222-8528-edc1b0bc54bb)
![280995898-386c64eb-c820-4096-abc3-099d6fd9fa43](https://github.com/sujithrabkn/DBMS/assets/119477857/c9a0bb59-a7d4-4046-a5cb-bf8f7b073b2d)

### Q14) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
SELECT designation AS job, COUNT(*) AS num_employees FROM manager GROUP BY designation ORDER BY num_employees DESC;

### OUTPUT:

![280995987-eb8d1370-c455-4a2b-9401-501d832e0c31](https://github.com/sujithrabkn/DBMS/assets/119477857/cf72e41e-be79-4f71-811f-b25014a7ba8b)

## RESULT :
Thus the basic DML commands are executed.
