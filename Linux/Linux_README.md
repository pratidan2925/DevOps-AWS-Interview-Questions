# Linux

#### What is Linux

- Linux is an open-source operating system kernel developed by Linus Torvalds in 1991. It's the core component of various Linux distributions (or distros) such as Ubuntu, Fedora, and Debian. Linux is known for its stability, security, and flexibility, making it popular for use in servers, desktop computers, mobile devices, and embedded systems. It supports a wide range of software and is highly customizable to meet different needs.
---
#### how to give permission to Linux ?  And What is chmod ?

"chmod" is a command in Linux used to change permissions for files and directories. It allows you to specify who can read, write, or execute a file or directory. You can use symbolic or octal notation to set permissions. For example, chmod u+x file.txt adds execute permission for the owner of "file.txt", while chmod 755 file.txt gives the owner full permissions and read/execute permissions to the group and others.

- Read -  4      

- write - 2     

- execute - 1
 ---
#### 777 in Linux

- In Linux, "777" is a file permission notation representing full read, write, and execute permissions for the owner, group, and others.
 ---
#### Which Linux  and Windows version do you use?

linux :

Ubuntu 18.x  -- decamped /not in use for  5/6 months.

Ubuntu 22.04  –  Recently used.

Ubuntu 24.04  -- latest version – recently used.

Windows : 

2019 -recently used .

2022- latest version

 - Note : Company never goeson latest version ,as it may have issues. So they always use one     version older than the latest version .
 ---
#### What is the key difference  between Linux server and ubuntu server?

Linux Server: "Linux server" refers to any server operating system based on the Linux kernel. It's a broad term encompassing various distributions (distros) like Ubuntu Server, CentOS, Debian, Fedora, etc. Each distribution may have its own package management system, default software, and support policies.

- Ubuntu Server: Ubuntu Server is a specific distribution of Linux tailored for server environments. It's maintained by Canonical and is based on the Debian architecture. Ubuntu Server is known for its ease of use, regular updates, strong community support, and compatibility with a wide range of software packages. It's often chosen for web servers, cloud deployments, and enterprise applications.
In essence, while "Linux server" is a generic term referring to any server running a Linux-based operating system, "Ubuntu server" specifically denotes a server running the Ubuntu distribution of Linux.
 ---
#### What is thread in Linux

- In Linux, a thread is a basic unit of execution within a process, capable of running tasks concurrently with other threads. They share the same memory and resources as their parent process, enabling efficient multitasking and parallel processing within applications.
---
#### What is a zombie process in Linux?

- In short, a zombie process in Linux is a terminated process that still has an entry in the process table because its parent process hasn't yet acknowledged its termination.
---
#### Explain Grep command.
- The grep command in Unix/Linux is used to search for specific patterns within files. It stands for "Global Regular Expression Print". grep is a powerful tool for searching through text files and displaying lines that match a given pattern.
 ---
#### What is etc  folder ?
- The /etc folder is a key part of Linux and other Unix-like systems. It's where the system keeps important settings and configuration files.
·         Stores Settings: This folder holds configuration files that control how the system and various programs behave.
·         System-Wide Impact: Changes in this folder affect the whole system, not just one user.
 ---
#### Difference Between YUM and APT
YUM (Yellowdog Updater, Modified) and APT (Advanced Package Tool) are both package management systems used in Linux distributions.
YUM  is used for Amazon Linux while APT is used for Ubuntu Linux.
 
Distribution: Primarily used in RPM-based distributions like Red Hat Enterprise Linux (RHEL), CentOS, and Fedora.
·         Package Format: Handles .rpm (Red Hat Package Manager) files.
·         Dependencies: Automatically resolves and installs package dependencies.
·         Repositories: Uses repository configurations in /etc/yum.repos.d/.
·         Commands: Common commands include yum install, yum update, yum remove, and yum search.
·         Features: Supports plugins, allows for easy repository management, and has a strong focus on backward compatibility.


APT
·         Distribution: Primarily used in Debian-based distributions like Debian, Ubuntu, and their derivatives.
·         Package Format: Handles .deb (Debian) files.
·         Dependencies: Automatically resolves and installs package dependencies.
·         Repositories: Uses repository configurations in /etc/apt/sources.list and /etc/apt/sources.list.d/.
·         Commands: Common commands include apt-get install, apt-get update, apt-get remove, and apt-cache search. apt is a newer, user-friendly command-line tool that combines the most commonly used commands.
·         Features: Offers a more user-friendly command-line interface with apt, provides extensive documentation, and emphasizes a large community and ecosystem.

---
####  How to get info for all the packages installed on Linux system
- yum list installed
- apt list –installed
---
#### How to check the kernel version in Linux
- uname -r -- This command will output the kernel version.
cat /proc/version -- This command will display the kernel version along with additional information about the build
 hostnamectl -- This command will display the kernel version along with additional information about the build
