# MySQL vs MongoDB

## Overview

### MySQL
- **Type**: Relational Database Management System (RDBMS)
- **Data Model**: Tables with rows and columns
- **Schema**: Fixed schema (tables must be defined before use)
- **Query Language**: SQL (Structured Query Language)
- **Transactions**: Supports ACID transactions
- **Use Cases**: Traditional applications requiring structured data, complex queries, and transactions

### MongoDB
- **Type**: NoSQL Document Database
- **Data Model**: JSON-like documents (BSON)
- **Schema**: Schema-less (flexible schema)
- **Query Language**: MongoDB Query Language (MQL)
- **Transactions**: Supports multi-document ACID transactions (introduced in MongoDB 4.0)
- **Use Cases**: Applications with dynamic or unstructured data, real-time analytics, and rapid development

## Data Model

### MySQL
- **Tables**: Data is stored in tables with predefined schemas.
- **Rows and Columns**: Each table has rows (records) and columns (attributes).
- **Relationships**: Supports relationships between tables (one-to-one, one-to-many, many-to-many) using foreign keys.

### MongoDB
- **Documents**: Data is stored as documents in collections.
- **BSON**: Binary JSON format for documents (supports nested structures).
- **Collections**: Group of documents (similar to tables in SQL).

## Schema

### MySQL
- **Schema Design**: Requires a fixed schema; changes require migration.
- **Normalization**: Data normalization to reduce redundancy.

### MongoDB
- **Schema Flexibility**: Schema can vary between documents within the same collection.
- **Denormalization**: Often denormalized data to optimize read performance.

## Query Language

### MySQL
- **SQL**: Uses SQL for querying and managing data.
  ```sql
  SELECT * FROM users WHERE age > 25;
