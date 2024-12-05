
#### What is Ansible?
 Ansible is an open-source IT automation tool used for configuration management, application deployment, and task automation.

#### What is the use of Ansible? 
Ansible is used for automating repetitive tasks, managing configurations, deploying applications, and orchestrating complex workflows.

#### What are the features of Ansible?
- Agentless architecture
- Easy to learn and use with YAML
- Idempotent operations
- Extensible with modules and plugins
- Strong security with SSH

#### What are the advantages of Ansible?
Simple setup and use
No need for agents
Reduces manual repetitive tasks
Consistent configurations across systems
Scalable and efficient

#### What is Ansible Galaxy?
 Ansible Galaxy is a repository for Ansible roles where users can share and reuse roles created by the community.

#### What is CI/CD? 
Continuous Integration (CI) and Continuous Deployment (CD) are practices that automate the integration and deployment of code changes to improve software quality and delivery speed.

#### What is configuration management? 
Configuration management involves maintaining consistency of a system's performance, functional, and physical attributes with its design, operational information, and requirements.

#### What are Ansible server requirements? 
Ansible requires Python 2.7 or 3.5+ on the control node and managed nodes. It also requires an SSH connection to the managed nodes.

#### What are Ansible tasks? 
Tasks are single units of work that Ansible executes on the managed nodes, defined within a playbook.

#### Explain a few of the basic terminologies or concepts in Ansible
**Playbook:** A YAML file containing tasks.
**Inventory:** A file listing managed nodes.
**Modules:** Units of code that perform specific tasks.
**Roles:** Reusable collections of tasks and configurations.
**Handlers:** Special tasks triggered by other tasks.

#### What is a playbook? 
- A playbook is a YAML file containing a series of tasks and configurations to be executed on managed nodes.

#### What are Ad hoc commands? Give an example
 Ad hoc commands are one-liner Ansible commands used for quick, simple tasks. Example: ansible all -m ping.

#### Compare Ansible with Chef
Ansible: Agentless, uses YAML for configuration, simpler setup.
Chef: Agent-based, uses Ruby, more complex setup, but more mature.

#### What is a YAML file and how do we use it in Ansible?
 YAML (Yet Another Markup Language) is a human-readable data serialization format. Ansible uses YAML for writing playbooks and configuration files.
Code difference between JSON and YAML:
      #JSON
      ```
             {
               "name": "John",
                "age": 30,
                "city": "New York"
             }

                         # YAML
            name: John
            age: 30
            city: New York
            ```
#### How is Ansible different from Puppet?
Ansible: Agentless, uses YAML, push configuration.
Puppet: Agent-based, uses its own language, pull configuration.


#### What is Ansible-doc? 
Ansible-doc displays documentation on Ansible modules and plugins.

#### What is the code you need to write for accessing a variable name? 
{{ variable_name }}

#### What is the method to check the inventory vars defined for the host?
 Use the command: ansible -m debug -a "var=hostvars['hostname']" localhost
 
#### Explain Ansible facts
 Facts are system properties gathered by Ansible from managed nodes during a playbook run.
Discuss the method to create an empty file with Ansible
 Use the file module with state=touch.
 ```
- name: Create an empty file
  file:
    path: /path/to/file
    state: touch
```
#### Explain Ansible modules in detail 
Modules are reusable, standalone scripts that Ansible runs on your behalf. They perform specific tasks like managing files, installing packages, or managing services.

#### What are callback plug-ins in Ansible?
 Callback plugins enable adding new behaviors or extending Ansible’s output processing.
 
#### What is Ansible inventory and its types?
 Inventory is a file that lists the managed nodes. Types include static and dynamic inventories.
 
#### What is an Ansible vault?
Ansible Vault allows encrypting sensitive data within Ansible files

 #### How do we write an Ansible handler with multiple tasks?
 Handlers can only perform a single task, but you can chain multiple handlers together.
```
handlers:
  - name: handler1
    command: echo "Handler 1"
  - name: handler2
    command: echo "Handler 2"
```
#### How to generate encrypted passwords for a user module? 
Use the mkpasswd command from the whois package.


#### Explain the concept of blocks under Ansible

Blocks group tasks and can handle errors, rescue, and always operations.
```
- block:
    - name: Example task
      debug:
        msg: "This is a task within a block"
  rescue:
    - name: Rescue task
      debug:
        msg: "This task runs on error"
  always:
    - name: Always task
      debug:
        msg: "This task always runs"
```
#### Do you have any idea of how to turn off the facts in Ansible? 
Set gather_facts: no in the playbook.

