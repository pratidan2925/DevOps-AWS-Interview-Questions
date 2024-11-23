Linux

What is Linux
Linux is an open-source operating system kernel developed by Linus Torvalds in 1991. It's the core component of various Linux distributions (or distros) such as Ubuntu, Fedora, and Debian. Linux is known for its stability, security, and flexibility, making it popular for use in servers, desktop computers, mobile devices, and embedded systems. It supports a wide range of software and is highly customizable to meet different needs.

how to give permission to Linux ?  And What is chmod ?
"chmod" is a command in Linux used to change permissions for files and directories. It allows you to specify who can read, write, or execute a file or directory. You can use symbolic or octal notation to set permissions. For example, chmod u+x file.txt adds execute permission for the owner of "file.txt", while chmod 755 file.txt gives the owner full permissions and read/execute permissions to the group and others.
Read -  4                  	write - 2                               	execute - 1
 
777 in Linux
In Linux, "777" is a file permission notation representing full read, write, and execute permissions for the owner, group, and others.
 
Which Linux  and Windows version do you use?
linux :
Ubuntu 18.x  -- decamped /not in use for  5/6 months.
Ubuntu 22.04  –  Recently used.
Ubuntu 24.04  -- latest version – recently used.
Windows : 
2019 -recently used .
2022- latest version
Note : Company never goeson latest version ,as it may have issues. So they always use one     version older than the latest version .
 
What is the key difference  between Linux server and ubuntu server?
Linux Server: "Linux server" refers to any server operating system based on the Linux kernel. It's a broad term encompassing various distributions (distros) like Ubuntu Server, CentOS, Debian, Fedora, etc. Each distribution may have its own package management system, default software, and support policies.
Ubuntu Server: Ubuntu Server is a specific distribution of Linux tailored for server environments. It's maintained by Canonical and is based on the Debian architecture. Ubuntu Server is known for its ease of use, regular updates, strong community support, and compatibility with a wide range of software packages. It's often chosen for web servers, cloud deployments, and enterprise applications.
In essence, while "Linux server" is a generic term referring to any server running a Linux-based operating system, "Ubuntu server" specifically denotes a server running the Ubuntu distribution of Linux.
 
What is thread in Linux
In Linux, a thread is a basic unit of execution within a process, capable of running tasks concurrently with other threads. They share the same memory and resources as their parent process, enabling efficient multitasking and parallel processing within applications.

What is a zombie process in Linux?
In short, a zombie process in Linux is a terminated process that still has an entry in the process table because its parent process hasn't yet acknowledged its termination.

Explain Grep command.
The grep command in Unix/Linux is used to search for specific patterns within files. It stands for "Global Regular Expression Print". grep is a powerful tool for searching through text files and displaying lines that match a given pattern.
 
What is etc  folder ?
The /etc folder is a key part of Linux and other Unix-like systems. It's where the system keeps important settings and configuration files.
·         Stores Settings: This folder holds configuration files that control how the system and various programs behave.
·         System-Wide Impact: Changes in this folder affect the whole system, not just one user.
 
Difference Between YUM and APT
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


 How to get info for all the packages installed on Linux system
yum list installed
apt list –installed

How to check the kernel version in Linux
uname -r -- This command will output the kernel version.
cat /proc/version -- This command will display the kernel version along with additional information about the build
 hostnamectl -- This command will display the kernel version along with additional information about the build

 Explain Linux distribution
A Linux distribution, often referred to as a "distro," is a complete operating system built on the Linux kernel along with a collection of software applications, libraries, and utilities.
Examples of popular Linux distributions include Ubuntu, Fedora, Debian, CentOS, Arch Linux, and openSUSE. Each distribution may target specific use cases, such as general-purpose desktops, servers, embedded systems, or specialized applications.

How to backup a Linux server?
To back up a Linux server, there are several methods you can use, depending on the requirements and the environment. Some of the most common methods include using rsync, tar, dd, rsnapshot, Bacula, and Duplicity
 rsync: Efficient for file synchronization and backups.
tar: Creates compressed archive files.
dd: For full disk backups.
Automation with cron: Schedule regular backups.
Advanced Tools:
rsnapshot: For incremental backups.
Bacula and Duplicity: For more complex needs, including encryption and remote backups.


how to check running processes in linux /what is the use of ps-aux in linux /what is Top command & its uses.
top Command
Displays real-time system summary and list of processes.
Ps-aux Command
Displays information about active processes.
a: Displays processes from all users.
u: Shows detailed user-oriented format.
x: Includes processes without a controlling terminal.

How to check system load in linux
top Command
Displays real-time information about system processes, including system load.
Load average: Displayed at the top of the screen, shows system load over the last 1, 5, and 15 minutes.


What is the Inode number ?
An inode number is a unique identifier assigned to each file or directory in a Unix-based file system, like Linux. It helps the operating system keep track of file attributes and locate files efficiently. It's like a fingerprint for each file or directory.


What is Nginx?
Nginx is a popular web server software used to host websites and serve web content on the internet. It's like a traffic cop for the internet, directing web traffic to the right places. Nginx is known for its speed and efficiency, handling large volumes of web traffic with ease. It's commonly used as a reverse proxy, load balancer, and HTTP cache, making websites faster and more reliable. In simple terms, Nginx helps websites run smoothly and handle lots of visitors without slowing down.

What is Cron job in Linux
A cron job is a task scheduled to run at specific times or intervals on a Unix-based system like Linux. You can use the cron utility to schedule repetitive tasks, such as running scripts, executing commands, or performing system maintenance, automatically without manual intervention.

What is the nslookup command ?
The "nslookup" command is a network utility used in Unix-like operating systems to query DNS (Domain Name System) servers for various types of DNS records. It allows you to obtain information about domain names, IP addresses, and other DNS-related records.

How to Start a Linux server. nr Start-ds
 To start a Linux server, boot it up either from a virtual machine manager or by pressing the power button if it's a physical server. Then, log in using SSH or a remote desktop connection. Finally, verify that essential services are running and check the server's status.
Use commands like uptime or systemctl status to verify its status.

Explain Grep vs sed command
 Grep:
Purpose: Searches for patterns within text.
Functionality: Prints lines that match a specified pattern.
Usage Example: grep 'error' logfile.txt - Finds and displays lines containing "error" in logfile.txt.
Sed:
Purpose: Stream editor for modifying text.
Functionality: Performs find-and-replace, text transformation, and filtering.
Usage Example: sed 's/error/success/' logfile.txt - Replaces the first occurrence of "error" with "success" in each line of logfile.txt.
 
Explain Cat vs more command
cat (concatenate):
Purpose: Displays the content of files and concatenates them.
Functionality: Outputs the entire content of a file to the terminal.
Usage Example: cat filename.txt - Displays the full content of filename.txt.
more:
Purpose: Displays the content of files one screen at a time.
Functionality: Allows for paginated viewing of long text files, enabling scrolling through the content.
Usage Example: more filename.txt - Displays the content of filename.txt one screen at a time.
Summary:
cat is used to quickly display the full content of a file.
more is used to view the content of a file one page at a time, which is useful for long files.
