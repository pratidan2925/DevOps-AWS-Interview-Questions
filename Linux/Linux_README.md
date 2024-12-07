# Linux

#### What is Linux

- Linux is an open-source operating system kernel developed by Linus Torvalds in 1991. It's the core component of various Linux distributions (or distros) such as Ubuntu, Fedora, and Debian. Linux is known for its stability, security, and flexibility, making it popular for use in servers, desktop computers, mobile devices, and embedded systems. It supports a wide range of software and is highly customizable to meet different needs.
---
#### how to give permission to Linux ?  And What is chmod ?

- "chmod" is a command in Linux used to change permissions for files and directories. It allows you to specify who can read, write, or execute a file or directory. You can use symbolic or octal notation to set permissions. For example, chmod u+x file.txt adds execute permission for the owner of "file.txt", while chmod 755 file.txt gives the owner full permissions and read/execute permissions to the group and others.

- Read -  4      

- write - 2     

- execute - 1
 ---
#### 777 in Linux

In Linux, "777" is a file permission notation representing full read, write, and execute permissions for the owner, group, and others.
 ---
#### Which Linux  and Windows version do you use?

- **linux :**
- Ubuntu 18.x  -- decamped /not in use for  5/6 months.
- Ubuntu 22.04  –  Recently used.
- Ubuntu 24.04  -- latest version – recently used.

- **Windows :** 
- 2019 -recently used .
- 2022- latest version

 - Note : Company never goeson latest version ,as it may have issues. So they always use one     version older than the latest version .
 ---
#### What is the key difference  between Linux server and ubuntu server?

- **Linux Server:** "Linux server" refers to any server operating system based on the Linux kernel. It's a broad term encompassing various distributions (distros) like Ubuntu Server, CentOS, Debian, Fedora, etc. Each distribution may have its own package management system, default software, and support policies.
- **Ubuntu Server:** Ubuntu Server is a specific distribution of Linux tailored for server environments. It's maintained by Canonical and is based on the Debian architecture. Ubuntu Server is known for its ease of use, regular updates, strong community support, and compatibility with a wide range of software packages. It's often chosen for web servers, cloud deployments, and enterprise applications.
- In essence, while "Linux server" is a generic term referring to any server running a Linux-based operating system, "Ubuntu server" specifically denotes a server running the Ubuntu distribution of Linux.
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
- Stores Settings: This folder holds configuration files that control how the system and various programs behave.
- System-Wide Impact: Changes in this folder affect the whole system, not just one user.
 ---
#### Difference Between YUM and APT
- YUM (Yellowdog Updater, Modified) and APT (Advanced Package Tool) are both package management systems used in Linux distributions.
- **YUM**  is used for Amazon Linux while APT is used for Ubuntu Linux.
 
- Distribution: Primarily used in RPM-based distributions like Red Hat Enterprise Linux (RHEL), CentOS, and Fedora.
- Package Format: Handles .rpm (Red Hat Package Manager) files.
- Dependencies: Automatically resolves and installs package dependencies.
- Repositories: Uses repository configurations in /etc/yum.repos.d/.
- Commands: Common commands include yum install, yum update, yum remove, and yum search.
- Features: Supports plugins, allows for easy repository management, and has a strong focus on backward compatibility.

**APT**
- Distribution: Primarily used in Debian-based distributions like Debian, Ubuntu, and their derivatives.
- Package Format: Handles .deb (Debian) files.
- Dependencies: Automatically resolves and installs package dependencies.
- Repositories: Uses repository configurations in /etc/apt/sources.list and /etc/apt/sources.list.d/.
- Commands: Common commands include apt-get install, apt-get update, apt-get remove, and apt-cache search. apt is a newer, user-friendly command-line tool that combines the most commonly used commands.
- Features: Offers a more user-friendly command-line interface with apt, provides extensive documentation, and emphasizes a large community and ecosystem.

---
####  How to get info for all the packages installed on Linux system
- yum list installed
- apt list –installed
---
#### How to check the kernel version in Linux
- uname -r -- This command will output the kernel version.
- cat /proc/version -- This command will display the kernel version along with additional information about the build
- hostnamectl -- This command will display the kernel version along with additional information about the build
---
####  Explain Linux distribution
- A Linux distribution, often referred to as a "distro," is a complete operating system built on the Linux kernel along with a collection of software applications, libraries, and utilities.
Examples of popular Linux distributions include Ubuntu, Fedora, Debian, CentOS, Arch Linux, and openSUSE. Each distribution may target specific use cases, such as general-purpose desktops, servers, embedded systems, or specialized applications.
---
#### How to backup a Linux server?
- To back up a Linux server, there are several methods you can use, depending on the requirements and the environment. Some of the most common methods include using rsync, tar, dd, rsnapshot, Bacula, and Duplicity
-  rsync: Efficient for file synchronization and backups.
- tar: Creates compressed archive files.
- dd: For full disk backups.
- Automation with cron: Schedule regular backups.
**Advanced Tools:**
- rsnapshot: For incremental backups.
- Bacula and Duplicity: For more complex needs, including encryption and remote backups.
---

#### how to check running processes in linux /what is the use of ps-aux in linux /what is Top command & its uses.
- **top Command**
- Displays real-time system summary and list of processes.

- **Ps-aux Command**
- Displays information about active processes.
    - a: Displays processes from all users.
    - u: Shows detailed user-oriented format.
    - x: Includes processes without a controlling terminal.
---
#### How to check system load in linux
- top Command
- Displays real-time information about system processes, including system load.
- Load average: Displayed at the top of the screen, shows system load over the last 1, 5, and 15 minutes.

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
- **nr Start-ds**
 - To start a Linux server, boot it up either from a virtual machine manager or by pressing the power button if it's a physical server. - Then, log in using SSH or a remote desktop connection. Finally, verify that essential services are running and check the server's status.
- Use commands like uptime or systemctl status to verify its status.
---
#### Explain Grep vs sed command
- **Grep:**
- Purpose: Searches for patterns within text.
- Functionality: Prints lines that match a specified pattern.
- Usage Example: grep 'error' logfile.txt - Finds and displays lines containing "error" in logfile.txt.
- **Sed:**
- Purpose: Stream editor for modifying text.
- Functionality: Performs find-and-replace, text transformation, and filtering.
- Usage Example: sed 's/error/success/' logfile.txt - Replaces the first occurrence of "error" with "success" in each line of logfile.txt.
--- 
#### Explain Cat vs more command
- **- cat (concatenate):**
- Purpose: Displays the content of files and concatenates them.
- Functionality: Outputs the entire content of a file to the terminal.
- Usage Example: cat filename.txt - Displays the full content of filename.txt.

- **- more:**
- Purpose: Displays the content of files one screen at a time.
- Functionality: Allows for paginated viewing of long text files, enabling scrolling through the content.
- Usage Example: more filename.txt - Displays the content of filename.txt one screen at a time.
- **Summary:**
- cat is used to quickly display the full content of a file.
- more is used to view the content of a file one page at a time, which is useful for long files.




---
#### How do you diagnose and fix a network connectivity issue on a Linux server?
- **Diagnose:**
- Check Network Interfaces: Use ip a or ifconfig to check the status of network interfaces.
- Ping Test: Test connectivity to local and remote hosts using ping.
- Traceroute: Use traceroute to identify where connectivity issues occur in the network path.
- Check Routing Table: Use ip route to verify correct routing.
- Review Logs: Check system logs (/var/log/syslog or /var/log/messages) for network-related errors.
- **Fix:**
- Correct Network Configuration: Ensure IP settings, gateway, and DNS configurations are correct in /etc/network/interfaces or similar files.
- Restart Networking Service: Restart networking services with systemctl restart network or systemctl restart NetworkManager.
- Update Drivers/Kernel: Ensure network drivers and kernel are up-to-date.

#### Explain the process of setting up and configuring a mail server on Linux.
- Choose Mail Server Software: Common choices include Postfix, Sendmail, or Exim.
- Install Software:
- Postfix: sudo apt-get install postfix
- Configure:
- Edit Configuration Files: Configure /etc/postfix/main.cf for Postfix. Set parameters like myhostname, mydestination, and relayhost.
- Setup Domains and Aliases: Configure virtual domains and aliases in /etc/postfix/virtual.
- Start and Enable Services: Start Postfix with systemctl start postfix and enable it with systemctl enable postfix.
- Test: Use telnet or mail command to test sending and receiving mail.

