#### How many agents you can use in ansible / With how many agents you work in ansible
  - Ansible is agentless. (Agentless: No agents required on managed nodes, only SSH and Python.)
  - 
#### Explain Ansible Architecture


- Ansible's architecture is designed to be simple and agentless, making it easy to deploy and manage. Here's an overview of its key components and how they interact:
-Key Components
- Control Node:
The machine where Ansible is installed and from which you run your automation scripts (playbooks).
Requires only SSH access to the managed nodes and Python installed on them.
- Managed Nodes:
The target machines that Ansible manages.
No need for Ansible to be installed on these nodes; only SSH and Python are required.
- Inventory:
A file or script that lists the managed nodes (hosts).
Can be static (a simple list of IPs or hostnames) or dynamic (generated by a script that queries an external source).
- Modules:
Units of work that Ansible executes on managed nodes.
Examples include yum, apt, copy, file, and service.
Can be written in any language that returns JSON, but Python is the most common.
- Plugins:
Extend Ansible's core functionality.
Types include action plugins, callback plugins, connection plugins, and more.
- Playbooks:
YAML files that define a series of tasks to be executed on managed nodes.
Each playbook consists of one or more plays, which map hosts to roles.
- Roles:
A way to group tasks, handlers, files, templates, and variables.
Used to organize complex playbooks.
- Handlers:
Tasks that are triggered by the notify directive in other tasks.
Typically used to restart services.
- Facts:
Information about the managed nodes collected by Ansible.
Can be accessed in playbooks and templates.
- Vars:
Variables that can be defined in playbooks, roles, or inventory.
Used to customize tasks and templates.
Workflow
- Initialization:
The control node reads the inventory file and playbooks.
The control node connects to managed nodes over SSH.
- Execution:
The control node sends modules to the managed nodes.
The modules are executed on the managed nodes.
Results are sent back to the control node.
- Configuration Management:
Playbooks orchestrate the execution of tasks in a defined order.
Tasks can include installing packages, copying files, configuring services, and more.

#### 3. Interview important playbooks
###### Multi-OS Ansible Playbook

```yaml
- hosts: all
  become: yes
  tasks:
    - name: Install Apache on Ubuntu
      apt:
        name: apache2
        state: present
      when: ansible_os_family == "Debian"
      ignore_errors: True

    - name: Install httpd on RedHat
      yum:
        name: httpd
        state: present
      when: ansible_os_family == "RedHat"
      ignore_errors: True
```

###### Handler playbook
```
---
 - name: Handlers Example
   hosts: webservers
   gather_facts: false
   tasks:
     - name: Install httpd latest version
       yum:
         name: httpd
         state: latest
       become: true
       notify: restart_httpd

   handlers:
     - name: restart_httpd
       become: true
       service:
         name: httpd
         state: started
```
#### 4. What is the default Inventory path ? How can you change the path of the Inventory
The default inventory file is typically located at /etc/ansible/hosts. This file contains information about the hosts (servers) that Ansible will manage.
Changing the Inventory Path
Command Line Option:
ansible-playbook -i /path/to/inventory playbook.yml
Environment Variable:
export ANSIBLE_INVENTORY=/path/to/inventory
ansible-playbook playbook.yml
Configuration File (ansible.cfg):
Create or modify ansible.cfg:

[defaults]
inventory = /path/to/inventory

#### 5. What is Role ? Explain some Roles
Role : A role is a way to organize related tasks, variables, files, templates, and other resources in a structured manner. Roles provide a reusable and modular approach to managing configuration and deployment tasks
defaults: Contains default variables for roles. Variables defined here have the lowest precedence, meaning they can be easily overridden by other variable definitions.
files: Stores static files that can be deployed to remote hosts. These files can be copied as-is using the copy module or referenced in tasks.
handlers: Contains tasks that are triggered by other tasks using the notify directive. Handlers typically perform actions like restarting services and are executed at the end of a playbook run.
meta: Holds metadata for roles, including dependencies on other roles, author information, and role version. The main file here is usually main.yml.
tasks: Contains the main list of tasks to be executed by the role. The main entry file is main.yml, and additional task files can be included using include or import directives.
templates: Contains Jinja2 templates that can be rendered and deployed to remote hosts. Templates are processed and variables are replaced with their values during deployment.
tests: Used for testing roles. This folder can include sample playbooks, inventory files, or other test-related files to ensure the role functions correctly.
vars: Stores variable files that define higher precedence variables for roles. These variables can override those defined in the defaults directory.

