---
course_slug: linux-bash-for-beginners
tutorial_number: 3
type: note
---
To remove a file in the terminal use the `rm` command.

List the contents of the current working directory using the `ls` command.
In this example there is a `index.html` file.  To remove this file use the `rm` command.
```bash
$ ls
index.html

$ rm index.html
$ ls

```

To remove directories and their contents use the `rm` command with the `-R` argument
```bash
$ ls 
node_modules
$ rm -R node_modules
$ ls

```

To see what has been deleted add the  `-v` argument to the `rm` command.
```bash
$ ls 
node_modules
$ rm -Rv node_modules
node_modules/bin
node_modules

```
Notice that the `node_modules` and `bin` directories have been removed.

Use the `*` symbol to only remove the contents of a directory

```bash
$ rm -Rv node_modules/*
node_modules/bin

$ ls 
node_modules
$ ls node_modules/

```
In this example only the contents of node_modules is removed.  The node_modules directory is kept.

Warning do not run the following as this will remove everything from the root directory if you have the correct permissions.

```bash
$ rm -Rv /
```
