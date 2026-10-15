# Requirements List

## A. Functional Requirements (12) - ID FR-01 to FR-12

| ID | Requirement |
| :--- | :--- |
| **FR-01** | System shall allow users to register and login with University ID and password. |
| **FR-02** | System shall allow searching books by Title, Author, ISBN, and Category. |
| **FR-03** | System shall display real-time availability status (Available / Issued / Reserved). |
| **FR-04** | System shall allow Librarian to issue a book to a student/faculty. |
| **FR-05** | System shall allow Librarian to process return of a book. |
| **FR-06** | System shall automatically calculate fine for overdue books (Rs. 10 per day). |
| **FR-07** | System shall allow users to reserve a book that is currently issued. |
| **FR-08** | System shall send email/SMS notification 2 days before due date. |
| **FR-09** | System shall allow Admin to add, update, and delete book records. |
| **FR-10** | System shall allow Admin to manage user accounts (Add/Block/Delete). |
| **FR-11** | System shall generate reports: Daily Issue/Return, Fine Collection, Defaulter List. |
| **FR-12** | System shall allow users to view their borrowing history and current loans. |

## B. Non-Functional Requirements (5) - ID NFR-01 to NFR-05

| ID | Category | Requirement |
| :--- | :--- | :--- |
| **NFR-01** | Performance | System shall support 100 concurrent users and search response < 2 seconds. |
| **NFR-02** | Security | All passwords shall be encrypted (bcrypt) and session timeout after 15 min idle. |
| **NFR-03** | Usability | New librarian shall learn issue/return operation in < 10 minutes training. UI shall be simple. |
| **NFR-04** | Availability | System shall be available 99% of time during library hours (8 AM - 8 PM). |
| **NFR-05** | Backup & Recovery | System shall take daily automatic backup and allow full restore in < 30 minutes. |

## C. Assumptions and Constraints (5)

1.  **Assumption:** All users have University ID and active internet access in library.
2.  **Assumption:** Librarian has basic computer knowledge.
3.  **Constraint:** System will be Web-based only for this version (No mobile app in Phase-1).
4.  **Constraint:** Budget limited - must use open-source stack (PHP/MySQL or Python/Django).
5.  **Constraint:** Project must be completed within 8 weeks as per Project Schedule.