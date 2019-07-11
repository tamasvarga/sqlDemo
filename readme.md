### DDL
```SQL
CREATE TABLE Department( 
  Id int NOT NULL,
  Name char(50) NOT NULL,
  CONSTRAINT PK_Department PRIMARY KEY (ID)
);

CREATE TABLE Employee( 
  Id int NOT NULL,
  Name char(50) NOT NULL,
  Salary int, 
  DepartmentID int,
  CONSTRAINT PK_Employee PRIMARY KEY (Id),
  CONSTRAINT FK_Emplyee_Dapartment FOREIGN KEY (DepartmentID) REFERENCES Department(ID)
);

``` 

### DML

```SQL

INSERT INTO Department (Id, Name) VALUES (1, 'HR');
INSERT INTO Department (Id, Name) VALUES (2, 'Marketing');
INSERT INTO Department (Id, Name) VALUES (3, 'Delivery');



INSERT INTO Department (Id, Name) VALUES (1, 'HR');
INSERT INTO Department (Id, Name) VALUES (2, 'Marketing');
INSERT INTO Department (Id, Name) VALUES (3, 'Delivery');
INSERT INTO Department (Id, Name) VALUES (4, 'IT');


INSERT INTO Employee (Id, Name, Salary, DepartmentID) VALUES (1, 'Péter', 5000, 1);
INSERT INTO Employee (Id, Name, Salary, DepartmentID) VALUES (2, 'Csilla', 1000, 2);
INSERT INTO Employee (Id, Name, Salary, DepartmentID) VALUES (3, 'Dalma', 10000, 3);
INSERT INTO Employee (Id, Name, Salary, DepartmentID) VALUES (4, 'Karcsi', 5000, 2);
INSERT INTO Employee (Id, Name, Salary, DepartmentID) VALUES (5, 'Emese', 5000, 3);
INSERT INTO Employee (Id, Name, Salary, DepartmentID) VALUES (6, 'Lilla', 25000, 1);
INSERT INTO Employee (Id, Name, Salary, DepartmentID) VALUES (7, 'Kriszta', 13000, 2);
INSERT INTO Employee (Id, Name, Salary, DepartmentID) VALUES (8, 'Róbert', 27000, 3);
INSERT INTO Employee (Id, Name, Salary, DepartmentID) VALUES (9, 'Béla', 5000, 1);
INSERT INTO Employee (Id, Name, Salary) VALUES (10, 'Béla', 5000);
``` 
