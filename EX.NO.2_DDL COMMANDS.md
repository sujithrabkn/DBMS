# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb

### SQL QUERY:
```
Create database studentdb; 
use studentdb;
```
### OUTPUT:

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
Create table student(RegNum int,Name varchar(30),Age int,Address varchar(20),PhoneNumber int);
insert into student values(212222230001,'AAA',18,'xxx',1234567890);
insert into student values(212222230002,'BBB',19,'yyy',9876543210);
```

### OUTPUT:
![Screenshot 2023-10-19 093836](https://github.com/sujithrabkn/DBMS/assets/119477857/372ecc22-b7c5-45b9-a0bf-07d245f9c2af)
![Screenshot 2023-10-19 093843](https://github.com/sujithrabkn/DBMS/assets/119477857/5d694ac0-37f0-4fd5-ada8-853f86117e57)

### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
ALTER TABLE student 
ADD department VARCHAR(255);
```
### OUTPUT:
![Screenshot 2023-10-19 093850](https://github.com/sujithrabkn/DBMS/assets/119477857/1d72986e-7ac3-40da-b7f8-56d381567b00)

### 4) Rename the student table to mystudent

### SQL QUERY: 
```
ALTER TABLE student RENAME TO mystudent;
```


### OUTPUT:
![Screenshot 2023-10-19 093856](https://github.com/sujithrabkn/DBMS/assets/119477857/b6e30b95-67c2-404b-be59-cd5cf47ee808)

### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
TRUNCATE TABLE mystudent;
```

### OUTPUT:
![Screenshot 2023-10-19 093901](https://github.com/sujithrabkn/DBMS/assets/119477857/e7ac5b3e-139c-450e-b310-63a6559625f0)

### 4) Drop the mystudent table
 
### SQL QUERY: 
```
DROP TABLE mystudent;
```

### OUTPUT:


![Screenshot 2023-10-19 093906](https://github.com/sujithrabkn/DBMS/assets/119477857/98e17c98-059a-45db-8a20-55f0d4d4d424)






## Result:

         Thus the basic DDL commands in SQL are executed. 


