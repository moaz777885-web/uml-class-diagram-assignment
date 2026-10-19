# Library Management System — UML Class Diagram Report

| | |
|---|---|
| **Group members** | Moaz Mohammed Yacoub (202510648) and Amar Ahmed Alduom (202512897) |
| **Instructor** | Eric Maniraguha |
| **Institution** | Kigali Independent University (ULK) |
| **Date** | 20 October 2026 |

---

## 1. Introduction

A UML class diagram shows the classes of a system, their attributes and methods, and the relationships between them. This report presents the class diagram for the Library Management System. It contains four classes: **Book**, **Member**, **Librarian**, and **Loan**.

## 2. UML Class Diagram

![UML Class Diagram of the Library Management System](../diagrams/uml_class_diagram.png)

*Figure 1: UML class diagram of the Library Management System.*

## 3. Classes, Attributes, and Methods

### 3.1 Book

| Attributes | Methods |
|------------|---------|
| `- bookId: String` | `+ checkAvailability(): Boolean` |
| `- title: String` | `+ updateDetails(): void` |
| `- author: String` | |
| `- isbn: String` | |
| `- available: Boolean` | |

Stores information about a library book. The `available` attribute shows whether the book can currently be borrowed.

### 3.2 Member

| Attributes | Methods |
|------------|---------|
| `- memberId: String` | `+ register(): void` |
| `- fullName: String` | `+ viewLoans(): List<Loan>` |
| `- email: String` | |
| `- phone: String` | |

Stores information about a registered library user. A member can register and view their own loans.

### 3.3 Librarian

| Attributes | Methods |
|------------|---------|
| `- librarianId: String` | `+ registerMember(): void` |
| `- fullName: String` | `+ issueBook(): Loan` |
| `- email: String` | `+ acceptReturn(): void` |

Represents the employee who manages library activities, including registering members, issuing books, and accepting returns.

### 3.4 Loan

| Attributes | Methods |
|------------|---------|
| `- loanId: String` | `+ createLoan(): void` |
| `- issueDate: Date` | `+ markReturned(): void` |
| `- dueDate: Date` | `+ isOverdue(): Boolean` |
| `- returnDate: Date` | |
| `- status: String` | |

Represents one borrowing transaction. It records the dates of borrowing and returning and the current status of the loan.

## 4. Relationships and Multiplicities

All three relationships are **associations** with the Loan class at the centre.

| Relationship | Label | Multiplicity | Explanation |
|--------------|-------|--------------|-------------|
| Member — Loan | borrows | **1** to **0..*** | One member can borrow zero or many times. Each loan belongs to exactly one member. |
| Book — Loan | is lent in | **1** to **0..*** | One book can appear in zero or many loans over time. Each loan is for exactly one book. |
| Librarian — Loan | issues | **1** to **0..*** | One librarian can issue zero or many loans. Each loan is issued by exactly one librarian. |

## 5. Design Notes

- `register()` in Member lets a member sign up, while `registerMember()` in Librarian lets the librarian register a member on their behalf.
- `issueBook()` in Librarian is the action of lending a book, and it uses `createLoan()` in Loan to create the loan record.

## 6. UML Notation Used

- `-` means a private attribute; `+` means a public method.
- `String` is text, `Boolean` is true or false, `Date` is a date, and `void` means nothing is returned.
- `1` means exactly one; `0..*` means zero or many.

## 7. Conclusion

The class diagram shows how members, books, librarians, and loans are related in the Library Management System. Loan connects the other three classes, so every borrowing transaction can be traced to one member, one book, and one librarian.
