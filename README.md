# Library Management System - Database Programming Project

## Overview
This project is a comprehensive **Library Management System** designed using **MySQL** to efficiently manage various library operations. It encompasses the management of books, authors, patrons, and lending activities. The system is structured through a well-designed relational database schema and includes robust MySQL functions, procedures, and automated triggers that ensure data integrity and streamline the library's daily operations.

## Key Features:
- **Book and Author Management**: Add, update, and manage books and authors with ease. The system also supports many-to-many relationships between books and authors.
- **Patron Management**: Efficiently handles library members, including various patron types (e.g., student, faculty).
- **Lending and Returns**: Tracks the lending process and overdue books, calculating fines automatically. The system ensures that books cannot be checked out multiple times until they are returned.

## Database Schema:
The following tables form the backbone of the system:
- **Books**: Stores details about books, such as title, year published, cost, subject, and available copies.
- **Authors**: Contains author details, including first and last name, and birth year.
- **Patrons**: Maintains records of library members, including first and last name, and patron type.
- **Checkouts**: Manages book lending activities, tracking checkout, return dates, and overdue books.
- **Writes**: Establishes the many-to-many relationship between books and authors.

## Functions:
Several MySQL functions were implemented to automate and facilitate core library operations:
- `AUTHOR_EXISTS`: Verifies if an author exists in the database.
- `BOOK_EXISTS`: Checks for the existence of a book.
- `CALCULATE_OPEN_FINE`: Calculates overdue fines based on the number of days late.
- `PATRON_EXISTS`: Verifies if a patron is registered in the library.
- `BOOK_AVAILABLE`: Checks if a book is available for checkout.
- `VALIDATE_CHECKIN`: Ensures the validity of a book check-in.
- `CALCULATE_TOTAL_FINES`: Computes the total fines for a patron.
- `AUTHOR_BOOK_COUNT`: Returns the total number of books associated with a specific author.
- `MOST_POPULAR_BOOK`: Identifies the book with the highest checkout frequency.
- `PATRON_BOOK_HISTORY`: Provides a summary of all books checked out by a patron.

## Procedures:
To further streamline the operations, the following procedures were created:
- `ADD_BOOK`: Adds a new book to the library.
- `ADD_AUTHOR_TO_BOOK`: Associates an author with a book.
- `CHECKOUT_BOOK`: Manages the process of checking out a book.
- `CHECKIN_BOOK`: Handles book returns.
- `REMOVE_BOOK`: Deletes a book and its associations.
- `UPDATE_BOOK_DETAILS`: Updates information about a book.
- `REGISTER_PATRON`: Registers new library members.

## Triggers:
Automated triggers ensure data integrity and improve operational efficiency:
- **On Checkout**: Reduces the available copies of a book.
- **On Checkin**: Increases the available copies when a book is returned.
- **Prevent Duplicate Checkout**: Ensures a book cannot be checked out multiple times before being returned.
- **Validate Book Copies**: Prevents the available copy count from falling below zero.

## Testing:
The system was thoroughly tested with various typical and edge-case scenarios using the `main.sql` file, which includes a series of tests covering all functionalities, ensuring the reliability and robustness of the system.

## Conclusion:
This **Library Management System** provides a solid foundation for managing library operations efficiently. Its modular design, automated functionalities, and data integrity mechanisms make it an ideal solution for libraries seeking to streamline and digitize their operations.
