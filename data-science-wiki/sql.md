# SQL Basics for GitHub Notebook 📘
##### Created by @jl33-ai 👦🏻

## Introduction 📑 

Structured Query Language (SQL) is a standard Database language which is used to create, maintain and retrieve the data from relational databases like MySQL, Oracle, SQL Server, PostGre, etc. 
Almost all major DBMS support SQL as standard database language.

## 🏁 Getting Started: 

1. 🌐 **Installation** - There are many SQL platforms available such as MySQL, Oracle, MSSQL. Choose one that best suits your needs and install the related software. For beginners, most often used is MySQL.
2. 💻 **IDE** - You can use any text editor to write your SQL queries, but it's recommended to use IDE's such as MySQL Workbench or DBeaver where you can simply run your queries.

## Core SQL Operations 🛠 

#### 👉 Basics: 

```markdown
*'*' - Select all elements.
'FROM' - The table to query from.
```

#### 👉 Select: 
```markdown
*Example*  
SELECT column1, column2  
FROM table_name;

```

#### 👉 Insert:
```markdown
*Example*  
INSERT INTO table_name (column1, column2, column3)  
VALUES (value1, value2, value3);
```

#### 👉 Update:
```markdown
*Example*  
UPDATE table_name  
SET column1=value1, column2=value2  
WHERE some_column=some_value;
```

#### 👉 Delete:
```markdown
*Example*  
DELETE FROM table_name  
WHERE some_column=some_value;
```

## SQL Constraints ⛓ 

Constraints are used to limit the type of data that can go into a table. This ensures the accuracy and reliability of the data in the table. If there is any violation between the constraint and the data action, the action is aborted. Constraints can be column level or table level.

#### 👉 Types of Constraints in SQL:

1. NOT NULL Constraint
2. UNIQUE Constraint
3. PRIMARY Key
4. FOREIGN Key
5. CHECK Constraint
6. DEFAULT Constraint

#### 👉 Usage of Constraints:
```markdown
*Example of NOT NULL constraint*  
CREATE TABLE Customers (  
CustomerID INT NOT NULL,  
CustomerName VARCHAR (255) NOT NULL,  
ContactName VARCHAR (255),  
Country VARCHAR (255),  
City VARCHAR (255)  
);
```

## Conclusion 📝 

SQL is a very important skill for anyone in IT or Data related fields. This guide is just a starting point, to proceed further, one should try to learn more complex SQL statements, try out different queries, and perfect their skills with practice.
