# Data Catalog for Gold Layer

## Overview

The Gold Layer represents business-ready data structured to support analytical queries, reporting, and decision-making. It consists of dimension tables and fact tables designed using a star schema.

---

## 1. `gold.dim_customers`

**Purpose:** Stores customer information enriched with demographic and geographic attributes.

| Column Name | Data Type | Description |
|---|---|---|
| `customer_key` | INT | Surrogate key uniquely identifying each customer record in the dimension table. |
| `customer_id` | INT | Unique numerical identifier assigned to each customer. |
| `customer_number` | NVARCHAR(50) | Alphanumeric customer identifier used for tracking and referencing. |
| `first_name` | NVARCHAR(50) | Customer's first name. |
| `last_name` | NVARCHAR(50) | Customer's last name or family name. |
| `country` | NVARCHAR(50) | Country associated with the customer. |
| `marital_status` | NVARCHAR(50) | Customer's marital status, such as Married or Single. |
| `gender` | NVARCHAR(50) | Customer's gender, such as Male, Female, or n/a. |
| `birthdate` | DATE | Customer's date of birth. |
| `create_date` | DATE | Date the customer record was created in the source system. |

---

## 2. `gold.dim_products`

**Purpose:** Stores product information and attributes, including category, subcategory, cost, and product line.

| Column Name | Data Type | Description |
|---|---|---|
| `product_key` | INT | Surrogate key uniquely identifying each product record in the dimension table. |
| `product_id` | INT | Unique numerical identifier assigned to the product. |
| `product_number` | NVARCHAR(50) | Alphanumeric product code used for identification and tracking. |
| `product_name` | NVARCHAR(50) | Descriptive name of the product, including details such as type, color, or size. |
| `category_id` | NVARCHAR(50) | Identifier associated with the product category. |
| `category` | NVARCHAR(50) | High-level classification of the product, such as Bikes or Components. |
| `subcategory` | NVARCHAR(50) | More specific classification within the product category. |
| `maintenance` | NVARCHAR(50) | Indicates whether the product requires maintenance. |
| `cost` | INT | Product cost in whole currency units. |
| `product_line` | NVARCHAR(50) | Product line or series to which the product belongs. |
| `start_date` | DATE | Date the product became available or the product record became effective. |

---

## 3. `gold.fact_sales`

**Purpose:** Stores sales transaction details and connects customer and product dimensions for analytical reporting.

| Column Name | Data Type | Description |
|---|---|---|
| `
