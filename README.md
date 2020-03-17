# Postgresql Notes cum Cheatsheet

## Database
| command | usage |
|---------|-------|
| `\l` | list databases. |
| `create database shoe_commerce;` | create a new database. |
| `alter database shoe_commerce rename to sock_commerce;` | alter database name. |
| `drop database shoe_commerce;` | remove a database. |

## Table
| command | usage |
|---------|-------|
| `\dt` | list tables. |

### Create table
```sql
CREATE TABLE shoes(
   id serial PRIMARY KEY,
   name VARCHAR (50) NOT NULL,
   image_src TEXT NOT NULL,
   created_at TIMESTAMP default current_timestamp
);
```

## Datatypes
[tutorial](https://www.postgresqltutorial.com/postgresql-data-types/)

1. `boolean` or `bool`
2.  `CHAR(n)` or `VARCHAR(n)` or `TEXT`
3. ... continued