---
####  Explain Linux distribution
- A Linux distribution, often referred to as a "distro," is a complete operating system built on the Linux kernel along with a collection of software applications, libraries, and utilities.
Examples of popular Linux distributions include Ubuntu, Fedora, Debian, CentOS, Arch Linux, and openSUSE. Each distribution may target specific use cases, such as general-purpose desktops, servers, embedded systems, or specialized applications.
---
#### How to backup a Linux server?
- To back up a Linux server, there are several methods you can use, depending on the requirements and the environment. Some of the most common methods include using rsync, tar, dd, rsnapshot, Bacula, and Duplicity
 rsync: Efficient for file synchronization and backups.
tar: Creates compressed archive files.
dd: For full disk backups.
Automation with cron: Schedule regular backups.
Advanced Tools:
rsnapshot: For incremental backups.
Bacula and Duplicity: For more complex needs, including encryption and remote backups.
---

#### how to check running processes in linux /what is the use of ps-aux in linux /what is Top command & its uses.
- top Command
Displays real-time system summary and list of processes.

- Ps-aux Command
Displays information about active processes.
a: Displays processes from all users.
u: Shows detailed user-oriented format.
x: Includes processes without a controlling terminal.
---
#### How to check system load in linux
top Command
Displays real-time information about system processes, including system load.
Load average: Displayed at the top of the screen, shows system load over the last 1, 5, and 15 minutes.

---
#### What is the Inode number ?
An inode number is a unique identifier assigned to each file or directory in a Unix-based file system, like Linux. It helps the operating system keep track of file attributes and locate files efficiently. It's like a fingerprint for each file or directory.

---
#### What is Nginx?
 - Nginx is a popular web server software used to host websites and serve web content on the internet. It's like a traffic cop for the internet, directing web traffic to the right places. Nginx is known for its speed and efficiency, handling large volumes of web traffic with ease. It's commonly used as a reverse proxy, load balancer, and HTTP cache, making websites faster and more reliable. In simple terms, Nginx helps websites run smoothly and handle lots of visitors without slowing down.
---
#### What is Cron job in Linux
- A cron job is a task scheduled to run at specific times or intervals on a Unix-based system like Linux. You can use the cron utility to schedule repetitive tasks, such as running scripts, executing commands, or performing system maintenance, automatically without manual intervention.
---
#### What is the nslookup command ?
- The "nslookup" command is a network utility used in Unix-like operating systems to query DNS (Domain Name System) servers for various types of DNS records. It allows you to obtain information about domain names, IP addresses, and other DNS-related records.
---
#### How to Start a Linux server.
- nr Start-ds
 To start a Linux server, boot it up either from a virtual machine manager or by pressing the power button if it's a physical server. Then, log in using SSH or a remote desktop connection. Finally, verify that essential services are running and check the server's status.
Use commands like uptime or systemctl status to verify its status.
---
#### Explain Grep vs sed command
- Grep:
Purpose: Searches for patterns within text.
Functionality: Prints lines that match a specified pattern.
Usage Example: grep 'error' logfile.txt - Finds and displays lines containing "error" in logfile.txt.
Sed:
Purpose: Stream editor for modifying text.
Functionality: Performs find-and-replace, text transformation, and filtering.
Usage Example: sed 's/error/success/' logfile.txt - Replaces the first occurrence of "error" with "success" in each line of logfile.txt.
--- 
#### Explain Cat vs more command
- cat (concatenate):
Purpose: Displays the content of files and concatenates them.
Functionality: Outputs the entire content of a file to the terminal.
Usage Example: cat filename.txt - Displays the full content of filename.txt.

- more:
Purpose: Displays the content of files one screen at a time.
Functionality: Allows for paginated viewing of long text files, enabling scrolling through the content.
Usage Example: more filename.txt - Displays the content of filename.txt one screen at a time.
Summary:
cat is used to quickly display the full content of a file.
more is used to view the content of a file one page at a time, which is useful for long files.




---
#### How do you diagnose and fix a network connectivity issue on a Linux server?
- Diagnose:
Check Network Interfaces: Use ip a or ifconfig to check the status of network interfaces.
Ping Test: Test connectivity to local and remote hosts using ping.
Traceroute: Use traceroute to identify where connectivity issues occur in the network path.
Check Routing Table: Use ip route to verify correct routing.
Review Logs: Check system logs (/var/log/syslog or /var/log/messages) for network-related errors.
- Fix:
Correct Network Configuration: Ensure IP settings, gateway, and DNS configurations are correct in /etc/network/interfaces or similar files.
Restart Networking Service: Restart networking services with systemctl restart network or systemctl restart NetworkManager.
Update Drivers/Kernel: Ensure network drivers and kernel are up-to-date.

#### Explain the process of setting up and configuring a mail server on Linux.
Choose Mail Server Software: Common choices include Postfix, Sendmail, or Exim.
- Install Software:
Postfix: sudo apt-get install postfix
- Configure:
Edit Configuration Files: Configure /etc/postfix/main.cf for Postfix. Set parameters like myhostname, mydestination, and relayhost.
Setup Domains and Aliases: Configure virtual domains and aliases in /etc/postfix/virtual.
Start and Enable Services: Start Postfix with systemctl start postfix and enable it with systemctl enable postfix.
Test: Use telnet or mail command to test sending and receiving mail.

