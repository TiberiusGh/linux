# Learning linux commands
This short text is suppose to give you a introduction to handling the terminal in Linux and learning some of the most common commands. This will not be done by us going through every single command and all it flags and parameters. The content of this module is:

- A short introduction to the shell
- A list with the commands you should be able to handle
- A video going through some commands and some text editors
- A number of exercises for you to try out on your own


## The shell
The shell, or the command line interpreter, is a vital tool in a Linux system. It is this program that interprets user commands (either written by the user of read from a script-file). This is the terminal, the promt, and this is the place you will spend most of your time when working with your Linux server.

There are different types of shells in the Linux/Unix-world.

- Bourne Shell (sh) - Developed at AT&T (Bell Laboratories). This is one of the oldest shell and where the name "shell" is from.
- Korn Shell (ksh), Almquist shell (ash), C-Shell (csh) are different kind of shells that all are different clones of the bourne shell.
- Bourne-Again Shell (bash) os the GNU-projects implementation and an extended version of the Bourne Shell. This is the most common shell and default on most systems.
- Z Shell (zsh) - contains a lot of the same features as bash but with a few difference like file globbing and spelling correction.

### Bash-files
We will be concentration on the bash shell since it is the default shell on most systems. One thing to notice when talking about your shell is the the system have some different files that can come in handy to know about. All these files are hidden files (having a dot in the beginning of the name) and could be revealed by the `ls -la` command.

- /bin/bash - the executable
- /etc/profile - The systemwide initialization file, first executed for login shells
- ~/.bash_profile - The personal initialization file, read by the /etc/profile (.bash_login or .profile if not found). Executed only on login.
- .bashrc - This file is executed every time a new instance of a bash shell is created, should be read by the .bash_profile (or similar)
- .bash_history - A list of all commands executed by this user
- .bash_logout - Executes when user logs out

More about this: http://mywiki.wooledge.org/DotFiles

## Linux commands
Enough about the shell it self. To be able to do something on the system you should be able to execute some commands. You have probably done this before by executing the cd-command for changing directory or the ls-command for listing files in the current directory. As said before this module is not going through all different commands. Some of them will be used in the demo videos but to understand them you have to do your own study. To help you along we will give you a link to a cheat sheet that have the most common commands written down. You should go through them (read about them with the man-command) and get use to them.

First of all you might want to look at the demos where I show you how to get a Ubuntu- and centOS-server up and running with vagrant. This will give you playing grounds when testing your commands. In the demo video I also talk about the man-command and something about the built-in text editors you can find in the Linux systems.

You find the cheat sheet here: https://files.fosswire.com/2007/08/fwunixref.pdf, it is CC-licensed from https://fosswire.com/post/2007/08/unixlinux-command-cheat-sheet/
