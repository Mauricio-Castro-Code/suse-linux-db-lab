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
![Systemctl Status](PON_AQUI_EL_LINK_DE_TU_IMAGEN_1)

### 2. Database Creation & SQL Queries
> *Demonstrating successful connection to the DB engine, table creation, and querying synthetic SAP user data.*
![SQL Query Result](PON_AQUI_EL_LINK_DE_TU_IMAGEN_2)

---

## 🚀 Next Steps (Roadmap)
* **Phase 2:** Disaster Recovery Simulation (Implementing logical backups with `pg_dump`, simulating database corruption, and executing full restoration procedures).
* **Phase 3:** Synthetic Data Generation via Python scripting.

---
*Created as a practical portfolio project - March 2026*
