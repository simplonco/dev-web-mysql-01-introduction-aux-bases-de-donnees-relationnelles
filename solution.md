---
title: "MySQL 01 - Introduction aux bases de données relationnelles - Solution"
description: "Comprendre les bases de données relationnelles et écrire tes premières requêtes SQL"
show_toc: true
parent: MySQL 01 - Introduction aux bases de données relationnelles
---

## Créer la base de données

```sql
CREATE DATABASE wild_db_quest;
USE wild_db_quest;
```

## Créer la table wizard

```sql
CREATE TABLE wizard (
  id INT NOT NULL AUTO_INCREMENT,
  firstname VARCHAR(100) NOT NULL,
  lastname VARCHAR(100) NOT NULL,
  birthday DATE DEFAULT NULL,
  birth_place VARCHAR(255) DEFAULT NULL,
  biography TEXT DEFAULT NULL,
  PRIMARY KEY (id)
);
```

## Modifier la table wizard

```sql
ALTER TABLE wizard
  ADD is_muggle BOOLEAN NOT NULL DEFAULT 0;
```

## Créer la table school

```sql
CREATE TABLE school (
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(100) NOT NULL,
  capacity INT,
  country VARCHAR(255) NOT NULL,
  PRIMARY KEY (id)
);
```

## SHOW TABLES

```
+-------------------------+
| Tables_in_wild_db_quest |
+-------------------------+
| school                  |
| wizard                  |
+-------------------------+
```

## DESCRIBE wizard

```
+-------------+--------------+------+-----+---------+----------------+
| Field       | Type         | Null | Key | Default | Extra          |
+-------------+--------------+------+-----+---------+----------------+
| id          | int          | NO   | PRI | NULL    | auto_increment |
| firstname   | varchar(100) | NO   |     | NULL    |                |
| lastname    | varchar(100) | NO   |     | NULL    |                |
| birthday    | date         | YES  |     | NULL    |                |
| birth_place | varchar(255) | YES  |     | NULL    |                |
| biography   | text         | YES  |     | NULL    |                |
| is_muggle   | tinyint(1)   | NO   |     | 0       |                |
+-------------+--------------+------+-----+---------+----------------+
```

## DESCRIBE school

```
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| id       | int          | NO   | PRI | NULL    | auto_increment |
| name     | varchar(100) | NO   |     | NULL    |                |
| capacity | int          | YES  |     | NULL    |                |
| country  | varchar(255) | NO   |     | NULL    |                |
+----------+--------------+------+-----+---------+----------------+
```