# Database Table Operations

## 📸 Lab Screenshots

### Lab Overview
![Lab Overview](Screenshot%20(51).png)

### Country Table Structure
![Country Table Structure](Screenshot%20(53).png)

## 📖 Scenario
The database operations team for an organization has configured a relational database instance. The team asked me to practice creating and dropping (deleting) databases and tables using SQL commands.

## 🎯 Lab Objectives
After completing this lab, I learned how to:
- Use the **CREATE** statement to create databases and tables
- Use the **SHOW** statement to view available databases and tables
- Use the **ALTER** statement to modify the structure of a table
- Use the **DROP** statement to delete databases and tables

## 🗄️ Database Structure

### Country Table Schema
| Field | Type | Null | Key | Default | Extra |
|-------|------|------|-----|---------|-------|
| Code | char(3) | NO | PRI | | |
| Name | char(52) | NO | | | |
| Continent | enum('Asia', 'Europe', 'North America', 'Africa', 'Oceania', 'Antarctica', 'South America') | NO | | Asia | |
| Region | char(26) | NO | | | |
| SurfaceArea | float(10,2) | NO | | | |
| IndepYear | smallint(6) | YES | | 0 | |
| Population | int(11) | NO | | NULL | |
| LifeExpectancy | float(3,1) | YES | | NULL | |
| GDP | float(10,2) | YES | | NULL | |
| GDPI | float(10,2) | YES | | NULL | |

## 🧠 What I Learned

### SQL Operations

**1. CREATE Operations**
- How to create a new database using `CREATE DATABASE database_name;`
- How to create tables with specific columns and data types
- Understanding different data types: `char`, `int`, `float`, `enum`, `smallint`
- Setting primary keys (`PRI`) to uniquely identify records

**2. SHOW Operations**
- Viewing all databases: `SHOW DATABASES;`
- Viewing all tables in a database: `SHOW TABLES;`
- Viewing table structure: `DESCRIBE table_name;`

**3. ALTER Operations**
- Adding new columns to existing tables
- Modifying column data types
- Renaming columns or tables

**4. DROP Operations**
- Deleting tables: `DROP TABLE table_name;`
- Deleting databases: `DROP DATABASE database_name;`

### Database Concepts

- **Primary Keys (PRI):** Used to uniquely identify each record in a table
- **Data Types:** Understanding when to use different data types (char vs varchar, int vs smallint, float)
- **NULL vs NOT NULL:** Knowing when fields must have values vs when they can be empty
- **Default Values:** Setting default values when no data is provided
- **Enum:** Using predefined lists of allowed values

### Real-World Application

This lab simulates real database administration tasks:
- Creating database schemas for applications
- Designing table structures with proper data types
- Maintaining and modifying database structures as requirements change
- Safely removing old or unused tables

## 🔧 Technologies Used
- **SQL** (Structured Query Language)
- **MySQL** (Relational Database Management System)
- **AWS Database Services** (RDS or similar)
- **Command Line Interface** (CLI) or SQL Workbench

## 🏆 Skills Demonstrated
- SQL query writing
- Database schema design
- Table creation and modification
- Database administration basics
- Understanding of relational database concepts
- Data type selection and optimization

## 📅 Lab Date
June 2026

## 🎓 Part of
AWS re/Start Program - Database Module

---

## 🔍 Sample SQL Commands Learned

```sql
-- Create a new database
CREATE DATABASE world;

-- Use a specific database
USE world;

-- Create a table
CREATE TABLE country (
    Code char(3) PRIMARY KEY,
    Name char(52) NOT NULL,
    Continent enum('Asia','Europe','North America','Africa','Oceania','Antarctica','South America') DEFAULT 'Asia',
    Region char(26) NOT NULL,
    SurfaceArea float(10,2) NOT NULL,
    IndepYear smallint(6),
    Population int(11) NOT NULL,
    LifeExpectancy float(3,1),
    GDP float(10,2),
    GDPI float(10,2)
);

-- View table structure
DESCRIBE country;

-- Add a new column
ALTER TABLE country ADD COLUMN LocalName char(50);

-- Drop a table
DROP TABLE country;
