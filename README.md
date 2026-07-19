# Ansible Blog Application Deployment

This project automates deployment of a blogging application to a remote Nginx server using Ansible.

## Project Overview
The playbook installs and configures Nginx, creates the application directory, copies application files, applies an Nginx server block template, enables the site, and ensures the service is running.

## Project Structure
- `inventory` - target server details
- `playbook.yml` - main Ansible deployment playbook
- `templates/nginx.conf.j2` - Nginx virtual host template
- `README.md` - project documentation

## Prerequisites
- Ubuntu/Debian-based remote server
- SSH access to the target server
- Ansible installed on the control node
- Sudo privileges on the target server

## Usage
1. Update the `inventory` file with your server details.
2. Place application files in a local folder if needed.
3. Run:
   ```bash
   ansible-playbook -i inventory playbook.yml -u ubuntu -K
   ```

## What the playbook does
- Installs Nginx
- Creates application directory
- Copies application files
- Deploys Nginx configuration from template
- Enables the site
- Removes default site
- Starts/restarts Nginx

## Notes
This project is intended as a basic DevOps deployment example and can be extended using roles, variables, and CI/CD integration.
