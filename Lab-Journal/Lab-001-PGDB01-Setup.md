# Lab 001 – PostgreSQL Lab Environment Setup

## Table of Contents

- Lab Information
- Objective
- Environment
- Success Criteria
- Activities Completed
- Commands Practiced
- Skills Practiced
- Lessons Learned
- Screenshots
- Reflection
- Next Lab

## Prerequisites

- VMware Workstation Pro installed
- Ubuntu Server ISO downloaded
- Basic Linux terminal knowledge

## Lab Information

| Item | Value |
|------|-------|
| Lab Number | 001 |
| Lab Name | PostgreSQL Environment Setup |
| Author | Minhaj Ahmed |
| Date | 2026-08-06 |
| Platform | VMware Workstation Pro |
| Virtual Machine | PGDB01 |
| Operating System | Ubuntu Server 26.04 LTS |
| Database | PostgreSQL 18 |
| Status | ✅ Completed |

Estimated Duration: 45 minutes
Difficulty: Beginner
---

# Objective

Build the first PostgreSQL virtual machine for the Enterprise DBA Lab and verify that PostgreSQL is installed, running, and ready for administration.

---

# Environment

| Component | Details |
|-----------|---------|
| Hypervisor | VMware Workstation Pro |
| Virtual Machine | PGDB01 |
| Operating System | Ubuntu Server 26.04 LTS |
| Memory | 4 GB |
| CPU | 2 vCPU |
| Disk | 40 GB |
| Network | NAT |
| Database | PostgreSQL 18 |

---

# Success Criteria

The lab is considered successful when:

- Ubuntu Server is installed successfully.
- PostgreSQL is installed.
- PostgreSQL cluster status is **Online**.
- Connection to PostgreSQL using `psql` is successful.
- PostgreSQL version is verified.
- A new database (`dbalab`) is created successfully.

---

# Procedure

- Created the virtual machine **PGDB01** using VMware Workstation Pro.
- Installed Ubuntu Server 26.04 LTS.
- Updated Ubuntu packages using APT.
- Installed PostgreSQL 18 and PostgreSQL Contrib packages.
- Verified the PostgreSQL cluster status.
- Connected to PostgreSQL using the `psql` command-line interface.
- Verified the PostgreSQL version.
- Created the first PostgreSQL database named **dbalab**.

---

# Commands Practiced

## Update Ubuntu

```bash
sudo apt update
sudo apt upgrade -y
```

## Install PostgreSQL

```bash
sudo apt install postgresql postgresql-contrib -y
```

## Verify PostgreSQL Cluster

**Command**

```bash
pg_lsclusters
```

**Sample Output**

```text
Ver Cluster Port Status Owner
18  main    5432 online postgres
```

## Connect to PostgreSQL

```bash
sudo -u postgres psql
```

## Verify PostgreSQL Version

```sql
SELECT version();
```

## Create Database

```sql
CREATE DATABASE dbalab;
```

---

# Skills Practiced

- VMware virtual machine provisioning
- Ubuntu Server installation
- Linux package management (APT)
- PostgreSQL installation
- PostgreSQL cluster verification
- PostgreSQL administration using `psql`
- Database creation
- Technical documentation

---

# Lessons Learned

- PostgreSQL on Ubuntu is installed using the APT package manager.
- The PostgreSQL cluster can be verified using the `pg_lsclusters` command.
- The `psql` command-line interface is the primary tool for PostgreSQL administration.
- PostgreSQL uses port **5432** by default.
- Proper documentation improves troubleshooting and repeatability.

---

# Screenshots

## Figure 1 – VMware Virtual Machine Configuration

![VMware Settings](../Images/01-vm-settings.png)

---

## Figure 2 – Ubuntu Server Login

![Ubuntu Login](../Images/02-ubuntu-login.png)

---

## Figure 3 – PostgreSQL Version Verification

![PostgreSQL Version](../Images/03-postgresql-version.png)

---

## Figure 4 – PostgreSQL Cluster Status

![Cluster Status](../Images/04-pg-lsclusters.png)

---

## Figure 5 – Database Creation

![Create Database](../Images/05-create-database.png)

---

# Reflection

This lab established the foundation of my PostgreSQL learning environment. Beyond installing PostgreSQL, I gained hands-on experience with Ubuntu Server, Linux command-line administration, package management using APT, and PostgreSQL verification. This environment will be be used for future labs covering security, backup and recovery, performance tuning, replication, monitoring, automation, and cloud database technologies.

---

# Outcome

The PostgreSQL lab environment was successfully deployed and verified. The server is operational and ready for future exercises involving user management, backup and recovery, security, performance tuning, replication, and automation.

---

# Next Lab

**Lab 002 – PostgreSQL Roles, Users, Databases, and Schemas**

---

**Lab Status:** ✅ Completed

**Repository:** Enterprise DBA Lab

## Verification Checklist

- [x] Ubuntu installed
- [x] PostgreSQL installed
- [x] PostgreSQL cluster online
- [x] Connected using psql
- [x] Database created

# References

- PostgreSQL Documentation
- Ubuntu Server Documentation
- VMware Workstation Pro Documentation

## Document History

| Version | Date | Description |
|----------|------------|----------------------------|
| 1.0 | 2026-08-06 | Initial version |

**Author:** Minhaj Ahmed
