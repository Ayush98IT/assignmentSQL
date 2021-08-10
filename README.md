# assignmentSQL
MySQL Shell 8.0.26

Copyright (c) 2016, 2021, Oracle and/or its affiliates.
Oracle is a registered trademark of Oracle Corporation and/or its affiliates.
Other names may be trademarks of their respective owners.

Type '\help' or '\?' for help; '\quit' to exit.
 MySQL  JS > \sql
Switching to SQL mode... Commands end with ;
 MySQL  SQL > create schema `seriesdb`;
ERROR: Not connected.
 MySQL  SQL > \connect root@localhost
Creating a session to 'root@localhost'
Please provide the password for 'root@localhost': **********
Save password for 'root@localhost'? [Y]es/[N]o/Ne[v]er (default No): Yes
Fetching schema names for autocompletion... Press ^C to stop.
Your MySQL connection id is 11 (X protocol)
Server version: 8.0.26 MySQL Community Server - GPL
No default schema selected; type \use <schema> to set one.
 MySQL  localhost:33060+ ssl  SQL > create schema `seriesdb`;
Query OK, 1 row affected (0.0088 sec)
 MySQL  localhost:33060+ ssl  SQL > show database;
ERROR: 1064: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'database' at line 1
 MySQL  localhost:33060+ ssl  SQL > show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| seriesdb           |
| sys                |
+--------------------+
5 rows in set (0.0062 sec)
 MySQL  localhost:33060+ ssl  SQL > create table name(id INT NOT NULL AUTO_INCREMENT,name VARCHAR(256)NOT NULL,PRIMARY KEY(id));
ERROR: 1046: No database selected
 MySQL  localhost:33060+ ssl  SQL > connect database
                                 ->
                                 -> connect database;
ERROR: 1064: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'connect database
connect database' at line 1
 MySQL  localhost:33060+ ssl  SQL > connect databases
                                 -> c
                                 -> connect databases;
ERROR: 1064: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'connect databases
c
connect databases' at line 1
 MySQL  localhost:33060+ ssl  SQL > connect databases;
ERROR: 1064: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'connect databases' at line 1
 MySQL  localhost:33060+ ssl  SQL > connect database;
ERROR: 1064: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'connect database' at line 1
 MySQL  localhost:33060+ ssl  SQL > connect databases;
ERROR: 1064: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'connect databases' at line 1
 MySQL  localhost:33060+ ssl  SQL > show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |              create table director(id INT NOT NULL AUTO_INCREMENT,nameVARCHAR(256)NOT NULL,PRIMARY J)
                                 -> create table director(id INT NOT NULL AUTO_INCREMENT,nameVARCHAR(256)NOT NULL,PRIMARY J)
                                 -> create table director(id INT NOT NULL AUTO_INCREMENT,nameVARCHAR(256)NOT NULL,PRIMARY JI)
                                 -> create table director(id INT NOT NULL AUTO_INCREMENT,nameVARCHAR(256)NOT NULL,PRIMARY J)
                                 -> create table director(id INT NOT NULL AUTO_INCREMENT,nameVARCHAR(256)NOT NULL,PRIMARY )
                                 -> create table director(id INT NOT NULL AUTO_INCREMENT,nameVARCHAR(256)NOT NULL,PRIMARY)
                                 -> create table director(id INT NOT NULL AUTO_INCREMENT,nameVARCHAR(256)NOT NULL,PRIMAR)
                                 -> ]HH;
ERROR: 1064: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '(256)NOT NULL,PRIMARY J)
]HH' at line 1
 MySQL  localhost:33060+ ssl  SQL > create table `name`(id INT NOT NULL AUTO_INCREMENT,name VARCHAR(256)NOT NULL,PRIMARY KEY(id));
ERROR: 1046: No database selected
 MySQL  localhost:33060+ ssl  SQL > create database seriesdb;
ERROR: 1007: Can't create database 'seriesdb'; database exists
 MySQL  localhost:33060+ ssl  SQL > use seriesdb;
