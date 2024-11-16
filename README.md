This is a learning objective about Linux, from [Linnaeus University](http://lnu.se), Kalmar, Sweden.
This work is licensed under [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/)

This work is intended for the students in the [UDM - Utvecklare och drift av mjukvarusystem](https://coursepress.lnu.se/program/utveckling-och-drift-av-mjukvarusystem/student/) and the [WP - Webbprogrammerare](http://webbprogrammerare.se) programs.
This is not a complete course in Linux but just an introduction for program students at [Linnaeus University](www.lnu.se), Kalmar, Sweden

**All video recording will be in Swedish**

This content is concentrated to server versions of the Ubuntu distributions.

## Goal
The student should get an understanding of the Linux system and its characteristics. The student will also get some experience in using bash commands, text editors and bash scripting.

## About this learning object
[Video on youtube](https://www.youtube.com/watch?v=Cb5ij5VMyzk) - Explains this learning object

### Linux - an introduction 

[Video on youtube](https://www.youtube.com/watch?v=K81c6R2COmI) - A short introduction to Linux, it's history and use today ([Slides](https://rawgit.com/CS-LNU-Learning-Objects/linux/master/slides/introduction.html))

In the video [Vagrant](https://www.vagrantup.com/) and [Virtual box](https://www.virtualbox.org/) are used for running virtual machines with Ubuntu and CentOS. 

If you have docker installed and running you could start use these commands to start up instances:

```bash
docker run -it ubuntu /bin/bash   # runs and starts a ubuntu container
docker run -it centos /bin/bash   # runs and starts a centos container
```

If you do not have Docker installed, this is a perfect time to install it. You find Docker Desktop at [https://www.docker.com/get-started](https://www.docker.com/get-started)

### The shell

[This text document](https://github.com/CS-LNU-Learning-Objects/linux/blob/master/commands.md)) gives an introduction to a Linux system shell. It will also link to a Cheat Sheet with different commands you should study. At the end of the text there are some exercises to practice on.

### Using the terminal, text editors

[Video on youtube](https://www.youtube.com/watch?v=623APOnLtJE) - Showing how to work with the shell and some of its text editors

#### Resources on the text editors

  * https://www.howtogeek.com/howto/42980/the-beginners-guide-to-nano-the-linux-command-line-text-editor/
  * https://www.linux.com/learn/vim-101-beginners-guide-vim

### Package management

[Video on youtube](https://www.youtube.com/watch?v=ekVqif-vKK0) - A short video how to update your system and how to install new packages/applications

### Users, Permissions, Groups

  Be sure to [read this article](https://www.linode.com/docs/tools-reference/linux-users-and-groups) to get the theoretical view of how Linux is handling files, directories, users and permissions

[Video on youtube](https://www.youtube.com/watch?v=WKNCQAMzBV0) - Some example of user/groups handling in Linux

### Introduction to Bash scripting

  * A short introduction - [Video](https://www.youtube.com/watch?v=aGQQBefu5Uc)
  * A simple example of a script - [Video](https://www.youtube.com/watch?v=H1b9dVDz2TE&feature=youtu.be)
  * Some ideas for exercise scripts - [Text](https://github.com/CS-LNU-Learning-Objects/linux/blob/master/bash-exercise.md)

#### Resources for bash

  The net is full of different pages about bash scripting. A good start is the three links below. Since you all know about programming; what a selection statement and a loop is for example we are more into studying the syntax. Especially the "part 1" and "part 2" is good for this. The third part have some good examples of bash scripts though. Start by reading these guides.

* Bash programming tutorial from developer
  * [Part 1](https://www.funtoo.org/Bash_by_Example,_Part_1)
  * [Part 2](https://www.funtoo.org/Bash_by_Example,_Part_2)
  * [Part 3](https://www.funtoo.org/Bash_by_Example,_Part_3)

 There is much more to learn if you want. Here are some extra resources. It could also come in handy to have a reference page when you have to look up stuff.

  * [Bash Reference Manual](https://www.gnu.org/software/bash/manual/bash.html) <- for references use
  * [Bash Guide for Beginners](https://web.archive.org/web/20230624030500/https://www.howtogeek.com/42980/the-beginners-guide-to-nano-the-linux-command-line-text-editor/)

  * [Bash programming introduction (from 2000)](http://en.tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html)
  * [Advanced Bash Scripting Guide](http://www.tldp.org/LDP/abs/html/)
  * [Collection of Bash Examples](http://www.fifi.org/doc/bash/examples/)

## More resources
To get a deeper understanding and get a searchable pdf during this learning object we recommend the following links:

  * [Linux Fundamentals by Paul Cobbaut](http://linux-training.be/linuxfun.pdf) - In English
  * [Att använda Linux och GNU by Linus Walleij](https://dflund.se/~triad/gnulinux/) - In Swedish


## Feel free to contribute
This content can always have higher quality. Help us to make it better. Fork it!
Make pull requests! All can help!

[Repository](https://github.com/CS-LNU-Learning-Objects/linux)

## Contact
Contact us through GitHub
