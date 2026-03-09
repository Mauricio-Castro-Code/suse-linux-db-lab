# SAP Basis Infrastructure Simulation Lab 🛠️

## 🎯 Objective
This project serves as a hands-on simulation of an enterprise SAP back-end environment. The goal is to demonstrate practical proficiency in Linux system administration, command-line operations, and relational database management—core competencies required for a Junior SAP Basis / TMS Engineer.

## 💻 Tech Stack & Environment
* **Operating System:** openSUSE Leap 16.0 (AArch64) - Headless Server setup
* **Database Engine:** PostgreSQL
* **Virtualization:** Parallels Desktop (running on Apple Silicon / ARM architecture)
* **Core Tools:** Bash CLI, `zypper` package manager, `systemd`

## ⚙️ Key Operations Executed

### 1. Headless Server Deployment & Navigation
* Deployed an openSUSE environment without a Graphical User Interface (GUI) to simulate real-world server conditions.
* Navigated and administered the system exclusively via the Command Line Interface (CLI).

### 2. Package & Service Management
* Utilized SUSE's native package manager (`zypper`) to fetch, install, and configure the PostgreSQL server.
* Managed background services (daemons) using `systemctl`, ensuring the database engine is enabled for persistence (`systemctl enable`) and monitoring its health status (`systemctl status`).

### 3. Database Administration & SQL
* Switched user environments securely (`su - postgres`) to manage the database engine.
* Created a test database (`sap_test`) and structured tables to simulate an SAP user registry.
* Executed standard SQL queries (`CREATE`, `INSERT`, `SELECT`) to validate data integrity and operational success.

---

## 📸 Lab Evidence

*Note: The following screenshots validate the successful execution of CLI commands and database operations.*

### 1. Service Monitoring (systemctl)
> *Demonstrating the PostgreSQL service actively running and enabled on the SUSE server.*
> <img width="1023" height="805" alt="Captura de pantalla 2026-03-04 a la(s) 1 00 10 p m" src="https://github.com/user-attachments/assets/14bd7604-98b5-4457-bd7b-522e7abfd196" />

### 2. Database Creation & SQL Queries
> *Demonstrating successful connection to the DB engine, table creation, and querying synthetic SAP user data.*
> <img width="1024" height="572" alt="Captura de pantalla 2026-03-04 a la(s) 1 04 12 p m" src="https://github.com/user-attachments/assets/0f879817-0ec4-4473-a786-06ebadb36ec2" />

---

### 4. Synthetic Data Generation & Automation
* Developed a Python script utilizing the `psycopg2` adapter to automate the generation and injection of 500+ synthetic SAP user records.
* Demonstrated intermediate scripting capabilities and database connectivity without relying on external network protocols (Unix sockets).

### 📸 Evidence
> *Developing a custom Python automation script using the psycopg2 adapter to generate and structure 500+ synthetic SAP user records.*
<img width="1340" height="810" alt="Captura de pantalla 2026-03-04 a la(s) 2 57 42 p m" src="https://github.com/user-attachments/assets/4f620021-8f40-4d19-a125-7841d510f965" />

> *Executing the Python script via the command-line interface to securely inject the synthetic data volume directly into the PostgreSQL engine.*
<img width="1083" height="149" alt="Captura de pantalla 2026-03-04 a la(s) 3 32 56 p m" src="https://github.com/user-attachments/assets/bfb78840-d0b7-45a5-9fff-824e7d17bbc2" />

---

### 5. Disaster Recovery & Logical Backups
* Simulated a critical data loss incident by dropping the production database.
* Executed logical backups using `pg_dump` and successfully performed a full system restoration, guaranteeing data persistence and SLA compliance.

### 📸 Evidence
> *Performing a full logical backup of the populated database utilizing native PostgreSQL tools (pg_dump) to ensure data preservation.*
<img width="1338" height="199" alt="Captura de pantalla 2026-03-04 a la(s) 3 10 40 p m" src="https://github.com/user-attachments/assets/95dd027d-8aff-40eb-a3a9-8f51d445e1ed" />


> *Intentionally dropping the primary database to simulate a critical system failure and validate our disaster recovery protocols.*
<img width="1342" height="202" alt="Captura de pantalla 2026-03-04 a la(s) 3 13 41 p m" src="https://github.com/user-attachments/assets/2e7d8873-5985-4ac3-9e2c-153582283a91" />

> *Demonstrating the successful restoration of 500+ records after a simulated database crash.*
<img width="1341" height="610" alt="Captura de pantalla 2026-03-04 a la(s) 3 18 37 p m" src="https://github.com/user-attachments/assets/4de68302-ada5-46f9-b05a-046d1667d749" />

---
### 6. Automated System Health Monitoring (Bash & Cron)
* Developed a custom Bash script (`health_check.sh`) to proactively monitor critical server resources, including available RAM, root disk capacity, and PostgreSQL daemon status.
* Configured automated background execution and log generation by scheduling a `cronjob` to run the health check every 5 minutes, ensuring continuous system observability.

---
### 📸 Phase 3 Evidence

> *Developing a custom Bash script via CLI to query system resources and database health status, outputting the results to an audit log.*
<img width="1275" height="830" alt="Captura de pantalla 2026-03-08 a la(s) 8 42 04 p m" src="https://github.com/user-attachments/assets/8abdc09d-ffeb-4681-8006-74aa4536a412" />


> *Validating the script execution and reviewing the generated audit log containing timestamped resource metrics.*
<img width="569" height="189" alt="Captura de pantalla 2026-03-08 a la(s) 8 43 59 p m" src="https://github.com/user-attachments/assets/6f06f943-4452-4e52-ae84-2e9eecd31a42" />


> *Scheduling the monitoring script as a background task using crontab for continuous, unattended execution every 5 minutes.*
<img width="542" height="446" alt="Captura de pantalla 2026-03-08 a la(s) 8 53 26 p m" src="https://github.com/user-attachments/assets/cb55cd50-e5df-4509-bb69-e906f80e9107" />



---
*Created as a practical portfolio project - March 2026*
