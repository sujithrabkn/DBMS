# Ex. No: 10 PL/SQL program using Triggers 
### DATE: 26-10-2023
### AIM: 
To create PL/SQL program to display new and old salary of customer when before/ after updation takes place. 

### Steps:
1. Create a trigger for each row when updation occurs.
2. Declare the variable in Declare section.
3. Start the begin section.
4. Calculate the salary changes.
5. Display the result 
6. End the begin section.

### Program:
```
CREATE TABLE employed(
  empid NUMBER,
  empname VARCHAR2(10),
  dept VARCHAR2(10),
  salary NUMBER
);

CREATE TABLE sal_log (
  log_id NUMBER GENERATED ALWAYS AS IDENTITY,
  empid NUMBER,
  empname VARCHAR2(10),
  old_salary NUMBER,
  new_salary NUMBER,
  update_date DATE
);
```

```
-- Create the trigger
CREATE OR REPLACE TRIGGER log_sal_update
BEFORE UPDATE ON employed
FOR EACH ROW
BEGIN
  IF :OLD.salary != :NEW.salary THEN
    INSERT INTO sal_log (empid, empname, old_salary, new_salary, update_date)
    VALUES (:OLD.empid, :OLD.empname, :OLD.salary, :NEW.salary, SYSDATE);
  END IF;
END;
/
-- Insert the values in the employee table
insert into employed values(1,'GOJO','HR',100000);
insert into employed values(2,'Yuta','SALES',500000)


-- Update the salary of an employee
UPDATE employed
SET salary = 60000
WHERE empid = 1;
-- Display the employee table
SELECT * FROM employed;

-- Display the salary_log table
SELECT * FROM sal_log;
```
### Output:
![277101485-649492a9-f73e-4d34-a8e9-49a1549896d7](https://github.com/sujithrabkn/DBMS/assets/119477857/edb1e993-7a2d-4e9a-b3f2-047415a27dc4)

![277101521-9028742a-5375-4170-9d83-0ddcd998a6f0](https://github.com/sujithrabkn/DBMS/assets/119477857/f115912e-41d6-4243-b133-1683283dab2e)

![277101530-8aba2177-395e-425e-8fb1-a5f9fd0e6994](https://github.com/sujithrabkn/DBMS/assets/119477857/de91fa7e-08be-42ab-b3f4-862c66eb6cc9)

### Result:
Thust the program was performed sucessfully.
