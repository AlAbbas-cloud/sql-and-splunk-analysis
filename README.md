# SQL & Splunk Cybersecurity Analysis Project

This project showcases my hands-on work with SQL databases, SQL injection testing, big data concepts, and Splunk log analysis. It was completed as part of my cybersecurity training and demonstrates practical skills used in real Security Operations Centre (SOC) environments.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Tools & Technologies](#tools--technologies)
- [Repository Structure](#repository-structure)
- [SQL Work](#sql-work)
- [SQL Injection](#sql-injection)
- [Splunk Analysis](#splunk-analysis)
- [Big Data](#big-data)
- [SOC Responsibilities](#soc-responsibilities)
- [Troubleshooting & Contingency Task](#troubleshooting--contingency-task)
- [Skills Demonstrated](#skills-demonstrated)
- [Why This Project Matters](#why-this-project-matters)
- [Future Improvements](#future-improvements)

---

## Project Overview

This project simulates the role of a junior cybersecurity analyst at “MidTown IT.”  
The tasks include:

- Creating and managing a SQL database  
- Running SQL queries (SELECT, INSERT, UPDATE, DELETE)  
- Demonstrating SQL injection and mitigation  
- Explaining big data concepts (Four Vs)  
- Using Splunk to ingest, search, and analyse logs  
- Detecting anomalies such as brute-force attacks  
- Understanding SOC responsibilities and data sources  
- Troubleshooting database corruption scenarios  

---

## Tools & Technologies

- **MySQL / SQL Server**
- **Splunk Enterprise**
- **Heavy.AI (Big Data Demo)**
- **Windows Event Logs**
- **Linux log files**
- **Cybersecurity analysis techniques**

---

## Repository Structure

- [sql/](sql/)  
- [sql_injection/](sql_injection/)  
- [splunk/](splunk/)  
- [big_data/](big_data/)  
- [soc/](soc/)  

Each folder contains documentation, commands, screenshots, and analysis notes.

---

## SQL Work

This section includes:

- Database creation  
- Table creation  
- Insert, update, and delete operations  
- SQL queries for filtering and selecting data  
- Screenshots of the populated employee table  

See:  
👉 [`sql/`](sql/)

---

## SQL Injection

This section documents:

- The injection payload used (`' OR 'a'='a`)  
- How the bypass worked  
- Tools used for SQL injection research  
- Mitigation strategies (WAF, stored procedures, input validation)  

See:  
👉 [`sql_injection/`](sql_injection/)

---

## Splunk Analysis

This section includes:

- Splunk installation  
- Data ingestion  
- Searching logs  
- Detecting brute-force attempts  
- Screenshots of Splunk dashboards and search results  

See:  
👉 [`splunk/`](splunk/)

---

## Big Data

This section explains:

- The Four Vs of Big Data  
- How Splunk handles large datasets  
- Heavy.AI Twitter Cyber Security search  
- Screenshots of maps and tweet results  

See:  
👉 [`big_data/`](big_data/)

---

## SOC Responsibilities

This section covers:

- Monitoring  
- Incident response  
- Threat intelligence  
- Log sources (firewalls, IDS, access control, SIEM)  
- How Splunk supports SOC workflows  

See:  
👉 [`soc/`](soc/)

---

## Troubleshooting & Contingency Task

This section documents how I handled a simulated database corruption issue, including:

- Backups  
- Error log review  
- Table integrity checks  
- Recovery steps  
- XAMPP reinstallation  

See:  
👉 [`sql/troubleshooting.md`](sql/troubleshooting.md)

---

## Skills Demonstrated

- SQL database creation and management  
- SQL injection awareness and mitigation  
- Splunk log ingestion and searching  
- Anomaly detection and brute-force investigation  
- Big data concepts (Four Vs)  
- SOC-style monitoring and reporting  
- Troubleshooting and recovery workflows  
- GitHub project structuring and documentation  

---

## Why This Project Matters

This project demonstrates my ability to work with real security tools, analyse logs, detect threats, and document findings clearly. It reflects the practical skills expected in junior SOC, IT support, and cybersecurity analyst roles.

---

## Future Improvements

- Add automated scripts for log parsing  
- Build dashboards in Splunk  
- Add more SQL injection payload examples  
- Include visual diagrams of the database schema  
- Add a SOC-style incident report template  
