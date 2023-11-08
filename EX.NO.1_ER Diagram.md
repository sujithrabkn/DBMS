# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE : 10-08-2023
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![image (3)](https://github.com/sujithrabkn/DBMS/assets/119477857/ab9284ec-e7f2-4b64-b48b-c449b6e3ebf4)


### Relational model
![image (4)](https://github.com/sujithrabkn/DBMS/assets/119477857/079f8c66-2d8a-40db-8460-ec437fb0068b)


### SQL DDL Schema 
```
CREATE TABLE Bank
(
  Name INT NOT NULL,
  Code INT NOT NULL,
  Address INT NOT NULL,
  PRIMARY KEY (Code)
);

CREATE TABLE Branch
(
  Branch_id INT NOT NULL,
  Name INT NOT NULL,
  Address INT NOT NULL,
  PRIMARY KEY (Branch_id)
);

CREATE TABLE Loan
(
  Loan_id INT NOT NULL,
  Loan_type INT NOT NULL,
  Amount INT NOT NULL,
  PRIMARY KEY (Loan_id),
  UNIQUE (Loan_type)
);

CREATE TABLE Account
(
  Account_No INT NOT NULL,
  Account_Type INT NOT NULL,
  Balance INT NOT NULL,
  PRIMARY KEY (Account_No),
  UNIQUE (Account_Type)
);

CREATE TABLE Customer
(
  Customer_id INT NOT NULL,
  Name INT NOT NULL,
  Phone INT NOT NULL,
  Address INT NOT NULL,
  PRIMARY KEY (Customer_id)
);
```

## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
