# User Stories & Acceptance Criteria

## 1. User Stories (8) - Format: As a..., I want..., so that...

1.  **US-01:** As a Student, I want to search books by title, so that I can find my required book quickly.
2.  **US-02:** As a Student, I want to see my borrowed books and due dates, so that I can avoid fines.
3.  **US-03:** As a Faculty Member, I want to reserve a book that is issued, so that I get it next.
4.  **US-04:** As a Librarian, I want to issue a book by scanning Student ID and Book ID, so that process is fast.
5.  **US-05:** As a Librarian, I want system to auto-calculate fine, so that I don't make manual errors.
6.  **US-06:** As a Librarian, I want to see defaulter list, so that I can follow up with students.
7.  **US-07:** As a Library Admin, I want to add new books in bulk via Excel upload, so that I save time.
8.  **US-08:** As a Library Admin, I want to generate monthly reports, so that I can present to management.

## 2. Measurable Acceptance Criteria for each User Story

| User Story | Acceptance Criteria |
| :--- | :--- |
| US-01 | Search returns results in <2 sec, shows title, author, availability status. Search with partial keyword works. |
| US-02 | Dashboard shows Book Title, Issue Date, Due Date, Fine if any. Accuracy 100%. |
| US-03 | Reserve button only active if book is 'Issued'. User gets notification when book available. Max 2 reserves per user. |
| US-04 | Issue transaction completes in <60 seconds. Updates inventory immediately. |
| US-05 | Fine = (Current Date - Due Date) * 10 Rs. Calculation correct for leap year. |
| US-06 | Defaulter list shows Student ID, Book, Due Date, Days Overdue, Fine. Export to PDF. |
| US-07 | Excel upload of 100 books completes in <30 sec with 100% data validation. |
| US-08 | Report generated in <5 sec. Contains correct counts. Export to PDF/Excel works. |

## 3. AI Assistant Review of Requirements (5 Suggestions)

We used AI assistant (Meta AI) to review requirements for Ambiguity, Omissions, Conflicts, Testability.

| # | AI Suggestion | Type | Accept / Reject | Justification |
| :--- | :--- | :--- | :--- | :--- |
| 1 | FR-06 "calculate fine" is ambiguous - specify fine per day and when it starts. | Ambiguity | **Accept** | Added exact rule: Rs.10/day after due date, included in FR-06. |
| 2 | Missing requirement: What is max books a student can issue? | Omission | **Accept** | Added business rule: Student max 3 books, Faculty max 5 books. Added as FR-13 implicitly covered in validation. |
| 3 | Conflict: NFR-02 says session timeout 15 min, but librarian needs longer during issue rush. | Conflict | **Accept** | Changed to: Student session 15 min, Librarian/Admin session 60 min. |
| 4 | NFR-03 "simple UI" is not testable. Need measurable usability metric. | Testability | **Accept** | Rewrote NFR-03 to: Learn in <10 min training + SUS score >75. |
| 5 | AI suggested adding biometric login for security. | Improvement | **Reject** | Out of scope for Phase-1 due to budget constraint and hardware limitation. Will consider in Phase-2. |

## 4. Traceability Matrix

| Requirement ID | Linked User Stories | Priority (High/Med/Low) |
| :--- | :--- | :--- |
| FR-01 | US-04, US-07 | High |
| FR-02 | US-01 | High |
| FR-03 | US-01, US-03 | High |
| FR-04 | US-04 | High |
| FR-05 | US-04 | High |
| FR-06 | US-05 | High |
| FR-07 | US-03 | Medium |
| FR-08 | US-02 | Medium |
| FR-09 | US-07 | High |
| FR-10 | US-07 | High |
| FR-11 | US-06, US-08 | High |
| FR-12 | US-02 | High |
| NFR-01 to NFR-05 | All US | High |