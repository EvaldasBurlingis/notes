## Managing database

```bash

use <database name>;                    # select database
SHOW databases;                         # list databases
CREATE DATABASE <database name>;        # create new databse
DROP DATABASE <database name>           # drop database

SHOW TABLES;                            # list tables
CREATE TABLE <table name>;              # create table
DROP TABLE <table name>;                # remove table


```

## QUERIES

* Get all data

```sql
    SELECT * FROM <table name>;
```

* Get selected columns

```sql
    SELECT id, email FROM <table name>;
```

* Get specified data.
**Operators:** =, >, <, >=, <=, !=, BETWEEN, LIKE, IN 

```sql
    SELECT * FROM <table name> WHERE id = 5'
```

## Managing users

```bash

CREATE USER '<name>'@'localhost' IDENTIFIED WITH mysql_native_password BY '<password>';         # create new user
GRANT ALL PRIVILEGES ON <database>.* TO '<user>'@'localhost';                                   # grant all privileges to specific database

mysql -u <user> -p                                                                              # access database
```

## Checking status of mysql

```bash

systemctl status mysql.service          # get status of mysql server
sudo systemctl start mysql              # start mysql server
sudo systemctl stop mysql               # stop mysql server

```

