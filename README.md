# Customer-Orders-Database-Solutions (MS SQL Server)

## Overview

This repository contains a complete solution for a normalized SQL Server database capturing information about customers, their orders, and their salespersons. The solution includes:

- **Database design in 3NF**: Diagram and documentation
- **DDL and DML SQL scripts**: For all tables, views, functions, stored procedures, and sample data insertion (25+ records per table)
- **Jupyter notebook**: Python code to insert data, retrieve data, and visualize results

---

## Contents

| File/Folder          | Description                                                                                   |
|----------------------|----------------------------------------------------------------------------------------------|
| `CustomerOrdersDB.sql` | SQL file containing all DDL and DML statements (tables, views, function, procedure, inserts) |
| `CustomerOrders.ipynb` | Jupyter notebook with all Python code (data insertion, data retrieval, visualization)         |
| `DatabaseDiagram.png`  | Embedded database diagram showing tables, columns, keys, and relationships                   |
| `README.md`            | This documentation file                                                                     |

---

## Database Design

- **Tables**:
  - `SalesPerson`: Stores sales person details (`SalesPersonID`, `FirstName`, `LastName`)
  - `Customer`: Stores customer details (`CustomerID`, `CustomerName`, `State`, foreign key to `SalesPersonID`)
  - `OrderHeader`: Stores order information (`OrderNumber`, `OrderDate`, `CustomerID`)
  - `OrderDetail`: Stores order line items (`OrderDetailID`, `OrderNumber`, `ItemName`, `Quantity`, `PriceUSD`)

- **Normalization**: All tables are in 3NF, with proper use of primary and foreign keys.

- **Diagram**: See [`DatabaseDiagram.png`](DatabaseDiagram.png.pdf) for logical structure, column data types, nullability, primary keys, and foreign key directions.

---

## SQL Scripts

- **DDL**: Create tables, relationships, function for USD→Euro conversion, stored procedure for inserting salespersons.
- **DML**: Insert at least 25 records into each table.
- **Views**:
  - Customers and their salespersons
  - Most expensive item per customer
  - Most expensive item per salesperson
  - Total purchase amount per item per customer

---

## Python Scripts

- **Data Insertion**: Bulk insert 25+ records per table using `pyodbc` (or similar) in Jupyter notebook.
- **Data Retrieval**: Query the database for reporting and analysis.
- **Visualization**: Charts of sales by customer and by state using `matplotlib` or `seaborn`.

---

## Usage Instructions

1. **Database Setup**
   - Run `CustomerOrdersDB.sql` in SQL Server Management Studio to create the schema and insert sample data.

2. **Python Analysis**
   - Open `CustomerOrders.ipynb` in Jupyter.
   - Ensure you have the necessary Python libraries (`pyodbc`, `pandas`, `matplotlib`, etc.).
   - Update the connection string for your SQL Server instance.
   - Run all cells to perform data insertion/visualization.

---

## Requirements

- **SQL Server**: All SQL is written for Microsoft SQL Server (T-SQL).
- **Python**: Jupyter notebook with `pyodbc` and data visualization libraries.
- **No external dependencies**: All code runs locally.

---

## Deliverables

- **Database Diagram**: Logical names, data types, nullability, PKs, FKs (direction), in `DatabaseDiagram.png`
- **Single SQL File**: All DDL and DML in `CustomerOrdersDB.sql`
- **Jupyter Notebook**: All Python code in `CustomerOrders.ipynb`
- **README**: This file

---

## Notes

- All code, data, and diagrams are provided for your direct upload to Canvas/GitHub as required.
- The SQL file is self-contained and can be run as a single script.
- The database design and queries follow best practices for normalization and reporting.

---

## Author

[Jagadeeshwari]  
[mandapallijagadeeshwari@gmail.com]  


---
