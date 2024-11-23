# Linux 

### 1. What is Linux?
Linux is an open-source operating system kernel developed by Linus Torvalds in 1991. It's the core component of various Linux distributions (or distros) such as Ubuntu, Fedora, and Debian. Linux is known for its stability, security, and flexibility, making it popular for use in servers, desktop computers, mobile devices, and embedded systems. It supports a wide range of software and is highly customizable to meet different needs.

---

### 2. How to give permission to Linux? What is `chmod`?
`chmod` is a command in Linux used to change permissions for files and directories. It allows you to specify who can read, write, or execute a file or directory. You can use symbolic or octal notation to set permissions. 

- **Example 1**: `chmod u+x file.txt` adds execute permission for the owner of `file.txt`.
- **Example 2**: `chmod 755 file.txt` gives the owner full permissions and read/execute permissions to the group and others.

#### Permission Values:
- Read: 4
- Write: 2
- Execute: 1

---

### 3. What does "777" mean in Linux?
In Linux, `777` is a file permission notation representing full read, write, and execute permissions for the owner, group, and others.

---

### 4. Which Linux and Windows versions do you use?

- **Linux**:
  - **Ubuntu 18.x**: Decommissioned/not in use for 5–6 months.
  - **Ubuntu 22.04**: Recently used.
  - **Ubuntu 24.04**: Latest version – recently used.

- **Windows**:
  - **2019**: Recently used.
  - **2022**: Latest version.

> **Note**: Companies often avoid the latest version due to potential issues and typically use one version older than the latest.

---

### 5. What is the key difference between a Linux server and an Ubuntu server?

- **Linux Server**: Refers to any server operating system based on the Linux kernel. Examples include Ubuntu Server, CentOS, Debian, and Fedora. Each has unique features, package management, and support policies.
- **Ubuntu Server**: A specific Linux distribution tailored for server environments. It's based on Debian and maintained by Canonical, known for its ease of use, regular updates, and strong community support.

In essence, "Linux server" is a generic term, while "Ubuntu server" refers specifically to a server running the Ubuntu distribution.

---

### 6. What is a thread in Linux?
In Linux, a thread is a basic unit of execution within a process, capable of running tasks concurrently with other threads. Threads share the same memory and resources as their parent process, enabling efficient multitasking and parallel processing within applications.

---

### 7. What is a zombie process in Linux?
A zombie process in Linux is a terminated process that still has an entry in the process table because its parent process hasn't yet acknowledged its termination.

---

### 8. Explain the `grep` command.
The `grep` command in Unix/Linux is used to search for specific patterns within files. It stands for "Global Regular Expression Print." It is a powerful tool for searching through text files and displaying lines that match a given pattern.

---

### 9. What is the `/etc` folder?
The `/etc` folder is a key part of Linux and other Unix-like systems. It contains important settings and configuration files. 

- **Purpose**: Stores system-wide configuration files for software and the operating system.
- **Impact**: Changes in this folder affect the whole system, not just one user.

---

### 10. Difference between YUM and APT

#### YUM:
- **Distribution**: Used in RPM-based distributions like Red Hat, CentOS, and Fedora.
- **Package Format**: Handles `.rpm` files.
- **Repositories**: Configurations in `/etc/yum.repos.d/`.
- **Commands**: Examples include `yum install`, `yum update`, and `yum remove`.

#### APT:
- **Distribution**: Used in Debian-based distributions like Ubuntu and Debian.
- **Package Format**: Handles `.deb` files.
- **Repositories**: Configurations in `/etc/apt/sources.list`.
- **Commands**: Examples include `apt-get install`, `apt-get update`, and `apt-cache search`.

---

### 11. How to get info for all the packages installed on a Linux system?
- For RPM-based systems: `yum list installed`
- For Debian-based systems: `apt list --installed`

---

### 12. How to check the kernel version in Linux?
- `uname -r`: Outputs the kernel version.
- `cat /proc/version`: Displays the kernel version with additional build details.
- `hostnamectl`: Displays kernel and system information.

---

### 13. Explain Linux distribution.
A Linux distribution, often referred to as a "distro," is a complete operating system built on the Linux kernel, along with software applications, libraries, and utilities. Examples include Ubuntu, Fedora, CentOS, and Arch Linux.

---

### 14. How to backup a Linux server?
Common methods:
- **rsync**: Efficient for file synchronization and backups.
- **tar**: Creates compressed archive files.
- **dd**: Used for full disk backups.
- **Automation**: Use cron jobs for scheduling.

Advanced tools include:
- **rsnapshot**: For incremental backups.
- **Bacula and Duplicity**: For encrypted and remote backups.

---

### 15. How to check running processes in Linux? What is the use of `ps -aux` in Linux? What is the `top` command & its uses?

- **`top`**: Displays real-time system processes and summary.
- **`ps -aux`**:
  - `a`: Shows processes from all users.
  - `u`: Displays detailed user-oriented format.
  - `x`: Includes processes without a controlling terminal.

---

### 16. How to check system load in Linux?
- Use the `top` command to see real-time information about system load.
- **Load average**: Displays the load over the last 1, 5, and 15 minutes.

---

### 17. What is the inode number?
An inode number is a unique identifier for each file or directory in a Unix-based file system. It stores file metadata and allows efficient file access.

---

### 18. What is Nginx?
Nginx is a web server software known for its speed and efficiency in handling web traffic. It's commonly used as a reverse proxy, load balancer, and HTTP cache.

---

### 19. What is a Cron job in Linux?
A cron job is a scheduled task in Linux that runs at specified times or intervals. It's used for repetitive tasks like running scripts or system maintenance.

---

### 20. What is the `nslookup` command?
The `nslookup` command is a network utility for querying DNS servers for domain names, IP addresses, and other DNS records.

---

### 21. How to start a Linux server?
- Boot up via a virtual machine manager or power on a physical server.
- Log in using SSH or remote desktop.
- Verify status using commands like `uptime` or `systemctl status`.

---

### 22. Explain `grep` vs `sed` commands.
- **`grep`**: Searches and prints lines matching a pattern.
- **`sed`**: Edits and transforms text within files.

---

### 23. Explain `cat` vs `more` commands.
- **`cat`**: Displays the entire file content.
- **`more`**: Paginated viewing for long files.