#### 6. What are modules ? Explain some modules
Modules are the units of work that perform tasks on the remote hosts. They are the building blocks of Ansible's functionality, allowing you to manage system resources, configurations, applications, and services. Modules can be written in any language that can return JSON, but Python is the most common.
ping: Tests the connection between Ansible and the target host. It's often used to verify that the host is reachable and ready for further tasks.
file: Manages file and directory properties, such as permissions, ownership, and the presence or absence of a file or directory.
apt: Manages packages with the apt package manager, used primarily on Debian-based systems like Ubuntu.
yum: Manages packages with the yum package manager, used primarily on Red Hat-based systems like CentOS and Fedora.
copy: Copies files from the local machine to remote hosts.
template: Processes files using Jinja2 templates and copies the resulting files to remote hosts.
user: Manages user accounts on remote hosts.
package: An abstract module that works with various package managers (like apt, yum, etc.) to install, update, or remove packages.
service: Manages services on remote hosts, allowing you to start, stop, restart, and enable/disable services.
firewalld: Configures the firewalld firewall on remote hosts.
archive: Creates archive files (like tar or zip) from files on remote hosts.
unarchive: Extracts archive files (like tar or zip) on remote hosts.
shell: Executes shell commands on remote hosts.
command: Executes commands on remote hosts but does not process through the shell. It's safer than the shell module for executing system commands.
debug: Prints statements during playbook execution for debugging purposes.
lineinfile: Ensures a particular line is present (or absent) in a file.
fetch: Fetches files from remote hosts and saves them to the local machine.

#### 7. How  can you take backup of Ansible master
Taking backup of server
Taking backup of ansible home directory by archiving the directory
All playbooks are in remote repo(github) so they will automatically backup the playbook.


#### 1. Introduction
 - I'm a DevOps Engineer with 2-3 years of experience in managing and automating deployment pipelines, infrastructure provisioning, and monitoring. I have expertise in tools like Jenkins, Ansible, Terraform, Docker, and Kubernetes, as well as experience with cloud services like AWS and Azure. My background includes developing CI/CD pipelines, automating infrastructure tasks, and ensuring high availability and scalability of applications.
