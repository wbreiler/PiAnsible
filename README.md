# PiAnsible

An Ansible project for managing Raspberry Pi devices, specifically focused on Docker installation and configuration.

## Overview

This project provides an automated way to set up and configure Docker on Raspberry Pi devices using Ansible. It includes a playbook that installs Docker and Docker Compose, making it easy to deploy containerized applications on your Raspberry Pi.

## Prerequisites

- Ansible installed on your control machine
- SSH access to your Raspberry Pi
- Python 3 installed on the Raspberry Pi

## Configuration

1. Copy `hosts.example` to `hosts`:

   ```bash
   cp hosts.example hosts
   ```

2. Edit the `hosts` file to match your Raspberry Pi's configuration:
   - Update the hostname if different from `raspberrypi`
   - Update the IP address or hostname if not using `.local` domain
   - Update the username if different from `pi`

## Usage

Run the playbook to install Docker and Docker Compose:

```bash
ansible-playbook -i hosts playbook.yml
```

This will:

- Install Docker on your Raspberry Pi
- Install Docker Compose
- Add the specified user to the Docker group

## Project Structure

- `playbook.yml` - Main Ansible playbook for Docker installation
- `hosts` - Inventory file for your Raspberry Pi (not tracked in git)
- `hosts.example` - Example inventory file
- `docker-compose.yml` - For defining multi-container Docker applications

## Security Notes

- The playbook requires sudo privileges on the target machine
- Make sure to use secure SSH keys for authentication
- Keep your `hosts` file secure as it contains connection information

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
