# 📚 Library Management System – Enterprise Database Design

## 🚀 Overview

The **Library Management System** is a high-performance relational database solution designed to manage complex library ecosystems. The system focuses on scalability, strict data integrity, and enterprise-grade relational modeling using SQL Server.

This project follows a **Data-First approach**, starting with detailed Entity-Relationship (ER) analysis and transforming it into a fully normalized relational schema (3NF).

---

## 🏗 Architectural Foundation

### ✔ Schema Normalization (3NF)

The database is fully optimized to Third Normal Form (3NF) to eliminate:

* Data redundancy
* Update anomalies
* Inconsistent dependencies

### ✔ Recursive Staff Hierarchy

Implemented a self-referencing relationship using:

```
SupervisorID → Employees.Emp_ID
```

This enables modeling of multi-level organizational structures within a single Employees entity.

### ✔ Physical Asset Mapping

Granular tracking of physical inventory through hierarchical mapping:

```
Floor → Block → Shelf → Book
```

This design ensures efficient asset organization and retrieval.

---

## 🧩 Advanced Design Patterns

### 🔁 Circular Dependency Resolution

Resolved mutual dependencies between **Employees** and **Floors** using staged constraint injection via:

```
ALTER TABLE
```

This approach ensures referential integrity without violating creation order.

### 🔗 Many-to-Many Relationship Handling

Implemented a junction table:

```
Author_Book
```

to manage scalable N:M relationships between Authors and Books.

### 📞 Multivalued Attribute Normalization

User contact numbers were separated into a dedicated table:

```
User_Phones
```

This allows multiple phone numbers per user while maintaining normalization rules.

---

## 🛠 Technical Specifications

| Category       | Technology / Concept                  |
| -------------- | ------------------------------------- |
| DBMS           | SQL Server                            |
| Modeling Level | Advanced Relational Mapping           |
| Integrity      | Entity, Domain, Referential Integrity |
| Scalability    | 10+ Relational Entities               |
| Validation     | UNIQUE, CHECK, DEFAULT Constraints    |

---

## 🚀 Enterprise-Grade Features

### 🔐 Secure Identification

* UNIQUE constraint on SSN
* UNIQUE constraint on Email

Prevents identity duplication across the system.

### 🏢 Asset Lifecycle Management

Designed to support dynamic expansion of:

* Library wings
* Floors
* Shelving units

### 🔄 Transactional Precision

The **Borrow** entity functions as a transactional ledger including:

* Date_Borrowed
* Due_Date
* Financial Amount (DECIMAL for accuracy)

### 🛡 Referential Guards

Strict FOREIGN KEY constraints prevent orphan records across all modules.

### 📑 Performance Optimization

* Indexed Primary Keys
* Optimized data types
* Efficient relational mapping

---

## 📊 Database Layers Included

1. **Conceptual Model** – ER Diagram
2. **Logical Model** – Relational Schema
3. **Physical Model** – SQL Server Implementation

---

## 🎯 Key Learning Outcomes

* Advanced ER Modeling
* Constraint-Driven Database Design
* Circular Dependency Handling
* Enterprise-Level Data Integrity Enforcement
* Scalable Relational Architecture

---

## 📌 Conclusion

This project demonstrates a production-oriented database architecture designed with enterprise principles, focusing on data consistency, maintainability, and long-term scalability.

---

### ⭐ If you find this project useful, consider giving it a star on
