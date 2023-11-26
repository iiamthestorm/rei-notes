https://www.youtube.com/playlist?list=PLUaB-1hjhk8FE_XZ87vPPSfHqb6OcM0cF
# Basic SQL
### Installing microsoft sql
- SQL Server Management Studio: [https://docs.microsoft.com/en-us/sql/...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbnpCY1BSekxsWTgzSGFtbHg5Nmw5anEwVUFyd3xBQ3Jtc0trSkFmYWxNWU55M3NuSjMwNXYxQmc0d3FicFljamhkUzRCQno4dV81THhfUnpEVHJVM1VGbHJGYkdxSF9wNzlfLXU1RXJwN0FMQmFJSktYR3hlQVNFR0VZZmViVmRXVzhJOV9rNFpYb3BaZXF5ak82SQ&q=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fsql%2Fssms%2Fdownload-sql-server-management-studio-ssms%3Fview%3Dsql-server-ver15&v=RSlqWnP-Dy8) 
- SQL Server: [https://www.microsoft.com/en-us/sql-s...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbVpBY0ZJYjg5MXRqWFJGbk5pSFc4TFF0NExXUXxBQ3Jtc0ttM3NnZ2NXbjd5WGpVZ0Nna0xTZGcwOXFoTVJMSDJkcjNsdXp5eHgwRnkweEU0WHBaY003WkpjWjgzZUdEQTJjbnpmaHhrR2pZdXN6d1NrMnkxM2wwVUpKQWl4TkhfcmJnR0E4Y0t3UVlBdVcycV9GRQ&q=https%3A%2F%2Fwww.microsoft.com%2Fen-us%2Fsql-server%2Fsql-server-downloads&v=RSlqWnP-Dy8) 
- Github Scripts: [https://github.com/AlexTheAnalyst/SQL...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbWNDZGxGd2ZJN0FqOW5pX21IUy1FNWhTRDlPZ3xBQ3Jtc0tsRlh0NDV0T1lWVUlkT2puODlJTmN5ZE40eDh5ZHVNWVRJRGxRVThvVS1ac0c5RVlRYndLeGhHOUZhTk92VHRaZVg0ZUpwWUlMSzQyYmw5Zm5iR282dDZySDRyZTBEemVKMlU2ZGM0SjV2empmcnhKYw&q=https%3A%2F%2Fgithub.com%2FAlexTheAnalyst%2FSQL-Code%2Fblob%2Fmaster%2FSQL%2520Basics%2520Create%2520Table%2520and%2520Insert%2520Into&v=RSlqWnP-Dy8)
### Create Tables
CREATE TABLE EmployeeDemographics
(EmployeeID int,
FirstName varchar(50),
LastName varchar(50),
Age int,
Gender varchar(50)
)

CREATE TABLE EmployeeSalary
(EmployeeID int,
JobTitle varchar(50),
Salary int
)

INSERT INTO EmployeeDemographics VALUES
(1003, 'Dwight', 'Schrute', 29, 'Male'),
(1004, 'Angela', 'Martin', 31, 'Female'),
(1005, 'Toby', 'Flenderson', 32, 'Male'),
(1006, 'Michael', 'Scott', 35, 'Male'),
(1007, 'Meredith', 'Palmer', 32, 'Female'),
(1008, 'Stanley', 'Hudson', 38, 'Male'),
(1009, 'Kevin', 'Malone', 31, 'Male')

INSERT INTO EmployeeSalary VALUES
(1001, 'Salesman', 45000),
(1002, 'Receptionist', 36000),
(1003, 'Salesman', 63000),
(1004, 'Accountant', 47000),
(1005, 'HR', 50000),
(1006, 'Regional Manager', 65000),
(1007, 'Supplier Relations', 41000),
(1008, 'Salesman', 48000),
(1009, 'Accountant', 42000)
### Select + From Statements
SELECT *
FROM EmployeeDemographics

SELECT FirstName
FROM EmployeeDemographics

SELECT LastName
FROM EmployeeDemographics

SELECT TOP 5 FirstName, LastName
FROM EmployeeDemographics

SELECT DISTINCT(EmployeeID)
FROM EmployeeDemographics

SELECT DISTINCT(Gender)
FROM EmployeeDemographics

SELECT COUNT(Gender)
FROM EmployeeDemographics

SELECT COUNT(Gender) AS GenderCount
FROM EmployeeDemographics

SELECT MAX(Salary)
FROM EmployeeSalary

SELECT MIN(Salary)
FROM EmployeeSalary

SELECT AVG(Salary)
FROM EmployeeSalary

If you in the master, then:
SELECT *
FROM SQLTutorial.dbo.EmployeeSalary

### Where Statement
SELECT *
FROM EmployeeDemographics
WHERE FirstName = 'Jim'

SELECT *
FROM EmployeeDemographics
WHERE FirstName <> 'Jim'

SELECT *
FROM EmployeeDemographics
WHERE Age >= 30

SELECT *
FROM EmployeeDemographics
WHERE Age <= 30

SELECT *
FROM EmployeeDemographics
WHERE Age <= 30 AND Gender = 'Male'

SELECT *
FROM EmployeeDemographics
WHERE Age >= 30 OR Gender = 'Male'

SELECT * 
FROM EmployeeDemographics
WHERE FirstName LIKE '%A%'  -- Like a Wildcard

SELECT *
FROM EmployeeDemographics
WHERE FirstName IS NOT NULL

SELECT *
FROM EmployeeDemographics
WHERE FirstName IS NULL

SELECT *
FROM EmployeeDemographics
WHERE FirstName IN ('Pam', 'Michael')  -- IN is to choose multiple name that you want to be included

### Group By + Order By Statements
SELECT *
FROM EmployeeDemographics
ORDER BY 4 Desc, 5 Desc

SELECT Gender, COUNT(Gender) AS CountGender
FROM EmployeeDemographics
WHERE AGE > 31
GROUP BY Gender
## Intermediate SQL
### 