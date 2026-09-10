# Ansible Nginx Automation

## Project Overview

A simple Ansible project to automate the installation and configuration of Nginx on an Ubuntu Server.

The project uses a **single Ubuntu Server running in VirtualBox**, acting as both the Ansible control node and managed node.

## Architecture

```text
Ansible
   |
   v
Ubuntu Server
   |
   v
Install & Configure Nginx
   |
   v
Deploy HTML Website
   |
   v
Nginx :80
   |
   v
Browser
```

## Project Structure

```text
ansible-nginx/
├── inventory
├── nginx.yml
└── index.html.j2
```

## What This Project Does

* Installs Nginx using Ansible
* Starts and enables Nginx
* Deploys a custom HTML page
* Uses Jinja2 template
* Uses Ansible Handler to restart Nginx when required
* Verifies Nginx and HTTP response

## Technologies

* Ubuntu Server
* Ansible
* Nginx
* Jinja2
* VirtualBox

## Important Commands

### Test Ansible

```bash
ansible -i inventory webservers -m ping
```

### Check Playbook Syntax

```bash
ansible-playbook -i inventory nginx.yml --syntax-check
```

### Run Playbook

```bash
ansible-playbook -i inventory nginx.yml
```

### Verify Nginx

```bash
systemctl is-active nginx
```

### Verify Website

```bash
curl http://localhost
```

### Check Nginx Configuration

```bash
sudo nginx -t
```

## Result

Ansible successfully installs and configures Nginx and deploys the custom website automatically.

The website can be accessed from the host machine using:

```text
http://<Ubuntu-Server-IP>
```

## Skills Demonstrated

**Ansible | Linux | Nginx | Jinja2 | Automation | VirtualBox | Troubleshooting**
