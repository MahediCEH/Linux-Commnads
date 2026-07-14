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

#### [📦 Package Management](#-1-package-management)
#### [📁 Navigation & File Management](#-2-navigation--file-management)
#### [📄 Text Processing & Viewing](#-3-text-processing--viewing)
#### [👤 User & Permission Management](#-4-user--permission-management)
#### [🌐 Networking & Firewalls](#-5-networking--firewalls)
#### [⚙️ Process & System Information](#%EF%B8%8F-6-process--system-information)
#### [💾 Storage, Archive & Compression](#-7-storage-archive--compression)
#### [🛡️ Security Tools](#%EF%B8%8F-8-security-tools)
#### [📂 Linux System Directories](#-9-linux-system-directories)
#### [🖥️ General Linux Commands](#%EF%B8%8F-10-general-linux-commands)

---

## Command Reference

This section provides a categorized collection of essential Linux commands with concise descriptions and practical examples. Use it as a quick reference while learning Linux or working in cybersecurity.

---

## 📦 1. Package Management

Package management commands are used to install, update, upgrade, remove, and manage software packages on Linux systems.

| Command | Description | Example |
|---------|-------------|---------|
| `apt update` | Updates the local package index from the configured repositories. It does not install or upgrade any packages. | `sudo apt update` |
| `apt upgrade ` | Upgrades all installed packages to their latest available versions without asking for confirmation. | `sudo apt upgrade -y` |
| `apt` | Debian-based package manager used to install, remove, search, and manage software packages. | `sudo apt install git` |

---

## 📁 2. Navigation & File Management

These commands are used to navigate the filesystem and perform common file and directory operations.

| Command | Description | Example |
|---------|-------------|---------|
| `pwd` | Displays the full path of the current working directory. | `pwd` |
| `ls` | Lists files and directories in the current location. | `ls` |
| `ls -la` | Lists all files and directories, including hidden files, in a detailed long format. | `ls -la` |
| `cd` | Changes the current working directory to another location. | `cd /Downloads` |
| `cp` | Copies one or more files or directories to another location. | `cp test.txt /Documents` |
| `mv` | Moves files and directories. | `sudo mv file.txt /Downloads` |
| `mv` | Renames files and directories. | `sudo mv old.txt new.txt` |
| `rm` | Removes files permanently. Use with caution. | `rm file.txt` |
| `rm -rf` | Removes directories permanently. Use with caution. | `rm -rf DirectoryName` |
| `mkdir` | Creates a new directory. | `mkdir myfolder` |
| `touch` | Creates a new empty file or updates the timestamp of an existing file. | `touch hello.txt` |
| `ln` | Creates hard links or symbolic links (shortcuts) between files. | `ln me.txt me2.txt` |
| `find` | Searches for files and directories based on name, type, size, permissions, or other criteria. | `find / -name "*.php"` |
| `locate` | Quickly finds files using a pre-built database. | `locate php.ini` |
| `which` | Displays the location of an executable command in the system's PATH. | `which python3` |
| `whereis` | Shows the binary, source code, and manual page locations of a command. | `whereis ssh` |
| `file` | Identifies the actual file type regardless of its extension. | `file image.png` |

---

## 📄 3. Text Processing & Viewing

These commands help you view, search, compare, edit, and manipulate text files directly from the terminal.

