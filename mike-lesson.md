https://github.com/ATL-WDI-Exercises/intro-to-command-line/blob/master/star_wars_command_line.md

# Terminal & Bash Basics

## Outline
* What is an Operating System?
* History of UNIX
* Advantages of the Command Line Interface
* The BASH shell
* Command line basics
* File System basics
* Processes

## What is an Operating System?
An operating system (OS) is a resource manager. It takes the form of a set of software routines that allow users and application programs to access system resources (e.g. the CPU, memory, disks, printers, network cards, etc.) in a safe, efficient and abstract way.

## History of UNIX
* The UNIX OS was originally created at Bell Labs by Ken Thompson and Dennis Ritchie back in 1969.
* It was released to the public in 1975.
* The Seventh Edition, released in 1978, marked a split in UNIX development into two main branches:
  - SYSV (System 5) - developed by AT&T and other commercial companies.
  - BSD (Berkeley Software Distribution) - arose from the University of California at Berkeley where Ken Thompson spent a sabbatical year.
* Apple Computer transitioned its origianal home grown operating system over to a BSD variant of UNIX in 2000 known as OSX.
* In 2007 OSX became a certified UNIX.
* Linux is a free open source UNIX OS for PCs that was originally developed in 1991 by Linus Torvalds, a Finnish undergraduate student.

## Advantages of the Command Line Interface
* More expressive:

    ls -als | sort -nr | head -5               # List the 5 largest files in the current directory
    find . -name '*.md' | xargs grep -i unix   # Search for Markdown files containing "unix"

* Faster: once you learn the commands, you can more efficiently get work done.
* Automation: you can create scripts that run a series of UNIX commands.

### Some TERMinology
* Terminal - the application that presents a command line interface to the user.
* Shell - a command line interpreter that executes the commands that the user types. Common shells are sh, bsh, csh, ksh, bash, and zsh (we will be using bash in this class)
* Process - a program that is currently running on the computer
* Application - a program that consists of one or more processes

## The BASH Shell
* Important configuration files
  - ~/.bash_profile
  - ~/.bashrc
* Why 2 files?
  - .bash_profile is executed for login shells
  - .bashrc is executed for interactive non-login shells

NOTE: files that begin with a dot are considered `hidden` files in that they are not commonly viewed by the user. You can always view them if needed with the `ls -a` command.

## Command line basics
  * UNIX command format: `command --flag1 --flag2 arguments`
  * The PATH
    - the `which` command vs. the BASH `type` command
    - `alias which='type -a`
  * Pipes and Redirection
    - `echo "Hello, WDI" > greeting.txt`
    - `ls -als | sort -nr | head`
    - `ls '*.md' | xargs grep -i wdi`

## File System basics
* directories / folders and files
* file types
* tree structure: parents and children
* UNIX commands for files and directories:
  - pwd, cd, ls, mkdir, rmdir
  - absolute vs. relative paths
  - $HOME and ~
  - touch, cat, more/less, cp, mv, rm
  - wildcards
  - File ownership
    * All files and directories belong to an owner and a group
    * The owner and the group have specific access to the file/directory
    * `chown <n*owner> files`
    * `chgrp <new-group> files`
  - File permissions
    * Read
      - File: user can view the contents of the file
      - Directory: user can list the files
    * Write
      - File: user can modify the contents of the file
      - Directory: user can create new files and remove existing files
    * Execute
      - File: user can use the file as a UNIX command
      - Directory: user can change into the directory
    * `chmod options files`

## Processes
* foreground and background processes
* process ID
* process input and output (stdin, stdout, stderr)
* The `ps` command

## References
* [Unix Intro Course](http://www.doc.ic.ac.uk/~wjk/UnixIntro/)
