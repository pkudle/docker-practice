This is sample project, done to deploy student registration app.
- Backend is in Java Sprinboot
- Frontend is in React
- Database used is MariaDB

# MariaDB Setup and Configuration Guide for Windows

This guide explains how to set up MariaDB, create a database, and Create Database User

## 1. Installing MariaDB

Installing MariaDB on Ubntu

```shell
apt update && apt install mariadb-server -y
```

## 2. Securing MariaDB

Open the Command Prompt as Administrator and run the following command to secure your installation:

```shell

mysql_secure_installation
```

Follow the prompts to:
Set a root password.
Remove insecure default users and test databases.
Disable remote root login.

## 3. Setting Up the Database

Open terminal and login to MariaDB:

```bash

mysql -u root -p
```

Enter the root password when prompted.

Create a new database and user:

```sql
CREATE DATABASE student_db;
GRANT ALL PRIVILEGES ON springbackend.* TO 'username'@'localhost' IDENTIFIED BY 'your_password';
```
Replace username and your_password with your desired username and password.

Exit MariaDB:

```sql

EXIT;
```

## 4. You will need Database Credentials to Connect Backend with Database
1. DB_HOST = 172.17.0.2
2. DB_USER = root
3. DB_PASS = redhat
4. DB_PORT = 3306
5. DB_NAME = student_db