#### What are the registered variables under Ansible? 
Registered variables store the output of tasks for later use.

#### By default, the Ansible reboot module waits for how many seconds. Is there any way to increase it? 
By default, it waits for 600 seconds. You can increase it using the reboot_timeout parameter.

#### Can docker modules be implemented in Ansible? If so, how can you use it?
 Yes, Ansible can manage Docker containers using community.docker modules.
```
- name: Start a Docker container
  community.docker.docker_container:
    name: my_container
    image: my_image
```
#### How do you test Ansible projects? 
Use tools like Molecule and Testinfra for testing Ansible roles and playbooks.


#### How many agents you can use in ansible / With how many agents you work in ansible
  - Ansible is agentless. (Agentless: No agents required on managed nodes, only SSH and Python.)
  - 
#### Explain Ansible Architecture


- Ansible's architecture is designed to be simple and agentless, making it easy to deploy and manage. Here's an overview of its key components and how they interact:
-Key Components
- **Control Node:**
The machine where Ansible is installed and from which you run your automation scripts (playbooks).
Requires only SSH access to the managed nodes and Python installed on them.
- **Managed Nodes:**
The target machines that Ansible manages.
No need for Ansible to be installed on these nodes; only SSH and Python are required.
- **Inventory:**
A file or script that lists the managed nodes (hosts).
Can be static (a simple list of IPs or hostnames) or dynamic (generated by a script that queries an external source).
- **Modules:**
Units of work that Ansible executes on managed nodes.
Examples include yum, apt, copy, file, and service.
Can be written in any language that returns JSON, but Python is the most common.
- **Plugins:**
Extend Ansible's core functionality.
Types include action plugins, callback plugins, connection plugins, and more.
- **Playbooks:**
YAML files that define a series of tasks to be executed on managed nodes.
Each playbook consists of one or more plays, which map hosts to roles.
- **Roles:**
A way to group tasks, handlers, files, templates, and variables.
Used to organize complex playbooks.
- **Handlers:**
Tasks that are triggered by the notify directive in other tasks.
Typically used to restart services.
- **Facts:**
Information about the managed nodes collected by Ansible.
Can be accessed in playbooks and templates.
- **Vars:**
Variables that can be defined in playbooks, roles, or inventory.
Used to customize tasks and templates.
Workflow
- **Initialization:**
The control node reads the inventory file and playbooks.
The control node connects to managed nodes over SSH.
- **Execution:**
The control node sends modules to the managed nodes.
The modules are executed on the managed nodes.
Results are sent back to the control node.
- **Configuration Management:**
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
```
ansible-playbook -i /path/to/inventory playbook.yml
```
Environment Variable:
```
export ANSIBLE_INVENTORY=/path/to/inventory
```
ansible-playbook playbook.yml
Configuration File (ansible.cfg):
Create or modify ansible.cfg:
```
[defaults]
inventory = /path/to/inventory
```
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
- Answer: You can run a playbook on a specific inventory by specifying the inventory file in the command, e.g., ansible-playbook -i <inventory-file> playbook.yml.

.


#### 2. What are Ansible roles, and how do you use them?
Answer: Ansible roles are a way to organize Ansible playbooks into reusable components. Each role is structured to contain tasks, handlers, variables, files, templates, and other elements required to perform a particular function. Roles can be reused across different playbooks.
- Scenario: In my work, I create Ansible roles to manage the configuration of servers, such as installing and configuring Apache. This approach allows me to reuse the role in multiple environments, ensuring consistency and reducing duplication.





#### What are Ansible roles, and how do you use them?
Ansible roles are a way to organize playbooks into reusable components. Each role contains tasks, variables, files, templates, and handlers specific to a particular service or function. Roles can be used to break down complex playbooks into smaller, more manageable parts, promoting reuse and easier maintenance. They are defined in a specific directory structure and can be imported and applied to hosts in your playbooks.

#### 3. Ansible Config File
Answer: The main configuration file for Ansible is ansible.cfg. This file can define settings such as the inventory file location, SSH options, and other Ansible behaviors. You can place it in the current directory, your home directory, or /etc/ansible/ansible.cfg.

#### 41. What is group_vars in Ansible?
In Ansible, group_vars is a directory that contains YAML files defining variables for groups of hosts. These variables apply to all hosts in a specified group. The group_vars directory is located in the Ansible playbook directory and allows you to organize and manage variables more effectively.
For example, if you have a group called webservers, you can create a file named group_vars/webservers.yml with variables specific to that group:
```
# group_vars/webservers.yml
nginx_version: 1.18.0
document_root: /var/www/html
```
These variables will be available to all hosts that belong to the webservers group.

