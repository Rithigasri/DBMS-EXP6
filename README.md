# EXPERIMENT 06:SET OPERATIONS
## AIM:
The aim of this program is to perform set operations (Union, Union All, Intersect, and Except) between two tables, A and B, in order to combine, find common elements, or identify differences between the tables.

## ALGORITHM:
1. Create table A with attributes ID and name.
2. Create table B with attributes ID and name.
3. Insert values into table A.
4. Insert values into table B.
5. Display the contents of table A.
6. Display the contents of table B.
7. Perform set operations: 
a. Union: Combine rows from table A and table B, eliminating duplicates. 
b. Union All: Combine rows from table A and table B, including duplicates. 
c. Intersect: Find common rows between table A and table B. 
d. Except: Find rows in table A that do not exist in table B.
8. Display the results of each set operation.
## PROGRAM:
```
create database if not exists MyDatabase;
use MyDatabase;
CREATE TABLE A (
  ID INTEGER PRIMARY KEY,
  name TEXT
);

CREATE TABLE B (
  ID INTEGER PRIMARY KEY,
  name TEXT
);

-- Insert values into table A
INSERT INTO A VALUES (1, 'John');
INSERT INTO A VALUES (2, 'Alice');
INSERT INTO A VALUES (3, 'Bob');

-- Insert values into table B
INSERT INTO B VALUES (2, 'Alice');
INSERT INTO B VALUES (3, 'Bob');
INSERT INTO B VALUES (4, 'Charlie');

-- Display table A
SELECT * FROM A;

-- Display table B
SELECT * FROM B;

SELECT * FROM A
UNION
SELECT * FROM B;

SELECT * FROM A
UNION ALL
SELECT * FROM B;

SELECT * FROM A
INSERTSET;
SELECT * FROM B;

SELECT * FROM A
EXCEPT
SELECT * FROM B;
```
## OUTPUT:
### The output for table A will be:
![image](https://github.com/Rithigasri/DBMS-EXP6/assets/93427256/a2c32d5c-8ce6-4e4f-938f-2d25e3f97965)

### The output for table B will be:
![image](https://github.com/Rithigasri/DBMS-EXP6/assets/93427256/3011f00e-9b1e-4137-8558-ef49d2dab164)

### Union:
![image](https://github.com/Rithigasri/DBMS-EXP6/assets/93427256/ad859187-d8cd-4b3b-bc25-66c8a6bf32e1)

### Union All:
![image](https://github.com/Rithigasri/DBMS-EXP6/assets/93427256/edab6aec-bcab-48c1-81da-3d81af8a7b8c)

### Intersect:
![image](https://github.com/Rithigasri/DBMS-EXP6/assets/93427256/cd584a26-2c72-44b8-9d73-a25bf3717dd7)

### Except:
![image](https://github.com/Rithigasri/DBMS-EXP6/assets/93427256/5f8d72a8-6326-401e-b492-95754dd8328c)

## RESULT:
These results illustrate the outcomes of the set operations performed on tables A and B.
