---
description: Aprende cómo conectar tu instancia de aimicromind a una database
---

# Databases

***

aimicromind soporta 4 tipos de databases:

* SQLite
* MySQL
* PostgreSQL
* MariaDB

## SQLite (Default)

SQLite será la default database. Estas databases se pueden configurar con las siguientes environment variables:

```sh
DATABASE_TYPE=sqlite
DATABASE_PATH=/root/.aimicromind #tu preferred location
```

Un archivo `database.sqlite` será created y saved en el path especificado por `DATABASE_PATH`. Si no se especifica, el default store path será en tu home directory -> .aimicromind

**Note:** Si ninguna de las environment variables está especificada, SQLite será la fallback database choice.

## MySQL

```sh
DATABASE_TYPE=mysql
DATABASE_PORT=3306
DATABASE_HOST=localhost
DATABASE_NAME=aimicromind
DATABASE_USER=user
DATABASE_PASSWORD=123
```

## PostgreSQL

```sh
DATABASE_TYPE=postgres
DATABASE_PORT=5432
DATABASE_HOST=localhost
DATABASE_NAME=aimicromind
DATABASE_USER=user
DATABASE_PASSWORD=123
PGSSLMODE=require
```

## MariaDB

```bash
DATABASE_TYPE="mariadb"
DATABASE_PORT="3306"
DATABASE_HOST="localhost"
DATABASE_NAME="aimicromind"
DATABASE_USER="aimicromind"
DATABASE_PASSWORD="mypassword"
```

## How to use aimicromind databases SQLite y MySQL/MariaDB

# The video tutorial for that coming soon 
