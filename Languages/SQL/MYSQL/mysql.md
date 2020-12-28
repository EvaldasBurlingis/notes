## Managing database

```bash

use <database name>;                    # select database
SHOW databases;                         # list databases
CREATE DATABASE <database name>;         # create new databse

SHOW TABLES;                            # list tables
CREATE TABLE <table name>;               # create table


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