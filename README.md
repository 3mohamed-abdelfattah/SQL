# SQL Commands Repository

## Overview

This repository is dedicated to providing comprehensive examples and explanations of SQL commands, organized by their types: DDL (Data Definition Language), DQL (Data Query Language), DML (Data Manipulation Language), DCL (Data Control Language), and TCL (Transaction Control Language). This resource is designed to help both beginners and experienced developers improve their understanding and skills in SQL.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [SQL Command Types](#sql-command-types)
  - [DDL (Data Definition Language)](#ddl-data-definition-language)
  - [DQL (Data Query Language)](#dql-data-query-language)
  - [DML (Data Manipulation Language)](#dml-data-manipulation-language)
  - [DCL (Data Control Language)](#dcl-data-control-language)
  - [TCL (Transaction Control Language)](#tcl-transaction-control-language)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)

## Prerequisites

Before you begin, ensure you have met the following requirements:

- You have a SQL database management system installed (e.g., MySQL, PostgreSQL, SQLite).
- You have a basic understanding of SQL and database concepts.
- You have a text editor or an IDE (e.g., VS Code, PyCharm).


## Usage

1. Open your SQL client (e.g., MySQL Workbench, pgAdmin) and connect to your database.

2. Load the SQL scripts from the repository to create and populate your database.

3. Follow the tutorials and examples provided in the repository to practice and improve your SQL skills.

## SQL Command Types

### DDL (Data Definition Language)

DDL commands are used to define the structure of the database schema. Examples include:

- **CREATE**: Used to create a new table, view, or other database objects.

    ```sql
    -- Example: Creating a new table
    CREATE TABLE employees (
        id INT PRIMARY KEY,
        name VARCHAR(100),
        department VARCHAR(50)
    );
    ```

- **ALTER**: Used to modify an existing database object.

    ```sql
    -- Example: Adding a new column to a table
    ALTER TABLE employees
    ADD salary DECIMAL(10, 2);
    ```

- **DROP**: Used to delete an existing database object.

    ```sql
    -- Example: Dropping a table
    DROP TABLE employees;
    ```

- **TRUNCATE**: Used to remove all records from a table, but the structure remains.

    ```sql
    -- Example: Truncating a table
    TRUNCATE TABLE employees;
    ```

### DQL (Data Query Language)

DQL commands are used to query the database and retrieve data. The primary DQL command is:

- **SELECT**: Used to retrieve data from the database.

    ```sql
    -- Example: Selecting data from a table
    SELECT * FROM employees WHERE department = 'IT';
    ```

### DML (Data Manipulation Language)

DML commands are used to manipulate the data within the database. Examples include:

- **INSERT**: Used to add new records to a table.

    ```sql
    -- Example: Inserting new records into a table
    INSERT INTO employees (id, name, department)
    VALUES (1, 'John Doe', 'IT'),
           (2, 'Jane Smith', 'HR');
    ```

- **UPDATE**: Used to modify existing records in a table.

    ```sql
    -- Example: Updating records in a table
    UPDATE employees
    SET department = 'Finance'
    WHERE id = 2;
    ```

- **DELETE**: Used to remove records from a table.

    ```sql
    -- Example: Deleting records from a table
    DELETE FROM employees
    WHERE id = 1;
    ```

### DCL (Data Control Language)

DCL commands are used to control access to data within the database. Examples include:

- **GRANT**: Used to give privileges to users.

    ```sql
    -- Example: Granting privileges to a user
    GRANT SELECT, INSERT ON employees TO user1;
    ```

- **REVOKE**: Used to remove privileges from users.

    ```sql
    -- Example: Revoking privileges from a user
    REVOKE INSERT ON employees FROM user1;
    ```

### TCL (Transaction Control Language)

TCL commands are used to manage transactions in the database. Examples include:

- **COMMIT**: Used to save all changes made during the current transaction.

    ```sql
    -- Example: Committing a transaction
    COMMIT;
    ```

- **ROLLBACK**: Used to undo changes made during the current transaction.

    ```sql
    -- Example: Rolling back a transaction
    ROLLBACK;
    ```

- **SAVEPOINT**: Used to set a point within a transaction to which you can later roll back.

    ```sql
    -- Example: Creating a savepoint
    SAVEPOINT sp1;
    ```

## Contributing

Contributions are always welcome! If you have any suggestions, bug reports, or improvements, please:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

Please ensure your contributions adhere to the coding standards and best practices.

## Acknowledgements

- [SQLBolt](https://sqlbolt.com/) for SQL tutorials and exercises.
- [W3Schools](https://www.w3schools.com/sql/) for comprehensive SQL documentation.
- [Stack Overflow](https://stackoverflow.com/) for community support and solutions.
