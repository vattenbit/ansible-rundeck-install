# ansible-rundeck-docker

This repository contains an Ansible playbook for installing and configuring Rundeck on a target machine. It automates the setup process, including required dependencies, package installation, basic configuration, and service management. Ideal for quick deployments in testing or production environments.

## Usage

To run the playbook and deploy Rundeck, use the following command:

```bash
ansible-playbook -i hosts main.yaml -e "email=your-email@example.com domain=rundeck.domain.com"

