
	### Az összes alkalmazott minden adata
```SQL
SELECT * FROM Employee
``` 
### Azok  az  alkalmazottak,  aki  többet  keresnek  mint  10 000 Ft.

```SQL
SELECT * FROM Employee
WHERE Salary > 10000
``` 
###  Azok  az  alkalmazottak,  aki  többet  keresnek  mint  10 000 Ft, de kevesebbet mint 20 000 Ft
```SQL
SELECT * FROM Employee
WHERE Salary BETWEEN 10000 AND 20000; --Inclusive

SELECT * FROM Employee
WHERE Salary > 10000 AND Salary < 20000 -- Exclusive
``` 
###  Azok  az  alkalmazottak,  aki  többet  keresnek  mint  10 000 Ft,  vagy kevesebbet, mint 5000
```SQL
SELECT * FROM Employee
WHERE Salary > 10000 OR Salary < 5000
``` 
### Az összes alkalmazott minden adata
```SQL
SELECT * FROM Employee
``` 
### Azok  az  alkalmazottak,  aki  többet  keresnek  mint  10 000 Ft.

```SQL
SELECT * FROM Employee
WHERE Salary > 10000
``` 
###  Azok  az  alkalmazottak,  aki  többet  keresnek  mint  10 000 Ft, de kevesebbet mint 20 000 Ft
```SQL
SELECT * FROM Employee
WHERE Salary BETWEEN 10000 AND 20000; --Inclusive

SELECT * FROM Employee
WHERE Salary > 10000 AND Salary < 20000 -- Exclusive
``` 
###  Azok  az  alkalmazottak,  aki  többet  keresnek  mint  10 000 Ft,  vagy kevesebbet, mint 5000
```SQL
### Az összes alkalmazott minden adata
```SQL
SELECT * FROM Employee
``` 
### Azok  az  alkalmazottak,  aki  többet  keresnek  mint  10 000 Ft.

```SQL
SELECT * FROM Employee
WHERE Salary > 10000
``` 
###  Azok  az  alkalmazottak,  aki  többet  keresnek  mint  10 000 Ft, de kevesebbet mint 20 000 Ft
```SQL
SELECT * FROM Employee
WHERE Salary BETWEEN 10000 AND 20000; --Inclusive

SELECT * FROM Employee
WHERE Salary > 10000 AND Salary < 20000 -- Exclusive
``` 
###  Hány keresnek 10 000 Ft felett?
```SQL
SELECT COUNT(*) FROM Employee
WHERE Salary > 10000;

SELECT COUNT(ID) FROM Employee
WHERE Salary > 10000;
``` 
### Hány különböző bérű alkalmazott van?
```SQL
SELECT Salary FROM Employee
SELECT DISTINCT Salary FROM Employee
SELECT COUNT(Salary) FROM Employee
SELECT COUNT(DISTINCT Salary) FROM Employee
```
### Mennyi a bérek átlaga, minimuma, maximuma?
```SQL
SELECT AVG(Salary), MIN(Salary), MAX(Salary) FROM Employee
```

### Alkalmazottak bérek szerint rendezve (Csökkenő, Növekvő)
```SQL
SELECT * FROM Employee
ORDER BY Salary DESC

SELECT * FROM Employee
ORDER BY Salary ASC
``` 
###  Hányan dolgoznak az egyes osztályokon?
```SQL
SELECT DepartmentId, COUNT (Id) AS Dologzok_Szama FROM Employee
GROUP BY DepartmentId
```
### Mennyi az átlagfizetés az egyes osztályokon?

```SQL
SELECT DepartmentId, AVG (Salary) FROM Employee
GROUP BY DepartmentId
```
### Azok az osztályok, ahol az átlagfizetés több, mint 10 000 Ft.
```SQL
SELECT DepartmentId, COUNT(ID) FROM Employee
GROUP BY DepartmentId
HAVING AVG (Salary) > 10000
```

