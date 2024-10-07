# Bookstore Database System

This project implements a simple database system for managing a collection of books, authors, and genres. The design allows for easy retrieval and management of book-related information.

## Database Design

The database consists of three main tables:

1. **Authors**: Stores information about book authors.
2. **Genres**: Stores different genres of books.
3. **Books**: Stores information about books, linking them to their authors and genres.

### Tables Overview

- **Authors**
  - `id`: Unique identifier for each author.
  - `name`: Full name of the author.
  - `bio`: Short biography of the author.

- **Genres**
  - `id`: Unique identifier for each genre.
  - `name`: Name of the genre.

- **Books**
  - `id`: Unique identifier for each book.
  - `title`: Title of the book.
  - `author_id`: Foreign key referencing the `Authors` table.
  - `genre_id`: Foreign key referencing the `Genres` table.
  - `published_year`: Year the book was published.

## SQL Commands

### Create Tables

The following SQL commands can be used to create the necessary tables in your database:

```sql
-- Create Authors table
CREATE TABLE Authors (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    bio TEXT
);

-- Create Genres table
CREATE TABLE Genres (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL
);

-- Create Books table
CREATE TABLE Books (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    author_id INT,
    genre_id INT,
    published_year INT,
    FOREIGN KEY (author_id) REFERENCES Authors(id),
    FOREIGN KEY (genre_id) REFERENCES Genres(id)
);