#### In Ansible, where are the hosts stored?
Hosts are typically stored in an inventory file, usually located in /etc/ansible/hosts or specified by the -i option in command-line operations.

#### What is the home path of Ansible?
The home path for Ansible configuration files is usually /etc/ansible on Linux systems. User-specific configuration files can be found in ~/.ansible or ~/.ansible.cfg.

#### Can you provide Ansible YAML scripts for deploying services on JBoss and Tomcat?
Example for JBoss:
```
- name: Deploy JBoss Application
  hosts: jboss_servers
  tasks:
    - name: Copy JBoss configuration
      copy:
        src: /local/path/to/jboss-config
        dest: /remote/path/to/jboss-config
    - name: Start JBoss service
      service:
        name: jboss
        state: started
```

Example for Tomcat:
```
- name: Deploy Tomcat Application
  hosts: tomcat_servers
  tasks:
    - name: Copy Tomcat WAR file
      copy:
        src: /local/path/to/app.war
        dest: /opt/tomcat/webapps/app.war
    - name: Start Tomcat service
      service:
        name: tomcat
        state: started
```

#### Can you write a sample code in Ansible? Suppose there is one master Ansible server and 50-60 slave servers. You want to install a command. Take your own command.
Example Ansible Playbook:
```
- name: Install a command on all servers
  hosts: all
  become: yes
  tasks:
    - name: Install curl
      apt:
        name: curl
        state: present
```

Explanation: This playbook installs curl on all hosts specified in the inventory file. The become: yes directive escalates privileges to root to perform the installation.




#### How do you install Nginx in the Ansible playbook?
To install Nginx in an Ansible playbook:
```
- name: Install Nginx
  hosts: webservers
  become: yes
  tasks:
    - name: Install Nginx package
      apt:
        name: nginx
        state: present
```
#### What are Register targets in Ansible?
In Ansible, register is used to capture the output of a task and store it in a variable. This registered variable can be used in subsequent tasks for conditional execution or debugging.

#### How do you use Ansible?
Answer: I use Ansible to automate configuration management, application deployment, and task automation. Ansible uses playbooks written in YAML to define the desired state of the system and execute tasks across multiple machines. It's agentless and relies on SSH for communication, making it straightforward to implement and use.

#### You have written Ansible playbooks, can you explain?
Answer: Yes, I have written Ansible playbooks to automate various tasks. Playbooks are YAML files that define a series of tasks to be executed on remote servers. Each playbook contains one or more plays, which map a set of tasks to a group of hosts. For example, I’ve used playbooks to install and configure software, deploy applications, and manage system settings.

#### Can you tell me the use cases for Ansible playbooks? And what have you done?
Answer: Ansible playbooks are used for automating tasks such as software installation, configuration management, and system updates. For example, I've used Ansible playbooks to deploy web applications, configure server settings, and ensure consistency across multiple servers. Playbooks can also be used to manage user accounts, deploy databases, and orchestrate complex multi-step processes.




#### 56. Ansible Roles
Ansible roles are a way to organize playbooks and associated files into reusable units. Roles typically contain tasks, handlers, variables, files, templates, and modules. They allow for easy sharing and reuse of Ansible code.

#### 57. Ansible Tower and its advantages
- Ansible Tower is a web-based interface for managing Ansible automation. Advantages include:
- **Visual Dashboard:** Provides a visual interface to manage playbooks, inventory, and jobs.
- **Role-based Access Control:** Manage user access based on roles.
- **Job Scheduling:** Schedule automation tasks and monitor job progress.
- **Inventory Management:** Easily manage dynamic and static inventory.



#### 37. Ansible playbook to copy files from server A to server B
```
- hosts: server_a
  tasks:
    - name: Copy file to server B
      copy:
        src: /path/to/source/file
        dest: /path/to/destination/on/server_b

```




####  8. Check whether the file is present or not; if yes, change port number from 80 to 8080 using Ansible Playbook.
```
- hosts: localhost
  tasks:
    - name: Check if file exists
      stat:
        path: /etc/nginx/nginx.conf
      register: file_check


    - name: Change port from 80 to 8080
      lineinfile:
        path: /etc/nginx/nginx.conf
        regexp: 'listen 80;'
        line: 'listen 8080;'
      when: file_check.stat.exists
```




8.How can you distribute tasks on Ansible?
9. Extra module in Ansible 
10. Callback plugin in Ansible
11. Custom module and core module
