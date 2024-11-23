# Distributed Book Storage Using Firebase

This repository contains the implementation of a distributed data storage system for storing and querying book information using Firebase Realtime Databases. The system partitions data by hashing author names and distributes the data across two Firebase databases.

---

## Table of Contents

- [Introduction](#introduction)
- [Operations](#operations)
  - [add_book](#1-add_book-40-points)
  - [search_by_author](#2-search_by_author-30-points)
  - [search_by_year](#3-search_by_year-30-points)
- [Requirements](#requirements)
- [Testing and Submission](#testing-and-submission)
- [Usage](#usage)
- [References](#references)

---

## Introduction

The project demonstrates a distributed data storage system for a collection of books. Each book is represented as a JSON object containing the following attributes:
- **author**: The author of the book.
- **title**: The title of the book.
- **year**: The publication year of the book.
- **price**: The price of the book.

Books are partitioned based on a hash of the author's name and stored in one of two Firebase Realtime Databases. The operations include adding books and querying by author or year, ensuring efficient data retrieval without downloading unnecessary data.

---

## Operations

### 1. `add_book` (40 Points)

This method stores book information in one of the two Firebase databases based on the hash value of the author's name.

#### Method Signature:
```python
def add_book(book_id: str, book_data: dict) -> None:
    """
    Adds a book to the appropriate Firebase database based on the hash of the author's name.

    Args:
        book_id (str): Unique identifier for the book.
        book_data (dict): JSON object containing book information:
            {
                "author": str,
                "title": str,
                "year": int,
                "price": float
            }
    """

python3 your_script.py add_book 100 '{"author": "John Smith", "title": "Book Title", "year": 2023, "price": 29.99}'


def search_by_author(author: str) -> list:
    """
    Searches for all books written by the specified author.

    Args:
        author (str): The author's name.

    Returns:
        list: A list of JSON objects representing the books written by the author.
    """

python3 your_script.py search_by_author "John Smith"

def search_by_year(year: int) -> list:
    """
    Searches for all books published in the specified year.

    Args:
        year (int): The publication year.

    Returns:
        list: A list of JSON objects representing the books published in the specified year.
    """

python3 your_script.py search_by_year 2023

