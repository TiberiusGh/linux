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

## stdin, stdout, stderr and pipes
One thing to know about when executing commands/programs in the bash-terminal is standard streams. In computer programming are standard streams pre-connected input and output. The **standard output (stdout)** is a place that a program can send information (like text). The program never know where this information goes. It could be a ordinary file, a printer or on the screen.

The **standard input(stdin)** is a place where a program gets information from. It never knows from where. It could be from a file, from the keyboard or from a output from another program. This makes it possible to pipe commands which means that you can combine to commands where the first program execution produces a stdout that the next program takes as stdin and processes. This goes well with the philosophy in Unix where you should have small programs with minimal features that are good at one thing. An example of this could be:

`ls -a | grep ba`

This list all files, which produces a stdout and by using the pipe-character (|) is sent to the grep command that takes it as stdin and outputs all files beginning with "ba".

`ps | grep bash | cut -d ' ' -f 2`

Of course you could pipe several times. The above command uses "ps" to list all processes on the system, filter them with "grep" to just show the bash process and use cut to just show the processID.

The **standard error (stderr)** is where eventual error messages are sent to.

The stdin, stdout and stderr are known as **file descriptors**. So when a program is executed these three file descriptors opens. 0 for stdin, 1 for stdout and 3 for stderr. We can use this with **redirection operators**. Here are some examples.

```bash
# writes the output of the /proc/cpuinfo into a file named cpu.txt
# it will be override
cat /proc/cpuinfo > cpu.txt

# The same but it will append info at the end of the file
cat /proc/cpuinfo >> cpu.txt

# Redirect the stderr to the file
cat /proc/nofile 2> cpu.txt

# reversed - on the grep command we redirect stdin from the filename
grep 'model name' < cpu.txt

# redirect stdout to cpu.txt and if there are a stderr to error.txt
cat /proc/nofile 1> cpu.txt 2> error.txt
```

## Exercises
After doing your homework with the commands and looking at the demo video you can try your knowledge out by doing this exercises:

1. In your home directory, create a directory called "dump" with a file called "test.txt". Open this file with an editor and write "I was here" in it.
2. Find a command that opens the file you created and write its content out to the standard output (eg. writing it out in your shell)
3. Find a command that appends the row "I was here to" to the file "test.txt"
4. Create a new folder called "dump2" at the same level as the directory "dump"
5. Find a command that makes a copy of the file "test.txt", that will get the name "test2.txt" and place it in the newly created directory ("dump2")
6. Remove the directory "dump" (including the "test.txt"-file)
7. In the "dump2"-directory rename the file test2.txt to test.txt
8. Create a new file called ".config". Create a gzip-file in your home directory with these two files (test.txt and .config) and name it archive.tar.gz
9. Remove the "dump2"-directory and it contents and remove the newly created compressed file
10. Use the netstat command to list all ESTABLISHED tcp ports in your system
11. Write a oneline-command that clones one github repository and creates a tar with Bzip compression with that git-folder. You may need to install "git" first using `sudo apt-get install git` or `sudo yum install git`

### Solution suggestions to above exercise
1.
```bash
# Go to home directory and make a directory
cd ~ && mkdir dump
touch dump/test.txt
# Use nano or vi for editing the file
```
2.
```bash
# whole file
cat dump/test.txt
# alternatives
less dump/test.txt
tail dump/test.txt
head dump/test.txt
```
3.
```bash
echo 'I was here to' >> dump/test.txt
```
4.
```bash
cd ~ && mkdir dump2
```
5.
```bash
cp dump/test.txt dump2/test2.txt
```
6.
```bash
rm -r dump
```
7.
```bash
mv dump2/test2.txt dump2/test.txt
```
8.
```bash
cd dump2
touch .config
tar czf ../archive.tar.gz .config test.txt
```
9.
```bash
cd ~
tar -xzvf archive.tar.gz -C .
```
10.
```bash
netstat -atn | grep ESTABLISHED
```
11.
```bash
git clone https://github.com/1dv031/syllabus && tar -cjvf backup.tar.bz2 syllabus -C .
```
