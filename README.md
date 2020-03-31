# Development Database Tool
Tool to deploying databases for a software development environment.

<br>

## Databases
&nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/mongodb_45x57.png) &nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/mysql_70x47.png) &nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/postgres_120x55_despl.png) &nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/Apache_Cassandra_66_60.png) &nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/mariadb_65x55.png) &nbsp;&nbsp;&nbsp;

## GUIs
&nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/mongo-express_142x35.png) &nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/phpmyadmin_82x46.png) &nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/pgadmin_105x54.png) &nbsp;&nbsp;&nbsp;
![Mysql Logo](resources/cassandra_web_69_61b.png) &nbsp;&nbsp;&nbsp;

<br>

## Requirements
* Docker Community Edition (https://docs.docker.com/install/)
* Docker Compose (https://docs.docker.com/compose/install/)

<br>

## Run Mongodb (and Mongo-express)
```bash
$ docker-compose -f mongo-compose.yml up -d
Starting mongo         ... done
Starting mongo_express ... done
```
Go to http://localhost:5002/

##### Login Mongodb:
```text
user: root
pass: root
```

## Run Mysql (and PhpMyAdmin)
```bash
$ docker-compose -f mysql-compose.yml up -d
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

## Run Postgres (and PgAdmin)
```bash
# Required!:  sudo chown -R 5050:5050 gui_volumes/pgadmin
$ docker-compose -f postgres-compose.yml up -d
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

## Run Cassandra (and Cassandra-Web)
```bash
$ docker-compose -f cassandra-compose.yml up -d cassandra
Starting cassandra     ... done
# Wait 30 seconds for the cassandra service to finish getting up
$ docker-compose -f cassandra-compose.yml up -d cassandra-web
Starting cassandra-web ... done
```
Go to http://localhost:5003/

## Run MariaDB (and PhpMyAdmin)
```bash
$ docker-compose -f mariadb-compose.yml up -d
Starting mariadb    ... done
Starting phpmyadmin ... done
```
Go to http://localhost:5004/

##### Login PhpMyAdmin:
```text
user: root
pass: root
```

##### Login MariaDB:
```text
user: root
pass: root
```

## Stop services. Don't worry, the data persists!
```bash
$ docker-compose -f mongo-compose.yml stop
$ docker-compose -f mysql-compose.yml stop
$ docker-compose -f postgres-compose.yml stop
$ docker-compose -f cassandra-compose.yml stop
$ docker-compose -f mariadb-compose.yml stop
```

## Remove services. Don't worry, the data continues to persist!
```bash
$ docker-compose -f mongo-compose.yml down
$ docker-compose -f mysql-compose.yml down
$ docker-compose -f postgres-compose.yml down
$ docker-compose -f cassandra-compose.yml down
$ docker-compose -f mariadb-compose.yml down
```

<br>

## License
[MIT](LICENSE)