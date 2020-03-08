# Development Database Tool
Tool to deploying databases for a software development environment.

## Databases
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/mongodb_111x30.png) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/mysql_70x47.png) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/postgres_120x55_despl.png) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

## GUIs
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/mongo-express_142x35.png) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/phpmyadmin_82x46.png) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/pgadmin_105x54.png) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

## Requirements
* Docker Community Edition (https://docs.docker.com/install/)
* Docker Compose (https://docs.docker.com/compose/install/)

## Run Mongodb and its GUI (Mongo-express)
```bash
$ docker-compose -f mongo-compose.yml start
Starting mongo         ... done
Starting mongo_express ... done
```
Go to http://localhost:5002/

##### Login Mongodb:
```text
user: root
pass: root
```

## Run Mysql and its GUI (PhpMyAdmin)
```bash
$ docker-compose -f mysql-compose.yml start
Starting mysql      ... done
Starting phpmyadmin ... done
```
Go to http://localhost:5001/

##### Login PhpMyAdmin:
```text
user: root
pass: root
```

##### Login Mysql:
```text
user: root
pass: root
```

## Run Postgres and its GUI (PgAdmin)
```bash
# Required!:  sudo chown -R 5050:5050 gui_volumes/pgadmin
$ docker-compose -f postgres-compose.yml start
Starting postgres ... done
Starting pgadmin  ... done
```
Go to http://localhost:5000/

##### Login PgAdmin:
```text
user: user@domain.com
pass: mypass
```

##### Login Postgres:
```text
user: postgres
pass: mysecretpassword
```

## Stop services. Don't worry, the data persists!
```bash
$ docker-compose -f mongo-compose.yml stop
$ docker-compose -f mysql-compose.yml stop
$ docker-compose -f postgres-compose.yml stop
```

## Remove services. Don't worry, the data continues to persist!
```bash
$ docker-compose -f mongo-compose.yml down
$ docker-compose -f mysql-compose.yml down
$ docker-compose -f postgres-compose.yml down
```
