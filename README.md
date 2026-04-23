# goit-rdb-hw-02

## Homework 02

**Database Design Using Semantic Models**

This project contains the completed homework for Topic 2, focused on database normalization, ER modeling, and schema creation in MySQL Workbench.

---

## Task Overview

The initial table was analyzed and transformed step by step into:

- **First Normal Form (1NF)**
- **Second Normal Form (2NF)**
- **Third Normal Form (3NF)**

After normalization:

- an **ER diagram** was created;
- tables were implemented in **MySQL Workbench**;
- relationships between entities were defined using primary and foreign keys.

---

## Initial Table

The source table contained the following fields:

- Order Number
- Product Name and Quantity
- Client Address
- Order Date
- Client Name

This structure contained duplicated data and non-atomic values, so normalization was required.

---

## Final Database Structure

The final schema consists of 4 tables:

### `clients`

Stores client information.

- client_id
- client_name
- client_address

### `orders`

Stores customer orders.

- order_id
- order_date
- client_id

### `products`

Stores product names.

- product_id
- product_name

### `order_items`

Stores products included in each order.

- order_item_id
- order_id
- product_id
- quantity

---

## Relationships

- One client can have many orders (**1:N**)
- One order can have many order items (**1:N**)
- One product can appear in many order items (**1:N**)

---

## Repository Structure

```text
goit-rdb-hw-02/
│
├── README.md
├── schema.sql
└── screenshots/
    ├── p1_1nf.png
    ├── p2_2nf.png
    ├── p3_3nf.png
    ├── p4_er_diagram.png
    └── p5_workbench_schema.png
```
