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

>> It reads the file from beginning to end and outputs the content.


- `echo`
Prints text to the terminal.

- `less`
Allows scrolling through the contents of a file one page at a time.

>> Use spacebar to move forward, q to quit

- `man`
Displays the manual page for a specified command. 
```bash 
man ls
```

- `head`
Displays the first few lines of a file.

- `tail`
Shows the last few lines of a file.

- `sort`
Arranges lines of a file or input in a specific order, usually alphabetically or numerically.





