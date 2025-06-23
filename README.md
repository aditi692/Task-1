# Task-1
1. Author
Stores author information.

Column Name	Data Type	Description
author_id	INTEGER	Unique ID for each author (Primary Key).
name	TEXT	Full name of the author. (Not null)

2. Book
Contains information about each book in the library.

Column Name	Data Type	Description
book_id	INTEGER	Unique book ID (Primary Key).
title	TEXT	Title of the book. (Not null)
genre	TEXT	Genre of the book (e.g., Fiction, Non-fiction).

3. Book_Author
Represents a many-to-many relationship between books and authors.

Column Name	Data Type	Description
book_id	INTEGER	Foreign key referencing Book(book_id).
author_id	INTEGER	Foreign key referencing Author(author_id).
Primary Key	(book_id, author_id)	Composite key ensuring uniqueness for each book-author pair.

4. Member
Holds data of registered library members.

Column Name	Data Type	Description
member_id	INTEGER	Unique member ID (Primary Key).
name	TEXT	Full name of the member.
email	TEXT	Unique email address for communication and identification.

5. Loan
Tracks the lending and return details of books issued to members.

Column Name	Data Type	Description
loan_id	INTEGER	Unique loan ID (Primary Key).
book_id	INTEGER	Foreign key referencing Book(book_id).
member_id	INTEGER	Foreign key referencing Member(member_id).
loan_date	DATE	Date when the book was borrowed.
return_date	DATE	Date when the book was returned or due.
