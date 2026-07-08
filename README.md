# Linux Command Handbook

> A practical collection of Linux commands that I'm learning throughout my cybersecurity journey.

This repository contains my personal notes, explanations, and examples of commonly used Linux commands for beginners, system administration, and ethical hacking.

---

## 📖 About

Linux is one of the most important skills in cybersecurity. This repository serves as my personal handbook while learning Linux and Kali Linux.

Rather than simply memorizing commands, my goal is to understand:

- What each command does
- When to use it
- Common options
- Real-world examples
- Best practices

---

## 📚 Topics Covered

#### 📦 Package Management
#### 📁 Navigation & File Management
#### 📄 Text Processing
### 👤 User & Permissions
### 🌐 Networking
### ⚙️ System Monitoring
### 💾 Storage & Archives
### 🛡️ Security Tools
### 📂 Linux Directory Structure

Let's deep dive.....

# 📦 1. Package Management

Package management commands are used to install, update, upgrade, remove, and manage software packages on Linux systems.

| Command | Description | Example |
|---------|-------------|---------|
| `apt update` | Updates the local package index from the configured repositories. It does not install or upgrade any packages. | `sudo apt update` |
| `apt upgrade -y` | Upgrades all installed packages to their latest available versions without asking for confirmation. | `sudo apt upgrade -y` |
| `apt` | Debian-based package manager used to install, remove, search, and manage software packages. | `sudo apt install git` |
| `pacman` | Default package manager for Arch Linux and its derivatives. It installs, updates, removes, and manages packages. | `sudo pacman -Syu` |
| `yum` | Package manager used in older RHEL, CentOS, and Fedora systems to manage software packages. | `sudo yum update` |
| `rpm` | Installs, verifies, queries, and removes RPM packages on Red Hat-based Linux distributions. | `rpm -i package.rpm` |

# 📁 2. Navigation & File Management

These commands are used to navigate the filesystem and perform common file and directory operations.

| Command | Description | Example |
|---------|-------------|---------|
| `pwd` | Displays the full path of the current working directory. | `pwd` |
| `ls` | Lists files and directories in the current location. | `ls -la` |
| `cd` | Changes the current working directory to another location. | `cd /var/www/html` |
| `cp` | Copies one or more files or directories to another location. | `cp file.txt /tmp/` |
| `mv` | Moves or renames files and directories. | `mv old.txt new.txt` |
| `rm` | Removes files or directories permanently. Use with caution. | `rm -rf test/` |
| `mkdir` | Creates a new directory. | `mkdir myfolder` |
| `touch` | Creates a new empty file or updates the timestamp of an existing file. | `touch hello.txt` |
| `ln` | Creates hard links or symbolic links (shortcuts) between files. | `ln -s /opt/app app` |
| `find` | Searches for files and directories based on name, type, size, permissions, or other criteria. | `find / -name "*.php"` |
| `locate` | Quickly finds files using a pre-built database. | `locate php.ini` |
| `which` | Displays the location of an executable command in the system's PATH. | `which python3` |
| `whereis` | Shows the binary, source code, and manual page locations of a command. | `whereis ssh` |
| `file` | Identifies the actual file type regardless of its extension. | `file shell` |
| `dd` | Copies and converts data at the block level. Commonly used for creating disk images and bootable USB drives. | `dd if=/dev/sda of=backup.img` |

# 📄 3. Text Processing & Viewing

These commands help you view, search, compare, edit, and manipulate text files directly from the terminal.

| Command | Description | Example |
|---------|-------------|---------|
| `cat` | Displays the entire contents of a file in the terminal. | `cat /etc/passwd` |
| `less` | Opens a file for interactive viewing, allowing you to scroll forward and backward. Ideal for large files. | `less access.log` |
| `head` | Displays the first 10 lines of a file by default. | `head file.txt` |
| `tail` | Displays the last 10 lines of a file by default. | `tail log.txt` |
| `grep` | Searches for text or patterns within files using regular expressions. | `grep "admin" config.php` |
| `nano` | Opens the Nano terminal text editor for creating or editing files. | `nano config.txt` |
| `vim` | Opens the Vim text editor, a powerful editor commonly used by Linux administrators. | `vim config.txt` |
| `echo` | Prints text or variable values to the terminal or writes them to a file. | `echo "Hello World"` |
| `diff` | Compares two files line by line and displays their differences. | `diff a.txt b.txt` |
| `cmp` | Compares two files byte by byte and reports the first difference found. | `cmp a.txt b.txt` |
| `comm` | Compares two sorted files and displays unique and common lines. | `comm a.txt b.txt` |
| `sort` | Sorts lines in a file alphabetically or numerically. | `sort names.txt` |

# 👤 4. User & Permission Management

These commands are used to manage users, groups, permissions, ownership, and administrative privileges.

| Command | Description | Example |
|---------|-------------|---------|
| `whoami` | Displays the username of the currently logged-in user. | `whoami` |
| `id` | Shows the current user's UID, GID, and group memberships. | `id` |
| `sudo` | Executes a command with superuser (root) privileges. | `sudo apt update` |
| `sudo -l` | Lists the commands the current user is allowed to execute with sudo. | `sudo -l` |
| `sudo su` | Switches to the root user shell if the user has sufficient privileges. | `sudo su` |
| `useradd` | Creates a new user account. | `sudo useradd admin` |
| `passwd` | Creates or changes a user's password. | `passwd user` |
| `chmod` | Changes file or directory permissions. | `chmod 755 script.sh` |
| `chown` | Changes the ownership of a file or directory. | `chown root file.txt` |

# 🌐 5. Networking & Firewalls

These commands are used to configure, troubleshoot, and secure network connections.

