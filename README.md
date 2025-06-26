# dataProject
sql
Build a Complete Database Management System

Library Management System 
Project Description
This project is a MySQL-based relational database for a Library Management System. It manages books, members, authors, categories, and book loans. The database is designed with proper constraints (primary keys, foreign keys, NOT NULL, UNIQUE, CHECK) and relationships (one-to-many and many-to-many) to ensure data integrity and efficient querying.
Features:
 
Books: Stores book details (title, ISBN, author, etc.) with constraints on ISBN and copy counts.
Authors: Stores author information, linked to books (one-to-many). 
Members: Tracks library members with unique emails
Loans: Manages book borrowing and returns, with due dates and fines.
Categories: Organizes books by genre, with a many-to-many relationship via a junction table.
Indexes: Added for optimized querying on frequently accessed columns.

How to Run/Setup the Project

Prerequisites:

MySQL Server (version 5.7 or higher) installed.
MySQL client (e.g., MySQL Workbench, command-line client, or phpMyAdmin).


Steps: 1

Clone this repository: git clone <repository-url>
Open your MySQL client and connect to your MySQL server.
Import the library_management.sql file:
Command line: mysql -u <username> -p < library_management.sql
MySQL Workbench: Use the "Server" > "Data Import" option or run the SQL script directly.


The script will create the library_management database and all tables with constraints.
Verify the database structure using SHOW TABLES; and DESCRIBE <table_name>;.


Testing:

Insert sample data to test relationships and constraints.
Example queries:INSERT INTO Authors (first_name, last_name, email) VALUES ('John', 'Doe', 'john.doe@example.com');
INSERT INTO Books (title, author_id, isbn, publication_year, total_copies, available_copies) VALUES ('Sample Book', 1, '1234567890123', 2020, 5, 5);



Entity-Relationship Diagram (ERD)
The ERD for this database can be visualized using tools like MySQL Workbench or online tools (e.g., dbdiagram.io). Below is a textual representation of the relationships:

Authors (1) ↔ (M) Books
Books (M) ↔ (M) Categories via Book_Categories
Books (M) ↔ (M) Members via Loans

For a visual ERD, import the .sql file into MySQL Workbench and use the "Database" > "Reverse Engineer" feature to generate the diagram.
Note: If you need a screenshot of the ERD, generate it using MySQL Workbench and upload it to this repository as erd.png.
Repository Structure

library_management.sql: The main SQL script containing all CREATE TABLE statements and constraints.



