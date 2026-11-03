# SQL Practice - Day 1
## Running MySQL
- SQL is a language used to talk to a database server.
- MySQL is a database server.
- phpMyAdmin is a webpage that lets you talk to SQL.
- XAMPP is a package that bundles Apache (a web server), MySQL (a database sever), and PHP.
- Steps:
    1. Open XAMPP control panel and Start Apache (to run phpMyAdmin) and MySQL (for the database server).
    2. Open phpMyAdmin in your browser via the link `http://localhost/phpmyadmin`
    3. Create a new database folder by clicking the `New` button on the sidebar of the webpage.
## Data Types and Extras
- Data Types
    1. INT - numbers    

            student_id INT
    2. VARCHAR - string of characters and specifies the maximum number of characters allowed

            full_name VARCHAR(20)
    3. DATE - date in year-month-day format

            birthdate DATE
- Extras
    - PRIMARY KEY - signifies that the column is the unique identifier for the entity
    - AUTO_INCREMENT - adds 1 for every instance of the entity
    
            student_id INT AUTO_INCREMENT PRIMARY KEY
## Creating Table
- Code format:

        CREATE TABLE [table name] (
            [column_name] [type] [extras],
            [column_name] [type] [extras]
        );
- The table represents a storage for an entity, a real world object.
- The columns is the header and represents the attributes of that entity.
- Steps:
    1. Go to `SQL` tab
    2. Enter the code for your table.

            Example:
            CREATE TABLE student (
                student_id INT AUTO_INCREMENT PRIMARY KEY,  
                full_name VARCHAR(50),
                birthdate DATE
            );
    3. Click `Go` at the bottom (scroll down).
## Inserting Rows
- Code format:

        INSERT INTO [table name]([column name], [column name]) VALUES ([value], [value]), ([value], [value]);
- Each row represents an instance of that entity.
- Specify the column names and match the values in arrangement.
- You can add multiple rows at once by separating them using comma, just like in the format above.
- Texts and dates should be wrapped in quotes.
- Leave out auto increment columns as MySQL fills it in automatically.
- Steps:
    1. Go to `SQL` tab
    2. Enter the code for your row.

            Example:
            INSERT INTO student(full_name, birthdate) VALUES ('Jethro Elano', '2008-12-15');
    3. Click `Go` at the bottom (scroll down).
## Selecting Data
- Code format:

        SELECT [column name] FROM [table name];
- This is used to select, gather, extract, or show data for each row and column.
- You can use `*` to select all columns.
- Steps:
    1. Go to `SQL` tab
    2. Enter the code for your selection.

            Example:
            SELECT * FROM student;  -- selects all columns and shows 
            SELECT full_name FROM student;
    3. Click `Go` at the bottom (scroll down).