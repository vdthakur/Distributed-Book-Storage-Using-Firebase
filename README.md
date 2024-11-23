# Distributed Book Storage Using Firebase

This repository contains the implementation of a distributed data storage system for storing and querying book information using Firebase Realtime Databases. The system partitions data by hashing author names and distributes the data across two Firebase databases.

---

## Table of Contents

- [Introduction](#introduction)
- [Operations](#operations)
  - [`add_book`](#1-add_book)
  - [`search_by_author`](#2-search_by_author)
  - [`search_by_year`](#3-search_by_year)
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

### 1. `add_book`

This method stores book information in one of the two Firebase databases based on the hash value of the author's name.

*Execution:*  
*`python3 script.py add_book 100 '{"author": "John Smith", "title": "Book Title", "year": 2023, "price": 19.99}'`*

---

### 2. `search_by_author`

This method retrieves all books written by a specific author from the Firebase databases. It queries the appropriate database without downloading unnecessary data.

*Execution:*  
*`python3 script.py search_by_author "<author_name>"`*

---

### 3. `search_by_year`

This method retrieves all books published in a specified year from the Firebase databases. It queries the appropriate database without downloading unnecessary data.

*Execution:*  
*`python3 script.py search_by_year 2023`*


