# 📚 Book Management System

A console-based Book Management System written in C that allows users to manage a collection of books — add, search, update, delete, filter by category, and sort by price or rating.

---

## Features

- Add new books to the collection
- Display all books in a formatted table
- Search books by ID or name (case-insensitive)
- Delete a book by searching and removing it
- Update a book's price or rating
- Filter books by category
- Sort books by price or rating (ascending or descending)
- Preloaded with 10 sample books across crime, comedy, and suspense categories

---

## Data Structure

Each book stores the following fields:

| Field        | Type    | Description                  |
|--------------|---------|------------------------------|
| `id`         | int     | Unique book identifier       |
| `bookName`   | char[]  | Name of the book (max 20)    |
| `authorName` | char[]  | Author's name (max 20)       |
| `catagory`   | char[]  | Book category (max 20)       |
| `price`      | int     | Price of the book            |
| `rating`     | float   | Rating between 0.0 and 10.0  |

---

## Getting Started

### Prerequisites

- GCC compiler (or any C compiler)
- Linux / macOS / Windows (with GCC via MinGW or WSL)

### Compile

```bash
gcc bookManagementSystem.c -o bookManagementSystem
```

### Run

```bash
./bookManagementSystem
```

---

## Menu Options

```
**************************
1. Add Book
2. Display All Books
3. Search Book
4. Remove Book
5. Update Book Data
6. Show Category's Books
7. Display Sorted Books
**************************
Enter 0 to Exit
```

---

## Usage Examples

### Add a Book
Select option `1` and enter the book details when prompted (ID, name, author, category, price, rating).

### Search a Book
Select option `3`, then choose to search by:
- `1` — Book ID
- `2` — Book Name (case-insensitive)

### Delete a Book
Select option `4`. The system will prompt you to search for the book first, then remove it if found.

### Update a Book
Select option `5`. Search for the book, then choose to update:
- `1` — Price
- `2` — Rating

### Filter by Category
Select option `6` and enter a category name (e.g., `crime`, `comedy`, `suspense`). The search is case-insensitive.

### Sort Books
Select option `7`, then choose:
- Sort by `1` Price or `2` Rating
- Order: `1` Ascending or `2` Descending

The original data is not modified — sorting is done on a temporary copy.

---

## Preloaded Sample Data

| ID | Name                  | Author              | Category | Price | Rating |
|----|-----------------------|---------------------|----------|-------|--------|
| 1  | The Guide             | R.K. Narayan        | fiction  | 199   | 9.2    |
| 2  | Godan                 | Munshi Premchand    | fiction  | 150   | 8.9    |
| 3  | Malgudi Days          | R.K. Narayan        | fiction  | 175   | 9.0    |
| 4  | The White Tiger       | Aravind Adiga       | drama    | 299   | 8.7    |
| 5  | Train to Pakistan     | Khushwant Singh     | drama    | 220   | 8.5    |
| 6  | Pinjar                | Amrita Pritam       | drama    | 180   | 8.3    |
| 7  | The Rozabal Line      | Ashwin Sanghi       | suspense | 350   | 7.8    |
| 8  | Chanakyas Chant       | Ashwin Sanghi       | suspense | 320   | 8.1    |
| 9  | Sacred Games          | Vikram Chandra      | crime    | 499   | 9.1    |
| 10 | Delhi Noir            | Hirsh Sawhney       | crime    | 275   | 7.6    |

---

## Known Limitations

- Book name and author name are limited to 20 characters
- Maximum collection size is 50 books (set at compile time)
- `gets()` is used for string input — deprecated in modern C; can be replaced with `fgets()` for safety
- Rating validation only enforces an upper bound of 10; negative ratings are not rejected

---

## File Structure

```
bookManagementSystem.c   # Main source file (all logic in a single file)
```

---

## License

This project is open for educational use.
