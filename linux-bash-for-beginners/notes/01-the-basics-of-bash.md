## Printing the current working directory
To print the current directory used the `pwd` command.
```bash
$ pwd
```

## Changing directory

To move around the Linux file system in the terminal use the `cd` command followed by either an absoulte path to the destination or a relative path to the current wordking directory.

To go to the root directory of the file system
```bash 
$ cd /
```

To go to the public directory within my_project directory which is held in the current working directory
```bash
$ cd my_project/public
```
To go to the home directory
```bash
$ cd ~/
```

Use `~` to start the cd  command from the current home directory
```bash
$ cd ~/code
```

## Listing directory contents

Use the `ls` command to list the contents of the current working directory

```bash
$ ls
```


## Creating directories
Use the `mkdir` command to create a directory

To create a directory called code in the current working directory
```bash
$ mkdir code
```

To create code in the home directory
```bash
$ mkdir ~/code
```