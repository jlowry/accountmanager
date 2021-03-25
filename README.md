# accountmanager

## Dependencies
```sh
apt install lua-dbi-mysql
```

unpack into opt

update service files.

## Database setup
```sql
CREATE DATABASE accountmanager CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_520_ci;
CREATE USER 'accountmanager'@'localhost' IDENTIFIED BY 'secret';
GRANT CREATE, ALTER, INDEX, SELECT, UPDATE, INSERT, DELETE, REFERENCES ON accountmanager TO 'accountmanager'@'localhost';
```

ensure that there is random data in the key

update the database connection details.

```
./manage.py migrate
```

## Building 
```
apt install build-essential python3-dev default-libmysqlclient-dev
```

