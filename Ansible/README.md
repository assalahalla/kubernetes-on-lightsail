# kubernetes-on-lightsail

## Project Overview:

My project revolves around creating a Kubernetes cluster consisting of four nodes on AWS Lightsail. I chose Lightsail due to its simplicity and cost-effectiveness, making it an ideal platform for my personal project. By setting up a Kubernetes cluster, I can gain hands-on experience with managing containerized applications and exploring various Kubernetes features.

## Repository Structure

The repository follows a typical Ansible project structure, organized as follows:
- roles
    - tasks
        - main.yml
    - vars
        - main.yml
    - templates
        - template.j2
- hosts
- playbook.yml

- `roles`: This directory contains the Ansible roles used in the project. Roles provide a modular and reusable way to organize tasks, variables, and templates.
- `roles/tasks/main.yml`: This file contains the main tasks for the roles defined in the project. Tasks define the individual steps or actions that Ansible performs during server configuration.
- `roles/vars/main.yml`: This file contains the variables specific to the roles defined in the project. Variables allow for customization and flexibility in configuring the servers.
- `roles/templates/template.j2`: This file is a Jinja2 template used by the Ansible roles. Templates enable the generation of dynamic configuration files or scripts.
- `hosts`: This file specifies the inventory of hosts that the Ansible playbook will target. It lists the IP addresses or hostnames of the machines to be configured or managed.
- `playbook.yml`: This is the main Ansible playbook file. It defines the sequence of roles, tasks, and other operations that Ansible will execute on the target hosts.

## Getting Started

To use this project for your own server configuration automation, follow these steps:

1. Clone this repository to your local machine.
2. Customize the roles, tasks, variables, and templates to match your specific server configuration requirements.
3. Update the `hosts` file with the IP addresses or hostnames of your target servers.
4. Run the `playbook.yml` playbook using Ansible to apply the desired configuration to your servers.

Please note that this project is tailored to my personal needs and preferences. You may need to modify or extend it to suit your own requirements.

Here are some of the roles included in the server configuration automation project:

## Ansible Roles:

To simplify the configuration process and ensure reusability, I structured my Ansible project using roles. Roles allow me to organize tasks, variables, and templates into logical units, making it easier to manage and maintain the project.

**1. Docker Role:**
The Docker role handles the installation and configuration of Docker on each node. It ensures that Docker is properly installed and ready to run containerized applications.

**2. Kubernetes Role:**
The Kubernetes role focuses on installing and configuring Kubernetes components, such as kubectl, kubelet, and kubeadm. While it could include the controller configuration step and joining the worker nodes, I have chosen to keep this part manual for now. 

**3. AWS CLI Role:** 
The AWS CLI role installs and configures the AWS Command Line Interface on the nodes. This allows me to interact with AWS services and perform tasks such as managing Lightsail instances or accessing other AWS resources.

**4. Ansible Playbook:**
The playbook.yml file serves as the entry point for my Ansible project. It orchestrates the execution of different roles and defines the target hosts where the configurations will be applied. By running the playbook, I can automate the entire setup process, eliminating the need for manual configuration on each node.