| Command | Description | Example |
|---------|-------------|---------|
| `cat` | Displays the entire contents of a file in the terminal. | `cat /etc/passwd` |
| `less` | Opens a file for interactive viewing, allowing you to scroll forward and backward. Ideal for large files. Use “q” to quit. | `less access.log` |
| `tail` | Views the end of a file. Most commonly used with -f to monitor log files in real time as new entries are added. | `tail log.txt` |
| `grep` | Searches for text or patterns within files using regular expressions. | `grep "admin" config.php` |
| `nano` | Opens the Nano terminal text editor for creating or editing files. | `nano config.txt` |
| `echo` | Prints text or variable values to the terminal or writes them to a file. | `echo "Hello World" >>file.txt` |
| `sort` | Sorts lines in a file alphabetically or numerically. | `sort names.txt` |
| `wc` | Counts the number of lines, words, and characters (or bytes) in a file. It's useful for quickly checking the size or contents of a text file. | `wc file.txt` |
| `uniq` | Removes or displays duplicate lines from a sorted file. It is commonly used to find unique entries in text data. | `uniq list.txt` |
| `cut` | Extracts specific columns or fields from each line of a file. It's useful for working with structured text like CSV files or `/etc/passwd`. | `cut -d: -f1 /etc/passwd` |
| `sed` | Edits text by searching and replacing words or patterns without opening the file in an editor. It is commonly used for automated text modifications. | `sed 's/http/https/g' file.txt` |
| `awk` | Processes and analyzes text files by working with columns and patterns. It's commonly used to extract, filter, and format data. | `awk '{print $1}' file.txt` |
| `xargs` | Converts input from standard input into command-line arguments for another command. It's useful for processing multiple files or items efficiently. | `cat list.txt \| xargs rm` |

---

## 👤 4. User & Permission Management

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
| `cut -d: -f1 /etc/passwd` | Show total users of the system. | `cut -d: -f1 /etc/passwd` |
| `userdel` | Delete any user account, except the currently logged-in user or accounts that are actively in use.. | `sudo userdel username` |

---

## 🌐 5. Networking & Firewalls

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
| `curl` | Transfers data to or from a server using various protocols. Commonly used for testing APIs and downloading content. | `curl https://example.com, curl ifconfig.me` |
| `wget` | Downloads files from the web using HTTP, HTTPS, or FTP. | `wget https://example.com/file.zip` |
| `ssh` | Securely connects to a remote machine over SSH. | `ssh root@10.0.0.1` |
| `ufw` | Manages firewall rules using Uncomplicated Firewall. | `sudo ufw enable` |
| `iptables` | Configures advanced Linux firewall and packet filtering rules. | `sudo iptables -L` |

---

## ⚙️ 6. Process & System Information

These commands help monitor running processes, manage system services, and display system information.

| Command | Description | Example |
|---------|-------------|---------|
| `ps aux` | Displays detailed information about all running processes on the system. | `ps aux \| grep apache` |
| `htop` | Shows a real-time view of running processes (to get the process ID), CPU usage, memory usage, and system performance. | `htop` |
| `kill` | Terminates a running process using its Process ID (PID). | `kill 1234` |
| `killall` | Terminates all processes with the specified name. | `killall firefox` |
| `service` | Starts, stops, restarts, or checks the status of a system service. | `service ssh status` |
| `uname -a` | Displays detailed information about the Linux kernel, system architecture, and hostname. | `uname -a` |
| `env` | Displays all current environment variables. | `env` |
| `export` | Creates or exports environment variables for the current shell session. | `export VAR=value` |
| `alias` | Creates a shortcut for a command or command sequence. | `alias ll='ls -la'` |
| `unalias` | Remove alias. | `unalias ll` |
| `man` | Opens the manual page for a command. | `man ls` |
| `whatis` | Displays a brief one-line description of a command. | `whatis nmap` |

---

## 💾 7. Storage, Archive & Compression

These commands help manage storage devices, mount filesystems, and create or extract archives.

| Command | Description | Example |
|---------|-------------|---------|
| `df` | Displays disk space usage for mounted filesystems in a human-readable format. | `df -h` |
| `mount` | Mounts a storage device or filesystem to a directory. | `mount /dev/sdb1 /mnt` |
| `vmhgfs-fuse` | Mounts a VMware shared folder inside a Linux virtual machine. | `sudo vmhgfs-fuse .host:/ /mnt/hgfs -o allow_other` |
| `tar` | Creates, extracts, or manages `.tar` archive files. | `tar -xvzf file.tar (extract), tar -czf backup.tar.gz Project/  (create zip)` |
| `zip` | Compresses files and directories into a ZIP archive. | `zip files.zip file1.txt` |
| `unzip` | Extracts files from a ZIP archive. | `unzip files.zip` |
| `unzip` | Compress file. | `gzip backup.sql` |

