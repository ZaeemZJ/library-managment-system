

## 📚 Library Management System – OEL Project Report

### 🧑‍💻 Student Information:
- **Name:** [Your Name]  
- **Roll Number:** [Your Roll Number]  
- **Subject:** Open Ended Lab  
- **Semester:** [Your Semester]  
- **Faculty Guide:** [Faculty Name]  

---

### 📝 Project Title:
**Library Management System using Java**

---

### 🔍 Objective:
The objective of this project is to develop a simple, console-based **Library Management System** using Java. The system helps manage a small library catalog by allowing users to add, remove, search, issue, return, and sort books efficiently.

---

### ⚙️ Technologies Used:
- **Programming Language:** Java  
- **Data Structures Used:** LinkedList, Array  
- **Tools Used:** IDE (Eclipse/IntelliJ/VS Code), Java SDK  

---

### 📋 Features Implemented:
1. **Add Book:**  
   Allows the user to add a new book by entering ID, title, and author.

2. **Remove Book:**  
   Enables removal of a book from the catalog using the book's ID.

3. **Search Book:**  
   Allows the user to search for books by title (partial match supported).

4. **Issue Book:**  
   Issues a book to a user, marking it as issued and storing it in a separate array.

5. **Return Book:**  
   Returns a previously issued book and updates the status accordingly.

6. **Display All Books:**  
   Lists all books currently in the catalog along with their details.

7. **Sort Books by Title:**  
   Sorts and displays books alphabetically by their title using a simple bubble sort algorithm.

---

### 📦 Data Structures & Logic:
- **LinkedList<Book>:** Used to store the main catalog for efficient addition/removal.
- **Book[] issuedBooks:** Fixed-size array to store currently issued books.
- **Bubble Sort:** Used in `sortBooks()` to alphabetically sort books by title.

---

### 👨‍💻 Sample Code Snippet:
```java
Book(int id, String title, String author) {
    this.id = id;
    this.title = title;
    this.author = author;
    this.isIssued = false;
}
```

```java
static void issueBook() {
    System.out.print("Enter Book ID to issue: ");
    int id = sc.nextInt();
    for (Book b : catalog) {
        if (b.id == id && !b.isIssued) {
            b.isIssued = true;
            issuedBooks[issuedCount++] = b;
            System.out.println("Book issued.");
            return;
        }
    }
    System.out.println("Book not available or already issued.");
}
```

---

### ✅ Conclusion:
This project demonstrates fundamental concepts of **object-oriented programming**, **data structures**, and **user input handling** in Java. It simulates a basic but functional library system and can be expanded further with features like file handling, GUI, user login system, and fine management.

---

### 🔄 Possible Enhancements:
- Implement file/database storage to retain data across sessions.
- Add a graphical user interface (GUI) using Swing or JavaFX.
- Handle multiple users with login/logout and roles (Admin/Student).
- Track book return dates and overdue fines.

---
