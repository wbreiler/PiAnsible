# PiAnsible

**PiAnsible** is a collection of Ansible playbooks designed to automate the setup and configuration of various services on a Raspberry Pi running Raspberry Pi OS Lite (64-bit). These playbooks simplify the installation and management of essential packages, Docker, Docker Compose, and containers such as Apache2.

## Features

- **System Update and Upgrade**: Automatically updates and upgrades the Raspberry Pi OS.
- **Docker & Docker Compose Installation**: Installs Docker and Docker Compose, allowing for containerized applications.
- **Apache2 Docker Container Setup**: Deploys an Apache2 server in a Docker container, serving a default HTML page.
- **Modular Task Structure**: Each task is separated into different YAML files for better organization and maintainability.

## Prerequisites

- A Raspberry Pi running Raspberry Pi OS Lite (64-bit).
- Ansible installed on your local machine or control node.
- SSH access to the Raspberry Pi.

## Directory Structure
```
PiAnsible/
├── tasks/
│   ├── update-upgrade.yml
│   ├── docker-compose-install.yml
│   ├── apache-docker-install.yml
├── playbook.yml
└── README.md
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/PiAnsible.git
cd PiAnsible
```

### 2. Update the Inventory File

Ensure your inventory file (not included in the repo) lists the IP addresses or hostnames of the Raspberry Pi(s) you want to configure.

Example inventory file:

```
[all]
pi1.local ansible_user=pi
```

### 3. Run the Playbook
To update and upgrade your system, install Docker and Docker Compose, and set up the Apache2 Docker container, run the following command:
```
ansible-playbook playbook.yml
```

## Customization
	•	Modify the task files in the tasks/ directory to customize the installation and configuration steps.
	•	The Apache2 default HTML file can be edited in the tasks/apache-docker-install.yml file.

## Contibuting
Feel free to submit issues or pull requests to contribute to this project.


## License
This project is licensed under the GNU General Public License v3.0 (GPL-3.0).

### What This Means

The GPL-3.0 is a free software license that guarantees end users the freedom to run, study, share, and modify the software. The key aspects of GPL-3.0 include:

	•	Freedom to Use: You can use the software for any purpose.
	•	Freedom to Study and Modify: You can study how the program works and change it to make it do what you wish. Access to the source code is a precondition for this.
	•	Freedom to Distribute Copies: You can redistribute copies of the original program so you can help others.
	•	Freedom to Distribute Modified Versions: You can distribute copies of your modified versions to others. By doing this you can give the whole community a chance to benefit from your changes. Access to the source code is a precondition for this.

If you distribute copies or modified versions of the software, you must pass on the same freedoms to others. That means you must distribute the source code and keep the GPL license intact.