| Command | Description | Example |
|---------|-------------|---------|
| `ping` | Tests network connectivity by sending ICMP echo requests to a host. | `ping google.com` |
| `ifconfig` | Displays or configures network interface settings (legacy command). | `ifconfig` |
| `ip a` | Displays detailed network interface and IP address information. | `ip a` |
| `netstat` | Displays active network connections, routing tables, and listening ports (legacy command). | `netstat -tuln` |
| `ss` | Displays socket statistics and network connections. A modern replacement for `netstat`. | `ss -tuln` |
| `nmap` | Scans hosts, ports, and services to identify network vulnerabilities. | `nmap -sV 192.168.1.1` |
| `traceroute` | Shows the path packets take from your computer to a destination host. | `traceroute google.com` |
| `dig` | Retrieves detailed DNS information for a domain. | `dig example.com` |
| `nslookup` | Queries DNS servers to obtain domain or IP address information. | `nslookup example.com` |
| `curl` | Transfers data to or from a server using various protocols. Commonly used for testing APIs and downloading content. | `curl https://example.com` |
| `wget` | Downloads files from the web using HTTP, HTTPS, or FTP. | `wget https://example.com/file.zip` |
| `ssh` | Securely connects to a remote machine over SSH. | `ssh root@10.0.0.1` |
| `ufw` | Manages firewall rules using Uncomplicated Firewall. | `sudo ufw enable` |
| `iptables` | Configures advanced Linux firewall and packet filtering rules. | `sudo iptables -L` |

# ⚙️ 6. Process & System Information

These commands help monitor running processes, manage system services, and display system information.

| Command | Description | Example |
|---------|-------------|---------|
| `ps aux` | Displays detailed information about all running processes on the system. | `ps aux \| grep apache` |
| `top` | Shows a real-time view of running processes, CPU usage, memory usage, and system performance. | `top` |
| `kill` | Terminates a running process using its Process ID (PID). | `kill 1234` |
| `killall` | Terminates all processes with the specified name. | `killall firefox` |
| `service` | Starts, stops, restarts, or checks the status of a system service. | `service ssh status` |
| `uname -a` | Displays detailed information about the Linux kernel, system architecture, and hostname. | `uname -a` |
| `env` | Displays all current environment variables. | `env` |
| `export` | Creates or exports environment variables for the current shell session. | `export VAR=value` |
| `history` | Displays the list of previously executed commands. | `history \| grep nmap` |
| `cal` | Displays a calendar in the terminal. | `cal` |
| `alias` | Creates a shortcut for a command or command sequence. | `alias ll='ls -la'` |
| `man` | Opens the manual page for a command. | `man ls` |
| `whatis` | Displays a brief one-line description of a command. | `whatis nmap` |

# 💾 7. Storage, Archive & Compression

These commands help manage storage devices, mount filesystems, and create or extract archives.

| Command | Description | Example |
|---------|-------------|---------|
| `df` | Displays disk space usage for mounted filesystems in a human-readable format. | `df -h` |
| `mount` | Mounts a storage device or filesystem to a directory. | `mount /dev/sdb1 /mnt` |
| `vmhgfs-fuse` | Mounts a VMware shared folder inside a Linux virtual machine. | `sudo vmhgfs-fuse .host:/ /mnt/hgfs -o allow_other` |
| `tar` | Creates, extracts, or manages `.tar` archive files. | `tar -xvf file.tar` |
| `zip` | Compresses files and directories into a ZIP archive. | `zip files.zip file1.txt` |
| `unzip` | Extracts files from a ZIP archive. | `unzip files.zip` |

# 🛡️ 8. Security Tools

These are common cybersecurity and penetration testing tools frequently used in Kali Linux.

| Command | Description | Example |
|---------|-------------|---------|
| `msfconsole` | Launches the Metasploit Framework console for penetration testing and exploit development. | `msfconsole` |
| `hydra` | Performs password auditing against various network services using dictionary or brute-force attacks. | `hydra -l admin -P pass.txt ssh://192.168.1.10` |
| `john` | Cracks password hashes using dictionary, brute-force, or rule-based attacks. | `john --wordlist=rockyou.txt hash.txt` |
| `nikto` | Scans web servers for common security vulnerabilities and misconfigurations. | `nikto -h http://target.com` |
| `sqlmap` | Automates the detection and exploitation of SQL injection vulnerabilities on authorized web applications. | `sqlmap -u "http://site.com?id=1" --dbs` |
| `burpsuite` | Starts Burp Suite, a GUI-based platform for web application security testing. | `burpsuite` |
| `dirb` | Performs directory and file brute-force scanning on web servers. | `dirb http://target.com` |
| `gobuster` | Discovers hidden directories, files, virtual hosts, or DNS subdomains using wordlists. | `gobuster dir -u http://site.com -w wordlist.txt` |
| `wireshark` | Launches Wireshark for capturing and analyzing network traffic. | `wireshark` |

# 📂 9. Linux System Directories

Understanding the Linux filesystem is essential for system administration and cybersecurity.

| Directory | Description |
|-----------|-------------|
| `/usr/bin` | Contains most executable programs and standard user commands available to all users. |
| `/usr/local/bin` | Stores locally installed or manually compiled executable programs that are not managed by the system package manager. |

---

## 📜 Handbook Preview

Click the image below to view the complete handbook.

---

## 🎯 Purpose

This project is part of my cybersecurity learning journey.

It helps me:

- Practice Linux daily
- Understand command-line tools
- Build a personal knowledge base
- Prepare for penetration testing
- Improve system administration skills

---

## ⚠️ Disclaimer

Some commands in this repository can modify or delete files, change system configurations, or interact with security tools. Always practice in a safe and authorized environment such as a virtual machine or lab.
