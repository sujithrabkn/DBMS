# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE : 17-08-2023
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
create database student_db;
```
### OUTPUT:
![280927112-afb1fb7d-977c-441f-a8ea-5c9e7d10e7cc](https://github.com/sujithrabkn/DBMS/assets/119477857/58a35d5e-ef98-40d7-a9d4-0a692a79fe07)

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
create table student(Regno int, Name varchar(20),Age int,Address varchar(50),Phonenumber varchar(10));
```

### OUTPUT:
![280927652-35ec9dce-e676-4dee-8fe9-b95e8db3c07e](https://github.com/sujithrabkn/DBMS/assets/119477857/20caef92-38af-425e-9a25-8e6413d4d273)

### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
alter table student add dept varchar(20);
```
### OUTPUT:

![280927915-fc795c4a-ff2d-4373-9d5e-29e0970b7e9f](https://github.com/sujithrabkn/DBMS/assets/119477857/b0eb3496-34a7-4186-b505-cfb28b7664b0)

### 4) Rename the student table to mystudent

### SQL QUERY: 
```
rename table student to mystudent;
```


### OUTPUT:
![280928382-7b0162da-97de-4979-a38b-9f27ab267433](https://github.com/sujithrabkn/DBMS/assets/119477857/056f6082-cfe9-4266-a121-d9dbbd2cf31d)

### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
truncate table mystudent;
```

### OUTPUT:
![280930875-6ac30209-4af2-47b5-88ba-4cf3d1c518ce](https://github.com/sujithrabkn/DBMS/assets/119477857/19b022f9-cbdd-42dc-9688-f4f14499cb7d)

### 4) Drop the mystudent table
 
### SQL QUERY: 
```
drop table mystudent;
```

### OUTPUT:

![280931508-ebb895b1-8b0c-4bb2-bbc5-81e7e9df2042](https://github.com/sujithrabkn/DBMS/assets/119477857/a44c5541-c1d5-4c33-aacf-41e28054a15c)

## Result:

Thus the basic DDL commands in SQL are executed. 


