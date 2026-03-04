# SUSE Linux Database Lab

## Project Overview

This project simulates a **corporate-style Linux server environment**
for the installation and management of a relational database system. The
goal is to demonstrate practical skills in **Linux system
administration, database deployment, and infrastructure automation**
using open-source technologies.

Instead of distributing a full virtual machine, this repository provides
the **automation script and configuration steps** required to replicate
the environment on any compatible system.

This approach reflects real-world engineering practices where
infrastructure is documented and automated rather than manually
reproduced.

------------------------------------------------------------------------

## Objective

To simulate the deployment of a **database server in a SUSE Linux
environment**, including:

-   Linux system administration
-   Database installation and initialization
-   Service management using `systemctl`
-   Package management using `zypper`
-   Infrastructure automation via Bash scripting

The project mirrors how **enterprise environments provision database
servers for internal applications**.

------------------------------------------------------------------------

## Technology Stack

| Technology | Description |
|------------|-------------|
| **openSUSE Leap 16.0 (AArch64)** | Enterprise-grade Linux distribution |
| **PostgreSQL** | Open-source relational database |
| **Bash** | Shell scripting for server automation |
| **Zypper** | SUSE package manager |
| **Systemd** | Service management framework |

---


------------------------------------------------------------------------

## Architecture

    +-----------------------+
    |    Linux Server       |
    |  openSUSE Leap 16.0  |
    +----------+------------+
               |
               v
    +-----------------------+
    |     PostgreSQL DB     |
    |  Relational Database  |
    +-----------------------+

The server is provisioned through a **bash automation script** that
installs and enables the database service.

------------------------------------------------------------------------

## Automation Script

The repository includes the script:

`install_db.sh`

This script performs the following operations:

1.  Refresh system repositories
2.  Install PostgreSQL packages
3.  Enable PostgreSQL service
4.  Start the database service

This represents a **basic infrastructure automation pattern used in
DevOps workflows**.

------------------------------------------------------------------------

## Installation Script Example

``` bash
#!/bin/bash

echo "Updating repositories..."
sudo zypper refresh

echo "Installing PostgreSQL..."
sudo zypper install -y postgresql postgresql-server

echo "Enabling PostgreSQL service..."
sudo systemctl enable postgresql

echo "Starting PostgreSQL service..."
sudo systemctl start postgresql

echo "Database installation completed successfully."
```

------------------------------------------------------------------------

## How to Run

Clone the repository:

``` bash
git clone https://github.com/yourusername/suse-linux-db-lab.git
cd suse-linux-db-lab
```

Give execution permissions:

``` bash
chmod +x install_db.sh
```

Run the script:

``` bash
./install_db.sh
```

------------------------------------------------------------------------

## Screenshots

Add screenshots of your environment inside an `images` folder:

-   System environment
-   PostgreSQL installation
-   PostgreSQL service running

Example:

    images/system.png
    images/postgres_install.png
    images/postgres_running.png

------------------------------------------------------------------------

## Skills Demonstrated

-   Linux system administration
-   Database server deployment
-   Bash automation
-   Infrastructure reproducibility
-   Command-line environment management

------------------------------------------------------------------------

## Future Improvements

Possible enhancements:

-   Database user and role management
-   PostgreSQL remote access configuration
-   Backup automation scripts
-   Containerized deployment using Docker
-   Infrastructure provisioning using Ansible or Terraform

------------------------------------------------------------------------

## Author

Mauricio Castro Valencia\
Computer Science Engineering Student

GitHub\
https://github.com/Mauricio-Castro-Code

LinkedIn\
https://www.linkedin.com/in/mauricio-castro-valencia-125985200/

------------------------------------------------------------------------

## License

This project is provided for **educational and demonstration purposes**.
