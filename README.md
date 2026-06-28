# Library Management System

A console-based library management system built with C++.

The application allows an administrator to manage books and users, search the library catalogue, and track borrowed books and available copies.

## Features

- Add books with an ID, name, and quantity.
- Add library users with a name and ID.
- Search for books using a name prefix.
- List books sorted by ID.
- List books sorted alphabetically by name.
- Borrow available book copies.
- Return borrowed books.
- Display users who borrowed a specific book.
- Display all users and their borrowed book IDs.
- Validate book and user names during borrowing and returning.

## Menu Options

```text
1) Add book
2) Search books by prefix
3) Print users who borrowed a book
4) Print library sorted by ID
5) Print library sorted by name
6) Add user
7) Borrow a book
8) Return a book
9) Print users
10) Exit
```

## Program Design

The program is organized into three structures.

### `book`

Stores information about a book:

- Book ID
- Book name
- Total quantity
- Number of borrowed copies

It also handles borrowing, returning, prefix matching, and printing book information.

### `user`

Stores information about a library user:

- User ID
- User name
- IDs of borrowed books

It handles registering borrowed books, returning books, and displaying user information.

### `library_system`

Coordinates the application and manages:

- The collection of books
- Registered users
- Menu operations
- Book and user searches
- Borrowing and returning operations
- Sorted output

## Technologies and Concepts

- C++
- Structures and member functions
- Constructors
- Fixed-size arrays
- Linear search
- Prefix matching
- Sorting with `std::sort`
- Custom comparison functions
- Assertions
- Input validation
- Console input and output

## Getting Started

### Prerequisites

A C++ compiler supporting C++11 or later, such as GCC, Clang, or Microsoft Visual C++.

### Compile

Using GCC:

```bash
g++ -std=c++11 main.cpp -o library-system
```

### Run

Linux or macOS:

```bash
./library-system
```

Windows:

```powershell
.\library-system.exe
```

## Usage Examples

### Add a Book

Select option `1`, then enter the book information:

```text
Enter book info: id & name & total quantity:
101 CppHowToProgram 7
```

This adds a book with:

- ID: `101`
- Name: `CppHowToProgram`
- Quantity: `7`

### Add a User

Select option `6`, then enter the user's name and ID:

```text
Enter user name & national id:
Ahmed 1001
```

### Search by Prefix

If the library contains these books:

```text
CppHowToProgram
CppForDummies
CppForAdvancedLevels
CoreJava
```

Searching for `CppFo` returns:

```text
CppForDummies
CppForAdvancedLevels
```

### Borrow a Book

Select option `7` and provide the user and book names:

```text
Enter user name and book name:
Ahmed CppHowToProgram
```

If a copy is available, the borrowed count increases and the book ID is added to the user's borrowed books.

### Return a Book

Select option `8` and enter the same information:

```text
Enter user name and book name:
Ahmed CppHowToProgram
```

The book is removed from the user's borrowed books and becomes available again.

## Project Constraints

- The system stores up to 10 books.
- The system stores up to 10 users.
- Book and user names must be entered without spaces.
- Data is stored in memory and is lost when the program closes.
- Searches are case-sensitive.
- Book and user names are expected to be unique.

## What I Learned

This project helped me practice:

- Modeling related data and behavior with structures.
- Coordinating multiple components in one system.
- Tracking relationships between users and books.
- Implementing borrowing and returning workflows.
- Searching data using exact names and prefixes.
- Sorting objects using custom comparison functions.
- Validating input before performing operations.
- Maintaining consistent data across related records.

## Future Improvements

- Replace fixed-size arrays with STL containers.
- Prevent duplicate book and user IDs.
- Prevent users from borrowing the same book more than once.
- Validate that a user borrowed a book before returning it.
- Support names containing spaces.
- Add persistent file or database storage.
- Add book deletion and user removal.
- Add due dates and overdue-book tracking.
- Add automated tests.
- Improve error handling for invalid input.

## Acknowledgements

This project was completed as part of a C++ course focused on programming fundamentals, problem-solving, software design, and project-building skills.

## License

This project is intended for educational purposes.