#### How do you implement and manage disk quotas for users on a Linux system?
- Install Quota Tools: Install quota tools if not already installed (sudo apt-get install quota).
- **Configure Filesystems:**
- Edit /etc/fstab: Add usrquota and/or grpquota to the filesystem options. Example: /dev/sda1 /home ext4 defaults,usrquota 0 2.
- **Apply Quotas:**
- Create Quota Files: Use quotacheck -cug /home to create quota files.
- Set Quotas: Use edquota -u username to set user quotas, and quotaon -v /home to enable quotas.
- Monitor Quotas: Use repquota /home to review quota usage.

#### Describe the steps to compile and install software from source in Linux.
- Download Source Code: Obtain the source code tarball (e.g., wget https://example.com/software.tar.gz).
- Extract: Extract the tarball with tar -xzf software.tar.gz.
- Navigate to Directory: Change to the extracted directory (cd software).
- Configure: Run ./configure to check for dependencies and configure the build environment.
- Compile: Compile the software with make.
- Install: Install the compiled software with sudo make install.
- Verify: Check the installation by running the software or using which to locate the binary.

#### What are the key differences between systemd and init? How do you manage services with systemd?
**Differences:**
- Initialization: systemd is an advanced init system that uses parallelization and dependency tracking. init is an older, simpler system that processes scripts sequentially.
- Service Management: systemd uses unit files and a more comprehensive service management framework, while init uses shell scripts.
**Managing Services with systemd:**
- Start Service: systemctl start service_name
- Stop Service: systemctl stop service_name
- Enable Service: systemctl enable service_name
- Disable Service: systemctl disable service_name
- Check Status: systemctl status service_name
- View Logs: journalctl -u service_name


#### How do you handle kernel module management in Linux?
- List Modules: Use lsmod to list currently loaded modules.
- Load Module: Use modprobe module_name to load a module.
- Unload Module: Use modprobe -r module_name or rmmod module_name to remove a module.
- View Module Information: Use modinfo module_name to view detailed information about a module.


#### Explain how to set up a secure FTP server in Linux.
- Install vsftpd: sudo apt-get install vsftpd
- Configure:
- Edit Configuration File: Modify /etc/vsftpd.conf. Set parameters like anonymous_enable=NO, local_enable=YES, write_enable=YES, chroot_local_user=YES.
- Enable SSL/TLS: Configure SSL/TLS settings if required (ssl_enable=YES, rsa_cert_file=/etc/ssl/certs/vsftpd.pem).
- Start and Enable Service: Start with systemctl start vsftpd and enable with systemctl enable vsftpd.


#### How do you use iptables to configure firewall rules? Provide an example.
- List Rules: iptables -L
- Add Rule: Use iptables -A INPUT -p tcp --dport 22 -j ACCEPT to allow incoming SSH traffic.
- Save Rules: Save the configuration to ensure persistence (iptables-save > /etc/iptables/rules.v4).
- Example: To block all incoming traffic except for SSH and HTTP:
``` 
iptables -P INPUT DROP
iptables -A INPUT -p tcp --dport 22 -j ACCEPT
iptables -A INPUT -p tcp --dport 80 -j ACCEPT
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT

```
#### What are the steps to configure NFS (Network File System) for file sharing in Linux?
- Install NFS Server: sudo apt-get install nfs-kernel-server
- Configure Exports:
- Edit /etc/exports: Add the directory to be shared and its permissions, e.g., /srv/nfs/share *(rw,sync,no_subtree_check).
-  Export Shares: Run exportfs -a to apply the changes.
- Start and Enable NFS: Start with systemctl start nfs-kernel-server and enable with systemctl enable nfs-kernel-server.
- Client Configuration:
- Install NFS Client: sudo apt-get install nfs-common
- Mount NFS Share: mount server:/srv/nfs/share /mnt

#### How do you automate system administration tasks in Linux using shell scripts?
- Write Script: Create a shell script file with #!/bin/bash at the top and include commands for tasks you want to automate.
- Make Executable: Use chmod +x script.sh to make the script executable.
- Schedule: Use cron to schedule scripts. Edit the crontab file with crontab -e and add a line like 0 2 * * * /path/to/script.sh to run the script daily at 2 AM.


#### Explain the process of setting up a DNS server using BIND in Linux.
- Install BIND: sudo apt-get install bind9
- Configure BIND:
- Edit /etc/bind/named.conf.local: Add zone definitions, e.g.,

```
zone "example.com" {
    type master;
    file "/etc/bind/db.example.com";
};
```

- Create Zone Files: Create and edit zone files (e.g., /etc/bind/db.example.com) with DNS records.
- Restart BIND: Apply changes with systemctl restart bind9.
- Test: Use dig or nslookup to test DNS resolution.
#### How do you manage and monitor running processes in Linux? Discuss tools and commands you use.
- **Commands:**
- ps: Display information about running processes. Use ps aux for a detailed list.
- top: Monitor processes in real-time with a dynamic interface.
- htop: An enhanced version of top with a more user-friendly interface.
- systemctl: Manage services and view their status with systemctl status service_name.
**Monitoring Tools:**
- netstat: Monitor network connections.
- vmstat: Report system performance.

#### Describe how to create and manage Docker containers on a Linux server.
- Create Container: Use docker run to create and start a container, e.g., docker run -d --name my_container nginx.
- Manage Containers:
- List: docker ps shows running containers.
- Stop: docker stop my_container
- Remove: docker rm my_container
- View Logs: docker logs my_container
- Dockerfile: Define container configuration and build custom images with docker build -t my_image ..

#### How do you configure and use rsyslog for centralized logging in Linux?
- Install rsyslog: sudo apt-get install rsyslog
- Configure Server:
- Edit /etc/rsyslog.conf: Enable UDP/TCP reception with lines like module(load="imudp") and input(type="imudp" port="514").
- Restart rsyslog: Apply changes with systemctl restart rsyslog.
- Configure Clients:
- Edit /etc/rsyslog.conf: Add *.* @server_ip:514 to send logs to the server.
- Verify: Use logger to test log sending and check the server logs.


#### What are your methods for securing SSH access on a Linux server?
- Use Strong Passwords: Ensure strong passwords for SSH access.
- Use SSH Keys: Configure key-based authentication and disable password authentication in /etc/ssh/sshd_config.
- Change Default Port: Change the default SSH port from 22 to a non-standard port.
- Limit Access: Use AllowUsers or AllowGroups directives in /etc/ssh/sshd_config to restrict access.
- Firewall Rules: Restrict access to the SSH port using firewall rules (e.g., with iptables or ufw).

#### Explain how to set up and configure a proxy server in Linux.
- Install Proxy Server Software: Examples include Squid (sudo apt-get install squid).
- **Configure:**
- Edit Configuration File: Configure /etc/squid/squid.conf with ACLs and rules for access control.
- **Example:**

```
acl localnet src 192.168.1.0/24
http_access allow localnet
```

- Start and Enable: Start with systemctl start squid and enable with systemctl enable squid.

#### How do you troubleshoot file permission issues in Linux?
- Check Permissions: Use ls -l to view file permissions.
- Change Permissions: Use chmod to modify permissions (e.g., chmod 755 file).
- Check Ownership: Use chown to change file ownership (e.g., chown user:group file).
- Review SELinux/AppArmor: Check for security contexts or profiles if using SELinux or AppArmor.

#### Describe the process of setting up and managing a MySQL or PostgreSQL database server in Linux.
- **Install MySQL/PostgreSQL:**
- MySQL: sudo apt-get install mysql-server
- PostgreSQL: sudo apt-get install postgresql
- **Configure:**
- MySQL: Edit /etc/mysql/mysql.conf.d/mysqld.cnf for configurations.
- PostgreSQL: Edit /etc/postgresql/<version>/main/postgresql.conf.
- Start and Enable: Start with systemctl start mysql or systemctl start postgresql and enable with systemctl enable mysql or systemctl enable postgresql.
- **Manage Databases:**
- MySQL: Use mysql command-line tool.
- PostgreSQL: Use psql command-line tool.

#### How do you perform a system audit to ensure compliance with security policies in Linux?
- Use Audit Tools:
- auditd: Install and configure auditd for system auditing. Configure rules in /etc/audit/audit.rules.
- osquery: Use osquery to perform SQL-like queries on the system.
- Review Logs: Analyze audit logs located in /var/log/audit/.
- Security Scanning: Use tools like Lynis or OpenVAS for vulnerability scanning.

#### What are the steps to configure a VPN server on a Linux machine?
- Install VPN Software: For example, OpenVPN (sudo apt-get install openvpn).
- **Configure VPN:**
- Edit Configuration Files: Set up server and client configuration files in /etc/openvpn/.
- Start VPN Service: Start with systemctl start openvpn@server and enable with systemctl enable openvpn@server.
- Configure Firewall: Ensure necessary ports are open (e.g., 1194/udp for OpenVPN).
- Test: Connect using a VPN client to verify functionality.





 #### Why linux is more secure than windows explain in short.
-  Linux is often seen as more secure than Windows for a few simple reasons:
- **Open Source:** Since the code is open for everyone to see, many people can check and fix security problems quickly.
- **User Permissions:** Linux restricts what regular users can do, making it harder for viruses to cause damage.
- **Built-In Security:** It has strong security tools like SELinux and AppArmor that help protect the system.
- **Variety:** There are many different versions of Linux, so a virus for one version might not work on another.
- **Less Targeted:** Fewer people use Linux compared to Windows, so it's less of a target for hackers.
- These factors make Linux generally more secure.


#### Difference between Linux and windows
- **Source Code:**
- Linux: Open source, allowing anyone to view, modify, and distribute the code.
- Windows: Closed source, proprietary software owned by Microsoft.
- **Cost:**
- Linux: Generally free to use and distribute.
- Windows: Requires a paid license.
- **User Permissions:**
- Linux: Enforces strict user permissions and roles, enhancing security.
- Windows: Uses a user account control system, which is less strict compared to Linux.
- **Customization:**
- Linux: Highly customizable, from the kernel to the user interface.
- Windows: Limited customization options; changes are mostly superficial (e.g., themes).
- **Software Installation:**
- Linux: Uses package managers (e.g., apt, yum) to install software from repositories.
- Windows: Software is typically installed using executable (.exe) files from various sources.
- **Security:**
- Linux: Generally considered more secure due to its permissions system, smaller user base, and open-source nature.
- Windows: More targeted by malware due to its larger user base and popularity.
- **Performance:**
- Linux: Known for its efficiency and performance, particularly on older hardware.
- Windows: Requires more resources, especially for newer versions.
 
#### 3. Explain IIS
IIS (Internet Information Services) is Microsoft's web server software for hosting websites and applications on Windows servers. It provides features for managing, securing, and scaling web services with support for various programming languages and protocols.

#### 4. What is interpreter and compiler
- An interpreter translates source code into machine code line-by-line and executes it immediately. Languages like Python and JavaScript use interpreters.
- compiler translates the entire source code into machine code at once, creating an executable file. Languages like C and C++ use compilers.
- Interpreted languages offer faster development and platform independence but slower execution, while compiled languages offer faster execution and standalone executables but slower development cycles.


#### Explain the Linux boot process in detail.
- The Linux boot process involves the following steps:
- BIOS/UEFI: Initializes hardware and locates the boot loader.
- Boot Loader (GRUB/LILO): Loads the kernel into memory and passes control to it.
- Kernel Initialization: Decompresses and initializes the kernel, mounts the root filesystem, and starts the init process.
- Init Process (systemd/init): Starts system and user space services, setting up the user environment.


#### Describe how to troubleshoot a Linux system that won't boot.
- Check boot messages and logs using journalctl -xb.
- Boot into rescue mode or use a live CD.
- Check the boot loader configuration (/boot/grub/grub.cfg).
-Verify filesystem integrity with fsck.
- Reinstall or repair the boot loader if necessary.


#### How can you recover a root password on a Linux system?
- Boot into single-user mode by editing the boot parameters in GRUB.
- Add single or init=/bin/bash to the kernel parameters.
- Once in single-user mode, use passwd to change the root password.
- Reboot the system.


#### Explain the differences between ext4, XFS, and Btrfs file systems.
- ext4: Default filesystem for many Linux distributions, reliable and performant for general use.
- XFS: High-performance filesystem, ideal for large files and parallel I/O, good for high-throughput environments.
- Btrfs: Modern filesystem with advanced features like snapshots, compression, and subvolumes, suitable for complex storage solutions.

#### How do you optimize system performance in Linux? Provide specific examples.
- Disk I/O: Use ionice and tune I/O schedulers.
- Memory: Adjust swappiness and use sysctl parameters.
- CPU: Use nice and cpuset to manage CPU affinity.
- Networking: Tune TCP parameters in /etc/sysctl.conf.


#### What are cgroups and namespaces in Linux, and how are they used in containerization?
- Cgroups (Control Groups): Limit, account, and isolate resource usage (CPU, memory, I/O) of process groups.
- Namespaces: Isolate different aspects of system resources (processes, networking, filesystems) for a set of processes.
- Use in Containerization: Together, they provide the foundation for container isolation and resource management (e.g., Docker).

#### Describe the process of setting up and configuring a high-availability cluster in Linux.
- Install and configure clustering software (e.g., Pacemaker, Corosync).
- Set up shared storage (e.g., NFS, SAN).
- Configure fencing devices to prevent split-brain scenarios.
- Create and manage cluster resources and constraints.
- Test failover and recovery processes.

#### Explain the Linux kernel's role in managing hardware resources.
- The Linux kernel interfaces with hardware through drivers.
- Manages CPU scheduling, memory allocation, I/O operations, and networking.
- Provides system calls for user-space applications to interact with hardware.

#### What are some advanced uses of awk and sed? Provide examples.
- **awk:** Data extraction and reporting.

```
awk '{sum += $2} END {print sum}' file.txt

```
- **sed:** Stream editing.

```
sed -e 's/foo/bar/g' -e '/baz/d' file.txt

```
#### How do you secure a Linux server against unauthorized access and attacks?
- Use SSH key-based authentication.
- Configure firewalls with iptables or firewalld.
- Keep the system updated with security patches.
- Use fail2ban to protect against brute force attacks.
- Disable unused services and ports.

#### Describe the process of compiling and installing a custom Linux kernel.
- Download the kernel source from kernel.org.
- Extract the source and configure the kernel options using make menuconfig.
- Compile the kernel with make and make modules.
- Install the modules with make modules_install.
- Install the kernel with make install.
- Update the boot loader configuration.
- Reboot into the new kernel.


#### What are SELinux and AppArmor, and how do they differ?
- SELinux: Uses a set of policies to enforce mandatory access control (MAC), more granular and powerful but complex.
- AppArmor: Uses profile-based MAC, easier to use and manage but less granular compared to SELinux.

#### Explain the process of setting up and using LVM (Logical Volume Manager) in Linux.
- **Setup:**

```
pvcreate /dev/sda1
vgcreate myvg /dev/sda1
lvcreate -n mylv -L 10G myvg
mkfs.ext4 /dev/myvg/mylv
mount /dev/myvg/mylv /mnt
```

- Usage: Allows flexible disk management, resizing volumes, and snapshots.


#### How do you monitor and manage system logs effectively on a Linux server?
- Use journalctl for systemd logs.
- Configure rsyslog or syslog-ng for centralized logging.
- Rotate logs with logrotate.
- Analyze logs with tools like grep, awk, or log analysis platforms like ELK stack.


#### What is the difference between soft limits and hard limits in ulimit? How do you configure them?
- Soft Limit: Maximum resource a user can access until modified.
- Hard Limit: Maximum resource limit a user can set.
- **Configuration:**

```
ulimit -Sn 1024  # Set soft limit
ulimit -Hn 4096  # Set hard limit
```

#### Describe the steps to create and manage RAID arrays in Linux.
- Install mdadm.
- **Create RAID array:**

```
mdadm --create /dev/md0 --level=1 --raid-devices=2 /dev/sda1 /dev/sdb1

```
- **Create filesystem and mount:**

```
mkfs.ext4 /dev/md0
mount /dev/md0 /mnt
```

- Add to /etc/mdadm/mdadm.conf and /etc/fstab for persistence.

#### How do you handle and troubleshoot disk I/O issues in Linux?
- Use iostat, iotop, and blktrace to monitor disk I/O.
- Check for disk errors with dmesg.
- Optimize I/O scheduler settings.
- Balance I/O load across multiple disks.


#### Explain the use of strace and lsof for debugging in Linux.
**strace:** Trace system calls made by a process.
```
strace -p <pid>
```

**lsof:** List open files and the processes using them.
```
lsof -i :80  # List processes using port 80
```
#### What are some best practices for managing and automating Linux system updates?
- Use package managers (e.g., yum, apt) with automation tools like Ansible.
- Schedule regular update checks.
- Test updates in a staging environment before production deployment.
- Use unattended upgrades for critical security patches.

#### How do you set up network bonding and teaming in Linux?
- Bonding: Configure in /etc/network/interfaces or /etc/sysconfig/network-scripts/ifcfg-bond0.

```
# /etc/network/interfaces
auto bond0
iface bond0 inet dhcp
bond-slaves eth0 eth1
bond-mode 1

```
- Teaming: Configure using nmcli or teamd daemon.

#### Explain how to configure and troubleshoot NFS and Samba file sharing services.
- **NFS:**
- Install nfs-kernel-server.
- Configure exports in /etc/exports.
- Start the NFS service.
- Troubleshoot with showmount and exportfs.
- **Samba:**
- Install samba.
- Configure shares in /etc/samba/smb.conf.
- Start the Samba service.
- Troubleshoot with smbclient and testparm.

#### Describe the use and configuration of iptables and firewalld.
- **iptables:**
- Manage rules directly with iptables commands or scripts.
- Persist rules in /etc/iptables/rules.v4.
- **firewalld:**
- Use firewall-cmd to manage rules.
- Zone-based management, easier for dynamic and runtime changes.

#### How do you manage and analyze performance metrics using tools like sar, iostat, and vmstat?
**sar:** Collect and display system activity.

```
sar -u 1 3  # CPU usage
```

**iostat:** Monitor I/O device loading.

```
iostat -x 1 3

```
**vmstat:** Report virtual memory statistics.

```
vmstat 1 3
```

#### What are some advanced techniques for memory management in Linux?
- Use sysctl to tweak kernel parameters (e.g., vm.swappiness).
- Analyze memory usage with smem and pmap.
- Optimize applications with memory caching (e.g., memcached).

#### Explain how to configure and optimize a Linux system for database workloads.
- Adjust kernel parameters for I/O and memory (sysctl).
- Use appropriate filesystem (e.g., XFS) for databases.
- Configure RAID for better I/O performance.
- Optimize database-specific settings (e.g., PostgreSQL configuration).

#### Describe the process of setting up a central authentication system using LDAP.
- Install and configure an LDAP server (e.g., OpenLDAP).
- Populate the LDAP directory with user data.
- Configure client machines to use LDAP for authentication.
- Integrate with PAM and NSS modules.


#### What are systemd unit files, and how do you create and manage them?
- Unit files describe services, targets, and other systemd objects.
**Example service unit file:**

```
[Unit]
Description=My Service

[Service]
ExecStart=/usr/bin/my-service

[Install]
WantedBy=multi-user.target
```

- Manage with systemctl (e.g., systemctl start my-service).

#### How do you perform a kernel upgrade on a critical production system with minimal downtime?
- Schedule maintenance window.
- Prepare a rollback plan.
- Use kexec for rebootless kernel updates if supported.
- Update the kernel package and reboot.
- Verify the new kernel functionality.

#### Explain the process of migrating services from one Linux server to another.
- Plan the migration and test in a staging environment.
- Backup data and configurations.
- Sync data using rsync.
- Update DNS or load balancer configurations.
- Verify service functionality on the new server.


#### How do you handle file system corruption and recovery in Linux?
- Use fsck to check and repair filesystems.
- Mount the filesystem in read-only mode if possible.
- Restore from backups if repairs fail.
- Investigate the cause of corruption to prevent future issues.




#### Run a Task/Script in the Background:
- Command: nohup command &
- Explanation: nohup allows a command to continue running even after the terminal is closed. The & puts the command in the background.

#### Kernel-Related Messages:
- Command: dmesg
- Explanation: dmesg displays kernel-related messages including hardware and system startup messages.

#### List Configured Physical Volumes:
- Command: pvdisplay or pvs
- Explanation: pvdisplay or pvs shows information about physical volumes in LVM (Logical Volume Manager).

#### Display Memory Usage:
- Command: free
- Explanation: free displays memory usage, including swap space.

#### Check Disk Usage by User:
- Command: du -sh /home/*
- Explanation: du (disk usage) displays the amount of space used by each user's home directory.

#### Check Linux Filesystem:
- Command: lsblk -f
- Explanation: lsblk -f lists block devices and their filesystem information.

#### Sort Content from a File:
- Command: sort file
- Explanation: sort arranges the lines in a file in alphabetical or numerical order.

#### Display Unique Content from a File:
- Command: sort file | uniq
- Explanation: sort arranges lines, and uniq removes duplicate lines.

#### Search Multiple Words in a File:
- Command: egrep "word1|word2" file
- Explanation: egrep (or grep -E) searches for multiple patterns separated by |.

#### Count Lines in a File:
- Command: wc -l file
- Explanation: wc -l counts the number of lines in a file.

#### Check if Two Files are Identical:
- Command: cmp fileA fileB
- Explanation: cmp compares two files byte by byte.

#### Compare and Display Differences Between Files:
- Command: diff -u fileA fileB
- Explanation: diff -u shows the differences between two files in a unified format.

#### Record Terminal Activity:
- Command: script filename
- Explanation: script records all terminal activity to a file.

#### Display Starting Two Characters of Each Line:
- Command: cut -c 1-2 file.txt
- Explanation: cut -c 1-2 extracts the first two characters from each line.

#### Display a Specific Line from a File:
- Command: sed -n '5p' file.txt
- Explanation: sed -n '5p' prints the fifth line of the file.

#### Replace a Specific Word in a File:
- Command: sed -i 's/from/to/g' file.txt
- Explanation: sed -i 's/from/to/g' replaces all occurrences of from with to in the file.

#### Extend Size of a File Without Adding Data:
- Command: truncate -s 100M file.txt
- Explanation: truncate -s changes the size of a file to 100 MB without modifying its contents.

#### Check CPU/Core/Thread Info:
- Command: lscpu
- Explanation: lscpu provides detailed information about CPU architecture and cores.


#### 1. What is the awk command in Linux?
A. powerful text-processing programming language transforming data.

#### 2. How do you check free space available in Linux?
A. display the amount of disk space used and available on Linux file systems.

#### 3. How can you connect to remote servers without a password? How is this achieved?
- Using SSH Key Authentication.
- Generate SSH key pair with ssh-keygen.
- Copy the public key to the remote server using ssh-copy-id user@remote_host.
- Ensure the ~/.ssh/authorized_keys file on the remote server contains your public key.

#### 4. How do you connect to a remote Linux server using SSH?
A. Use the ssh command: ssh user@remote_server.


#### 5. How do you monitor system performance in Linux?
A. Use commands like top, htop, vmstat, iostat, and sar.

#### 6.How do you check the network connectivity in Linux?
A. Use the ping command: ping <hostname or IP>. For example, ping google.com.

 
#### What is the boot process in Linux?
- The Linux boot process involves several stages:
- BIOS/UEFI: Initializes hardware and loads the bootloader from disk.
- Bootloader (GRUB, LILO, etc.): Loads the kernel into memory and passes control to it.
- Kernel Initialization: The kernel initializes system hardware, mounts the root filesystem, and starts the init process.
- Init/Systemd: The init process (or systemd on modern systems) starts essential system services and the user environment.
- Runlevel Initialization: Based on the runlevel or target, specific services and processes are started.
- Login: The system is ready for user logins.


#### How can you create a zero-size file in Linux?
Use the touch command: touch filename. This creates an empty file if it does not already exist or updates the timestamp if it does.

#### What are soft links and hard links in Linux? How do you create them? What are the differences between these two types of links?
- **Soft Links (Symbolic Links):** They are references to another file or directory. Created using ln -s target link_name. They can span filesystems and can point to directories.
- **Hard Links:** They are references to the same inode as the target file, essentially creating another directory entry for the same file. Created using ln target link_name. Hard links cannot span filesystems and cannot be used for directories.
- **Differences:**
- Soft links can be broken if the target is deleted, while hard links remain valid.
- Hard links cannot link to directories (except for . and ..).


#### What is the first line typically written in a shell script? What is its meaning? What happens if this line is omitted, and how do you run the script in such a case?
- The first line is usually #!/bin/bash or #!/bin/sh, known as a shebang. It specifies the interpreter to execute the script.
- If omitted, the script will not have a specified interpreter, and you need to explicitly call the interpreter to run it, e.g., bash script.sh.


#### How can you run a shell script in the background in Linux?
Use & at the end of the command: ./script.sh &. This runs the script in the background.


#### What is a crontab in Linux? Explain how it works and how to configure and schedule a job using crontab.
- A crontab is a file that contains a list of commands to be executed at specified intervals. It uses the cron daemon to schedule and run these jobs.
**Configure a job:**
- Edit the crontab file using crontab -e.
- Add a line with the format: * * * * * command_to_run, where the five asterisks represent minute, hour, day of month, month, and day of week, respectively.
- Save the file to schedule the job.


#### How do you allow ports in Linux?
- Use firewall management tools like iptables or firewalld:
- With iptables: iptables -A INPUT -p tcp --dport port_number -j ACCEPT.
- With firewalld: firewall-cmd --add-port=port_number/tcp --permanent followed by firewall-cmd --reload.


#### How do you troubleshoot a remote server that is experiencing issues?
- Check Connectivity: Use ping, traceroute, or telnet to test network connectivity.
- Check Logs: Examine system and application logs for errors.
- Resource Utilization: Use commands like top, free, df, and du to check resource usage.
- SSH Access: Ensure you can SSH into the server and verify service statuses with systemctl or service.


#### What are the ping, telnet, curl, and wget commands in Linux?
- ping: Tests network connectivity to a host.
- telnet: Connects to a specific port on a remote host to test connectivity.
- curl: Transfers data to or from a server using various protocols (e.g., HTTP, FTP).
- wget: Downloads files from the web using HTTP, HTTPS, or FTP.


#### How can you check the status of services in a Linux machine?
Use systemctl status service_name or service service_name status for services managed by systemd or SysVinit, respectively.

#### do you kill a process in Linux?
- Use the kill command with the process ID (PID): kill PID.
- For more forceful termination, use kill -9 PID.


#### What are the nice and renice commands in Linux?
- nice: Starts a process with a specified priority level (niceness). Example: nice -n 10 command.
- renice: Changes the priority of an already running process. Example: renice -n 10 -p PID.


#### What is an inode in Linux?
An inode is a data structure on a filesystem that stores information about a file or directory, such as its size, owner, permissions, and disk location, but not its name.

#### How do you check CPU utilization in Linux?
Use commands like top, htop, or mpstat (from the sysstat package) to view CPU usage statistics.


#### What are the differences between the top and htop commands?
- top: Provides a text-based interface for monitoring system processes and resource usage.
- htop: An enhanced, interactive version of top with a more user-friendly interface, color-coding, and the ability to scroll through the process list.


#### What is a mount in Linux, and how do you create one?
- A mount is the process of making a filesystem accessible at a specific directory in the existing filesystem tree. To create one:
- Use the mount command: mount /dev/device /mount_point.

#### How do you troubleshoot live logs in Linux?
- Use commands like tail -f /path/to/logfile to view real-time log updates.
- Check logs in directories like /var/log/ for system and application logs.

#### What is the sed command in Linux?
sed (stream editor) is used for parsing and transforming text from input streams or files. Example: sed 's/old/new/g' file replaces all occurrences of "old" with "new".

#### What is the awk command in Linux?
- awk is a text-processing tool used for pattern scanning and processing. It can perform operations on text files and data streams. - -Example: awk '{print $1}' file prints the first field of each line.

#### What are the grep and egrep commands in Linux?
- grep: Searches for patterns within files. Example: grep 'pattern' file.
- egrep: An extended version of grep that supports extended regular expressions.

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
- $?: The exit status of the last executed command.
- $#: The number of positional parameters passed to the script.
- $*: All the positional parameters passed to the script as a single string.

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


#### 6. How do you set up Apache on a Linux server?
Answer:
- Update the package index using sudo apt-get update (Debian/Ubuntu) or sudo yum update (RHEL/CentOS).
- Install Apache with sudo apt-get install apache2 or sudo yum install httpd.
- Start the Apache service using sudo systemctl start apache2 or sudo systemctl start httpd.
- Enable Apache to start on boot using sudo systemctl enable apache2 or sudo systemctl enable httpd.
- Verify the installation by accessing the server's IP address in a web browser.

#### 7. What are the steps to convert HTTP to HTTPS?
Answer:
- Obtain an SSL certificate from a trusted Certificate Authority (CA).
- Install the SSL certificate on the web server (Apache/Nginx).
- Update the web server configuration to redirect HTTP traffic to HTTPS by modifying the server block and enabling the mod_ssl module (Apache) or configuring SSL in the server block (Nginx).
- Test the configuration by accessing the site via HTTPS.
- Optionally, update DNS settings if required.





# Linux
#### What is Linux?
Linux is an open-source operating system kernel initially developed by Linus Torvalds. It forms the core of many Linux distributions, which are complete operating systems including the Linux kernel along with applications, utilities, and libraries

#### Who invented Linux? Explain the history of Linux?
Linux was invented by Linus Torvalds in 1991 while he was a student at the University of Helsinki, Finland. Torvalds developed Linux as a hobby project, inspired by Unix and aiming to create a free and open-source Unix-like operating system kernel.

#### What is the difference between Linux and Unix?
Linux is a Unix-like operating system kernel, not Unix itself. Unix refers to a family of multitasking, multi-user computer operating systems originally developed in the 1970s. Linux is Unix-like in that it follows Unix principles and is POSIX-compliant, but it is not derived from the original Unix codebase.

#### What is the core of the Linux operating system?
The core of the Linux operating system is the Linux kernel. It manages hardware resources and provides essential services for all other parts of the operating system.

#### What is Linux Kernel?
The Linux kernel is the core component of the Linux operating system. It manages system resources, including CPU, memory, and devices, and provides low-level functionalities required for higher-level software to run.

#### What is BASH?
BASH (Bourne Again SHell) is the default command-line interpreter or shell for most Linux distributions. It provides a command-line interface (CLI) to interact with the operating system, execute commands, and automate tasks through shell scripting.

#### What is LILO?
LILO (LInux LOader) was one of the first boot loaders used in Linux distributions. It loaded the Linux kernel into memory during the boot process from a hard disk. It has largely been replaced by GRUB (GRand Unified Bootloader) in modern Linux distributions.

#### What is CLI?
CLI stands for Command-Line Interface. It is a text-based interface used to interact with the operating system by typing commands. Linux systems typically provide multiple command-line shells, such as BASH, Zsh, and Tcsh.

#### What is the advantage of Open Source?
- Advantages of open source software include:
- Transparency and auditability of code.
- Flexibility to modify and customize software.
- Community-driven development and support.
- Cost-effectiveness (often free to use).
- Reduced vendor lock-in.

#### What is the disadvantage of Open Source?
- Disadvantages of open source software may include:
- Limited or fragmented support compared to commercial software.
- Potential for security vulnerabilities if not actively maintained.
- Higher learning curve for users unfamiliar with open source tools.
- Integration challenges in heterogeneous environments.

#### What is Shell? 
It seems there might be a typo in your question. If you meant "What Shell is," it refers to the type of command-line interpreter or shell being used in Linux, such as BASH, Zsh, or others.

#### How many types of Shells are there in Linux?
- There are several types of shells in Linux, including:
- BASH (Bourne Again SHell): Most common and default on many Linux distributions.
- Zsh (Z Shell): Offers more features and customization options compared to BASH.
- Fish: User-friendly with features like autosuggestions and syntax highlighting.
- Ksh (KornShell): Enhanced version of the original Unix Shell (sh).
- Tcsh/Csh: C-like syntax and command-line editing features.

#### What are the basic components of Linux?
- The basic components of Linux include:
- Kernel: Manages system resources and interfaces with hardware.
- Shell: Provides command-line interface for user interaction.
- Filesystem: Organizes and stores data on storage devices.
- Utilities: Essential tools and commands for system management and administration.
- Libraries: Collections of precompiled routines that applications can use.

#### How do you open a command prompt when issuing a command?
- To open a command prompt (terminal) in Linux and issue commands:
- Use a terminal emulator application like GNOME Terminal, Konsole, or xterm.
- Press Ctrl + Alt + T on the keyboard (default shortcut for many desktop environments).
- Use the Terminal application in the applications menu of your Linux desktop environment.

#### What is a swap space?
Swap space (or swap) in Linux is a reserved area on a storage device (usually a hard disk or SSD) that the operating system uses as virtual memory when physical RAM is fully utilized. It allows the system to swap out less frequently used memory pages to free up RAM for more active processes.

#### What is the GUI?
GUI stands for Graphical User Interface. It is a visual way for users to interact with the operating system and applications, using icons, windows, menus, buttons, and other graphical elements.

#### Explain File Permissions types in Linux?
- In Linux, file permissions are represented by three types of permissions:
- Read (r): Allows reading/viewing the contents of a file or directory.
- Write (w): Allows modifying the contents of a file or directory.
- Execute (x): Allows executing (running) a file if it is a program or script.
- Permissions are set for three categories of users: owner, group, and others, with different combinations of these permissions (e.g., rwx, rw-, r--) controlling access.

#### What are environmental variables?
Environmental variables in Linux are dynamic named values that define the operating environment for processes running on the system. They can influence how processes behave and interact with the system and are often used in shell scripting and configuration.

#### What are symbolic links?
Symbolic links (symlinks or soft links) in Linux are pointers to files or directories. They act like shortcuts in Windows, providing a convenient way to reference files or directories without duplicating content. Unlike hard links, symbolic links can span across different filesystems.

#### What are hard links?
Hard links in Linux are directory entries that point to the same underlying inode (data structure representing a file) as another file or directory. They provide multiple filenames (hard links) for a single file, allowing efficient file management and saving disk space.

#### What is redirection?
Redirection in Linux refers to directing the input or output of a command to/from a file, device, or another command. It allows manipulating standard input (stdin), standard output (stdout), and standard error (stderr) streams.

#### What are Daemons?
Daemons in Linux are background processes or services that run continuously, performing various system tasks or waiting for requests to handle. They often start during system boot and continue running until the system is shut down

#### Describe the root account?
The root account in Linux is the administrative account with full access to all files, commands, and system resources. It has unrestricted privileges, including the ability to modify system-critical files, install software, and manage users.

#### Explain the virtual desktop?
A virtual desktop in Linux refers to multiple independent desktop environments or workspaces that users can switch between. It allows organizing and managing different sets of applications and windows, providing a more organized and productive user experience.

#### What are the different modes when using the vi editor?
- In the vi editor (and its improved version, vim), there are different modes:
- Normal mode: Used for navigating and executing commands.
- Insert mode: Used for inserting or editing text.
- Visual mode: Used for selecting blocks of text.
- Command-line mode: Used for entering editor commands like saving or quitting.

#### What are inode and process id?
- Inode: In Linux, an inode is a data structure that stores metadata about a file or directory, excluding its name and actual data. It -includes information like file size, permissions, timestamps, and pointers to data blocks.
- Process ID (PID): PID is a unique identifier assigned to each running process in the Linux system. It allows the operating system to manage and control processes, including allocating resources and terminating them.

#### What are the Process states in Linux?
- Processes in Linux can be in several states:
- Running: Actively executing on a CPU core.
- Sleeping: Waiting for an event or condition to complete (e.g., I/O operation).
- Stopped: Suspended or paused, often due to signals or debugging.
- Zombie: Terminated, but its parent process has not yet read its exit status.
- Uninterruptible sleep: Waiting for a resource that cannot be interrupted by signals.

#### Explain Process Management System Calls in Linux?
Process management system calls in Linux are API functions that allow programs to manage processes. Examples include fork() to create new processes, exec() to replace the current process image, wait() to wait for child processes to terminate, and kill() to send signals to processes.

#### Explain File Permission groups in Linux?
In Linux, file permissions are grouped into three

#### What Is a File system in Linux?
A file system in Linux is a method for storing and organizing files on a storage device (like a hard disk or SSD). It defines how data is stored, retrieved, and managed. Linux supports various file systems, each with its own features and optimizations.

#### Explain different file system types in Linux?
- Common file system types in Linux include:
- **ext4:** Default file system for most Linux distributions, offering features like journaling, extended file attributes, and large file system support.
- **ext3:** An earlier version of ext4 with journaling support.
- **XFS:** High-performance file system with scalability and advanced features like support for large files and metadata.
- **Btrfs:** Modern file system with features like snapshots, checksums, and support for multiple devices (RAID).
- **FAT32:** File Allocation Table file system suitable for compatibility with Windows and other operating systems.
- **NTFS:** New Technology File System used by Windows, with read/write support in Linux through third-party drivers.
- **ZFS:** Advanced file system with built-in data integrity, snapshotting, and RAID-like features (not native to Linux but available through third-party implementations).

#### Why LVM is required?
LVM (Logical Volume Manager) is required in Linux for flexible storage management. It allows administrators to create, resize, and move logical volumes (similar to partitions) dynamically, without needing to shut down the system or lose data. LVM provides features like snapshots and thin provisioning, making storage management more efficient.

#### What is umask?
umask is a command and a file mode creation mask in Linux that determines the default permissions of newly created files and directories. It subtracts from the maximum permissions (typically 666 for files and 777 for directories), specifying which permissions should be disabled by default.

#### How to set the mask permanently for a user?
- To set umask permanently for a user:
- Open the user's shell configuration file (e.g., ~/.bashrc for BASH).
- Add or modify the umask command to set the desired mask.
- Save the file and either log out and log in again or use source ~/.bashrc to apply the changes immediately.
- Example:echo "umask 022" >> ~/.bashrc
- source ~/.bashrc

#### What is network bonding in Linux?
Network bonding (or NIC bonding) in Linux is a technique that allows combining multiple network interfaces (NICs) into a single logical bonded interface. It provides fault tolerance and high availability by ensuring network connectivity even if one NIC or network link fails.

#### What are the different modes of Network bonding in Linux?
- Different modes of network bonding in Linux include:
- Mode 0 (Balance-rr): Round-robin load balancing without aggregation.
- Mode 1 (Active-backup): Active-passive failover configuration.
- Mode 2 (Balance-xor): XOR hashing of source and destination MAC addresses.
- Mode 3 (Broadcast): Sends all traffic down all slave interfaces.
- Mode 4 (802.3ad or LACP): Dynamic link aggregation using the IEEE 802.3ad protocol.
- Mode 5 (Balance-tlb): Adaptive transmit load balancing.
- Mode 6 (Balance-alb): Adaptive load balancing, combining balance-tlb and receive load balancing.

#### How to check the default route and routing table?
- To check the default route and routing table in Linux:
- Use the ip route show command to display the routing table, including the default route.
- Alternatively, use route -n or netstat -nr for older Linux distributions.

#### How to check which ports are listening in my Linux Server?
- To check which ports are listening on your Linux server:
- Use the netstat command with the -tuln or -tulnp options to display listening TCP (-t) and UDP (-u) ports along with their numeric (-n) and process (-p) information.
- Example: netstat -tulnp

#### Where are kernel modules located?
Kernel modules (.ko files) in Linux are located in the /lib/modules/{kernel-version}/kernel/ directory. Each kernel version has its own directory containing modules specific to that kernel version.

#### How to change the default run level in Linux?
- In Linux, run levels determine the state of the system and which services are started. To change the default run level:
- Edit the /etc/inittab file or use the systemctl command (for systemd-based distributions) to set the default target.
- Example (for systemd): systemctl set-default multi-user.target
- This sets the default run level to multi-user mode (similar to run level 3 in traditional init systems).

#### How to share a directory using NFS?
- To share a directory using NFS (Network File System) in Linux:
- Install NFS server packages (nfs-kernel-server on Debian/Ubuntu, nfs-utils on Red Hat/CentOS).
- Edit the NFS exports file (/etc/exports) to define the directory to be shared and the access permissions.
- Export the directory using the exportfs command.
- Start or restart the NFS server (systemctl restart nfs-server or service nfs-server restart).
- Configure firewall rules if necessary (ufw or firewalld) to allow NFS traffic.
- Example /etc/exports entry: /shared_directory   *(rw,sync,no_root_squash)



#### How to lock a user account in Linux?
- To lock a user account in Linux, you can use the passwd command with the -l option:
- sudo passwd -l username
- This locks the specified user account (username). Locked accounts prevent the user from logging in.

#### What is the ‘ls’ command and what does it do?
- The ls command in Linux lists directory contents:
- Without options, ls lists files and directories in the current directory.
- Common options include -l (long format), -a (show hidden files), -h (human-readable sizes), etc.

#### What is the tail command in Linux?
- The tail command displays the last part of a file:
- By default, tail shows the last 10 lines of a file.
- Options like -n can be used to specify the number of lines (-n 20 for example).
- -f option can be used to follow (tail -f) the output of a file in real-time.
- Example: tail -n 20 filename.log

#### What is grep command in Linux?
- The grep command searches for patterns in files:
- It prints lines matching a specified pattern or regular expression from one or more files.
- Options like -i (ignore case), -r (recursive), -v (invert match), etc., enhance its functionality.
- Example: grep "pattern" filename

#### What is ps command in Linux?
- The ps command shows information about processes:
- Without options, ps lists processes running in the current terminal session.
- Options like -ef (all processes), -aux (all processes with more details), -u (specific user processes), etc., provide different views.
- Example: ps -aux

#### What is the env command in Linux?
- The env command runs a command in a modified environment:
- It prints the current environment or runs a command with specified environment variables.
- Useful for setting temporary environment variables or checking the environment before executing a script.
- Example: env

#### What is the top command in Linux?
- The top command displays real-time system resource usage:
- It shows information such as CPU usage, memory usage, running processes, load averages, etc.
- Interactive and updates continuously until you exit.
- Example: top

#### What is netstat command in Linux?
- The netstat command displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships:
- It prints network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
- Options like -t (TCP connections), -u (UDP connections), -l (listening ports), -r (routing table), etc., specify the type of information to display.
- Example: netstat -tuln

#### What is lsof command in Linux?
- lsof stands for "list open files".
- It is used to list all open files and the processes that opened them.
- It can also list network connections (lsof -i) and files opened by a specific user (lsof -u username).
- Example: lsof -i :80   # List processes using port 80

#### Explain about chmod command?
- chmod stands for "change mode".
- It is used to change the file or directory permissions in Linux.
- Permissions can be changed using symbolic (+/- permissions) or octal (numeric) modes.
- Example: chmod +x filename   # Add execute permission to file

#### Explain about chown command?
- chown stands for "change owner".
- It is used to change the owner and/or group of a file or directory in Linux.
- Example: chown user:group filename   # Change owner and group of file

#### What is the cp command in Linux?
- cp stands for "copy".
- It is used to copy files or directories in Linux.
- Syntax: cp source destination
- Example: cp file1.txt file2.txt   # Copy file1.txt to file2.txt

#### How to remove a file or directory from the system in Linux?
- To remove a file: rm filename
- To remove an empty directory: rmdir directory
- To remove a directory and its contents recursively: rm -r directory
- Example: rm file.txt

#### What is mkdir in Linux?
- mkdir stands for "make directory".
- It is used to create new directories in Linux.
- Example: mkdir directory_name

#### Explain rmdir command in Linux?
- rmdir stands for "remove directory".
- It is used to remove empty directories in Linux.
- Example: rmdir directory_name

#### How to exit from vi editors?
- To exit vi editor:
- Press Esc key to ensure you are in command mode.
- Type :q to quit without saving changes.
- Type :wq to save changes and quit.
- Type :q! to force quit without saving changes.
- Example: :q    # Quit vi editor

#### How to delete information from a file in vi?
- To delete text in vi editor:
- Press Esc key to switch to command mode.
- Move the cursor to the line or characters you want to delete.
- Press dd to delete the current line.
- Use x to delete the character under the cursor.
- Example: dd    # Delete current line

#### Enlist some Linux file content commands?
- Commands to view file contents in Linux:
- cat: Display file contents.
- head: Display first few lines of a file.
- tail: Display last few lines of a file.
- more or less: View file contents page by page.
- grep: Search for patterns in files.
- Example: cat file.txt

#### Enlist some Linux distributors (Distros) along with their usage?
- Popular Linux distributions:
- Ubuntu: General-purpose, user-friendly.
- CentOS: Enterprise-grade, stable, used for servers.
- Debian: Stable, community-driven, versatile.
- Fedora: Rapid updates, bleeding-edge features.
- Red Hat Enterprise Linux (RHEL): Commercial, for enterprise use.
- Arch Linux: Rolling-release, minimalistic, for advanced users.
- Linux Mint: User-friendly, based on Ubuntu.
- openSUSE: Stable, suitable for desktops and servers

#### Why we use LINUX?
- Reasons for using Linux:
- Open-source nature.
- Security and stability.
- Customizability and flexibility.
- Rich command-line interface.
- Wide range of distributions for different use cases.
- Community support and large software ecosystem.

#### What are the features of the Linux operating system?
- **Features of Linux:**
- Multi-user capability.
- Multi-tasking support.
- Security with permissions and user management.
- Networking capabilities.
- Portability across different hardware architectures.
- Scalability from embedded devices to supercomputers.
- Open-source software model.
- Command-line interface and scripting support.

#### Differentiate between BASH and DOS?
- **BASH (Bourne Again SHell):**
- Default shell in most Linux distributions.
- Rich set of features like scripting, variables, functions.
- Case-sensitive.
- Supports piping and redirection extensively.
- **DOS (Disk Operating System):**
- Command-line interface for older Microsoft operating systems.
- Not as feature-rich as BASH.
- Case-insensitive.
- Limited scripting capabilities.

#### What is meant by internal commands and external commands?
- **Internal commands:**
- Commands that are built into the shell (e.g., cd, echo in BASH).
- Executed directly by the shell itself.
- **External commands:**
- Commands that exist as separate executable files (e.g., /bin/ls, /usr/bin/grep).
- Executed by creating a new process by the shell.

#### What is meant by PIPE in Linux?
- PIPE (|):
- A way to chain commands in Linux.
- Redirects the output of one command as input to another command.
- Allows for complex command-line operations.
- Example: ls -l | grep "file"

#### Describe how a parent and child process communicate with each other?
- Parent and child processes:
- Parent process creates child processes using fork() system call.
- Communication can occur via shared memory, pipes, signals, or files.
- IPC (Inter-Process Communication) mechanisms like pipe(), socket(), or message queues are used.
- Examples include passing data through standard input/output or using explicit IPC mechanisms.

#### What is a Stateless Linux Server?
- A stateless Linux server:
- Does not retain any local state or data.
- Uses network storage or cloud storage for all data.
- Can be easily replaced or scaled horizontally.
- Configuration and application data are managed centrally.

#### Explain the features of Stateless Linux Server?
- Features of Stateless Linux Server:
- Simplified management and deployment.
- Enhanced security due to lack of persistent data.
- Scalability and resilience in cloud environments.
- Reduced maintenance overhead.
- Ideal for environments requiring rapid deployment and automation.

#### What is Zombie Process?
**Zombie Process:**
- A process that has completed execution but still has an entry in the process table.
- It is terminated but its entry remains until its parent process calls wait() or waitpid() system call to read its exit status.
- Zombies consume system resources until they are removed.
- Usually, handled automatically by the operating system.

#### Explain the work of the Ctrl+Alt+Del key combination on the Linux operating system?
In Linux, the Ctrl+Alt+Del key combination is typically used to initiate a system reboot. When pressed, it sends a reboot signal to the system, which will start the shutdown process and then reboot the system.

#### Why is Linux considered more secure than other operating systems?
- Linux is considered more secure than other operating systems due to several factors:
- Open Source: Transparency allows for peer review and quick fixes.
- Permissions: Strong user and file permissions system.
- Security Modules: Supports various security modules like SELinux and AppArmor.
- Updates: Regular security updates and patches.
- Limited Privileges: Services run with limited privileges by default.
- Community Support: Active community and quick responses to security vulnerabilities.

#### What is the tail command in Linux?
- The tail command in Linux is used to display the last part of a file.
- Syntax: tail [options] filename
- Example: tail -n 10 file.txt   # Display the last 10 lines of file.txt

#### What is the cat command in Linux?
- The cat command in Linux is used to concatenate and display the contents of files.
- Syntax: cat [options] filename
- Example: cat file.txt   # Display contents of file.txt

#### What is the grep command in Linux?
- The grep command in Linux is used to search for patterns in files or input streams.
- Syntax: grep [options] pattern [filename]
- Example: grep "error" logfile.txt   # Search for lines containing "error" in logfile.txt


#### What is ps command in Linux?
- The ps command in Linux is used to display information about running processes.
- Syntax: ps [options]
- Example: ps aux   # Display a detailed list of all running processes

#### What is the env command in Linux?
- The env command in Linux is used to display the current environment variables or run a command in a modified environment.
- Syntax: env [options] [command]
- Example: env   # Display all environment variables
- env PATH=/bin:/usr/bin ls   # Run `ls` command with modified PATH

#### What is the top Command in Linux?
- The top command in Linux is used to display dynamic real-time information about running processes and system resource usage.
- It provides a task manager-like interface showing CPU, memory, and other system information.
- Example: top   # Display real-time system usage statistics

#### What is the netstat command in Linux?
- The netstat command in Linux is used to display network connections, routing tables, interface statistics, masquerade connections, - -and multicast memberships.
- Syntax: netstat [options]
- Example:netstat -tulpn   # Display listening TCP and UDP connections with PIDs

#### What is the lsof command in Linux?
- The lsof command in Linux is used to list open files, including files opened by processes.
- It can also list network connections and various types of files opened by a specific user.
- Example:lsof -i :80   # List processes using port 80

#### What is the df command in Linux?
- The df command in Linux is used to display disk space usage of file systems.
 -             Syntax: df [options]
 -            Example: df -h   # Display disk space usage in human-readable format

#### What is the du command in Linux?
- The du command in Linux is used to estimate file space usage.
-             Syntax: du [options] [file or directory]
- Example: du -sh *   # Display total disk usage of files and directories in current directory

#### What is the iptables command in Linux?
- The iptables command in Linux is used to set up, maintain, and inspect the tables of IP packet filter rules in the Linux kernel's firewall.
- It is used to configure IPv4 packet filtering and NAT (Network Address Translation).
- Example: iptables -A INPUT -p tcp --dport 80 -j ACCEPT   # Allow incoming TCP traffic on port 80

#### What is the difference between Linux and Windows?
- **Linux:**
- Open-source operating system.
- Supports multiple desktop environments (GNOME, KDE, etc.).
- Command-line interface (CLI) driven with powerful shell scripting.
- Security features like permissions, SELinux, etc.
- **Windows:**
- Proprietary operating system from Microsoft.
- GUI-centric with Command Prompt and PowerShell.
- More widely used in desktop environments.
- Integrated with Microsoft ecosystem

#### What does the cd - command do?
- The cd - command in Linux changes the working directory to the previous directory you were in.
- It toggles between the current and the previous directory.
- Example: cd /var/log
- cd -

#### What does cd command do?
- The cd command in Linux is used to change the current working directory.
- Syntax: cd [directory]
- Example: cd /home/user   # Change directory to /home/user

#### What does (cd dir && command) do?
- (cd dir && command) is a shell command that changes the directory temporarily (cd dir) and then executes a command (command) in that directory.
- It ensures that command is executed in the context of the specified directory (dir) without permanently changing the current working directory.

#### What does pushd command do?
- The pushd command in Linux is used to push the current directory onto the directory stack and change to the specified directory.
- It allows easy navigation between directories using the directory stack.
- Example: pushd /var/log   # Push /var/log onto stack and change to /var/log

#### What is ls -lSr command?
- ls -lSr is a combination of options for the ls command in Linux.
- -l: Long listing format to display detailed information about files.
- -S: Sort files by size, largest file first.
- -r: Reverse the order of sorting.
- Example: ls -lSr   # List files in long format, sorted by size in descending order

#### What is du -s * | sort -k1,1rn | head command used for?
- du -s * | sort -k1,1rn | head is a command pipeline in Linux.
- du -s *: Displays total disk usage (du) of each file and directory (*) in the current directory.
- sort -k1,1rn: Sorts the output by the first field (-k1) numerically (n) in reverse order (r).
- head: Displays the first few lines of the sorted output.
- Example: du -s * | sort -k1,1rn | head   # Display top disk usage files and directories in current

#### What does this du -hs /home/* | sort -k1,1h command do?
- du -hs /home/*: Displays the disk usage (du) of each directory (/home/*) in a human-readable (-h) format and summarizes (-s) the total usage.
- |: Pipe symbol, redirects the output of the du command to the sort command.
- sort -k1,1h: Sorts (sort) the output by the first field (-k1) in a human-readable (-h) format, which sorts numbers with unit suffixes appropriately (like KB, MB).

#### What is df -h command?
- df -h command is used to display disk space usage of all mounted file systems in a human-readable format.
- -h: Display sizes in a human-readable format (e.g., MB, GB).
- Example: df -h   # Display disk space usage of all mounted file systems

#### What is df -i command?
- df -i command is used to display inode usage information for all mounted file systems.
- -i: Display information about file system inodes.
- Example: df -i   # Display inode usage information for all mounted file systems

#### What is fdisk -l command used for?
- fdisk -l command is used to list all partitions on a disk.
- -l: List the partition table for the specified device(s) and exit.
- Example: fdisk -l /dev/sda   # List partitions on the disk /dev/sda

#### How do you kill the program using one port in Linux?
- To kill a program using a specific port in Linux, you can use the lsof and kill commands together.
```
lsof -i :<port_number>   # Find the PID (Process ID) of the program using the port
kill -9 <PID>            # Kill the process using the PID
Replace <port_number> with the actual port number (e.g., 8080) and <PID> with the Process ID obtained from lsof command
```
#### How do you limit memory usage for commands?
- You can limit memory usage for commands using the ulimit command.
```
ulimit -v <memory_limit_in_kilobytes>   # Limit virtual memory usage
```
- This sets a maximum limit on the amount of virtual memory that can be used by subsequent commands in the current shell session.

#### How do you get the full path of a file in Linux?
- Use the realpath command to get the full canonicalized path of a file.
```
realpath /path/to/file   # Display the full path of the file
```
#### How do you list the contents of tar.gz and extract only one file?
- To list contents of a .tar.gz file: tar -tzf archive.tar.gz   # List contents of the tar.gz archiv
- To extract only one file from a .tar.gz archive: tar -xzf archive.tar.gz path/to/file   # Extract specific file from tar.gz archive

#### How do you find who is logged in?
- Use the who command to display information about users who are currently logged in.
- who   # Display who is logged in

#### How do you check the permissions of each directory to a file? -
- Use the ls command with -l option to display detailed file and directory permissions.
- ls -l   # Display permissions for files and directories in the current directory

#### How do you run the command every time a file is modified?

- You can use inotifywait command along with a loop to achieve this.
```
while inotifywait -e modify file.txt; do
    # Command to run when file.txt is modified
    echo "File modified!"
done
```
#### How to copy text to the clipboard?
- You can use xclip or xsel commands to copy text to the clipboard in Linux.
```
     echo "Text to copy" | xclip -selection clipboard
```
#### How do you check resources usage?
- Use commands like top, htop, free, vmstat, or sar to check resource usage (CPU, memory, disk, etc.) in Linux.
- top   # Display real-time system resource usage

#### How do you run a command for a limited time?
- Use the timeout command to run a command for a specified duration.
- timeout 10s command   # Run 'command' for 10 seconds

#### How do you combine two lines from two sorted files in Linux?
-  Use paste command to merge lines from two files side by side.
- paste file1.txt file2.txt   # Combine lines from file1.txt and file2.txt




#### What is realm command?
realm is a command-line tool used to manage and configure Kerberos realms and other related security realms on Linux systems, often used to join a Linux machine to an Active Directory domain.

#### What type of Linux machine do you use most frequently?
I frequently use Ubuntu for development and Amazon Linux for AWS environments. Both are popular choices for their stability and compatibility with various tools.

#### How do you check disk space in Linux? What command do you use?
To check disk space, I use the df -h command, which displays disk space usage in a human-readable format.

#### What command do you use in Linux to check CPU utilization?
To check CPU utilization, I use the top or htop command. Alternatively, mpstat from the sysstat package provides detailed CPU usage statistics.

#### HHow do you manage services and applications on a Linux server?
On a Linux server, I manage services using systemd commands like systemctl start/stop/restart/status <service>. Applications can be managed using package managers like apt for Debian-based systems or yum for Red Hat-based systems. I also use SSH for remote management and configuration files to control application settings.

#### In Linux, do you know what hard links and soft links are?
"Yes, hard links point to the same inode on the filesystem, meaning they reference the same file data. Soft links, or symbolic links, are pointers to another file or directory, which can be on different filesystems and have different inode numbers."

#### How will you create a user in Linux? Now make that user a Sudo user. How will you do that?
"To create a user, you can use the useradd command. For example: sudo useradd newuser. To set a password: sudo passwd newuser. To make the user a sudo user, you would add them to the sudo group: sudo usermod -aG sudo newuser."

#### Suppose you have an EC2 server in which Linux is running and you get an alert that your server's disk space utilization has gone above 90%. How will you troubleshoot it?
"I would use commands like df -h to check disk usage and du -sh /* to identify large directories. I’d also review logs and remove unnecessary files or directories."

#### How will you find out the top 10 files that are occupying the most space?
"Use the command du -ah / | sort -rh | head -n 10 to list the top 10 largest files and directories."



#### Do you know how to run cron jobs on a Linux server?
"Yes, you can use the crontab command to schedule cron jobs. Edit the crontab with crontab -e and add the job with the appropriate schedule and command."

#### In Linux, how do you change the permissions of files?
"Use the chmod command to change file permissions. For example, chmod 755 file.txt sets read, write, and execute permissions for the owner, and read and execute permissions for others."

#### How do you change the ownership of files in Linux?
"Use the chown command. For example, chown user:group file.txt changes the owner and group of the file."




