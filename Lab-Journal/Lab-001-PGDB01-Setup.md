# Lab 001 – PostgreSQL Lab Environment Setup

**Date:** 2026-08-06

## Objective

Build the first PostgreSQL virtual machine for the Enterprise DBA Lab.

---

## Activities Completed

* Created a VMware Workstation Pro virtual machine named PGDB01.
* Installed Ubuntu Server 26.04 LTS.
* Updated the operating system packages.
* Installed PostgreSQL 18.
* Verified the PostgreSQL cluster was online.
* Connected to PostgreSQL using the `psql` command-line client.
* Executed the first SQL query.
* Created the first PostgreSQL database.

---

## Commands Practiced

```bash
sudo apt update
sudo apt upgrade -y
sudo apt install postgresql postgresql-contrib -y
pg_lsclusters
sudo -u postgres psql
```

```sql
SELECT version();
CREATE DATABASE dbalab;
```

---

## Lessons Learned

* PostgreSQL clusters on Ubuntu can be verified using `pg_lsclusters`.
* The `psql` client is the primary command-line interface for PostgreSQL.
* Linux package management uses `apt` for installing and updating software.
* Proper documentation is an important part of database administration.

---

## Next Steps

* Learn PostgreSQL roles and users.
* Explore databases and schemas.
* Understand PostgreSQL configuration files.
* Begin backup and recovery exercises.

## Screenshots

### Figure 1 - VMware Virtual Machine Settings

![VMware Settings](../Images/01-vm-settings.png)

---

### Figure 2 - Ubuntu Server Login

![Ubuntu Login](../Images/02-ubuntu-login.png)

---

### Figure 3 - PostgreSQL Version

![PostgreSQL Version](../Images/03-postgresql-version.png)

---

### Figure 4 - PostgreSQL Cluster Status

![Cluster Status](../Images/04-pg-lsclusters.png)

---

### Figure 5 - First Database Created

![Create Database](../Images/05-create-database.png)