Default schema set to `seriesdb`.
Fetching table and column names from `seriesdb` for auto-completion... Press ^C to stop.
 MySQL  localhost:33060+ ssl  seriesdb  SQL > create table name(id INT NOT NULL AUTO_INCREMENT,name VARCHAR(256)NOT NULL,PRIMARY KEY(id));
Query OK, 0 rows affected (0.0433 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into name (name) values ('money heist');
Query OK, 1 row affected (0.0113 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into name (name) values ('pilot');
Query OK, 1 row affected (0.0096 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > describe seriesdb;
ERROR: 1146: Table 'seriesdb.seriesdb' doesn't exist
 MySQL  localhost:33060+ ssl  seriesdb  SQL > describe name;
+-------+--------------+------+-----+---------+----------------+
| Field | Type         | Null | Key | Default | Extra          |
+-------+--------------+------+-----+---------+----------------+
| id    | int          | NO   | PRI | NULL    | auto_increment |
| name  | varchar(256) | NO   |     | NULL    |                |
+-------+--------------+------+-----+---------+----------------+
2 rows in set (0.0145 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from seriesdb;
ERROR: 1146: Table 'seriesdb.seriesdb' doesn't exist
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from name;
+----+-------------+
| id | name        |
+----+-------------+
|  1 | money heist |
|  2 | pilot       |
+----+-------------+
2 rows in set (0.0005 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into name (name) values ('ray');
Query OK, 1 row affected (0.0090 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from name;
+----+-------------+
| id | name        |
+----+-------------+
|  1 | money heist |
|  2 | pilot       |
|  3 | ray         |
+----+-------------+
3 rows in set (0.0063 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > create table genre(id INT NOT NULL AUTO_INCREMENT,name VARCHAR(256)NOT NULL,PRIMARY KEY(id));
Query OK, 0 rows affected (0.0299 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into genre (name) values ('suspense');
Query OK, 1 row affected (0.0106 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select * from genre
                                           -> select*from genre;
ERROR: 1064: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'select*from genre' at line 2
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from genre;
+----+----------+
| id | name     |
+----+----------+
|  1 | suspense |
+----+----------+
1 row in set (0.0004 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into genre (genre) values ('suspense');
ERROR: 1054: Unknown column 'genre' in 'field list'
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from genre;
+----+----------+
| id | name     |
+----+----------+
|  1 | suspense |
+----+----------+
1 row in set (0.0010 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from name;
+----+-------------+
| id | name        |
+----+-------------+
|  1 | money heist |
|  2 | pilot       |
|  3 | ray         |
+----+-------------+
3 rows in set (0.0009 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into name (name) values ('the 100');
Query OK, 1 row affected (0.0112 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into name (name) values ('ozark');
Query OK, 1 row affected (0.0100 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from name;
+----+-------------+
| id | name        |
+----+-------------+
|  1 | money heist |
|  2 | pilot       |
|  3 | ray         |
|  4 | the 100     |
|  5 | ozark       |
+----+-------------+
5 rows in set (0.0007 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into genre (name) values ('thriller');
Query OK, 1 row affected (0.0088 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into genre (name) values ('action');
Query OK, 1 row affected (0.0083 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from genre;
+----+----------+
| id | name     |
+----+----------+
|  1 | suspense |
|  2 | thriller |
|  3 | action   |
+----+----------+
3 rows in set (0.0007 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into genre (name) values ('action');
Query OK, 1 row affected (0.0100 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into genre (name) values ('action');
Query OK, 1 row affected (0.0092 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from genre;
+----+----------+
| id | name     |
+----+----------+
|  1 | suspense |
|  2 | thriller |
|  3 | action   |
|  4 | action   |
|  5 | action   |
+----+----------+
5 rows in set (0.0008 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > create table director(id INT NOT NULL AUTO_INCREMENT,name VARCHAR(256)NOT NULL,PRIMARY KEY(id));
Query OK, 0 rows affected (0.0292 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into director (name) values ('jesus colemnar');
Query OK, 1 row affected (0.0129 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into director (name) values ('sam seder');
Query OK, 1 row affected (0.0023 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into director (name) values ('srijit mukherji');
Query OK, 1 row affected (0.0097 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into director (name) values ('jason rothenberg');
Query OK, 1 row affected (0.0090 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into director (name) values ('peter mulan');
Query OK, 1 row affected (0.0097 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from director;
+----+------------------+
| id | name             |
+----+------------------+
|  1 | jesus colemnar   |
|  2 | sam seder        |
|  3 | srijit mukherji  |
|  4 | jason rothenberg |
|  5 | peter mulan      |
+----+------------------+
5 rows in set (0.0007 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > create table country(id INT NOT NULL AUTO_INCREMENT,name VARCHAR(256)NOT NULL,PRIMARY KEY (id));
Query OK, 0 rows affected (0.0299 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into country (name) values ('spain');
Query OK, 1 row affected (0.0097 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into country (name) values ('us');
Query OK, 1 row affected (0.0082 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into country (name) values ('us');
Query OK, 1 row affected (0.0089 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into country (name) values ('aus');
Query OK, 1 row affected (0.0097 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from country;
+----+-------+
| id | name  |
+----+-------+
|  1 | spain |
|  2 | us    |
|  3 | us    |
|  4 | aus   |
+----+-------+
4 rows in set (0.0005 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into country (name) values ('ind');
Query OK, 1 row affected (0.0082 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from country;
+----+-------+
| id | name  |
+----+-------+
|  1 | spain |
|  2 | us    |
|  3 | us    |
|  4 | aus   |
|  5 | ind   |
+----+-------+
5 rows in set (0.0059 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > create table status(id INT NOT NULL AUTO_INCREMENT,name VARCHAR(256)NOT NULL,PRIMARY KEY(id));
Query OK, 0 rows affected (0.0344 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into status (name) values ('availabel');
Query OK, 1 row affected (0.0108 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into status (name) values ('availabel');
Query OK, 1 row affected (0.0093 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into status (name) values ('discontinued');
Query OK, 1 row affected (0.0031 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into status (name) values ('availabel');
Query OK, 1 row affected (0.0079 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into status (name) values ('discontinued');
Query OK, 1 row affected (0.0084 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from status;
+----+--------------+
| id | name         |
+----+--------------+
|  1 | availabel    |
|  2 | availabel    |
|  3 | discontinued |
|  4 | availabel    |
|  5 | discontinued |
+----+--------------+
5 rows in set (0.0006 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > create table yor(id INT NOT NULL AUTO_INCREMENT,name VARCHAR(256)NOT NULL,PRIMARY KEY(id));
Query OK, 0 rows affected (0.0301 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yor (name) values ('2010');
Query OK, 1 row affected (0.0157 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yor (name) values ('2013');
Query OK, 1 row affected (0.0087 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yor (name) values ('2000');
Query OK, 1 row affected (0.0090 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yor (name) values ('2019');
Query OK, 1 row affected (0.0083 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yor (name) values ('2012');
Query OK, 1 row affected (0.0087 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from yor;
+----+------+
| id | name |
+----+------+
|  1 | 2010 |
|  2 | 2013 |
|  3 | 2000 |
|  4 | 2019 |
|  5 | 2012 |
+----+------+
5 rows in set (0.0007 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > create table yoe(id INT NOT NULL AUTO_INCREMENT,name VARCHAR(256)NOT NULL,PRIMARY KEY(id));
Query OK, 0 rows affected (0.0290 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yoe (name) values ('exist');
Query OK, 1 row affected (0.0151 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yoe (name) values ('exist');
Query OK, 1 row affected (0.0090 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yoe (name) values ('2021');
Query OK, 1 row affected (0.0086 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yoe (name) values ('2010');
Query OK, 1 row affected (0.0085 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > insert into yoe (name) values ('exist');
Query OK, 1 row affected (0.0083 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL > select*from yoe;
+----+-------+
| id | name  |
+----+-------+
|  1 | exist |
|  2 | exist |
|  3 | 2021  |
|  4 | 2010  |
|  5 | exist |
+----+-------+
5 rows in set (0.0015 sec)
 MySQL  localhost:33060+ ssl  seriesdb  SQL >
