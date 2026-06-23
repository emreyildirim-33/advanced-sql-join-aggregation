# Advanced SQL JOIN & Aggregation

An SQL practice project focused on relational database querying, JOIN operations, aggregation functions, GROUP BY usage, subqueries, and analytical query writing.

The project is based on a library information system database containing students, books, authors, genres, and borrowing records.

## Overview

This project was developed as a hands-on SQL and relational database practice project.

The main goal was to practice writing SQL queries that retrieve meaningful information from multiple related tables. The project focuses on JOIN logic, aggregation, grouping, filtering, and query-based reporting.

The database simulates a school library system where students borrow books and book-related data is stored across multiple relational tables.

## Database Domain

The project uses a library information system with tables such as:

* `ogrenci`
* `islem`
* `kitap`
* `yazar`
* `tur`

These tables represent students, borrowing transactions, books, authors, and book genres.

## Core Concepts Practiced

* SQL JOIN operations
* Relational database querying
* `GROUP BY`
* `COUNT`
* `AVG`
* Filtering query results
* Aggregation-based reporting
* Subquery logic
* Multi-table data retrieval
* Query optimization basics
* Repository-based SQL query placement

## Main Query Tasks

The project includes SQL exercises such as:

* Listing books by genre
* Listing students who borrowed books
* Listing students who did not borrow books
* Counting borrowed books by class
* Counting total students
* Counting distinct student names
* Grouping students by name
* Counting students by class
* Listing each student with the number of books they read
* Calculating the average score of all books

## Example Query Concepts

### JOIN Query

```sql
SELECT o.ad, o.soyad, k.ad AS kitap_adi
FROM ogrenci o
JOIN islem i ON o.ogrencino = i.ogrencino
JOIN kitap k ON i.kitapno = k.kitapno;
```

### GROUP BY and COUNT

```sql
SELECT sinif, COUNT(*) AS ogrenci_sayisi
FROM ogrenci
GROUP BY sinif;
```

### AVG Aggregation

```sql
SELECT AVG(puan) AS ortalama_puan
FROM kitap;
```

## What I Practiced

* Writing SQL queries for relational databases
* Retrieving data from multiple related tables
* Using JOIN operations effectively
* Creating grouped reports with `GROUP BY`
* Using aggregation functions such as `COUNT` and `AVG`
* Finding records with and without related data
* Understanding many-to-one and one-to-many query patterns
* Practicing SQL from a backend developer perspective

## Project Structure

```text
src/
 └── main/
     └── resources/
         └── test.sql
```

## Getting Started

### Prerequisites

Make sure you have the following installed:

* PostgreSQL
* Java 17+
* Maven
* IntelliJ IDEA or another Java IDE

### Setup

Clone the repository:

```bash
git clone https://github.com/emreyildirim-33/advanced-sql-join-aggregation.git
cd advanced-sql-join-aggregation
```

Run the provided SQL setup file in your PostgreSQL database:

```text
src/main/resources/test.sql
```

Configure your database connection in `application.properties`.

Example:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/your_database
spring.datasource.username=your_username
spring.datasource.password=your_password
```

## Notes

This project was built as a database and SQL training project.
The main focus was not building a full library management application, but practicing SQL JOIN operations, aggregation, grouping, filtering, and relational query design.

## Repository

GitHub: https://github.com/emreyildirim-33/advanced-sql-join-aggregation
