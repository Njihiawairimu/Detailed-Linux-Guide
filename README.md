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
ls -l # Long listing format
ls -a # Shows hidden files
ls -lh # Lists in human readable format
```

- `pwd`
Prints the full path of the current working directory.

- `cd`
Changes the current directory to a different one specified by the user.

- `mkdir`
Creates a new directory or folder.

```bash
mkkdir <directory_path>
mkdir -p <directory path> # Create parent directory
```

- `mv`
Moves files or directories from one location to another. It can also be used to rename files or directories.
```bash
mv file.txt /Desktop/Documents # Move file
mv file.txt lucy.txt # Rename file
```

- `cp`
Copies files or directories from one location to another, while leaving a copy of the same file. 
```bash
cp file.txt /desktop # Copying to another destination
```

- `rm`
Removes or deletes files and directories from the file system.
```bash
rm file.txt # Deletes a file
rm -r lucy # Deletes a directory and its contents recursively
rm -i file.txt # Prompts before deletion
```

- `touch`
Creates an empty file with the specified name. It can also be used to update the timestamp of existing files.

```bash
touch new_file.txt
```

- `clear`
Clears all previous output on the terminal screen, giving a clean slate for new commands.

## 📁 Viewing and Editing Files

This section introduces commands used to view, edit, and understand file contents in the terminal.

- `cat`
Displays the contents of a file directly in the terminal. 

> It reads the file from beginning to end and outputs the content.

- `echo`
Prints text to the terminal.

```bash
echo "Hello world!"
echo "It's a new day!" > new_file.txt # Writes the text into the new_file.txt file
```

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
```

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

- `which`
Similar to `whereis`, but only shows one file path

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

## System Monitoring & Performance

### A. CPU, Memory & Process Usage commands

- `top`
  Monitor real-time system activity
- `htop`
  Returns enhanced interactive process viewer 
  To install, run `sudo apt install htop`
- `vmstat`          
  This reports on memory, CPU, and IO
- `free -h`        
  Displays memory usage in human-readable format
- `uptime`          
  Shows how long the system has been running

### B. Disk Usage & IO

- `df -h`           
    Checks disk space usage per filesystem
- `du -sh *`        
    Checks space used by directories/files in current path
- `iostat`          
    Checks CPU & IO statistics 
    To install, run `sudo apt install sysstat`

### C. Network Monitoring

- `ip a`            
    Show network interfaces
- `ss -tuln`        
    Display listening ports
- `ping <ip_address>`      
    Test connectivity of websites or servers
    Example:
    ```bash
    ping 20.180.98.233
    ```
- `traceroute <ip_address>`   
    Trace route to host
    ```bash
    traceroute 20.180.98.233
    ```
## User Management
### A. Add, delete or review user details
These permissions might need elevated permissions, so make sure to use `sudo`.

- `adduser`

  Create new user and home directory
  ```bash
  sudo adduser <user_name>
  ```

- `deluser`

    Delete user
    ```bash
    sudo deluser <user_name>
    ```

- `finger` (Yeah, yeah I know :) )

  Review and check a user's details
  Make sure you have installed `finger` using `sudo apt install finger`

  ```bash
  finger <user_name>
  ```

- `passwd`

  Set a password or edit a user's password.
  ```bash
  passwd <user_name>
  ```

- `whoami`

  Check the current user
  ```bash
  whoami 
  ```

- `su`

  Switch to the specified user

  ```bash
  su <user_name>
  ```

Other commands include:

```bash
cat /etc/passwd                 # List of all users
cat /etc/group                  # List of groups
id <user>                       # Show user's UID, GID, groups
who                             # Who is logged in
```

## File Permissions & Ownership

### A. Changing permissions
The `chmod` command in Unix-like operating systems is used to change the access permissions of files and directories. It allows you to control who can read, write, and execute (or search in the case of directories) files or directories. The name "chmod" is short for "change mode". 

Here are symbolic notations that can be used together with `chmod`:
- u: User (owner)
- g: Group
- o: Others 
- +: Add permission
- -: Remove permission
- =: Set permission exactly 
- r: Read
- w: Write
- x: Execute.

Here are some of the numeric notations that can be used to grant permissions:
- 4: Read
- 2: Write
- 1: Execute 
- 0: No permission

The numbers are combined to represent combined permissions (e.g., 7 is 4+2+1 which means a combination of read, write, and execute permissions)

> NOTE: Be very careful when running `chmod 777` as this give read, write and execute permissions to all users.

Example usage:

```bash
chmod u+x <filename> #Adds execute permission for the owner of the file.

chmod g-r <filename> # Removes read permission for the group of the file.

chmod 755 <filename> #Sets permissions to rwxr-xr-x (owner can read, write, and execute; group and others can read and execute).

chmod 644 <filename> #Sets permissions to rw-r--r-- (owner can read and write; group and others can read only).
```
### B. Changing Ownership

The chown command in Unix-like operating systems is used to change the owner and group of files and directories. It's a crucial command for managing file permissions and access control. The basic syntax is chown [options] owner[:group] file(s), where owner can be a user name or user ID, and group can be a group name or group ID.

Example usage:

```bash
chown john:users example.txt
chown -R jane:developers directory_name
```

> NOTE: ONLY the superuser (root) or a user with appropriate privileges can change the ownership of a file or directory. 