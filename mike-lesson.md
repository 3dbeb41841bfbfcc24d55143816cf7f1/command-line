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

* __Terminal__ : a program on a MAC that launches a window from which we can work with the computer via a command line interface (CLI).
* __Command Line Interface__ : an text-based User Interface for typing text commands and reading text results
* __REPL__ : a program that interacts with the user via a _R_ead, _E_valuate, _P_rint, _L_oop. The REPL offers a prompt to the user where the user enters a command. Then the REPL _R_eads the command, _E_valuates (interprets and executes) the command, _P_rints the results, and _L_oops (thus displaying the prompt to the user again. REPL's are the ultimate servants waiting to do whatever you command them to do!
* __Shell__ : a REPL that offers a set of general purpose commands for computer administration, launching programs, process management, and file system management. Just as we have many programming languages we can choose from, there are many shells as well. Common shells are `sh`, `bsh`, `csh`, `ksh`, `bash`, and `zsh`. We will be using the `bash` shell in this class.
  - `sh` or Bourne Shell: the original shell still used on UNIX systems and in UNIX-related environments.
  - `bash` or Bourne Again shell: the standard GNU shell, intuitive and flexible. Probably most advisable for beginning users while being at the same time a powerful tool for the advanced and professional user.
  - `csh` or C shell: the syntax of this shell resembles that of the C programming language. Sometimes asked for by programmers.
  - `tcsh` or TENEX C shell: a superset of the common C shell, enhancing user-friendliness and speed. That is why some also call it the Turbo C shell.
  - `ksh` or the Korn shell: sometimes appreciated by people with a UNIX background. A superset of the Bourne shell.
  - `zsh`: another popular shell that is derived from the Bourne Shell.

* Process - a program that is currently running on the computer
* Application - a program that consists of one or more processes

> Generally speaking a process may be running in the background while an Application (which consists of one or more processes) has a visible UI.

## The BASH Shell

## prompt
* customizing your prompt
* liquid prompt

## env variables
* PATH
* the `path` command

## scripts

## interacting with the file system
* ls, cd, mkdir, pwd, rmdir, touch, rm

## managing processes
* ps, top, Activity Monitor

## file permissions
* chown, chmod, rwx
* permissions for directories vs. files

## Important configuration files
* ~/.bash_profile
* ~/.bashrc

Why 2 files?

* .bash_profile is executed for login shells
* .bashrc is executed for interactive non-login shells

NOTE: files that begin with a dot are considered `hidden` files in that they are not commonly viewed by the user. You can always view them if needed with the `ls -a` command.

## Command line basics
  * UNIX command format: `command --flag1 --flag2 arguments`
  * The PATH
    - the `which` command vs. the BASH `type -a` command
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
* [BASH Beginner's Guide](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/)
