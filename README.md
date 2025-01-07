Library Management System - README
Overview
This Library Management System is a simple Python-based application that helps manage a library of books. It allows users to:

Add new books to the library.
Delete books from the library.
Modify book details (e.g., title, author, genre, year).
Search for a book by its unique ID.
Display a list of all books in the library.
Visualize the distribution of books by genre in a bar chart.
The system uses pandas for data manipulation and matplotlib for generating bar charts. The book details are stored in a CSV file (library.csv), and all operations (add, delete, modify, etc.) are performed on this file.

This README will guide you through the structure of the program and explain each function in detail so you can understand how everything works.

Prerequisites
Before running this system, make sure you have the following installed:

Python (version 3.x or above)
Pandas library: For data handling and manipulation.
Install it with: pip install pandas
Matplotlib library: For generating plots and visualizations.
Install it with: pip install matplotlib
You will also need a CSV file (library.csv) to store the library data. The file should contain the following columns:

Book ID: A unique identifier for each book.
Title: The title of the book.
Author: The author of the book.
Genre: The genre or category of the book.
Year: The year the book was published.
Example of library.csv format:

Book ID,Title,Author,Genre,Year
1,The Great Gatsby,F. Scott Fitzgerald,Fiction,1925
2,1984,George Orwell,Dystopian,1949
3,To Kill a Mockingbird,Harper Lee,Fiction,1960
4,The Catcher in the Rye,J.D. Salinger,Fiction,1951
5,The Hobbit,J.R.R. Tolkien,Fantasy,1937

Features and Functions

1. Show All Books

This option will display a list of all books in the library stored in the library.csv file. It presents the details in a tabular format, including the Book ID, Title, Author, Genre, and Year.

How it works:

The program loads the CSV file using pandas.
It prints all the records in a table format for easy viewing.
After viewing, it waits for the user to press Enter to return to the menu.

2. Add New Book

This option allows you to add a new book to the library by providing its details, such as Book ID, Title, Author, Genre, and Year.

How it works:

The program prompts the user to enter the Book ID, Title, Author, Genre, and Year.
These details are added to the existing library (stored in library.csv) using pandas.append().
The updated data is saved back to the CSV file.

3. Delete a Book

This option allows you to remove a book from the library by its unique Book ID.

How it works:

The program asks for the Book ID of the book to be deleted.
The program removes the corresponding record from the library using pandas.drop().
The updated data is saved back to the CSV file.

4. Modify Book Details

This option allows you to modify the details of an existing book. You can update the Title, Author, Genre, or Year of any book in the library.

How it works:

The program prompts for the Book ID of the book to modify.
It asks which field (Title, Author, Genre, or Year) you wish to modify.
The new value for that field is input by the user and updated in the CSV file using pandas.at[].
The updated data is saved back to the CSV file.

5. Search for a Book

This option allows you to search for a book by its unique Book ID.

How it works:

The program asks for the Book ID you want to search for.
It retrieves the book's details (if found) and displays them.
The search is performed using pandas.loc[] with the Book ID as the index.

6. Show Bar Graph for Genres

This option generates a bar chart to visually represent the distribution of books by their genre.

How it works:

The program counts how many books exist in each genre using pandas.value_counts() on the Genre column.
The bar chart is created using matplotlib and displayed with labels for the Genre on the x-axis and the count of books on the y-axis.
How to Run the System

Clone the Repository:
Download or clone the repository to your local machine.

Set Up Your CSV File:
Ensure that your library.csv file exists in the specified path (C:\\project\\library.csv). You can create your own CSV file or use the provided example format.

Run the Program:

Open your terminal or command prompt.
Navigate to the directory where your Python file is located.

Run the Python file:
python library_management_system.py

Interact with the Menu:

The program will display a menu with the available options. Enter the number corresponding to the action you want to perform.
You can continue using the system until you choose to exit by selecting option 0.
Example Interaction
======================================
1. Show All Books
2. Add New Book
3. Delete a Book
4. Modify Book Details
5. Search for a Book
6. Show Bar Graph for Genres
0. Exit
======================================
Enter your choice: 1

======================================
   Book ID                     Title              Author       Genre  Year
0       1          The Great Gatsby  F. Scott Fitzgerald   Fiction  1925
1       2                     1984        George Orwell   Dystopian  1949
2       3   To Kill a Mockingbird        Harper Lee   Fiction  1960
3       4   The Catcher in the Rye       J.D. Salinger   Fiction  1951
4       5               The Hobbit    J.R.R. Tolkien   Fantasy  1937
======================================
Press Enter to continue...

Conclusion

This Library Management System is a simple and intuitive way to manage a collection of books. Whether you're adding, deleting, or modifying books, or even generating visual reports, this system provides an easy-to-use interface for managing your library. The system is highly extensible, so you can modify or add more features as needed.

Feel free to contribute to this project, enhance its capabilities, or simply use it for your own library management needs!