#### How do you implement and manage disk quotas for users on a Linux system?
Install Quota Tools: Install quota tools if not already installed (sudo apt-get install quota).
- Configure Filesystems:
Edit /etc/fstab: Add usrquota and/or grpquota to the filesystem options. Example: /dev/sda1 /home ext4 defaults,usrquota 0 2.
- Apply Quotas:
Create Quota Files: Use quotacheck -cug /home to create quota files.
Set Quotas: Use edquota -u username to set user quotas, and quotaon -v /home to enable quotas.
Monitor Quotas: Use repquota /home to review quota usage.

#### Describe the steps to compile and install software from source in Linux.
Download Source Code: Obtain the source code tarball (e.g., wget https://example.com/software.tar.gz).
Extract: Extract the tarball with tar -xzf software.tar.gz.
Navigate to Directory: Change to the extracted directory (cd software).
Configure: Run ./configure to check for dependencies and configure the build environment.
Compile: Compile the software with make.
Install: Install the compiled software with sudo make install.
Verify: Check the installation by running the software or using which to locate the binary.

#### What are the key differences between systemd and init? How do you manage services with systemd?
Differences:
Initialization: systemd is an advanced init system that uses parallelization and dependency tracking. init is an older, simpler system that processes scripts sequentially.
Service Management: systemd uses unit files and a more comprehensive service management framework, while init uses shell scripts.
Managing Services with systemd:
Start Service: systemctl start service_name
Stop Service: systemctl stop service_name
Enable Service: systemctl enable service_name
Disable Service: systemctl disable service_name
Check Status: systemctl status service_name
View Logs: journalctl -u service_name


#### How do you handle kernel module management in Linux?
List Modules: Use lsmod to list currently loaded modules.
Load Module: Use modprobe module_name to load a module.
Unload Module: Use modprobe -r module_name or rmmod module_name to remove a module.
View Module Information: Use modinfo module_name to view detailed information about a module.


#### Explain how to set up a secure FTP server in Linux.
Install vsftpd: sudo apt-get install vsftpd
Configure:
Edit Configuration File: Modify /etc/vsftpd.conf. Set parameters like anonymous_enable=NO, local_enable=YES, write_enable=YES, chroot_local_user=YES.
Enable SSL/TLS: Configure SSL/TLS settings if required (ssl_enable=YES, rsa_cert_file=/etc/ssl/certs/vsftpd.pem).
Start and Enable Service: Start with systemctl start vsftpd and enable with systemctl enable vsftpd.


#### How do you use iptables to configure firewall rules? Provide an example.
List Rules: iptables -L
Add Rule: Use iptables -A INPUT -p tcp --dport 22 -j ACCEPT to allow incoming SSH traffic.
Save Rules: Save the configuration to ensure persistence (iptables-save > /etc/iptables/rules.v4).
Example: To block all incoming traffic except for SSH and HTTP:
``` 
iptables -P INPUT DROP
iptables -A INPUT -p tcp --dport 22 -j ACCEPT
iptables -A INPUT -p tcp --dport 80 -j ACCEPT
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT

```
#### What are the steps to configure NFS (Network File System) for file sharing in Linux?
Install NFS Server: sudo apt-get install nfs-kernel-server
Configure Exports:
Edit /etc/exports: Add the directory to be shared and its permissions, e.g., /srv/nfs/share *(rw,sync,no_subtree_check).
Export Shares: Run exportfs -a to apply the changes.
Start and Enable NFS: Start with systemctl start nfs-kernel-server and enable with systemctl enable nfs-kernel-server.
Client Configuration:
Install NFS Client: sudo apt-get install nfs-common
Mount NFS Share: mount server:/srv/nfs/share /mnt
How do you automate system administration tasks in Linux using shell scripts?
Write Script: Create a shell script file with #!/bin/bash at the top and include commands for tasks you want to automate.
Make Executable: Use chmod +x script.sh to make the script executable.
Schedule: Use cron to schedule scripts. Edit the crontab file with crontab -e and add a line like 0 2 * * * /path/to/script.sh to run the script daily at 2 AM.


#### Explain the process of setting up a DNS server using BIND in Linux.
Install BIND: sudo apt-get install bind9
Configure BIND:
Edit /etc/bind/named.conf.local: Add zone definitions, e.g.,
bash
Copy code
```
zone "example.com" {
    type master;
    file "/etc/bind/db.example.com";
};
```

Create Zone Files: Create and edit zone files (e.g., /etc/bind/db.example.com) with DNS records.
Restart BIND: Apply changes with systemctl restart bind9.
Test: Use dig or nslookup to test DNS resolution.
#### How do you manage and monitor running processes in Linux? Discuss tools and commands you use.
Commands:
ps: Display information about running processes. Use ps aux for a detailed list.
top: Monitor processes in real-time with a dynamic interface.
htop: An enhanced version of top with a more user-friendly interface.
systemctl: Manage services and view their status with systemctl status service_name.
Monitoring Tools:
netstat: Monitor network connections.
vmstat: Report system performance.
Describe how to create and manage Docker containers on a Linux server.
Create Container: Use docker run to create and start a container, e.g., docker run -d --name my_container nginx.
Manage Containers:
List: docker ps shows running containers.
Stop: docker stop my_container
Remove: docker rm my_container
View Logs: docker logs my_container
Dockerfile: Define container configuration and build custom images with docker build -t my_image ..
How do you configure and use rsyslog for centralized logging in Linux?
Install rsyslog: sudo apt-get install rsyslog
Configure Server:
Edit /etc/rsyslog.conf: Enable UDP/TCP reception with lines like module(load="imudp") and input(type="imudp" port="514").
Restart rsyslog: Apply changes with systemctl restart rsyslog.
Configure Clients:
Edit /etc/rsyslog.conf: Add *.* @server_ip:514 to send logs to the server.
Verify: Use logger to test log sending and check the server logs.


#### What are your methods for securing SSH access on a Linux server?
Use Strong Passwords: Ensure strong passwords for SSH access.
Use SSH Keys: Configure key-based authentication and disable password authentication in /etc/ssh/sshd_config.
Change Default Port: Change the default SSH port from 22 to a non-standard port.
Limit Access: Use AllowUsers or AllowGroups directives in /etc/ssh/sshd_config to restrict access.
Firewall Rules: Restrict access to the SSH port using firewall rules (e.g., with iptables or ufw).
Explain how to set up and configure a proxy server in Linux.
Install Proxy Server Software: Examples include Squid (sudo apt-get install squid).
Configure:
Edit Configuration File: Configure /etc/squid/squid.conf with ACLs and rules for access control.
Example:
bash
Copy code
```
acl localnet src 192.168.1.0/24
http_access allow localnet
```

Start and Enable: Start with systemctl start squid and enable with systemctl enable squid.

#### How do you troubleshoot file permission issues in Linux?
Check Permissions: Use ls -l to view file permissions.
Change Permissions: Use chmod to modify permissions (e.g., chmod 755 file).
Check Ownership: Use chown to change file ownership (e.g., chown user:group file).
Review SELinux/AppArmor: Check for security contexts or profiles if using SELinux or AppArmor.

#### Describe the process of setting up and managing a MySQL or PostgreSQL database server in Linux.
Install MySQL/PostgreSQL:
MySQL: sudo apt-get install mysql-server
PostgreSQL: sudo apt-get install postgresql
Configure:
MySQL: Edit /etc/mysql/mysql.conf.d/mysqld.cnf for configurations.
PostgreSQL: Edit /etc/postgresql/<version>/main/postgresql.conf.
Start and Enable: Start with systemctl start mysql or systemctl start postgresql and enable with systemctl enable mysql or systemctl enable postgresql.
Manage Databases:
MySQL: Use mysql command-line tool.
PostgreSQL: Use psql command-line tool.
#### How do you perform a system audit to ensure compliance with security policies in Linux?
Use Audit Tools:
auditd: Install and configure auditd for system auditing. Configure rules in /etc/audit/audit.rules.
osquery: Use osquery to perform SQL-like queries on the system.
Review Logs: Analyze audit logs located in /var/log/audit/.
Security Scanning: Use tools like Lynis or OpenVAS for vulnerability scanning.
#### What are the steps to configure a VPN server on a Linux machine?
Install VPN Software: For example, OpenVPN (sudo apt-get install openvpn).
Configure VPN:
Edit Configuration Files: Set up server and client configuration files in /etc/openvpn/.
Start VPN Service: Start with systemctl start openvpn@server and enable with systemctl enable openvpn@server.
Configure Firewall: Ensure necessary ports are open (e.g., 1194/udp for OpenVPN).
Test: Connect using a VPN client to verify functionality.



# WINDOWS

 #### Why linux is more secure than windows explain in short.
 Linux is often seen as more secure than Windows for a few simple reasons:
**Open Source:** Since the code is open for everyone to see, many people can check and fix security problems quickly.
**User Permissions:** Linux restricts what regular users can do, making it harder for viruses to cause damage.
**Built-In Security:** It has strong security tools like SELinux and AppArmor that help protect the system.
**Variety:** There are many different versions of Linux, so a virus for one version might not work on another.
**Less Targeted:** Fewer people use Linux compared to Windows, so it's less of a target for hackers.
These factors make Linux generally more secure.


#### Difference between Linux and windows
**Source Code:**
Linux: Open source, allowing anyone to view, modify, and distribute the code.
Windows: Closed source, proprietary software owned by Microsoft.
**Cost:**
Linux: Generally free to use and distribute.
Windows: Requires a paid license.
**User Permissions:**
Linux: Enforces strict user permissions and roles, enhancing security.
Windows: Uses a user account control system, which is less strict compared to Linux.
**Customization:**
Linux: Highly customizable, from the kernel to the user interface.
Windows: Limited customization options; changes are mostly superficial (e.g., themes).
**Software Installation:**
Linux: Uses package managers (e.g., apt, yum) to install software from repositories.
Windows: Software is typically installed using executable (.exe) files from various sources.
**Security:**
Linux: Generally considered more secure due to its permissions system, smaller user base, and open-source nature.
Windows: More targeted by malware due to its larger user base and popularity.
**Performance:**
Linux: Known for its efficiency and performance, particularly on older hardware.
Windows: Requires more resources, especially for newer versions.
 
#### 3. Explain IIS
IIS (Internet Information Services) is Microsoft's web server software for hosting websites and applications on Windows servers. It provides features for managing, securing, and scaling web services with support for various programming languages and protocols.

#### 4. What is interpreter and compiler
- An interpreter translates source code into machine code line-by-line and executes it immediately. Languages like Python and JavaScript use interpreters.
- compiler translates the entire source code into machine code at once, creating an executable file. Languages like C and C++ use compilers.
- Interpreted languages offer faster development and platform independence but slower execution, while compiled languages offer faster execution and standalone executables but slower development cycles.


#### Explain the Linux boot process in detail.
The Linux boot process involves the following steps:
BIOS/UEFI: Initializes hardware and locates the boot loader.
Boot Loader (GRUB/LILO): Loads the kernel into memory and passes control to it.
Kernel Initialization: Decompresses and initializes the kernel, mounts the root filesystem, and starts the init process.
Init Process (systemd/init): Starts system and user space services, setting up the user environment.


#### Describe how to troubleshoot a Linux system that won't boot.
Check boot messages and logs using journalctl -xb.
Boot into rescue mode or use a live CD.
Check the boot loader configuration (/boot/grub/grub.cfg).
Verify filesystem integrity with fsck.
Reinstall or repair the boot loader if necessary.


#### How can you recover a root password on a Linux system?
Boot into single-user mode by editing the boot parameters in GRUB.
Add single or init=/bin/bash to the kernel parameters.
Once in single-user mode, use passwd to change the root password.
Reboot the system.


#### Explain the differences between ext4, XFS, and Btrfs file systems.
ext4: Default filesystem for many Linux distributions, reliable and performant for general use.
XFS: High-performance filesystem, ideal for large files and parallel I/O, good for high-throughput environments.
Btrfs: Modern filesystem with advanced features like snapshots, compression, and subvolumes, suitable for complex storage solutions.

#### How do you optimize system performance in Linux? Provide specific examples.
Disk I/O: Use ionice and tune I/O schedulers.
Memory: Adjust swappiness and use sysctl parameters.
CPU: Use nice and cpuset to manage CPU affinity.
Networking: Tune TCP parameters in /etc/sysctl.conf.


#### What are cgroups and namespaces in Linux, and how are they used in containerization?
Cgroups (Control Groups): Limit, account, and isolate resource usage (CPU, memory, I/O) of process groups.
Namespaces: Isolate different aspects of system resources (processes, networking, filesystems) for a set of processes.
Use in Containerization: Together, they provide the foundation for container isolation and resource management (e.g., Docker).

#### Describe the process of setting up and configuring a high-availability cluster in Linux.
Install and configure clustering software (e.g., Pacemaker, Corosync).
Set up shared storage (e.g., NFS, SAN).
Configure fencing devices to prevent split-brain scenarios.
Create and manage cluster resources and constraints.
Test failover and recovery processes.

#### Explain the Linux kernel's role in managing hardware resources.
The Linux kernel interfaces with hardware through drivers.
Manages CPU scheduling, memory allocation, I/O operations, and networking.
Provides system calls for user-space applications to interact with hardware.

#### What are some advanced uses of awk and sed? Provide examples.
awk: Data extraction and reporting.
bash
Copy code
```
awk '{sum += $2} END {print sum}' file.txt

```
sed: Stream editing.
bash
Copy code
```
sed -e 's/foo/bar/g' -e '/baz/d' file.txt

```
#### How do you secure a Linux server against unauthorized access and attacks?
Use SSH key-based authentication.
Configure firewalls with iptables or firewalld.
Keep the system updated with security patches.
Use fail2ban to protect against brute force attacks.
Disable unused services and ports.
Describe the process of compiling and installing a custom Linux kernel.
Download the kernel source from kernel.org.
Extract the source and configure the kernel options using make menuconfig.
Compile the kernel with make and make modules.
Install the modules with make modules_install.
Install the kernel with make install.
Update the boot loader configuration.
Reboot into the new kernel.


#### What are SELinux and AppArmor, and how do they differ?
SELinux: Uses a set of policies to enforce mandatory access control (MAC), more granular and powerful but complex.
AppArmor: Uses profile-based MAC, easier to use and manage but less granular compared to SELinux.
Explain the process of setting up and using LVM (Logical Volume Manager) in Linux.
Setup:
bash
Copy code
```
pvcreate /dev/sda1
vgcreate myvg /dev/sda1
lvcreate -n mylv -L 10G myvg
mkfs.ext4 /dev/myvg/mylv
mount /dev/myvg/mylv /mnt
```

Usage: Allows flexible disk management, resizing volumes, and snapshots.


#### How do you monitor and manage system logs effectively on a Linux server?
Use journalctl for systemd logs.
Configure rsyslog or syslog-ng for centralized logging.
Rotate logs with logrotate.
Analyze logs with tools like grep, awk, or log analysis platforms like ELK stack.


#### What is the difference between soft limits and hard limits in ulimit? How do you configure them?
Soft Limit: Maximum resource a user can access until modified.
Hard Limit: Maximum resource limit a user can set.
Configuration:
bash
Copy code
```
ulimit -Sn 1024  # Set soft limit
ulimit -Hn 4096  # Set hard limit
```

#### Describe the steps to create and manage RAID arrays in Linux.
Install mdadm.
Create RAID array:
bash
Copy code
```
mdadm --create /dev/md0 --level=1 --raid-devices=2 /dev/sda1 /dev/sdb1

```
Create filesystem and mount:
bash
Copy code
```
mkfs.ext4 /dev/md0
mount /dev/md0 /mnt
```

Add to /etc/mdadm/mdadm.conf and /etc/fstab for persistence.

#### How do you handle and troubleshoot disk I/O issues in Linux?
Use iostat, iotop, and blktrace to monitor disk I/O.
Check for disk errors with dmesg.
Optimize I/O scheduler settings.
Balance I/O load across multiple disks.


#### Explain the use of strace and lsof for debugging in Linux.
strace: Trace system calls made by a process.
bash
Copy code
```
strace -p <pid>
```

lsof: List open files and the processes using them.
bash
Copy code
```
lsof -i :80  # List processes using port 80

```
#### What are some best practices for managing and automating Linux system updates?
Use package managers (e.g., yum, apt) with automation tools like Ansible.
Schedule regular update checks.
Test updates in a staging environment before production deployment.
Use unattended upgrades for critical security patches.

#### How do you set up network bonding and teaming in Linux?
Bonding: Configure in /etc/network/interfaces or /etc/sysconfig/network-scripts/ifcfg-bond0.
bash
Copy code
```
# /etc/network/interfaces
auto bond0
iface bond0 inet dhcp
bond-slaves eth0 eth1
bond-mode 1

```
Teaming: Configure using nmcli or teamd daemon.
#### Explain how to configure and troubleshoot NFS and Samba file sharing services.
NFS:
Install nfs-kernel-server.
Configure exports in /etc/exports.
Start the NFS service.
Troubleshoot with showmount and exportfs.
Samba:
Install samba.
Configure shares in /etc/samba/smb.conf.
Start the Samba service.
Troubleshoot with smbclient and testparm.

#### Describe the use and configuration of iptables and firewalld.
iptables:
Manage rules directly with iptables commands or scripts.
Persist rules in /etc/iptables/rules.v4.
firewalld:
Use firewall-cmd to manage rules.
Zone-based management, easier for dynamic and runtime changes.

#### How do you manage and analyze performance metrics using tools like sar, iostat, and vmstat?
sar: Collect and display system activity.
bash
Copy code
```
sar -u 1 3  # CPU usage
```

iostat: Monitor I/O device loading.
bash
Copy code
```
iostat -x 1 3

```
vmstat: Report virtual memory statistics.
bash
Copy code
```
vmstat 1 3
```

#### What are some advanced techniques for memory management in Linux?
Use sysctl to tweak kernel parameters (e.g., vm.swappiness).
Analyze memory usage with smem and pmap.
Optimize applications with memory caching (e.g., memcached).

#### Explain how to configure and optimize a Linux system for database workloads.
Adjust kernel parameters for I/O and memory (sysctl).
Use appropriate filesystem (e.g., XFS) for databases.
Configure RAID for better I/O performance.
Optimize database-specific settings (e.g., PostgreSQL configuration).

#### Describe the process of setting up a central authentication system using LDAP.
Install and configure an LDAP server (e.g., OpenLDAP).
Populate the LDAP directory with user data.
Configure client machines to use LDAP for authentication.
Integrate with PAM and NSS modules.


#### What are systemd unit files, and how do you create and manage them?
Unit files describe services, targets, and other systemd objects.
Example service unit file:
ini
Copy code
```
[Unit]
Description=My Service

[Service]
ExecStart=/usr/bin/my-service

[Install]
WantedBy=multi-user.target
```

Manage with systemctl (e.g., systemctl start my-service).

#### How do you perform a kernel upgrade on a critical production system with minimal downtime?
Schedule maintenance window.
Prepare a rollback plan.
Use kexec for rebootless kernel updates if supported.
Update the kernel package and reboot.
Verify the new kernel functionality.
Explain the process of migrating services from one Linux server to another.
Plan the migration and test in a staging environment.
Backup data and configurations.
Sync data using rsync.
Update DNS or load balancer configurations.
Verify service functionality on the new server.


#### How do you handle file system corruption and recovery in Linux?
Use fsck to check and repair filesystems.
Mount the filesystem in read-only mode if possible.
Restore from backups if repairs fail.
Investigate the cause of corruption to prevent future issues.




#### Run a Task/Script in the Background:
Command: nohup command &
Explanation: nohup allows a command to continue running even after the terminal is closed. The & puts the command in the background.

#### Kernel-Related Messages:
Command: dmesg
Explanation: dmesg displays kernel-related messages including hardware and system startup messages.

#### List Configured Physical Volumes:
Command: pvdisplay or pvs
Explanation: pvdisplay or pvs shows information about physical volumes in LVM (Logical Volume Manager).

#### Display Memory Usage:
Command: free
Explanation: free displays memory usage, including swap space.

#### Check Disk Usage by User:
Command: du -sh /home/*
Explanation: du (disk usage) displays the amount of space used by each user's home directory.

#### Check Linux Filesystem:
Command: lsblk -f
Explanation: lsblk -f lists block devices and their filesystem information.

#### Sort Content from a File:
Command: sort file
Explanation: sort arranges the lines in a file in alphabetical or numerical order.

#### Display Unique Content from a File:
Command: sort file | uniq
Explanation: sort arranges lines, and uniq removes duplicate lines.

#### Search Multiple Words in a File:
Command: egrep "word1|word2" file
Explanation: egrep (or grep -E) searches for multiple patterns separated by |.

#### Count Lines in a File:
Command: wc -l file
Explanation: wc -l counts the number of lines in a file.

#### Check if Two Files are Identical:
Command: cmp fileA fileB
Explanation: cmp compares two files byte by byte.

#### Compare and Display Differences Between Files:
Command: diff -u fileA fileB
Explanation: diff -u shows the differences between two files in a unified format.

#### Record Terminal Activity:
Command: script filename
Explanation: script records all terminal activity to a file.

#### Display Starting Two Characters of Each Line:
Command: cut -c 1-2 file.txt
Explanation: cut -c 1-2 extracts the first two characters from each line.

#### Display a Specific Line from a File:
Command: sed -n '5p' file.txt
Explanation: sed -n '5p' prints the fifth line of the file.

#### Replace a Specific Word in a File:
Command: sed -i 's/from/to/g' file.txt
Explanation: sed -i 's/from/to/g' replaces all occurrences of from with to in the file.

#### Extend Size of a File Without Adding Data:
Command: truncate -s 100M file.txt
Explanation: truncate -s changes the size of a file to 100 MB without modifying its contents.

#### Check CPU/Core/Thread Info:
Command: lscpu
Explanation: lscpu provides detailed information about CPU architecture and cores.


#### 1. What is the awk command in Linux?
A. powerful text-processing programming language transforming data.

#### 2. How do you check free space available in Linux?
A. display the amount of disk space used and available on Linux file systems.

#### 3. How can you connect to remote servers without a password? How is this achieved?
A. Using SSH Key Authentication.
Generate SSH key pair with ssh-keygen.
Copy the public key to the remote server using ssh-copy-id user@remote_host.
Ensure the ~/.ssh/authorized_keys file on the remote server contains your public key.

#### 4. How do you connect to a remote Linux server using SSH?
A. Use the ssh command: ssh user@remote_server.


#### 5. How do you monitor system performance in Linux?
A. Use commands like top, htop, vmstat, iostat, and sar.

#### 6.How do you check the network connectivity in Linux?
A. Use the ping command: ping <hostname or IP>. For example, ping google.com.

#### 7. What are the ping, telnet, curl, and wget commands in Linux?
A. ping: Checking network connectivity
telnet: it will connect another servers
curl: curl is used in command lines or scripts to transfer data
wget: download file It supports HTTP, HTTPS, and FTP protocols


 
#### What is the boot process in Linux?
The Linux boot process involves several stages:
BIOS/UEFI: Initializes hardware and loads the bootloader from disk.
Bootloader (GRUB, LILO, etc.): Loads the kernel into memory and passes control to it.
Kernel Initialization: The kernel initializes system hardware, mounts the root filesystem, and starts the init process.
Init/Systemd: The init process (or systemd on modern systems) starts essential system services and the user environment.
Runlevel Initialization: Based on the runlevel or target, specific services and processes are started.
Login: The system is ready for user logins.


#### How can you create a zero-size file in Linux?
Use the touch command: touch filename. This creates an empty file if it does not already exist or updates the timestamp if it does.

#### What are soft links and hard links in Linux? How do you create them? What are the differences between these two types of links?
Soft Links (Symbolic Links): They are references to another file or directory. Created using ln -s target link_name. They can span filesystems and can point to directories.
Hard Links: They are references to the same inode as the target file, essentially creating another directory entry for the same file. Created using ln target link_name. Hard links cannot span filesystems and cannot be used for directories.
Differences:
Soft links can be broken if the target is deleted, while hard links remain valid.
Hard links cannot link to directories (except for . and ..).


#### What is the first line typically written in a shell script? What is its meaning? What happens if this line is omitted, and how do you run the script in such a case?
The first line is usually #!/bin/bash or #!/bin/sh, known as a shebang. It specifies the interpreter to execute the script.
If omitted, the script will not have a specified interpreter, and you need to explicitly call the interpreter to run it, e.g., bash script.sh.


#### How can you run a shell script in the background in Linux?
Use & at the end of the command: ./script.sh &. This runs the script in the background.


#### What is a crontab in Linux? Explain how it works and how to configure and schedule a job using crontab.
A crontab is a file that contains a list of commands to be executed at specified intervals. It uses the cron daemon to schedule and run these jobs.
Configure a job:
Edit the crontab file using crontab -e.
Add a line with the format: * * * * * command_to_run, where the five asterisks represent minute, hour, day of month, month, and day of week, respectively.
Save the file to schedule the job.


#### How do you allow ports in Linux?
Use firewall management tools like iptables or firewalld:
With iptables: iptables -A INPUT -p tcp --dport port_number -j ACCEPT.
With firewalld: firewall-cmd --add-port=port_number/tcp --permanent followed by firewall-cmd --reload.


#### How do you troubleshoot a remote server that is experiencing issues?
Check Connectivity: Use ping, traceroute, or telnet to test network connectivity.
Check Logs: Examine system and application logs for errors.
Resource Utilization: Use commands like top, free, df, and du to check resource usage.
SSH Access: Ensure you can SSH into the server and verify service statuses with systemctl or service.


#### What are the ping, telnet, curl, and wget commands in Linux?
ping: Tests network connectivity to a host.
telnet: Connects to a specific port on a remote host to test connectivity.
curl: Transfers data to or from a server using various protocols (e.g., HTTP, FTP).
wget: Downloads files from the web using HTTP, HTTPS, or FTP.


#### How can you check the status of services in a Linux machine?
Use systemctl status service_name or service service_name status for services managed by systemd or SysVinit, respectively.

#### do you kill a process in Linux?
Use the kill command with the process ID (PID): kill PID.
For more forceful termination, use kill -9 PID.


#### What are the nice and renice commands in Linux?
nice: Starts a process with a specified priority level (niceness). Example: nice -n 10 command.
renice: Changes the priority of an already running process. Example: renice -n 10 -p PID.


#### What is an inode in Linux?
An inode is a data structure on a filesystem that stores information about a file or directory, such as its size, owner, permissions, and disk location, but not its name.

#### How do you check CPU utilization in Linux?
Use commands like top, htop, or mpstat (from the sysstat package) to view CPU usage statistics.


#### What are the differences between the top and htop commands?
top: Provides a text-based interface for monitoring system processes and resource usage.
htop: An enhanced, interactive version of top with a more user-friendly interface, color-coding, and the ability to scroll through the process list.


#### What is a mount in Linux, and how do you create one?
A mount is the process of making a filesystem accessible at a specific directory in the existing filesystem tree. To create one:
Use the mount command: mount /dev/device /mount_point.

#### How do you troubleshoot live logs in Linux?
Use commands like tail -f /path/to/logfile to view real-time log updates.
Check logs in directories like /var/log/ for system and application logs.

#### What is the sed command in Linux?
sed (stream editor) is used for parsing and transforming text from input streams or files. Example: sed 's/old/new/g' file replaces all occurrences of "old" with "new".

#### What is the awk command in Linux?
awk is a text-processing tool used for pattern scanning and processing. It can perform operations on text files and data streams. Example: awk '{print $1}' file prints the first field of each line.

#### What are the grep and egrep commands in Linux?
grep: Searches for patterns within files. Example: grep 'pattern' file.
egrep: An extended version of grep that supports extended regular expressions.

#### How can you list only directories in a Linux environment?
Use ls -d */ to list directories in the current directory.

#### How do you check the processes running in Linux?
Use ps aux or top to list running processes. For a more detailed view, pstree can be used to display processes in a tree format.

#### How do you get a Java thread dump in Linux?
Use the jstack command followed by the PID of the Java process: jstack PID.

#### How can you check the running ports on a Linux machine?
Use netstat -tuln or ss -tuln to list all listening ports and associated services.

#### How do you declare a variable in a shell script?
Declare a variable using variable_name=value. For example: name="John".

#### What do $?, $#, and $* represent in shell scripting?
$?: The exit status of the last executed command.
$#: The number of positional parameters passed to the script.
$*: All the positional parameters passed to the script as a single string.

#### How do you read a command line input in a shell script?
Use the read command: read variable_name. Example: read name.

#### What is umask in Linux?
umask is a command that sets default file creation permissions. It defines the default permissions that are masked out when files or directories are created.


#### How do you change file permissions in Linux?
Use the chmod command. Example: chmod 755 filename sets read, write, and execute permissions for the owner, and read and execute permissions for others.

#### How can you connect to remote servers without a password? How is this achieved?
Use SSH keys for passwordless authentication. Generate a key pair using ssh-keygen, and copy the public key to the remote server’s ~/.ssh/authorized_keys file using ssh-copy-id.


#### How do you open a file in read-only mode in the vi editor?
Use the command vi -R filename or open the file normally and enter command mode, then type :view filename.


#### What is the purpose of the export command in Linux?
The export command sets environment variables that are available to child processes. Example: export VAR=value.

#### How do you send error logs and stdout logs to different files in Linux?
Use redirection operators. Example: command > stdout.log 2> error.log.

#### What is the nohup command in Linux?
nohup (no hang up) allows a command to continue running even after the user has logged out. Example: nohup command &.


#### What does the netstat command do in Linux?
netstat displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.


#### How do you run a script at boot level in Linux?
Place the script in /etc/init.d/ and create a symlink to it in the appropriate runlevel directories (e.g., /etc/rc.local for traditional SysVinit systems). For systemd, create a service file and enable it using systemctl enable service_name.

