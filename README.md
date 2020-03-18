# Postgresql

## Cheatsheet
### Database
| command | usage |
|---------|-------|
| `\l` | list databases. |
| `create database shoe_commerce;` | create a new database. |
| `alter database shoe_commerce rename to sock_commerce;` | alter database name. |
| `drop database shoe_commerce;` | remove a database. |

### Table
| command | usage |
|---------|-------|
| `\dt` | list tables. |

#### Create table
```sql
CREATE TABLE shoes(
   id serial PRIMARY KEY,
   name VARCHAR (50) NOT NULL,
   image_src TEXT NOT NULL,
   created_at TIMESTAMP default current_timestamp
);
```

#### Insert data
```sql
   INSERT INTO shoes(name, image_src)
   VALUES
      ('nike', 'https://static.nike.com/a/images/t_PDP_864_v1/f_auto,b_rgb:f5f5f5/25ff6e8e-77e0-43de-b78b-37082b091533/air-jordan-1-mid-shoe-BpARGV.jpg');
```

### Data
#### List data in a table
```sql
select * from shoes;
```

### Datatypes
[tutorial](https://www.postgresqltutorial.com/postgresql-data-types/)

1. `boolean` or `bool`
2.  `CHAR(n)` or `VARCHAR(n)` or `TEXT`
3. ... continued

## SQL concepts
### Primary keys
