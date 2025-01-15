# postgresql

creating database

```postgresql
CREATE DATABASE database_name
```
connecting the database with the postgresql

```postgresql
\c sql_demo
```

creating table

```postgresql
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
