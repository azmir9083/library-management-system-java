# Library Management System (Java)

A menu-driven console application for managing a small library. It adds and searches books, registers students, and handles borrowing and returning with stock tracking. It is built with core object-oriented programming in Java.

*Course project at San Francisco Bay University.*

## Features

| Menu option | What it does |
|---|---|
| 1. Add Book | Adds a book with ID, title, author, genre and quantity |
| 2. Display Books | Lists all books in the catalog |
| 3. Search Book | Finds books by exact title or author (case-insensitive) |
| 4. Add Student | Registers a student with ID, name, email and department |
| 5. View Students | Lists all registered students |
| 6. Borrow Book | Checks that the student and book exist and a copy is available, then decreases the quantity |
| 7. Return Book | Increases the quantity of the returned book |
| 8. Exit | Closes the program |

## Design

- **`Book`** and **`Student`** classes use private fields with getters, setters and `toString()` (encapsulation).
- **`LibraryManagementSystem`** holds the catalog in `ArrayList`s and runs the menu loop with a `switch`.
- Lookups use the Java Streams API (`stream().filter(...).findFirst()`).

## Project Structure

```
library-management-system-java/
├── src/
│   └── LibraryManagementSystem.java
├── docs/
│   └── sample_output.pdf   # console output from a full test run
├── .gitignore
└── README.md
```

## Requirements

- **Java JDK 8 or newer.** Check with `java -version` and `javac -version`.
- No external libraries.

## How to Run

```bash
git clone https://github.com/azmir9083/library-management-system-java.git
cd library-management-system-java/src
javac LibraryManagementSystem.java
java LibraryManagementSystem
```

You can also open the folder in IntelliJ IDEA, Eclipse or VS Code and run `LibraryManagementSystem.main`.

## Sample Session

```
Library Management System Menu:
1. Add Book
...
Enter your choice: 1
Enter Book ID: 101
Enter Title: Clean Code
Enter Author: Robert Martin
Enter Genre: Programming
Enter Quantity: 2
Book added successfully!

Enter your choice: 6
Enter Student ID: 1
Enter Book ID: 101
Book borrowed successfully!
```

Tested with OpenJDK. It compiles without warnings and all 8 menu options run correctly.

## Possible Improvements

- Validate input so the menu doesn't crash on non-numeric entries (`InputMismatchException`).
- Save data to a file or database so it persists between runs.
- Track which student borrowed which book.

## Author

**Md Azmir Bhuiyan**, Computer Science, San Francisco Bay University · [LinkedIn](https://www.linkedin.com/in/md-azmir-bhuiyan-97174034b)
