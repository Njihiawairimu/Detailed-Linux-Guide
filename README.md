# Detailed-Linux-Guide
This is Basic Linux Guide — your quick-start resource to navigating and using Linux effectively as a beginner!

## :spanner: What is Linux?
Linux is a family of open-source, Unix-like operating systems built around the Linux kernel

## Linux Distros
- Ubuntu 
- Arch Linux
- CentOS
- Red Hat
- Parrot OS
- Peppermint OS

## What is terminal?
It's a text-based interface that allows users to interact with the operating system by entering commands
Also known as **command line interface or CLI**

- Start the terminal by pressing `ctrl + ALT + T`
- Use `TAB` to autocomplete directory/file names
- use the `↑` to access previous commands

## File Directory Management

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
Removes or deletes files and directories from the file system. It permanently deletes data, so caution is advised.

- `touch`
Creates an empty file with the specified name. It can also be used to update the timestamp of existing files.

- `clear`
Clears all previous output on the terminal screen, giving a clean slate for new commands.

