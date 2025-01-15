# postgresql

Creating database

```sql
CREATE DATABASE database_name
```
Connecting the database with the postgresql

```sql
\c database_name
```

Creating table

```sql
CREATE TABLE Product (
    id SERIAL PRIMARY KEY,
    category VARCHAR(100) NOT NULL,
    name VARCHAR(255) NOT NULL,
    price REAL NOT NULL,
    clearance BOOLEAN NOT NULL DEFAULT FALSE,
    color VARCHAR(50),
    size VARCHAR(3),
    length VARCHAR(20),
    material VARCHAR(100)
);
```
To insert values in the table

```sql
INSERT INTO Product (
    category, 
    name, 
    price, 
    clearance, 
    color, 
    size, 
    length, 
    material
)
VALUES
    ('hoodie', 'Cozy Hoodie', 49.99, FALSE, 'Black', 'M', 'regular', 'Cotton'),
    ('sleepwear', 'Comfy Pajamas', 29.99, TRUE, 'White', 'S', NULL, 'Cotton'),
    ('sweater', 'Winter Sweater', 79.99, FALSE, 'Red', 'L', NULL, 'Wool'),
    ('tops', 'Casual T-shirt', 19.99, TRUE, 'Blue', 'XS', NULL, 'Polyester'),
    ('other', 'Leather Jacket', 129.99, FALSE, 'Brown', 'M', NULL, 'Leather');
```

To know the description of the table

```sql
\d table_name
```
update the column in a table

```sql

update table_name
set column_name='value'
where unique_indentifier=6;

-- example:

update product
set color='pink'
where id=6;

```
