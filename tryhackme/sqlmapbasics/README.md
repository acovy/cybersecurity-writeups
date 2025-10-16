# 🧩 TryHackMe — SQLMap Basics (Walkthrough / Course Overview)

## 📅 Overview
**SQL injection** is one of the most common and long-standing web vulnerabilities in cybersecurity. This room introduces the fundamentals of databases, how web applications interact with them, and how improper handling of user input can lead to SQL injection. You will also learn how to use an automated tool — **sqlmap** — to discover and exploit SQL injection vulnerabilities, and practice these skills with a hands-on challenge.

---

## 🧠 Why this matters
Websites rely on databases to store and retrieve structured data: user accounts, product catalogs, posts, logs and more. When a user types their credentials on a login form or searches for a product, the application constructs a **SQL query** and asks the database to return or modify data.

If user input is not handled safely, an attacker can manipulate those queries to make the database do things it shouldn’t — for example, bypass authentication, extract sensitive data, or modify/delete records. That flaw is called **SQL injection (SQLi)** and it remains a high-impact issue in real-world applications.

---

## 🎯 Learning objectives
By the end of this room you will be able to:

- Explain what a **database** and a **DBMS** (Database Management System) are, and how web apps interact with them.  
- Describe the core concept of **SQL injection** and why it occurs.  
- Use **sqlmap** to discover and exploit SQL injection vulnerabilities (automated enumeration and extraction).  
- Apply practical techniques in a hands-on lab to identify and extract data from a vulnerable application.

---

## 📚 Topics covered
- What is a database and common DBMS examples (MySQL, PostgreSQL, SQLite, MS SQL Server).  
- How web applications construct and send SQL queries.  
- Why unsanitized user input can lead to SQL injection.  
- Basic SQLi payloads and concepts (e.g., boolean/union/error-based injections).  
- Introduction to **sqlmap**: discovery, DBMS fingerprinting, enumeration, dumping tables and columns.  
- Practical challenge: find an injection point and extract a flag / sensitive data.

---

## 🧭 Room prerequisites
- No strict prerequisites — **SQL fundamentals** (SELECT, WHERE, basic operators) will help but are not required.  
- Familiarity with the command line is useful.  
- Basic knowledge of HTTP and web forms is helpful for understanding input vectors.

---

## 💻 Quick practical notes (sqlmap examples)
> These examples are illustrative — always run tools only against systems you are authorized to test.

```bash
# Basic test for SQL injection on a URL parameter
sqlmap -u "http://target/page.php?id=1" --batch --level=2

# Enumerate DBMS, databases, tables and columns
sqlmap -u "http://target/page.php?id=1" --dbs
sqlmap -u "http://target/page.php?id=1" -D database_name --tables
sqlmap -u "http://target/page.php?id=1" -D database_name -T table_name --columns

# Dump a specific table
sqlmap -u "http://target/page.php?id=1" -D dbname -T users --dump
