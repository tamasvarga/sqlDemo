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
