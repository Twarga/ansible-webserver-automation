# Ansible Project

## Description
This project utilizes Ansible for advanced Linux/Unix administration tasks, focusing on automation and Infrastructure as Code (IaC). It includes playbooks for web server configuration, security, RBAC, and load balancing using Nginx.

## File Structure
- **files:** Directory containing configuration files.
- **hosts:** Inventory file listing target hosts.
- **nginx_lb_playbook.yml:** Ansible playbook for configuring Nginx as a load balancer.
- **rbac_configuration.yml:** Ansible playbook for RBAC (Role-Based Access Control) configuration.
- **README.md:** This file - your guide to the project.
- **security_conf_playbook.yml:** Ansible playbook for comprehensive security configuration.
- **update_playbook.yml:** Ansible playbook for scheduled system updates.
- **web_server_playbook.yml:** Ansible playbook for setting up and configuring web servers.

## Instructions
1. Ensure Ansible is installed on your machine.
2. Modify the 'hosts' inventory file to include your target servers.
3. Run individual playbooks using the following commands:

   - **Web Servers Playbook:**
     ```bash
     ansible-playbook -i hosts web_server_playbook.yml --ask-become-pass
     ```

   - **Load Balancer Playbook:**
     ```bash
     ansible-playbook -i hosts nginx_lb_playbook.yml
     ```

   - **RBAC Configuration Playbook:**
     ```bash
     ansible-playbook -i hosts rbac_configuration.yml --ask-become-pass
     ```

   - **Security Configuration Playbook:**
     ```bash
     ansible-playbook -i hosts security_conf_playbook.yml --ask-become-pass
     ```

   - **Scheduled Updates Playbook:**
     ```bash
     ansible-playbook -i hosts update_playbook.yml --ask-become-pass
     ```

## Suggestions for Improvement
1. Consider using Vagrant for virtualization.
2. Create a master playbook to execute all playbooks in a specific order.
3. Utilize Ansible Vault to secure sensitive information such as SSH keys.

For more details and customization, refer to the specific playbook files and configurations in the project.
