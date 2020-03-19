# Cheatsheet
[A good tutorial site](https://www.postgresqltutorial.com/)

## Database
| command | usage |
|---------|-------|
| `\l` | list databases. |
| `\c shoe_commerce` | connect to a database, to run queries on it. |
| `create database shoe_commerce;` | create a new database. |
| `alter database shoe_commerce rename to sock_commerce;` | alter database name. |
| `drop database shoe_commerce;` | remove a database. |

### Copying a database
```sql
CREATE DATABASE new_commerce WITH TEMPLATE shoe_commerce OWNER postgres;
```

<br/><br/><br/>

## Table
| command | usage |
|---------|-------|
| `\dt` | list tables. |
| `\d shoes` | Displays structure of table. |

### Create table
```sql
CREATE TABLE shoes(
   id serial PRIMARY KEY,
   name VARCHAR (50) NOT NULL,
   image_src TEXT NOT NULL,
   created_at TIMESTAMP default current_timestamp
);
```

### Insert data
```sql
   INSERT INTO shoes(name, image_src)
   VALUES
      ('nike', 'https://static.nike.com/a/images/t_PDP_864_v1/f_auto,b_rgb:f5f5f5/25ff6e8e-77e0-43de-b78b-37082b091533/air-jordan-1-mid-shoe-BpARGV.jpg');
```

### List data in a table
```sql
select * from shoes;
```

<br/><br/><br/>

## Relations and Joins
There are different kinds of joins. 

| Join type | Usage |
|-----------|-------|
| Inner join | one person to one passport information join |
| Left join | one person to (0-)many cars join. |
| Right join | many people to the same conuntry join. |
4. Full outer join
5. Cross join
6. Natural join
7. self-join -- special

### How to use a join

#### Left join
```sql
SELECT
-- All the columns from users and auth_tokens table that we'd like to display.
   users.id,
   users.username,
   auth_tokens.token
-- ,
FROM
-- ,
   users
--                    ON primary key field = foreign key field
LEFT JOIN auth_tokens ON users.id = auth_tokens.user_id;
```

<br/><br/><br/>

## Datatypes
[tutorial](https://www.postgresqltutorial.com/postgresql-data-types/)

1. `boolean` or `bool`
2.  `CHAR(n)` or `VARCHAR(n)` or `TEXT`
3. ... continued

<br/><br/>
# SQL concepts
## Primary keys
Unique identity for a record in table.

## Relationships
Prevents amending the same object again and again, <-- this approach is frowned upon in relational databases. 
You could create a different object in a different table and point to this one.
