# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE: 07-09-2023
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## Data Control Language (DCL) commands
* Data control language (DCL) is used to access the stored data.
* It is mainly used for revoke and to grant the user the required access to a database.
## List of DCL commands: 
1. GRANT : It is used to insert data into a table.
2. REVOKE: It is used to update existing data within a table.
## Transaction control language(TCL) commands
1. COMMIT : COMMIT command in SQL is used to save all the transaction-related changes permanently to the disk
2. START TRANSACTION : to start the transaction
3. ROLLBACK : undo the transaction upto savepoint 
4. SAVEPOINT : create a savepoint to save the different parts of the same transaction using different names

### Q1) Create a table employee with employee id ,name and Address

### QUERY:
```
sql
create table employee(
emp_id numeric,
emp_name varchar(10),
addr varchar(40)
);
```
### OUTPUT:
![276302151-56bbda44-a582-42e3-9738-5b1d035dd675](https://github.com/sujithrabkn/DBMS/assets/119477857/4d362289-94b4-4359-8bd0-01a80448e79f)

### Q2) Insert three rows into emploee table 


### QUERY:
```
sql
insert into employee values(1,'Luffy','EastBlue');
insert into employee values(2,'Shanks','GodValley');
insert into employee values(3,'Grap','MarinFord');
```
### OUTPUT:
![276302974-db081e71-759d-44df-b847-75294a2e2a34](https://github.com/sujithrabkn/DBMS/assets/119477857/876b5a28-a9d0-4a0a-b6b0-1c17ee0b82f3)

### Q3) Start the transaction and create a save point s1.

### QUERY:
```
sql
savepoint A;
```
### OUTPUT:
![276303398-d491985f-d652-4510-baba-69bda39920c4](https://github.com/sujithrabkn/DBMS/assets/119477857/9c9c462e-f1ce-404f-a392-81d4f967690b)

### Q4) Perform insertion into employee table.

### QUERY:
```
sql
insert into employee(4,'Robin','EniesLobby');
```
### OUTPUT:
![276303961-b9d81949-f840-4fb4-8427-6c5efb79da74](https://github.com/sujithrabkn/DBMS/assets/119477857/57aa6753-be4d-45b8-9b7a-e1a015f61e1e)


### Q6)	Display the employee table and create a save point s2 .


### QUERY:
```
sql
select * from employee;
savepoint s2;
```
### OUTPUT:

![276304509-bc86bb69-d7ad-4193-aeda-050214882984](https://github.com/sujithrabkn/DBMS/assets/119477857/71ff621d-bc0f-4a9f-a462-070f65583815)

### Q7)	Perform updation on any one of the row.


### QUERY:
  ```
sql
update employee set emp_name='Nico Robin' where emp_id=4;
```
### OUTPUT:

![276305358-2e9e6855-56ea-40f4-ba36-56f8eafd68ee](https://github.com/sujithrabkn/DBMS/assets/119477857/7444fbbc-fc5c-4b6d-957d-2c74c7984f86)

### Q8) Display the employee table and rollback to  save point s2 


### QUERY:
```
sql
select * from employee;
rollback to s2;
```
### OUTPUT:

![276305855-b66b2852-7cbc-49e6-a059-579485f3ff49](https://github.com/sujithrabkn/DBMS/assets/119477857/e6dc43c5-fc57-4e0a-8722-89e5fe244824)

### Q9) Display the employee table and commit the changes; 


### QUERY:
```
sql
select * from employee;
commit;
```
### OUTPUT:

![276306207-7dd55645-f515-4c5b-9174-1b3a9bc24e30](https://github.com/sujithrabkn/DBMS/assets/119477857/5efc55b3-da5c-4724-bfb9-a5844b65a9af)

### Q10) Rollback to save point s1;


### QUERY:
```
sql
rollback to A;
```
### OUTPUT:

![276306832-441afff5-9f95-418b-ad8b-c2b5cfbf810d](https://github.com/sujithrabkn/DBMS/assets/119477857/9393379d-bec6-422b-8602-1337f9e17294)

### Q11)	Create a new user and grant access to any one database with "insert and update"


### QUERY:
```
CREATE USER new_user;
GRANT INSERT, UPDATE ON database_name TO new_user;
```
### OUTPUT:
![281134636-3c3761a5-28c0-4c83-a203-89e0087e6676](https://github.com/sujithrabkn/DBMS/assets/119477857/0e57e576-b9aa-4bbf-910f-19dd06d736b5)

![281134796-fd08ac3a-d1a5-4a16-af6a-f3bc5ff24629](https://github.com/sujithrabkn/DBMS/assets/119477857/1173bad7-a928-4b08-80a0-9313cec335d8)

### Q12) Check the user access and display the result 


### QUERY:
```
SHOW GRANTS FOR new_user;
```
### OUTPUT:
![281134999-2fbd5d94-7610-4828-a072-c84372c06442](https://github.com/sujithrabkn/DBMS/assets/119477857/bee829c6-eebe-4314-bf97-3bd4bf3d8233)

### Q13) Revoke the privillages.

### QUERY:
```
SHOW GRANTS FOR new_user;
REVOKE INSERT, UPDATE ON database_name FROM new_user;
SHOW GRANTS FOR new_user;
```
### OUTPUT:
![281136125-bd4b2b58-817e-42ea-b84d-a59af0382c11](https://github.com/sujithrabkn/DBMS/assets/119477857/46b8bcfc-01f7-48ce-b45d-d7b2b6541cc3)


## RESULT :
Thus the basic TCL and DCL commands are executed.