---

## 🛡️ 8. Security Tools

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
| `searchsploit` | Searches the local Exploit Database for publicly known exploits. Useful for finding exploits related to specific software versions. | `searchsploit apache 2.4` |
| `whatweb` | Identifies the technologies used by a website, such as its CMS, framework, server, and programming language. | `whatweb https://example.com` |
| `wafw00f` | Detects whether a website is protected by a Web Application Firewall (WAF). Helps identify security protections before testing. | `wafw00f https://example.com` |
| `ffuf` | Discovers hidden files, directories, virtual hosts, or parameters using wordlists. Commonly used during web application reconnaissance. | `ffuf -u https://example.com/FUZZ -w /usr/share/wordlists/dirb/common.txt` |
| `feroxbuster` | Recursively searches for hidden files and directories on web servers. Great for content discovery during security testing. | `feroxbuster -u https://example.com` |
| `enum4linux` | Collects information from Windows or SMB systems, including users, groups, and shared folders. | `enum4linux -a 192.168.1.10` |
| `smbclient` | Connects to Windows SMB file shares to browse, upload, or download files. | `smbclient //192.168.1.10/share` |
| `smbmap` | Lists available SMB shares and checks their access permissions on a remote Windows system. | `smbmap -H 192.168.1.10` |
| `netexec` | Performs enumeration and authentication testing against Windows and Active Directory environments. Formerly known as CrackMapExec. | `netexec smb 192.168.1.10` |
| `responder` | Captures authentication hashes on local networks by responding to common Windows name resolution requests. Use only in authorized environments. | `sudo responder -I eth0` |
| `impacket-*` | A collection of Python tools for interacting with Windows protocols and Active Directory services. | `impacket-psexec administrator@192.168.1.10` |
| `evil-winrm` | Opens a remote PowerShell session on a Windows machine using the WinRM service. | `evil-winrm -i 192.168.1.10 -u administrator -p Password123` |
| `bloodhound` | Maps relationships in Active Directory to help identify privilege escalation paths. | `bloodhound` |
| `certipy` | Finds and tests Active Directory Certificate Services (AD CS) for configuration issues. | `certipy find -u user -p password -dc-ip 192.168.1.10` |
| `amass` | Discovers subdomains using passive and active reconnaissance techniques. | `amass enum -d example.com` |
| `subfinder` | Quickly finds subdomains from public sources. Ideal for reconnaissance. | `subfinder -d example.com` |
| `dnsrecon` | Performs DNS enumeration to gather information about a domain and test DNS configurations. | `dnsrecon -d example.com` |
| `theHarvester` | Collects emails, hosts, IP addresses, and subdomains from public sources for OSINT. | `theHarvester -d example.com -b all` |
| `recon-ng` | A modular framework that automates Open Source Intelligence (OSINT) gathering. | `recon-ng` |
| `maltego` | A graphical OSINT tool used to visualize relationships between people, domains, emails, and other entities. | `maltego` |
| `masscan` | Extremely fast port scanner designed to scan large networks in a short time. | `masscan 192.168.1.0/24 -p80,443` |
| `nuclei` | Scans targets for known vulnerabilities using community-maintained templates. | `nuclei -u https://example.com` |
| `httpx` | Checks whether web servers are alive and collects information about HTTP and HTTPS services. | `httpx -u https://example.com` |
| `exiftool` | Displays and edits metadata stored in images, documents, videos, and other files. | `exiftool image.jpg` |
| `binwalk` | Analyzes firmware files and extracts embedded files or compressed data. | `binwalk firmware.bin` |
| `foremost` | Recovers deleted files from disk images using file carving techniques. | `foremost image.dd` |
| `steghide` | Hides or extracts secret data inside image and audio files using steganography. | `steghide extract -sf image.jpg` |
| `volatility3` | Analyzes memory dumps to investigate malware, running processes, and other forensic evidence. | `vol.py -f memory.raw windows.info` |
| `autopsy` | A graphical digital forensics platform for analyzing disk images and investigating evidence. | `autopsy` |
| `hashid` | Identifies the most likely algorithm used to generate a hash value. | `hashid 5f4dcc3b5aa765d61d8327deb882cf99` |
| `crunch` | Creates custom password wordlists based on specified length and character sets. | `crunch 8 8 abc123` |
| `cewl` | Crawls a website and builds a custom wordlist from the words it finds. | `cewl https://example.com -w words.txt` |
| `medusa` | Performs password auditing against various network services using username and password lists. | `medusa -h 192.168.1.10 -u admin -P passwords.txt -M ssh` |
| `bettercap` | A network attack framework used for tasks such as packet sniffing, spoofing, and Man-in-the-Middle testing. Use only with authorization. | `sudo bettercap -iface eth0` |
| `ettercap` | Performs Man-in-the-Middle (MITM) attacks for testing the security of local networks. | `sudo ettercap -G` |
| `aircrack-ng` | A suite of tools used to assess the security of Wi-Fi networks. | `aircrack-ng capture.cap` |
| `hashcat` | A high-performance password recovery tool that cracks password hashes using CPUs or GPUs. | `hashcat -m 0 hashes.txt rockyou.txt` |
| `dirb` | Brute-forces web directories and files to discover hidden content on a web server using a wordlist. Commonly used during web reconnaissance. | `dirb http://example.com/` |

