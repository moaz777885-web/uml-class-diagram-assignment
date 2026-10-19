# Library Management System — Project Description Report

| | |
|---|---|
| **Group members** | Moaz Mohammed Yacoub (202510648) and Amar Ahmed Alduom (202512897) |
| **Instructor** | Eric Maniraguha |
| **Institution** | Kigali Independent University (ULK) |
| **Date** | 20 October 2026 |

---

## 1. Project Title and Business Idea

**Project title:** Library Management System

**Business idea:** A library needs an information system to organise information about its books, members, and librarians, and to record when books are borrowed and returned.

## 2. Problem Statement

Managing a library manually is difficult when it holds many books and members. Recording borrowed books, checking whether a book is available, and tracking return dates takes time and can lead to errors, missing information, or duplicate records.

## 3. Purpose of the Proposed System

The purpose of the system is to organise book, member, librarian, and loan information in one structured model. It will make it easier to track borrowed books, check availability, and identify overdue loans.

## 4. Project Scope

### 4.1 Included in the scope

- Storing book details: book ID, title, author, and ISBN.
- Registering library members and storing their details.
- Storing librarian information.
- Recording book issue and return transactions.
- Recording issue date, due date, return date, and loan status.
- Checking book availability and identifying overdue loans.
- Designing a UML class diagram to represent the system.

### 4.2 Excluded from the scope

- Developing a complete working software application.
- Designing a graphical user interface.
- Implementing a database.
- Online book reservations or payments.
- Barcode or RFID integration.
- Automated email or SMS notifications.

The project focuses on system analysis and UML modelling, not full software development.

## 5. Main Classes and Their Responsibilities

| Class | Responsibility |
|-------|----------------|
| **Book** | Represents a library book. Stores its ID, title, author, ISBN, and availability. Can check availability and update book details. |
| **Member** | Represents a registered library user. Stores ID, full name, email, and phone. Can register and view their loans. |
| **Librarian** | Represents a library employee. Stores ID, full name, and email. Can register members, issue books, and accept returns. |
| **Loan** | Represents one borrowing transaction. Stores loan ID, issue date, due date, return date, and status. Can create a loan, mark it as returned, and check if it is overdue. |

## 6. System Requirements

### 6.1 Functional requirements

The system should be able to:

1. Store and manage book information.
2. Register library members and store their details.
3. Store librarian information.
4. Record each book-borrowing transaction.
5. Link each loan to one book, one member, and one librarian.
6. Record the issue date, due date, return date, and loan status.
7. Update the loan status when a book is returned.
8. Check whether a book is available.
9. Identify overdue loans.

### 6.2 Non-functional requirements

- **Simplicity:** the design should be easy to understand.
- **Accuracy:** borrowing and returning information should be recorded consistently.
- **Maintainability:** each class should have clear responsibilities.
- **Clarity:** the diagram should be readable and show relationships clearly.

## 7. Conclusion

The Library Management System model provides a clear structure for managing books, members, librarians, and loans. By identifying the main classes, their responsibilities, and the system requirements, the project lays a foundation for future development. The UML class diagram is presented in Report 2.
