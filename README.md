# ansible-rundeck-docker

This repository contains an Ansible playbook for installing and configuring Rundeck on a target machine. It automates the setup process, including required dependencies, package installation, basic configuration, and service management. Ideal for quick deployments in testing or production environments.

## Usage

To run the playbook and deploy Rundeck, use the following command:

```bash
ansible-playbook -i hosts main.yaml -e "email=your-email@example.com domain=rundeck.domain.com"
```

### Example `hosts` file

Below is an example of how to configure the `hosts` inventory file:

```ini
[rundecks]
rundeck-server ansible_host=192.168.1.100 ansible_user=your-ssh-user ansible_password=your-ssh-password ansible_become_password=your-sudo-password
```

- **`rundeck-server`**: The hostname or IP address of the target machine where Rundeck will be deployed.
- **`ansible_host`**: The IP address of the target machine.
- **`ansible_user`**: The SSH user used to connect to the target machine.
- **`ansible_password`**: The password for the SSH user (if not using SSH keys).
- **`ansible_become_password`**: The password for `sudo` or privilege escalation.
