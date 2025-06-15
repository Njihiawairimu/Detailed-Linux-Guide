# Detailed-Linux-Guide
This is Basic Linux Guide — your quick-start resource to navigating and using Linux effectively as a beginner!

## 🔧 What is Linux?
Linux is a family of open-source, Unix-like operating systems built around the Linux kernel

## 🖥️ Linux Distros
- Ubuntu 
- Arch Linux
- CentOS
- Red Hat
- Parrot OS
- Peppermint OS

## 💻 What is terminal?
It's a text-based interface that allows users to interact with the operating system by entering commands
Also known as **command line interface or CLI**

> Tips:
- Start the terminal by pressing `ctrl + ALT + T`
- Use `TAB` to autocomplete directory/file names
- use the `↑` to access previous commands

## 📁 File Directory Management

Here's how to navigate and manage files/folders from the terminal:

- `ls`
Lists the contents of a directory, such as files and subdirectories.
```bash
ls -l --long listing format
ls -a shows hidden files
ls -lh lists in human readable format
```

- `pwd`
Prints the full path of the current working directory.

- `cd`
Changes the current directory to a different one specified by the user.

- `mkdir`
Creates a new directory or folder.
```bash
mkdir -p <directory path> -- create parent directory
```

- `mv`
Moves files or directories from one location to another. It can also be used to rename files or directories.
```bash
mv file.txt /Desktop --move file
mv file.txt lucy.txt --renme file
```

- `cp`
Copies files or directories from one location to another. 
```bash
cp file.txt /desktop -- copying to another destination
```

- `rm`
Removes or deletes files and directories from the file system.
```bash
rm file.txt --deletes a file
rm -r lucy -- deletes a directory and its contents recursively
rm -i file.txt --prompts before deletion
```

- `touch`
Creates an empty file with the specified name. It can also be used to update the timestamp of existing files.

- `clear`
Clears all previous output on the terminal screen, giving a clean slate for new commands.

## 📁 Viewing and Editing Files

This section introduces commands used to view, edit, and understand file contents in the terminal.

- `cat`
Displays the contents of a file directly in the terminal. 

> It reads the file from beginning to end and outputs the content.

- `echo`
Prints text to the terminal.

- `less`
Allows scrolling through the contents of a file one page at a time.

> Use spacebar to move forward, q to quit

- `head`
Displays the first few lines of a file.

- `tail`
Shows the last few lines of a file.

- `sort`
Arranges lines of a file or input in a specific order, usually alphabetically or numerically.

## 🧾 File Comparison

These commands are used for comparing files and directories

- `diff`
Compares two text files line by line and highlights differences.
```bash
diff file.txt lucy.txt
```
> `vimdiff` - Displays side-by-side visual differences between files using the Vim editor interface
> `colordiff` - Provide syntax-colored output for better readability

- `cmp`
Compares two files byte by byte
```bash
cmp file.txt lucy.txt
```
- `comm`
Compares two sorted files
```bash
comm file1.ipynb file2.ipynb
```
> Files must be sorted before using

## 📦 Archives & Compression in Linux

These commands are used for creating, extracting, and managing archived and compressed files

- `zip`
Compresses files into a zip archive
```bash
`zip archive.zip file1.ipynb file2.ipynb`
```

- `unzip`
Decompresses files from a zip archive
```bash
`unzip archive.zip file1.ipynb file2.ipynb`

## 🔍 Searching Commands

These commands help you find specific files, directories or content within files.

- `find`
Searches for files and directories based on criteria such as name, type or modification date.
```bash 
find *.md -- find all .md files
```

- `grep`
Searches for specific patterns or text within files.
```bash
grep 'linux' app.py -- searches for the text Linux in that file
grep -r 'linux' /Desktop/Detailed-Linux-Guide -- searches the directory recursively
```

- `locate`
Finds files and directories by name using a pre-built index (database of all file paths on your system).
```bash
locate *.py
```

- `whereis`
Displays the location of the binary, source and manual files for a given command. It helps locate where software is installed.

## 📦 Package Management Commands

These commands are used for managing software packages
> `apt` means Advanced Package Tool

- `sudo apt update` 
Updates the package list

- `sudo apt upgrade`  
  Installs available updates for all installed packages.
  
- `sudo apt install python3`  
  Installs a package.

- `apt list --installed`  
  Lists all installed packages.

- `sudo apt remove python3`  
  Removes a package 

> ** Notes **
- CentOS - Replaces `apt` with `yum`
- Red Hat - Replaces `apt` with `rpm`
- Fedora - Replaces `apt` with `dnf`
- Arch Linux - REplaces `apt` with `pacman`

## 🖥️ UNIX System Name & Identification Commands

These commands are used for retrieving system name, kernel version, machine type, and other environment information

- `uname`  
  Prints the kernel name (e.g., Linux).
  
- `uname -a`  
  Prints all available system info: kernel name, hostname, kernel version, etc.
  
- `uname -r`  
  Shows the kernel release version.
  
- `uname -s`  
  Shows the kernel name.
  
- `uname -n`  
  Shows the network node hostname.
  
- `uname -m`  
  Displays machine hardware name (e.g., x86_64).
  
- `uname -p`  
  Displays processor type.
  
- `uname -v`  
  Shows kernel version details.

## 📡 Networking

These commands are used for networking tasks such as checking IP addresses, diagnosing connections, testing ports, and managing interfaces

- `ssh` - Secure Shell
Connets to a remote server securely
```bash
ssh <username>@<hostname>
```
- `ip` 

Replaces the older `ifconfig`(Interface Configuation) command.
- `ip a` or `ip addr`  
    Lists all IP addresses.

- `ip link`  
  Lists all network interfaces.
  
- `ip route`  
  Shows routing table.

- `traceroute`
Shows the path packets take to reach a network host.
```bash
`traceroute <hostname or IP>`
```
- `wget`
Download files from the internet.
```bash
`wget <URL>`
```

## ❓ Help Commands

These commands assist users in learning about other commands, their options and usage.

- `man`
Displays the manual (man page) for a command.

- `--help`
Used after a command to show a brief summary of its usage. It is a quick alternative to the full manual.

- `whatis`
Provides a one-line description of a command. 




