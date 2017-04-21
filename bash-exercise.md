## Bash Exercises

This is just a few ideas for handy scripts that could be done as exercises for getting more experience in bash scripting. If you look through the reference material you will find more exercises.

1. **Archiving script** - Write a script that take two paths as parameter. Everyting under the first path should be compressed and saved to the second path. The compressed file should have a timestamp as a name.


```bash
# compress everything under ~/doc and put the compressed file in ~/archive
./archiving.sh ~/doc ~/archive
```

2. **git pull recursive** - Write a script that takes a path as a parameter and search for git-repositories (directoris containing a ".git-directory") and make a git pull on theses. This script should be good when working in many repositories with other people. Ypu could probobly find many more things to script involving git.
