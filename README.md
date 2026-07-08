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

### 📦 Package Management
### 📁 Navigation & File Management
### 📄 Text Processing
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
