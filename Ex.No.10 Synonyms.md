# EXP NO 08: SYNONYMS AND ASSERTIONS IN SQL 
### DATE: 12-10-2023
## AIM:
To create a student database and create a synonym and assertions.

## THEORY
## SYNONYM
<div align="justify">
A SYNONYM provides another name for database object, referred to as original object, that may exist on a local or another server.
</div>
## ASSERTIONS
<div align="justify">
* An assertion is a piece of SQL which makes sure a condition is satisfied, else or it stops the action being taken on a database.
* An assertion is a constraint that might be dependent upon multiple rows of multiple tables.
</div>

## Query:
### 1) Create a table EMPLOYEE and perform insertion of two rows.

### SQL QUERY: 
```
CREATE TABLE EMPLOYEE (
    employee_id INT ,
    name VARCHAR(255),
    department VARCHAR(255),
    salary DECIMAL(10, 2)
);
```
### OUTPUT:
![277110918-71b5a740-3ed6-400c-a81e-55b48f5a29f8](https://github.com/sujithrabkn/DBMS/assets/119477857/e1cd3ae0-4066-4222-b09a-40618da6c97c)
![277111028-f4d76026-48c5-4d61-a806-4befa6e93d93](https://github.com/sujithrabkn/DBMS/assets/119477857/b6893a85-8b42-4ee6-8441-99b0b3fdc2a4)

### 2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY: 
```
CREATE SYNONYM S1 FOR EMPLOYEE;
```
### OUTPUT:

![277111055-b455ceaa-8657-442e-b801-a7c7b7e87b67](https://github.com/sujithrabkn/DBMS/assets/119477857/c0a2b101-bacd-4a49-92be-cdcb54fbc98d)

### 3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
```
SELECT * FROM S1;
```
### OUTPUT:

![277111121-6919a5b8-9f79-4180-a956-3df97ee88b03](https://github.com/sujithrabkn/DBMS/assets/119477857/43bd127b-269d-4c53-bf1e-3aa5e5a12747)

### 4) Drop the synonym.

### SQL QUERY: 
```
DROP SYNONYM S1;
```
### OUTPUT:

![277111169-6368462e-e8b5-4451-8364-19a41290c302](https://github.com/sujithrabkn/DBMS/assets/119477857/d28166a8-7e4a-433f-8b26-f9654a33ac1e)


### 5) Create a supplier table and create a sequence S2 for supplier table id.

### SQL QUERY: 
```
CREATE TABLE supplier (
    id INT,
    name VARCHAR(255),
    address VARCHAR(255),
    contact_person VARCHAR(255)
);

CREATE SEQUENCE S2 START 1;
```
### OUTPUT:

![277111203-6941eec5-a29d-49f2-b642-9faa553c5710](https://github.com/sujithrabkn/DBMS/assets/119477857/c33b1941-1604-4483-a6de-292d77cdb187)
![277111228-4fd3c19f-6eb2-433a-b260-cb701ca8daac](https://github.com/sujithrabkn/DBMS/assets/119477857/0a37b3fd-3110-439b-ab2f-ae6dfcaf5bde)

### 6) insert the data into supplier table use sequence.

### SQL QUERY: 
```
INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'ABC Suppliers', '123 Main Street', 'John Doe');

INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'XYZ Distributors', '456 Elm Road', 'Jane Smith');
```
### OUTPUT:
![277111446-2f779d72-49da-4e24-8749-575d5625a31b](https://github.com/sujithrabkn/DBMS/assets/119477857/5c8ee483-26b7-485c-ad71-87eddc5ff686)

### 7) Drop the sequence

### SQL QUERY: 
```
DROP SEQUENCE S2;
```
### OUTPUT:
![277111327-bde530b6-caf5-48e6-96a6-e32d87846e74](https://github.com/sujithrabkn/DBMS/assets/119477857/0fc8b672-c085-4a03-9f7d-16d72fda6859)

### RESULT :
Thus the sequence and synonym created and used in SQL.