---

## 📂 9. Linux System Directories

Understanding the Linux filesystem is essential for system administration and cybersecurity.

| Directory | Description |
|-----------|-------------|
| `/usr/bin` | Contains most executable programs and standard user commands available to all users. |
| `/usr/local/bin` | Stores locally installed or manually compiled executable programs that are not managed by the system package manager. |

---

## 🖥️ 10. General Linux Commands

These commands are commonly used for everyday Linux tasks, including terminal management, system information, command history, and user session monitoring.

| Command | Description | Example |
|---------|-------------|---------|
| `clear` | Clears the terminal screen without deleting command history. You can also press **Ctrl + L** to achieve the same result. | `clear` or `Ctrl + L` |
| `reset` | Resets the terminal to its default state, useful when the terminal becomes corrupted or unreadable. | `reset` |
| `exit` | Closes the current terminal session or exits the active shell. | `exit` |
| `reboot` | Restarts the Linux system safely. Root or sudo privileges are usually required. | `sudo reboot` |
| `shutdown` | Powers off the system safely after stopping running services. | `sudo shutdown now` |
| `history` | Displays the list of previously executed commands. | `history` |
| `history \| grep` | Searches the command history for a specific keyword or command. | `history \| grep ssh` |
| `!!` | Repeats the most recently executed command. | `!!` |
| `!123` | Executes the command with history number **123**. Replace `123` with the desired history number. | `!123` |
| `stat` | Displays detailed information about a file or directory, including size, permissions, timestamps, and ownership. | `stat file.txt` |
| `tree` | Displays files and directories in a tree-like hierarchical structure. | `tree -L 2` |
| `hostname` | Displays the system's hostname. | `hostname` |
| `hostnamectl` | Displays or manages the system hostname and related operating system information. | `hostnamectl` |
| `arch` | Displays the system's CPU architecture (for example, `x86_64`). | `arch` |
| `users` | Displays the usernames of users currently logged into the system. | `users` |
| `who` | Displays information about users currently logged in, including terminal sessions and login times. | `who` |
| `last` | Displays the login history of users by reading the system's login records. | `last` |

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