#### 2. What is Ansible?
Ansible is an open-source automation tool used for configuration management, application deployment, and task automation. It allows you to manage systems and applications efficiently and is designed to be simple, powerful, and agentless.
#### 3. Ansible Architecture
- Ansible's architecture consists of the following components:
Control Node: The machine where Ansible is installed and from which commands are executed.
Managed Nodes: The machines managed by Ansible, also known as hosts. Ansible connects to these nodes using SSH.
Inventory: A file listing the managed nodes. It can be static or dynamic.
Modules: Reusable, standalone scripts used by Ansible to perform tasks.
Plugins: Extend Ansible's core functionality. Examples include connection plugins, callback plugins, and inventory plugins.
Playbooks: YAML files containing a series of tasks to be executed on managed nodes.
Roles: Organizational units of Ansible playbooks, including tasks, handlers, variables, and templates.
#### 4. Ansible Module
Ansible modules are discrete units of code that can be used from the command line or in a playbook task. They perform specific functions, such as installing packages, copying files, or managing services. Examples include yum, apt, copy, service, and user.
#### 5. Use of Handlers
Handlers are used in Ansible to perform actions in response to events. They are similar to regular tasks but are only run when notified by other tasks. Handlers are commonly used to restart services after configuration changes.
#### 6. What is the use of Ansible template?
Ansible templates are used to create configuration files dynamically. They use the Jinja2 templating engine to allow the insertion of variables and conditional logic. Templates are helpful for generating configuration files that need to be customized for different environments or systems.
#### 7. Write a playbook to copy a file from one server to another server
```
---
- name: Copy a file from one server to another
  hosts: source_server
  tasks:
    - name: Copy file to destination server
      copy:
        src: /path/to/source/file
        dest: /path/to/destination/file
      delegate_to: destination_server
```
#### 8. Ansible Galaxy and Collection
Ansible Galaxy: Ansible Galaxy is a repository for Ansible roles and collections. It allows users to share and download pre-built roles and collections to speed up their automation projects.
Collections: Collections are a way to package and distribute Ansible content, including roles, modules, plugins, and documentation. They help organize and distribute Ansible content more effectively.
#### 9. Advantages of Ansible Tower
Centralized management: Manage all Ansible playbooks and inventories in a centralized interface.
Role-based access control (RBAC): Control access to resources based on user roles.
Workflow automation: Create complex workflows to orchestrate different playbooks and tasks.
Real-time job monitoring: Monitor job status and view detailed job logs in real-time.
Notification: Integrate with email, Slack, and other notification systems.
#### 10. Job Schedule in Ansible Tower
Ansible Tower allows you to schedule jobs to run at specific times or intervals. This can be done through the Tower interface by setting up job templates with defined schedules.
#### 11. Key Benefits of Ansible Tower
Scalability: Manage thousands of nodes easily.
Security: Control access with RBAC and encrypt sensitive data.
Compliance: Ensure consistent application of policies and configurations.
Efficiency: Automate repetitive tasks and reduce manual intervention.
Visibility: Gain insights into job status and logs for troubleshooting.
#### 12. Role-Based Access Control (RBAC)
RBAC in Ansible Tower allows you to define roles and permissions for users and teams. This ensures that users have access only to the resources and actions they are authorized for, enhancing security and compliance.
#### 13. What you automate using Python
Using Python, I automate tasks such as:
Data processing and analysis
System monitoring and alerting
API interactions and data retrieval
Infrastructure provisioning and management
Deployment and configuration of applications
#### 14. For which project did you use Ansible Tower and what was the purpose of choosing Ansible
I used Ansible Tower in a project that involved managing a large number of servers across multiple environments. The purpose of choosing Ansible Tower was to streamline the deployment process, ensure consistency, and provide centralized management with role-based access control.
#### 15. Can we use Ansible as an IaC tool?
Yes, Ansible can be used as an Infrastructure as Code (IaC) tool to provision and manage infrastructure resources. It is commonly used to configure servers, deploy applications, and manage cloud resources.
#### 16. Can we run multiple tasks in parallel using Ansible?
Yes, Ansible can run multiple tasks in parallel using the async and poll keywords or by using strategies such as free.
#### 17. Ansible Vault
Ansible Vault is a feature that allows you to encrypt sensitive data such as passwords, API keys, and other secrets within your Ansible playbooks and roles. This ensures that sensitive information is not exposed in plaintext.
Example usage:
ansible-vault encrypt secrets.yml
ansible-vault decrypt secrets.yml
ansible-vault edit secrets.yml
Summary
Ansible is a powerful automation tool used for configuration management, application deployment, and infrastructure provisioning. It offers various features such as handlers, templates, and vaults for secure management. Ansible Tower enhances Ansible's capabilities by providing a centralized management interface, role-based access control, and job scheduling.


#### 12. Ansible ping Command: Provide Command for 1. All Playbooks, 2. Single Playbook, 3. When I Want to Run Playbook on Any Specific Inventory Without Mentioning it in the Command
Answer:
Ping All Hosts: ansible all -m ping
Ping a Specific Host: ansible <hostname> -m ping
Run Playbook on Specific Inventory: If you want to run a playbook on a specific inventory without specifying it in the command, set the inventory parameter in the ansible.cfg file or define it in the playbook itself.


#### 13. Ansible Static and Dynamic Inventory
Answer:
Static Inventory: A static inventory is a list of managed nodes defined in a file, typically called hosts or inventory, where you explicitly list the IPs or hostnames.
Dynamic Inventory: A dynamic inventory fetches information from external sources like cloud providers (AWS, Azure) or a database to get the list of managed nodes.


#### 14. Suppose I Want to Run a Playbook on Any Specific Inventory: How Should I Do It?
Answer: You can run a playbook on a specific inventory by specifying the inventory file in the command, e.g., ansible-playbook -i <inventory-file> playbook.yml.

8.How can you distribute tasks on Ansible?
9. Extra module in Ansible 
10. Callback plugin in Ansible
11. Custom module and core module.




