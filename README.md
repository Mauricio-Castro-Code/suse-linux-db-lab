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
> *Escribimos nuestro script*
<img width="1340" height="810" alt="Captura de pantalla 2026-03-04 a la(s) 2 57 42 p m" src="https://github.com/user-attachments/assets/4f620021-8f40-4d19-a125-7841d510f965" />

> *Ejecturamos nuestro script*
<img width="1083" height="149" alt="Captura de pantalla 2026-03-04 a la(s) 3 32 56 p m" src="https://github.com/user-attachments/assets/bfb78840-d0b7-45a5-9fff-824e7d17bbc2" />

---

### 5. Disaster Recovery & Logical Backups
* Simulated a critical data loss incident by dropping the production database.
* Executed logical backups using `pg_dump` and successfully performed a full system restoration, guaranteeing data persistence and SLA compliance.

### 📸 Evidence
> *Hacemos un Backup de nuestra DB*
<img width="1338" height="199" alt="Captura de pantalla 2026-03-04 a la(s) 3 10 40 p m" src="https://github.com/user-attachments/assets/95dd027d-8aff-40eb-a3a9-8f51d445e1ed" />


> *Borramos la Base de Datos*
<img width="1342" height="202" alt="Captura de pantalla 2026-03-04 a la(s) 3 13 41 p m" src="https://github.com/user-attachments/assets/2e7d8873-5985-4ac3-9e2c-153582283a91" />

> *Demonstrating the successful restoration of 500+ records after a simulated database crash.*
<img width="1341" height="610" alt="Captura de pantalla 2026-03-04 a la(s) 3 18 37 p m" src="https://github.com/user-attachments/assets/4de68302-ada5-46f9-b05a-046d1667d749" />


---
*Created as a practical portfolio project - March 2026*
